# Sub-theme

CivicTheme must never be modified directly. Your sub-theme inherits everything from CivicTheme and is where all custom work happens — overriding components, adding new ones, and adjusting styles. The build system merges your sub-theme's components with the base theme's components at compile time, so your overrides take priority automatically.

## Prerequisites

- CivicTheme installed and sub-theme generated (see [GovCMS SaaS installation](../../installation/govcms-saas.md) or [Drupal installation](../../installation/drupal-theme.md))
- NodeJS 22+ and NPM 10+ available
- Front-end assets built successfully (`npm run build`)

## Creating a sub-theme

CivicTheme provides a starter theme and a script to generate a child theme.

Run the following command from within the `civictheme` theme directory:

```shell
php civictheme_create_subtheme.php <theme_machine_name> "Human theme name" "Human theme description" /path/to/theme_machine_name
```

This generates a sub-theme in `path/to/theme_machine_name` with everything ready to be installed and compiled.

### Enabling the sub-theme

Enable the theme in UI or with Drush:

```sh
drush theme:enable theme_machine_name
```

### Compiling assets

Run the following command from within your sub-theme directory:

```sh
npm run build
```

{% hint style="info" %}
NodeJS version >=22 is required to compile front-end assets.
{% endhint %}

## Directory structure

The sub-theme creation script generates the following project scaffold:

```
<your_theme>/
├── .storybook/              # Storybook configuration
├── assets/                  # Static assets
│   ├── backgrounds/         # Background images
│   ├── fonts/               # Custom fonts
│   ├── icons/               # SVG icons
│   ├── logos/               # Theme logos
│   └── sass/                # Drupal-specific SCSS
│       ├── theme.scss       # Theme-level styles
│       └── theme.editor.scss # CKEditor5 styles
├── components/              # Component overrides and new components
│   ├── 00-base/             # Base layer (variables, mixins)
│   ├── 01-atoms/            # Atomic components
│   ├── 02-molecules/        # Molecule components
│   ├── 03-organisms/        # Organism components
│   ├── 04-templates/        # Page templates
│   ├── variables.base.scss       # Your base variable overrides
│   └── variables.components.scss # Your component variable overrides
├── dist/                    # Compiled output (generated)
├── templates/               # Drupal Twig template overrides
├── build.js                 # Build system script
├── vite.config.js           # Vite/Storybook configuration
├── package.json             # NPM dependencies and scripts
├── <theme_name>.info.yml    # Drupal theme declaration
└── <theme_name>.libraries.yml # Drupal asset libraries
```

### Key directories

- **`components/`** — where you override existing CivicTheme components or add new ones. The atomic design hierarchy (00-base through 04-templates) mirrors CivicTheme's own structure.
- **`assets/`** — where you place your site's logos, icons, fonts, and background images.
- **`templates/`** — where you add Drupal-specific Twig template overrides that map Drupal data to components.
- **`components/variables.base.scss`** and **`components/variables.components.scss`** — where you override CivicTheme's design tokens (colors, spacing, typography) without touching the base theme.

## Library system

Your sub-theme declares its compiled assets as Drupal libraries in `<theme_name>.libraries.yml`. The key library is `global`, which loads your compiled CSS and JavaScript on every page.

The sub-theme's `info.yml` file uses `libraries-override` to replace CivicTheme's compiled assets with your sub-theme's compiled assets. This is how the build system's merged output takes over from the base theme:

```yaml
libraries-override:
  civictheme/global:
    css:
      theme:
        dist/civictheme.base.css: dist/styles.base.css
        dist/civictheme.theme.css: dist/styles.theme.css
        dist/civictheme.variables.css: dist/styles.variables.css
    js:
      dist/civictheme.drupal.base.js: dist/scripts.drupal.base.js
```

You should not need to modify these library definitions unless you are adding entirely new Drupal libraries (separate from the component system).

## Placeholder assets

The starter kit ships with placeholder logos, backgrounds, and a screenshot. Replace these with your site's actual assets:

1. **Logos** — replace files in `assets/logos/`. CivicTheme supports multiple logo variants for header and footer, light and dark themes, and desktop and mobile sizes.
2. **Backgrounds** — replace files in `assets/backgrounds/`.
3. **Favicon** — update via the Drupal theme settings page.
4. **Screenshot** — replace `screenshot.png` (shown in Drupal's Appearance page).

After replacing assets, rebuild:

```bash
npm run dist
```

## Troubleshooting

### Build fails with rsync errors

The build system uses rsync to merge component directories. Ensure rsync is installed and available on your system. On macOS it is included by default; on Windows, use WSL or install rsync separately.

### Storybook shows blank page or missing components

- Check the browser console for errors
- Ensure `npm run dist` completed successfully before starting Storybook
- Verify that `dist/constants.json` exists (Storybook reads icon and asset lists from it)

### Changes not appearing in Drupal

- Clear Drupal caches: `drush cr`
- Confirm you ran `npm run dist` after making changes
- Check that your sub-theme (not the base CivicTheme) is set as the default theme

### Node version mismatch

The sub-theme includes an `.nvmrc` file specifying the required Node version. Use `nvm use` to switch to the correct version before running any npm commands.

{% hint style="warning" %}
**Remove examples from civictheme_starter_kit**

CivicTheme 1.11 saw the upgrade to SDCs which came with a namespace change. The existing example components need to be removed so that civictheme sub-themes built with this tool work correctly.

We will address this issue in CivicTheme 1.12. As a workaround, please delete the following directories from your new sub-theme manually (unless you have added some code changes):

    /components/01-atoms/demo-button
    /components/01-atoms/demo-button
    /components/03-organisms/header
{% endhint %}

# Chapter 1: Installing CivicTheme on Drupal

This chapter walks your team through installing CivicTheme on a standalone Drupal site. By the end, you will have CivicTheme installed via Composer, required modules enabled, a sub-theme generated, front-end assets built, and the site ready for customisation.

Unlike GovCMS SaaS, a standard Drupal site uses Composer to manage theme dependencies, which simplifies the installation process.

## Prerequisites

- [ ] A working Drupal 10.2+ or 11+ site with Composer-managed dependencies
- [ ] Composer installed and available on the command line
- [ ] Drush installed (recommended for command-line operations)
- [ ] NodeJS 22+ and NPM 10+ available on your machine
- [ ] Administrator access to the Drupal site

## Step 1: Install CivicTheme and enable modules

For instructions on installing CivicTheme via Composer, see the [Drupal theme installation reference](../../installation/drupal-theme.md).

## Step 2: Generate your sub-theme

CivicTheme must not be modified directly — all custom work happens in a sub-theme. A script generates the full sub-theme scaffold:

```bash
cd web/themes/contrib/civictheme
php civictheme_create_subtheme.php <SUBTHEME_MACHINE_NAME> "<Subtheme Human Name>" "<A description>" ../custom/<SUBTHEME_MACHINE_NAME> --remove-examples
```

Then enable it:

```bash
drush theme:enable <SUBTHEME_MACHINE_NAME> -y
drush config-set -y system.theme default <SUBTHEME_MACHINE_NAME>
```

> **Naming tip**: Name your sub-theme after the site, not after CivicTheme. Avoid including "civic" or "civictheme" in the machine name — it creates confusion when maintaining the theme later.

The script options and the generated directory structure are documented in the [sub-theme reference](../../development/drupal-theme/sub-theme.md).

## Step 3: Build front-end assets

```bash
cd web/themes/custom/<SUBTHEME_MACHINE_NAME>
nvm use
npm install
npm run build
```

Verify that the `dist` directory was created. Navigate to your site in the browser and confirm that default CivicTheme styling is applied.

## Step 4: Provision content

CivicTheme includes pre-configured blocks, menus, and configuration entities that set up the default site structure. 

Navigate to `/admin/appearance/settings/<SUBTHEME_MACHINE_NAME>` and press the **Provision content** button. Then export configuration with `drush cex -y`.

See the [Provision content section](../../installation/drupal-theme.md) for more information.

## Step 5: Verify the installation

After provisioning, your site should match the [default CivicTheme site](https://default.civictheme.io/) (without homepage content). Check that:

- [ ] The header displays with the CivicTheme logo and navigation
- [ ] The footer displays with default blocks (social links, footer navigation, acknowledgement, copyright)
- [ ] The site responds correctly on mobile (navigation collapses to mobile menu)
- [ ] The admin theme is accessible at `/admin`

## Troubleshooting

For common installation issues (content not appearing, styling not applied, module dependency errors), see the troubleshooting section in the [Drupal theme installation reference](../../installation/drupal-theme.md#troubleshooting).

## Where to get help

For all support options, see [Getting help](../../getting-started/getting-help.md).

## Next step

With CivicTheme installed and your sub-theme generated, the next step is to understand the sub-theme structure and set up your local development workflow.

Continue to [Chapter 2: Setting Up Your Sub-Theme](../shared/02-sub-theme-setup.md).

# Chapter 3: Configuring Colors and Theme Settings

This chapter covers the first customisation most teams tackle after installation: making the site match your brand. CivicTheme provides two levels of visual configuration — a no-code UI for site managers and SCSS variable overrides for developers. By the end, you will have your brand colors applied, header and footer configured, and understand how CivicTheme's color system works.

## Prerequisites

- [ ] Sub-theme set up and build system working (see [Chapter 2](02-sub-theme-setup.md))
- [ ] Administrator access to the Drupal site
- [ ] Your brand's color values (hex codes) for primary, secondary, and accent colors

## Step 1: Access the theme settings page

All visual configuration starts at the theme settings page:

```
/admin/appearance/settings/<your_theme_machine_name>
```

This page provides sections for colors, header, footer, components, and content provisioning. Changes made here take effect immediately across the site without requiring a code deployment.

## Step 2: Configure the header and footer

The header and footer each have independent theme (light/dark) and logo settings. CivicTheme supports multiple logo display modes (default, stacked, inline, inline stacked). Upload your logo files in `assets/logos/` in your sub-theme, then select them through the theme settings.

The header configuration reference covers all available options including navigation styles. See [Header configuration](../../configuration/header.md). The footer configuration reference covers footer-specific options including background image settings. See [Footer configuration](../../configuration/footer.md).

## Step 3: Set up brand colors

CivicTheme's color system is built around a small set of **brand colors** that automatically derive a full color palette. You set 3 brand colors per theme (light and dark), and CivicTheme generates all the heading, body, background, border, interaction, and status colors from them.

The Color Selector UI, brand color derivation formulas, individual palette overrides, and Drush commands for scripted workflows are documented in the [color selector reference](../../development/drupal-theme/color-selector.md).

The full color system architecture, the `ct-component-theme` mixin, CSS custom property generation, and variable naming conventions are documented in the [colors system reference](../../development/drupal-theme/systems/colors.md).

## Step 4: Override colors via SCSS (developer workflow)

For deeper control, developers can override colors at the SCSS level in the sub-theme. This is useful when you want colors baked into the compiled CSS rather than managed through the Drupal UI.

There are three levels of SCSS color override:

1. **Brand colors** — override `$ct-colors-brands` in `variables.base.scss` to change the foundation values that feed into all derivations
2. **Palette colors** — override `$ct-colors` in `variables.base.scss` to set specific semantic colors (heading, body, interaction-background, etc.)
3. **Component colors** — override individual component variables in `variables.components.scss` (e.g., `$ct-button-light-primary-background-color`)

Component variables follow the naming pattern: `$ct-[component]-[theme]-[subcomponent]-[state]-[property]`.

After any SCSS changes, rebuild:

```bash
npm run dist
```

The variable override system, `!default` flag mechanism, and the two variable files are documented in the [variables reference](../../development/uikit/components/variables.md).

## Step 5: Verify your color configuration

After setting up colors (via UI or SCSS), check these areas:

- [ ] Light theme pages — headings, body text, links, and buttons use your brand colors
- [ ] Dark theme sections — colors switch correctly when components use the dark theme
- [ ] Header and footer — themed correctly with your logo and brand colors
- [ ] Interactive elements — buttons, links, and form fields show correct hover and focus states
- [ ] Status messages — information, warning, error, and success messages are clearly distinguishable
- [ ] Accessibility — ensure sufficient contrast ratios between text and backgrounds (WCAG 2.2 AA requires 4.5:1 for body text, 3:1 for large text)

## Troubleshooting

For common color issues (colors not updating, dark theme problems, palette overrides being reset), see the troubleshooting section in the [color selector reference](../../development/drupal-theme/color-selector.md#troubleshooting).

## Next step

With your site's visual identity configured, the next step is to learn how to modify existing CivicTheme components when the default appearance or behavior does not meet your needs.

Continue to [Chapter 4: Overriding Existing Components](04-overriding-components.md).

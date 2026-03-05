# Color selector

### Managing colors

Website colors can be specified via:

* **Color Selector** — the admin UI for setting brand and palette colors without code
* **[CSS code](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme\_starter\_kit/components/variables.base.scss#L42)** — SCSS variable overrides in `variables.base.scss`
* **CSS code with Color Selector overrides** — a combination of both

For the full color system architecture, formula syntax, and derivation map, see [Colors system](systems/colors.md).

### Using the Color Selector UI

1. Navigate to the theme settings page: `/admin/appearance/settings/<your_theme_machine_name>`
2. Ensure **Use Color Selector** is enabled
3. Enable **Use Brand Colors** — this lets you set 3 brand colors and have the rest derived automatically
4. Set your brand colors for both **Light** and **Dark** themes:

| Color | Purpose | Example |
|-------|---------|---------|
| **Brand 1** | Primary color — used for headings, interaction backgrounds, links | Your primary brand color |
| **Brand 2** | Background color — used for page backgrounds, borders, input fields | A neutral or light color |
| **Brand 3** | Accent/highlight color | A contrasting accent color |

5. Save the configuration

#### How color derivation works

From your 3 brand colors, CivicTheme derives the full palette using formula-based transformations:

- **Headings** — derived from Brand 1 with a shade (darkening) operation
- **Body text** — derived from Brand 1, shaded then tinted
- **Backgrounds** — derived from Brand 2 with tint (lightening) and shade operations for light, medium, and dark variants
- **Borders** — derived from Brand 2 with varying shade levels
- **Interaction colors** — derived from Brand 1 (backgrounds) and Brand 2 (text) for hover, focus, and active states
- **Highlight** — uses Brand 3 directly
- **Status colors** (information, warning, error, success) — use fixed accessible defaults that can be overridden individually

Each derived color uses a formula like `brand1|shade,60` (mix Brand 1 with 60% black) or `brand2|tint,90` (mix Brand 2 with 90% white). You can see the dependents by enabling "Show dependents" on the color picker.

#### Overriding individual palette colors

If the derived colors do not meet your needs, you can override any individual palette color in the Color Selector UI. Uncheck "Use Brand Colors" to gain full manual control over every color in the palette, or keep Brand Colors enabled and override specific palette values as needed.

#### Disabling Color Selector

If colors managed in CSS code only, make sure that Color Selector is disabled in UI or with Drush command:

```sh
drush config-set civictheme.settings colors.use_color_selector 0
```

#### Setting colors via Drush command

Palette colors can be set in bulk via Drush command by providing Brand colors:

```sh
# Enable Color Selector.
drush config-set civictheme.settings colors.use_color_selector 1

# Enable Brand Colors.
drush config-set civictheme.settings colors.use_brand_colors 1

# Set Brand Colors.
drush --include=path/to/civictheme/src/Drush civictheme:set-brand-colors light_brand1 light_brand2 light_brand3 dark_brand1 dark_brand2 dark_brand3

# Purge dynamic assets cache. Will be rebuilt during next pageload.
drush --include=path/to/civictheme/src/Drush civictheme:clear-cache
```

**Example**

```sh
drush -y config-set civictheme.settings colors.use_color_selector 1
drush -y config-set civictheme.settings colors.use_brand_colors 1
drush --include=path/to/civictheme/src/Drush civictheme:set-brand-colors "#00698f" "#e6e9eb" "#121313" "#61daff" "#003a4f" "#00698f"
drush --include=path/to/civictheme/src/Drush civictheme:clear-cache
```

## Troubleshooting

### Colors not updating after changing brand colors

- Clear Drupal caches: `drush cr`
- If using the Color Selector, ensure you pressed Save on the theme settings page
- If using SCSS overrides, ensure you ran `npm run dist` and cleared caches

### Dark theme colors look wrong

- Ensure you set brand colors for both light and dark themes — they are independent
- Dark theme brand2 should typically be a dark background color, not the same as light brand2

### Individual palette overrides being reset

- If "Use Brand Colors" is enabled, derived colors will recalculate when brand colors change. Override at the palette level if you need a value to stay fixed regardless of brand color changes.

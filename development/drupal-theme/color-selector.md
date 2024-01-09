# Color selector

### Managing colors

Website colors can be specified via:

* Color Selector
* [CSS code](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme_starter_kit/components/variables.base.scss#L42)
* CSS code with Color Selector overrides

See [theme settings](../../content-authoring/site-wide-configuration/theme-settings/) for more details about colors and to set colors via Color Selector.

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

# Namespaces

Component namespaces have changed with the release of CivicTheme 1.11 which migrated CivicTheme components to use Single Directory Components.

## Current Namespace Format

All CivicTheme components now use the format `civictheme:<component_name>` for example `civictheme:button` or `civictheme:accordion`. There is no longer nesting of components into their atomic directories.

## Sub-theme Namespacing

In a sub-theme, a new component is namespaced with the sub-theme's machine name. For example: `civictheme_subtheme:new_button`

However, when overriding a CivicTheme component, the sub-theme uses the original CivicTheme namespace `civictheme:button` to refer to this overridden component. This ensures that the override properly replaces the base theme's component.

## Single Directory Components

For more information about the Single Directory Components specification, see the [Drupal documentation on SDC](https://www.drupal.org/docs/develop/theming-drupal/using-single-directory-components).
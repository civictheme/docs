# Chapter 5: Creating New Components

This chapter walks through building a completely new component for your sub-theme. It covers the full lifecycle from deciding where the component fits in the atomic design hierarchy through to integrating it with Drupal via paragraph types and preprocess hooks. By the end, you will have a repeatable process for adding custom components that follow CivicTheme conventions.

## Prerequisites

- [ ] Sub-theme set up with build system working (see [Chapter 2](02-sub-theme-setup.md))
- [ ] Understanding of component override patterns (see [Chapter 4](04-overriding-components.md))
- [ ] Familiarity with Twig, SCSS, JavaScript, and Drupal's paragraph system

## Step 1: Decide the component level and create files

Determine where your component fits in the atomic design hierarchy (atom, molecule, or organism), then create the required file set: `.component.yml`, `.twig`, `.scss`, `.stories.js`, and optionally `.js`.

The atomic design levels, required files, variable registration, and component checklist are documented in the [creating components reference](../../development/uikit/components/creating-components.md). The file conventions (Twig, SCSS, JS patterns) are in the [components system reference](../../development/drupal-theme/systems/components.md).

## Step 3: Build and preview

Compile your new component and preview it in Storybook:

```bash
npm run dist
npm run storybook
```

Navigate to your component in Storybook and verify all props work correctly across both light and dark themes.

## Step 4: Integrate with Drupal

To use your component in Drupal's content authoring workflow, you need to connect it to Drupal's data layer. SDC components can be included in any Drupal Twig template — not just paragraph templates. Look at the `templates` directory in CivicTheme to see how components are integrated into Drupal's theme system (nodes, blocks, fields, pages, etc.).

A common pattern for content-authorable components involves three pieces:

1. **A paragraph type** — often a component needs multiple fields to be grouped together. CivicTheme in many instances uses a paragraph type in Drupal with fields to match to a component's props. Field names follow CivicTheme's naming convention (`field_c_p_` prefix for CivicTheme paragraph fields, `field_p_` for custom paragraph fields).

2. **A preprocess include** — create an include file in `includes/` that extracts Drupal field values and maps them to component props using CivicTheme utility functions like `civictheme_get_field_value()`. Include it from your sub-theme's `.theme` file.

3. **A Drupal template** — create a thin Twig template in `templates/paragraph/` that includes your component and passes the preprocessed variables. Keep HTML in the component template, not in the Drupal template.

The three-step implementation pattern, field naming conventions, utility functions, and best practices are documented in the [mapping system reference](../../development/drupal-theme/systems/mapping.md). The template conventions are documented in the [templates reference](../../development/drupal-theme/templates.md). Asset management is covered in the [assets reference](../../development/drupal-theme/assets.md).

## Step 5: Rebuild, deploy, and test

```bash
npm run dist
drush cr
```

1. Create a page in Drupal and add your new paragraph type
2. Fill in the fields and save
3. Verify the component renders correctly on the front end
4. Test in both light and dark theme contexts

## Component checklist

See the [component checklist](../../development/uikit/components/creating-components.md#component-checklist) for the full verification list before considering your component complete.

## Contributing back

If your component may be useful to the broader CivicTheme community, consider contributing it upstream. The contribution guide covers the process from feature branch through PR review. See [Contributing](../../contributing.md).

## Next step

With both component overriding and creation covered, the remaining chapters focus on keeping your site current and secure after the initial build.

Continue to [Chapter 6: Updating Packages](06-updating-packages.md).

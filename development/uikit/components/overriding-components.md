# Overriding Existing Components

This reference covers the process for overriding an existing CivicTheme component in your sub-theme — from deciding whether to override, through the copy-and-register process, to style-only alternatives.

## When to Override vs. Create New

| Situation | Approach |
|-----------|----------|
| Change the look of an existing component (colors, spacing, layout) | **Override** — modify the existing component in your sub-theme |
| Change the behavior of an existing component (JavaScript interactions) | **Override** — modify the component's `.js` file |
| Add a variant to an existing component (a new button style) | **Override** — extend the component's template and SCSS |
| Build something that does not map to any existing component | **Create new** — see [Creating components](creating-components.md) |
| Combine existing components in a new way | **Create new** — compose a molecule or organism from existing atoms |

## Identifying the Component

Components are organised by atomic design level in the base CivicTheme theme:

```
civictheme/components/
├── 00-base/        # Foundation (variables, mixins, grid)
├── 01-atoms/       # Button, Tag, Heading, Link, etc.
├── 02-molecules/   # Cards, Accordion, Breadcrumb, etc.
├── 03-organisms/   # Header, Footer, Banner, Navigation, etc.
└── 04-templates/   # Page layouts
```

Use Storybook to browse components visually, or search the base theme's `components/` directory for the component name.

## Copy and Register

Copy the entire component directory from the base theme into the matching location in your sub-theme:

```bash
# Example: overriding the button component
cp -r path/to/civictheme/components/01-atoms/button \
      your_theme/components/01-atoms/button
```

Keep the same directory name and location within the atomic hierarchy. The build system matches components by directory name when merging.

In your copied `component.component.yml`, add a `replaces` key to declare the override:

```yaml
replaces: 'civictheme:button'
```

Both components must have compatible schemas — the props and slots in your override must match the original. You can add new props, but existing ones must remain compatible.

## Modifying the Component

Modify only the files you need to change — but for clarity and maintainability, it is recommended to copy the entire component directory.

CivicTheme components follow strict conventions for SCSS (BEM naming, design tokens, theme mixins), Twig (prop validation, class construction, nested includes with `only`), and JavaScript (constructor pattern, data-attribute selection, no jQuery). The complete file conventions and code patterns are documented in the [components system reference](../../drupal-theme/systems/components.md).

## Style-Only Overrides (Simpler Alternative)

If you only need to change a component's visual appearance without modifying its template or JavaScript, you can override just the SCSS variables instead of copying the entire component.

Edit `components/variables.components.scss` in your sub-theme:

```scss
// Override button colors without copying the component
$ct-button-light-primary-background-color: #custom-color;
$ct-button-light-primary-hover-background-color: #custom-hover;
```

This is the lightest-touch approach and avoids maintaining a full copy of the component. Use it when variable overrides are sufficient. The variable override mechanism and naming conventions are documented in the [variables reference](variables.md).

## Rebuild and Verify

After making changes:

```bash
npm run dist
npm run storybook
```

Check all variants of the component (light/dark theme, different sizes, states) in Storybook. Then clear Drupal caches (`drush cr`) and verify on the live site.

## Common Pitfalls

For common issues (forgetting to rebuild, namespace conflicts, breaking the prop schema, preprocess hook dependencies), see the [common pitfalls](../../drupal-theme/systems/components.md#common-pitfalls) section of the components system reference.

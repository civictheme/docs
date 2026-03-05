# Creating New Components

This reference covers the process of creating a new component that follows CivicTheme conventions: atomic design placement, required files, variable registration, and the component checklist.

## Atomic Design Levels

Determine where your component fits in the hierarchy:

| Level | What it contains | Examples |
|-------|-----------------|----------|
| **Atom** (`01-atoms/`) | A single UI element that cannot be broken down further | Button, Tag, Heading, Input |
| **Molecule** (`02-molecules/`) | A combination of atoms forming a functional group | Card, Accordion, Breadcrumb, Search |
| **Organism** (`03-organisms/`) | A complex section composed of molecules and atoms | Header, Footer, Banner, Navigation |

**Rules of thumb:**
- If it contains only HTML elements and no other CivicTheme components, it is an atom
- If it includes other CivicTheme atoms or molecules via `{% include %}`, it is a molecule or organism
- If it represents a major page section, it is an organism

## Single Directory Components (SDC)

CivicTheme uses Drupal's Single Directory Component (SDC) architecture. Each component lives in its own directory containing all related files. The `.component.yml` file registers the component with Drupal and defines its props schema using JSON Schema. Drupal validates props against this schema at render time, so incorrect prop types or missing required values will raise errors.

Components are referenced by namespace and machine name (e.g., `civictheme:feature-card`). In your sub-theme, new components are automatically registered under your sub-theme's namespace. To override a base theme component, add `replaces: civictheme:component_name` to your `.component.yml`.

## Required Files

Create a directory for your component in the appropriate atomic level (e.g., `your_theme/components/02-molecules/feature-card`). Each component needs these files:

| File | Purpose |
|------|---------|
| `feature-card.component.yml` | SDC metadata: name, status, description, props schema (JSON Schema with Drupal's metadata schema), and slots for rich content areas |
| `feature-card.twig` | HTML template with prop validation, BEM class construction, and nested includes |
| `feature-card.scss` | Styles using BEM naming, design tokens, and the `ct-component-theme` mixin |
| `feature-card.stories.js` | Storybook story with interactive controls for all props |
| `feature-card.js` | JavaScript using constructor pattern (only if the component has interactive behavior) |

The `.component.yml` file is the starting point — it defines the component's interface. Props use JSON Schema types (`string`, `boolean`, `object`, `array`) with optional `enum` constraints and `default` values. Slots are used for content areas that accept rendered markup rather than simple values.

The conventions for each file type — Twig prop validation, SCSS theme mixins, JavaScript constructor patterns, Storybook controls, and the full `.component.yml` schema — are documented in the [components system reference](../../drupal-theme/systems/components.md).

## Registering Component Variables

If your component needs theme-specific color variables, define them in `components/variables.components.scss` using the naming convention `$ct-[component]-[theme]-[property]` with `!default` flags:

```scss
$ct-feature-card-light-background-color: ct-color-light('background-light') !default;
$ct-feature-card-light-title-color: ct-color-light('heading') !default;
$ct-feature-card-dark-background-color: ct-color-dark('background-light') !default;
$ct-feature-card-dark-title-color: ct-color-dark('heading') !default;
```

For details on the variable system, see [Variables](variables.md).

## Drupal Integration

To use your component in Drupal's content authoring workflow, you need three pieces:

1. **A paragraph type** — with fields matching your component's props, using CivicTheme's field naming conventions (`field_c_p_` for CivicTheme paragraph fields, `field_p_` for custom paragraph fields)
2. **A preprocess include** — in `includes/` that extracts Drupal field values and maps them to component props using utility functions like `civictheme_get_field_value()`
3. **A Drupal template** — a thin Twig template in `templates/paragraph/` that includes your component

The implementation pattern and field naming conventions are documented in the [mapping system reference](../../drupal-theme/systems/mapping.md). Template conventions are in the [templates reference](../../drupal-theme/templates.md).

## Component Checklist

Before considering your component complete, verify:

- [ ] Component displays correctly in Storybook across all prop combinations
- [ ] Light and dark themes both render correctly
- [ ] Responsive behavior works at all breakpoints (xxs through xl)
- [ ] SCSS uses design tokens (`ct-spacing()`, `ct-typography()`, `ct-breakpoint()`) — no hardcoded values
- [ ] BEM naming follows the `ct-<component>__<element>--<modifier>` convention
- [ ] JavaScript (if any) prevents double initialization and uses vanilla JS
- [ ] Drupal integration maps all fields correctly via preprocess hooks
- [ ] `npm run lint` passes without errors

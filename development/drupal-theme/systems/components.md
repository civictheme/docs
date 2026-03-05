# Components

This guide outlines the standard file structure and characteristics for CivicTheme components, based on the established patterns in the codebase.

## Overview

Each component follows a consistent file structure with specific purposes for each file type. This ensures maintainability, reusability, and proper integration with the CivicTheme design system.

## File Types and Purposes

### `*.component.yml` - Component Metadata and Schema

**Purpose**: Defines the component's properties, validation rules, and documentation for the design system.

**Characteristics**:
- Uses JSON Schema format with Drupal's metadata schema
- Defines all available props with types, descriptions, and validation rules
- Includes enums for constrained values (e.g., theme options, size variants)
- Provides default values where appropriate
- Serves as the single source of truth for component configuration
- Enables automatic form generation in Storybook and Drupal

**Key sections**:
- `$schema`: References Drupal's metadata schema
- `name`: Human-readable component name
- `status`: Component stability status
- `description`: Component purpose and usage
- `props`: Detailed property definitions with validation

### `*.twig` - Template File

**Purpose**: Defines the HTML structure and logic for rendering the component.

**Characteristics**:
- Contains comprehensive documentation in the header comment block
- Lists all available props with types and descriptions
- Implements conditional logic for different component states
- Uses Twig's template inheritance and includes
- Handles multiple component variants (e.g., different types, sizes, themes)
- Includes accessibility attributes and ARIA labels
- Supports both static and dynamic content rendering

**Key patterns**:

**Prop validation** — validate props at the top of the template using ternary operators:

```twig
{% set kind = kind in ['button', 'link', 'reset', 'submit'] ? kind : 'button' %}
{% set type = type in ['primary', 'secondary', 'tertiary'] ? type : null %}
{% set theme = theme in ['light', 'dark'] ? theme : 'light' %}
```

**Class construction** — build modifier classes dynamically:

```twig
{% set type_class = type ? 'ct-button--%s'|format(type) : '' %}
{% set size_class = size ? 'ct-button--%s'|format(size) : '' %}
{% set modifier_class = '%s %s %s'|format(type_class, size_class, modifier_class|default('')) %}
```

**Nested component includes** — use `only` to limit the scope of variables passed to child components:

```twig
{% include 'civictheme:icon' with {
  symbol: icon,
  size: 'small',
} only %}
```

**Blocks for extensibility** — use Twig blocks to allow further overriding by child templates:

```twig
{% block content_block %}
  <div class="ct-card__content">
    {{ content }}
  </div>
{% endblock %}
```

### `*.stories.js` - Storybook Configuration

**Purpose**: Creates interactive documentation and testing environment for the component.

**Characteristics**:
- Defines Storybook metadata and component configuration
- Maps component props to Storybook controls
- Provides default values for all component variants
- Enables interactive testing of different prop combinations
- Imports constants and design tokens for consistent options
- Supports component categorisation in Storybook navigation

**Key features**:
- Control types (radio, text, boolean, select) for different prop types
- Default story with sensible fallback values
- Integration with design system constants
- Component organisation in Storybook hierarchy

### `*.js` - JavaScript Functionality

**Purpose**: Provides interactive behaviour and event handling for the component.

**Characteristics**:
- Implements component-specific functionality and interactions
- Handles user events (click, focus, keyboard navigation)
- Manages component state and lifecycle
- Provides accessibility enhancements
- Uses vanilla JavaScript for broad compatibility
- Includes comprehensive event handling and error prevention
- Uses `data-` attributes for element selection to ensure HTML changes don't break functionality
- Avoids dependencies on jQuery, using standard DOM APIs
- Automatically wrapped with Drupal behaviours at build time

**Key patterns**:
- Constructor pattern for component initialisation
- Event delegation and proper cleanup
- Accessibility support (keyboard navigation, ARIA)
- State management and visual feedback
- Integration with design system classes
- Data attribute-based element selection for reusability
- Standard DOM methods (querySelector, addEventListener, etc.)
- Proper error handling and validation

**Implementation approach**:
- Common utilities are managed in `/components/00-base`
- Element connections use `data-` attributes instead of classes, IDs, or element tags
- Ensures minimal impact on JS when HTML structure changes
- Promotes reusability across different HTML structures
- Build process automatically wraps with `Drupal.behaviors.attach` functions

### `*.scss` - Source Styles

**Purpose**: Defines the component's visual styling using SCSS.

**Characteristics**:
- Uses SCSS features (variables, mixins, nesting)
- Implements BEM methodology for class naming
- Integrates with design system tokens and variables
- Provides responsive design support
- Includes focus states and accessibility styling
- Uses mixins for consistent styling patterns
- Supports light and dark theme variants
- Uses CivicTheme's color palette system for consistent theming

**Key patterns**:

**BEM naming** — all classes use the pattern `ct-<component>__<element>--<modifier>`:

```scss
.ct-button {              // Block
  $root: &;               // Store root selector for complex selectors

  &__icon {               // Element
    margin-right: ct-spacing(1);
  }

  &--primary {            // Modifier
    @include ct-button-type('primary');
  }
}
```

**Design tokens** — use token functions instead of hardcoded values:

```scss
padding: ct-spacing(3);             // 24px (3 * 8px particle)
border-width: ct-particle(0.125);
@include ct-typography('heading-4');
@include ct-breakpoint(m) { }       // Mobile-first breakpoint
```

**Theme support** — use the component theme mixin for light/dark theme support:

```scss
@include ct-component-theme($root) using($root, $theme) {
  @include ct-component-property($root, $theme, background-color);

  #{$root}__title {
    @include ct-component-property($root, $theme, title, color);
  }
}
```

**Key features**:
- Design system integration via variables and mixins
- Responsive breakpoints and media queries
- State-based styling (hover, focus, active, disabled)
- Theme support (light/dark variants)
- Modular and maintainable structure
- Color palette integration using `$ct-colors` variable map
- BEM naming convention for maintainable CSS architecture

**Implementation approach**:
- Most styles managed within components in `/components` directory
- `/assets/sass` reserved for Drupal-specific styles (admin blocks, CKEditor, Layout Builder)
- Color application via `/subtheme/components/variables.base.scss` using `$ct-colors`
- Fine-tuning colors in `/subtheme/components/variables.components.scss`
- Default color map reference: `civictheme/components/00-base/_variables.base.scss`
- Component color variables reference: `civictheme/components/00-base/_variables.components.scss`
- Encouraged to support both light and dark themes for new components
- Particularly important for giveback components

### `*.css` - Compiled Styles

**Purpose**: Generated CSS file for production use.

**Characteristics**:
- Automatically generated from SCSS source files
- Contains vendor-prefixed and optimised CSS
- Includes responsive design rules
- Provides fallback values and browser compatibility
- Optimised for performance and file size

**Important notes**:
- **Do not edit directly** - changes will be overwritten
- Generated via build process (`npm run dist`)
- Contains design system variables and custom properties
- Includes comprehensive state styling and accessibility features

## Development Guidelines

### File Naming Convention
- All files use the same base name as the component
- Follow kebab-case for component names
- Maintain consistent file extensions

### Component Structure
1. Start with the `*.component.yml` to define the component's interface
2. Create the `*.twig` template with proper documentation
3. Add `*.stories.js` for interactive documentation
4. Implement `*.js` for any required interactivity
5. Style with `*.scss` using design system patterns
6. Build generates the final `*.css` file

### Best Practices
- File header documentation is generated from the *.component.yml document
- Use design system tokens and variables consistently
- Implement proper accessibility features
- Test all component variants in Storybook
- Follow established naming conventions and patterns
- Ensure responsive design support
- Include proper error handling and validation

This structure ensures components are maintainable, reusable, and properly integrated with the CivicTheme design system while providing excellent developer experience through comprehensive documentation and testing tools.

## Common Pitfalls

### Forgetting to rebuild

Changes to SCSS, JavaScript, or Twig files require running `npm run dist`. Storybook's watch mode handles this automatically, but if you are testing in Drupal you need to rebuild and clear caches.

### Namespace conflicts

Your overridden component must use `replaces: 'civictheme:component_name'` in its `.component.yml` file. Without this, Drupal will see two components with conflicting names.

### Breaking the prop schema

When overriding a component's `.component.yml`, ensure existing props remain compatible. Adding new props is safe; removing or changing the type of existing props will break templates that depend on them.

### Preprocess hook dependencies

Some components receive their data from preprocess hooks in the base CivicTheme theme's `includes/` directory. If your override adds new props, you will need to provide data for them through your sub-theme's own preprocess hooks. The [mapping system](mapping.md) explains how Drupal entities are connected to component templates through preprocess functions.

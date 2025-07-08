# Colors in CivicTheme

## Overview

The CivicTheme color system is a sophisticated, multi-layered approach to managing colours across components. It provides a flexible foundation for creating consistent, accessible, and themeable user interfaces that support both light and dark themes.

## Quick Start

To use the CivicTheme color system:

1. **Define brand colours** in `$ct-colors-brands` (optional)
2. **Override default colours** in `$ct-colors` (optional)
3. **Use component variables** in `_variables.components.scss` for specific styling
4. **Apply themes** using the `ct-component-theme` mixin in component SCSS files

## Color System Architecture

### 1. Base Color Foundation (`_variables.base.scss`)

The color system is built on a foundation of semantic colour tokens that are mapped to actual colour values:

```scss
// Brand colours can be extended
$ct-colors-brands: () !default;

// Default colour palette can be overridden
$ct-colors: () !default;

// Default semantic colour mapping
$ct-colors-default: (
  'light': (
    'heading': ct-color-shade(ct-color-constant-light('brand1'), 60),
    'body': ct-color-tint(ct-color-shade(ct-color-constant-light('brand1'), 80), 20),
    'background-light': ct-color-tint(ct-color-constant-light('brand2'), 90),
    'background': ct-color-constant-light('brand2'),
    'interaction-background': ct-color-constant-light('brand1'),
    'interaction-text': ct-color-tint(ct-color-constant-light('brand2'), 80),
    // ... more semantic colours
  ),
  'dark': (
    'heading': ct-color-tint(ct-color-constant-dark('brand1'), 95),
    'body': ct-color-tint(ct-color-constant-dark('brand1'), 85),
    'background': ct-color-constant-dark('brand2'),
    'interaction-background': ct-color-constant-dark('brand1'),
    'interaction-text': ct-color-constant-dark('brand2'),
    // ... more semantic colours
  )
);
```

### 2. Component-Specific Variables (`_variables.components.scss`)

Component variables map semantic colours to specific component properties:

```scss
// Tag component variables
$ct-tag-light-primary-background-color: ct-color-light('interaction-background') !default;
$ct-tag-light-primary-color: ct-color-light('interaction-text') !default;
$ct-tag-dark-primary-background-color: ct-color-dark('interaction-background') !default;
$ct-tag-dark-primary-color: ct-color-dark('interaction-text') !default;
```

## How New Color Palettes Are Mapped

### Step 1: Define Brand Colours (Optional)

To create a custom colour palette, start by defining your brand colours:

```scss
// In your theme's variables.base.scss
$ct-colors-brands: (
  'light': (
    'brand1': #0066cc,  // Primary brand colour
    'brand2': #f8f9fa,  // Secondary brand colour
    'brand3': #ff6b35,  // Accent brand colour
  ),
  'dark': (
    'brand1': #4d94ff,  // Primary brand colour (dark variant)
    'brand2': #1a1a1a,  // Secondary brand colour (dark variant)
    'brand3': #ff8c69,  // Accent brand colour (dark variant)
  )
);
```

### Step 2: Override Default Colours (Optional)

You can override specific semantic colours without changing the entire palette:

```scss
// In your theme's variables.base.scss
$ct-colors: (
  'light': (
    'interaction-background': #custom-primary,
    'interaction-text': #custom-text,
  ),
  'dark': (
    'interaction-background': #custom-primary-dark,
    'interaction-text': #custom-text-dark,
  )
);
```

### Step 3: Component Variables Automatically Update

Once you've defined your brand colours or overridden semantic colours, all component variables automatically use the new values because they reference the semantic colour functions:

```scss
// These automatically use your new colours
$ct-tag-light-primary-background-color: ct-color-light('interaction-background');
$ct-tag-light-primary-color: ct-color-light('interaction-text');
```

## How Light and Dark Theme Colours Are Applied

### The `ct-component-theme` Mixin

The `ct-component-theme` mixin is the core mechanism for applying theme-specific styles:

```scss
@mixin ct-component-theme($name) {
  @each $theme in light, dark {
    &.ct-theme-#{$theme} {
      @content($name, $theme);
    }
  }
}
```

### Component Implementation Pattern

Components use this pattern to apply theme-specific styles:

```scss
.ct-tag {
  $root: &;

  // Base styles (shared across themes)
  border-radius: $ct-tag-border-radius;
  display: inline-block;

  // Theme-specific styles
  @include ct-component-theme($root) using($root, $theme) {
    &#{$root}--primary {
      @include ct-component-property($root, $theme, primary, background-color);
      @include ct-component-property($root, $theme, primary, border-color);
      @include ct-component-property($root, $theme, primary, color);
    }
  }
}
```

### CSS Custom Properties Generation

The `ct-component-property` mixin generates CSS custom properties:

```scss
@mixin ct-component-property($args...) {
  $property: list.nth($args, list.length($args));
  #{$property}: ct-component-var($args...);
}
```

This generates CSS like:
```css
.ct-tag.ct-theme-light.ct-tag--primary {
  background-color: var(--ct-tag-light-primary-background-color);
  border-color: var(--ct-tag-light-primary-border-color);
  color: var(--ct-tag-light-primary-color);
}

.ct-tag.ct-theme-dark.ct-tag--primary {
  background-color: var(--ct-tag-dark-primary-background-color);
  border-color: var(--ct-tag-dark-primary-border-color);
  color: var(--ct-tag-dark-primary-color);
}
```

### Colour Function Resolution

The `ct-color-light()` and `ct-color-dark()` functions resolve to CSS custom properties:

```scss
@function ct-color-light($name) {
  @return _ct-color($name, 'light');
}

@function _ct-color($name, $theme, $is-flat: false) {
  // ... validation logic ...

  @if not $is-flat {
    $color: ct-component-var(ct, color, $theme, $name);
  }

  @return $color;
}
```

This creates a chain: `ct-color-light('interaction-background')` → `var(--ct-color-light-interaction-background)` → actual colour value.

## Variable Naming Convention

Component variables follow a strict naming pattern:

```
$ct-[component]-[theme]-[?subcomponent]-[?state]-[rule]
```

Examples:
- `$ct-tag-light-primary-background-color`
- `$ct-button-dark-secondary-hover-border-color`
- `$ct-navigation-light-dropdown-menu-item-active-background-color`

## Practical Example: Creating a Custom Tag Variant

To add a new "success" variant to the tag component:

1. **Add component variables** in `_variables.components.scss`:
```scss
$ct-tag-light-success-background-color: ct-color-light('success') !default;
$ct-tag-light-success-border-color: $ct-tag-light-success-background-color !default;
$ct-tag-light-success-color: white !default;
$ct-tag-dark-success-background-color: ct-color-dark('success') !default;
$ct-tag-dark-success-border-color: $ct-tag-dark-success-background-color !default;
$ct-tag-dark-success-color: white !default;
```

2. **Add component styles** in `tag.scss`:
```scss
@include ct-component-theme($root) using($root, $theme) {
  // ... existing variants ...

  &#{$root}--success {
    @include ct-component-property($root, $theme, success, background-color);
    @include ct-component-property($root, $theme, success, border-color);
    @include ct-component-property($root, $theme, success, color);
  }
}
```

## Benefits of This System

1. **Semantic Colour Mapping**: Colours are defined by purpose, not specific values
2. **Automatic Theme Support**: Light and dark themes are handled automatically
3. **CSS Custom Properties**: Enables runtime theme switching
4. **Extensible**: Easy to add new colours or override existing ones
5. **Consistent**: All components follow the same theming pattern
6. **Maintainable**: Changes to brand colours propagate throughout the system

## Key Files

- `_variables.base.scss`: Foundation colour definitions
- `_variables.components.scss`: Component-specific colour mappings
- `mixins/_color.scss`: Colour utility functions
- `mixins/_component.scss`: Theme application mixins

## Next Steps

To implement a new colour palette:

1. Define your brand colours in `$ct-colors-brands`
2. Override any semantic colours in `$ct-colors` if needed
3. Test components in both light and dark themes
4. Use the existing component variables for consistency
5. Add new component variables following the naming convention

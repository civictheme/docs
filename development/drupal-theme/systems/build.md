# Build System

## Overview

CivicTheme's build system is a custom asset compilation pipeline designed specifically for Drupal themes. Built around `build.js`, it provides a simplified, fast approach to managing theme assets while prioritising speed and auditability over complex optimisation features.

The system is engineered to handle the unique requirements of government digital services, ensuring consistent asset delivery across different environments while maintaining the flexibility needed for custom theme development.

## Core Architecture

### Asset Compilation Pipeline

The build system processes multiple asset types through a unified pipeline:

1. **Combines component directories** — uses rsync to merge CivicTheme's components with your sub-theme's components into a temporary `components_combined/` directory. This combined directory is used by Storybook so it can render all components together. SDC components ship their own compiled CSS alongside their component files in the `components/` directory.
2. **Compiles SCSS** — processes theme-level stylesheets (theme styles, layout styles, editor styles, admin styles, variables) into CSS in `dist/` using `sass-embedded`. Component-level SCSS is compiled to `.css` files within each component's own directory.
3. **Bundles JavaScript** — wraps component JavaScript in Drupal behavior patterns.
4. **Copies assets** — moves fonts, icons, images, and other static assets to `dist/assets/`.
5. **Generates constants** — exports SCSS variables, icon names, backgrounds, and logos to `dist/constants.json` for use in Storybook.

### Component System Integration

The build system manages CivicTheme's component architecture:

- **Component Combination**: Merges base CivicTheme components with custom theme components
- **SDC Support**: Generates isolated CSS/JS for Single Directory Components
- **Dependency Resolution**: Handles imports and ensures proper load order across the component hierarchy

### Multi-Environment Output

The system generates optimised outputs for different contexts:

- **Drupal Integration**: Produces files compatible with Drupal's asset management system
- **Storybook Support**: Creates separate builds for the Storybook development environment
- **Editor/Admin Styles**: Generates specialised stylesheets for different Drupal interfaces

## Build Modes and Commands

The build system supports multiple operational modes:

- **Full Build**: Complete asset compilation for production deployment
- **Watch Mode**: File system monitoring with automatic rebuilds for development
- **Selective Building**: Targeted compilation of specific asset types (styles, JavaScript, assets)
- **CLI Integration**: Parallel execution of npm scripts for improved performance

### Commands

```bash
# Full build (assets + Storybook static site)
npm run build

# Compile assets only (faster, no Storybook)
npm run dist

# Watch mode (recompiles on file changes)
npm run dist:watch

# Lint SCSS and JavaScript
npm run lint
npm run lint-fix

# Start Storybook dev server (runs dist first, then watches)
npm run storybook
```

### Key output files

| File | Purpose |
|------|---------|
| `dist/styles.base.css` | Base component styles |
| `dist/styles.theme.css` | Theme-specific styles |
| `dist/styles.variables.css` | CSS custom properties (color variables) |
| `dist/scripts.drupal.base.js` | JavaScript wrapped in Drupal behaviors |
| `dist/constants.json` | SCSS variables, icon names, backgrounds, and logos for Storybook |

## Configuration and Constants

### Theme Detection

The system automatically detects and links to the base CivicTheme installation, ensuring proper inheritance and customisation paths.

### Constants Generation

Extracts and processes design tokens including:
- Background configurations
- Icon definitions
- Logo specifications
- SCSS variable mappings

### Path Management

Handles complex directory structures and relative paths required for Drupal theme integration.

## Design Philosophy

The build system makes several deliberate architectural decisions:

### Performance Optimisations

- **Unix-focused**: Optimised for Unix-like environments with rsync for efficient file operations
- **Speed over optimisation**: Prioritises build speed over minification/uglification
- **Selective watching**: File monitoring limited to specific file types for efficiency
- **Minimal dependencies**: Uses native Node.js and command-line tools to reduce external dependencies

### Critical Assumptions

The system operates under specific technical constraints:

- Unix-like environment with rsync availability
- CivicTheme directory structure conventions
- Drupal integration patterns (behaviours, asset paths)
- Component-based architecture with clear separation of concerns

## Next Steps

To begin using the build system:

1. Ensure your environment meets the Unix-like requirements
2. Review the CivicTheme directory structure conventions
3. Configure your theme's build settings
4. Run the initial build process

For detailed implementation guidance, refer to the [Drupal theme development documentation](../README.md).

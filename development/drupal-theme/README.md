---
description: Documentation for developing and customising CivicTheme for Drupal
---

# Drupal theme

This section contains comprehensive documentation for developing and customising CivicTheme for Drupal.

## Installation

For installation instructions, see [Drupal theme installation](../../installation/drupal-theme.md).

## Core Development

- [assets](assets.md) - Asset management (CSS, JS, fonts, images)
- [templates](templates.md) - Using CivicTheme UI Kit components in Drupal
- [namespaces](namespaces.md) - Component namespace system and organisation
- [sub-theme](sub-theme.md) - Creating and customising sub-themes

## Systems Architecture

The systems section contains CivicTheme's unique architectural approaches:

- [systems](systems/README.md) - Overview of all systems and learning path
- [systems/build](systems/build.md) - Custom build system and development workflows
- [systems/components](systems/components.md) - Component-centric architecture and template separation
- [systems/colors](systems/colors.md) - Color override system and design token customisation
- [systems/mapping](systems/mapping.md) - How Drupal entities map to component templates

## Theme Customisation

- [color-selector](color-selector.md) - Color customisation tools and options
- [layout-builder](layout-builder.md) - Working with Drupal's Layout Builder
- [automated-list](automated-list.md) - Automated list component implementation

## Platform-Specific Guides

- [using-in-govcms-saas](using-in-govcms-saas.md) - GovCMS SaaS implementation guide
- [updating-civitheme-govcms-sass](updating-civitheme-govcms-sass.md) - SASS update procedures for GovCMS

## Key Concepts

CivicTheme emphasises these core principles:

1. **Component-centric development** - Organised folder structure for maintainable code
2. **Template separation** - Component Twig templates separated from Drupal HTML files
3. **Preprocess functions** - Custom data population for component templates
4. **Build system** - Custom asset compilation workflows
5. **Color system** - Flexible theming capabilities

## Learning Path

To effectively work with CivicTheme:

1. Start with [templates](templates.md) to understand component separation
2. Review [systems/build](systems/build.md) for development workflow
3. Study [systems/components](systems/components.md) for data flow patterns
4. Explore [systems/colors](systems/colors.md) and [assets](assets.md) for theming

This documentation provides everything needed to build maintainable, component-centric Drupal sites using CivicTheme's ecosystem.

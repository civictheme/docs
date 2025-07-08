# CivicTheme Systems

CivicTheme has several unique architectural approaches for developing themes that promote component-centric development and maintainability. Understanding these systems is essential for building sites that work effectively within the CivicTheme ecosystem.

## Overview

CivicTheme's development approach is built around these core systems:

- **Component-centric architecture** - Organised folders for styles, JavaScript, and templates
- **Template separation** - Component Twig templates separated from Drupal `*html.twig` files
- **Preprocess functions** - Custom functions to populate component template properties
- **Color system** - Custom color overrides and theming capabilities
- **Build system** - Custom asset compilation and development workflow

## System Documentation

Each system has detailed documentation that explains implementation patterns and best practices:

### [Build System](build.md)
Learn about CivicTheme's custom build system, including asset compilation, configuration, and development workflows.

### [Components](components.md)
Understand the component-centric approach, including template separation, preprocess functions, and how to map Drupal data to component properties.

### [Colors](colors.md)
Explore the color override system and how to customise CivicTheme's design tokens.

### [Styles](styles.md)
Learn about the styling system, including SASS architecture and component-specific styles.

### [Scripts](scripts.md)
Understand JavaScript organisation and how to extend component behaviours.

### [Mapping](mapping.md)
Discover how Drupal entities are mapped to component templates and properties.

## Related Documentation

### Component Development
- [Templates](../templates.md) - How to use CivicTheme UI Kit components in Drupal
- [Namespaces](../namespaces.md) - Component namespace system and organisation
- [Assets](../assets.md) - Asset management and component structure
- [UI Kit Components](../../uikit/extending-components.md) - Extending and customising components

### Content Authoring
- [Component List](../../components/component-list.md) - Complete component library
- [Content Components](../../content-authoring/components/README.md) - Using components in content

## Learning Path

To effectively work with CivicTheme systems:

1. **Start with the basics**: Read [Templates](../templates.md) to understand component separation
2. **Understand the build system**: Review [Build System](build.md) for development workflow
3. **Learn component mapping**: Study [Components](components.md) for data flow patterns
4. **Customise appearance**: Explore [Colors](colors.md) and [Styles](styles.md) for theming
5. **Extend functionality**: Use [Scripts](scripts.md) for custom behaviours

## Key Benefits

Learning these systems enables you to:

- Build **component-centric** sites that are maintainable and scalable
- Create **reusable patterns** that work across different projects
- Leverage **CivicTheme's ecosystem** effectively
- Maintain **consistent design** and development standards
- **Extend functionality** without breaking existing patterns

## Getting Help

- [Getting Help](../../getting-started/getting-help.md) - Community resources and support
- [Contribution Model](../../contributing/contribution-model.md) - How to contribute to the ecosystem
- [GitHub Organisation](https://github.com/civictheme/) - Source code and issues

# Chapter 4: Overriding Existing Components

This chapter covers the most common development task on a CivicTheme project: changing how an existing component looks or behaves. Rather than modifying the base theme (which must never be changed), you copy component files into your sub-theme and modify them there. The build system automatically picks up your version and uses it instead of the original.

## Prerequisites

- [ ] Sub-theme set up with build system working (see [Chapter 2](02-sub-theme-setup.md))
- [ ] Storybook running locally for preview
- [ ] Familiarity with Twig, SCSS, and BEM naming conventions

## Overview

Before overriding a component, decide whether you actually need an override or a new component. Then follow the copy-and-register process: copy the component directory, add a `replaces` key, and modify only what's needed. For style-only changes, you can override SCSS variables without copying the component at all.

The full override process — when to override vs. create new, the copy-and-register steps, style-only alternatives, and rebuild/verify workflow — is documented in the [overriding components reference](../../development/uikit/components/overriding-components.md).

The file conventions (Twig, SCSS, JS patterns) and common pitfalls are in the [components system reference](../../development/drupal-theme/systems/components.md).

## Next step

When overriding an existing component is not enough and you need something entirely new, the next chapter covers creating components from scratch.

Continue to [Chapter 5: Creating New Components](05-creating-components.md).

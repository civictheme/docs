---
hidden: true
---

# Components

CivicTheme [UI kit](https://uikit.civictheme.io/) provides 50+ components out of the box with a comprehensive system to modify, extend and create new components to fit your needs.

Twig components created with the CivicTheme UI kit are designed to be CMS-agnostic: they can be used by any application that can use Twig templates.

There are no CMS-specific mechanisms used in the UI kit.

### Modifying components colours

CivicTheme comes with an extensive variables and colour customisation system to enable you to change the look and feel.

See [colors variables override code sample](https://github.com/civictheme/uikit/blob/main/components/variables.base.scss).

### Extending components

Many CivicTheme components come with extendable areas (slots) which can be used by injecting HTML through pre-defined (empty) variables. Every Twig file provides a list of available empty slots (see [example](https://github.com/civictheme/uikit/blob/main/components/02-molecules/promo-card/promo-card.twig)).

For more advanced use-cases, it is also possible to [extend components using Twig blocks.](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme_starter_kit/components/02-molecules/navigation-card/navigation-card.twig)

###

# Drupal theme

### Requirements and constraints

* CivicTheme Drupal theme MAY be used out of the box without any customisations.
* CivicTheme Drupal theme MUST NOT be changed for customisations. If customisations are required - a consumer theme MUST be created and used as a sub-theme of the CivicTheme theme.
* CivicTheme Drupal theme MUST be fully compatible with GovCMS SaaS:
  * MUST NOT have any modules
  * MUST NOT rely on any libraries
  * MUST NOT rely on GovCMS content structures
  * MUST assume that FE compilation happens on local machine and then committed to the repository
  * MUST provide a static version of compiled Storybook for the CivicTheme-based consumer site.

### Agreements

* Config is stored in the `civictheme` theme's `config/install` and `config/optional` directories.
* All machine names are prefixed with `civictheme_` for:
  * Content types
  * Vocabularies
  * Text formats
  * User roles
* All labels do not use `CivicTheme` in UI.
* Field names are:
  * Prefixed with `field_c_<first_letter_of_entity_type>`.
  * Given generic names based on their purpose and should be shared across multiple bundles.
  * Named using singular nouns
* Vocabularies are:
  * Named using plural nouns

# Code naming conventions

{% hint style="info" %}
Requirement levels (MUST, SHOULD, MAY) are used in accordance with [RFC2119](https://www.ietf.org/rfc/rfc2119.txt)
{% endhint %}

* Configuration MUST be stored in the `civictheme` theme's `config/install` and `config/optional` directories.
* All machine names MUST be prefixed with `civictheme_` for:
  * Content types
  * Vocabularies
  * Text formats
  * User roles
* UI MUST NOT refer to `CivicTheme` .
* `page` or `article` SHOULD NOT be used as a prefix for the name of a content type unless absolutely necessary, instead: `News article` , `Blog page`
* Field names MUST be:
  * Prefixed with `field_c_<first_letter_of_entity_type>_`
  * Given generic names based on their purpose and SHOULD be shared across multiple bundles
  * Named using singular nouns
* Vocabularies MUST be:
  * Named using plural nouns
  * Named using contextual information to distinguish between vocabularies used for specific purposes: `Blog topics` instead of just `Topics`

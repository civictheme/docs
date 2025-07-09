# Mapping in CivicTheme

## Overview

CivicTheme separates its component Twig files from its Drupal implementation. This separation requires preprocess functions to extract data from Drupal entities, process it as necessary, and map it to the expected properties of the UI Kit Twig file. This approach encourages building CivicTheme components in a reusable fashion where the HTML is more generalised and less Drupal-specific.

***

## Quick Start

### Prerequisites

- A CivicTheme subtheme
- Basic understanding of Drupal preprocess functions
- Familiarity with Twig templating

### Basic Implementation

1. **Create a custom include file** for your field processing logic
2. **Implement a preprocess hook** to call your custom function
3. **Update the Twig template** to reference the CivicTheme component

***

## Utilities

CivicTheme provides utilities to simplify preprocess function development:

- [Utilities](https://github.com/civictheme/monorepo-Drupal/blob/develop/web/themes/contrib/civictheme/includes/utilities.inc) - Helper functions for common Drupal operations

***

## Implementation Example

The following example demonstrates how to map a Drupal field to display as a CivicTheme tag component. This covers the fundamentals of gathering data from an entity in a preprocess function, passing it through the `*.html.twig` template, and setting it on the `civictheme:tag` component.

### Step 1: Theme File

**File:** `subtheme.theme`

```php
require_once __DIR__ . '/includes/custom_field.inc';

function subtheme_preprocess_field(array &$variables): void {
  _civictheme_preprocess_custom_field($variables);
}
```

**What this does:**
- Includes the custom field processing logic
- Calls the custom preprocess function when the field preprocess hook is triggered

### Step 2: Custom Field Processing

**File:** `includes/custom_field.inc`

```php
use Drupal\Core\Entity\FieldableEntityInterface;

function _civictheme_preprocess_custom_field(array &$variables): void {
  if ($variables['field_name'] !== 'field_custom_field') {
    return;
  }

  $node = $variables['element']['#object'] ?? NULL;
  if ($node instanceof FieldableEntityInterface) {
    $variables['custom_value'] = civictheme_get_field_value($node, 'field_c_n_custom', TRUE);
  }
}
```

**What this does:**
- Checks that the correct field is being processed
- Retrieves the node attached to the field and validates its type
- Uses the `civictheme_get_field_value` utility to extract the field value
- Adds the processed value to the `custom_value` property

### Step 3: Twig Template

**File:** `templates/field/field--node--field-c-n-custom.html.twig`

```twig
{% include 'civictheme:tag' %}
```

**What this does:**
- References the CivicTheme tag component
- Passes all available properties through to the component
- Can be modified to reference custom components if needed

***

## Best Practices

### File Organisation

- Place custom code in dedicated `*.inc` files specific to the feature being implemented
- Use descriptive file names that clearly indicate the purpose
- Keep preprocess functions focused and single-purpose

### Template Structure

As much HTML as possible should live in the components. The Drupal Twig templates should act as connectors to the components. It should be common for Drupal `*.html.twig` templates to contain only an include of a component Twig file.

### Data Processing

- Always validate field names before applying custom processing
- Use CivicTheme utilities for common operations
- Ensure proper type checking for entities and fields
- Follow Drupal coding standards and best practices

***

## Next Steps

- Explore the [CivicTheme utilities](https://github.com/civictheme/monorepo-Drupal/blob/develop/web/themes/contrib/civictheme/includes/utilities.inc) for additional helper functions
- Review other component implementations for patterns and approaches
- Consider contributing improvements to the mapping system

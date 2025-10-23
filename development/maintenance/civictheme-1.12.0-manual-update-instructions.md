Instructions for manual mitigation

These instructions require an experienced developer to implement, to be able to test XSS protections and remove the information disclosure issues on entity reference fields.

The purpose of these instructions is for users that wish to mitigate the security issues found in CivicTheme (<1.12.0)
and manually update their older projects. 

It is also for those checking their sub-theme for XSS and information disclosure issues.

## Manual Instructions


## Key Information

CivicTheme provides a field API system for retrieving commonly used field values specific to CivicTheme.

*We strongly recommend that you use this system solely to retrieve field data for use within components.*
Not using this API will mean that the developer is reliant on implementing mitigations for XSS.

The following functions are available for use:

- `civictheme_get_field_value` - retrieves field values from fields that CivicTheme regularly uses. All field types within CivicTheme are supported and several more. Raise an issue if you require other field types supported.
- `civictheme_get_field_referenced_entities` - retrieves and checks access to referenced entities in a field of an entity. Also manages the cacheability metadata for the referenced entities.
- `civictheme_get_field_referenced_entity` - retrieves the first referenced entity in a field of an entity.
- `civictheme_get_referenced_entity_labels` - retrieves labels of the referenced entities.
- `civictheme_embed_svg` - embeds SVG from provided URL. This function does not protect against XSS and relies on appropriate level of user managing SVG Icons.

We recommend revieewing the `web/themes/contrib/`civictheme/includes/utilities.inc` for these utility functions.

## Updates to components

We have implemented updates to `heading.twig` and `button.twig` by removing the `raw` filter from the content outputs in these components.

Patches below for what change was required of each component:

```
diff --git a/components/01-atoms/heading/heading.twig b/components/01-atoms/heading/heading.twig  
index a6f95bf4..ab245f70 100644  
--- a/components/01-atoms/heading/heading.twig  
+++ b/components/01-atoms/heading/heading.twig  
@@ -19,6 +19,6 @@  
   
{% if content %}  
  <h{{ level }} class="ct-heading {{ modifier_class -}}" {% if attributes is not empty %}{{- attributes|raw -}}{% endif %}>  
-    {{- content|raw -}}  
+    {{- content -}}  
  </h{{ level }}>  
{% endif %}
```

In the latest change this looks like this for `button.twig`:

```
diff --git a/components/01-atoms/button/button.twig b/components/01-atoms/button/button.twig  
index 708bd62a..332d6ef2 100644  
--- a/components/01-atoms/button/button.twig  
+++ b/components/01-atoms/button/button.twig  
@@ -45,9 +45,9 @@  
      } only -%}  
    {% endset %}  
    {% if icon_placement == 'before' %}  
-      {{- icon_markup -}}{{ text|raw }}  
+      {{- icon_markup -}}{{ text }}  
    {% else %}  
-      {{ text|raw }}{{- icon_markup -}}  
+      {{ text }}{{- icon_markup -}}  
    {% endif %}  
  {%- else -%}  
    {%- include 'civictheme:text-icon' with {

```

These components have changed over time but the intent is to remove raw from content entered data.

### Remove attributes field from iframe paragraph
- Create a view to see whether you have any values in Attributes field for Iframe paragraph
- Remove the Attributes field (`field_c_p_attributes`)
- Delete field.field.paragraph.civictheme_iframe.field_c_p_attributes
- Delete field.storage.paragraph.field_c_p_attributes
- Update `\civictheme_preprocess_paragraph__civictheme_iframe` to add any required iframe attributes to the preprocess

### Update Content Author and Approver permission

- Remove permission to create, edit Icons media type

## CivicTheme API updates

It is the intention of CivicTheme sub-themes that all values used in CivicTheme components should be retrieved using the CivicTheme API and `civictheme_get_field_value` or `civictheme_get_field_referenced_entities` rather than through the Drupal entity field API.

CivicTheme uses this API for retrieving all field values for components.

- `civictheme_get_field_referenced_entities`
- `civictheme_get_field_referenced_entity`
- `civictheme_get_field_value`
- `civictheme_get_referenced_entity_labels`

These changes are adding the build array argument so CivicTheme can manage cacheable metadata but it is easiest to replace each function completely rather than patch in changes.

### Replace `civictheme_get_field_referenced_entities` with updated version

```php
/**  
 * Gets the referenced entities in a field of an entity. * * @param \Drupal\Core\Entity\FieldableEntityInterface $entity  
 *   The host entity.  
 * @param string $field_name  
 *   The entity reference field.  
 * @param array<string, mixed> $build  
 *   Render array to apply cacheability metadata to.  
 * * @return array<int|string, \Drupal\Core\Entity\EntityInterface>  
 *   Referenced entities. */function civictheme_get_field_referenced_entities(FieldableEntityInterface $entity, string $field_name, array &$build = []): array {  
  $trigger_bc = empty($build);  
  if ($trigger_bc) {  
    @trigger_error('Calling ' . __FUNCTION__ . ' without the $build argument is deprecated in civictheme:1.12.0 It will be required in civictheme:1.13.0. Triggered when getting entity for ' . $field_name . '. See https://www.drupal.org/node/3552745', E_USER_DEPRECATED);  
  }  
  if (civictheme_field_has_value($entity, $field_name)) {  
    /** @var \Drupal\Core\Entity\EntityInterface[] $referenced_entities */  
    $referenced_entities = $entity->get($field_name)->referencedEntities();  
    if (empty($referenced_entities)) {  
      return [];  
    }  
    $access_checked_referenced_entities = [];  
    foreach ($referenced_entities as $referenced_entity) {  
      $access = $referenced_entity->access('view', NULL, TRUE);  
      $cacheability = $cacheability ?? CacheableMetadata::createFromRenderArray($build);  
      $cacheability->addCacheableDependency($access);  
      $cacheability->addCacheableDependency($referenced_entity);  
  
      if ($access->isAllowed()) {  
        $access_checked_referenced_entities[$referenced_entity->id()] = $referenced_entity;  
      }  
    }  
    $cacheability->applyTo($build);  
    if ($trigger_bc && \Drupal::service('renderer')->hasRenderContext()) {  
      // The calling code didn't pass a render array that we can attach  
      // cacheable metadata to. There is a render context and $build has had      // cacheability metadata added, so we can simply render it, and it will      // bubble up to the current theme hook.      \Drupal::service('renderer')->render($build);  
    }  
  }  
  
  return $access_checked_referenced_entities ?? [];  
}
```

### Replace `civictheme_get_field_value` with updated version

```php
/**  
 * Gets values from fields that CivicTheme regularly uses. * * This function complements the field API system, providing a convenient way to * retrieve commonly used field values specific to CivicTheme. * * If a field type is not listed, and you need to retrieve its value, consider * using the field API system directly. * * @param \Drupal\Core\Entity\FieldableEntityInterface $entity  
 *   Entity to check field existence.  
 * @param string $field_name  
 *   Field name to get the value for.  
 * @param bool $only_first  
 *   Return only the first value of a multi-value field.  
 * @param mixed $default  
 *   Default value to return.  
 * @param array<string, mixed> $build  
 *   Render array to apply cacheability metadata to.  
 *   (required for entity reference fields). * * @return mixed|null  
 *   Whether the field exists and is not empty. * * @SuppressWarnings(PHPMD.BooleanArgumentFlag)  
 * @SuppressWarnings(PHPMD.CyclomaticComplexity)  
 * @SuppressWarnings(PHPMD.ElseExpression)  
 * @SuppressWarnings(PHPMD.StaticAccess)  
 */function civictheme_get_field_value(FieldableEntityInterface $entity, string $field_name, bool $only_first = FALSE, mixed $default = NULL, array &$build = []): mixed {  
  $value = $default;  
  
  if (!civictheme_field_has_value($entity, $field_name)) {  
    return $value;  
  }  
  
  $field = $entity->get($field_name);  
  $field_type = $field->getFieldDefinition()->getType();  
  
  switch ($field_type) {  
    case 'boolean':  
      $value = (bool) $field->getString();  
      break;  
  
    case 'integer':  
  
    case 'list_integer':  
      $value = (int) $field->getString();  
      break;  
  
    case 'list_string':  
    case 'string':  
    case 'string_long':  
      $value = $field->getString();  
      $value = Xss::filter($value);  
      break;  
  
    // Field types where we want to return field item.  
    case 'datetime':  
    case 'daterange':  
    case 'image':  
    case 'link':  
      $list = $field;  
      if (!$list->isEmpty()) {  
        $value = $only_first ? $list->first() : $list;  
      }  
      break;  
  
    // Field types where we want to return entities.  
    case 'entity_reference':  
    case 'entity_reference_revisions':  
      if ($only_first) {  
        $value = civictheme_get_field_referenced_entity($entity, $field_name, $build);  
      }  
      else {  
        $value = civictheme_get_field_referenced_entities($entity, $field_name, $build);  
      }  
      break;  
  
    case 'text_long':  
    case 'text_with_summary':  
    case 'text':  
      // Opinionated.  
      // This implementation renders the field if it has a single value.      // If the field contains multiple values, it relies on view() to handle      // the rendering.      if ($only_first) {  
        $field = $field->first();  
        $field_value = $field->get('value')->getString();  
        $field_format = $field->get('format')->getString();  
        $value = empty($field_format) ? $field_value : check_markup($field_value, $field_format);  
        break;  
      }  
  
      $value = $field->view();  
      break;  
  }  
  
  return $value;  
}

```

## Replace `civictheme_get_field_referenced_entity` function

Update the function with the below:

```php

/**  
 * Gets the first referenced entity in a field of an entity. * * @param \Drupal\Core\Entity\FieldableEntityInterface $entity  
 *   The host entity.  
 * @param string $field_name  
 *   The entity reference field.  
 * @param array<string, mixed> $build  
 *   Render array to apply cacheability metadata to.  
 * * @return \Drupal\Core\Entity\EntityInterface|null  
 *   Referenced entity. */function civictheme_get_field_referenced_entity(FieldableEntityInterface $entity, string $field_name, array &$build = []): ?EntityInterface {  
  $referenced_entity = NULL;  
  
  $entities = civictheme_get_field_referenced_entities($entity, $field_name, $build);  
  if (!empty($entities)) {  
    $referenced_entity = reset($entities);  
    if (!$referenced_entity instanceof EntityInterface) {  
      $referenced_entity = NULL;  
    }  
  }  
  
  return $referenced_entity;  
}


```

## Replace `civictheme_get_referenced_entity_labels` function

```php
/**  
 * Get labels of the referenced entities. * * @param \Drupal\Core\Entity\FieldableEntityInterface $entity  
 *   The host entity.  
 * @param string $field_name  
 *   The entity reference field.  
 * * @return array<int,string>  
 *   The label(s). * * @SuppressWarnings(PHPMD.StaticAccess)  
 */function civictheme_get_referenced_entity_labels(FieldableEntityInterface $entity, string $field_name): array {  
  $labels = [];  
  $referenced_entities = civictheme_get_field_value($entity, $field_name) ?? [];  
  foreach ($referenced_entities as $referenced_entity) {  
    if ($referenced_entity instanceof EntityInterface) {  
      $labels[] = Xss::filter((string) $referenced_entity->label());  
    }  
  }  
  
  return $labels;  
}

```

## Replace `civictheme_embed_svg`

```php
/**  
 * Embed SVG from provided URL. * * @param string $url  
 *   Local URL or local path to retrieve SVG from.  
 * @param array $css_classes  
 *   Array of CSS classes to add.  
 * * @return string|null  
 *   Loaded SVG or NULL if unable to load SVG. */function civictheme_embed_svg(string $url, array $css_classes = []): ?string {  
  $svg_path = DRUPAL_ROOT . (str_starts_with($url, 'http') ? parse_url(str_replace('.png', '.svg', $url), PHP_URL_PATH) : str_replace('.png', '.svg', $url));  
  if (!file_exists($svg_path)) {  
    return NULL;  
  }  
  
  $content = (string) file_get_contents($svg_path);  
  
  if (!empty($css_classes)) {  
    $content = str_replace('<svg ', '<svg class="' . implode(' ', $css_classes) . '" ', $content);  
  }  
  
  // Tag list taken from  
  // https://developer.mozilla.org/en-US/docs/Web/SVG/Reference/Element.  // Excludes <a>, <script> and <style>.  $supported_svg_tags = implode('', [  
    '<animate>',  
    '<animateMotion>',  
    '<animateTransform>',  
    '<circle>',  
    '<clipPath>',  
    '<defs>',  
    '<desc>',  
    '<ellipse>',  
    '<feBlend>',  
    '<feColorMatrix>',  
    '<feComponentTransfer>',  
    '<feComposite>',  
    '<feConvolveMatrix>',  
    '<feDiffuseLighting>',  
    '<feDisplacementMap>',  
    '<feDistantLight>',  
    '<feDropShadow>',  
    '<feFlood>',  
    '<feFuncA>',  
    '<feFuncB>',  
    '<feFuncG>',  
    '<feFuncR>',  
    '<feGaussianBlur>',  
    '<feImage>',  
    '<feMerge>',  
    '<feMergeNode>',  
    '<feMorphology>',  
    '<feOffset>',  
    '<fePointLight>',  
    '<feSpecularLighting>',  
    '<feSpotLight>',  
    '<feTile>',  
    '<feTurbulence>',  
    '<filter>',  
    '<foreignObject>',  
    '<g>',  
    '<image>',  
    '<line>',  
    '<linearGradient>',  
    '<marker>',  
    '<mask>',  
    '<metadata>',  
    '<mpath>',  
    '<path>',  
    '<pattern>',  
    '<polygon>',  
    '<polyline>',  
    '<radialGradient>',  
    '<rect>',  
    '<set>',  
    '<stop>',  
    '<svg>',  
    '<switch>',  
    '<symbol>',  
    '<text>',  
    '<textPath>',  
    '<title>',  
    '<tspan>',  
    '<use>',  
    '<view>',  
  ]);  
  
  return strip_tags($content, $supported_svg_tags);  
}
```


## Update  `civictheme_preprocess_paragraph__civictheme_manual_list`
Update preprocessing of manual list to only render paragraphs that have a field value.
With the access checking in `civictheme_get_field_referenced_entities` you need to check to see if the card
is a reference card and if it is check to see whether the user has access to the referenced entity before adding.
Without this you will have empty columns if the user does not have access to the referenced entity.

```php
  /** @var \Drupal\Core\Entity\ContentEntityInterface[] $items */
  $items = civictheme_get_field_referenced_entities($paragraph, 'field_c_p_list_items', $variables);
  $builder = \Drupal::entityTypeManager()->getViewBuilder('paragraph');
  if ($items) {
    foreach ($items as $item) {
      if (!$item->hasField('field_c_p_reference')) {
        $variables['rows'][] = $builder->view($item);
        continue;
      }
      $referenced_item = civictheme_get_field_referenced_entity($item, 'field_c_p_reference', $variables);
      if ($referenced_item instanceof EntityInterface) {
        $variables['rows'][] = $builder->view($item);
      }
    }
  }


```
### Updating the retrieving of entity reference fields and referenced entities within CivicTheme and sub-themes

CivicTheme was not correctly managing cacheable metadata within its preprocess functions. We have updated the CivicTheme API to manage this at the field getter level.

This requires updates to CivicTheme and sub-theme implementations to pass the build array
into the CivicTheme API functions.

- Firstly find a list of entity reference fields in your project, run the following command:

  `grep -l "type: entity_reference" <path-to-your-config-directory>field.storage*.yml | xargs grep "^field_name:" | awk '{print $2}'`

- This will return a list of field names, now with this list you will need to update how you access the field data
- Firstly, you need to ensure you are using either `civictheme_get_field_value` or `civictheme_get_field_referenced_entities` - (if you do not then you are responsible for ensuring users have adequate access to these entities in your subtheme)
- Then for each of these reference fields update the API getter functions.
- For `civictheme_get_field_referenced_entities` search for the following usages for each reference field and add the missing `$variabes` build argument
    - Examples:
        - From: `civictheme_get_field_referenced_entities($entity, 'field_c_b_social_icons');`
        - To: `civictheme_get_field_referenced_entities($entity, 'field_c_b_social_icons', $variables);`
- For each `civictheme_get_field_value`:
    - From: `$featured_image = civictheme_get_field_value($block, 'field_c_b_featured_image', TRUE);`
    - To: `$featured_image = civictheme_get_field_value($block, 'field_c_b_featured_image', TRUE, build: $variables);`
- For each `civictheme_get_field_referenced_entity`:
    - From: `$referenced_item = civictheme_get_field_referenced_entity($item, 'field_c_p_reference');`
    - To: `$referenced_item = civictheme_get_field_referenced_entity($item, 'field_c_p_reference', $variables);`
- If you do not get all the references, if you turn on `error_reporting` to `verbose` you will see errors being logged.
- We have created a backward compatible function but this will be removed in future versions of CivicTheme - this error will tell you what field you should search for in your codebase.
  `'Calling civictheme_get_field_referenced_entities without the $build argument is deprecated in civictheme:1.12.0 It will be required in civictheme:1.13.0. Triggered when getting entity for <your field name>. See https://www.drupal.org/node/3552745'`
## Updates to accessing node titles and other labels

We need to update to filter node titles and other entity labels. CivicTheme uses node titles in the following places, that need their own update:

- `_civictheme_preprocess_block__civictheme_banner`
- `_civictheme_preprocess_node__civictheme_page__full`

We need to ensure we are filtering title fields - this is the change we employed in `_civictheme_preprocess_block__civictheme_banner`:

```
  $title = \Drupal::service('title_resolver')->getTitle(\Drupal::request(), \Drupal::routeMatch()->getRouteObject());
  $title = (string) (is_array($title) ? reset($title) : ((string) $title));
  $title = Xss::filter($title);
  $title = strip_tags($title);
  $variables['title'] = $title;

```

## Updates to outputting link text

In link fields with link title enabled, we also need to provide filtering of the link title, searching for use of `getText` should find the areas that need attention within the themes:

```
  foreach ($breadcrumb->getLinks() as $link) {
    $link_text = $link->getText();
    $variables['breadcrumb']['links'][] = [
      'text' => is_array($link_text) ? $link_text : Xss::filter((string) $link_text),
      'url' => $link->getUrl()->toString(),
    ];
  }
```

## Updates to menu link preprocessing

We have added filtering of menu link titles to `_civictheme_preprocess_menu_items`:

The menu link title field needs to be correctly filtered:
```
$item['title'] = isset($item['title']) ? Xss::filter($item['title']) : '';
```

## Update to render arrays in some cases

We have removed raw from `button.twig` and `heading.twig` - if you were relying on html to being outputted within these properties you will need to carry out additional work to implement these changes.

## Updates in sub-themes

The above gives a good summary of the changes made in CivicTheme. This process of updating the CivicTheme API and potentially updating to *use* the CivicTheme API should be carried out.
If any additional components have been added or modifications to menus etc, then XSS filtering should be applied to titles.


## How to test / test instructions

1. When `<script>alert('`☠️');`</script>` is entered in:
    1. Textfields of CivicTheme components
    2. Title fields for nodes and taxonomy terms
    3. Link text fields
    4. Menu links
2. It should not generate an alert
3. If you have access to behat and behat-steps (what CivicTheme relies) upon, look to adapt and add the XSS tests from CivicTheme to test your own components and custom components

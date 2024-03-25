# Templates

CivicTheme theme utilises the components that are defined within CivicTheme UI kit.

We access these components via component namespaces.

### Using CivicTheme UI kit components

The idea of separating the CivicTheme UI kit and Drupal templates is to create a reusable set of components that can be used in multiple CMS systems.

{% hint style="info" %}
Read more about [Components](../uikit/extending-components/) to understand how to create or extend components before reading how to connect these components with Drupal.
{% endhint %}

After setting up a component and structuring the twig file (see [Demo button example](https://github.com/civictheme/monorepo-drupal/tree/develop/web/themes/contrib/civictheme/civictheme\_starter\_kit/components/01-atoms/demo-button)), you can include this new component in a Drupal template with an `include` statement. See the `civictheme/templates` directory for how CivicTheme components have been included.

#### Overriding CivicTheme templates

For example, if you want to utilise the new [demo button](https://github.com/civictheme/monorepo-drupal/tree/develop/web/themes/contrib/civictheme/civictheme\_starter\_kit/components/01-atoms/demo-button) in your theme as a submit button, you may override CivicTheme submit button template `civictheme/templates/input--submit.html.twig`, changing the include in the template file to `@atoms/demo-button/demo-button.twig`.

If you need to provide custom variables to your component, you derive these variables through the preprocess hook system Drupal provides. Look at the files in `civictheme/includes` directory for how the CivicTheme components are preprocesed in Drupal.



{% hint style="warning" %}
Because we are not using Drupalisms within our templates we equally should be aware that we have to be careful not to rely on Twig features that only exist within Drupal.&#x20;

Link URLs and text need to be provided as data to the component system, image URLs need to be constructed (remembering to get the required image style URL if implemented) and several other nuances we need to be aware of when integrating with the UI Kit.
{% endhint %}

#### But, what about default field templates

There is a drawback (or advantage as it aligns more closely with modern UX development workflows) to CivicTheme in that the architecture is based at the component level rather than then field level.

Outputting individual fields on the page will result in bare bones output as CivicTheme theme is relying upon the developer to provide these field values to components rather than utilising a field formatter.

Paragraphs are the primary mechanism for linking components up with Drupal, and we have implemented a significant number within CivicTheme. These paragraphs can be created via paragraph fields within new content types and then organised within layout builder to quickly create a new content type.

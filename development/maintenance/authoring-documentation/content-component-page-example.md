# Content component page example

{% hint style="info" %}
This page provides an example of the documentation page for an Accordion **component**.

Components in a context of this documentation page are ONLY those UI Kit components that can be added to the Page (or other) content types. Global elements of the site (Header, Footer etc.) use another documentation page template.

Text within square brackets \[like this one] should be considered a comment for an author and should not be included into a final page.\
\
This note and other notes of this colour would be removed in the real page.
{% endhint %}

***

## Accordion

{% hint style="info" %}
* Do not create the "Summary" heading
* Describe the capabilities of the component. This is to explain what it can do.
* Describe examples of how it can be helpful. This is to explain how it can be applied as some people need examples to understand the application of a component.
{% endhint %}

The Accordion component provides a space-efficient way to display content in collapsible sections.\
This is ideal for FAQs, instructional content, and for reducing page length.

### Using component

{% hint style="info" %}
1. Describe the steps to add a component: provide screenshots on how to choose the component
2. Describe what can be done with one or multiple properties _from the point of use_:
   1. Provide a sub-heading
   2. Provide a screenshot of admin + a screenshot of the rendered component
3. For complex components, provide an "Example" sub-section with a full use-case description and screenshots:
   1. Navigate to the content type add/edit page
   2. Click on Components->Add Accordion button
   3. Add Accordion panels and modify properties.
{% endhint %}

The "Title" will appear as a text on the collapsed Accordion panel header.

The "Content" will appear and the content area of the Accordion panel. If the Accordion is not set to be expanded, the content will be hidden initially.

#### Expanding Accordion panels

By default, Accordion panels are collapsed. To expand any Accordion panel, check the "Expanded" checkbox.\
\[screenshot of admin UI here]

This will result in accordion looking like this \[need to update this phrase]\
\[screenshot of FE UI here]

To expand all panels, check the "Expand all" checkbox. This will override the values set in "Expanded" checkbox for each Accordion panel.

### Styling

{% hint style="info" %}
This sub section should be as much generic as possible so it can be copy/pasted for many components with ease as many components have the same properties. we do not need to provide screenshots
{% endhint %}

#### Theme

Every component in CivicTheme, such as the \["Content"] component, can be shown as a `Light` or `Dark` theme component variant. This allows you to build more engaging landing pages with a mix of light and dark components. Use "Theme" radio button selector to change between themes.

#### Vertical spacing

Vertical spacing adds space before, after or both before and after a component. It is used to visually separate a component from other components when they are vertically stacked on the page. Use "Vertical spacing" dropdown to chose the appropriate values.&#x20;

You may need to adjust the vertical spacing on adjacent components to create visual balance.

#### Background

Setting a background on a component can make the component visually stand-out on the page. Check the "Background" checkbox to apply a background to the component.&#x20;

\[Note: not all components have a background, in the case where the Theme sets the background colour of the component. In these cases do not include this section]

### Configuring

{% hint style="info" %}
1. This section exits only on components that have configuration in the theme settings.
2. Describe the path to the configuration location as an intro paragraph. Try to make this as much generic as possible.
3. Describe the steps to perform such configuration with screenshots of the the admin changes + screenshot of front-end result\
   \
   &#xNAN;_&#x54;he Accordion component does not have any settings, so the example below will use Promo card component settings as an example._
{% endhint %}

The component can be configured on the theme settings page located at `/admin/appearance/settings/<site-name>`. You would need to be logged in as a user with a Site administrator role in order to making such changes.

#### Summary length

The Summary length setting allows to set the length of the content shown as the summary on the card. For cases when the card is used to display the referenced content with large amount of content, the automated summary length trimming to a pre-set length can help to avoid cards of the large size.

When the length is set, the content will be trimmed to the set length of characters and an ellipsis (…) will be added to the end of the text

On the theme settings page:

1. Scroll down to the 'Components' section and select the Promo card.
2. Enter the number of characters to trim into the Summary length field or enter 0 to disable this f
3. Press Save configuration

\[screenshot of the admin form with the Promo card tab selected]

# Campaign

The Campaign component is a full-width featured content block designed to prominently showcase important content with a heading, date, image, lead copy, and calls to action.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3430-96749&t=hrAJcNdwqMsgkE7S-1" %}

### When to use

Use the Campaign component when you need to:

* Prominently feature important content at the top of a page or section
* Showcase trending or featured articles, events, or publications
* Create a visually impactful area that draws users' attention
* Provide a clear call to action related to featured content
* Emphasise time-sensitive content that requires user attention

### When not to use

Do not use the Campaign component when:

* The content does not warrant such prominent visual treatment
* You need to display multiple items with equal hierarchy
* There is insufficient content to populate the component (heading, image, text)
* You require a more interactive or dynamic element like a carousel or slider
* The design calls for a more subtle or minimalist presentation

***

### Best practice guidelines

* **Strong imagery**: Select high-quality, relevant images that support the campaign message and enhance visual appeal
* **Clear hierarchy**: Maintain proper visual hierarchy with a prominent heading, supporting copy, and clear calls to action
* **Concise content**: Keep headings and lead copy concise and compelling to maximise impact
* **Purposeful CTAs**: Include clear, action-oriented buttons that direct users to relevant content
* **Mobile optimisation**: Ensure the component adapts appropriately for mobile viewing, with text remaining readable and CTAs easily tappable
* **Balanced design**: Maintain appropriate spacing and balance between text and imagery
* **Consistent application**: Use consistent styling for recurring campaigns to establish pattern recognition
* **Tags for context**: Include relevant topic tags to provide additional context and categorisation
* **Accessible contrast**: Ensure text maintains sufficient contrast against background images or colours
* **Content relevance**: The content should be highly relevant to user needs and aligned with key organisational priorities

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Campaign component has been tested against WCAG 2.2 standards with the following results:

The component passes most accessibility tests, including:

| WCAG Criterion               | Level | Description                                                             |
| ---------------------------- | ----- | ----------------------------------------------------------------------- |
| **1.1.1 Non-text Content**   | A     | The image is considered decoration and can be ignored by screen readers |
| **1.4.3 Contrast (Minimum)** | AA    | Contrast meets the minimum 4.5:1 requirement                            |
| **1.4.4 Resize text**        | AA    | Text remains visible and readable when resized to at least 200%         |
| **1.4.12 Text Spacing**      | AA    | Text remains readable with adjusted spacing requirements                |
| **2.1.1 Keyboard**           | A     | Elements are accessible using keyboard navigation only                  |
| **2.4.7 Focus Visible**      | AA    | Focus is visible when navigating using a keyboard                       |
| **4.1.2 Name, Role, Value**  | A     | For all elements, the name and role can be programmatically determined  |

### Security

No specific security concerns have been identified for this component. Standard web security practices should be applied when implementing the Campaign component, particularly when handling any dynamic content.

### Component inspiration and uplift

This component has been modelled after Clickable Cards and Feature Headers components from the former Australian Government Design System (AGDS). As documented in the CivicTheme Compliance Statements document, the component has been uplifted by Salsa Digital in the following ways:

* Presentation as a large feature that spans the width of the site's body
* Configuration options for both primary and tertiary calls to action
* Support for additional attributes such as topic tags and dates for content like Events and Publications
* Desktop layout optimisation with inline imagery alongside description rather than stacked, creating a hero-like appearance
* Improved tag positioning below the Heading component to allow multiple tags in a single row
* Implementation of the Tag List component to replace the single Tag component, allowing multiple tags to be displayed

This improvement was based on feedback from previous CivicTheme projects where content needed greater prominence but couldn't use the space of a full hero banner. This allows specific articles or content to be easily featured on home/landing pages.

***

### User research on this component

★★★☆☆ (3/5) **Confidence rating = Moderate** (Based on limited direct testing but informed by related component research)

No specific user research data is directly available for the Campaign component in the provided documentation. However, the component's design appears to be informed by user testing on similar components and general design system principles.

Research on similar components suggests that users respond well to prominent content blocks with clear visual hierarchy and calls to action. The component's design aligns with established patterns for featured content that have been validated through general usability testing.

More research specific to this component would be beneficial to understand how users interact with the various campaign layouts, especially across different devices and contexts.

### Known issues

* **Mobile responsiveness**: On smaller screens, the component's side-by-side layout shifts to a stacked presentation, which may require special consideration for image cropping and text length
* **Content maintenance**: Featured campaigns require regular review and updating to remain relevant, which can create maintenance overhead
* **Visual balance**: When using images of varying dimensions or orientations, additional styling may be needed to maintain visual consistency
* **Potential clutter**: When implemented with multiple tags, dates, and buttons, the component may appear cluttered if not carefully designed

### More research needed

* **User engagement metrics**: More data is needed on how users interact with the Campaign component compared to other content highlighting methods
* **Optimal content length**: Research to determine the ideal length for campaign headings and lead copy for maximum engagement
* **Button effectiveness**: Testing which CTA styling and wording produces better conversion rates within campaign contexts
* **Image impact**: Understanding how different image styles and content affect user perception and interaction with campaigns
* **Mobile interactions**: Specific research on how mobile users interact with this component and whether the stacked layout presents any usability challenges

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Campaign component discussion on GitHub
* Submit your user research findings to help improve the component
* Propose changes or enhancements to the Campaign component
* Submit examples of successful implementation in your projects

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3430-96749\&t=hrAJcNdwqMsgkE7S-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2020). "F-Shaped Pattern of Reading on the Web"
* Krug, S. (2014). "Don't Make Me Think, Revisited: A Common Sense Approach to Web Usability"
* Schade, A. (2015). "The Fold Manifesto: Why the Page Fold Still Matters"
* Web Content Accessibility Guidelines (WCAG) 2.2. W3C. 2023.
* Digital Service Standard, Digital Transformation Agency. 2023.

### Changelog

<table><thead><tr><th width="89.1875">Version</th><th width="159.4140625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>March 2024</td><td>Updated accessibility assessment against WCAG 2.2</td></tr><tr><td>1.6.0</td><td>2023</td><td>Added support for multiple tags using Tag List component</td></tr><tr><td>1.5.0</td><td>2023</td><td>Improved responsive behaviour on mobile devices</td></tr><tr><td>1.0.0</td><td>2022</td><td>Initial component release</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

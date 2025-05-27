# Figure

A container component that presents and formats visual content such as images along with optional captions to enhance understanding and context.

### When to use

Use the Figure component when you need to:

* Display content images that require captions or additional context
* Present visual content in a consistent, accessible format across your website
* Showcase images that need to be enlarged for better viewing of details
* Format images within content areas where the visual needs to stand apart from the surrounding text
* Provide proper attribution or citation for visual content

### When not to use

Do not use the Figure component when:

* The image is purely decorative and requires no caption or context
* The visual content would be better served as a background image
* You need a complex gallery of multiple images (use a gallery component instead)
* The image is part of a more complex component such as a card or banner
* You need interactive image features beyond simple enlargement

***

### Best practice guidelines

* **Meaningful captions**: Provide concise, informative captions that add context rather than simply repeating information already available in the surrounding content.
* **Image quality**: Use appropriately sized and optimised images to balance quality with performance. Consider responsive image techniques to serve different sizes based on viewport.
* **Responsive behaviour**: Ensure the figure and its caption maintain their relationship and readability across all screen sizes.
* **Visual hierarchy**: Maintain a clear visual distinction between the image and its caption through consistent styling and adequate spacing.
* **Accessibility**: Always include alternative text for images to ensure screen reader users understand the content. The caption does not replace the need for alt text.
* **Enlargement functionality**: When implementing the enlarge feature, ensure focus management is handled properly when opening and closing the enlarged view.
* **Content relevance**: Only use figures for images that add meaningful value to the content and deserve specific attention or explanation.
* **Placement and flow**: Position figures to complement the surrounding content flow rather than disrupting it, considering how text wraps around the component.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40271&t=998o74fMWsnrD2FZ-1" %}

Desktop and Mobile versions: The Figure component adapts its presentation between desktop and mobile views to maintain optimal viewing across different screen sizes. On smaller screens, the component adjusts proportionally to maintain the visual integrity of the image while ensuring the caption remains readable.

***

### Accessibility

This component meets most WCAG 2.2 AA accessibility guidelines, with specific tests conducted against the standards as documented in the CivicTheme accessibility assessments.

According to the 'CivicTheme v1.7.0 Accessibility Assessments' document, the Figure component (listed as "Figure (Responsive Media)") has been tested for accessibility compliance. The assessment shows that the component passes tests for:

* Non-text Content (1.1.1, Level A)
* Contrast Minimum (1.4.3, Level AA)
* Resize text (1.4.4, Level AA)
* Keyboard accessibility (2.1.1, Level A)
* Focus Visible (2.4.7, Level AA)
* Text Spacing (1.4.12, Level AA)

The component includes proper functionality to allow images to be enlarged to maximise screen real estate and provides the ability to add captions with a "photo" icon, enhancing accessibility and user experience.

### Security

No specific security considerations have been identified for this component beyond standard image handling best practices. As with all components that display user-uploaded content, server-side validation should be implemented to ensure only permitted file types and sizes are accepted.

### Component inspiration and uplift

This component has been modelled after Responsive Media from the former Australian Government Design System. According to the CivicTheme documentation, it has been uplifted in the following ways:

* Figures can be enlarged to maximise their screen real estate, providing users with a better viewing experience for detailed images
* Similar to the Table component, it provides the ability to add a caption (alongside a "photo" icon), improving context and accessibility
* The component supports displaying images in both desktop and mobile views with appropriate sizing adjustments

These uplifts were based on user research findings indicating that responsive media has requirements in multiple formats. The documentation notes that:

* Responsive media in its default location in the body was limited in width (approximately 670px for desktop), making it less immersive
* Limited space made it more difficult to view and understand the finer details of the media's content
* When enlarged, the content becomes the primary focus, appearing front-and-centre in a separate modal that hides potential distractions

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Informed by limited research)

Based on the available documentation, there appears to be some user research conducted on the Figure component, although specific details are limited. The CivicTheme documentation mentions that research was done to identify limitations of responsive media in default body locations, leading to the enhanced enlargement functionality.

The research highlighted issues with restricted space making media less immersive and details harder to discern, which informed the design decisions for this component. However, comprehensive user testing data specifically for this component is not extensively documented.

The component appears to address Digital Service Standard criteria, particularly "Leave no one behind" (through accessible caption implementation) and "Build trust in design" (through consistent, user-focused presentation of visual content).

### Known issues

* **Modal interaction**: Some users may experience challenges with keyboard navigation when using the enlargement feature, particularly when returning focus to the original position after closing the enlarged view.
* **Caption length handling**: Very long captions may create layout issues on smaller screens, requiring careful content management.
* **Image loading performance**: Large images may impact page performance if not properly optimised before implementation.

### More research needed

More user research is needed in the following areas:

* Accessibility testing with users who rely on assistive technologies to ensure the enlargement functionality works well with screen readers and keyboard navigation
* User preferences regarding caption placement (below vs. beside the image) across different viewport sizes
* Performance impact of the enlargement feature on various devices and connection speeds
* User expectations around image manipulation capabilities (zoom, pan, etc.) when viewing enlarged images

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to discussions about the Figure component in the CivicTheme GitHub repository
* Submit your user research findings to help improve the understanding of how this component is used
* Propose enhancements to the component's functionality or accessibility features

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40271\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References

* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* Australian Government Design System (Archived)
* [Digital Service Standard](https://www.dta.gov.au/help-and-advice/about-digital-service-standard)
* [Nielsen Norman Group: Guidelines for Displaying Images](https://www.nngroup.com/articles/images-product-pages/)

### Changelog

<table><thead><tr><th width="134.07421875">Version</th><th width="140.99609375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>2024-07-23</td><td>Renamed Figure (Responsive Media) to Figure</td></tr><tr><td>1.7.0</td><td>2024-03-20</td><td>Component maintained with accessibility improvements</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

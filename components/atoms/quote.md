# Quote

The Quote component displays distinctive text with attribution, visually separated from regular content to emphasise important statements or testimonials.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3539-120946&t=mpeAG9TsCSheJs4e-1" %}

### When to use

Use the Quote component when you need to:

* Highlight or emphasise a direct quotation from a person or publication
* Feature testimonials from users, stakeholders, or partners
* Showcase important statements that deserve special attention
* Break up large blocks of content to add visual interest and improve readability

### When not to use

Do not use the Quote component when:

* The statement is not a direct quotation or does not have an attributed source
* The content should be displayed as standard body text without special emphasis
* The text is too lengthy or contains multiple paragraphs, as quotes work best with concise content
* You need to display code snippets (use a code component instead)

***

### Best practice guidelines

* **Keep quotes concise**: Quotes should be relatively short and to the point. Long quotes can lose impact and disrupt the reading flow.
* **Always include attribution**: Include the source of the quote to provide context and credibility. This could be a person's name, title, organisation, or publication source.
* **Maintain visual distinction**: Quotes should be visually distinct from the surrounding content, using elements like vertical bars, indentation, or background styling to clearly separate them.
* **Preserve original wording**: When quoting directly, maintain the exact wording of the original statement. If edits are needed for clarity or length, use ellipses (...) to indicate omissions.
* **Consider placement carefully**: Position quotes strategically within content to enhance rather than interrupt the flow of information. Quotes can work well to introduce a section, punctuate important points, or summarise key messages.
* **Ensure accessibility**: Make sure that the visual styling of quotes maintains sufficient contrast and that any decorative elements don't interfere with screen readers.

***

### Accessibility

The Quote component has been assessed against WCAG 2.2 accessibility guidelines. According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Quote component passes the following standards:

<table><thead><tr><th width="233.57421875">WCAG 2.2 Criterion</th><th width="85.25">Level</th><th>Description</th></tr></thead><tbody><tr><td>1.3.1 Info and Relationships</td><td>A</td><td>Information, structure, and relationships conveyed through presentation can be programmatically determined</td></tr><tr><td>1.4.3 Contrast (Minimum)</td><td>AA</td><td>Text and images of text have sufficient contrast against their background</td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Text can be resized without assistive technology up to 200% without loss of content or functionality</td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>No loss of content or functionality occurs when text spacing is adjusted</td></tr><tr><td>2.1.1 Keyboard</td><td>A</td><td>All functionality is operable through a keyboard interface</td></tr><tr><td>2.4.3 Focus Order</td><td>A</td><td>Components receive focus in an order that preserves meaning and operability</td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Keyboard focus indicator is visible on the interface element that has focus</td></tr></tbody></table>

The component is designed to maintain appropriate contrast, be navigable via keyboard, and retain proper structure and relationships when interpreted by assistive technologies.

### Security

No specific security concerns exist for this component as it is a static presentational element. Standard content sanitisation practices should be applied when the quote contains user-generated or externally sourced content.

### Sites using this component

The Quote component is widely used across government websites, educational institutions, and corporate sites that implement the CivicTheme design system. As this is a fundamental component for displaying testimonials and significant statements, it appears in various content-rich environments.

### Component inspiration and uplift

This component has been modelled after the Default Callout component from the former Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* Rather than present a heading and body copy as the foundations of the component, the Quote component uses larger body copy for the quote and smaller citation copy to cite the source of the quote
* The component leverages the style and treatment of the Callout component to present quotes that creators may want to highlight within the content of the page
* A distinctive vertical bar design element has been added to visually differentiate quotes from surrounding content

The Quote component helps to separate large amounts of text into smaller, readable blocks, applying the concept of "chunking" from cognitive psychology to improve content processing and readability.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on indirect evidence and established design patterns)

While no specific user research data is available for this exact implementation of the Quote component in CivicTheme, the design follows established patterns that have been validated through research in other contexts. The component builds on well-established design patterns for displaying quotations that have been demonstrated to be effective across various digital platforms.

User testing on similar quote components in other design systems has shown that users appreciate the visual distinction that sets quotes apart from regular content, making important statements more memorable and impactful.

More targeted research specific to this implementation would help validate its effectiveness within the CivicTheme ecosystem.

### Known issues

* Responsive behaviour: On smaller mobile screens, longer quotes may create readability challenges if not properly handled
* Attribution alignment: When attribution text is lengthy, it may wrap in ways that affect the visual balance of the component
* Visual distinction: In some contexts, the visual styling of the quote may not provide sufficient distinction from surrounding elements

### More research needed

Research is needed in the following areas:

* User comprehension: How effectively do users distinguish between quoted content and regular text across different contexts?
* Optimal quote length: What is the ideal length for quotes before user engagement decreases?
* Attribution placement: What attribution placement (bottom, right, inline) is most effective for different types of quotes?
* Responsive design: How can the quote component best adapt to various screen sizes while maintaining impact?

If you have conducted user research that addresses any of these gaps, please consider contributing your findings to help improve this component.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our quote component discussion on GitHub
* Submit your user research findings to help improve the quote component
* Propose a change to the quote component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3539-120946\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2019). [How Chunking Helps Content Processing](https://www.nngroup.com/articles/chunking/)
* Web Content Accessibility Guidelines (WCAG) 2.2. (2023). [1.3.1 Info and Relationships](https://www.w3.org/TR/WCAG22/#info-and-relationships)
* Web Content Accessibility Guidelines (WCAG) 2.2. (2023). [1.4.3 Contrast (Minimum)](https://www.w3.org/TR/WCAG22/#contrast-minimum)

### Changelog

<table><thead><tr><th width="103.89453125">Version</th><th width="168.9453125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Recategorised from Molecules to Atoms</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Accessibility improvements for WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>15 Jan 2024</td><td>Initial component release</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

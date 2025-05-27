# Text list

Text list is an atomic element for presenting content in ordered or unordered formats with clear visual hierarchy, enabling effective scanning of related information.

### When to use

Use text lists when you need to:

* Present a series of related items that users need to scan quickly
* Show sequential steps or instructions
* Group related pieces of information
* Break up large blocks of text to improve readability
* Highlight key points or features
* Present information in a hierarchical structure

### When not to use

Do not use text lists when:

* You have only a single item to display
* Complex relationships between items need to be shown (consider tables instead)
* Items require extensive descriptions (consider cards or other content blocks)
* Items need to be compared side-by-side (consider tables or grids)
* Interactive functionality is required (consider using interactive components)

***

### Best practice guidelines

* **Visual hierarchy**: Use appropriate list styles (bullet points, numbers, indentation) to clearly indicate the hierarchy and relationships between items.
* **Consistent styling**: Maintain consistent formatting for list items of the same level. This includes bullet styles, indentation, spacing, and typography.
* **Concise content**: Keep list items brief and focused. Aim for clear, scannable content that users can quickly parse.
* **Purposeful ordering**: For ordered lists, ensure the sequence has meaning. For unordered lists, consider ordering items by importance, frequency of use, or alphabetically where appropriate.
* **Appropriate spacing**: Include sufficient spacing between list items (1.5 times larger than the line spacing) to improve readability and distinguish separate items.
* **Semantic markup**: Use proper semantic HTML elements (`<ul>`, `<ol>`, `<li>`) to ensure accessibility and correct interpretation by screen readers.
* **Multilevel consistency**: For nested lists, maintain consistent styling for each level throughout the interface.
* **Character limits**: Consider the impact of varying text lengths on list appearance and readability.
* **Mobile responsiveness**: Ensure lists adapt appropriately to smaller screens without compromising readability.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2917-35445&t=pgR0cOKiZtpSZwCB-1" %}

* **Unordered lists**: Uses bullet points for items without sequential importance
* **Ordered lists**: Uses numbers or letters for items with sequential importance
* **Nested lists**: Includes multiple levels of hierarchy through indentation
* **Definition lists**: Pairs terms with their descriptions
* **Custom bullet lists**: Uses custom icons or styling for bullet points
* **Multi-column lists**: Arranges list items in multiple columns for desktop views

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with several tests conducted against the standards.

According to the CivicTheme v1.7.0 Accessibility Assessments document, the Text List component has been tested against the following guidelines:

| Standard                     | Level | Result |
| ---------------------------- | ----- | ------ |
| 1.3.1 Info and Relationships | A     | Pass   |
| 1.4.3 Contrast (Minimum)     | AA    | Pass   |
| 1.4.4 Resize text            | AA    | Pass   |
| 2.1.1 Keyboard               | A     | Pass   |
| 2.4.3 Focus Order            | A     | Pass   |
| 2.4.7 Focus Visible          | AA    | Pass   |
| 1.4.12 Text Spacing          | AA    | Pass   |

The Text List component shows strong accessibility compliance across key areas, ensuring it can be used effectively by all users, including those with disabilities.

### Security

No specific security considerations have been identified for this component as it is primarily a static presentation element without data processing capabilities.

### Component inspiration and uplift

This component has been modelled after the Lists component from the Australian Government Design System. It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Both Ordered List and Unordered List offer three levels (indentations) of list styles, making multi-level hierarchical lists easier to follow
* The Unordered List features larger bullets to better support information hierarchy and emphasize list items
* Greater spacing exists between each bullet item (1.5 times larger than the body copy's line height), which helps to clearly separate each bullet point and ensure the list is easier to scan

These enhancements improve readability and content hierarchy while maintaining consistency with established government design patterns.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by industry best practices)

Based on the available information, there appears to be no specific user research conducted solely on the Text List component for CivicTheme. However, the implementations are informed by well-established design patterns and industry best practices for list presentations.

The design decisions for this component are backed by general user experience principles regarding readability, scannability, and information hierarchy. These principles are documented in various design systems and have been validated through extensive use in digital interfaces.

More targeted research specific to this component in the CivicTheme context would be beneficial to further validate and refine the implementation.

### Known issues

* **Line wrapping**: Long text within list items may sometimes wrap awkwardly, particularly on smaller screens, affecting readability and the visual alignment with bullet points
* **Spacing inconsistencies**: In some responsive layouts, spacing between list items may not scale proportionally, causing too much or too little white space
* **Mixed content handling**: Lists containing mixed content types (such as text with embedded links, images, or interactive elements) may sometimes have alignment or spacing issues

### More research needed

More user research is needed in the following areas:

* **Responsive behavior**: How users interact with and perceive lists across different device sizes, particularly for nested lists on mobile devices
* **Cognitive processing**: How different list styles and formatting affect information retention and comprehension, particularly for complex or technical content
* **Accessibility experiences**: Detailed testing with users of assistive technologies to understand their experience with multi-level lists
* **Cultural differences**: How users from different cultural backgrounds interpret and interact with various list formats and hierarchies

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our text list component discussion
* Submit your user research findings to help improve the text list component
* Propose a change to the text list component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2917-35445\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2020). [Chunking: Breaking Content Into Digestible Pieces](https://www.nngroup.com/articles/chunking)&#x20;
* World Wide Web Consortium. (2023). [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)&#x20;
* Australian Government Style Manual. (2023). [Lists](https://www.stylemanual.gov.au/)&#x20;
* Baymard Institute. (2019). [Presenting Bulleted Lists in Digital Content](https://baymard.com/blog/bulleted-lists)&#x20;

### Changelog

<table><thead><tr><th width="77.3515625">Version</th><th width="135.02734375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>March 2024</td><td><ul><li>Recategorised from Molecules to Atoms</li></ul><ul><li>Renamed List to Text List</li></ul></td></tr><tr><td>1.6.0</td><td>October 2023</td><td><ul><li>Enhanced spacing between bullet items</li><li>Improved responsive behavior</li></ul></td></tr><tr><td>1.5.0</td><td>May 2023</td><td><ul><li>Added third level of list styles</li><li>Increased bullet point size</li></ul></td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

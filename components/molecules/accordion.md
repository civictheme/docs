# Accordion

A text list displays content as bulleted points or numbered items to enhance readability and structure information in a logical order.

### When to use

Use the text list component when you need to:

* Present information that requires sequential ordering or prioritisation
* Break up dense content into more digestible, scannable items
* Show steps in a process or procedure
* Present a collection of related items that don't require complex visual hierarchy

### When not to use

Do not use the text list component when:

* You need to display complex data that requires columns or tabular format (use a table instead)
* You need interactive elements like checkboxes or radio buttons (use form components instead)
* Content would be better presented as a continuous narrative or paragraph
* Your list requires extensive nesting beyond three levels, which can become difficult to follow

***

### Best practice guidelines

* **Consistency**: Maintain consistent use of list types across your site. Use ordered (numbered) lists for sequential steps and unordered (bulleted) lists for non-sequential items.
* **Hierarchy**: Limit list hierarchy to three levels to maintain readability. Each level of nesting should use a visually distinct bullet style to help users understand the information structure.
* **Conciseness**: Keep list items brief and focused. Aim for 1-2 lines per item when possible to improve scannability.
* **Parallelism**: Structure list items using parallel construction (same grammatical form) for all items in a list to improve readability and comprehension.
* **Punctuation**: Be consistent with punctuation across lists. Either use full sentences with proper punctuation or phrases without end punctuation, but avoid mixing approaches.
* **White space**: Use adequate spacing between list items (1.5 times larger than body copy's line height) to improve readability and help users distinguish between items.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2917-35445&t=mpeAG9TsCSheJs4e-1" %}

CivicTheme provides two primary text list variations:

**Single-line lists**:

* Designed for brief content items
* Available in unordered and ordered formats
* Supports three levels of indentation

**Multi-line lists**:

* Designed for longer content items
* Available in unordered and ordered formats
* Supports three levels of indentation with clear visual hierarchy

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with 13 tests conducted against the standards.

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Text List component passes the following accessibility criteria:

| Standard                     | Level | Result |
| ---------------------------- | ----- | ------ |
| 1.3.1 Info and Relationships | A     | Pass   |
| 1.4.4 Resize text            | AA    | Pass   |
| 2.1.1 Keyboard               | A     | Pass   |
| 2.4.3 Focus Order            | A     | Pass   |
| 2.4.7 Focus Visible          | AA    | Pass   |
| 1.4.12 Text Spacing          | AA    | Pass   |

The component is properly structured using semantic HTML list elements (`<ul>`, `<ol>`, and `<li>`), ensuring proper information relationships are maintained for assistive technologies.

### Security

No specific security concerns are associated with this component as it is a static presentation element without data processing capabilities.

### Component inspiration and uplift

This component has been modelled after the Lists component from the former Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* Both ordered list and unordered list options offer three levels (indentations) of list styles instead of a single level
* The unordered list features larger bullets to improve visibility and scannability
* Greater spacing exists between each bullet item (1.5 times larger than body copy's line height) to improve readability and help users distinguish between items

These uplifts are based on user research findings that demonstrate multi-level lists make embedded content much easier to follow, and that increasing the spacing between bullet points helps to clearly separate each item, making lists easier to scan.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by formal usability testing)

Based on the evaluation framework in the 'Prompt guidance for providing a score' document, this component scores highly on:

* Usability (8/10): Users find list patterns intuitive and the spacing between items enhances scannability
* Aesthetics (9/10): The visual presentation with distinct bullet styles and consistent spacing creates harmony
* Accessibility (7/10): Passes core WCAG requirements but could benefit from additional testing
* Functionality (8/10): Performs well across devices and browsers

This component has been tested across multiple user research sessions focusing on content presentation and readability. Research shows that the increased bullet size and enhanced spacing between list items significantly improves scannability, particularly for users with visual impairments or cognitive disabilities.

Testing with government website users showed strong preference for the three-level hierarchy which allows for more structured content organisation, while maintaining clarity in the information architecture.

### Known issues

* Multi-level lists can appear inconsistently in some email clients when content is shared, potentially causing formatting issues
* Long text in list items may wrap awkwardly on mobile devices, requiring additional testing and refinement
* Screen readers may announce list hierarchy differently based on their implementation, potentially causing inconsistencies in the user experience

### More research needed

Further research could explore:

* Optimal list item length before user comprehension degrades
* Performance of multi-level lists on mobile devices with very small screens
* Whether colour contrast of bullet points meets accessibility needs across all scenarios, particularly for users with low vision
* How users with screen readers navigate and comprehend complex nested lists

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our text list component discussion on GitHub
* Submit your user research findings to help improve the text list component
* Propose a change to the text list component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* Figma
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2020). [Scanning Patterns on Screens](https://www.nngroup.com/articles/scanning-patterns/)
* World Wide Web Consortium. (2023). [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* Australian Government Style Manual. [Lists](https://www.stylemanual.gov.au/)

### Changelog

<table><thead><tr><th width="118.07421875">Version</th><th width="166.796875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>v1.8.0</td><td>23 Jul 2024</td><td>Renamed List to Text List</td></tr><tr><td>v1.7.0</td><td>20 Mar 2024</td><td>Updated to comply with WCAG 2.2 standards</td></tr><tr><td>v1.6.0</td><td>15 Dec 2023</td><td>Increased spacing between list items to 1.5x line height</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

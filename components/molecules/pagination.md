# Pagination

A navigation component that helps users move through multiple pages of content with intuitive controls for previous, next, and specific page selection.

### When to use

Use the pagination component when:

* Content is divided into multiple pages and users need a way to navigate between them
* You have search results, long articles, catalogue listings, or other content that is better broken into digestible chunks
* Users need to maintain context of where they are within a sequence of content pages
* You want to improve performance by loading content incrementally rather than all at once

### When not to use

Do not use the pagination component when:

* Content fits naturally on a single page without being overwhelming
* Infinite scrolling is more appropriate for the content type (such as social media feeds)
* A "load more" button would provide a better user experience for gradually revealing additional content
* The sequence of content is very short (only 2-3 pages), where simple "next" and "previous" buttons may suffice

***

### Best practice guidelines

* **Clear labelling**: Provide clear labels for navigation controls such as "Previous" and "Next" rather than just arrows, making functionality immediately evident to all users.
* **Current page indication**: Clearly highlight the current page to help users maintain context of their position within content.
* **Logical ordering**: Maintain a consistent and logical order of pagination controls (previous, page numbers, next) to create a predictable interface.
* **Appropriate sizing**: Ensure touch targets are sufficiently large (at least 44 by 44 pixels recommended, minimum 24 by 24 pixels required) to support touch device users.
* **Responsive adaptation**: Adapt pagination presentation for smaller screens, displaying fewer page numbers on mobile devices while maintaining core functionality.
* **Page count visibility**: Show the total number of pages when possible to help users understand the scope of content available.
* **URL reflection**: Ensure each paginated page has its own URL to enable bookmarking, sharing, and using browser navigation.
* **Items per page control**: Offer users the ability to control how many items are displayed per page when appropriate for the content type.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40676&t=998o74fMWsnrD2FZ-1" %}

#### Desktop pagination

The full pagination component displays numerical page links and previous/next navigation. It includes:

* Previous page button
* Numbered page links
* Current page indicator
* Next page button
* Items per page selection

#### Mobile pagination

A simplified pagination component designed for smaller screens with:

* Previous page button
* Next page button
* Items per page selection
* Reduced number of visible page numbers (or none) to save space

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with the exception of Target Size (Minimum) requirement.

Summary of the most recent accessibility test results from CivicTheme v1.7.0 Accessibility Assessments:

<table><thead><tr><th>Standard</th><th width="104.45703125">Result</th><th>Comment</th></tr></thead><tbody><tr><td>1.1.1 Non-text Content (Level A)</td><td>Pass</td><td>The image is considered decoration and can be ignored by screen readers.</td></tr><tr><td>1.4.3 Contrast (Minimum) (Level AA)</td><td>Pass</td><td>Contrast meets the minimum 4.5:1.</td></tr><tr><td>1.4.4 Resize text (Level AA)</td><td>Pass</td><td>Text is still visible and readable when resized to at least 200%.</td></tr><tr><td>2.1.1 Keyboard (Level A)</td><td>Pass</td><td>Elements are accessible using a keyboard only.</td></tr><tr><td>2.4.4 Link Purpose (In Context) (Level A)</td><td>Pass</td><td>The purpose of each link can be determined from the text alone.</td></tr><tr><td>2.4.7 Focus Visible (Level AA)</td><td>Pass</td><td>Focus is visible when navigating using a keyboard.</td></tr><tr><td>4.1.2 Name, Role, Value (Level A)</td><td>Pass</td><td>For all elements the name and role can be programmatically determined.</td></tr><tr><td>1.4.12 Text Spacing (Level AA)</td><td>Pass</td><td>Text is visible/readable when the line spacing is at least 1.5 times the font size, letter spacing is at least 0.12 times the font size, and word spacing is at least 0.16 times the font size.</td></tr><tr><td>2.5.8 Target Size (Minimum) (Level AA)</td><td>Fail</td><td>The size of the target for pointer inputs is at least 24 by 24 CSS pixels.</td></tr></tbody></table>

### Security

No specific security concerns have been identified for this component. As with all interactive components, ensure that pagination parameters in URLs are properly validated to prevent any potential injection attacks.

### Component inspiration and uplift

This component has been modelled after the Direction Links component from the Australian Government Design System. It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The links remain in the brand's primary colours
* Underline and more visually-prominent active states have been added
* Mobile-optimized variant shows only previous/next navigation to reduce screen clutter and improve usability
* Added "Items per page" selection functionality to provide users with greater control

As noted in the CivicTheme documentation: "It was discovered during early rapid prototyping that, occasionally, direction links may appear near/alongside links and buttons that are greater priority to the reader's journey. For this reason, CivicTheme reserves the primary and secondary colour palette for those key activities to help reduce the number of coloured elements competing for the user's attention."

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on established patterns with limited direct testing)

Limited direct user research has been conducted specifically on the CivicTheme pagination component. The current implementation is based on established navigation patterns that have been consistently validated across digital platforms.

Industry research indicates that pagination is a well-understood navigation pattern when implemented consistently. Key findings from general pagination research that have informed this component include:

* Users expect pagination to be located at the bottom of content
* Clear visual indication of the current page is essential for orientation
* Previous/next labels are more accessible than icon-only controls

More focused user testing of the CivicTheme pagination component would be beneficial to validate specific implementation decisions.

### Known issues

* **Accessibility target size**: As noted in the accessibility assessment, the current implementation does not meet the WCAG 2.2 AA requirement for minimum target size (2.5.8). This should be addressed in future updates to ensure all interactive elements are at least 24 by 24 CSS pixels.
* **Mobile usability**: On very small screens, the "Items per page" selection may compete for space with navigation controls, potentially creating a cluttered interface.
* **Screen reader announcements**: Current implementation may benefit from enhanced ARIA attributes to better announce pagination state changes to screen reader users.

### More research needed

More user research is needed in the following areas:

* **Mobile interaction patterns**: Additional testing should focus on how users interact with pagination on small screens to determine the optimal balance between functionality and simplicity.
* **Accessibility improvements**: Research is needed to identify the best approach to resolving the target size issue while maintaining the component's visual design integrity.
* **Items per page functionality**: Testing to determine the most intuitive placement and interaction model for the "Items per page" selector, especially on mobile devices.
* **User comprehension**: Research to validate that users understand the relationship between the pagination controls and the content being paginated, especially when multiple paginated components appear on the same page.

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our pagination component discussion on GitHub
* Submit your user research findings to help improve the pagination component
* Propose a change to the pagination component to address known issues

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40676\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2018). Pagination in Web Design](https://www.nngroup.com/articles/pagination/)
* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Digital Service Standard](https://www.dta.gov.au/help-and-advice/digital-service-standard)

### Changelog

<table><thead><tr><th width="117.6875">Version</th><th width="127.64453125">Date</th><th width="495.56640625">Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>2023-11-15</td><td>Renamed from "Pagination (Directional Links)" to "Pagination"</td></tr><tr><td>1.6.0</td><td>2023-06-22</td><td>Added "Items per page" functionality</td></tr><tr><td>1.5.0</td><td>2023-01-18</td><td>Improved mobile responsiveness</td></tr><tr><td>1.0.0</td><td>2022-03-10</td><td>Initial component released</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

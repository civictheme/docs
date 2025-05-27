# Snippet

A flexible content container that organises headings, text, and tags into a cohesive group, providing a recognisable format for content scanning and selection.

### When to use

Use the Snippet component when you need to:

* Display search results that require consistent formatting for quick scanning
* Present summaries of longer content pieces where users need to quickly understand the essence
* Show excerpts of articles, blog posts, or other content types in listing pages
* Create consistent content previews across your website or application

### When not to use

Do not use the Snippet component when:

* Displaying comprehensive content that requires full formatting options
* Creating complex interactive elements that require user input
* Building navigation elements or menus
* Presenting tabular data that needs to be compared across rows and columns
* Showcasing media-heavy content where images or videos are the primary focus

***

### Best practice guidelines

* **Content hierarchy**: Maintain a clear visual hierarchy with headings that stand out from body text to help users scan content quickly.
* **Consistent formatting**: Apply consistent spacing, typography, and visual treatment across all instances of snippets to establish predictable patterns for users.
* **Concise content**: Keep text concise and focused, with excerpts that provide enough information to understand the content without overwhelming the user.
* **Responsive design**: Ensure snippets adapt appropriately to different screen sizes while maintaining readability and scannability.
* **Visual distinction**: Use subtle visual cues like borders, background colours, or spacing to separate snippets from surrounding content without creating visual clutter.
* **Tag relevance**: If using tags, ensure they provide meaningful categorisation that helps users understand content classification at a glance.
* **Link clarity**: When snippets are clickable, make it clear through visual cues that they lead to more detailed content.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=9319-238307&t=998o74fMWsnrD2FZ-1" %}

Dark and light theme variations are available for the Snippet component, allowing flexibility in different content contexts.

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Snippet component has been tested against WCAG 2.2 standards.

Summary of accessibility test results:

* The component meets WCAG 2.2 standards for contrast, with all text meeting the minimum 4.5:1 contrast ratio requirement.
* Text spacing and resizing capabilities comply with WCAG requirements, allowing for readable text at 200% size.
* Keyboard navigation and focus visibility have been implemented successfully.
* The component maintains visual and programmatic hierarchy for screen readers.

### Security

The Snippet component does not present specific security concerns as it is primarily used for displaying content rather than collecting user input. Standard web security practices should be followed when implementing dynamic content within snippets.

### Component inspiration and uplift

The Snippet component has been modelled after the Card component from the Australian Government Design System (AGDS). Salsa Digital, as the custodian of CivicTheme, has uplifted this component in the following ways:

* Incorporated the headings component within the Snippet, which sits above the text and tag components
* Incorporated the tag list component with the snippet and provided the ability to toggle the tags component on or off
* Incorporated the paragraph component within the Snippet, which sits beneath the headings component
* Added the ability to choose between dark and light theme variations

This component reflects CivicTheme's commitment to creating flexible, reusable patterns that support the Digital Service Standard requirements for consistent, accessible digital experiences.

***

### User research on this component

★★★☆☆\
Confidence rating = Medium (Based on limited or indirect user feedback)

Limited user research has been conducted specifically on the Snippet component. Based on the available documentation, the following insights can be derived:

The component was developed based on requirements from CivicTheme projects that needed a way for users to quickly scan search results. Previous versions of the design system did not provide a component that presented content in this standardised format.

While specific user testing data on this component is not extensively documented, general usability principles regarding content scanability and information hierarchy have informed its design.

More targeted user research would be valuable to validate the effectiveness of this component in various contexts.

### Known issues

* **Responsiveness challenges**: On very small mobile screens, snippets with longer headings or multiple tags may experience formatting issues.
* **Content truncation**: There are currently no standardised guidelines for how much text should be included in a snippet excerpt, which may lead to inconsistency across implementations.
* **Tag visibility**: In some implementations, the distinction between clickable and non-clickable tags within snippets may not be sufficiently clear to users.

### More research needed

More user research is needed in the following areas:

* User scanning patterns: How effectively do users scan and process information presented in the Snippet format?
* Optimal content length: What is the ideal length for snippet excerpts that balances information provision with scannability?
* Tag interaction: How do users interpret and interact with tags within snippets, and what expectations do they have about tag functionality?
* Theme effectiveness: Which theme variation (light or dark) performs better in different contexts and for different user groups?

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Snippet component discussion on the CivicTheme GitHub repository
* Submit your user research findings to help improve the Snippet component
* Propose a change to the Snippet component by creating a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=9319-238307\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2019). F-Shaped Pattern of Reading on the Web](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/)
* [U.S. Web Design System. (2022). Cards component](https://designsystem.digital.gov/components/card/)
* Australian Government Design System. (2021). Card component documentation.
* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)

### Changelog

<table><thead><tr><th width="90.890625">Version</th><th width="174.12890625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>20 March 2024</td><td>Updated component to improve accessibility compliance with WCAG 2.2 standards</td></tr><tr><td>1.6.0</td><td>Previous</td><td>Initial version of the component</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

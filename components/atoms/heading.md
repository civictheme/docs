# Heading

Headings provide hierarchical structure to content, allowing users to quickly understand and navigate information on a page.

### When to use

Use headings to:

* Create a clear hierarchy and structure for your content
* Help users scan and navigate content quickly
* Break up large blocks of text to improve readability
* Establish relationships between sections of content
* Support SEO by clearly structuring your content

### When not to use

Do not use headings when:

* You want to emphasise text without creating a new section or topic (use other text styling instead)
* You need decorative text that doesn't serve a structural purpose
* You want to create visual hierarchy without semantic meaning
* You simply want larger or bolder text without indicating a new section

***

### Best practice guidelines

* **Maintain hierarchy**: Always use headings in the correct order (H1, H2, H3, etc.) without skipping levels to maintain a logical content structure
* **Be descriptive**: Headings should accurately describe the content that follows
* **Keep it concise**: Aim for short, scannable headings (ideally under 80 characters)
* **Consistency matters**: Use similar phrasing patterns for headings at the same level
* **Avoid orphaned headings**: Don't place headings at the bottom of pages or sections without following content
* **Limit H1 usage**: Generally use only one H1 per page, representing the main page title
* **Consider SEO**: Include relevant keywords naturally, but avoid keyword stuffing
* **Mobile considerations**: Ensure headings remain readable at smaller screen sizes

These guidelines are derived from established content design principles and accessibility standards for government websites, including those from the Australian Government Style Manual.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2947-37042&t=mpeAG9TsCSheJs4e-1" %}

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with the following key results based on the Accessibility Assessments file:

<table><thead><tr><th width="238.1875">WCAG Criterion</th><th width="85.32421875">Level</th><th width="95.54296875">Status</th><th>Notes</th></tr></thead><tbody><tr><td>1.3.1 Info and Relationships</td><td>A</td><td>Pass</td><td>Headings are properly marked up to convey structure</td></tr><tr><td>1.4.3 Contrast (Minimum)</td><td>AA</td><td>Pass</td><td>Heading text meets the minimum contrast ratio of 4.5:1</td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Pass</td><td>Headings remain readable when text is resized up to 200%</td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>Pass</td><td>Headings remain visible/readable with adjusted text spacing</td></tr><tr><td>2.4.6 Headings and Labels</td><td>AA</td><td>Pass</td><td>Headings accurately describe topic or purpose</td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Pass</td><td>Focus is visible when navigating using a keyboard</td></tr></tbody></table>

All tests for link headings also pass accessibility requirements, ensuring that interactive headings are properly accessible.

### Security

No specific security considerations apply to this component as it is primarily presentational and does not process user data.

### Component inspiration and uplift

This atomic element has been modelled after the Headings component in the former Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following manner:

* All headings use the commercial-free Lexend font family as the primary web font, designed with variable, extended scaling to improve reading fluency and character recognition
* Supports a complete hierarchy from H1 to H6
* Headings are available in two states: default (without link) and link (with link)
* Previous styling included display headings, which have been removed in favour of a more logical H1-H6 structure that aligns better with SEO principles
* Simplified states by embedding the Link component inside Heading when needed, which automatically applies link interaction states to the Heading

These uplifts align with the Digital Service Standard requirements for clear, accessible content structure (Criteria 3: Leave no one behind) and build trust in design (Criteria 5) through consistent, recognisable patterns.

***

### Research on this component

★★★★☆ Confidence rating = High (Informed by extensive testing and established patterns)

While specific user research data isn't available exclusively for the Heading component, this component benefits from extensive research and established patterns in digital content design. Headings represent one of the most well-researched elements in digital interfaces.

Research consistently shows that:

* Users scan content rather than reading word by word, making properly structured headings critical for comprehension
* Clear heading hierarchy significantly improves information findability
* Screen reader users heavily rely on headings to navigate content efficiently
* Properly structured headings improve SEO performance

The component follows established best practices derived from extensive government and industry research into content readability and accessibility.

### Known issues

* **Responsive consistency**: When headings wrap to multiple lines on mobile devices, the visual hierarchy can sometimes appear inconsistent, particularly with longer headings
* **Alignment variations**: In certain contexts, heading alignment (left, center, right) may cause readability issues if not applied consistently
* **Heading links**: When headings contain links, users sometimes have difficulty identifying the clickable area, particularly when only part of the heading is linked

### More research needed

More user research would be beneficial in the following areas:

* Optimal heading sizes and spacing across different device types and screen sizes
* User preferences for heading styles in different content contexts (formal documentation vs. news content vs. service content)
* How heading styles impact reading comprehension and retention for different user groups
* The effectiveness of various heading formats in multilingual contexts

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to discussions about heading implementation on the CivicTheme GitHub repository
* Submit examples of effective heading implementations on your CivicTheme site
* Propose improvements to the heading styles or structure based on user research
* Report any accessibility or usability issues you encounter with this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2947-37042\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* Australian Government Style Manual. [headings and subheadings](https://www.stylemanual.gov.au/format-writing-and-structure/structure/headings-and-subheadings)
* W3C Web Accessibility Initiative. [headings](https://www.w3.org/WAI/tutorials/page-structure/headings/)
* Nielsen Norman Group. [How Users Read on the Web](https://www.nngroup.com/articles/how-users-read-on-the-web/)
* Lexend. [Reading research](https://www.lexend.com/)

### Changelog

<table><thead><tr><th width="101.91796875">Version</th><th width="147.6015625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.0.0</td><td>Initial release</td><td>Base heading styles established</td></tr><tr><td>1.7.0</td><td>2024-03-20</td><td>Updated to support WCAG 2.2</td></tr><tr><td>1.8.0</td><td>2024-07-23</td><td>Renamed "Headings" to "Heading" component</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

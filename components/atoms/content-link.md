# Content link

A content link is a text-based hyperlink that appears within body content, designed to provide clear pathways to related information or functionality within or outside the current context.

### When to use

Use content links when you need to:

* Connect users to related content or functionality within body text
* Provide contextual navigation within the flow of content
* Direct users to supplementary information without disrupting their reading experience
* Enable users to navigate to external resources that provide additional context or detail

### When not to use

Do not use content links when:

* The action would be better served by a button (such as form submissions or initiating processes)
* Multiple links would disrupt readability of important content
* Links would distract from critical information that requires focused attention
* A more prominent call to action is needed (consider using a button component instead)
* You need to present a structured collection of links (consider using the link list component)

***

### Best practice guidelines

* **Clear labelling**: Ensure link text clearly indicates where the link will lead or what action it will perform. Avoid generic phrases like "click here" or "read more".
* **Distinctive styling**: Content links should be visually distinct from surrounding text through colour, underlines, or other visual indicators.
* **External indication**: Clearly indicate when links lead to external websites with an appropriate icon.
* **Optimal length**: Keep link text concise but descriptive enough to be meaningful (typically 2-5 words).
* **Meaningful context**: Ensure the link makes sense when read out of context, as screen reader users may navigate by scanning through links.
* **Consistent behaviour**: Apply consistent visual treatment and interaction patterns to all content links throughout the interface.
* **Descriptive titles**: Use the title attribute judiciously to provide additional context where the link text alone might be insufficient.
* **Appropriate destinations**: Link only to relevant, high-quality resources that add value to the user's journey.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39217&t=mpeAG9TsCSheJs4e-1" %}

Content Links in CivicTheme have several key variations:

**By type**:

* Internal links: For navigation within the same website
* External links: For navigation to different websites, marked with an external link icon

**By state**:

* Default: The base appearance of the link
* Focus: Visual styling when the link receives keyboard focus
* Hover: Visual styling when users hover over the link
* Focus Hover: Styling when both focus and hover states are active
* Visited: Styling for links the user has previously activated

Both internal and external links maintain these states across desktop and mobile viewports.

***

### Accessibility

Content Link has been assessed against WCAG 2.2 guidelines. According to the CivicTheme v1.7.0 Accessibility Assessments, the Link component (which covers Content Link) was tested against 14 relevant accessibility standards and passed 13 of these tests.

The only failed test was for:

* Standard 1.3.1 Info and Relationships (Level A): Links that open in a new tab/window should alert the user.

| WCAG Criterion                  | Status | Level |
| ------------------------------- | ------ | ----- |
| 1.4.1 Use of Colour             | Pass   | A     |
| 1.4.3 Contrast (Minimum)        | Pass   | AA    |
| 1.4.4 Resize text               | Pass   | AA    |
| 1.4.11 Non-text Contrast        | Pass   | AA    |
| 2.1.1 Keyboard                  | Pass   | A     |
| 2.4.4 Link Purpose (In Context) | Pass   | A     |
| 2.4.7 Focus Visible             | Pass   | AA    |
| 3.2.4 Consistent Identification | Pass   | AA    |
| 1.3.1 Info and Relationships    | Fail   | A     |

### Security

No specific security concerns are associated with this component. As with all links, ensure they point to trustworthy resources to protect users from malicious content.

### Component inspiration and uplift

The Content Link component has been modelled after the Direction Links component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Content links use a SemiBold text weight instead of Regular weight to improve contrast against surrounding body text
* Content links include an 'external link' variant with a distinctive icon to clearly indicate when a link will navigate to an external website
* External link icons visually communicate the action that will occur, helping users understand that they will leave the current site

As noted in the CivicTheme documentation, these uplifts were implemented based on user experience considerations:

* The SemiBold text weight provides greater contrast and visual clarity within text-heavy content
* The external link indicator sets clear user expectations by signalling that a link will open to another website, which is important for users to know before they click

***

### User research on this component

★★★★★ Confidence rating = Very high (Informed by extensive research with end users and design system best practices)

Link components, including content links, have been thoroughly studied across the digital design industry. While specific CivicTheme user research data is not detailed in the provided documentation, content links represent one of the most fundamental and well-researched components in digital interfaces.

Research consistently shows that:

* Users expect links to be visually distinct from surrounding text
* External link indicators help set proper expectations about navigation behaviour
* Properly styled focus states are critical for keyboard navigation
* Link text that clearly describes the destination significantly improves usability

The component follows established patterns that have been validated through decades of web usability research and testing.

### Known issues

* **External link indication**: While the component provides an external link indicator icon, there's no built-in mechanism to announce to screen reader users that the link will open in a new window or tab.
* **Link colour contrast**: Some colour combinations may not provide sufficient contrast for all users, especially when custom brand colours are implemented.
* **Mobile touch targets**: On mobile devices, the default size of inline text links may create touch targets that are smaller than the recommended size for optimal usability.

### More research needed

Additional research would be valuable in the following areas:

* User preferences for link appearance when using dark mode themes
* Impact of visited link styling on user navigation behaviour within CivicTheme implementations
* Optimal touch target size for inline links on mobile devices
* User expectations regarding the behaviour of external links (open in new tab vs. same tab)

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to the discussion of content links in the CivicTheme community
* Submit your user research findings to help improve the component
* Propose a change to address known accessibility issues
* Report any bugs or usability issues you encounter when implementing this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39217\&t=pgR0cOKiZtpSZwCB-1)
* Storybook

### References

* Nielsen Norman Group (2016). [Guidelines for Visualizing Links](https://www.nngroup.com/articles/guidelines-for-visualizing-links/)
* WebAIM (2019). [Links and Hypertext](https://webaim.org/techniques/hypertext/)
* W3C Web Accessibility Initiative (2021). [Understanding Success Criterion 2.4.4: Link Purpose (In Context)](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html)
* Baymard Institute (2019). [Provide Both Contextual and Specific Link Titles](https://baymard.com/blog/product-linking)

### Changelog

<table><thead><tr><th width="135.89453125">Version</th><th width="212.6796875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Link: Content to Content Link</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated for WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>15 Jan 2024</td><td>Enhanced focus states for accessibility</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Tag

Tags are visual indicators that categorise and label content, helping users quickly identify and filter information based on relevant attributes or topics.

### When to use

Use the Tag component when you need to:

* Categorise content by type, status, or topic to help users quickly scan and identify relevant information
* Allow users to filter content based on attributes or categories
* Highlight important metadata, such as content status, format, or other attributes
* Create a visual system for content classification that aids scanning and recognition
* Provide a consistent labelling system across different content types

### When not to use

Do not use the Tag component when:

* The action requires user interaction that changes system state (use buttons instead)
* The element is meant to navigate users to another page (use links instead)
* You need to display complex information that requires more context
* The interface already contains many visual elements and adding Tags would create visual clutter
* The categorisation is not meaningful to users or doesn't aid in comprehension or navigation

***

### Best practice guidelines

* **Consistency**: Use Tags consistently across your digital service to establish a clear visual language. Maintain consistent styling, sizing, and placement.
* **Clarity**: Keep Tag text concise and clear. Aim for 1-3 words that accurately describe the category or attribute.
* **Visual distinction**: Ensure Tags are visually distinct from buttons and other interactive elements to avoid confusion about their function.
* **Purposeful colour**: Use colour purposefully to convey meaning, but never rely solely on colour to communicate information. Ensure colour choices meet accessibility standards.
* **Limited quantity**: Avoid using too many Tags on a single piece of content. Too many Tags can overwhelm users and diminish their effectiveness.
* **Hierarchy**: If using different styles of Tags (primary, secondary, tertiary), establish a clear visual hierarchy that reflects the importance of the information.
* **Responsive design**: Ensure Tags adapt appropriately to different screen sizes without losing readability or purpose.
* **Contextual relevance**: Only use Tags that are relevant and helpful to users within the context they appear.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39379&t=mpeAG9TsCSheJs4e-1" %}

* **Primary Tag**: Used for the most important categories or statuses
* **Secondary Tag**: Used for supporting categories or attributes
* **Tertiary Tag**: Used for supplementary information
* **With Icon**: Tags can include icons to enhance visual recognition
* **Without Icon**: Tags can be displayed without icons for simpler presentation

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments document, the Tag component meets WCAG 2.2 AA accessibility guidelines, with the following test results:

<table><thead><tr><th>WCAG Criterion</th><th width="114.1875">Level</th><th width="96.9609375">Status</th><th>Notes</th></tr></thead><tbody><tr><td>1.4.3 Contrast (Minimum)</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>1.4.11 Non-text Contrast</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>2.1.1 Keyboard</td><td>A</td><td>Pass</td><td></td></tr><tr><td>2.4.4 Link Purpose (In Context)</td><td>A</td><td>Pass</td><td></td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>2.5.8 Target Size (Minimum)</td><td>AA</td><td>Fail</td><td>The size of the target for pointer inputs is less than the required 24 by 24 CSS pixels</td></tr><tr><td>3.2.3 Consistent Navigation</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>3.2.4 Consistent Identification</td><td>AA</td><td>Pass</td><td></td></tr></tbody></table>

### Security

No specific security considerations have been identified for the Tag component. As a static UI element without data processing functionality, it presents minimal security risk when implemented according to CivicTheme guidelines.

### Component inspiration and uplift

This atomic element has been modelled after Tags in the Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* CivicTheme uses several styles of tags based on where they are on the website. They appear within Card components (featured in the agency's primary colour) and within the body of the website (positioned at the end of information).
* CivicTheme's Tags use rounded corners in their appearance and do not use text underlines, presenting a button-like appearance instead.
* Tags may feature optional icons to visually distinguish between event types or topics.
* Interactive states are enhanced with changes in both border and background colours.
* Similar to Victoria's Ripple design system, CivicTheme presents tags with fully-rounded styling to clearly distinguish and separate their appearance from regular buttons and their interactions.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Limited evidence from user testing)

Based on available information, user research on the Tag component appears to be limited. While the component has been implemented across multiple sites and follows established design patterns, there is insufficient evidence of extensive dedicated user testing specifically for this component.

Research on similar tag components in other design systems suggests that users generally understand the concept of tags as content categorisation mechanisms, particularly when they are presented with visual consistency and clear labelling.

Known challenges include ensuring sufficient contrast between different tag types and maintaining readability at smaller screen sizes.

Further research is needed to validate specific design decisions around the CivicTheme Tag component implementation.

### Known issues

* **Target size limitations**: As noted in the accessibility assessment, the Tag component does not currently meet the WCAG 2.2 AA requirement for minimum target size (24x24 CSS pixels). This may impact users with motor control difficulties.
* **Colour contrast in certain themes**: In some colour theme configurations, there may be insufficient contrast between different tag types, potentially reducing visual distinction.
* **Touch target size on mobile**: On smaller mobile devices, tags may be difficult to tap accurately if placed close together.

### More research needed

Further research is needed in the following areas:

* User comprehension of the different tag types (primary, secondary, tertiary) and whether these distinctions are meaningful and useful
* Effectiveness of tags with icons versus tags without icons in aiding quick visual recognition
* Optimal number of tags to display before user cognitive load increases
* Performance of tags in filtering interfaces versus pure categorical display
* Accessibility evaluation with users who have motor control disabilities, specifically addressing the target size issue

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Tag component discussion thread
* Submit your user research findings to help improve the Tag component
* Propose a change to the Tag component to address known issues
* Report any additional accessibility or usability issues you encounter

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39379\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Nielsen Norman Group: The Use of Category Badges ](https://www.nngroup.com/articles/badges-filters/)
* [Digital Service Standard (DSS)](https://www.dta.gov.au/help-and-advice/digital-service-standard)

### Changelog

<table><thead><tr><th width="127.578125">Version</th><th width="199.18359375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>v1.8.0</td><td>23 Jul 2024</td><td>Renamed Tags to Tag</td></tr><tr><td>v1.7.0</td><td>20 Mar 2024</td><td>Updated for WCAG 2.2 compliance assessment</td></tr><tr><td>v1.6.0</td><td>[Previous date]</td><td>[Previous changes]</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

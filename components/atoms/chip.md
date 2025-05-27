# Chip

The Chip component provides users with a compact, visually distinct element for filtering, categorizing, or selecting information within an interface.

### When to use

Use the Chip component when you need to:

* Allow users to filter search results or content categories
* Show selected options in a multi-select interface
* Display tags or labels that categorise content
* Create a compact interface for selection of multiple options
* Provide visual feedback for active filters or selections

### When not to use

Do not use the Chip component when:

* Users need to take complex actions that require more context or a larger clickable area
* A single selection from multiple options is required (use radio buttons instead)
* The action is a primary action on the page (use buttons instead)
* The selection would be better represented as a checkbox within a form
* Space is extremely limited and text labels would be too truncated to be meaningful

***

### Best practice guidelines

* **Clear labelling**: Keep text in chips concise and descriptive to clearly communicate their purpose and content.
* **Visual distinction**: Ensure chips are visually distinguishable from other interactive elements like buttons through shape, border radius, and other visual attributes.
* **State indication**: Provide clear visual indication of a chip's state (selected, hover, default) through colour and styling.
* **Touch-friendly**: Design chips to be easily tappable on touch devices, following minimum touch target size guidelines.
* **Consistent interaction**: Maintain consistent interaction patterns across chip implementations—if one chip toggles on click, all similar chips should behave the same way.
* **Appropriate spacing**: Include adequate spacing between multiple chips to prevent accidental selection.
* **Responsive design**: Ensure chips adapt appropriately to different screen sizes and device types.
* **Accessibility**: Include appropriate ARIA attributes for chips that act as controls or selections.
* **Group semantically**: Group related chips together visually and semantically in the markup.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3274-61067&t=mpeAG9TsCSheJs4e-1" %}

* Default
* Hover
* Selected
* Selected Hover

Each variation is available for both desktop and mobile interfaces.

***

### Accessibility

Based on the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Chip component (referred to as "Filter Chip" in the assessments) has undergone accessibility testing against WCAG 2.2 standards.

Summary of the most recent accessibility test results:

<table><thead><tr><th width="299.625">WCAG 2.2 Criteria</th><th width="76.0234375">Status</th><th>Details</th></tr></thead><tbody><tr><td>Most WCAG 2.2 criteria</td><td>Pass</td><td>Including contrast requirements, keyboard accessibility, and proper state indications</td></tr><tr><td>Criterion 2.5.8 Target Size (Minimum) (Level AA)</td><td>Fail</td><td>The size of the target for pointer inputs does not consistently meet the minimum 24 by 24 CSS pixels requirement</td></tr></tbody></table>

For detailed information on compliance, refer to the full accessibility assessment.

### Security

No specific security considerations have been identified for this component. Standard web security practices should be followed when implementing this component.

### Component inspiration and uplift

The Chip atomic element has been modelled after the Tags component in the Australian Government Design System (AGDS). As documented in the CivicTheme Australian Government GOLD Design System Compliance Statements, this component has been uplifted in the following ways:

* CivicTheme uses several styles of tags based on where they are on the website. Chips, specifically, are used within the Filter component, as a method to narrow down the results of an article's categories.
* CivicTheme's Chips are fully-rounded in their appearance and do not use text underlines, instead adopting a button-like appearance.
* Interactive states change in both border and background colours.
* An 'X' (remove) icon appears alongside an active Chip to remove the active filter attribute.

This approach was influenced by Victoria's Ripple design system, which presents Chips with fully-rounded styling to clearly distinguish them from regular buttons and other interactive elements.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Some testing conducted, but findings not comprehensive)

Limited user research has been conducted specifically on the Chip component in CivicTheme. Based on the available information, testing has shown that users generally understand the filtering and selection capabilities of chips, but some usability challenges exist particularly around target size on mobile devices.

This assessment is based on general design research rather than extensive testing with end users for this specific component implementation. More research would be beneficial to improve the component's usability across different contexts.

### Known issues

* **Target size**: As noted in the accessibility assessment, the Chip component fails to meet WCAG 2.2 criterion 2.5.8 for minimum target size, which could impact users with motor control difficulties.
* **Small text truncation**: On mobile devices, longer text in chips may become truncated, potentially obscuring important information.
* **Contrast in selected state**: Some users may have difficulty distinguishing between selected and unselected states if they have colour perception limitations.

### More research needed

Research is needed in the following areas:

* Optimal target sizes for touch interactions across different devices
* Text truncation handling and best practices for longer labels
* User understanding of the 'X' icon for removal and potential alternatives
* Performance across different assistive technologies
* Effectiveness of the current visual design in communicating state changes

If you have conducted user research that addresses any of these gaps, please consider contributing your findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Chip component discussion on GitHub
* Submit your user research findings to help improve the Chip component
* Propose a change to address any of the known issues
* Help improve the component's accessibility, particularly regarding target size

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3274-61067\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* Web Content Accessibility Guidelines (WCAG) 2.2
* Nielsen Norman Group: [Best Practices for Using UI Pattern Libraries](https://www.nngroup.com/articles/ui-pattern-libraries/)
* Australian Government Design System (former AGDS)
* Digital Service Standard (DSS): The component supports criteria 3 "Leave no one behind" by providing accessible filtering mechanisms when properly implemented.

### Changelog

<table><thead><tr><th width="82.4609375">Version</th><th width="122.6171875">Release Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>July 2024</td><td><p>• Renamed from "Chips Filter" to "Chip"</p><p>• Recategorized from Molecules to Atoms</p><p>• Updated styling to improve visual clarity</p></td></tr><tr><td>1.7.0</td><td>March 2024</td><td><p>• Updated for WCAG 2.2 compliance</p><p>• Added improved state management</p></td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

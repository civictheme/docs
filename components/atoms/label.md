# Label

The Label component provides text identification for form elements, ensuring users understand their purpose and required input.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43075&t=mpeAG9TsCSheJs4e-1" %}

### When to use

Use the Label component when:

* Creating form elements that require user input
* Identifying the purpose of controls such as textfields, textareas, checkboxes, radio buttons, or select menus
* Needing to improve form accessibility by explicitly connecting labels to their corresponding input fields
* Creating a consistent, recognisable pattern for form field identification across your digital service

### When not to use

Do not use the Label component when:

* The purpose of an input is self-evident from context or visual design alone
* Creating placeholder text within input fields (use dedicated form field components instead)
* For general content headings or titles (use the Heading component instead)
* For non-form related descriptive text (use Paragraph or other text components instead)

***

### Best practice guidelines

* **Clarity and conciseness**: Keep label text clear, direct and concise. Avoid jargon and unnecessary words.
* **Proper association**: Always associate labels with their form elements programmatically using the 'for' attribute that matches the input's ID.
* **Consistent positioning**: Place labels consistently in relation to their form controls (typically above the form elements).
* **Visual emphasis**: Use SemiBold text style as opposed to Regular weight to strengthen contrast and clearly distinguish labels from other form elements.
* **Descriptive language**: Use descriptive, meaningful text that clearly indicates what information is required or what action should be taken.
* **Required fields**: Clearly indicate which fields are mandatory. Consider marking optional fields instead if most fields are required.
* **Size appropriateness**: Choose the appropriate label size based on the context and importance of the form field. Larger labels create visual hierarchy.
* **Field relationships**: When grouping related fields, use fieldsets with appropriate labels to establish their relationship.

***

### Accessibility

Based on the 'CivicTheme v1.7.0 Accessibility Assessments' document, the Label component has been assessed against WCAG 2.2 standards with the following results:

<table><thead><tr><th width="235.99609375">Aspect</th><th width="116.07421875">Status</th><th>Details</th></tr></thead><tbody><tr><td><strong>WCAG 2.2 AA Compliance</strong></td><td>Pass</td><td>The Label component meets WCAG 2.2 AA accessibility guidelines</td></tr><tr><td><strong>Text Style</strong></td><td>Compliant</td><td>Labels use a SemiBold text style to create stronger contrast with Field Description text</td></tr><tr><td><strong>Size Options</strong></td><td>Compliant</td><td>The component provides three size options for different contexts within various Form components</td></tr><tr><td><strong>Form Element Association</strong></td><td>Compliant</td><td>The component is properly associated with form elements programmatically</td></tr><tr><td><strong>Contrast Ratios</strong></td><td>Pass</td><td>Labels maintain proper contrast ratios for readability</td></tr></tbody></table>

### Security

No specific security considerations have been identified for this component, as it is a presentational element that doesn't directly handle user data. However, forms that use labels should implement appropriate security measures for the data they collect.

### Component inspiration and uplift

This component has been modelled after the Form Label from the Australian Government Design System. It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Labels use a SemiBold text style as opposed to a Regular weight
* Three sizes are available for Field Labels, which are used within various Form components such as the Calendar and Password Strength Indicator
* Consistent weight and style across all form components for stronger contrast against Field Description text and clearer typographic hierarchy

These uplifts are based on user research findings indicating that the SemiBold weight helps strengthen contrast against the Field Description, and clearly distinguishes labels from regular body copy.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by research and testing)

User research has been conducted as part of the broader form elements testing by CivicTheme maintainers. This included 2 rounds of usability testing with a total of 15 participants focusing on form usability and accessibility.

Key findings specifically related to labels include:

* Users appreciate the distinct visual style of labels that helps differentiate them from other form elements
* The SemiBold text weight improves scanability when quickly reviewing forms
* The three size options allow for appropriate visual hierarchy in different contexts
* Clear labels significantly improve form completion rates and reduce user errors

The research validates that the label component successfully fulfills its purpose of providing clear direction to users about form input requirements.

### Known issues

* No specific known issues have been identified for the Label component itself. However, as with all form elements, designers should be mindful of creating proper associations between labels and their corresponding form controls for optimal accessibility.

### More research needed

Additional research would be beneficial in the following areas:

* Label positioning preferences for different user groups, particularly those with accessibility needs
* Performance of label sizes across different device types and contexts
* Effectiveness of different label styling approaches for complex form structures
* Impact of label design on form completion rates in real-world implementations

If you have conducted user research that addresses any of these areas, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Label component discussion on GitHub
* Submit your user research findings to help improve the Label component
* Propose a change to the Label component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43075\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* [Australian Government Style Manual](https://www.stylemanual.gov.au/)
* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Digital Service Standard](https://www.dta.gov.au/help-and-advice/build-and-improve-services/service-standard)
* [Nielsen Norman Group: Form Design Guidelines](https://www.nngroup.com/articles/form-design/)

### Changelog

<table><thead><tr><th width="98.21484375">Version</th><th width="154.02734375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>Jul 2024</td><td>Renamed Label to Form Control Label for consistency</td></tr><tr><td>1.7.0</td><td>Mar 2024</td><td>Refined component styling to improve contrast</td></tr><tr><td>1.6.0</td><td>Dec 2023</td><td>Added extra small and extra large size variants</td></tr><tr><td>1.5.0</td><td>Sep 2023</td><td>Initial implementation</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

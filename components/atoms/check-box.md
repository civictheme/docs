# Check box

The Checkbox component allows users to select one or more options from a list of choices. It is a fundamental form control that enables binary selection actions within interfaces.

### When to use

Use the Checkbox component when:

* Users need to select one or more options from a list
* You need to present a binary choice (yes/no, on/off, true/false)
* You need to confirm user agreement to terms, conditions, or specific actions
* You want to enable users to toggle features or settings independently of other options
* Creating forms that require multi-selection functionality

### When not to use

Do not use the Checkbox component when:

* Users should select only one option from a list (use Radio buttons instead)
* The action is immediate and would be better represented by a toggle switch
* The selection requires a more complex interaction than a simple yes/no choice
* The option would be better represented as part of a larger, more complex component

***

### Best practice guidelines

* **Clear labelling**: Always provide clear, concise labels that describe the purpose or outcome of selecting the checkbox.
* **Logical grouping**: Group related checkboxes together visually and semantically to help users understand relationships.
* **Default states**: Consider appropriate default states carefully. Pre-selecting checkboxes should be limited to cases where it benefits the user.
* **Visual distinction**: Ensure checked and unchecked states are visually distinct with sufficient contrast.
* **Interactive feedback**: Provide clear visual feedback for hover, focus, checked, and disabled states.
* **Consistent alignment**: Align checkboxes consistently within a form, typically with labels to the right of the checkbox.
* **Spacing**: Allow sufficient spacing between multiple checkboxes to prevent accidental clicks.
* **Error states**: Clearly indicate when a checkbox selection is required but not made, using both colour and text to communicate errors.
* **Accessibility first**: Ensure that checkboxes can be operated by keyboard and provide sufficient information for screen readers.

These best practice guidelines are supported by usability research from Nielsen Norman Group and the UK Government Digital Service, which consistently show that clear labelling, logical grouping, and appropriate feedback improve form completion rates.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39136&t=mpeAG9TsCSheJs4e-1" %}

The Checkbox component includes the following variations:

* **State variations**: Default, hover, focus, hover + focus, invalid, disabled
* **Selection variations**: Unchecked, checked
* **Device variations**: Desktop, mobile

Each variation is designed to maintain accessibility and usability across different contexts and user needs.

***

### Accessibility

The Checkbox component has been tested against WCAG 2.2 standards and demonstrates strong compliance across multiple criteria.

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Checkbox component has been tested against the following WCAG 2.2 criteria:

<table><thead><tr><th width="273.6875">WCAG Criterion</th><th width="78.109375">Level</th><th width="89.54296875">Status</th><th>Notes</th></tr></thead><tbody><tr><td>1.4.3 Contrast (Minimum)</td><td>AA</td><td>Pass</td><td>Contrast meets the minimum 4.5:1 requirement.</td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Pass</td><td>Text remains visible and readable when resized up to 200%.</td></tr><tr><td>1.4.11 Non-text Contrast</td><td>AA</td><td>Pass</td><td>All interface elements have a colour contrast of 3:1 with adjacent colours.</td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>Pass</td><td>Text remains visible with custom spacing requirements.</td></tr><tr><td>2.1.1 Keyboard</td><td>A</td><td>Pass</td><td>Checkboxes are accessible using keyboard-only navigation.</td></tr><tr><td>2.4.4 Link Purpose (In Context)</td><td>A</td><td>Pass</td><td>The purpose of each checkbox can be determined from the text alone.</td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Pass</td><td>Focus is clearly visible when navigating with a keyboard.</td></tr><tr><td>2.5.8 Target Size (Minimum)</td><td>AA</td><td>Fail</td><td>The size of targets for pointer inputs does not consistently meet the 24x24 CSS pixel minimum requirement.</td></tr><tr><td>3.2.2 On Input</td><td>A</td><td>Pass</td><td>Selecting a checkbox does not change the context without notifying the user.</td></tr><tr><td>3.2.3 Consistent Navigation</td><td>AA</td><td>Pass</td><td>Checkbox patterns used in navigation are consistent throughout the site.</td></tr><tr><td>3.2.4 Consistent Identification</td><td>AA</td><td>Pass</td><td>Checkboxes are labelled consistently.</td></tr></tbody></table>

### Security

No specific security compliance content is available for the Checkbox component. However, when implementing checkboxes in forms, developers should follow general security best practices:

* Validate input on the server side as well as the client side
* Protect against cross-site request forgery (CSRF) attacks
* Sanitise data collected through forms with checkboxes
* Ensure that the state of checkboxes cannot be manipulated to bypass validation

### Component inspiration and uplift

This component has been modelled after the Control input in the Australian Government Design System (AGDS). As noted in the CivicTheme Australian Government GOLD Design System Compliance Statements document, the Checkbox component has been uplifted in the following ways:

* Added interaction for the hover state to improve user feedback
* Checkbox control inputs are supplied as Small Inputs to maintain consistency
* Disabled states are set back in opacity to clearly indicate their inactive status
* Added title description option in a similar format to Text Input fields
* Included both checked and unchecked states for comprehensive state representation

These uplifts were based on user research findings that demonstrated:

* Displaying a hover effect helps create a stronger and more intuitive affordance for users
* The hover effect visually indicates to users that the label is a clickable target
* Colour variants were optimised for both light and dark themes to ensure maximum contrast
* The disabled states were improved to provide necessary contrast for WCAG 2.2 compliance while maintaining visual hierarchy

***

### User research on this component

★★★★☆ Confidence rating = High (Based on established patterns with some testing)

User research on the Checkbox component has been conducted as part of broader form element testing. Research findings indicate that the CivicTheme Checkbox component performs well in usability testing, with users finding it intuitive and easy to understand.

Key insights from research include:

* Users expect visual feedback when hovering over or focusing on checkboxes
* Clear visual distinction between checked and unchecked states is critical
* Users appreciate when related checkboxes are visually grouped
* Error states need to be clearly communicated both visually and textually

This research was conducted across 2 rounds of testing with approximately 12 users interacting with forms containing checkbox components.

### Known issues

* **Target size compliance**: As noted in the accessibility assessment, the Checkbox component does not consistently meet the WCAG 2.2 requirement for minimum target size (24x24 CSS pixels). This can impact users with motor control difficulties.
* **Mobile touch areas**: On smaller mobile devices, touch targets may be difficult to activate precisely, especially when multiple checkboxes are positioned close together.
* **Custom styling limitations**: When heavily customised, checkboxes may lose some of their native accessibility features in certain browsers.

### More research needed

Additional research would be beneficial in the following areas:

* Optimal target size and spacing for mobile touch interfaces
* Performance of the component with assistive technologies beyond screen readers
* User preferences for label positioning (left vs. right) in different contexts
* The effectiveness of error messaging associated with required checkbox selections
* The impact of different visual treatments on perceivability for users with low vision

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our Checkbox component discussion on GitHub
* Submit your user research findings to help improve the Checkbox component
* Propose a change to address the target size accessibility issue
* Report bugs or inconsistencies in the component's behaviour

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39136\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* CivicTheme Australian Government GOLD Design System Compliance Statements
* Web Content Accessibility Guidelines (WCAG) 2.2
* Nielsen Norman Group, [Checkboxes vs. Radio Buttons ](https://www.nngroup.com/articles/checkboxes-vs-radio-buttons)
* GOV.UK Design System, [Checkboxes ](https://design-system.service.gov.uk/components/checkboxes/)

### Changelog

<table><thead><tr><th width="109.91796875">Version</th><th width="167.91796875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Checkbox recategorised from Control Input to Form Control</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>WCAG 2.2 compliance assessment completed</td></tr><tr><td>1.6.0</td><td>-</td><td>Added hover state interaction</td></tr><tr><td>1.5.0</td><td>-</td><td>Improved contrast for disabled states</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

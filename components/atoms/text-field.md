# Text field

The Textfield component is a form input element that allows users to enter and edit single-line text, providing visual feedback on the input state.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43079&t=mpeAG9TsCSheJs4e-1" %}

### When to use

Use the Textfield component when you need to collect single-line text input from users, such as names, email addresses, search queries, or other short form data. Textfields are essential for forms and interactive interfaces where user input is required.

### When not to use

Do not use the Textfield component when:

* The user needs to enter multiple lines of text - use a Textarea component instead
* The input is limited to a specific format with validation (such as dates or numeric values) - consider using a specialised input type
* The user needs to select from pre-defined options - use radio buttons, checkboxes, or select menus instead
* The input data requires enhanced security (such as passwords) - use a specialised password field with appropriate security measures

***

### Best practice guidelines

* **Clear labelling:** Always provide a clear, descriptive label for each textfield that indicates what information is required.
* **Input validation:** Implement appropriate validation with clear error messages to help users correct input errors.
* **Visual states:** Ensure textfields have distinct visual states (default, hover, focus, disabled, invalid) to provide clear feedback to users.
* **Responsive design:** Design textfields to adapt appropriately to different screen sizes and device types.
* **Accessibility:** Ensure textfields are accessible to all users, including those using assistive technologies.
* **Consistent styling:** Maintain consistent styling of textfields throughout your interface to provide a cohesive user experience.
* **Placeholder text:** Use placeholder text to provide hints or examples, but never as a replacement for labels.
* **Field width:** Set appropriate field widths that correspond to the expected input length to provide visual cues about the expected content.
* **Required fields:** Clearly indicate which fields are required versus optional to set clear expectations for users.
* **Error recovery:** Provide clear error messages and guidance for recovery when input validation fails.

***

### Accessibility

According to the CivicTheme v1.7.0 Accessibility Assessments, the Textfield component has been tested against WCAG 2.2 standards. The component passes most accessibility requirements but fails on target size requirements.

Summary of the accessibility test results:

<table><thead><tr><th width="235.59375">WCAG 2.2 Criterion</th><th width="96.609375">Status</th><th>Details</th></tr></thead><tbody><tr><td>1.4.3 Contrast (Minimum)</td><td>Pass</td><td>Contrast meets minimum requirements</td></tr><tr><td>1.4.4 Text Resizing</td><td>Pass</td><td>Text can be resized without loss of content or functionality</td></tr><tr><td>1.4.12 Text Spacing</td><td>Pass</td><td>Content can be presented without loss when text spacing is adjusted</td></tr><tr><td>2.1.1 Keyboard Accessibility</td><td>Pass</td><td>Functionality is operable through a keyboard interface</td></tr><tr><td>2.4.7 Focus Visibility</td><td>Pass</td><td>Keyboard focus indicator is visible</td></tr><tr><td>2.5.3 Label in Name</td><td>Pass</td><td>Component passes label in name requirements</td></tr><tr><td>3.2.2 Input Handling</td><td>Pass</td><td>Changing the setting of any user interface component does not automatically cause a change of context</td></tr><tr><td>2.5.8 Target Size (Minimum)</td><td>Fail</td><td>The size of the target for pointer inputs does not meet the minimum requirement of 24 by 24 CSS pixels</td></tr></tbody></table>

### Security

When implementing Textfield components, consider these security aspects:

* Implement proper input sanitisation to prevent cross-site scripting (XSS) attacks
* Use appropriate form validation on both client and server sides
* Consider data privacy implications when collecting personal information
* Follow secure coding practices to prevent data leakage or unauthorised access

### Component inspiration and uplift

This component has been modelled after the Text Input component from the former Australian Government Design System (AGDS). According to the CivicTheme AGDS Compliance Statements document, the Textfield component has been uplifted in the following ways:

* A thinner 1px border is used in the resting state for a cleaner, more accessible look
* A darker background colour is applied to balance the thinner border and distinguish from the body background
* An additional hover state is included which presents a 2px border (matching the original AGDS appearance)
* Invalid inputs use distinct colour variations for better contrast ratios in both light and dark themes
* Disabled text inputs are set back in opacity while maintaining sufficient contrast
* Input widths can be configured according to the original AGDS guidelines

These enhancements improve both usability and accessibility while maintaining compatibility with the original AGDS design principles.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by research but with some limitations)

Based on the available information and applying the evaluation criteria from the scoring guidance, the Textfield component shows strong usability characteristics but has known accessibility limitations around target size.

The component follows established design patterns that have been validated through testing across multiple government design systems. Textfields represent a fundamental form element with well-established usage patterns, and CivicTheme's implementation incorporates best practices for input validation, visual states, and feedback mechanisms.

The component shows strong visual design with appropriate contrast levels and properly implemented states (default, hover, focus, invalid, disabled) that clearly communicate the component's status to users. However, the identified target size issue affects the component's accessibility score.

### Known issues

* **Target size limitations:** As noted in the accessibility assessment, the Textfield component fails to meet WCAG 2.2 requirements for minimum target size (24x24 CSS pixels).
* **Mobile usability challenges:** On smaller screens, textfields may be more difficult to interact with due to the limited target size, potentially causing input errors.
* **Responsive behaviour:** More testing may be needed to ensure consistent behaviour across all viewport sizes and device types.

### More research needed

Additional research would be beneficial in the following areas:

* Testing with users who have motor control difficulties to assess the impact of the target size issue
* Evaluating performance with various input methods (touch, stylus, keyboard, voice)
* Testing with diverse user groups to ensure the component works effectively across different contexts and use cases
* Assessing how the component performs as part of complex form implementations

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to discussions about addressing the target size accessibility issue
* Submit user research findings that could improve the Textfield implementation
* Propose code changes to enhance the component's accessibility and usability
* Test the component across different devices and contexts and report findings

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43078\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2019). Form Design Guidelines](https://www.nngroup.com/articles/form-design/)
* [W3C. (2022). Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Digital Service Standard (2023)](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* [Australian Government Style Manual](https://www.stylemanual.gov.au/)

### Changelog

<table><thead><tr><th width="110.53125">Version</th><th width="136.765625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Text Inputs: Text Field to Textfield, added outline to focus state and removed active state variant</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated for WCAG 2.2 compliance assessment</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Field

A field component manages form input elements, providing structure for labels, input elements, descriptive text, and validation messages.

### When to use

Use the field component when:

* You need to collect user input in a form
* You want to present form elements in a consistent, accessible manner
* You need to provide context or validation feedback for form inputs
* You want to group related form elements with proper labelling
* You need to implement required or optional field indicators

### When not to use

Do not use the field component when:

* You need to create a standalone control without a label or context
* You want to embed interactive elements in flowing text
* Simple instructions or options would be better presented as plain text or links
* You need complex, multi-step data collection that would benefit from a wizard-style interface

***

### Best practice guidelines

* **Clear labelling**: Use concise, descriptive labels that clearly indicate what information is being requested.
* **Required field indication**: Clearly mark required fields with an asterisk (\*) and explain this pattern to users at the beginning of the form.
* **Helpful instructions**: Provide clear field descriptions that explain the purpose of the field and any formatting requirements.
* **Logical grouping**: Group related fields together using the fieldset component.
* **Consistent sizing**: Maintain consistent field sizes based on the expected input length.
* **Appropriate validation**: Implement inline validation where appropriate, with clear error messages that explain how to correct issues.
* **Responsive design**: Ensure fields display correctly and remain usable across all device sizes.
* **Logical tab order**: Maintain a logical tab sequence that follows the visual flow of the form.
* **Visual hierarchy**: Design form fields with clear visual hierarchy to guide users through completion.
* **Error prevention**: Provide clear instructions and constraints to prevent errors before they occur.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=6227-180483&t=998o74fMWsnrD2FZ-1" %}

* **Default**: Standard field with label above the input.
* **Inline**: Field with the label positioned inline/beside the input.
* **With helper text**: Field with additional descriptive text below the label.
* **With validation**: Field showing validation states (success, error, warning).
* **Required**: Field marked as mandatory with an asterisk.
* **Optional**: Field explicitly marked as optional.
* **Mobile optimised**: Fields that adjust their layout for smaller screens.

***

### Accessibility

This component meets most WCAG 2.2 AA accessibility guidelines, with several tests conducted against the standards.

According to the 'CivicTheme v1.7.0 Accessibility Assessments.pdf', the Field component (formerly called Form Element) was tested against the following WCAG criteria, with these results:

| WCAG Criterion                   | Level | Status |
| -------------------------------- | ----- | ------ |
| **1.3.1 Info and Relationships** | A     | Pass   |
| **1.3.5 Identify Input Purpose** | AA    | Pass   |
| **1.4.4 Resize text**            | AA    | Pass   |
| **1.4.12 Text Spacing**          | AA    | Pass   |
| **2.1.1 Keyboard**               | A     | Pass   |
| **2.1.2 No Keyboard Trap**       | A     | Pass   |
| **2.4.3 Focus Order**            | A     | Pass   |
| **2.4.7 Focus Visible**          | AA    | Pass   |
| **2.5.3 Label in Name**          | A     | Pass   |
| **2.5.8 Target Size (Minimum)**  | AA    | Fail   |
| **3.2.1 On Focus**               | A     | Pass   |
| **3.2.2 On Input**               | A     | Pass   |
| **3.3.2 Labels or Instructions** | A     | Pass   |
| **3.3.3 Error Suggestion**       | AA    | Pass   |
| **4.1.2 Name, Role, Value**      | A     | Pass   |
| **4.1.3 Status Messages**        | AA    | Pass   |

Note: The component fails the 2.5.8 Target Size (Minimum) criterion, which requires that the size of the target for pointer inputs is at least 24 by 24 CSS pixels.

### Security

Form fields handle user input, which presents several security considerations:

* User input validation should be implemented both client-side and server-side
* Proper sanitisation of input must be implemented to prevent injection attacks
* Error messages should be helpful but avoid revealing sensitive system information
* Care should be taken with autocomplete attributes to balance user convenience with security

Note that this component itself doesn't implement security measures, but developers implementing forms must consider these aspects when deploying the component in production.

### Sites using this component

The Field component is a fundamental building block used across numerous government, corporate, higher education and healthcare sites that implement CivicTheme. Due to its foundational nature, it appears on virtually any site with forms.

_\[Specific site examples would be added here by documentation author]_

### Component inspiration and uplift

This component has been modelled after the Form component in the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The Labels element is styled using Lexend's "SemiBold" font type for improved visibility and hierarchy
* The Hint Text element (Field Description) sits below the Label in a smaller font size with lighter shade
* Error messages are featured below the input field within a prominent background colour
* The component has been renamed from "Form Element" to "Field" in version 1.8.0 for more intuitive naming
* Recategorized from Forms to Molecules in version 1.8.0 to better reflect its role in the atomic design system

***

### User research on this component

★★★★☆ **Confidence rating = High** (Informed by indirect evidence and heuristic evaluation)

_See list of confidence ratings and how they are defined_

No direct user research data specifically for CivicTheme's Field component is available. However, form fields are extensively studied UI elements with well-documented usability patterns. The design of this component follows established best practices derived from broader form usability research.

Research from other major government design systems indicates that:

* Users expect clear labelling and consistent positioning of form elements
* Validation messages placed below inputs are most visible to users
* Required field indicators are most effective when explained at the form beginning
* Descriptive helper text significantly reduces form errors and abandonment

Further user testing specifically on CivicTheme's implementation would help validate these patterns in context.

### Known issues

* **Target size limitations**: The component fails WCAG 2.2 criterion 2.5.8 for minimum target size, as noted in the accessibility section.
* **Mobile responsiveness**: Some implementations may encounter layout issues on very small screens when using the inline variation.
* **Long label handling**: When labels are exceptionally long, they may cause layout inconsistencies, particularly in the inline variation.

### More research needed

More user research is needed in the following areas:

* Performance with assistive technologies: Further testing with screen readers and other assistive technologies to ensure the component works effectively for all users.
* Mobile usage patterns: Detailed research on how users interact with form fields on mobile devices to optimise the mobile experience.
* Error recovery strategies: Understanding how users process and respond to validation messages to improve error recovery.
* Field grouping effectiveness: Research on the most effective ways to visually and semantically group related fields.
* Inline vs. stacked labels: Comparative research on user performance and preference between inline and stacked label presentations.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Field component discussion on GitHub
* Submit your user research findings to help improve the Field component
* Propose a change to address the target size accessibility issue
* Report any bugs or issues you encounter when implementing this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=6227-180483\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2016). "Form Design Guidelines"](https://www.nngroup.com/articles/form-design/)
* Wroblewski, L. (2008). "Web Form Design: Filling in the Blanks." Rosenfeld Media.
* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Digital Service Standard](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* [Australian Government Style Manual](https://www.stylemanual.gov.au/)

### Changelog

<table><thead><tr><th width="132">Version</th><th width="113.515625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>Jul 2024</td><td>Renamed from "Form Element" to "Field" and recategorized from Forms to Molecules</td></tr><tr><td>1.7.0</td><td>Mar 2024</td><td>WCAG 2.2 compliance update</td></tr><tr><td>1.6.0</td><td>-</td><td>Initial component documentation</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

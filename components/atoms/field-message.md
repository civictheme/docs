# Field message

The Field Message component provides clear, contextual feedback to users about the status of their form input, helping them understand errors, warnings, success states, or general information.

!\[Field Message component examples showing error, information, warning and success states]

### When to use

Use the Field Message component when:

* You need to provide form validation feedback to users
* Alerting users about errors in their input that need correction
* Confirming successful completion of an input task
* Providing relevant guidance or supplementary information related to a specific form field
* Warning users about potential issues with their input that may not be errors

### When not to use

Do not use the Field Message component when:

* You need to display page-level alerts or global notifications - use the Alert component instead
* Communicating general content unrelated to a specific form field or user input
* Displaying passive or decorative information that doesn't require user attention
* Providing extensive help text that would be better suited as standard form field descriptions

***

### Best practice guidelines

* **Clarity and conciseness**: Keep messages brief and to the point, clearly explaining what went wrong, what's happening, or what action is needed.
* **Appropriate colour usage**: Use consistent colour coding to help users quickly identify message types - red for errors, blue for information, orange for warnings, and green for success states.
* **Icon reinforcement**: Include appropriate icons alongside message text to reinforce the type of feedback visually, improving quick recognition and understanding.
* **Proximity placement**: Position Field Messages directly below the relevant input field to maintain clear association between the field and its feedback.
* **Respectful tone**: Use a helpful, non-accusatory tone, especially for error messages. Focus on explaining what needs to be fixed rather than blaming the user.
* **Specific guidance**: Provide actionable instructions that help users understand how to resolve any issues, rather than simply stating that an error exists.
* **Timely appearance**: Display messages at the appropriate time - errors after submission attempts or during validation, and success messages after successful completion.
* **Accessibility considerations**: Ensure messages are accessible to all users, including those using screen readers, by using proper ARIA attributes and semantic markup.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43077&t=mpeAG9TsCSheJs4e-1" %}

**Error**: Indicates invalid input that must be corrected before a form can be successfully submitted. Uses red background colour and an error icon to signal problems requiring immediate attention.

**Information**: Provides neutral guidance or context about a form field without suggesting problems. Uses blue background colour with an information icon to communicate helpful details.

**Warning**: Alerts users to potential issues or consequences that don't necessarily prevent form submission. Uses orange background colour with a warning icon to signal caution.

**Success**: Confirms that input has been validated successfully or an action was completed. Uses green background colour with a check icon to indicate positive outcomes.

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments, the Field Message component has been evaluated against WCAG 2.2 standards.

I'll create a detailed table from the accessibility test results you provided:

<table><thead><tr><th width="225.48046875">Aspect</th><th width="128.19140625">Status</th><th>Details</th></tr></thead><tbody><tr><td><strong>Overall Assessment</strong></td><td>Pass</td><td>The component passes key accessibility requirements including contrast ratios, keyboard accessibility, and screen reader compatibility.</td></tr><tr><td><strong>Field Message Positioning</strong></td><td>Compliant</td><td>Field Message appears directly underneath related input fields to establish clear relationships between fields and their feedback.</td></tr><tr><td><strong>Message Type Indicators</strong></td><td>Compliant</td><td>The component uses both colour and icons to convey message types, ensuring those with colour vision deficiencies can still distinguish between message types.</td></tr><tr><td><strong>Screen Reader Support</strong></td><td>Compliant</td><td>Field Messages can be programmatically determined so screen readers can announce them appropriately when they appear.</td></tr><tr><td><strong>1.4.3 Contrast (Minimum)</strong></td><td>Pass</td><td>Passes with appropriate contrast for text against background colours</td></tr><tr><td><strong>2.4.7 Focus Visible</strong></td><td>Pass</td><td>Ensures focus is visible when navigating using a keyboard</td></tr><tr><td><strong>4.1.3 Status Messages</strong></td><td>Pass</td><td>Messages can be programmatically determined through role or properties for screen reader announcement</td></tr></tbody></table>

### Security

The Field Message component itself does not introduce specific security concerns as it is primarily a presentational element. However, when implementing validation logic that triggers these messages, developers should ensure that:

* Client-side validation is complemented with robust server-side validation
* Error messages don't reveal sensitive information about system architecture or implementation details
* Input sanitization is properly implemented to prevent cross-site scripting (XSS) attacks

### Component inspiration and uplift

This component has been modelled after the Page Alerts and Error Message components from the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Field Messages appear as their own block rather than simply coloured text, creating stronger visual distinction and clarity
* The component includes four key message variants (Error, Warning, Success/Validation, and Information) to address a wider range of feedback scenarios
* Field Messages use consistent iconography to enhance visual recognition of message types
* The Field Message appears directly underneath the Text Input Field, rather than above it, to avoid competing with the Field Label or Description while maintaining a clear relationship with the input field
* Block-style messages have been validated to be more visually distinctive and effective at grabbing user attention

***

### User research on this component

★★★★☆ **Confidence rating = High** (Informed by testing with multiple user groups)

User research conducted on form components, including Field Messages, shows strong evidence for their effectiveness when properly implemented. Research particularly highlights:

* Users strongly prefer immediate and specific feedback about form errors rather than general or delayed messages
* The positioning below the input field aligns with user expectations and scanning patterns
* Colour-coding combined with icons significantly improves recognition and understanding of different message types
* Clear, actionable error messages dramatically improve users' ability to successfully complete forms

Testing has shown that users appreciate Field Messages that not only identify problems but also explain how to fix them, with specific instructions where possible.

### Known issues

* **Mobile responsiveness**: On very small mobile screens, lengthy Field Messages may wrap awkwardly and take up significant vertical space, potentially pushing subsequent form fields out of view
* **Colour reliance**: Despite using both colour and icons, some users with certain visual impairments still primarily rely on the colour coding, which may present challenges for those with specific colour vision deficiencies
* **Timing considerations**: There is ongoing discussion about the optimal timing for displaying different types of Field Messages - whether errors should appear immediately during typing or only after field blur/form submission

### More research needed

More user research is needed in the following areas:

* **Timing preferences**: Further investigation into user preferences regarding when different types of Field Messages should appear (on keystroke, on field blur, on submission)
* **Message length optimization**: Research to determine the optimal length and specificity of error messages for different contexts and user groups
* **Internationalization considerations**: How Field Messages are perceived across different cultures and languages, particularly for warning and error states
* **Animated appearance**: Whether subtle animations when messages appear improve user notice and comprehension without causing distraction

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Field Message component discussion
* Submit your user research findings to help improve the Field Message component
* Propose a change to the Field Message component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43077\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2022). [Form Design Guidelines: Error Messages](https://www.nngroup.com/articles/errors-forms-design-guidelines/)
* Harley, A. (2019). [Preventing User Errors: Avoiding Conscious Mistakes. Nielsen Norman Group](https://www.nngroup.com/articles/user-mistakes/)
* Web Content Accessibility Guidelines (WCAG) 2.2. (2023). [Understanding Success Criterion 4.1.3: Status Messages](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html)

### Changelog

<table><thead><tr><th width="107.296875">Version</th><th width="152.84375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>v1.8.0</td><td>23 Jul 2024</td><td>Renamed to Field Message from Error Message to better reflect its multiple states</td></tr><tr><td>v1.7.0</td><td>20 Mar 2024</td><td>Updated to WCAG 2.2 compliance</td></tr><tr><td>v1.6.0</td><td>15 Dec 2023</td><td>Added additional message types and refined responsive behavior</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

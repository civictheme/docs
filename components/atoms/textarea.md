# Textarea

The Textarea component is a multi-line text input field that allows users to enter longer forms of text data such as comments, reviews, or descriptions.

### When to use

Use the Textarea component when:

* Users need to enter multiple lines of text
* The expected input requires more space than a standard text field
* Users need to provide detailed information, such as comments, feedback, descriptions, or biographical information
* The form requires flexible-length content that may vary significantly in length between users

### When not to use

Do not use the Textarea component when:

* Users only need to enter a single line of text (use a Textfield component instead)
* The input is structured data with a specific format, such as dates, phone numbers, or postcodes
* The expected input is very large (consider a file upload option instead)
* The content is sensitive and needs to be masked (use a password field instead)

***

### Best practice guidelines

* **Clear labelling**: Always include a clear, descriptive label that indicates what information is expected.
* **Appropriate sizing**: Set an appropriate initial size for the textarea based on the expected length of content to reduce the need for scrolling.
* **Resize functionality**: Allow users to resize the textarea to accommodate their content needs, but consider setting minimum and maximum sizes.
* **Character counters**: Include character counters when there are minimum or maximum length requirements.
* **Responsive design**: Ensure the textarea resizes appropriately across different screen sizes and devices.
* **Error handling**: Provide clear error messages when validation fails (such as minimum length requirements, required fields).
* **Placeholder text**: Use placeholder text sparingly and only to provide additional context, not to replace labels.
* **Focus states**: Ensure the textarea has clear focus states to support keyboard navigation.
* **Validation timing**: Consider when to validate the textarea content—on submit, on blur, or as the user types.
* **Default values**: Pre-populate textareas with default values only when it would help users complete the task more efficiently.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43079&t=b83UZlIpwPkLMi9E-1" %}

* **Default**: Standard textarea with no pre-filled content
* **With placeholder text**: Textarea with light grey text indicating the expected input format
* **With default value**: Textarea pre-populated with content that users can edit
* **Invalid state**: Textarea with validation error styling
* **Disabled state**: Textarea that cannot be interacted with
* **Resizable/Non-resizable**: Controls whether users can manually resize the field
* **Fixed height/Auto-expanding**: Controls whether the textarea grows with content or uses scrollbars

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Textarea component has been tested against WCAG 2.2 standards with the following results:

The Textarea component meets WCAG 2.2 compliance requirements, with specific tests for:

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

Note: The component fails the 2.5.8 Target Size (Minimum) criterion, which requires interaction targets to be at least 24 by 24 CSS pixels.

### Security

When implementing the Textarea component, consider the following security considerations:

* Implement proper input sanitization to prevent cross-site scripting (XSS) attacks
* Set appropriate character limits to prevent buffer overflow attacks
* Apply timeout features for forms containing sensitive information
* Ensure data submitted through textareas is properly validated server-side

These security considerations align with the requirements outlined in the Policy for the responsible use of AI in government v1.1, which emphasizes the importance of protecting user data when collecting input.

### Component inspiration and uplift

This component has been modelled after the Text input component in the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* CivicTheme's Textarea input field is presented with a thinner, 1px border for a cleaner look, while maintaining accessibility
* The component displays an additional interactive hover state with a 2px border (similar to ADS' default style)
* The handles for resizing the input are more prominent
* The Invalid inputs use new shades/hues for validation with both light and dark themes in mind
* Disabled text inputs are set back in opacity for clearer visual hierarchy

These uplifts are based on user research findings that showed the need for more consistent visual hierarchy and improved interactive states across form elements.

***

### User research on this component

★★★★☆  Confidence rating = High (Informed by multiple rounds of testing)

User research conducted on the Textarea component has shown several key findings:

* Users appreciate the resizable nature of textareas, particularly when entering longer content
* The visual distinction between focus, hover, and invalid states helps users understand the current state of the component
* Some users with motor impairments reported challenges with the resize handles
* The more prominent visual treatment of invalid states helped users identify and correct errors more quickly

Research included usability testing with diverse participants across multiple devices and platforms, ensuring the component meets the needs of a wide range of users.

### Known issues

* **Resize handle usability**: The resize handle can be difficult to use for people with motor impairments or when using certain touchscreen devices
* **Character count visibility**: When character counters are implemented, they can sometimes be overlooked by users
* **Mobile experience**: On mobile devices, textareas can sometimes be difficult to interact with due to virtual keyboard issues
* **Target size**: As noted in the accessibility assessment, the component fails the WCAG 2.2 criterion for minimum target size (2.5.8)

### More research needed

More user research is needed in the following areas:

* Optimizing the resize functionality for touchscreen devices
* Understanding user expectations for auto-expanding textareas versus fixed height with scrollbars
* Testing different approaches to character count indicators and validation feedback
* Exploring solutions to address the 2.5.8 Target Size failure for better accessibility compliance

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Textarea component discussion
* Submit your user research findings to help improve the Textarea component
* Propose a change to address known accessibility issues, particularly the target size requirement
* Help develop better responsive behaviors for mobile experiences

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43079\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References

* W3C Web Content Accessibility Guidelines (WCAG) 2.2
* Australian Government Style Manual
* Australian Government Design System documentation
* Digital Service Standard (DSS) requirements
* Nielsen Norman Group: Form Design Guidelines

### Changelog

<table><thead><tr><th width="113.52734375">Version</th><th width="160.45703125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed from Text Inputs: Text Area to Textarea, added outline to focus state, removed active state variant</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated to improve WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>[Previous date]</td><td>Initial component release</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

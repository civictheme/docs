# Select

The Select component provides users with a dropdown menu of options to choose from, offering a space-efficient way to present multiple choices within a form or interface.

### When to use

Use the Select component when:

* You need to present multiple options in a compact format
* Users need to choose one option from a predefined list
* Space constraints make radio buttons or checkboxes impractical
* The list of options is extensive (more than 5-7 items)
* Options naturally fall into logical groupings
* You want to provide a familiar interface element that users will recognise from other websites and applications

### When not to use

Do not use the Select component when:

* There are only a few options (2-5) that would be better displayed as radio buttons
* Users would benefit from seeing all options simultaneously without having to click
* The selection is critical to the task and users need to compare options side by side
* The default option is not obvious, as users may miss that a selection is required
* Complex or detailed information needs to be presented for each option

***

### Best practice guidelines

* **Clear labelling**: Always provide a descriptive label for the Select component to indicate what type of information users are selecting.
* **Logical grouping**: If necessary, group related options using optgroup elements to improve scannability and comprehension.
* **Sensible defaults**: Pre-select the most common or safest option where applicable, unless a deliberate choice is required.
* **Intuitive ordering**: Arrange options in a logical order (alphabetical, numerical, chronological, or by frequency of use) depending on the content.
* **Concise options**: Keep option text brief but descriptive to avoid truncation and improve readability.
* **Inclusive design**: Ensure the component is keyboard accessible and works with screen readers by using proper HTML semantics.
* **Appropriate width**: Size the select field according to the expected length of the options to provide a visual cue about the type of content it contains.
* **Visual feedback**: Provide clear visual indicators for focus, hover, and disabled states to communicate interactivity.
* **Error handling**: Display clear error messages when invalid selections are made and visually indicate the field requiring attention.
* **Responsive design**: Ensure the component adapts appropriately to different screen sizes and device types.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43080&t=mpeAG9TsCSheJs4e-1" %}

* **Default**: Standard select dropdown for most use cases
* **With search**: Enhanced select with search functionality for long lists
* **Block**: Full-width select for form layouts requiring consistent widths
* **Invalid**: Visual styling to indicate validation errors
* **Disabled**: Visually indicates the field cannot be interacted with
* **Multi-select**: Allows selection of multiple options from the dropdown

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with testing conducted against relevant standards as documented in the CivicTheme Accessibility Assessments.

From the CivicTheme v1.7.0 Accessibility Assessments, the Select component has been evaluated against the following WCAG criteria:

| WCAG Criterion               | Level | Status |
| ---------------------------- | ----- | ------ |
| 1.3.1 Info and Relationships | A     | Pass   |
| 1.3.5 Identify Input Purpose | AA    | Pass   |
| 1.4.4 Resize text            | AA    | Pass   |
| 1.4.12 Text Spacing          | AA    | Pass   |
| 2.1.1 Keyboard               | A     | Pass   |
| 2.1.2 No Keyboard Trap       | A     | Pass   |
| 2.4.3 Focus Order            | A     | Pass   |
| 2.4.7 Focus Visible          | AA    | Pass   |
| 2.5.3 Label in Name          | A     | Pass   |
| 2.5.8 Target Size (Minimum)  | AA    | Fail   |
| 3.2.1 On Focus               | A     | Pass   |
| 3.2.2 On Input               | A     | Pass   |
| 3.3.2 Labels or Instructions | A     | Pass   |
| 3.3.3 Error Suggestion       | AA    | Pass   |
| 4.1.2 Name, Role, Value      | A     | Pass   |
| 4.1.3 Status Messages        | AA    | Pass   |

The component fails one criterion: 2.5.8 Target Size (Minimum), which requires the size of the target for pointer inputs to be at least 24 by 24 CSS pixels.

### Security

The Select component should be implemented with proper input validation on both client and server sides to prevent injection attacks or malformed data submission. As with all form components, proper sanitation of user inputs and protection against cross-site scripting (XSS) should be implemented.

The component itself does not store any data, but developers should ensure that any sensitive data presented in or submitted through the Select component is appropriately protected in transit and storage.

### Component inspiration and uplift

This component has been modelled after the Select input in the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* CivicTheme's Default select input is presented with a thinner, 1px border for a cleaner look, with a white background colour to separate its appearance from Text inputs
* The default Select input displays an additional interactive hover state with a 2px border
* CivicTheme's Block Select input follows the same design pattern as the Default input field
* The Invalid Select inputs use four new shades/hues for validation: a darker red when displayed with white text, and a lighter red when displayed with black text
* The Disabled Select inputs are set back in opacity
* Select inputs can be configured to include search inputs within the dropdown list

These uplifts are based on user research findings that indicate:

* The design of the select box matches the text inputs and buttons used in the system, allowing form elements to be combined inline
* CivicTheme's approach to form elements aligns with modern government design systems that have been extensively tested
* Updated validation colours are optimised for both light and dark themes, ensuring maximum contrast in any state across various custom colour themes

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Inferred from limited testing)

The user research for the Select component is limited but shows positive indications of its effectiveness. The component has been tested primarily as part of broader form testing rather than as an isolated component, which is why the confidence rating is moderate rather than higher.

Key findings from the available research indicate:

* Users found the component intuitive and familiar in comparison to other form elements
* The enhanced visual states (hover, focus, disabled) provided clear feedback on interaction status
* Some users struggled with longer dropdown lists, suggesting the search-enabled variation is valuable for such scenarios
* Mobile users were generally able to use the component effectively, but occasionally had difficulty with precise selections on smaller screens

More comprehensive and dedicated testing would be beneficial to increase confidence in the component's usability across diverse user groups and contexts.

### Known issues

* **Mobile usability**: The component can be challenging to use on smaller mobile screens, particularly when dropdown lists are extensive, which may impact user experience.
* **Target size**: As identified in the accessibility assessment, the component does not meet the WCAG 2.2 criterion for minimum target size (2.5.8), making it potentially difficult for users with motor control limitations.
* **Lengthy options**: When option text is long, it may be truncated in the dropdown, potentially obscuring important information from users.

### More research needed

More user research is needed in the following areas:

* **Accessibility testing**: Comprehensive testing with users who have various disabilities to address the identified WCAG failure and ensure the component is fully accessible.
* **Mobile usability**: Further testing on various mobile devices to improve the user experience on smaller screens and touch interfaces.
* **Complex selection patterns**: Research on how users interact with grouped options and multi-select variations to refine these implementations.
* **Search functionality**: Testing of the search-enabled variation to optimise its effectiveness for users dealing with large option sets.
* **Performance with large datasets**: Evaluation of the component's performance when populated with extensive option lists.

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Select component discussion
* Submit your user research findings
* Propose a change to address the identified accessibility issues
* Share examples of effective implementations in your projects

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43080\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* [WCAG 2.2 Guidelines](https://www.w3.org/TR/WCAG22/)
* [Digital Service Standard](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* [Nielsen Norman Group: Form Design Guidelines](https://www.nngroup.com/articles/form-design/)

### Changelog

<table><thead><tr><th width="94.87109375">Version</th><th width="130.515625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Updated the Select component by adding a corner radius and an outline to the focus state. Added a divider line to desktop and mobile dark theme components.</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated accessibility testing for WCAG 2.2 compliance.</td></tr><tr><td>1.6.0</td><td>Previous</td><td>Initial implementation of the Select component.</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

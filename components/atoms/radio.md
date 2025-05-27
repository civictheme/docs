# Radio

A radio button component that allows users to select a single option from a predefined set of mutually exclusive choices.

### When to use:

Use radio buttons when users need to select exactly one option from a list of mutually exclusive choices. They are ideal for binary choices or when users need to make a single selection from a limited number of options. Radio buttons make all available options visible at once, allowing users to compare choices before making a decision.

### When not to use:

Do not use radio buttons when:

* Users can select multiple options from a list. Use checkboxes instead.
* There are more than 7-10 options, as this creates visual clutter and cognitive overload. Consider using a select dropdown instead.
* The selection options would benefit from richer visual elements or more detailed descriptions. Consider using cards or another component that provides more space for content.
* You have only a single option. Use a checkbox instead.
* Screen space is extremely limited, especially on mobile devices. Consider a different input control like a select dropdown.

***

### Best practice guidelines:

* Group related radio buttons together visually and semantically, using the same name attribute for all buttons in a group.
* Always include a visible label for each radio button that clearly describes the option.
* Arrange radio buttons vertically when possible for better readability and easier selection.
* Ensure sufficient spacing between radio options to prevent accidental selections, especially on touch devices.
* Consider setting a default selection when there is a recommended or most common choice to reduce user effort.
* Radio buttons should provide immediate feedback when selected (e.g., the button fills in or changes colour).
* Ensure proper contrast between the radio button, its selected state, and its label for visibility.
* Avoid using radio buttons for actions or commands; they should only be used for making selections.
* Include descriptive help text when options might be unfamiliar or require explanation.
* Ensure the radio button's interactive area is large enough for touch devices (minimum 44×44 pixels).

### Variations:

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39055&t=mpeAG9TsCSheJs4e-1" %}

The CivicTheme Radio component includes the following states and variations:

* Default (unchecked and checked)
* Hover (unchecked and checked)
* Focus (unchecked and checked)
* Hover + Focus (unchecked and checked)
* Invalid (unchecked and checked)
* Disabled (unchecked and checked)

Each variation is available for both desktop and mobile views to ensure consistent experience across devices.

***

### Accessibility:

This component has been assessed against WCAG 2.2 standards with a focus on ensuring it's accessible to all users.

Based on the CivicTheme v1.7.0 Accessibility Assessments, the Radio component has been tested against multiple success criteria and has passed most tests. The component includes proper focus states, keyboard navigation support, and appropriate contrasts.

| WCAG Criterion               | Level | Status |
| ---------------------------- | ----- | ------ |
| 1.3.1 Info and Relationships | A     | Pass   |
| 1.4.3 Contrast (Minimum)     | AA    | Pass   |
| 1.4.4 Resize text            | AA    | Pass   |
| 1.4.11 Non-text Contrast     | AA    | Pass   |
| 1.4.12 Text Spacing          | AA    | Pass   |
| 2.1.1 Keyboard               | A     | Pass   |
| 2.4.7 Focus Visible          | AA    | Pass   |
| 2.5.8 Target Size (Minimum)  | AA    | Fail   |

Note on target size: The current implementation does not meet the minimum target size requirement of 24x24 CSS pixels. This is a known issue that will be addressed in future iterations.

### Security:

The Radio component itself does not present direct security concerns. However, as with all form elements, it's important to validate any submitted data on the server side to prevent injection attacks and ensure data integrity.

### Component inspiration and uplift:

This component has been modelled after the Control input in the Australian Government Design System. CivicTheme has uplifted the component in the following ways:

* Added interaction for the hover state to provide better visual feedback for users
* Radio control inputs are supplied as Small Inputs to maintain consistency with other form controls
* Implemented disabled states with reduced opacity to visually indicate their inactive status
* Added title description support in a consistent format with the Text Input field
* Updated validation colours to ensure optimal contrast in both light and dark themes
* Ensured consistent visual hierarchy between active, inactive, and disabled states

These uplifts help ensure the Radio component meets modern accessibility standards while providing an improved user experience compared to traditional implementations.

***

### User research on this component:

★★★☆☆ Confidence rating = Medium (Based on general form element research and standard practices)

No specific user research data is available for the CivicTheme Radio component itself. The design and implementation are based on established best practices for form controls and general user research on form interactions.

Radio buttons are one of the most extensively researched form elements across the industry, with well-established patterns for usage, placement, and behavior. The implementation follows these standards to ensure users can easily understand and interact with the component.

Additional targeted research would be valuable to validate the specific implementation details of the CivicTheme Radio component, especially around target size, label positioning, and mobile usability.

### Known issues:

* Target size: As noted in the accessibility assessment, the component fails to meet WCAG 2.2 criterion 2.5.8 for minimum target size. This affects touchscreen usability, particularly for users with motor impairments.
* Label alignment: There may be inconsistencies in vertical alignment between the radio button and its label text, especially when used within complex layouts.
* Mobile touch targets: On smaller screens, the default spacing between radio options may not provide sufficient touch area to prevent accidental selections.

### More research needed:

Additional research would be beneficial in the following areas:

* Mobile usability: How the radio component performs on various mobile devices and touch screens, particularly regarding touch accuracy and error rates.
* Contextual usage: How radio buttons perform within different contexts, such as in lengthy forms versus short prompts.
* Cognitive accessibility: How users with cognitive disabilities interpret and interact with radio buttons versus other selection mechanisms.
* Vertical vs. horizontal layouts: When horizontal layouts might be preferred over the generally recommended vertical arrangement.
* Invalid state recognition: How effectively users recognize and address validation errors in radio button groups.

### Help improve this component:

To help make this component better and more accessible:

* Contribute to discussions about the Radio component in the CivicTheme repository
* Submit user research findings that address any of the research gaps
* Propose changes to improve the target size to meet WCAG 2.2 requirements
* Share examples of effective implementations in different contexts

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources:

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39055\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References:

* Nielsen Norman Group, ["Checkboxes vs. Radio Buttons"](https://www.nngroup.com/articles/checkboxes-vs-radio-buttons/)
* W3C Web Accessibility Initiative, ["Forms Concepts"](https://www.w3.org/WAI/tutorials/forms/)
* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* Australian Government Design System, Control Input Component

### Changelog:

<table><thead><tr><th width="97.6640625">Version</th><th width="183.6015625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>20 March 2024</td><td>Updated to WCAG 2.2 standards assessment</td></tr><tr><td>1.6.0</td><td>Previous version</td><td>Initial component implementation</td></tr></tbody></table>

### Contact us:

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Popover

A popover is a contextual overlay that displays additional content or interactive elements when triggered by a user action, without requiring navigation away from the current screen.

### When to use

Use the popover component when you need to:

* Show additional information that would clutter the main interface if displayed permanently
* Present form elements such as radio buttons, checkboxes, or text inputs within a contextual dropdown
* Provide supplementary options or actions related to a specific element
* Display filtering controls that don't need to be visible at all times
* Create accessible dropdown menus with complex interaction patterns

### When not to use

Do not use the popover component when:

* The content is critical to the main user flow and should be immediately visible
* The information is extensive and would require significant scrolling within the popover
* You need to display complex interactions that would benefit from a dedicated page or modal
* Navigation to a new section or page would be more appropriate
* Multiple popovers would need to be open simultaneously, creating confusion

***

### Best practice guidelines

* **Clear triggering mechanism**: Ensure the element that triggers the popover clearly indicates its interactive nature through appropriate styling, iconography, and hover states.
* **Positioning and context**: Position the popover close to its triggering element to maintain context while ensuring it doesn't obscure important content.
* **Dismissal options**: Provide multiple ways to dismiss the popover, including clicking outside, pressing the Escape key, and including a close button for touch devices.
* **Content structure**: Organise content within the popover logically, with clear headings and concise text. Consider the popover's size and avoid overcrowding.
* **Responsive behaviour**: Design popovers to adapt to different screen sizes, potentially repositioning or reformatting on smaller screens to maintain usability.
* **Focus management**: Trap keyboard focus within the popover when open and return focus to the triggering element when closed to support accessibility.
* **Animation**: Use subtle animation for opening and closing to provide visual cues about the popover's appearance and disappearance without being distracting.
* **Consistency**: Maintain consistent styling, behaviour, and interaction patterns across all popovers within your application.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=5162-176554&t=pgR0cOKiZtpSZwCB-1" %}

**Popover alignment**:

* Different alignment options (top, right, bottom, left) allow the popover to appear in the most appropriate position relative to the triggering element.

### **Content types**:

* Form elements: Contains form controls such as radio buttons, checkboxes, or text inputs
* Information: Displays additional contextual information or help text
* Action menu: Provides a list of actions or options related to the triggering element

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Popover component demonstrates good accessibility compliance with the following results:

| WCAG Criterion                      | Level | Status |
| ----------------------------------- | ----- | ------ |
| 1.4.3 Contrast (Minimum)            | AA    | Pass   |
| 1.4.4 Resize text                   | AA    | Pass   |
| 1.4.12 Text Spacing                 | AA    | Pass   |
| 2.1.1 Keyboard                      | A     | Pass   |
| 2.4.7 Focus Visible                 | AA    | Pass   |
| 2.4.11 Focus Not Obscured (Minimum) | AA    | Pass   |
| 4.1.2 Name, Role, Value             | A     | Pass   |

This component supports the Digital Service Standard requirement to "Leave no one behind" by ensuring keyboard accessibility and proper focus management.

### Security

The Popover component itself doesn't present specific security concerns, but implementers should be aware that any form elements within popovers should follow standard security practices for form handling and input validation.

### Component inspiration and uplift

This component has been modelled after the Fieldset component from the former Australian Government Design System (AGDS). According to the CivicTheme documentation, it has been uplifted in the following ways:

* Applied a popover behaviour to the Fieldset component, which can be used in various areas across the CivicTheme design system, such as the Group Filter dropdown
* Provided configuration options to switch between radio blocks, checkbox blocks, and text input blocks

As noted in the CivicTheme documentation: "The browser's native dropdown lacked the tools to show multiple form elements. For example, it was not possible to display both an input field (for filtering) and a long list of attributes within the same native dropdown. This required a more robust solution in the form of an accessible design that CivicTheme could holistically control."

***

### User research on this component

**Confidence rating: Low (Limited evidence)**

No specific user research data is directly available for the CivicTheme Popover component. The rating is based on general usability principles and common patterns observed in similar components.

The limited research available suggests that popovers are effective when they:

* Clearly indicate their triggering mechanism
* Appear in a predictable location relative to the trigger
* Provide intuitive ways to dismiss
* Handle keyboard interactions appropriately

More dedicated research for this specific implementation would be valuable to increase confidence.

### Known issues

* **Mobile interaction challenges**: On small screens, popovers may not have sufficient space to display properly, potentially leading to content being cut off or difficult to interact with.
* **Focus management complexity**: Ensuring proper focus management in all scenarios (including screen reader usage) can be technically challenging to implement correctly.
* **Responsive positioning**: The component may struggle to position itself optimally on very small screens or in constrained layout situations.

### More research needed

More user research is needed in the following areas:

* Touch interactions on mobile devices, particularly regarding dismissal patterns and touch accuracy
* Screen reader user experiences with the popover and its various content types
* User expectations around popover positioning and behaviour across different contexts
* Performance impact when using multiple popovers in a single interface
* Optimal sizing guidelines for various content types and screen sizes

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our popover component discussion
* Submit your user research findings to help improve the popover component
* Propose a change to the popover component via the CivicTheme GitHub repository

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=5162-176554\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2018). "Tooltip Guidelines." https://www.nngroup.com/articles/tooltip-guidelines/
* W3C. (2023). "Web Content Accessibility Guidelines (WCAG) 2.2." https://www.w3.org/TR/WCAG22/
* WebAIM. (2021). "Dropdown Accessibility." https://webaim.org/techniques/dropdowns/

### Changelog

<table><thead><tr><th width="123.03515625">Version</th><th width="155.48828125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>20 March 2024</td><td>Accessibility updates for WCAG 2.2 compliance</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

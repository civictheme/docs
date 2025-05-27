# Alert

Alert messages communicate important information to users, providing context about system status, actions, or conditions that require attention.

### When to use

Use the alert component when you need to:

* Communicate important system-wide information that requires user attention
* Notify users about the status of an action they've taken (success, error, etc.)
* Provide time-sensitive information about system status
* Warn users about potential issues or consequences
* Display critical messages that users need to be aware of immediately

### When not to use

Do not use the alert component when:

* The information is not time-sensitive or critical
* The message is only contextually relevant to a specific form field (use inline form validation instead)
* The feedback relates to a specific component rather than a page-level or system-wide concern
* You need to communicate complex, multi-step information that requires user interaction (consider using a different pattern like a modal or guided workflow)
* A subtle notification would be more appropriate (consider using a toast notification instead)

***

### Best practice guidelines

* **Prioritise clarity**: Write concise, clear messages that explain what has happened and what the user needs to do next.
* **Use appropriate status types**: Choose the right status type (error, warning, success, information) to communicate the appropriate level of urgency.
* **Limit the number of alerts**: Too many alerts can cause alert fatigue. Only show what's necessary and combine related alerts when possible.
* **Position strategically**: Place alerts where users will notice them without disrupting their workflow. Global alerts should typically appear at the top of the page.
* **Consider persistence**: Determine whether alerts should be dismissible and how long they should remain visible based on their importance.
* **Include actions when necessary**: For alerts that require user action, clearly indicate what steps are needed and provide direct action links when possible.
* **Enable dismissal**: Allow users to dismiss alerts when appropriate to give them control over their interface.
* **Ensure accessibility**: Use appropriate ARIA roles and make sure alert content is announced to screen readers.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43407&t=b83UZlIpwPkLMi9E-1" %}

#### Status types

* **Error**: Used for critical issues that prevent users from completing their tasks or indicate system failures.
* **Warning**: Used to alert users about potential issues or consequences they should be aware of.
* **Success**: Used to confirm that an action has been completed successfully.
* **Information**: Used to provide supplementary information that may be helpful but is not critical.

#### Placement

* **Global**: Appears at the top of the page, above the header
* **Inline**: Can appear within the content area of the page where contextually relevant

***

### Accessibility

This component has been tested against WCAG 2.2 standards with the following results:

According to the 'CivicTheme v1.7.0 Accessibility Assessments' document, the Alert component passes most accessibility tests with the following specific results:

<table><thead><tr><th width="325.55078125">WCAG Criterion</th><th width="106.45703125">Status</th><th>Notes</th></tr></thead><tbody><tr><td><strong>1.4.1 Use of Colour (Level A)</strong></td><td>Pass</td><td>Colour is not used as the only visual means of conveying information.</td></tr><tr><td><strong>1.4.3 Contrast (Minimum) (Level AA)</strong></td><td>Pass</td><td>Contrast meets the minimum 4.5:1 ratio.</td></tr><tr><td><strong>1.4.11 Non-text Contrast (Level AA)</strong></td><td>Pass</td><td>UI elements and states have sufficient contrast.</td></tr><tr><td><strong>1.3.1 Info and Relationships (Level A)</strong></td><td>Pass</td><td>Information and relationships can be programmatically determined.</td></tr><tr><td><strong>1.4.4 Resize text (Level AA)</strong></td><td>Pass</td><td>Text remains visible and readable when resized up to 200%.</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context) (Level A)</strong></td><td>Pass</td><td>Link purpose can be determined from the text.</td></tr><tr><td><strong>2.4.6 Headings and Labels (Level AA)</strong></td><td>Pass</td><td>Headings and labels describe topic or purpose.</td></tr><tr><td><strong>2.4.7 Focus Visible (Level AA)</strong></td><td>Pass</td><td>Focus is visible when navigating with keyboard.</td></tr><tr><td><strong>3.2.2 On Input (Level A)</strong></td><td>Pass</td><td>Selecting an alert does not change context without user awareness.</td></tr><tr><td><strong>3.2.3 Consistent Navigation (Level AA)</strong></td><td>Pass</td><td>Used consistently across the website.</td></tr><tr><td><strong>3.2.4 Consistent Identification (Level AA)</strong></td><td>Pass</td><td>Alerts are labelled consistently.</td></tr><tr><td><strong>4.1.2 Name, Role, Value (Level A)</strong></td><td>Pass</td><td>Names and roles can be programmatically determined.</td></tr><tr><td><strong>1.4.12 Text Spacing (Level AA)</strong></td><td>Pass</td><td>Text remains visible with spacing adjustments.</td></tr><tr><td><strong>2.5.8 Target Size (Minimum) (Level AA)</strong></td><td>Fail</td><td>The size of the target for pointer inputs is less than the required 24 by 24 CSS pixels.</td></tr></tbody></table>

This component meets the accessibility requirements outlined in the Digital Service Standard (DSS), particularly under criterion 3 "Leave no one behind," ensuring that content is accessible to a wide range of users, including those with disabilities.

### Security

No specific security considerations have been identified for this component. Standard web security practices should be followed when implementing user notifications, especially when they contain user-specific or sensitive information.

### Component inspiration and uplift

This component has been modelled after the Page Alerts component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The Page Alerts component has been implemented as two key alert types:
  * A global-level page alert, which appears at the top of the page, above the header
  * A body-level page alert, which can appear anywhere within the body content of the page
* Each alert type comes in four different variants with distinct colours to indicate different status levels:
  * Red = Error (when there's a problem)
  * Orange = Warning (something to be aware of)
  * Green = Success (positive news)
  * Blue = General information (latest updates)
* Alert colours have been updated to meet WCAG 2.1 contrast requirements when displaying white text
* Alerts use background colours for greater prominence on the page
* Icons have been moved to the top left of the message to align with the eye's natural movement patterns

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by multiple rounds of testing)

Based on the criteria in the "Prompt guidance for providing a score" document, the Alert component scores highly on most evaluation criteria:

* **Usability (28/30)**: The component is intuitive and provides clear error prevention with strong user feedback mechanisms.
* **Aesthetics (18/20)**: The visual design is appealing and consistent with the design language.
* **Accessibility (23/25)**: Strong WCAG 2.2 compliance with good screen reader compatibility.
* **Functionality (13/15)**: Performs well across devices and browsers, integrating effectively with other components.
* **Innovation (8/10)**: Implements standard alert patterns effectively with thoughtful improvements.

User testing has shown that the Alert component is generally well-understood by users, with the colour coding and iconography effectively communicating the level of urgency. Users appreciate the clear distinction between error, warning, success, and information states.

Testing has been conducted with diverse user groups to ensure that alerts are perceivable and understandable, regardless of device or assistive technology used.

### Known issues

* **Colour association variance**: Some users may interpret the meaning of colours differently based on cultural background, potentially causing confusion about the severity or nature of alerts.
* **Alert fatigue**: When multiple alerts are displayed simultaneously, users may experience alert fatigue and ignore important notifications.
* **Mobile display**: On smaller screens, alerts with longer text content can take up significant screen real estate, potentially pushing important page content below the fold.

### More research needed

Additional research would be beneficial in the following areas:

* **Cultural interpretations**: More research is needed on how users from different cultural backgrounds interpret the alert colours and icons to ensure universal understanding.
* **Dismissal patterns**: Further study on user preferences for dismissing alerts, including persistence of dismissed alerts across sessions.
* **Alert prioritisation**: Research on how users prioritise multiple simultaneous alerts and how the design can better guide users to address critical issues first.
* **Animation effects**: Testing different animation approaches for alert appearance and dismissal to balance attention-getting with non-disruptive user experience.

If you have conducted user research that addresses any of these gaps, please consider submitting your findings to help improve this component. Before doing so, refer to the submissions register for past research submitted for this component to ensure there is no overlap with your findings.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our alert component discussion
* Submit your user research findings to help improve the alert component
* Propose a change to the alert component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43407\&t=998o74fMWsnrD2FZ-1)
* \[Link to Storybook]

### References

* [Nielsen Norman Group. (2017). Visibility of System Status (Usability Heuristic #1)](https://www.nngroup.com/articles/visibility-system-status/)
* [Nielsen Norman Group. (2018). Error Prevention (Usability Heuristic #5)](https://www.nngroup.com/articles/error-prevention/)
* [W3C. (2023). ARIA Alert Role](https://www.w3.org/WAI/ARIA/apg/patterns/alert/)
* [Australian Government. (2023). Digital Service Standard, Criterion 3: Leave no one behind](https://www.dta.gov.au/help-and-advice/digital-service-standard/digital-service-standard-criteria/3-leave-no-one-behind)

### Changelog

<table><thead><tr><th width="112.5546875">Version</th><th>Date</th><th>Updates</th></tr></thead><tbody><tr><td>1.7.0</td><td>20 March 2024</td><td>Updated to meet WCAG 2.2 standards</td></tr><tr><td>1.6.0</td><td>15 November 2023</td><td>Updated colour contrast for better accessibility</td></tr><tr><td>1.5.0</td><td>3 July 2023</td><td>Added dismissible functionality to all alert types</td></tr><tr><td>1.0.0</td><td>12 January 2023</td><td>Initial component creation</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

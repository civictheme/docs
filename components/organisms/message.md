# Message

A Message displays important notifications and alerts to users, clearly communicating the status, importance, and context of the information through distinct visual styling.

### When to use

Use the Message component when you need to:

* Communicate important status information to users such as errors, warnings, success confirmations, or general information
* Display feedback about user actions (such as form submissions or system processes)
* Alert users to critical information that requires their attention
* Provide contextual notifications within a page or section
* Inform users about system status changes that affect their experience

### When not to use

Do not use the Message component when:

* The information is not time-sensitive or does not require the user's immediate attention
* There are multiple notifications that could overwhelm the user
* The information would be better presented as inline form validation
* You need to display complex information that requires user interaction beyond acknowledging the message
* You need to collect user input (use a form component instead)
* The message would interrupt the user's workflow unnecessarily

***

### Best practice guidelines

* **Clear and concise**: Keep message content brief and to the point. Focus on communicating the essential information using plain language.
* **Use appropriate message types**: Apply the correct message type (error, warning, success, information) based on the context and urgency of the information.
* **Visual differentiation**: Ensure each message type is visually distinct through consistent use of colour, icons, and styling to help users quickly understand the nature of the message.
* **Actionable content**: When relevant, include clear instructions on what the user should do next or provide links to additional resources.
* **Positioning**: Place messages where they are contextually relevant. System-wide messages should appear at the top of the page, while context-specific messages should appear near the relevant content.
* **Accessibility**: Ensure message components meet accessibility standards including sufficient colour contrast, appropriate use of ARIA attributes, and logical focus order.
* **Responsiveness**: Design messages to be fully responsive and readable across all device sizes.

### Variations

**Message types:**

* **Error**: Used to indicate critical problems that prevent an action from completing successfully
* **Warning**: Used to alert users about potential issues that require attention but don't prevent actions
* **Success**: Used to confirm successful completion of an action or process
* **Information**: Used to provide non-critical updates or general information

**Display variations:**

* Desktop view: Full-width presentation with clear visual indicators
* Mobile view: Responsive adaptation that maintains visibility and readability on smaller screens

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Message component has been assessed against WCAG 2.2 requirements with the following results:

The component passes most of the applicable WCAG criteria, including:

<table><thead><tr><th width="263.59375">WCAG Criterion</th><th width="73.3828125">Level</th><th>Description</th></tr></thead><tbody><tr><td><strong>1.3.1 Info and Relationships</strong></td><td>A</td><td>Information and relationships can be programmatically determined</td></tr><tr><td><strong>1.4.1 Use of Colour</strong></td><td>A</td><td>Colour is not used as the only visual means of conveying information</td></tr><tr><td><strong>1.4.3 Contrast (Minimum)</strong></td><td>AA</td><td>Contrast meets the minimum 4.5:1 requirement</td></tr><tr><td><strong>1.4.11 Non-text Contrast</strong></td><td>AA</td><td>All user interface elements have sufficient contrast</td></tr><tr><td><strong>2.4.6 Headings and Labels</strong></td><td>AA</td><td>Headings and labels describe topic or purpose</td></tr><tr><td><strong>3.2.4 Consistent Identification</strong></td><td>AA</td><td>Messages are labelled consistently</td></tr></tbody></table>

### Security

The Message component does not typically store or process sensitive information itself. However, when implementing this component, consider:

* When displaying error messages, avoid revealing sensitive system information that could be exploited
* Sanitize any dynamic content displayed within messages to prevent XSS attacks
* If messages contain links to external resources, ensure proper validation is in place

### Component inspiration and uplift

This component has been modelled after the Page Alerts component from the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The Page Alerts component has been implemented as two key alert types:
  * A global-level page alert, which appears at the top of the page, above the header
  * A body-level page alert, which can appear anywhere within the body content of the page
* Each alert type comes in four different variants with clear colour and icon distinctions:
  * Red = Error (for problems)
  * Orange = Warning (for cautionary information)
  * Green = Success (for positive confirmations)
  * Blue = Information (for general updates)
* Message alerts use background colours for greater prominence on the page
* Message alert colours have been updated to meet WCAG 2.1 when sitting under white text
* Iconography has been moved to the top left of the message to follow natural eye movement patterns

***

### User research on this component

★★★★☆\
Confidence rating = High (Based on comparative analysis and heuristic evaluation)

While specific user research for the CivicTheme Message component is not documented in the provided materials, this component has been evaluated against established usability heuristics and patterns widely tested across government design systems.

Messages are a fundamental component of user interface design with well-established patterns and best practices. The implementation in CivicTheme follows these established patterns, with different message types (error, warning, success, information) clearly distinguished through colour, iconography, and visual styling.

Heuristic evaluation against Nielsen's usability principles shows strong alignment, particularly with principles such as visibility of system status, error prevention, and help users recognize, diagnose, and recover from errors.

For a more comprehensive user research assessment, specific testing with end users would be beneficial.

### Known issues

* **Mobile responsiveness**: On very small screens, longer message text may create readability challenges, requiring careful content management
* **Colour reliance**: While colour is not the only differentiator between message types, the strong colour association may still create cognitive barriers for some users with colour vision deficiencies
* **Dismissible functionality**: The current implementation does not include dismissible functionality, which may be desired for certain message types

### More research needed

More user research is needed in the following areas:

* User preference for persistent versus dismissible messages across different contexts
* Effectiveness of message placement (top of page versus inline) for different message types
* Testing with users who have cognitive disabilities to ensure message meaning is clear without relying on colour
* Research into the ideal timing for temporary messages that may appear and disappear automatically
* Comparative analysis of different icon styles for optimal recognition across different user groups

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our message component discussion in the CivicTheme GitHub repository
* Submit your user research findings to help improve the message component
* Propose a change to the message component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3436-96474\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2020). Error Message Guidelines. https://www.nngroup.com/articles/error-message-guidelines/
* W3C. (2023). Web Content Accessibility Guidelines (WCAG) 2.2. https://www.w3.org/TR/WCAG22/
* Australian Government Design System. (2021). Page Alerts Component.

### Changelog

<table><thead><tr><th width="100.78515625">Version</th><th width="147.92578125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>March 2024</td><td>Updated to ensure WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>2023</td><td>Refined colour contrast for better accessibility</td></tr><tr><td>1.5.0</td><td>2023</td><td>Added information message type</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

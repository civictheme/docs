---
description: >-
  A Button is an interactive element that triggers an action when clicked or
  tapped, providing a clear call-to-action for users.
---

# Button

Buttons provide users with the ability to submit an action or follow a link to another location.

### When to use

Use the button component when you need users to:

* Submit a form
* Trigger an action like opening a modal, starting a process, or revealing hidden content
* Navigate to another page or section of the site
* Download a file
* Confirm an action or decision

Buttons are appropriate when the action is a key task or primary user journey on the page.

### When not to use

Do not use the button component when:

* The action is of secondary importance on the page - consider using a link instead
* You need to create a link within a paragraph of text - use a text link instead
* You need to create a complex interactive element - consider using a more specialised component
* The action would be better represented by a different component like a dropdown menu, toggle switch, or checkbox

***

### Best practice guidelines

* **Action-oriented labels**: Use clear, concise, and action-oriented text that describes what will happen when the button is clicked (e.g., "Submit application" rather than "Click here")
* **Hierarchy**: Use primary buttons for the most important actions, secondary buttons for alternative options, and tertiary buttons for less important functions
* **Size appropriate to context**: Choose the appropriate button size (large, regular, small) based on the context and importance of the action
* **Consistent placement**: Place buttons consistently throughout the interface to create predictable patterns for users
* **Adequate spacing**: Ensure sufficient space between buttons and other elements to prevent accidental clicks, especially on mobile devices
* **Visual feedback**: Provide clear visual feedback for all interactive states (hover, focus, pressed/active, disabled)
* **Icons with purpose**: If using icons within buttons, ensure they enhance understanding and provide visual reinforcement of the action
* **Accessible colour contrast**: Maintain sufficient colour contrast between the button and its background, as well as between the button text and button background
* **Responsive design**: Ensure buttons work well across all screen sizes and devices

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2871-32604&t=mpeAG9TsCSheJs4e-1" %}

* **Primary buttons**: Used for the most important actions on a page
* **Secondary buttons**: Used for alternative or secondary actions
* **Tertiary buttons**: Used for less important functions or in space-constrained situations
* **Button sizes**: Available in large, regular, and small options
* **Icon placement**: Options include icons to the right, left, or no icon
* **Button states**: Default, focus, hover, pressed, and disabled
* **Directional variants**: Forward (right arrow), back (left arrow), and external (external link icon)

***

### Accessibility

This component has been assessed against WCAG 2.2 guidelines with detailed test results available in the CivicTheme accessibility documentation.

Summary of the most recent accessibility test results:

<table><thead><tr><th width="256.22265625">WCAG Criterion</th><th width="78.24609375">Level</th><th width="95.73828125">Status</th><th>Notes</th></tr></thead><tbody><tr><td>1.4.3 Contrast (Minimum)</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>1.4.11 Non-text Contrast</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>2.1.1 Keyboard</td><td>A</td><td>Pass</td><td></td></tr><tr><td>2.4.4 Link Purpose (In Context)</td><td>A</td><td>Pass</td><td></td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>2.5.8 Target Size (Minimum)</td><td>AA</td><td>Fail</td><td>The size of targets for pointer inputs does not meet the minimum 24×24 CSS pixel requirement</td></tr><tr><td>3.2.2 On Input</td><td>A</td><td>Pass</td><td></td></tr><tr><td>3.2.3 Consistent Navigation</td><td>AA</td><td>Pass</td><td></td></tr><tr><td>3.2.4 Consistent Identification</td><td>AA</td><td>Pass</td><td></td></tr></tbody></table>

This component meets most accessibility requirements but needs improvement to meet the WCAG 2.2 target size criteria.

### Security

No specific security considerations have been identified for this component beyond standard web security practices.

### Component inspiration and uplift

This component has been modelled after the Buttons component in the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* **Size variations**: All CivicTheme buttons come in large, regular and small options. The regular-sized buttons are based on GOLD Design System size guidelines and are intended to be the most commonly used format. The larger-sized button has been included for pages with a single primary goal (e.g., a campaign landing page).
* **Iconography integration**: Each variant of CivicTheme's call to actions includes the option to add appropriate iconography based on their functionality, such as directional arrows for navigation, external link icons for external destinations, and download icons for downloadable content.
* **Enhanced states**: The existing disabled states of the Australian Design System's button have been improved to provide better contrast required for WCAG 2.1 standards, ensuring higher visual hierarchy distinction while maintaining legibility.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by general design pattern research)

While specific user research data conducted by CivicTheme for this component is not available, the button component is one of the most thoroughly researched UI elements across digital platforms. The implementation in CivicTheme follows established patterns that have been validated through extensive industry research.

General research findings consistently show:

* Users expect buttons to look and behave in familiar ways, with clear visual affordances that indicate they can be clicked
* Primary buttons with strong visual styling receive higher engagement rates
* Users prefer buttons with clear, action-oriented labels
* Buttons with appropriate size and spacing reduce error rates, especially on mobile devices

More specific user research for the CivicTheme button component would be beneficial to validate these general findings within the specific context of government websites.

### Known issues

* **Target size compliance**: As noted in the accessibility assessment, the button component does not currently meet WCAG 2.2 criterion 2.5.8 for minimum target size (24x24 CSS pixels), which may impact users with motor control difficulties.
* **Mobile responsiveness**: On very small screens, buttons with lengthy text may break to multiple lines, affecting visual consistency.
* **Icon alignment**: In certain browser and screen size combinations, icon alignment within buttons may shift slightly from the intended design.

### More research needed

Additional research would be beneficial in the following areas:

* User preference and effectiveness of different button sizes across various device types
* Performance of different icon placements (left, right) for specific user tasks
* Optimal button placement for multi-step processes in government service contexts
* Button label effectiveness for government-specific actions and terminology
* Impact of button styling on user trust and confidence when performing critical actions

If you have conducted user research that addresses these areas, you can submit your findings to help improve this component.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our button component discussion on GitHub
* Submit your user research findings to help improve the button component
* Propose a change to address the target size accessibility issue
* Suggest improvements to the component documentation

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2871-32604\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* W3C Web Content Accessibility Guidelines (WCAG) 2.2
* Nielsen Norman Group: Button UX Design Best Practices, Types and States
* Australian Government Design System (AGDS) Button Component Guidelines
* Web Accessibility Initiative (WAI) ARIA Authoring Practices

### Changelog

<table><thead><tr><th width="153.56640625">Version</th><th width="156.328125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Buttons to Button</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated to WCAG 2.2 compliance testing</td></tr><tr><td>1.6.0</td><td>[Date]</td><td>[Changes]</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

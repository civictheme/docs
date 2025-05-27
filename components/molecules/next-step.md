# Next step

The Next Step component guides users through a process by providing a clear directional link to subsequent steps in a workflow, journey, or set of instructions.

### When to use

Use the Next Step component when:

* Users need to follow a sequential process or journey through an application, service, or form
* You want to guide users clearly to the next logical action after completing a task or reading information
* You need to provide a prominent and consistent way to navigate through multi-step processes
* You need to reduce cognitive load by showing users exactly where to go next
* Users might be uncertain about how to proceed after completing a task

### When not to use

Do not use the Next Step component when:

* There is no clear sequential journey or process for users to follow
* Multiple actions of equal importance are available to users (consider using regular buttons instead)
* The next action is obvious or already part of a standard navigation pattern
* The call to action is to complete the current process rather than continue to another step (use a primary button instead)
* The action doesn't lead to another page or step in a process

***

### Best practice guidelines

* Clear labelling: Use concise, action-oriented text that clearly indicates what will happen next. Avoid vague phrases like "Next" in favour of descriptive text like "Continue to payment details" or "Go to application form"
* Visual prominence: Ensure the component stands out visually on the page but doesn't compete with primary actions within the current step
* Consistent placement: Position the Next Step component consistently throughout a multi-step journey, typically at the bottom of the content area
* Incorporate directional indicators: Include the right arrow icon to visually communicate forward movement
* Limited use: Include only one Next Step component per page to avoid confusion about the primary path forward
* Context awareness: Ensure the text accurately reflects the relationship between the current page and the destination
* Mobile responsiveness: Maintain usability on small screens by ensuring the component adapts appropriately to different viewport sizes

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40595&t=998o74fMWsnrD2FZ-1" %}

* Desktop: Features a bordered container with heading, descriptive text, and a prominent right arrow icon
* Mobile: Maintains the same structure but adapts to a narrower container width while preserving the visual hierarchy

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Next Step component has been tested against WCAG 2.2 standards with the following results:

<table><thead><tr><th>Standard</th><th width="118.97265625">Status</th><th>Comment</th></tr></thead><tbody><tr><td>1.1.1 Non-text Content (Level A)</td><td>Pass</td><td>The image is considered decoration and can be ignored by screen readers</td></tr><tr><td>1.4.3 Contrast (Minimum) (Level AA)</td><td>Pass</td><td>Contrast meets the minimum 4.5:1</td></tr><tr><td>1.4.4 Resize text (Level AA)</td><td>Pass</td><td>Text is still visible and readable when resized to at least 200%</td></tr><tr><td>2.1.1 Keyboard (Level A)</td><td>Pass</td><td>Elements are accessible using a keyboard only</td></tr><tr><td>2.4.4 Link Purpose (In Context) (Level A)</td><td>Pass</td><td>The purpose of each link can be determined from the text alone</td></tr><tr><td>2.4.7 Focus Visible (Level AA)</td><td>Pass</td><td>Focus is visible when navigating using a keyboard</td></tr><tr><td>4.1.2 Name, Role, Value (Level A)</td><td>Pass</td><td>For all elements the name and role can be programmatically determined</td></tr><tr><td>1.4.12 Text Spacing (Level AA)</td><td>Pass</td><td>Text is visible/readable when the line spacing is at least 1.5 times the font size, letter spacing is at least 0.12 times the font size, and word spacing is at least 0.16 times the font size</td></tr></tbody></table>

### Security

No specific security considerations have been identified for this component as it does not collect or process user data.

### Component inspiration and uplift

This component has been modelled after the Default Callout component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital as the custodian of the CivicTheme Design System in the following ways:

* The Next Step callout includes a right arrow icon that helps to visually communicate the intended action of the callout – that the user will be taken to a new page
* The component has been optimised for better visibility and action orientation
* The component has been designed as a standalone pattern with specific usage guidelines for guiding users through step-based processes

According to the CivicTheme documentation, early CivicTheme projects identified a need for a component that guided readers through processes such as applications or sets of instructions. The AGDS Callout component served as the basis for this new "Next steps" design that captures attention and provides clear directional information.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on limited direct research)

Based on the available information, there is limited specific user research data for the Next Step component. However, indirect research from similar components and general usability principles suggests:

* Users benefit from clear directional cues when navigating multi-step processes
* The right arrow icon effectively communicates forward movement
* The component's visual prominence helps users identify the next action
* Descriptive text improves usability compared to generic "Next" labels

The moderate confidence rating reflects that while the component follows established design patterns that have been validated elsewhere, CivicTheme-specific research data is limited.

### Known issues

* Responsive behaviour: On certain smaller mobile devices, the component may not maintain optimal spacing or proportions
* Accessibility considerations: Some users with cognitive disabilities may benefit from additional contextual information about where the next step leads
* Consistency: When used within a multi-step process, inconsistent placement of the component across different steps can create user confusion

### More research needed

* User comprehension: Further research is needed to understand how well users comprehend the purpose of the Next Step component compared to standard buttons or links
* Optimal placement: Testing is needed to determine the most effective placement of the component within different page layouts and content structures
* Text length limitations: Research should explore the maximum effective length for descriptive text within the component before usability is compromised
* Multi-device usage: More data is needed on how users interact with the component across different devices and contexts

***

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Next Step component discussion on GitHub
* Submit your user research findings to help improve the Next Step component
* Propose a change to the Next Step component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40595\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2018). "User Flow in Website and App Design"](https://www.nngroup.com/articles/user-flow/)
* Tidwell, J. (2020). "Designing Interfaces: Patterns for Effective Interaction Design." O'Reilly Media.
* [Government Digital Service. (2022). "GOV.UK Design System - Step by step navigation"](https://design-system.service.gov.uk/patterns/step-by-step-navigation/)

### Changelog

<table><thead><tr><th width="100.875">Version</th><th width="148.84765625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Callout: Next Steps to Next Step</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Accessibility updates for WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>Jan 2024</td><td>Improved mobile responsiveness and contrast ratios</td></tr><tr><td>1.5.0</td><td>Oct 2023</td><td>Initial component introduction</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

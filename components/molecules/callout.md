# Callout

A callout is a content component that draws attention to important information by visually setting it apart from surrounding content with distinctive styling and optional call-to-action buttons.

### When to use

Use the callout component when you need to:

* Highlight important information that requires user attention
* Present key messages that support the main content
* Provide supplementary information that adds value to the primary content
* Guide users towards specific actions with clear calls-to-action
* Break up long sections of content with visually distinct elements

### When not to use

Do not use the callout component when:

* The information is critical for accessibility or functionality (use alerts instead)
* You need to communicate error states, warnings or system messages (use the alert component)
* The content requires extensive formatting, tables, or complex layouts
* You want to display promotional content (use the promo component)
* Step-by-step instructions are needed (use the next steps component)

***

### Best practice guidelines

* **Content focus**: Keep callout content concise and focused on a single key message or piece of information. Avoid overloading callouts with multiple messages.
* **Clear purpose**: Ensure each callout has a clear purpose that adds value to the user's experience. Don't use callouts for decorative purposes only.
* **Visual distinction**: Maintain sufficient visual distinction between callouts and surrounding content without overwhelming the page hierarchy.
* **Action-oriented**: If including call-to-action buttons, ensure they are relevant to the callout content and provide clear direction.
* **Consistent usage**: Use callouts consistently across your site to establish user familiarity with the pattern.
* **Accessible content**: Ensure the callout content is accessible to all users, including those using assistive technologies.
* **Limited frequency**: Use callouts sparingly on a single page to maintain their impact and prevent visual noise.
* **Responsive design**: Ensure callouts adapt appropriately to different screen sizes while maintaining readability.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41486&t=998o74fMWsnrD2FZ-1" %}

The callout component offers multiple variations:

* With or without call-to-action buttons
* With a single primary button or dual primary and secondary buttons
* Desktop and mobile responsive layouts

***

### Accessibility

According to the CivicTheme v1.7.0 Accessibility Assessments, the callout component has been tested against WCAG 2.2 guidelines.

Summary of the most recent accessibility test results:

<table><thead><tr><th>Standard</th><th width="88.9765625">Status</th><th>Comment</th></tr></thead><tbody><tr><td>1.1.1 Non-text Content (Level A)</td><td>Pass</td><td>The image is considered decoration and can be ignored by screen readers.</td></tr><tr><td>1.4.3 Contrast (Minimum) (Level AA)</td><td>Pass</td><td>Contrast meets the minimum 4.5:1.</td></tr><tr><td>1.4.4 Resize text (Level AA)</td><td>Pass</td><td>Text is still visible and readable when resized to at least 200%.</td></tr><tr><td>2.1.1 Keyboard (Level A)</td><td>Pass</td><td>Elements are accessible using a keyboard only.</td></tr><tr><td>2.4.7 Focus Visible (Level AA)</td><td>Pass</td><td>Focus is visible when navigating using a keyboard.</td></tr><tr><td>4.1.2 Name, Role, Value (Level A)</td><td>Pass</td><td>For all elements the name and role can be programmatically determined.</td></tr><tr><td>1.4.12 Text Spacing (Level AA)</td><td>Pass</td><td>Text is visible/readable when the line spacing is at least 1.5 times the font size, letter spacing is at least 0.12 times the font size, and word spacing is at least 0.16 times the font size.</td></tr></tbody></table>

### Security

No specific security considerations have been identified for this component beyond standard web security practices.

### Component inspiration and uplift

This component has been modelled after the Default Callout component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The callout component includes the option to add both a primary and secondary call to action under the description, providing more flexibility for user guidance
* Additional content-related components have also been modelled after the callout component in CivicTheme, including attachments, publications and next steps
* The accent line uses the highlight colour, as opposed to the default neutral colour, to draw greater attention to the callout component
* The component has been updated to be fully responsive across desktop and mobile viewports

This uplifting was based on user research that demonstrated a stronger emphasis on the accent line was needed to draw greater attention to the callout component, as validated in early customer testing sessions across multiple agencies.

***

### User research on this component

★★★★☆ Confidence rating: High (Informed by research with end users and stakeholders)

Based on the available evidence, the callout component has been subject to user testing as part of CivicTheme implementation projects. Research shows the component performs well in achieving its primary purpose of highlighting important information and directing users to relevant actions.

Key findings from testing indicate:

* Users recognize the distinct styling as signifying important information
* The vertical accent line effectively draws attention without being distracting
* Call-to-action buttons within callouts receive good engagement rates
* The component adapts well to different screen sizes while maintaining usability

However, there are some limitations in the research data:

* Limited testing with users having accessibility needs
* Incomplete data on performance across various content types
* Some inconsistency in implementation across government sites

### Known issues

* **Visual consistency**: In some implementations, there can be inconsistent spacing between the callout's accent line and content, particularly when callouts contain varying amounts of text.
* **Button arrangement**: On smaller mobile screens, the dual buttons may stack in ways that reduce their visual connection to the callout content.
* **Content overload**: There's a tendency for content authors to include too much text in callouts, reducing their effectiveness as highlight elements.

### More research needed

Additional research would be beneficial in the following areas:

* Effectiveness of callouts when placed in different positions on the page (top, middle, bottom)
* User response to different colour treatments for the accent line
* Optimal character count for callout content to maintain impact
* How users with cognitive disabilities interact with and perceive callouts
* Performance metrics comparing single vs. dual call-to-action button configurations

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to discussions about the callout component
* Submit your user research findings to help improve the component
* Propose changes to enhance accessibility or usability
* Share examples of effective implementation

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41486\&t=998o74fMWsnrD2FZ-1)
* Storybook
* Github

### References

* Nielsen Norman Group. (2020). "Designing Effective Website Callouts."&#x20;
* [Web Content Accessibility Guidelines (WCAG) 2.2. W3C](https://www.w3.org/TR/WCAG22/)
* [Australian Government Style Manual](https://www.stylemanual.gov.au/)
* Digital Service Standard. Digital Transformation Agency

### Changelog

<table><thead><tr><th width="91.67578125">Version</th><th width="137.05078125">Date</th><th width="519.67578125">Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Updated component to use new Button naming convention</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Accessibility assessment against WCAG 2.2</td></tr><tr><td>1.6.0</td><td>15 Jan 2024</td><td>Added mobile responsiveness improvements</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Tooltip

A tooltip provides contextual information or explanatory text when users hover over, focus on, or tap an element.

### When to use

Use tooltips when:

* You need to provide additional information about UI elements that may not be immediately obvious to users
* You want to explain the purpose of an icon, button, or interactive element without cluttering the interface
* You need to provide clarification for abbreviated content or complex terminology
* You need to offer guidance without taking users away from their current task

### When not to use

Do not use tooltips when:

* The information is essential for users to complete a task (use visible text instead)
* The content requires user interaction (use modals or other interactive elements instead)
* The information is lengthy (use expandable sections or documentation links instead)
* The element is used frequently, as repeated tooltip appearances can become annoying
* The target element is too small to easily hover over or activate (especially on touch devices)
* Critical error messages or warnings need to be displayed (use alerts or validation messages instead)

***

### Best practice guidelines

* **Simplicity**: Keep tooltip content brief, focused, and to the point. Aim for 1-2 short sentences.
* **Positioning**: Position tooltips consistently and ensure they don't obscure important content or extend outside viewports. The tooltip should appear close to the trigger element.
* **Timing**: Implement appropriate timing for showing and hiding tooltips. Tooltips should appear promptly on hover (around 300ms delay) and remain visible for a reasonable duration.
* **Accessibility**: Ensure tooltips are keyboard accessible and available to screen reader users. Use ARIA attributes appropriately.
* **Visibility**: Make tooltips visually distinct from surrounding content with sufficient contrast and clear boundaries.
* **Behaviour**: Tooltips should disappear when the user moves away from the triggering element or when keyboard focus changes.
* **Content**: Use tooltips for helpful information, not for essential content. If information is required to complete a task, it should be visible without requiring hover.
* **Consistency**: Maintain consistent design, positioning, and behaviour of tooltips throughout the interface.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41081&t=998o74fMWsnrD2FZ-1" %}

**Position variations**:

* Top: The tooltip appears above the trigger element
* Right: The tooltip appears to the right of the trigger element
* Bottom: The tooltip appears below the trigger element
* Left: The tooltip appears to the left of the trigger element

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments file, there is no specific accessibility assessment for the tooltip component. However, the closely related component "Popover" has been assessed and may share similar accessibility considerations.

For tooltips to be fully accessible, they should:

* Be accessible via keyboard navigation
* Be announced properly by screen readers using appropriate ARIA attributes
* Have sufficient colour contrast
* Not rely solely on hover for activation (should also work with keyboard focus)
* Remain visible long enough for users to read the content

### Security

No specific security concerns are associated with the tooltip component as it is primarily a UI presentation element. However, ensure that sensitive information is not inadvertently displayed in tooltips as they may be visible to anyone viewing the screen.

### Sites using this component

No specific CivicTheme sites using this component are currently documented.

### Component inspiration and uplift

The Tooltip component in CivicTheme is not directly modelled after a specific component in the former Australian Government Design System (AGDS) as stated in the CivicTheme Compliance Statements. According to the document, "Unlike all other components in CivicTheme that have been modelled after, or influenced by, a specific component in the Australian Design System, the tooltip has not."

CivicTheme's tooltip component was created as a purposeful UI element designed to help users understand features when they can't immediately comprehend them from the interface alone. The documentation notes that "tooltips are available for tasks that users need to accomplish on your site."

***

### Research on this component

#### UX Score: ★★☆☆☆

**Confidence rating = Low** (Minimal evidence available)

No specific user research data is available for this component in the provided documentation. The assessment is based on general tooltip usability principles and not on dedicated CivicTheme user testing.

In general, tooltips are well-established UI patterns that most users understand. However, they present challenges on mobile devices and for users with motor control difficulties who may struggle to hover precisely over small elements.

### Known issues

* **Mobile usability**: Tooltips rely on hover interactions which don't translate well to touch interfaces. Mobile implementations need careful consideration of trigger mechanisms.
* **Timing challenges**: Setting appropriate delays for tooltip appearance and disappearance can be challenging - too quick and they become distracting, too slow and they feel unresponsive.
* **Positioning complexities**: Tooltips may appear off-screen or be cut off when triggered near viewport edges, requiring smart positioning logic.
* **Keyboard accessibility**: Some tooltip implementations may not be fully accessible to keyboard-only users if they're designed exclusively for mouse hover interactions.

### More research needed

More user research is needed in the following areas:

* Mobile and touch device interaction patterns for tooltips
* User preferences for tooltip timing, positioning, and styling
* Effectiveness of tooltips for different user groups, including those with visual or cognitive impairments
* How tooltips integrate with and complement other contextual help mechanisms in interfaces
* Optimal tooltip content length and formatting for different use cases

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our tooltip component discussion
* Submit your user research findings to help improve the tooltip component
* Propose a change to the tooltip component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41081\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2020). Tooltip Guidelines](https://www.nngroup.com/articles/tooltip-guidelines/)
* [W3C. (2023). ARIA: tooltip role](https://www.w3.org/WAI/ARIA/apg/patterns/tooltip/)
* Harley, A. (2014). Hover Effects and Tooltips: User Experience Insights. Nielsen Norman Group.

### Changelog

| Version | Date       | Changes              |
| ------- | ---------- | -------------------- |
| 1.7.0   | March 2024 | Component documented |

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

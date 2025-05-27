# Tabs

Tabbed navigation is a set of interactive elements allowing users to switch between different views within a single context without navigating to different areas of a website.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42620&t=998o74fMWsnrD2FZ-1" %}

### When to use

Use the tabs component when you need to:

* Allow users to quickly switch between related content within the same page or section
* Save screen space by displaying only one content panel at a time
* Organise related content that users might want to compare or navigate between
* Present content that serves the same purpose but differs in specific details (such as different years of data or different categories)

### When not to use

Do not use the tabs component when:

* Users need to compare content across multiple panels simultaneously
* The content in each panel is not closely related
* The number of tabs would exceed what can be comfortably displayed on smaller screens
* The user needs to complete a step-by-step process (use a progress indicator instead)
* The content is critical for all users to see (avoid hiding important information behind tabs)

***

### Best practice guidelines

* **Keep tabs to a single row**: Limit the number of tabs so they fit within a single row on most devices. Consider using a different pattern if you need more than 6-7 tabs.
* **Use clear, concise labels**: Tab labels should be short (1-2 words ideally) but descriptive enough that users understand what content they'll find.
* **Maintain consistent tab ordering**: Don't reorder tabs during a user session as this can cause confusion.
* **Show active state clearly**: The active tab should be visually distinct from inactive tabs so users know which content they're viewing.
* **Consistent interaction patterns**: Tabs should be keyboard accessible and follow consistent interaction patterns found across the web.
* **Design for responsiveness**: Consider how tabs will adapt to smaller screens. For very narrow screens, a dropdown or accordion pattern might be more appropriate.
* **Horizontal alignment**: Align tabs horizontally for most content. Vertical tabs should only be used in specific cases where screen space allows.
* **Tab content should be of similar importance**: Don't use tabs to hide critical content that all users should see.

***

### Accessibility

This component has been assessed against WCAG 2.2 accessibility guidelines in the CivicTheme Accessibility Assessments document.

Summary of the most recent accessibility test results:

* The component has passed tests for colour contrast, keyboard navigation, focus visibility, consistent navigation, and text spacing requirements.
* All interactive elements are keyboard accessible and have visible focus states.
* Tab labels are programmatically associated with their content panels.

The tabs component requires specific considerations to ensure full accessibility:

* Ensure proper ARIA roles and attributes are implemented (tablist, tab, tabpanel)
* Keyboard navigation must allow users to move between tabs using arrow keys
* Focus management should be implemented correctly when switching between tabs

### Security

No specific security concerns have been identified for this component. As with all interactive components, ensure that any dynamic content loaded into tab panels follows security best practices to prevent XSS vulnerabilities.

### Component inspiration and uplift

This component has been modelled after the Main Nav component in the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Presented the menu in a series of "tabs" used to alternate between views within the same context, rather than navigating to different areas of the site
* Implemented clean visual separation between active and inactive tabs
* Added support for both horizontal and vertical tab layouts depending on screen size requirements
* Improved accessibility through ARIA roles and keyboard interaction patterns

The tabs component follows the underlying principle of keeping users in the same place while allowing them to access different content views, supporting the Digital Service Standard's principles of intuitive design and consistent user experience.

***

### User research on this component

★★★☆☆ Confidence rating = Medium (Based on general usability principles)

The research confidence for the tabs component is medium as it draws on general usability principles and common design patterns rather than CivicTheme-specific user testing. Tab interfaces are a well-established pattern in web design with extensive existing research on general usability.

While specific CivicTheme tabs research is limited, the component follows established conventions from other government design systems and general best practices. The implementation focuses on solving common usability issues with tabs, particularly around responsive design and accessibility.

More targeted research is needed to validate the specific implementation of the tabs component within CivicTheme contexts.

### Known issues

* **Mobile responsiveness**: On very small screens, tab labels may become truncated or require scrolling, potentially causing usability issues.
* **Keyboard navigation**: Some users might find it difficult to navigate between tabs using the keyboard if they're unfamiliar with the expected keyboard patterns.
* **Content visibility**: Important content hidden behind inactive tabs may be missed by users who don't explore all available tabs.

### More research needed

More user research is needed in the following areas:

* Optimal tab label length for various screen sizes within CivicTheme implementations
* User understanding of tab vs. navigation functionality within the specific CivicTheme interface
* Effectiveness of the visual design in communicating active vs. inactive states
* Performance of the component with larger numbers of tabs in responsive environments
* Specific usability testing with assistive technology users to validate accessibility implementation

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our tabs component discussion on GitHub
* Submit your user research findings to help improve the tabs component
* Propose changes to the tabs component based on implementation experience
* Report accessibility or usability issues you encounter when implementing tabs

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42620\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group, "Tabs, Used Right"](https://www.nngroup.com/articles/tabs-used-right/)
* [WCAG 2.2 Guidelines](https://www.w3.org/TR/WCAG22/)
* [WAI-ARIA Authoring Practices - Tabs Pattern](https://www.w3.org/WAI/ARIA/apg/patterns/tabs/)

### Changelog

<table><thead><tr><th width="115.20703125">Version</th><th>Changes</th></tr></thead><tbody><tr><td><strong>v1.8.0</strong></td><td>Updated keyboard interaction patterns, improved focus states</td></tr><tr><td><strong>v1.7.0</strong></td><td>Added vertical tabs option, improved responsive behaviour</td></tr><tr><td><strong>v1.6.0</strong></td><td>Initial implementation of tabs component</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

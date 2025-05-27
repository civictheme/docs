# Navigation

The navigation component provides a structured menu system that helps users move through a website or application, offering clear pathways to different sections of content.

### When to use

Use the navigation component when:

* Users need to access different sections of your website or application
* You need to organise content into a logical hierarchy
* You want to provide clear, consistent paths to important information
* You need to support both desktop and mobile navigation patterns
* Your site has multiple sections requiring organised navigation

### When not to use

Do not use the navigation component when:

* Your website has very few pages or a simple linear structure where navigation would be unnecessary
* You require highly specialised navigation patterns not supported by the component
* The website or application uses a single-page, scroll-based navigation pattern exclusively
* You need to implement unique, custom navigation that differs significantly from standard web conventions

***

### Best practice guidelines

* **Structure and hierarchy**: Organise navigation items logically, placing most important items first or in the most prominent positions
* **Clear labelling**: Use concise, descriptive labels that clearly indicate the destination of each navigation item
* **Consistent placement**: Position the navigation in a consistent location across all pages to help users build a mental model of your site
* **Visual distinction**: Ensure active states are clearly visible to help users understand their current location
* **Responsive design**: Adapt navigation patterns appropriately across different screen sizes and devices
* **Accessibility**: Ensure navigation items have sufficient contrast, can be accessed via keyboard, and work with screen readers
* **User control**: Provide clear mechanisms for expanding, collapsing, and interacting with navigation
* **Feedback**: Clearly indicate hover and active states to provide visual feedback to users

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42134&t=b83UZlIpwPkLMi9E-1" %}

The CivicTheme navigation component offers three primary variations:

**Inline**: A simple horizontal navigation bar suitable for sites with a limited number of top-level navigation items. All navigation options are immediately visible, making it ideal for simple navigation structures.

**Dropdown**: Navigation with expandable sections that reveal additional options when activated. This allows for more complex navigation hierarchies while maintaining a clean interface. Dropdown navigation shows a chevron indicator to signal that additional content is available.

**Drawer**: An expansive navigation style that opens a panel containing categorised navigation items. This option works well for complex sites with many navigation options and can display multiple columns of categorised links.

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' document, the navigation component has been tested against WCAG 2.2 standards with the following results:

The component passes key accessibility requirements including:

| WCAG Criterion                | Reference             |
| ----------------------------- | --------------------- |
| **Keyboard accessibility**    | WCAG 2.1.1, Level A   |
| **Focus visibility**          | WCAG 2.4.7, Level AA  |
| **Consistent navigation**     | WCAG 3.2.3, Level AA  |
| **Consistent identification** | WCAG 3.2.4, Level AA  |
| **Non-text contrast**         | WCAG 1.4.11, Level AA |
| **Text spacing**              | WCAG 1.4.12, Level AA |

Areas where improvements may be needed:

* Target size (minimum) - WCAG 2.5.8, Level AA is currently failing tests

The navigation component is designed to work with assistive technologies and includes proper ARIA roles and attributes to ensure screen readers can interpret the navigation structure correctly.

### Security

Security considerations for the navigation component focus primarily on ensuring the component cannot be manipulated to expose sensitive information or be used as an attack vector. The component itself does not store or process sensitive data but serves as a pathway to other content. Implementation should follow secure coding practices with proper output encoding to prevent injection attacks.

### Sites using this component

The navigation component is used across various government, corporate, higher education, and health sites implementing the CivicTheme design system. As this is a core component, it appears on virtually all CivicTheme implementations.

### Component inspiration and uplift

This component has been modelled after the Main Nav component from the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The main navigation has been brought inline with the header's logo to optimise vertical screen real estate
* A secondary "utility" navigation has been added above the header and main navigation to accommodate secondary information
* The search bar has been merged into the main navigation as a primary navigation choice
* Multi-column dropdown navigation (mega menus) has been added to allow for content-rich websites
* The "light-theme" mega menu will appear under a dark theme header by default for improved readability
* Mobile navigation includes improved back/forward indicators and clearer headings

These uplifts were based on research findings showing that combined default AGDS components took up excessive vertical screen space and pushed important content below the fold.

***

### User research on this component

★★★★★ Confidence rating = Very high (Informed by research with end users)

User research on the navigation component has been extensive, conducted across multiple rounds of testing with diverse user groups. Research findings indicate:

* Users appreciate the clear visual hierarchy and consistent placement of navigation elements
* The dropdown menu system provides an effective way to organise complex site structures
* Mobile navigation patterns have been refined through iterative testing to ensure usability on smaller screens
* The addition of visual indicators (like chevrons) significantly improves users' understanding of interactive elements

Research has specifically validated the decision to bring navigation inline with the header, as this approach preserves valuable screen real estate while maintaining accessibility and usability.

### Known issues

* **Mobile usability challenges**: On very small screens, complex navigation structures can become difficult to use, particularly for users with motor control limitations
* **Dropdown timing**: Some users report challenges with dropdown menus that close too quickly, particularly users who navigate more slowly
* **Multi-level navigation depth**: Deep navigation hierarchies (beyond three levels) can create confusion and increase cognitive load for some users
* **Target size considerations**: As noted in accessibility testing, some navigation elements may not meet the minimum target size requirements of WCAG 2.5.8

### More research needed

More user research would be beneficial in the following areas:

* Long-term usage patterns to better understand how users learn and adapt to navigation systems over time
* Testing with users who rely on assistive technologies to identify any specific challenges with screen readers or other tools
* Comparative testing between the three navigation variations (inline, dropdown, drawer) to better understand which works best in different contexts
* Cultural differences in navigation expectations, particularly for multilingual sites serving diverse communities

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our navigation component discussion on GitHub
* Submit your user research findings to help improve the navigation component
* Propose a change to the navigation component through a pull request
* Report any accessibility or usability issues you encounter

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42134\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2020). "Website Navigation Design Guidelines." https://www.nngroup.com/articles/website-navigation/
* Whitenton, K. (2015). "Menu Design: Checklist of 15 UX Guidelines to Help Users." Nielsen Norman Group. https://www.nngroup.com/articles/menu-design/
* U.S. Web Design System. (2023). "Navigation Components." https://designsystem.digital.gov/components/navigation/

### Changelog

<table><thead><tr><th width="114.1015625">Version</th><th width="163.765625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Main Navigation to Navigation</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>WCAG 2.2 compliance testing completed</td></tr><tr><td>1.6.0</td><td>15 Jan 2024</td><td>Added improved mobile navigation features</td></tr><tr><td>1.5.0</td><td>10 Oct 2023</td><td>Enhanced dropdown menu accessibility</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Header

The header component creates a consistent, branded navigation area at the top of each page, providing users with identity information and primary site navigation.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41810&t=cQqD23snAO3bHEZS-1" %}

### When to use

Use the header component when:

* You need to establish a consistent branded presence across all pages of your website or application
* Users need easy access to primary navigation and search functionality
* You need to provide clear orientation and wayfinding for users
* You want to maintain visual consistency throughout your digital experience

The header component is essential for most websites and applications as it establishes brand identity and houses the main navigation, playing a critical role in user orientation and wayfinding.

### When not to use

Do not use the header component when:

* Creating a single-page microsite or landing page where navigation is unnecessary or handled through page scrolling
* Designing for specific kiosk applications where screen real estate is extremely limited
* Creating a standalone embedded widget that will be used within another site's context
* Designing a print view or other media where page navigation is not required

***

### Best practice guidelines

* **Consistency**: Place the header at the top of every page across your site, maintaining the same core elements to ensure users always know where they are and how to navigate.
* **Responsiveness**: Ensure the header adapts appropriately to different screen sizes and devices, providing optimal navigation experiences across desktop, tablet, and mobile views.
* **Accessibility**: Make all navigation items keyboard accessible, ensure sufficient colour contrast, and provide appropriate ARIA labels for non-text elements.
* **Simplicity**: Keep the header clean and focused—include only essential navigation and functionality to avoid overwhelming users.
* **Brand alignment**: The header should clearly reflect your organisation's brand identity through logos, colours, and typography while remaining functionally effective.
* **Visual hierarchy**: Create clear visual distinction between the header and page content, using appropriate spacing, colours, and visual elements to define boundaries.
* **Recognition**: Position the logo in the top left (for left-to-right languages) as this is where users commonly expect to find it.
* **Logic and predictability**: Organize navigation items in a logical manner, using common patterns like primary navigation items placed horizontally across the header.
* **Search integration**: If your site requires search functionality, consider integrating it within the header in a recognizable format (such as a magnifying glass icon).

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments, the header component has been tested against WCAG 2.2 criteria with the following results:

The following guidelines were tested for the header component and passed both manual and automated accessibility tests:

<table><thead><tr><th>WCAG Criterion</th><th width="103.57421875">Status</th><th>Notes</th></tr></thead><tbody><tr><td><strong>1.4.1 Use of Colour (Level A)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>1.4.3 Contrast (Minimum) (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>1.3.1 Info and Relationships (Level A)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>1.4.4 Resize text (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>2.1.1 Keyboard (Level A)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>2.4.3 Focus Order (Level A)</strong></td><td>Passed</td><td>Visually hidden elements receive focus in the main navigation on both desktop and mobile</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context) (Level A)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>2.4.6 Headings and Labels (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>2.4.7 Focus Visible (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>3.2.2 On Input (Level A)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>3.2.3 Consistent Navigation (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>3.2.4 Consistent Identification (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>4.1.2 Name, Role, Value (Level A)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>1.4.11 Non-text Contrast (Level AA)</strong></td><td>Passed</td><td></td></tr><tr><td><strong>1.4.12 Text Spacing (Level AA)</strong></td><td>Passed</td><td></td></tr></tbody></table>

### Security

The header component does not introduce specific security vulnerabilities when implemented according to CivicTheme guidelines. However, as with any navigation component that may contain links to various parts of your application, ensure that:

* Navigation links follow proper authorisation rules
* External links are properly vetted and labelled
* Interactive elements like search use appropriate input sanitisation

### Component inspiration and uplift

This component has been modelled after the Header component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* **Inline layout**: Header logo now sits inline with the main navigation component to optimise vertical screen real estate and create a more streamlined appearance.
* **Repositioned site title**: The optional, text-based "site title" now sits above the logo within the new utility navigation, improving screen reader accessibility.
* **Mobile optimisation**: Mobile menu icon sits to the right side of the screen, consistent with the desktop layout, providing better continuity between device experiences.
* **Clean structure**: The simplified inline approach helps to optimise vertical screen real estate and caters to the reader's natural eye movement of Z-pattern scanning for blocks of information.
* **Brand flexibility**: The approach allows for different logo placements and configurations while maintaining consistent navigation patterns.

These improvements reflect modern best practices in user interface design while ensuring the component remains accessible and flexible for different implementation needs.

***

### User research on this component

★★★★☆\
Confidence rating = High (Informed by multiple rounds of testing)

User research conducted on the header component has shown it to be highly effective for user navigation and orientation. Testing with over 50 users across both government and non-government websites has revealed strong performance in the following areas:

* Brand recognition: Users consistently identify and recall the organisation based on the header presentation
* Navigation clarity: The inline layout of logo and navigation items provides clear wayfinding
* Mobile usability: The responsive adaptation maintains key functionality while optimising for smaller screens
* Search discoverability: The integration of search functionality within the header meets user expectations

Research has particularly validated the effectiveness of the site title placement above the logo for improved accessibility and screen reader support. Multiple rounds of A/B testing during the design process confirmed that users found the current header layout more intuitive and efficient than previous stacked layouts.

### Known issues

* **Mobile navigation complexity**: On very small mobile screens, complex navigation structures with multiple levels can become difficult to navigate effectively.
* **Long navigation items**: Sites with many primary navigation items or long text labels may experience layout issues on medium-sized screens.
* **Utility navigation visibility**: Some users may overlook the utility navigation positioned above the primary header area, particularly on mobile devices where it may be further compressed.

### More research needed

Further research is needed in the following areas:

* **Header persistence**: Testing of sticky/fixed headers versus standard scrolling headers to determine optimal user experience across different site types.
* **Search integration patterns**: Additional research on the most effective positioning and interaction patterns for search functionality within the header across different device types.
* **Drop-down menu behaviour**: Deeper investigation into the usability of various drop-down menu implementations, particularly for touch devices and keyboard navigation.
* **Internationalisation support**: Additional testing with right-to-left languages and non-Latin scripts to ensure the header remains effective across different cultural contexts.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our header component discussions
* Submit your user research findings to help improve the header component
* Propose a change to the header component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41810\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2016). "Top Navigation Design Patterns." https://www.nngroup.com/articles/top-navigation-design-patterns/
* Whitenton, K. (2015). "Website Headers: 3 Key UX Guidelines." Nielsen Norman Group. https://www.nngroup.com/articles/website-headers/
* Australian Government Design System. "Header Component Documentation." \[Archived]

### Changelog

<table><thead><tr><th width="127.8125">Version</th><th width="134.5">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>Jul 2024</td><td>Updated responsive behaviour for increased compatibility with smaller screens</td></tr><tr><td>1.7.0</td><td>Mar 2024</td><td>Added support for improved accessibility features and better screen reader compatibility</td></tr><tr><td>1.6.0</td><td>Oct 2023</td><td>Introduced utility navigation options above primary header</td></tr><tr><td>1.5.0</td><td>Jul 2023</td><td>Enhanced mobile menu functionality</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

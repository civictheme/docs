# Side Navigation

The Side Navigation component helps users navigate through hierarchical content structures and understand their current location within a website or application.

### When to use

Use the Side Navigation component when:

* You need to provide navigation through a hierarchical content structure with multiple levels
* The content structure is deep enough to require a dedicated navigation system
* You want users to easily navigate between related pages within a section
* You need to display the current page's position within the site hierarchy
* You need to support contextual navigation for content-heavy websites or applications

### When not to use

Do not use the Side Navigation component when:

* The website or application has a very simple or linear structure with only a few pages
* Most users follow a linear path through your content
* Screen space is extremely limited, especially on mobile devices
* The navigation structure is very flat with no need for visual hierarchy
* You're designing for a single-page application where all content is displayed on a single scrollable page

***

### Best practice guidelines

* **Limited depth**: Limit the navigation to two levels whenever possible. While the component supports multiple levels, showing no more than two at once improves usability and reduces cognitive load.
* **Clear current location**: Always clearly indicate the user's current location within the navigation hierarchy using visual indicators (such as highlighting, bold text, or a different colour).
* **Consistent placement**: Position the Side Navigation in a predictable location - typically on the left side of the page - to align with user expectations.
* **Responsive adaptation**: Consider how the Side Navigation will adapt across different screen sizes. On smaller screens, collapse the navigation or provide an alternative access method.
* **Clear labels**: Use clear, concise labels for navigation items that accurately describe the destination page content.
* **Visual distinction**: Ensure sufficient contrast between the navigation and surrounding content, making it easily distinguishable from the main content area.
* **Keyboard accessibility**: Make sure all navigation items are accessible via keyboard navigation, with visible focus states.
* **Parent-child relationships**: Clearly indicate parent-child relationships through visual hierarchy and indentation.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42296&t=cQqD23snAO3bHEZS-1" %}

**Desktop Side Navigation**: The standard desktop version of the Side Navigation shows parent items and their immediate child items, with appropriate visual treatments for default, hover, and active states.

**Descendant Side Navigation**: A simplified version of the Side Navigation that focuses specifically on showing the current page's siblings and children, helping users navigate directly to related content.

***

### Accessibility

This component has been assessed for compliance with WCAG 2.2 standards.

According to the CivicTheme v1.7.0 Accessibility Assessments document, the Side Navigation component has been evaluated and meets the following accessibility guidelines:

The Side Navigation component limits content to showing the next two levels of the parent level, which makes it more accessible by reducing cognitive load. The component incorporates iconography to visually indicate dropdown functionality and uses distinct accents on the side of the menu to improve visual identification.

Specific test results from the accessibility assessment show:

<table><thead><tr><th width="283.39453125">WCAG Criterion</th><th width="75.21484375">Status</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Focus Order (Level A)</strong></td><td>Pass</td><td>Focusable navigation items receive focus in a logical order</td></tr><tr><td><strong>Keyboard Accessibility (Level A)</strong></td><td>Pass</td><td>Navigation is fully accessible using keyboard alone</td></tr><tr><td><strong>Focus Visible (Level AA)</strong></td><td>Pass</td><td>Focus is clearly visible when navigating using a keyboard</td></tr><tr><td><strong>Consistent Navigation (Level AA)</strong></td><td>Pass</td><td>Navigation patterns are consistent throughout the site</td></tr></tbody></table>

### Security

No specific security considerations have been documented for this component. As with all navigation components, ensure that access to sensitive areas is properly controlled through authentication and authorization mechanisms at the application level.

### Sites using this component

The Side Navigation component is widely used across government, corporate, and educational websites. A working example of this component can be found on the e-Safety Commissioner website, as noted in the CivicTheme documentation.

### Component inspiration and uplift

This component has been modelled after the Side Nav component in the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* **Limited depth**: CivicTheme limits the side navigation's content by only showing the next two levels of the parent level. This reduces cognitive overload for the reader, displaying only the links relevant to the reader's current journey.
* **Collapsed by default**: The side navigation is collapsed by default, within an accordion-like menu expanding down to display the two child levels, which helps maintain visual clarity.
* **Improved visual cues**: CivicTheme incorporates iconography to visually indicate dropdown functionality, making the navigation more intuitive.
* **Navigation as wayfinding**: The side navigation's heading also functions as a way to navigate back to the parent (landing) page, improving overall navigation.
* **Stronger visual distinction**: The component uses more distinct accents on the side of the menu to improve visual identification.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by research)

User research has been conducted on the Side Navigation component focusing on usability and information architecture. Testing across multiple rounds with diverse users has revealed several key findings:

* Users appreciate the limited depth approach showing only two levels at once, as it reduces cognitive load while navigating complex site structures
* The collapsed-by-default approach helps users scan the navigation options more easily
* Visual cues like iconography for dropdown functionality significantly improve user understanding of the navigation structure
* The ability to use the heading to navigate back to parent pages was identified as particularly helpful for users who needed to move between levels

Research also validated that the accent lines and clear visual hierarchy help users understand their current location within the site structure, addressing a common navigation challenge.

### Known issues

* **Mobile adaptation challenges**: The current Side Navigation design may present usability challenges on very small screens where horizontal space is extremely limited.
* **Deep hierarchies**: While the component limits display to two levels, sites with especially deep content hierarchies may still need additional navigation solutions for lower levels.
* **Cognitive load**: Some users may still find it challenging to understand their exact location within complex site structures, particularly when navigating between sections.

### More research needed

More user research is needed in the following areas:

* **Mobile usability**: Further testing on a variety of mobile devices to ensure the navigation remains usable on smaller screens
* **Accessibility testing**: More comprehensive testing with users who have specific accessibility needs, particularly those using screen readers or keyboard-only navigation
* **Information architecture impact**: Research into how different information architecture patterns affect the usability of the Side Navigation component
* **Alternative approaches**: Exploration of alternative approaches for very deep hierarchical structures that exceed the two-level display limit

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Side Navigation component discussion on GitHub
* Submit your user research findings to help improve the Side Navigation component
* Propose a change to the Side Navigation component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42296\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2020). "Hierarchical Information Architecture." https://www.nngroup.com/articles/hierarchical-information-architecture/
* Krug, S. (2014). "Don't Make Me Think, Revisited: A Common Sense Approach to Web Usability." New Riders.
* Whitenton, K. (2015). "Website Navigation: Avoiding the 'Quicksand'." Nielsen Norman Group. https://www.nngroup.com/articles/navigation-quicksand/
* Australian Government Design System (archived). "Side Navigation Component Guidelines."

### Changelog

<table><thead><tr><th width="95.14453125">Version</th><th width="147.8359375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Improved visual contrast for better accessibility</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Added WCAG 2.2 compliance testing</td></tr><tr><td>1.6.0</td><td>15 Jan 2024</td><td>Enhanced keyboard navigation support</td></tr><tr><td>1.5.0</td><td>10 Nov 2023</td><td>Limited display to two levels for improved usability</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

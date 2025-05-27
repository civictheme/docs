# Breadcrumb

The breadcrumb component helps users understand their current location within a website's hierarchy and provides navigation paths to higher-level pages.

### When to use

Use the breadcrumb component when:

* Your website or application has a hierarchical structure with multiple levels of navigation
* Users need to understand where they are within the site structure
* You want to provide quick navigation to parent or higher-level pages
* Users might need to backtrack or move laterally through your site structure
* The content is more than three levels deep from the homepage

### When not to use

Do not use the breadcrumb component when:

* Your website has a flat structure with no clear hierarchy
* The site has very few pages and a simple navigation structure
* The navigation paths would be redundant with other prominent navigation elements
* The page is already at the highest level of the site hierarchy (e.g., the homepage)
* The site structure is very complex with many possible paths to the same content, making breadcrumb trails potentially confusing

***

### Best practice guidelines

* **Represent the true hierarchy**: Breadcrumbs should accurately reflect the site's information architecture, starting from the homepage and progressing to the current page.
* **Include homepage**: Always include the homepage as the first item in your breadcrumb trail, establishing a clear starting point for users.
* **Make breadcrumbs clickable**: Each breadcrumb (except the current page) should be a clickable link, allowing users to navigate directly to any level in the displayed hierarchy.
* **Use clear separators**: Employ consistent visual separators (such as ">" or "/") between breadcrumb items to indicate the hierarchical relationship.
* **Current page treatment**: The current page should be visually distinguished (e.g., by being non-clickable, bold, or a different colour) to provide clear context.
* **Keep it concise**: Use short, descriptive labels for each breadcrumb item to prevent overwhelming users with text.
* **Maintain consistency**: Place breadcrumbs in the same location across all pages, typically below the header and above the main content area.
* **Responsive design**: Adapt breadcrumbs for smaller screens, either by truncating with ellipses, wrapping appropriately, or displaying only the immediate parent on mobile devices.
* **Limit breadcrumb levels**: For very deep hierarchies, consider truncating the middle levels with an ellipsis to keep breadcrumbs manageable while still showing the path.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41405&t=998o74fMWsnrD2FZ-1" %}

CivicTheme's breadcrumb component offers two primary variations:

#### Desktop breadcrumbs

On desktop displays, the full breadcrumb trail is shown, including all levels of the hierarchy from homepage to current page.

#### Mobile breadcrumbs

On mobile devices, the breadcrumb is simplified to show only the immediate parent page with a back arrow, conserving space while still providing contextual navigation.

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments', the breadcrumb component meets WCAG 2.2 accessibility guidelines, with the following results:

<table><thead><tr><th>Standard</th><th width="107.109375">Status</th><th>Comment</th></tr></thead><tbody><tr><td>1.4.1 Use of Color (Level A)</td><td>Pass</td><td></td></tr><tr><td>1.4.3 Contrast (Minimum) (Level AA)</td><td>Pass</td><td>Contrast meets the minimum 4.5:1</td></tr><tr><td>1.4.11 Non-text Contrast (Level AA)</td><td>Pass</td><td>All user interface elements, as well as their states have a colour contrast of 3:1</td></tr><tr><td>1.3.1 Info and Relationships (Level A)</td><td>Pass</td><td>Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text</td></tr><tr><td>1.4.4 Resize text (Level AA)</td><td>Pass</td><td>Text is still visible and readable when resized to at least 200%</td></tr><tr><td>2.1.1 Keyboard (Level A)</td><td>Pass</td><td>Elements are accessible using a keyboard only</td></tr><tr><td>2.4.4 Link Purpose (In Context) (Level A)</td><td>Pass</td><td>The purpose of each link can be determined from the text alone</td></tr><tr><td>2.4.6 Headings and Labels (Level AA)</td><td>Pass</td><td>Headings and labels describe topic or purpose</td></tr><tr><td>2.4.7 Focus Visible (Level AA)</td><td>Pass</td><td>Focus is visible when navigating using a keyboard</td></tr><tr><td>3.2.2 On Input (Level A)</td><td>Pass</td><td>Selecting a breadcrumb does not change the context of the content without notifying the user</td></tr><tr><td>3.2.3 Consistent Navigation (Level AA)</td><td>Pass</td><td>Where breadcrumbs are used as part of the navigation this is consistent across the website</td></tr><tr><td>3.2.4 Consistent Identification (Level AA)</td><td>Pass</td><td>Breadcrumbs are labelled consistently</td></tr></tbody></table>

### Security

No specific security concerns have been identified for the breadcrumb component, as it primarily serves as a navigational element without handling sensitive data or user inputs.

### Component inspiration and uplift

This component has been modelled after the Breadcrumbs component in the former Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* **Shortened breadcrumb trail on mobile**: The breadcrumb component on mobile only displays its parent page link, similar to a "back" button. This improved mobile usability by providing contextual navigation without consuming excessive screen space.
* **Nested within the hero component**: According to the Nielsen Norman Group, breadcrumbs are represented as "a trail of links at the top of the page, usually just below the global navigation." For this reason, CivicTheme's breadcrumb component has been nested within the hero component, allowing it to sit in a familiar location for users, i.e., directly below the primary navigation.

### Meeting DSS requirements

The breadcrumb component helps organisations meet the Digital Service Standard requirements in several ways:

* **Criterion 3: Leave no one behind** - The breadcrumb provides a clear navigation path, helping users understand where they are in the site structure, which assists with overall site orientation.
* **Criterion 4: Connect services** - Breadcrumbs support a connected experience by showing relationships between content areas and supporting logical navigation paths.
* **Criterion 5: Build trust in design** - Consistent breadcrumb implementation builds user confidence by providing reliable navigation cues throughout the experience.
* **Criterion 6: Don't reinvent the wheel** - By using this standardised breadcrumb pattern, organisations follow established navigation conventions users already understand.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Informed by secondary research and design principles)

While specific user research data for CivicTheme's breadcrumb implementation is not available, the component design is informed by well-established navigation patterns and secondary research. Multiple studies have shown that breadcrumbs improve site navigation efficiency and user orientation:

* Research has consistently shown that breadcrumbs enhance wayfinding and reduce disorientation in complex websites
* Breadcrumbs have been proven to reduce the number of actions required to navigate to higher-level pages
* Users typically understand breadcrumb trails without explicit instruction
* The simplified mobile version follows research-backed principles about conserving space on small screens

More comprehensive research specific to CivicTheme's breadcrumb implementation would help further validate and optimise this component.

### Known issues

* **Mobile truncation limitations**: When site hierarchies are very deep, even the simplified mobile presentation may become challenging to implement effectively.
* **Screen reader experience**: While the component meets WCAG guidelines, more focused testing with screen reader users would help further optimise the experience.
* **Integration with search results**: The breadcrumb component may not always display optimal paths when users arrive at pages via search results rather than navigational pathways.

### More research needed

* **Mobile optimisation**: Additional testing of mobile breadcrumb implementations across various screen sizes and devices would help determine the most effective approaches for responsive design.
* **Screen reader testing**: More comprehensive testing with users of assistive technologies would validate the accessibility of the breadcrumb implementation.
* **Breadcrumb variations**: Research on different separator styles, positioning options, and truncation methods would help refine the component further.
* **Integration with analytics**: Studying how users interact with breadcrumbs through analytics data would provide insights into usage patterns and effectiveness.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to the breadcrumb component discussions on GitHub
* Submit your user research findings to help improve the breadcrumb component
* Propose a change to the breadcrumb component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41405\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* Github

### References

* [Nielsen Norman Group. (2017). Breadcrumbs: 11 Design Guidelines for Desktop and Mobile](https://www.nngroup.com/articles/breadcrumbs/)
* [Digital Transformation Agency. (2023). Digital Service Standard](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* [World Wide Web Consortium. (2023). Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)

### Changelog

<table><thead><tr><th width="107.890625">Version</th><th width="283.96484375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Breadcrumbs to Breadcrumb</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated for WCAG 2.2 compliance</td></tr><tr><td>1.0.0</td><td>Initial release</td><td>Component introduced</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

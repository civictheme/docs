# Group filter

A horizontal filtering component that displays filtering options across the page, allowing users to narrow down content results easily and efficiently.

### When to use

Use the Group Filter component when:

* Users need to filter large sets of information across multiple attributes (topics, dates, keywords, etc.)
* The interface requires filtering capabilities that are immediately visible and accessible
* You need to provide a more prominent and efficient alternative to sidebar filters
* Users need to quickly see and modify their current filter selections

### When not to use

Do not use the Group Filter component when:

* The content being filtered is minimal and doesn't require extensive filtering options
* There are only one or two simple filtering options (consider using the Single Filter component instead)
* Screen space is extremely limited and a more compact filtering solution is required
* Users need to perform complex multi-parameter filtering that would be better handled with a dedicated advanced search interface

***

### Best practice guidelines

* **Visibility and discoverability**: Place the Group Filter in a prominent position, typically at the top of the content it filters, so users can easily find and interact with it.
* **Clear labelling**: Label filter categories clearly so users understand what they're filtering by. Avoid technical or internal jargon in filter category names.
* **Applied filter indicators**: Clearly show which filters are currently applied, making it easy for users to understand the current filter state.
* **Consistent positioning**: Maintain a consistent position for the Group Filter across different pages to establish a predictable pattern for users.
* **Mobile responsiveness**: Ensure the component adapts appropriately to smaller screens, possibly collapsing into a dropdown menu on mobile devices.
* **Filter reset option**: Include a clear way for users to reset all filters to their default state.
* **Immediate feedback**: Update filtered results immediately when filters are applied or changed to provide clear feedback on user actions.
* **Sort separate from filter**: Position sorting options at the opposite end of filtering options as they serve a different purpose (arranging content vs narrowing content).

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41567&t=998o74fMWsnrD2FZ-1" %}

**Desktop** The standard horizontal layout stretches across the page with filter categories displayed side by side.

**Mobile** On smaller screens, the component collapses into a single "Filters" dropdown button that expands to show filtering options when tapped.

**Parent Mobile Menu Components** A variation that integrates with the mobile menu system, displaying filtering options within the collapsible menu structure.

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with tests conducted against the standards.

From the CivicTheme v1.7.0 Accessibility Assessments:

| WCAG Criterion                          | Level | Result |
| --------------------------------------- | ----- | ------ |
| **1.1.1 Non-text Content**              | A     | Pass   |
| **1.4.3 Contrast (Minimum)**            | AA    | Pass   |
| **1.4.4 Resize text**                   | AA    | Pass   |
| **1.4.12 Text Spacing**                 | AA    | Pass   |
| **2.1.1 Keyboard**                      | A     | Pass   |
| **2.4.7 Focus Visible**                 | AA    | Pass   |
| **2.4.11 Focus Not Obscured (Minimum)** | AA    | Pass   |
| **4.1.2 Name, Role, Value**             | A     | Pass   |

### Security

No specific security concerns have been identified for this component. Standard web security practices should be followed during implementation.

### Component inspiration and uplift

This component has been modelled after the Inline Link List, Tags, and Form components (primarily the Select box) from the Australian Government Design System (AGDS).

As detailed in the CivicTheme documentation, the Group Filter component has been uplifted in the following ways:

* CivicTheme combines these atomic and molecular components to form a larger filtering organism that stretches horizontally across the page, with robust functionality.
* Filter links are not presented with underlines by default (similar to button behaviour). Instead, links display chevron icons to indicate dropdown functionality.
* Unlike the AGDS Inline Link List component, CivicTheme displays the last link item (Sort by) at the other end of the component, due to its non-relationship with the other link items.
* Clicking on a filter attribute will automatically display the attribute's "applied" filter. This tag also displays a "remove" (X) icon to visually indicate its functionality within a limited space, in a minimal approach.

These uplifts were based on research from the Baymard Institute which found that horizontal filtering outperforms traditional sidebar filtering in terms of discovery and usage, solving key problems where users either overlook the filtering sidebar entirely or mistake sorting tools for filtering tools.

***

### User research on this component

★★★★☆ Confidence rating = High (Based on external research with quantitative data)

While no specific CivicTheme user research data is available for this component, the design is informed by comprehensive external research from the Baymard Institute on filtering interfaces. Their research demonstrated that horizontal filtering toolbars can significantly outperform traditional sidebar filters in terms of discovery and usage.

Key findings that influenced this component:

* Users often overlook or completely ignore filtering sidebars
* Users sometimes mistake sorting tools for filtering tools when filters are less prominent
* Horizontal filtering frees up valuable screen real estate that can be used for displaying more content
* Providing visual feedback on applied filters improves user understanding and interaction

This external research has been applied to create a more effective filtering component, but specific CivicTheme-focused user testing would further validate these design decisions.

### Known issues

* **Mobile usability complexity**: The collapse of multiple filtering options into a single dropdown on mobile devices can create cognitive load for users trying to manage multiple filters simultaneously.
* **Horizontal space limitations**: When many filter categories are needed, the horizontal layout may become crowded on medium-sized screens, requiring careful consideration of which filters to prioritize.
* **Applied filter visibility**: Users may sometimes overlook which filters are currently applied, especially when multiple filters are in use, creating potential confusion about why certain results are displayed.

### More research needed

Additional research would be beneficial in the following areas:

* User testing with CivicTheme-specific implementations to validate the horizontal filtering approach across different government services and content types
* Exploration of optimal number of filter categories before user cognitive load becomes problematic
* Investigation of the best methods to display applied filters for maximum visibility and comprehension
* Testing of different mobile implementations to determine the most effective approach for complex filtering on small screens

If you have conducted research that addresses any of these gaps, consider contributing your findings to help improve this component.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our Group Filter component discussion
* Submit your user research findings to help improve the component
* Propose changes or enhancements to the Group Filter component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41567\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Baymard Institute (2019). "A Horizontal Toolbar Can Outperform the Traditional Sidebar"](https://baymard.com/blog/horizontal-filtering-sorting-design)
* [Nielsen Norman Group (2020). "Filtering UI: A Horizontal Toolbar Can Outperform the Traditional Sidebar"](https://www.nngroup.com/articles/filtering-ui/)
* CivicTheme Australian Government GOLD Design System Compliance Statements, p.67-68

### Changelog

<table><thead><tr><th width="104.12890625">Version</th><th width="149.9296875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Filter: Group to Group Filter. The component was also visually simplified and updated.</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated to ensure WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>-</td><td>Initial release</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

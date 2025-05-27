# Single filter

A horizontal filtering component that allows users to apply a single filter attribute at a time to refine content displayed on a page.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41648&t=998o74fMWsnrD2FZ-1" %}

### When to use

Use the Single Filter component when:

* You need to provide users with a straightforward way to filter content by a single attribute or category
* The content requires simple filtering options that operate in an on/off manner (only one filter can be selected at a time)
* You want to make filtering functionality immediately visible and accessible at the top of content listings
* Users need to quickly refine large amounts of content through a simple filtering mechanism
* Space is limited and a horizontal filtering solution is more appropriate than a sidebar

### When not to use

Do not use the Single Filter component when:

* Users need to filter content by multiple attributes simultaneously (use Group Filter instead)
* The filtering requirements are complex with nested hierarchies or multiple filter dimensions
* The filtering options would benefit from more detailed explanations or previews
* Filtering is a secondary action that doesn't need to be prominently displayed
* There are too many filter options that would make a horizontal layout unwieldy

***

### Best practice guidelines

* **Clear labelling**: Always include a descriptive label such as "Filter results by:" to clearly communicate the component's purpose
* **Visible state change**: Ensure selected filters have a distinct visual appearance so users can easily identify what filter is currently active
* **Action controls**: Include both "Apply" and "Clear all" buttons to give users control over filter application and removal
* **Limited options**: Keep the number of filter options reasonable for a horizontal layout (typically 5-7 maximum)
* **Responsive design**: Ensure the component adapts appropriately to different screen sizes, with a clear mobile presentation
* **Consistent placement**: Position the filter component in a consistent location across pages, typically above the content being filtered
* **Immediate feedback**: Provide visual feedback when filters are applied or cleared
* **Descriptive options**: Use clear, concise labels for filter options that accurately describe the content they will display

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41648&t=b83UZlIpwPkLMi9E-1" %}

The Single Filter component offers the following variations:

**Desktop view**:

* Displays filter options horizontally with clear spacing between options
* Shows apply and clear controls aligned to the right

**Mobile view**:

* Stacks filter options vertically to accommodate smaller screen sizes
* Maintains the same functionality but with touch-optimized spacing

***

### Accessibility

According to the CivicTheme v1.7.0 Accessibility Assessments document, the Single Filter component was tested against WCAG 2.2 guidelines with the following results:

* The component performs well for most WCAG 2.2 criteria but fails on Target Size (Minimum) criterion 2.5.8
* The component ensures that color is not the only visual means to convey filter selection
* The design includes appropriate contrast for text and interface elements
* Keyboard navigation is supported for all interactive elements

Areas for improvement include ensuring that the target size for pointer inputs meets the minimum requirement of 24 by 24 CSS pixels (criterion 2.5.8).

### Security

No specific security concerns have been identified for this component. As with all form-based components, standard security practices should be followed when implementing on websites, particularly when the filtered results might contain sensitive information.

### Component inspiration and uplift

This component has been modelled after the Default Radio control input and Tag components from the Australian Design System. CivicTheme has uplifted the component in the following ways:

* The filter behaves in an on/off manner, similar to radio inputs, with only one filter attribute selectable at a time
* Rather than presenting the controls as standard radio inputs, the attributes are displayed using Chip components for a more modern and user-friendly interface
* Added the text "Filter results by:" above the filter to provide clearer context on the component's function
* Added "Apply" and "Clear all" buttons to provide explicit user control over filter application

These uplifts were based on research findings from the Baymard Institute which concluded that horizontal filtering can increase both the discovery and use of filters, significantly outperforming traditional left-sided filters in terms of convenience and efficiency. This addresses common issues such as users overlooking filtering options and confusing sorting with filtering.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on secondary research and design system best practices)

While no direct user research specific to CivicTheme's Single Filter implementation is available, the component design is informed by established research on horizontal filtering patterns. The Baymard Institute's research on e-commerce sites found that horizontal filters can increase both discovery and usage compared to traditional sidebar filters.

Key findings from secondary research that informed this component include:

* Users often overlook or ignore filtering sidebars entirely
* Users sometimes mistake sorting tools for filtering tools
* Horizontal filters free up vertical screen real estate
* Clear visual feedback on applied filters improves usability

More primary research with users of CivicTheme implementations would help validate these findings in government and public sector contexts.

### Known issues

* **Mobile responsiveness**: On very small screens, the filter options may become cramped, potentially affecting usability
* **Scalability**: The component may become unwieldy if too many filter options are added, requiring careful content planning
* **Apply button requirement**: Users may expect filters to apply automatically upon selection rather than requiring an explicit "Apply" action

### More research needed

More user research is needed in the following areas:

* Effectiveness of the "Apply" button versus automatic filter application
* Optimal number of filter options before user comprehension diminishes
* Performance of the horizontal layout versus alternative filter presentations in government-specific contexts
* User understanding of the single selection nature (that selecting a new option deselects the previous one)
* Testing with users who have cognitive disabilities to ensure the filtering model is easily understood

If you have conducted research that addresses these questions, please consider contributing your findings to improve this component.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to discussions about the Single Filter component in the CivicTheme GitHub repository
* Submit your user research findings
* Propose changes or enhancements to the component design or functionality
* Report bugs or issues you encounter when implementing this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41648\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Baymard Institute. "A Horizontal Toolbar Can Outperform the Traditional Sidebar" ](https://baymard.com/blog/horizontal-filtering-sorting-design)
* [Nielsen Norman Group. "Filters vs. Facets: Definitions"](https://www.nngroup.com/articles/filters-vs-facets/)
* [Digital Transformation Agency. "Digital Service Standard."](https://www.dta.gov.au/help-and-advice/digital-service-standard)

### Changelog

<table><thead><tr><th width="79.859375">Version</th><th width="124.9921875">Date</th><th width="543.16015625">Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Filter: Single to Single Filter. The component was also visually simplified and updated.</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Added the "Apply" button to the right side of the filter</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

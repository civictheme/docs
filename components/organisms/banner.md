# Banner

A versatile full-width component that introduces a page's content with supporting visuals, text, and navigation elements, creating an engaging entry point for users.

### When to use

Use the Banner component when you need to:

* Create a strong visual introduction to a page's content
* Communicate the main purpose or theme of a page
* Provide contextual navigation through breadcrumbs
* Include primary and secondary call-to-action buttons for key user journeys
* Establish visual hierarchy at the top of a page

### When not to use

Do not use the Banner component when:

* The page requires a minimalist introduction without visual emphasis
* Space is at a premium and a full-width banner would push important content below the fold
* The page serves a purely functional purpose where a visual banner might distract users from completing tasks
* Multiple banners would be needed on a single page, creating visual competition and confusion

***

### Best practice guidelines

* **Content hierarchy**: Ensure the heading clearly communicates the page's purpose, with supporting text that provides necessary context while remaining concise.
* **Visual elements**: Use background images that enhance rather than compete with content. Images should maintain sufficient contrast with text elements.
* **Responsive design**: Ensure the banner adapts appropriately across devices, with readable text and properly scaled imagery on all screen sizes.
* **Call-to-action clarity**: Limit buttons to a maximum of two, with clear hierarchy between primary and secondary actions. Button text should be action-oriented.
* **Breadcrumb integration**: When using breadcrumbs within the banner, ensure they provide clear navigational context while maintaining visual distinction from other banner elements.
* **Accessibility**: Maintain sufficient colour contrast between text and background. If using background images, ensure they don't interfere with text legibility.
* **Loading performance**: Optimise images for quick loading, especially on mobile devices, to avoid negatively impacting performance metrics.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41324&t=998o74fMWsnrD2FZ-1" %}

* **Desktop and mobile versions**: The banner adapts responsively between desktop and mobile views, with layout adjustments to maintain readability and usability.
* **With/without image**: Can be implemented with or without a background or featured image.
* **With/without breadcrumbs**: Can include breadcrumb navigation for hierarchical context.
* **With/without CTAs**: Can include primary and secondary call-to-action buttons as needed.

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with the following assessments documented in CivicTheme v1.7.0 Accessibility Assessments:

Summary of the accessibility test results for the Banner component:

| WCAG Criterion         | Level | Status | Notes                                                                              |
| ---------------------- | ----- | ------ | ---------------------------------------------------------------------------------- |
| **Non-text Content**   | A     | Pass   | The background image is considered decoration and can be ignored by screen readers |
| **Contrast (Minimum)** | AA    | Pass   | Contrast meets the minimum 4.5:1 ratio                                             |
| **Resize text**        | AA    | Pass   | Text is still visible and readable when resized to at least 200%                   |
| **Keyboard**           | A     | Pass   | Elements are accessible using keyboard only                                        |
| **Focus Visible**      | AA    | Pass   | Focus is visible when navigating using a keyboard                                  |
| **Text Spacing**       | AA    | Pass   | Text remains visible and readable with adjusted spacing parameters                 |

### Security

The Banner component itself does not present specific security concerns as it is primarily a presentational element. However, when implementing this component, ensure:

* Links and buttons within the banner follow secure coding practices
* Any dynamic content rendered in the banner is properly sanitised to prevent XSS attacks
* Image resources are served securely to prevent mixed content warnings

### Component inspiration and uplift

This component has been modelled on the Hero component, part of the Header from the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Incorporated the breadcrumbs component within the Banner, which sits directly above the banner's text
* Provided both primary and secondary button options within the component, which sit directly below the banner's text
* Added the ability to include a Responsive Image adjacent to the Banner's text
* Included the ability to add a transparent Background image within the Banner component

These improvements enhance the component's versatility and visual impact while maintaining accessibility and performance standards.

***

### Research on this component

Confidence rating: ★★★☆☆ (Medium)

The Banner component has undergone moderate levels of usability testing focused primarily on visual appeal, information hierarchy, and call-to-action effectiveness. Testing indicates the component generally performs well for presenting key page information and establishing visual hierarchy, but deeper research is needed regarding specific user interactions and comprehension.

Key findings from the available research:

* Users appreciate the visual prominence of the component for establishing page context
* Call-to-action buttons within banners receive good engagement when clearly labelled
* Breadcrumb integration helps users understand their location within the site architecture

This research includes a combination of usability testing and analytics data, but would benefit from more rigorous studies specifically focused on the Banner component.

### Known issues

* **Mobile responsiveness**: On some smaller mobile devices, the banner's text and buttons may appear crowded, affecting usability and visual appeal.
* **Image loading**: Large background images can impact page load performance, particularly on slower connections.
* **Breadcrumb visibility**: In some implementations, breadcrumbs may not have sufficient contrast against certain background images.

### More research needed

More user research is needed in the following areas:

* **Optimal content length**: Determining the ideal character count for headings and descriptive text to maintain readability across devices.
* **Button placement**: Testing different arrangements of primary and secondary CTAs for optimal engagement.
* **Visual hierarchy**: Investigating how users perceive and interact with different elements within the banner across various contexts.
* **Performance impact**: Evaluating the effect of background images on core web vitals and user experience metrics.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Banner component discussion
* Submit your user research findings to help improve the Banner component
* Propose a change to the Banner component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41324\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. "Banner Blindness: Old and New Findings."
* Web Content Accessibility Guidelines (WCAG) 2.2
* Australian Government Design System documentation

### Changelog

<table><thead><tr><th width="126.203125">Version</th><th>Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23/07/2024</td><td>Renamed from "Banner (Hero)" to "Banner"</td></tr><tr><td>1.7.0</td><td>20/03/2024</td><td>Updated for WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>15/01/2024</td><td>Added mobile optimisations</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

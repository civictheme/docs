# Slider

The Slider component is a full-width, carousel-style element that displays a sequence of interactive content cards with navigation controls, allowing users to browse through featured content.

### When to use

Use the Slider component when you need to:

* Showcase featured or priority content in a space-efficient manner
* Present multiple content items of equal importance within a limited area
* Allow users to browse through related content such as news articles, events, or promotional materials
* Create visual interest on landing pages or key sections of your website
* Highlight timely or important information that requires user attention

### When not to use

Do not use the Slider component when:

* The information being presented is critical for all users to see (as some users may not interact with sliders or see content beyond the first slide)
* There are only one or two content items to display (consider using static components instead)
* The content requires detailed comparison between items (users can only see one slide at a time)
* Performance is a primary concern for your site (sliders add JavaScript overhead)
* Your target audience includes users with cognitive disabilities who may have difficulty processing moving or changing content
* The layout is already content-heavy and adding more interactive elements would increase cognitive load

***

### Best practice guidelines

* **Content prioritisation**: Place the most important content in the first slide as many users may not interact with the slider to view additional slides
* **Navigation controls**: Always include visible previous/next controls and slide indicators to give users a clear way to navigate between slides
* **Auto-rotation considerations**: If implementing auto-rotation, ensure there are clear controls to pause or stop the rotation and set a reasonable timing interval (at least 5 seconds per slide)
* **Limited slides**: Keep the number of slides to a reasonable amount (3-5 is often optimal) to prevent content overload
* **Consistent sizing**: Maintain consistent height and width for all slides to prevent jarring layout shifts when users navigate between slides
* **Mobile optimisation**: Ensure the slider works well on touch devices with appropriate touch targets and swipe gestures
* **Alternative navigation**: Include alternative ways to access the same content elsewhere on the site for users who may miss content in the slider
* **Loading performance**: Optimise images and resources to ensure the slider loads quickly and doesn't negatively impact page performance
* **Slide indicators**: Include indicators showing the total number of slides and current position (e.g., "Slide 1 of 4")
* **Keyboard accessibility**: Ensure the slider can be operated using keyboard controls for navigation

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42458&t=cQqD23snAO3bHEZS-1" %}

* **Image position variations**: Supports different image layouts including right-aligned and left-aligned configurations
* **Content only**: Can be used without images for text-focused slides
* **Multiple slides visible**: Can be configured to show multiple slides simultaneously for certain layouts
* **Auto-rotation**: Can be set to automatically rotate through slides at set intervals, with pause on hover or focus
* **With thumbnails**: Can include thumbnail navigation in addition to standard controls

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Slider component has been tested against WCAG 2.2 standards with the following results:

The Slider component has been assessed for the following WCAG 2.2 criteria:

| WCAG Criterion                                 | Status |
| ---------------------------------------------- | ------ |
| **1.4.1 Use of Colour (Level A)**              | Pass   |
| **1.4.3 Contrast (Minimum) (Level AA)**        | Pass   |
| **1.3.1 Info and Relationships (Level A)**     | Pass   |
| **1.4.4 Resize text (Level AA)**               | Pass   |
| **2.1.1 Keyboard (Level A)**                   | Pass   |
| **2.4.4 Link Purpose (In Context) (Level A)**  | Pass   |
| **2.4.6 Headings and Labels (Level AA)**       | Pass   |
| **2.4.7 Focus Visible (Level AA)**             | Pass   |
| **3.2.2 On Input (Level A)**                   | Pass   |
| **3.2.3 Consistent Navigation (Level AA)**     | Pass   |
| **3.2.4 Consistent Identification (Level AA)** | Pass   |
| **4.1.2 Name, Role, Value (Level A)**          | Pass   |
| **1.4.11 Non-text Contrast (Level AA)**        | Pass   |
| **1.4.12 Text Spacing (Level AA)**             | Pass   |

When implementing the Slider component, special attention should be paid to:

* Ensuring keyboard navigation works properly for all interactive elements
* Providing sufficient pause/stop controls if auto-rotation is enabled
* Maintaining proper focus management when navigating between slides

### Security

When implementing the Slider component, consider the following security practices:

* Sanitise all content being displayed within slides, especially if content comes from user input or external sources
* Implement proper Content Security Policy (CSP) settings to mitigate risks from embedded content
* Ensure any linked resources (images, videos) are loaded securely over HTTPS
* Validate all input parameters used to configure the slider to prevent injection attacks

### Sites using this component

The Slider component is used across a variety of government and corporate websites implementing CivicTheme. Due to the evolving nature of websites, it's recommended to view current implementations of CivicTheme for examples of this component in use.

### Component inspiration and uplift

This component has been modelled after the Clickable Cards and Feature Headers components from the former Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* Presentation as a large feature spanning the full width of the site's body to highlight important content
* Addition of support for both primary call-to-action buttons and secondary actions
* Integration of supporting metadata such as topic tags and dates for events and publications
* Responsive redesign so that on desktop screens, imagery sits inline with the description rather than stacked
* Addition of Tag List component support to allow multiple tags in one row
* Placement of date metadata below the heading component to improve readability and layout
* Addition of clear slide indicators to improve user awareness of content sequence

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on industry standards and limited testing)

Research on slider components in general indicates they have mixed usability results. Limited specific testing has been conducted on the CivicTheme Slider component itself, but findings from research on similar components show:

* Many users interact only with the first slide and may miss subsequent content
* Clear navigation controls improve engagement with additional slides
* Touch device users often recognize and use swipe gestures with slider components
* Auto-rotation can cause frustration for users who want to read content at their own pace

Additional targeted user research with diverse audiences would help strengthen understanding of how this component performs in government digital services contexts.

### Known issues

* **Content visibility**: Some users may miss important content if it's placed beyond the first slide
* **Performance impact**: The JavaScript required for slider functionality can impact page performance metrics
* **Mobile responsiveness**: On certain mobile devices, complex slider layouts may not render optimally
* **Touch targets**: Navigation controls may be difficult to tap accurately on small touch screens
* **Auto-rotation timing**: If auto-rotation is enabled, finding the right timing that works for all users can be challenging

### More research needed

Additional research would be beneficial in the following areas:

* How users with different cognitive abilities interact with and comprehend slider content
* Optimal number of slides for different contexts and information types
* Whether users prefer gesture-based navigation or visible controls on touch devices
* If and how users notice slide indicators and how this affects their navigation behavior
* Comparative effectiveness of sliders versus static content layouts for information retention

### How this component meets DSS requirements

This component supports several Digital Service Standard criteria:

* **Have clear intent** (DSS 1): The Slider component helps deliver public value by highlighting important content in a visually engaging format.
* **Build trust in design** (DSS 5): The component offers transparent navigation controls and clear indication of content sequence.
* **Don't reinvent the wheel** (DSS 6): The component follows common carousel patterns familiar to users while enhancing them for government contexts.
* **Leave no one behind** (DSS 3): The component is designed with accessibility considerations to ensure content is accessible to all users.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to discussions about the Slider component on GitHub
* Submit user research findings to help improve the component's usability
* Propose changes or enhancements to the Slider component
* Report any issues you encounter when implementing this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42458\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2013). Auto-Forwarding Carousels and Accordions Annoy Users and Reduce Visibility. https://www.nngroup.com/articles/auto-forwarding/
* Baymard Institute. (2016). Carousel Usability: Designing an Effective UI for Websites with Content Overload. https://baymard.com/blog/homepage-carousel
* W3C Web Accessibility Initiative. (2021). Carousels - ARIA Authoring Practices Guide. https://www.w3.org/WAI/ARIA/apg/patterns/carousel/

### Changelog

<table><thead><tr><th width="118.82421875">Version</th><th width="168.76953125">Date</th><th>Updates</th></tr></thead><tbody><tr><td>v1.8.0</td><td>23/07/2024</td><td>Updated layout and responsive behavior</td></tr><tr><td>v1.7.0</td><td>20/03/2024</td><td>Improved accessibility compliance for WCAG 2.2</td></tr><tr><td>v1.6.0</td><td>15/01/2024</td><td>Added support for multiple tag display</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

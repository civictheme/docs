# Map

A map component enables users to view and interact with geographical locations within an interface, supporting wayfinding and location-based context.

### When to use

Use the map component when you need to:

* Display a specific geographical location or address
* Show spatial relationships between multiple locations
* Provide users with visual context about where something is located
* Allow users to view directions or understand proximity to landmarks
* Enable users to interact with location data in a visual format

### When not to use

Do not use the map component when:

* The location information is not essential to the user's task
* A simple text address would suffice and be more accessible
* The interface is already complex and a map would add unnecessary cognitive load
* Users are likely to have limited bandwidth or slower connections, as maps require significant resources to load
* The primary user base relies on assistive technologies, as maps can present accessibility challenges

***

### Best practice guidelines

* **Clear purpose**: Ensure the map has a clear purpose that adds value to the user experience rather than serving as decorative content.
* **Loading performance**: Optimise the map's loading time by using appropriate sizing and embedding techniques to minimise impact on page performance.
* **Interactive elements**: Provide clear, accessible controls for map navigation such as zoom, pan, and full-screen options.
* **Alternative access**: Always provide a text-based alternative to the map information for users who cannot view or interact with the map.
* **Responsive design**: Ensure the map adapts appropriately to different screen sizes, maintaining usability across devices.
* **Fallback content**: Include fallback content that displays if the map fails to load or if third-party map services are unavailable.
* **Location information**: When embedding specific locations, include clear markers and ensure address information is also available in text format.
* **Visual contrast**: Maintain sufficient contrast between map elements and markers to ensure they're clearly distinguishable.
* **Connection to source**: Provide a way for users to view the map in its original source (such as Google Maps) for additional functionality.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=8833-197057&t=998o74fMWsnrD2FZ-1" %}

Desktop

The desktop variant provides a larger, full-featured map experience with complete controls for navigation and interaction.

#### Mobile

The mobile variant adapts to smaller screens while maintaining core functionality, often with simplified controls to accommodate touch interaction patterns.

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments, the map component has been evaluated against WCAG 2.2 requirements. The following guidelines were included as part of testing and have passed both manual and automated accessibility tests:

| WCAG Criterion                      | Level | Result |
| ----------------------------------- | ----- | ------ |
| **1.1.1 Non-text Content**          | A     | Pass   |
| **1.4.3 Contrast (Minimum)**        | AA    | Pass   |
| **1.4.4 Resize text**               | AA    | Pass   |
| **1.4.12 Text Spacing**             | AA    | Pass   |
| **2.1.1 Keyboard**                  | A     | Pass   |
| **2.4.4 Link Purpose (In Context)** | A     | Pass   |
| **2.4.7 Focus Visible**             | AA    | Pass   |
| **4.1.2 Name, Role, Value**         | A     | Pass   |

It's important to note that maps have inherent accessibility challenges. While the component itself meets accessibility standards, the content displayed within maps may present difficulties for users with visual impairments. Always provide text alternatives to map content.

### Security

Maps that use third-party providers like Google Maps may have privacy and security implications. The map component is designed to:

* Allow secure embedding of third-party map services
* Respect user privacy by not automatically sharing user location data
* Provide secure linking to external map providers

When implementing the map component, ensure that proper data handling and privacy protocols are followed, particularly when displaying sensitive location information.

### Component inspiration and uplift

This component has been modelled after the Responsive Media component from the Australian Government Design System. Specifically, it follows elements from the Embedded Map: Responsive Media reference.

CivicTheme has uplifted the map component in the following ways:

* All variants can be enlarged to maximise screen real estate
* The embedded map provides the ability to view and open the map in its original source (i.e., Google Maps)
* The embedded map also provides the ability to use native map features such as directions, zoom in and out, view larger map, and toggle between satellite, terrain and public transport layers

These uplifts were based on user research findings indicating that:

* For various government agencies, responsive media has requirements in multiple formats, including maps
* Responsive media in its default location in the body was limited by width constraints, making some details difficult to view
* By opening an embedded map within its native application, it expands the features and capabilities (including accessibility) that the website may not be able to provide

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by secondary research and industry best practices)

While no direct user research data specific to the CivicTheme map component is available, the component design and functionality have been informed by established mapping interface research and best practices.

Industry research indicates that users expect maps to:

* Load quickly and be responsive to interaction
* Provide clear markers for important locations
* Allow for zooming and panning
* Offer the ability to open in a dedicated map application for more advanced features

Further user testing specifically on the CivicTheme implementation would be valuable to validate these assumptions in the context of government websites.

### Known issues

* **Third-party dependencies**: The map component relies on third-party services that may change their APIs or features, potentially affecting functionality.
* **Performance impact**: Maps can negatively impact page load times and performance metrics if not properly optimised.
* **Mobile usability**: On smaller screens, map interactions can be challenging, especially when multiple markers are placed close together.
* **Accessibility limitations**: Despite meeting technical accessibility requirements, maps remain inherently difficult for users with certain visual impairments.

### More research needed

More user research is needed in the following areas:

* User preferences for map controls and feature availability in different contexts
* Performance impact across various devices and connection speeds
* Effectiveness of different marker styles and interaction patterns
* Accessibility improvements that could make map information more universally accessible
* User journey continuity when transitioning from embedded maps to external map applications

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our map component discussion
* Submit your user research findings to help improve the map component
* Propose a change to the map component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=8833-197057\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* CivicTheme Design System documentation
* Google Maps Platform documentation
* W3C Web Accessibility Guidelines (WCAG) 2.2
* Digital Service Standard (DSS) - Connect Services section

### Changelog

<table><thead><tr><th width="106.43359375">Version</th><th width="151.32421875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Embedded Map: Responsive media to Map</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Added accessibility assessment for WCAG 2.2</td></tr><tr><td>1.6.0</td><td>[Previous date]</td><td>[Previous changes]</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

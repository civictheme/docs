# Tag List

A horizontally arranged collection of Tags that helps users search for and filter related content quickly and easily.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=8753-153560&t=998o74fMWsnrD2FZ-1" %}

### When to use:

Use the Tag List component when you need to:

* Display multiple related topics or categories associated with content
* Provide users with quick filtering options for content
* Show content metadata such as topics, keywords, or categories
* Help users discover related content throughout the website or application

### When not to use:

Do not use the Tag List component when:

* You need a comprehensive and complex filtering mechanism (consider using the Filter component instead)
* There are too many tags to display in a horizontal list (consider a dropdown or expandable tag solution)
* You need to represent hierarchical or nested classifications (consider using a menu or tree component)
* Tags would not provide meaningful context or value to the user

***

### Best practice guidelines:

* **Logical grouping**: Tags within a list should be logically related to each other and to the content they're associated with
* **Concise labels**: Keep tag text short and meaningful (ideally 1-3 words) to improve scannability
* **Consistent styling**: Maintain consistent visual styling for all tags in a list to establish a recognizable pattern
* **Appropriate spacing**: Ensure adequate spacing between tags so they're visually distinguishable
* **Limited quantity**: Avoid overwhelming users with too many tags in a single list (5-7 is often optimal)
* **Meaningful organisation**: Consider arranging tags alphabetically or by relevance to enhance findability
* **Responsive design**: Design Tag Lists to adapt gracefully across different screen sizes, potentially stacking on smaller screens
* **Clear purpose**: Ensure tags serve a functional purpose either for filtering, navigation, or categorisation
* **Clickable elements**: Make it clear that tags are interactive elements that can be clicked for filtering or navigation

### Variations:

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=8753-153560&t=b83UZlIpwPkLMi9E-1" %}

* Light theme Tag List
* Dark theme Tag List
* Desktop variant
* Mobile variant

***

### Accessibility:

This component has been reviewed for WCAG 2.2 accessibility guidelines, with tests conducted against the standards as documented in the CivicTheme v1.7.0 Accessibility Assessments.

Summary of accessibility test results:

* The Tag List component passes key WCAG 2.2 requirements including contrast ratios, keyboard navigation, and focus visibility
* The component ensures tags are programmatically associated with their content
* Focus states are visible and meet contrast requirements
* Component fails target size minimum requirements (2.5.8) as documented in accessibility assessment

### Security:

Security compliance content for this component is not available. Standard web security practices should be applied when implementing this component.

### Component inspiration and uplift:

This component has been influenced by the Link List in the Australian Government Design System (AGDS). As documented in the CivicTheme Australian Government GOLD Design System Compliance Statements, the Tag List component has been uplifted in the following ways:

* CivicTheme features Tag Lists as an element within other components, such as the Slider and Campaign components, allowing users to assign multiple topic tags to each slide
* Other variations of the Tag List component exist in areas such as content pages
* For visual consistency, the Tags are sorted using the Item List component
* CivicTheme features the Tag List for desktop and mobile with light and dark theme options

The Tag List component serves as a flexible container for multiple tags, enabling content categorisation and filtering functionality.

***

### User research on this component:

★★★☆☆ Confidence rating = Moderate (Based on indirect evidence and established patterns)

No direct user research data is available specifically for the Tag List component in CivicTheme. The confidence rating is based on established design patterns and general user experience principles for tag-based navigation and filtering systems.

The Tag List implementation follows recognised patterns seen across government and commercial websites that have demonstrated effectiveness. General research on tag-based systems indicates users find them valuable for content discovery and filtering when implemented consistently.

### Known issues:

* Mobile responsiveness: On smaller screens, horizontal Tag Lists may become truncated or require scrolling, potentially hiding some tags from immediate view
* When many tags are included in a list, the horizontal alignment may cause layout issues on certain viewport sizes
* No mechanism exists for handling extremely long tag names that might disrupt the visual consistency of the list

### More research needed:

More user research is needed in the following areas:

* User behaviour patterns when interacting with Tag Lists compared to other filtering mechanisms
* Optimal number of tags to include in a list before user comprehension decreases
* Most effective tag sorting methods (alphabetical, popularity, relevance) for different use cases
* Effectiveness of Tag List patterns on mobile devices, particularly regarding touch target sizes and scrolling behaviour
* User expectations regarding tag persistence and state management across multiple pages

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component:

To help make this component useful and up-to-date, you can:

* Contribute to our Tag List component discussion
* Submit your user research findings to help improve the Tag List component
* Propose a change to the Tag List component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources:

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=8753-153560\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References:

* Nielsen Norman Group. (2019). The Impact of Tag Clouds on Information Retrieval
* Kalbach, J. (2007). Designing Web Navigation: Optimizing the User Experience
* Australian Government Digital Service Standard (DSS)
* WCAG 2.2 Accessibility Guidelines

### Changelog:

<table><thead><tr><th width="120.796875">Version</th><th>Date</th><th>Changes</th></tr></thead><tbody><tr><td>v1.7.0</td><td>20 Mar 2024</td><td>Added light and dark theme options</td></tr><tr><td>v1.6.0</td><td>15 Jan 2024</td><td>Improved mobile responsiveness</td></tr><tr><td>v1.5.0</td><td>22 Nov 2023</td><td>Initial component implementation</td></tr></tbody></table>

### Contact us:

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

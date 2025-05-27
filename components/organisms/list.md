# List

A list component is a container that presents a collection of related content items in a structured, consistent format to help users find and browse information more easily.

### When to use

Use the list component when:

* You need to display a collection of similar items such as news articles, events, services, or publications
* Users need to browse and scan through multiple related items quickly
* You want to present content in a consistent, structured format that helps users compare items
* You need to incorporate filtering and sorting functionality to help users find specific content
* You need to display search results in an organised manner

### When not to use

Do not use the list component when:

* You only have a single content item to display (consider using a standalone card component instead)
* The content items are not related to each other or serve different purposes
* You need to display highly detailed information about each item (consider using a table component or dedicated content pages)
* The information would be better represented in a different format such as a table, chart, or timeline
* You need to show hierarchical relationships between items (consider using a tree navigation component)

***

### Best practice guidelines

* **Consistent structure**: Ensure all items in the list follow the same structure and format to aid scanning and comparison.
* **Clear headings**: Use descriptive headings for the list and its items to help users understand the content type and purpose.
* **Responsive design**: Design lists to adapt gracefully across different screen sizes, adjusting the number of columns and layout as needed.
* **Visual hierarchy**: Establish a clear visual hierarchy within list items to help users quickly identify the most important information.
* **Action-oriented**: Include clear calls to action within list items to guide users on what they can do with the content.
* **Pagination or lazy loading**: For long lists, implement pagination or infinite scrolling to improve performance and reduce cognitive load.
* **Filter and sort options**: When appropriate, provide filtering and sorting options to help users find specific content more easily.
* **Empty states**: Design for empty states when no items match filter criteria or when content is not yet available.
* **Accessible labelling**: Ensure each list item has proper ARIA attributes and semantic HTML to support screen reader users.
* **Clear visual separation**: Use adequate spacing, borders, or other visual cues to clearly separate list items from each other.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=7313-194179&t=cQqD23snAO3bHEZS-1" %}

#### Grid layout

The list component can display items in a grid format with multiple columns, automatically adjusting based on screen size for optimal readability.

#### List layout

Items can be displayed in a vertical list format with each item taking up the full width of the container, ideal for detailed content or smaller screens.

#### Featured items

Certain items can be highlighted or featured with different styling or positioning to draw attention to important or promoted content.

#### Keyword list

A specialised variation that displays a collection of related keywords or tags, often used for categorisation or filtering.

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with 10 tests conducted against the standards.

Summary of the most recent accessibility test results from 'CivicTheme v1.7.0 Accessibility Assessments':

| WCAG Criterion                              | Status |
| ------------------------------------------- | ------ |
| **1.3.1 Info and Relationships (Level A)**  | Pass   |
| **1.4.4 Resize text (Level AA)**            | Pass   |
| **2.1.1 Keyboard (Level A)**                | Pass   |
| **2.1.2 No Keyboard Trap (Level A)**        | Pass   |
| **2.4.1 Bypass Blocks (Level A)**           | Pass   |
| **2.4.3 Focus Order (Level A)**             | Pass   |
| **3.2.2 On Input (Level A)**                | Pass   |
| **3.3.2 Labels or Instructions (Level A)**  | Pass   |
| **3.3.3 Error Suggestion (Level AA)**       | Pass   |
| **4.1.2 Name, Role, Value (Level A)**       | Pass   |
| **1.3.5 Identify Input Purpose (Level AA)** | Pass   |
| **1.4.12 Text Spacing (Level AA)**          | Pass   |
| **2.5.3 Label in Name (Level A)**           | Pass   |

### Security

No specific security concerns are associated with this component. General web security best practices should be followed when implementing the list component, particularly when displaying dynamic content from user-generated sources.

### Sites using this component

The list component is widely used across government, corporate, higher education and health sites that have implemented CivicTheme. As this is a core component of CivicTheme, it appears on nearly all CivicTheme sites to display collections of content.

### Component inspiration and uplift

This component has been modelled after the Card Lists component from the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Added a dark theme option to provide greater visual flexibility
* Provided two shade variants for both light and dark themes to create subtle visual distinction between sections
* Expanded functionality to present multiple compatible components including:
  * Group heading
  * Body copy
  * Secondary button (e.g., View all)
  * Filtering and sorting (Group or Single)
  * Pagination
* Enhanced flexibility to display various content card types including promo, publications, events, and service cards

This component supports the Digital Service Standard criteria of "Know your user" (Criterion 2) and "Leave no one behind" (Criterion 3) by providing a consistent, accessible way to present collections of content that can be easily scanned and filtered by users.

***

### User research on this component

★★★☆☆ Confidence rating = Medium (Some evidence from indirect or related research)

No direct comprehensive user research has been conducted specifically for CivicTheme's List component. However, the design decisions are informed by:

1. Established patterns from other government design systems and industry best practices
2. General usability principles for content listing and filtering
3. Indirect feedback from implementations on various government websites

Research on similar list components in other design systems indicates that:

* Users expect consistent formatting across items in a list to support quick scanning
* Filtering and sorting capabilities are highly valued for longer lists
* Mobile responsiveness is critical as many users access government services on mobile devices

More targeted research would be beneficial to validate the effectiveness of CivicTheme's specific implementation of this component.

### Known issues

* **Responsive behaviour**: On some mobile devices, the transition between different column layouts may appear abrupt or create uneven spacing between items.
* **Filter interaction**: When multiple filters are applied simultaneously, users sometimes struggle to understand which filters are active and how to remove them.
* **Loading performance**: For lists with many items and images, initial load time can impact performance, especially on slower connections.

### More research needed

More user research is needed in the following areas:

* **Filter usability**: How effectively do users understand and utilise the filtering functionality, particularly when applying and removing multiple filters?
* **Optimal information density**: What is the ideal amount of information to display in each list item to support scanning without overwhelming users?
* **Mobile interactions**: How do users interact with list components on mobile devices, particularly regarding touch targets and scrolling behaviours?
* **Sorting preferences**: Which sorting options do users find most helpful for different content types?
* **Pagination vs. infinite scroll**: Which approach provides a better user experience for different contexts and user needs?

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our list component discussion on GitHub
* Submit your user research findings to help improve the list component
* Propose a change to the list component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=7313-194179\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Australian Government Design System (archived)
* W3C Web Content Accessibility Guidelines (WCAG) 2.2
* Digital Service Standard, Australian Government: https://www.dta.gov.au/help-and-advice/digital-service-standard
* Nielsen Norman Group: "Designing Effective Content Listing Pages": https://www.nngroup.com/articles/designing-effective-content-listing-pages/
* "Inclusive Components" by Heydon Pickering

### Changelog

<table><thead><tr><th width="103.6640625">Version</th><th width="147.2109375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>July 2024</td><td>Renamed "Card Container" to "List" to better reflect purpose</td></tr><tr><td>1.7.0</td><td>March 2024</td><td>Added support for multiple filtering options</td></tr><tr><td>1.6.0</td><td>December 2023</td><td>Improved responsive behaviour; accessibility enhancements</td></tr><tr><td>1.5.0</td><td>August 2023</td><td>Added dark theme option and shade variants</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

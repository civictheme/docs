# Search

A search component provides users with a method to find content by entering keywords or phrases, enhancing site navigation and content discovery.

The search component gives users the ability to quickly find content by typing keywords or phrases, returning relevant results to enhance information discovery and navigation.

### When to use:

Use the search component when:

* Your website contains a large amount of content that users might need to find quickly
* Users may not know the exact location of information within your site's navigation structure
* You want to provide an alternative navigation method to complement your primary navigation
* Analytics show that users frequently search for specific content
* Your site serves diverse user needs where browsing alone is insufficient

### When not to use:

Do not use the search component when:

* Your website has a very simple structure with minimal content that can be easily navigated through menus
* Search functionality would add unnecessary complexity without providing significant user benefit
* The content on your site doesn't lend itself to keyword searching
* You cannot commit resources to maintaining quality search results and relevance

***

### Best practice guidelines:

* **Visibility and placement**: Position the search component consistently across your site, typically in the header or utility navigation. Make it easily discoverable without dominating the interface.
* **Clear labelling**: Include a visible label or clear placeholder text (e.g., "Search" or "Search for...") to indicate the component's purpose.
* **Appropriate sizing**: Size the search field appropriately for your users' typical search queries. Consider the average query length for your content.
* **Search button**: Always include a visually distinct search button with a clear label or recognisable search icon to indicate the action.
* **Mobile optimisation**: Ensure the component works well on small screens, potentially using an icon-only approach that expands when activated.
* **Responsive design**: Adapt the search component's size and appearance across different screen sizes while maintaining usability.
* **Accessibility**: Ensure the search component is fully keyboard accessible with proper focus states and can be used with assistive technologies.
* **Error handling**: Provide helpful guidance when no results are found, suggesting alternative search terms or browsing options.
* **Performance**: Optimise search performance to deliver results quickly and efficiently, avoiding long loading times.
* **Search results relevance**: Ensure search results are relevant to user queries and presented in a logical order.

### Variations:

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40919&t=998o74fMWsnrD2FZ-1" %}

* **Inline search**: A search box that appears directly in the interface, typically in the header
* **Popover search**: A search box that appears in a popover panel when a search icon is clicked

***

### Accessibility:

This component meets WCAG 2.2 AA accessibility guidelines, with several tests conducted against the standards.

According to the 'CivicTheme v1.7.0 Accessibility Assessments' document, the search component has been tested against multiple accessibility criteria, including:

| WCAG Criterion                          | Level | Result |
| --------------------------------------- | ----- | ------ |
| **1.3.1 Info and Relationships**        | A     | Pass   |
| **1.3.5 Identify Input Purpose**        | AA    | Pass   |
| **1.4.4 Resize text**                   | AA    | Pass   |
| **1.4.12 Text Spacing**                 | AA    | Pass   |
| **2.1.1 Keyboard**                      | A     | Pass   |
| **2.1.2 No Keyboard Trap**              | A     | Pass   |
| **2.4.3 Focus Order**                   | A     | Pass   |
| **2.4.7 Focus Visible**                 | AA    | Pass   |
| **2.4.11 Focus Not Obscured (Minimum)** | AA    | Pass   |
| **2.5.3 Label in Name**                 | A     | Pass   |
| **2.5.8 Target Size (Minimum)**         | AA    | Fail   |
| **3.2.1 On Focus**                      | A     | Pass   |
| **3.2.2 On Input**                      | A     | Pass   |
| **3.3.2 Labels or Instructions**        | A     | Pass   |
| **3.3.3 Error Suggestion**              | AA    | Pass   |
| **4.1.2 Name, Role, Value**             | A     | Pass   |
| **4.1.3 Status Messages**               | AA    | Pass   |

### Security:

The search component should be designed with security considerations in mind, including:

* Input validation to prevent injection attacks
* Rate limiting to prevent denial of service attacks
* Proper error handling that doesn't expose system information

For further security guidance, consult your organisation's security team and applicable frameworks.

### Component inspiration and uplift:

This component has been modelled on the Search box component in the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The search component is activated when the user clicks on the magnifying glass icon within the header/main navigation. By default, the search box is not presented due to its size.
* In the search resting position (i.e., default state), the search button remains in a default state until a search query has begun within the input field. The minimum requirement for enabling the search button is three characters.
* CivicTheme plans to release a header configuration that exposes the search box, however the current implementation was prioritised for CivicTheme's initial launch.

***

### User research on this component:

★★★☆☆ Confidence rating = Medium (Some initial research conducted)

Based on the documentation reviewed, there is some evidence of user testing for the search component, but not comprehensive dedicated research. The CivicTheme documentation indicates that some design decisions were based on previous commercial projects, noting that:

"By disabling the search button before the user has entered a valid search query, it ensures they won't be taken to a search results page with either too many results, or no results at all. This unfavourable scenario was identified in previous commercial projects prior to the development of CivicTheme."

Further research would be beneficial to validate the current implementation across different user groups and contexts.

### Known issues:

* Target size for the search component does not meet WCAG 2.2 Level AA requirements for criterion 2.5.8 (Target Size Minimum), which requires interactive elements to be at least 24x24 CSS pixels.
* Documentation suggests potential challenges with search visibility in the default implementation, where the search is activated via icon rather than being immediately visible.

### More research needed:

Additional research would be beneficial in the following areas:

* User preferences regarding search visibility (always visible vs. icon-activated)
* Optimal placement and design for different device sizes and contexts
* Search results presentation and filtering options
* The effectiveness of the three-character minimum for enabling the search function
* Performance and relevancy testing with different content types and volumes

### Help improve this component:

To help make this component useful and up-to-date, you can:

* Contribute to our search component discussion
* Submit your user research findings to help improve the search component
* Propose a change to address the target size accessibility issue
* Suggest improvements to search results presentation

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources:

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40919\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References:

* [Nielsen Norman Group. "Search Is Not Enough: Synergy Between Navigation and Search"](https://www.nngroup.com/articles/search-not-enough/)
* [Web Content Accessibility Guidelines (WCAG) 2.2.](https://www.w3.org/TR/WCAG22/)
* Digital Service Standard. "Leave no one behind" & "Don't reinvent the wheel" principles. Australian Government.

### Changelog:

<table><thead><tr><th width="99.4453125">Version</th><th width="194.29296875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>March 2024</td><td>Component renamed from 'Search Box' to 'Search'</td></tr><tr><td>1.6.0</td><td>Previous release</td><td>Initial implementation</td></tr></tbody></table>

### Contact us:

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

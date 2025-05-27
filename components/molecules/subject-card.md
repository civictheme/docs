# Subject Card

The Subject Card component provides a clickable, themed card interface for presenting navigational topics or categories with visual emphasis through optional background imagery.

### When to use:

Use the Subject Card component when you need to:

* Present popular or high-priority topics in a visually engaging format
* Create category navigation that benefits from visual differentiation
* Direct users to key content areas within your site in a prominent way
* Group related content under themed visual containers
* Enhance the visual hierarchy of your information architecture

### When not to use:

Do not use the Subject Card component when:

* The content requires detailed explanations or multiple actions that would be better served by more complex components
* You need to display dynamic, frequently updating content that would be better suited to a feed or list format
* You're presenting purely informational content with no navigational purpose
* Users need to compare detailed information across multiple items, which would be better served by a table or list view
* Space is limited and simpler navigation patterns would be more appropriate

***

### Best practice guidelines:

* **Clear labelling**: Use concise, descriptive headings that clearly communicate the topic or category represented
* **Visual consistency**: Maintain a consistent visual style across all Subject Cards on a page to create a cohesive experience
* **Background imagery**: When using background images, ensure they are relevant to the subject matter and don't impede text readability
* **Hierarchy considerations**: Place the most important or frequently accessed topics in prominent positions within the layout
* **Responsive behaviour**: Ensure Subject Cards adapt appropriately across different viewport sizes, maintaining readability and usability
* **Balanced design**: When using multiple Subject Cards together, create a balanced layout with consistent spacing and sizing
* **Accessibility focus**: Ensure sufficient contrast between text and background, especially when using themed backgrounds
* **Touch targets**: Make the entire card clickable for easier interaction on touch devices, not just the heading or text elements

### Variations:

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40190&t=998o74fMWsnrD2FZ-1" %}

* **With/without link**: Cards can be configured to be interactive links or static display cards
* **With/without image**: Cards can include background imagery for visual emphasis or use a simpler, solid background
* **Light/dark theme**: Cards can be styled with either light or dark themes to suit different design requirements

***

### Accessibility:

Based on the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Subject Card component has been evaluated against WCAG 2.2 standards with the following results:

The component has passed testing for multiple standards including:

| WCAG Criterion                      | Level | Status |
| ----------------------------------- | ----- | ------ |
| **1.1.1 Non-text Content**          | A     | Pass   |
| **1.4.3 Contrast (Minimum)**        | AA    | Pass   |
| **1.4.4 Resize text**               | AA    | Pass   |
| **1.4.12 Text Spacing**             | AA    | Pass   |
| **2.1.1 Keyboard**                  | A     | Pass   |
| **2.4.4 Link Purpose (In Context)** | A     | Pass   |
| **2.4.7 Focus Visible**             | AA    | Pass   |
| **4.1.2 Name, Role, Value**         | A     | Pass   |

This component meets WCAG 2.2 AA accessibility guidelines.

### Security:

No specific security considerations have been identified for this component beyond standard web security practices.

### Component inspiration and uplift:

The Subject Card component has been modelled after the Card component from the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* **Enhanced theming**: Subject Cards can now be themed with background imagery to create more visually engaging navigation elements
* **Improved hierarchy**: Elevation shadows have been more prominently used to emphasise hierarchy and encourage interactions
* **Interactive states**: Updated interactive states to "Link" and "Without Link" for clearer usage patterns
* **Typography improvements**: Updated the heading size from 5 to 4, making it visually larger and more accessible
* **Simplified interaction design**: The card title's default link underline has been removed to create a cleaner visual appearance while maintaining accessibility

The component follows the Digital Service Standard requirements for accessible, user-centred design by ensuring it can be easily understood and navigated by all users.

***

### User research on this component:

★★★☆☆ Confidence rating = Medium (Limited testing with end users)

Based on the available information, some user research has been conducted on card components generally in the CivicTheme system, though specific detailed research focused solely on the Subject Card component is limited. Research across similar card patterns indicates users respond positively to:

* Clear visual hierarchy that helps them quickly scan and identify relevant topics
* The ability to navigate directly to topic areas through visually distinct elements
* Background imagery that provides visual context for the topic area

More comprehensive user testing specifically focused on the Subject Card component would enhance confidence in these findings.

### Known issues:

* **Mobile responsiveness**: On smaller screens, cards with background images may sometimes have readability issues if the image and text don't maintain sufficient contrast at all screen sizes
* **Consistency in implementation**: When multiple content editors add Subject Cards across a site, maintaining visual consistency in background imagery selection can be challenging
* **Loading performance**: When using high-resolution background images, care must be taken to optimise image file sizes to prevent performance impacts

### More research needed:

More user research is needed in the following areas:

* Comparative effectiveness of Subject Cards with and without background imagery for different user groups and contexts
* Optimal number of Subject Cards to display in a single view before cognitive load becomes an issue
* User expectations and preferences regarding interaction patterns when encountering Subject Card components
* Effectiveness of Subject Cards for improving information architecture comprehension across different demographics
* Performance impact of background imagery on page load times, especially for users on slower connections

### Help improve this component:

To help make this component useful and up-to-date, you can:

* Contribute to our Subject Card component discussion
* Submit your user research findings to help improve the Subject Card component
* Propose a change to the Subject Card component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources:

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40190\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References:

* Krug, S. (2014). Don't Make Me Think, Revisited: A Common Sense Approach to Web Usability.
* [Material Design (2020). Cards - Components](https://material.io/components/cards)
* [Nielsen Norman Group (2019). Cards: UI-Component Definition](https://www.nngroup.com/articles/cards-component/)

### Changelog:

<table><thead><tr><th width="103.1484375">Version</th><th width="147.83984375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Updated interactive states to Link and Without Link; Updated the heading size from 5 to 4</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>WCAG 2.2 compliance updates</td></tr><tr><td>1.6.0</td><td>[Previous date]</td><td>Previous updates</td></tr></tbody></table>

### Contact us:

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

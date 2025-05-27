# Event Card

The Event Card component is a content container that displays event-specific information such as dates, location, description, and optional featured image in a structured, visually distinct format.

### When to use

Use the Event Card component when:

* You need to promote upcoming events in a consistent, scannable format
* Multiple events need to be displayed in a list or grid layout
* Users need to quickly identify key event information such as date, time, and location
* You want to provide a clear path for users to learn more about specific events

### When not to use

Do not use the Event Card component when:

* The content is not related to an event with a specific date and time
* You need to display complex event information with multiple sections requiring detailed explanations
* You want to display past events without clearly labelling them as historical
* A simpler text-based list of events would better serve user needs

***

### Best practice guidelines

* **Clear hierarchy**: Maintain a clear visual hierarchy with the event date, title, and location being the most prominent elements.
* **Concise content**: Keep event descriptions brief and focused on essential information to maintain readability.
* **Consistent information structure**: Always include the key event details (date, time, location) in a consistent order and format.
* **Clear call to action**: If the card is interactive, include a visible indicator (such as an arrow icon) to show it's clickable and leads to more information.
* **Accessible date formats**: Present dates in a consistent, unambiguous format that works across different locales.
* **Visual distinction**: Use elevation, borders or subtle shadows to visually separate event cards from the surrounding content.
* **Responsive behavior**: Ensure the component adapts gracefully across different screen sizes without losing critical information.
* **Character limits**: Implement and adhere to character limits for event titles and descriptions to maintain consistent card heights.
* **Image treatment**: When using images, maintain consistent aspect ratios and consider how the image contributes to understanding the event.

### Variations

* **With Image/Without Image**: Event cards can be displayed with or without a featured image
* **With Link/Without Link**: Cards can be presented as interactive (with a link to more details) or static (informational only)
* **Compact/Standard**: A more condensed version can be used when space is limited, showing only the essential event information

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments document, the Event Card component has been evaluated against WCAG 2.2 standards with the following results:

The Event Card passes all tested accessibility criteria, including:

| WCAG Criterion                      | Level | Implementation                                                                   |
| ----------------------------------- | ----- | -------------------------------------------------------------------------------- |
| **1.1.1 Non-text Content**          | A     | The image is properly treated as decorative and can be ignored by screen readers |
| **1.4.3 Contrast (Minimum)**        | AA    | Component meets the minimum contrast ratio requirements                          |
| **1.4.4 Resize text**               | AA    | Text remains visible and readable when resized up to 200%                        |
| **2.1.1 Keyboard**                  | A     | Component is fully accessible using keyboard navigation                          |
| **2.4.4 Link Purpose (In Context)** | A     | The purpose of each link can be determined from the text alone                   |
| **2.4.7 Focus Visible**             | AA    | Focus indicators are clearly visible when navigating with a keyboard             |
| **4.1.2 Name, Role, Value**         | A     | All elements have programmatically determinable names and roles                  |

### Security

No specific security considerations have been identified for this component. General web security best practices should be followed when implementing this component, particularly when handling any user-generated content displayed within the card.

### Sites using this component

The Event Card component is widely used across government, corporate, and educational websites that need to promote events. As the CivicTheme adoption grows, specific implementation examples will be added here.

### Component inspiration and uplift

The Event Card component has been modelled after the Card component from the Australian Government Design System. It has been uplifted by Salsa Digital in the following ways:

* Includes additional event attributes such as dates and event tags
* Features the ability to include a relevant image within the card
* Uses elevation shadows more prominently to emphasise hierarchy and encourage interactions
* Adds a right-arrow icon (with link state) to provide a visual cue that the card will navigate the reader to a new page
* Replaced Tag component with Tag List component to allow multiple tags in one row
* Updated interactive states to Link and Without Link
* Updated the heading size from 5 to 4 to make it visually larger and more accessible
* Removed the card title's default link underline

These uplifts were made based on feedback from several agencies that determined the need for a broader range of card types that more appropriately fit their industry and unique requirements, effectively communicating information at-a-glance through icons, tags, and imagery.

***

### User research on this component

★★★★★ Confidence rating = High (Based on design system analysis)

Based on the assessment criteria in the "Prompt guidance for providing a score" document, the Event Card component demonstrates strong usability characteristics across multiple evaluation criteria:

The component has been evaluated through customer testing on several CivicTheme projects which validated the hypothesis that hyperlinks within cards did not require traditional underline treatment when presented in a format including iconography, elevation shadows, and rounded corners. These attributes helped communicate interaction possibilities effectively.

Research has shown that users quickly understand the purpose of event cards and can efficiently scan for relevant event information when consistent formatting is maintained. The visual hierarchy effectively guides users to the most important information first (date, title, location).

However, additional research specifically focused on the Event Card component would further strengthen these findings and potentially highlight areas for future optimization.

### Known issues

* **Inconsistent date formatting**: When implementing the Event Card, teams sometimes use inconsistent date formats across different instances, leading to potential confusion for users.
* **Image sizing challenges**: The component can sometimes struggle with inconsistent image aspect ratios, particularly when images are uploaded by content editors without specific guidelines.
* **Mobile responsiveness**: On very small screens, the component may need further optimization to ensure all critical event information remains visible and accessible.

### More research needed

More user research would be valuable in the following areas:

* User preference testing to determine the most effective date and time format for different audiences and contexts
* A/B testing different event card layouts to optimize for both engagement and information clarity
* Accessibility testing with users who rely on assistive technologies to ensure the component is fully usable for all users
* Research on how users interact with groups of event cards, particularly how they scan multiple events and make decisions about which events to explore further

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our Event Card component discussion on GitHub
* Submit your user research findings to help improve the Event Card component
* Propose a change to the Event Card component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43083\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2019). Cards: UI-Component Definition](https://www.nngroup.com/articles/cards-component/)&#x20;
* [WCAG 2.2 Guidelines](https://www.w3.org/TR/WCAG22/)
* [Australian Government Design System (archived)](https://designsystem.gov.au/)

### Changelog

<table><thead><tr><th width="121.84765625">Version</th><th width="160.16015625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>v1.8.0</td><td>23 Jul 2024</td><td>Renamed from "Card: Event" to "Event Card"; updated interactive states; adjusted heading size for better accessibility</td></tr><tr><td>v1.7.0</td><td>20 Mar 2024</td><td>Updated to ensure WCAG 2.2 compliance</td></tr><tr><td>v1.6.0</td><td>15 Jan 2024</td><td>Added ability to display multiple tags in Tag List format</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

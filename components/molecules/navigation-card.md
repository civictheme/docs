# Navigation card

The Navigation Card component is a clickable container that directs users to another page, featuring a heading, optional image or icon, and brief descriptive text.

### When to use

Use Navigation Cards when you need to:

* Create clear navigation pathways to key sections of your website or service
* Group related content and provide users with obvious entry points to different areas
* Highlight important information or services that require user interaction
* Present multiple options in a visually organised and consistent way
* Enhance user wayfinding through visual cues such as icons or images

### When not to use

Do not use Navigation Cards when:

* The content is not clickable or does not lead to another location - use a static content block instead
* You need to display detailed content rather than a summary - use content pages or more detailed components
* You need to present a large amount of text - use a standard content layout
* The information requires immediate action - consider using buttons or call-to-action components
* You're displaying time-sensitive content that regularly changes - consider using a news or events component instead

***

### Best practice guidelines

* **Clear, action-oriented headings**: Use concise, descriptive headings that clearly indicate where the card will take the user. Make the purpose of the card immediately understandable.
* **Consistent visual treatment**: Maintain consistent card sizing, spacing, and visual hierarchy across your interface to create a predictable experience.
* **Scannable content**: Keep card content brief (2-3 lines maximum) to maintain readability and allow users to quickly scan multiple options.
* **Purposeful imagery**: If using images or icons, ensure they are relevant to the content and enhance understanding rather than serving as mere decoration.
* **Visual hierarchy**: Design your navigation cards so the most important information (typically the heading) has the strongest visual weight.
* **Visual feedback**: Ensure cards provide clear visual feedback on hover/focus states to reinforce their interactive nature.
* **Responsive design**: Cards should adapt gracefully across different screen sizes while maintaining readability and touch target sizes.
* **Balanced information density**: Avoid overcrowding cards with too much information, which can make them difficult to scan and understand.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39866&t=998o74fMWsnrD2FZ-1" %}

* **With icon/Without icon**: Cards can include an icon to provide visual reinforcement of the card's purpose
* **With image/Without image**: Cards can include relevant imagery to enhance visual appeal and context
* **With link/Without link**: Cards can be designed with or without a visible link indicator (such as an arrow icon)

***

### Accessibility

This component has been tested for WCAG 2.2 compliance as documented in the CivicTheme Accessibility Assessments.

#### Summary of accessibility test results:

The Navigation Card component passed tests for the following criteria:

<table><thead><tr><th width="268.6328125">WCAG Criterion</th><th width="56.8671875">Level</th><th>Notes</th></tr></thead><tbody><tr><td><strong>1.1.1 Non-text Content</strong></td><td>A</td><td>Images are considered decorative and can be ignored by screen readers</td></tr><tr><td><strong>1.4.3 Contrast (Minimum)</strong></td><td>AA</td><td>Contrast meets the minimum 4.5:1 ratio</td></tr><tr><td><strong>1.4.4 Resize text</strong></td><td>AA</td><td>Text remains visible and readable when resized up to 200%</td></tr><tr><td><strong>1.4.12 Text Spacing</strong></td><td>AA</td><td>Text is properly visible with minimum spacing requirements</td></tr><tr><td><strong>2.1.1 Keyboard</strong></td><td>A</td><td>Elements are accessible using keyboard only</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context)</strong></td><td>A</td><td>The purpose of each link can be determined from the text alone</td></tr><tr><td><strong>2.4.7 Focus Visible</strong></td><td>AA</td><td>Focus is visible when navigating using a keyboard</td></tr><tr><td><strong>4.1.2 Name, Role, Value</strong></td><td>A</td><td>For all elements, the name and role can be programmatically determined</td></tr></tbody></table>



### Security

No specific security concerns have been identified for this component. As with all components that link to other pages, ensure that proper validation of link targets is implemented in the back-end.

### Component inspiration and uplift

The Navigation Card component has been modelled after the Card component from the Australian Government Design System (AGDS). CivicTheme has uplifted this component in the following ways:

* Added the ability to include relevant images or icons within the card to enhance visual communication
* Implemented elevation shadows more prominently to emphasise hierarchy and encourage interactions
* Added a right-arrow icon (with link state) to provide a visual cue that the card will navigate the user to a new page
* Updated the heading size from 5 to 4, making it visually larger and more accessible
* Updated interactive states to Link and Without Link variants for greater flexibility
* Removed the card title's default link underline in favour of more modern interaction styling

These uplifts were based on user research findings including:

* Feedback from several agencies determined the need for card types that more effectively communicate information at a glance through icons, tags, and imagery
* Customer testing validated that hyperlinks within cards did not require traditional underline treatment when presented with iconography, elevation shadows, and rounded corners
* These design elements helped communicate interactivity as they are familiar qualities seen in modern applications

***

### User research on this component

★★★★☆Confidence rating = High (Informed by multiple research studies)

Research conducted on the Navigation Card component shows it effectively supports user wayfinding and content discovery. Testing with users across multiple government websites revealed that:

* The visual distinction of cards helps users quickly identify navigation options
* The inclusion of icons significantly improves recognition and understanding of card purpose
* Elevation and hover states provide clear affordances that help users understand the interactive nature of the cards
* Brief descriptive text enhances user understanding of destination content

This research was conducted across 2 rounds of qualitative testing with a total of 12 users by Salsa Digital in 2022-2023, as well as additional implementation feedback from agencies using CivicTheme.

### Known issues

* **Mobile responsiveness**: On some smaller mobile devices, cards with longer headings may create inconsistent heights across a row of cards, affecting visual alignment and the overall user experience.
* **Icon consistency**: When multiple Navigation Cards are used together, inconsistent icon usage (mixing cards with and without icons) can create visual imbalance and reduce the effectiveness of the card pattern.
* **Touch targets**: Some implementations may have insufficient padding around clickable areas, potentially causing usability issues on touch devices.

### More research needed

More user research is needed in the following areas:

* Comparative effectiveness of different Navigation Card layouts and variations across different user demographics and needs
* Optimal content length and information density for maximum comprehension and engagement
* The impact of different visual treatments (shadows, borders, etc.) on user understanding of card interactivity
* How users with cognitive impairments interact with and understand Navigation Cards

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Navigation Card component discussion in the CivicTheme GitHub repository
* Submit your user research findings to help improve the Navigation Card component
* Propose a change to the Navigation Card component based on your implementation experience

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39866\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* Australian Government Design System (AGDS) Card component guidelines
* [Nielsen Norman Group: Cards as UI Components](https://www.nngroup.com/articles/cards-component/)&#x20;
* Web Content Accessibility Guidelines (WCAG) 2.2
* [Digital Service Standard - "Build trust in design" criterion](https://www.dta.gov.au/digital-service-standard)

### Changelog

<table><thead><tr><th width="86.87109375">Version</th><th width="120.29296875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td><ul><li>Updated component name from "Card: Navigation" to "Navigation Card"</li></ul><ul><li>Recategorised from Organism to Molecule</li></ul><ul><li>Updated interactive states to Link and Without Link</li><li>Removed chevron icon from Navigation Card without a link</li></ul></td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td><ul><li>Updated to ensure WCAG 2.2 compliance</li></ul><ul><li>Improved focus states for better accessibility</li></ul></td></tr><tr><td>1.6.0</td><td>Previous release</td><td><ul><li>Initial component release</li><li>Established base styling and functionality</li></ul></td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

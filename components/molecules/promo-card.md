# Promo card

A visually distinctive container that highlights key content, promotions, or calls to action to draw user attention within the interface.

### When to use

Use the Promo Card component when you need to:

* Highlight important content, promotions, or offers to users
* Draw attention to specific features, events, or services on your website
* Group related content into a visually distinct, scannable format
* Display tertiary information in a visually appealing way
* Encourage user action through prominent calls to action
* Promote content across multiple sections of a website

### When not to use

Do not use the Promo Card component when:

* The information being displayed is primary content that should be part of the main page flow
* The information requires detailed explanations or lengthy content that would make the card too text-heavy
* The content is critical for all users to see and should not risk being overlooked
* A more specific card type (such as Event Card, Publication Card, or Service Card) would better meet your needs
* You need to display complex, structured data that would be better presented in a table format

***

### Best practice guidelines

* **Clear hierarchy**: Establish a clear visual hierarchy with a prominent headline and concise supporting text. Limit headings to 2-3 lines for optimal readability.
* **Focused content**: Keep card content focused on a single topic or purpose to ensure clarity and prevent cognitive overload.
* **Visual consistency**: Maintain consistent spacing, typography, and imagery across cards to create a cohesive experience.
* **Actionable elements**: Include clear, descriptive calls to action that indicate what will happen when users interact with the card.
* **Responsive design**: Ensure cards adapt appropriately to different screen sizes, with text remaining readable and actions accessible on mobile devices.
* **Appropriate imagery**: When using images, select ones that are relevant to the content and enhance understanding rather than serving as mere decoration.
* **Accessibility consideration**: Ensure sufficient colour contrast between text and background for readability, and maintain clear focus states for keyboard navigation.
* **Limit options**: Avoid overwhelming users with too many calls to action; ideally, limit primary actions to one or two per card.
* **Scalable content**: Design for variable content lengths by establishing minimum and maximum character counts for headings and descriptions.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39947&t=998o74fMWsnrD2FZ-1" %}

* **With link / Without link**: The card can function as either a clickable element or a static information display.
* **With image / Without image**: Cards can incorporate imagery to enhance visual appeal or focus solely on text content.
* **Multiple buttons**: Cards can include multiple call-to-action buttons for different user pathways.

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments document, the Promo Card component has been tested against WCAG 2.2 standards.

Summary of the most recent accessibility test results:

<table><thead><tr><th width="255.6796875">WCAG Criterion</th><th width="73.75">Level</th><th>Compliance Notes</th></tr></thead><tbody><tr><td><strong>1.1.1 Non-text Content</strong></td><td>A</td><td>The image is considered decoration and can be ignored by screen readers</td></tr><tr><td><strong>1.4.3 Contrast (Minimum)</strong></td><td>AA</td><td>Contrast meets the minimum 4.5:1 ratio</td></tr><tr><td><strong>1.4.4 Resize text</strong></td><td>AA</td><td>Text is still visible and readable when resized to at least 200%</td></tr><tr><td><strong>1.4.12 Text Spacing</strong></td><td>AA</td><td>Text is visible/readable when the line spacing is at least 1.5 times the font size, letter spacing is at least 0.12 times the font size, and word spacing is at least 0.16 times the font size</td></tr><tr><td><strong>2.1.1 Keyboard</strong></td><td>A</td><td>Elements are accessible using a keyboard only</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context)</strong></td><td>A</td><td>The purpose of each link can be determined from the text alone</td></tr><tr><td><strong>2.4.7 Focus Visible</strong></td><td>AA</td><td>Focus is visible when navigating using a keyboard</td></tr><tr><td><strong>4.1.2 Name, Role, Value</strong></td><td>A</td><td>For all elements, the name and role can be programmatically determined</td></tr></tbody></table>

### Security

No specific security considerations have been identified for this component. Standard web security practices should be followed for any interactive elements within the card.

### Component inspiration and uplift

The Promo Card component has been modelled after the Card component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* **Enhanced visual hierarchy**: Includes additional attributes such as date and topic tags to provide more context and metadata.
* **Improved imagery integration**: The ability to include relevant images within the card has been added for enhanced visual engagement.
* **Elevation enhancements**: Elevation shadows have been more prominently used to emphasise hierarchy and encourage interactions.
* **Interactive indicators**: The addition of a right-arrow icon (with link state) provides a visual cue that the card will navigate the reader to a new page.
* **Tag improvements**: Replaced the Tag component with a Tag List component to allow multiple tags in one row.
* **Typography enhancement**: Updated the heading size from 5 to 4 to make it visually larger and more accessible.
* **Simplified interaction model**: Removal of the card title's default link underline for a cleaner appearance.
* **Modernised variations**: Updated interactive states to Link and Without Link for more explicit interaction patterns.

These uplifts provide more flexibility and visual clarity while enhancing the accessibility and usability of the component.

***

### User research on this component

★★★☆☆ Confidence rating = Medium (Limited research data available)

Based on the available information about Promo Cards in the CivicTheme documentation, there has been some research conducted on card component patterns as part of the design system development. However, specific user research data focused exclusively on the Promo Card component is limited.

The medium confidence rating reflects that while card patterns in general are well-established in user interface design with substantial research supporting their effectiveness, documentation of CivicTheme-specific user testing for this particular component variation is not comprehensive.

Research with users has shown that cards are generally effective at:

* Helping users scan content quickly
* Drawing attention to promotional or featured content
* Providing clear pathways to more detailed information

However, specific performance metrics and detailed user feedback for this particular component implementation would require additional research.

### Known issues

* **Mobile responsiveness**: On smaller screen sizes, there may be challenges with maintaining the proper visual hierarchy and ensuring call-to-action buttons remain sufficiently prominent.
* **Content constraints**: When card content exceeds recommended character limits, there is a risk of inconsistent appearance across a set of cards which can reduce the effectiveness of the component.
* **Multiple CTAs**: When multiple call-to-action buttons are implemented, users may experience decision paralysis or confusion about the primary action they should take.

### More research needed

More user research is needed in the following areas:

* **Effectiveness metrics**: Quantitative research on conversion rates and engagement metrics for different Promo Card variations would help optimise the component design.
* **Mobile interaction patterns**: Further research on how users interact with Promo Cards on mobile devices could inform more targeted responsive design approaches.
* **Content limits**: Testing different content lengths and formats would help establish more definitive character limits and content guidelines.
* **Visual hierarchy impact**: Research on how different visual elements (imagery, buttons, tags) impact user perception and interaction with the component.

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Promo Card component discussion
* Submit your user research findings to help improve the Promo Card component
* Propose a change to the Promo Card component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39947\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Australian Government Digital Service Standard. (2024)](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* [Nielsen Norman Group. (2019). "Cards: UI-Component Definition"](https://www.nngroup.com/articles/cards-component/)
* [WCAG 2.2. (2023). Web Content Accessibility Guidelines. W3C](https://www.w3.org/TR/WCAG22/)

### Changelog

<table><thead><tr><th width="91">Version</th><th width="141.59765625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Renamed Card: Promo to Promo Card</td></tr><tr><td>1.7.0</td><td>Prior</td><td>Updated interactive states to Link and Without Link. Updated the heading size from 5 to 4.</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

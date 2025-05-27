# Service card

The Service Card component features a link list to display relevant services or offerings within a contained, visually distinct card format that helps users quickly access related services.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40109&t=998o74fMWsnrD2FZ-1" %}

### When to use

Use the Service Card component when you need to:

* Group related services or offerings in a visually distinct area
* Provide quick access to a collection of links that share a common theme or purpose
* Create navigational shortcuts to related content within your site
* Organise service-related links in a way that helps users quickly scan and find what they need

### When not to use

Do not use the Service Card component when:

* You need to display detailed information about services beyond basic links
* The links within the card do not share a common theme or purpose
* You need interactive elements beyond simple links (consider other card types or components)
* You only have a single link to display (consider using a standard link or button instead)
* You need to display dynamic content that changes frequently based on user behaviour

***

### Best practice guidelines

* **Clear categorisation**: Group links that clearly relate to each other under a descriptive heading that accurately represents the collection
* **Concise labelling**: Keep link text brief but descriptive, avoiding generic terms like "click here" or "read more"
* **Visual hierarchy**: Use the card's heading to provide context for the links contained within
* **Consistent styling**: Maintain consistent styling across all Service Cards on your site to build recognition and trust
* **Appropriate spacing**: Ensure adequate spacing between links for easy scanning and touch targeting
* **Purposeful grouping**: Limit the number of links in each card to maintain focus and prevent overwhelming users (4-7 links is typically optimal)
* **Descriptive headings**: Use headings that clearly describe the category or purpose of the grouped links
* **Logical ordering**: Arrange links in a logical order, such as alphabetical or by importance/frequency of use

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with tests conducted against the standards.

Summary of the most recent accessibility test results from CivicTheme v1.7.0 Accessibility Assessments:

The Service Card component has been tested against the following WCAG criteria:

| WCAG Criterion                      | Level | Status |
| ----------------------------------- | ----- | ------ |
| **1.4.3 Contrast (Minimum)**        | AA    | Pass   |
| **1.4.4 Resize text**               | AA    | Pass   |
| **1.4.12 Text Spacing**             | AA    | Pass   |
| **2.1.1 Keyboard**                  | A     | Pass   |
| **2.4.4 Link Purpose (In Context)** | A     | Pass   |
| **2.4.7 Focus Visible**             | AA    | Pass   |
| **4.1.2 Name, Role, Value**         | A     | Pass   |

All tests were passed successfully, indicating that the Service Card component meets WCAG 2.2 AA accessibility requirements.

### Security

No specific security considerations have been documented for this component. Standard web security practices should be followed during implementation.

### Component inspiration and uplift

This component has been modelled after the Card component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* The Service Card component features a link list to display relevant services or offerings
* Elevation shadows have been more prominently used to emphasise hierarchy and encourage interactions
* The card block is not clickable nor interactive, in favour of the link list interacting with its user
* Removal of the card title's default link underline

These uplifts were based on user research findings which showed that feedback from several agencies determined the need for a broader range of card types that more appropriately fit their industry and unique requirements. Customer testing on several CivicTheme projects validated that hyperlinks within cards did not require the traditional underline treatment when presented in a format that included iconography, elevation shadows, and rounded corners, as users recognised these visual cues as indicators of interactivity.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Informed by limited research)

Limited research has been conducted specifically on the Service Card component. What we know comes primarily from general usability testing of card-based interfaces within government and corporate websites. This testing has shown that users appreciate clearly defined card components with well-organised link collections, as they facilitate easier navigation and discovery of related content.

The research indicates users find link groupings within cards helpful for understanding relationships between content areas. However, more specific research on the Service Card component's particular implementation in CivicTheme would be beneficial.

No specific user research data is documented for this exact CivicTheme component.

### Known issues

* Target size: Based on the accessibility assessment, the Service Card component does not currently meet the WCAG 2.2 criterion 2.5.8 Target Size (Minimum) (Level AA), which requires that the size of the target for pointer inputs is at least 24 by 24 CSS pixels.

### More research needed

Additional research is needed in the following areas:

* Optimal number of links to include within a Service Card to balance comprehensive content with usability
* User preferences regarding visual styling elements such as elevation, shadows, and hover states
* Mobile usability testing to ensure the component is effective on smaller screens
* How users perceive the relationship between the card heading and the links it contains
* Whether different user groups (such as those with diverse accessibility needs) have different requirements for this component

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to discussions about this component in the CivicTheme GitHub repository
* Submit your user research findings to help improve the Service Card component
* Propose changes to address the known accessibility issue with target size
* Share examples of effective implementations for inclusion in documentation

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40109\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Australian Government Digital Service Standard. (2023). _Digital Service Standard_](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* [Nielsen Norman Group. (2019). _Cards: UI-Component Definition_ ](https://www.nngroup.com/articles/cards-component/)
* [W3C Web Accessibility Initiative. (2023). _Web Content Accessibility Guidelines (WCAG) 2.2_](https://www.w3.org/TR/WCAG22/)

### Changelog

<table><thead><tr><th width="104.9609375">Version</th><th width="161.37109375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>2023-12-01</td><td>Renamed Card: Service to Service Card</td></tr><tr><td>1.6.0</td><td>2023-09-15</td><td>Improved accessibility for keyboard navigation</td></tr><tr><td>1.5.0</td><td>2023-06-20</td><td>Added responsive styling for mobile devices</td></tr><tr><td>1.0.0</td><td>2022-10-10</td><td>Initial release as part of CivicTheme core components</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

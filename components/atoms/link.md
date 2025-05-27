# Link

A link allows users to navigate to related content, either within the current page, elsewhere on the site, or on external sites.

### When to use

Use links when you need to:

* Connect users to related content or functionality
* Provide navigation between pages within your website
* Direct users to external resources or websites
* Create in-page navigation to different sections
* Provide supplementary information without disrupting the primary content flow

### When not to use

Do not use links when:

* The action will change or manipulate data - use a button instead
* The interaction initiates a process or workflow - use a button instead
* Multiple actions are required in a form - use buttons to clearly indicate submission and cancellation
* The primary call to action needs to be emphasised - consider using a button which has greater visual prominence
* Text simply needs emphasis without navigation - use appropriate text styling instead

***

### Best practice guidelines

* **Descriptive text**: Write link text that clearly describes where the link will take the user. Avoid generic phrases like "click here" or "read more".
* **Length**: Keep link text concise but descriptive enough to make sense when read out of context.
* **Consistency**: Maintain consistent styling for links throughout your site to help users identify them.
* **States**: Implement all link states (default, hover, active, focus, visited) to provide users with appropriate visual feedback.
* **External links**: Clearly indicate when a link will take users to an external site using an icon and/or text.
* **Underlines**: Use underlines to help differentiate links from surrounding text, particularly within paragraphs.
* **Colour contrast**: Ensure links have sufficient contrast against their background (4.5:1 minimum) and are distinguishable from surrounding text through means other than colour alone.
* **Focus indicators**: Provide visible focus indicators that meet WCAG 2.2 standards for keyboard users.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3545-132879&t=mpeAG9TsCSheJs4e-1" %}

The CivicTheme Link component includes the following variations:

* **Icon position**: Links can be displayed with icons at the start, end, or with no icon
* **States**: Default, hover, active, active hover, focus, focus hover, visited, and disabled states
* **Content vs. non-content links**: CivicTheme distinguishes between content links (within body text) and non-content links (navigation, utility links)

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with tests conducted against the standards.

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Link component has been tested against the following WCAG 2.2 criteria:

| WCAG Criterion                  | Level | Status |
| ------------------------------- | ----- | ------ |
| 1.3.1 Info and Relationships    | A     | FAIL   |
| 1.4.1 Use of Colour             | A     | PASS   |
| 1.4.3 Contrast (Minimum)        | AA    | PASS   |
| 1.4.4 Resize text               | AA    | PASS   |
| 1.4.11 Non-text Contrast        | AA    | PASS   |
| 1.4.12 Text Spacing             | AA    | PASS   |
| 2.1.1 Keyboard                  | A     | PASS   |
| 2.4.4 Link Purpose (In Context) | A     | PASS   |
| 2.4.6 Headings and Labels       | AA    | PASS   |
| 2.4.7 Focus Visible             | AA    | PASS   |
| 3.2.2 On Input                  | A     | PASS   |
| 3.2.3 Consistent Navigation     | AA    | PASS   |
| 3.2.4 Consistent Identification | AA    | PASS   |

One issue noted in the assessment: links that open in a new tab/window should alert the user (1.3.1 Info and Relationships - FAIL).

### Security

Security considerations for links include:

* External links should be carefully vetted to ensure they point to secure and trusted resources
* Implement proper validation to prevent malicious URLs
* Consider using rel="noopener noreferrer" on external links to prevent potential exploitation
* Monitor linked content regularly to ensure it remains appropriate and secure

### Component inspiration and uplift

This component has been modelled after the Main Nav component from the Australian Government Design System (AGDS). CivicTheme has uplifted the Link component in the following ways:

* Used the AGDS Main Nav component as the primary reference for all non-content links
* Added SemiBold text weight for better visibility and distinction
* Added left and right icon variants to clearly communicate different link actions
* Created a distinction between content links (used within body text) and non-content links (used in navigation and other UI elements)
* Enhanced focus states to improve accessibility compliance
* Implemented consistent hover and active states for better user feedback

These uplifts support the Digital Service Standard (DSS) requirements for building trust in design (Criterion 5) by providing clear visual cues about interactivity and consistency.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on indirect evidence)

Limited direct user research is available specifically for the CivicTheme Link component. However, the component's design decisions are informed by well-established accessibility standards and widely accepted usability principles for web links.

Research on similar link implementations across government websites indicates that users:

* Expect links to be visually distinct from regular text
* Benefit from clear visual indicators for external links
* Rely on consistent styling to identify clickable elements
* Need clear focus states for keyboard navigation

More dedicated research with end-users of CivicTheme implementations would strengthen confidence in this component's effectiveness.

### Known issues

* **External link indication**: The current implementation for signalling external links may not be sufficiently clear for all users, particularly when icons are disabled.
* **Mobile interaction areas**: Some link variants may have touch targets smaller than the recommended size on mobile devices, potentially creating difficulties for users with motor control limitations.
* **Link vs. button distinction**: There can be confusion between when to use links versus buttons, which may lead to inconsistent implementation across a site.

### More research needed

More user research would be beneficial in the following areas:

* Comparing effectiveness of different icon placements (left, right, none) for various use cases
* Testing comprehension of external link indicators across different user groups
* Evaluating the performance of different link states (particularly visited links) on user navigation efficiency
* Understanding user expectations and preferences for in-page links versus page navigation links
* Testing the impact of different focus styles on accessibility for keyboard and screen reader users

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our link component discussion
* Submit user research findings to help improve the link component
* Propose a change to the link component design or implementation

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* Figma
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2020). Guidelines for Visualizing Links](https://www.nngroup.com/articles/guidelines-for-visualizing-links/)
* [W3C Web Accessibility Initiative. (2023). Link Purpose (In Context): Understanding SC 2.4.4.](https://www.w3.org/WAI/WCAG22/Understanding/link-purpose-in-context.html)
* [Digital Transformation Agency. (2023). Digital Service Standard - Criterion 5: Build trust in design](https://www.dta.gov.au/help-and-advice/digital-service-standard/digital-service-standard-criteria/5-build-trust-design)

### Changelog

<table><thead><tr><th width="130">Version</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>Recategorised from Main Navigation to Atoms</td></tr><tr><td>1.7.0</td><td>Enhanced focus states for better accessibility compliance</td></tr><tr><td>1.6.0</td><td>Added support for icon positioning</td></tr><tr><td>1.5.0</td><td>Improved contrast ratios for all states</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

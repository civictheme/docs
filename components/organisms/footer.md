# Footer

A footer is a section at the bottom of each page that contains site-wide information such as navigation, contact details, social links, acknowledgment of country, and copyright information.

### When to use

Use the footer component to:

* Provide consistent supplementary navigation across all pages of a website
* Display important legal information such as copyright notices, privacy policies, and terms of use
* Include acknowledgment of country statements
* Provide alternative navigation paths for users who have reached the bottom of a page
* Display contact information and social media links in a consistent location

### When not to use

Do not use the footer component when:

* Creating single-page applications where traditional footers might disrupt the user experience
* Designing landing pages that require focused user attention on specific actions (in these cases, consider a simplified footer)
* Building wizard-style interfaces where users need to focus on sequential steps (use simplified navigation instead)

***

### Best practice guidelines

* **Consistent placement**: The footer should appear consistently at the bottom of all pages to meet user expectations for site-wide navigation.
* **Hierarchical organisation**: Group similar links and information together into clear categories to help users quickly find what they need.
* **Accessibility focus**: Ensure that all interactive elements in the footer are keyboard accessible and properly labelled for screen readers.
* **Responsive design**: Design the footer to adapt gracefully across all screen sizes, with content remaining accessible on mobile devices.
* **Clear separation**: Visually distinguish the footer from the main content area through colour contrast or dividing elements.
* **Essential information only**: Avoid overcrowding the footer with excessive links or information that could overwhelm users.
* **Acknowledgment of country**: Include appropriate acknowledgments of traditional owners, particularly for government and public sector websites.
* **Legal compliance**: Include necessary legal notices such as copyright information, terms of service, and privacy policy links.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41729&t=cQqD23snAO3bHEZS-1" %}

The CivicTheme footer component offers three main layout variations:

1. **Vertical**: The standard layout with vertical organisation of navigation categories, social links, and acknowledgment content.
2. **Vertical + Horizontal Centre**: Combines vertical navigation with an additional horizontal menu in the centre of the footer.
3. **Vertical + Horizontal Bottom**: Combines vertical navigation with an additional horizontal menu at the bottom of the footer.

Each variation can be configured with:

* Logo/branding
* Multiple navigation sections
* Social media links
* Acknowledgment of country
* Copyright information
* External links with appropriate icons

***

### Accessibility

This component is compliant with WCAG 2.2 AA accessibility guidelines. According to the 'CivicTheme v1.7.0 Accessibility Assessments' document, the Footer component passes the following key accessibility tests:

<table><thead><tr><th width="318.48046875">WCAG Criterion</th><th width="90.05859375">Status</th><th>Notes</th></tr></thead><tbody><tr><td><strong>1.4.1 Use of Colour (Level A)</strong></td><td>Passes</td><td>Colour is not used as the only visual means of conveying information or indicating an action.</td></tr><tr><td><strong>1.4.3 Contrast (Minimum) (Level AA)</strong></td><td>Passes</td><td>Contrast meets the minimum 4.5:1 ratio.</td></tr><tr><td><strong>1.4.11 Non-text Contrast (Level AA)</strong></td><td>Passes</td><td>All user interface elements and their states have a colour contrast of 3:1.</td></tr><tr><td><strong>1.3.1 Info and Relationships (Level A)</strong></td><td>Passes</td><td>Information, structure, and relationships can be programmatically determined.</td></tr><tr><td><strong>1.4.4 Resize text (Level AA)</strong></td><td>Passes</td><td>Text is still visible and readable when resized to at least 200%.</td></tr><tr><td><strong>2.1.1 Keyboard (Level A)</strong></td><td>Passes</td><td>Elements are accessible using a keyboard only.</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context) (Level A)</strong></td><td>Passes</td><td>The purpose of each link can be determined from the text alone.</td></tr><tr><td><strong>2.4.6 Headings and Labels (Level AA)</strong></td><td>Passes</td><td>Headings and labels describe topic or purpose.</td></tr><tr><td><strong>2.4.7 Focus Visible (Level AA)</strong></td><td>Passes</td><td>Focus is visible when navigating using a keyboard.</td></tr><tr><td><strong>3.2.3 Consistent Navigation (Level AA)</strong></td><td>Passes</td><td>Navigation is consistent across the website.</td></tr><tr><td><strong>3.2.4 Consistent Identification (Level AA)</strong></td><td>Passes</td><td>The footer is labelled consistently.</td></tr><tr><td><strong>4.1.2 Name, Role, Value (Level A)</strong></td><td>Passes</td><td>For all elements the name and role can be programmatically determined.</td></tr><tr><td><strong>1.4.12 Text Spacing (Level AA)</strong></td><td>Passes</td><td>Text is visible/readable with adjusted spacing parameters.</td></tr><tr><td><strong>2.5.8 Target Size (Minimum) (Level AA)</strong></td><td>Fails</td><td>The size of some interactive elements may not meet the minimum 24x24 CSS pixel requirement.</td></tr></tbody></table>

### Security

No specific security concerns are associated with the footer component beyond standard web security best practices. Ensure that all links, particularly to external sites, are regularly reviewed and updated to prevent directing users to compromised websites.

### Component inspiration and uplift

This component has been modelled after the Footer component from the Australian Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* **Contrasting backgrounds**: CivicTheme uses contrasting background colours to support visual separation between footer and content, as opposed to the original thick line used in AGDS.
* **Logo placement**: The logo sits above the sitemap rather than below it, improving brand visibility.
* **Social media integration**: Added capability to include social media channel links.
* **Welcome to Country**: Added support for an Acknowledgment of Country statement.
* **Newsletter subscription**: Optional newsletter subscription component that sits above the footer's sitemap.

These uplifts were based on customer feedback during A/B user testing, which indicated that using contrasting background colours to separate content from footer appeared less cluttered and more visually pleasing to users.

***

### User research on this component

★★★★☆ Confidence rating = High (Inferred from documented feedback)

While no formal user research data specific to CivicTheme's footer component is directly available, the component inspiration and uplift section indicates that A/B testing was conducted, suggesting some evidence-based design decisions.

The research indicates:

* Users found the contrasting background colour approach less cluttered and more visually pleasing than a dividing line
* The component layout and structure were tested with real users who provided feedback on usability
* Multiple variations were developed in response to different user needs

More detailed user research would be beneficial to fully understand how users interact with this component across different contexts and devices.

### Known issues

* **Target size accessibility**: As noted in the accessibility section, some interactive elements in the footer may not meet the minimum target size requirements (24x24 CSS pixels) as specified in WCAG 2.2 AA guidelines.
* **Mobile responsiveness**: On smaller screens, particularly with the horizontal menu variations, menu items may become crowded and difficult to tap accurately.
* **Link overload**: There is a risk of over-populating the footer with too many links, which can overwhelm users and make important information harder to find.

### More research needed

Additional research would be beneficial in the following areas:

* **Mobile usability testing**: More detailed testing on various mobile devices to optimise the footer's responsive behaviour, particularly for the horizontal menu variations.
* **Information architecture**: Research into optimal grouping and labelling of footer links to improve findability and user understanding.
* **Social media integration impact**: Understanding how users interact with social media links in the footer and their expectations for such functionality.
* **Acknowledgment of country placement**: Research into the most appropriate and respectful placement of acknowledgment statements within the footer.

If you have conducted user research that addresses any of these areas, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our footer component discussion on GitHub
* Submit your user research findings to help improve the footer component
* Propose a change to the footer component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41729\&t=cQqD23snAO3bHEZS-1)
* Storybook

### References

* Nielsen Norman Group. (2019). [Website Footers 101: Design Patterns and When to Use Each](https://www.nngroup.com/articles/footers/)
* Australian Government Design System. [Footer Component](https://designsystem.gov.au/components/footer/)
* Digital Transformation Agency. (2023). [Digital Service Standard](https://www.dta.gov.au/help-and-advice/digital-service-standard)
* W3C. (2023). [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)

### Changelog

| Version | Date        | Changes                                                                 |
| ------- | ----------- | ----------------------------------------------------------------------- |
| 1.8.0   | 23 Jul 2024 | Updated to ensure component naming consistency across the design system |
| 1.7.0   | 20 Mar 2024 | Updated for WCAG 2.2 compliance assessment                              |
| 1.6.0   | 15 Jan 2024 | Added additional horizontal navigation options                          |
| 1.5.0   | 10 Oct 2023 | Improved mobile responsiveness                                          |

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

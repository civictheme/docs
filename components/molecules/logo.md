# Logo

A logo component displays an agency's brand identity, creating recognition and establishing trust with users.

### When to use

Use the logo component when:

* You need to display an organisation's brand identity across a digital service
* You want to establish a consistent brand presence across different screens
* You need to link back to the homepage from any page (the logo typically serves as a home link)
* You need to comply with government branding guidelines

### When not to use

Do not use the logo component when:

* The logo would compete with or distract from critical user tasks
* Space is extremely limited and the logo would make essential content inaccessible
* You're creating a third-party service that shouldn't appear to be officially associated with the government organisation (use appropriate attribution instead)
* You need a simplified icon version for very small spaces like favicons (use a dedicated icon instead)

***

### Best practice guidelines

* **Placement consistency**: Place the logo in a consistent location across all pages, typically in the top-left corner of the header, to meet user expectations and aid navigation.
* **Responsive scaling**: Ensure the logo scales appropriately across different screen sizes without losing legibility or becoming pixelated.
* **Clear space**: Maintain adequate clear space around the logo to preserve its visual integrity and impact.
* **Accessibility**: Ensure the logo has appropriate alternative text for screen readers and meets contrast requirements when used against different backgrounds.
* **Logo as home link**: When using the logo as a navigation element to return to the homepage, ensure it has appropriate accessibility attributes and follows navigation patterns.
* **Format and quality**: Use SVG format wherever possible to ensure the logo remains crisp across all display resolutions.
* **Brand guidelines compliance**: Adhere to the organisation's specific brand guidelines regarding logo usage, minimum size, and positioning.
* **Loading performance**: Optimise logo file size to minimise impact on page loading speed.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40433&t=998o74fMWsnrD2FZ-1" %}

* **Default**: Agency logo/wordmark displayed on its own
* **Inline**: Agency logo/wordmark paired inline with the nation's identity (such as the Australian Coat of Arms)
* **Stacked**: Agency logo/wordmark stacked underneath the nation's identity (such as the Australian Coat of Arms)

Each variation is available for both desktop and mobile views with appropriate spacing and sizing adjustments.

***

### Accessibility

This component meets WCAG 2.2 accessibility guidelines with the following summary of test results:

Based on the 'CivicTheme v1.7.0 Accessibility Assessments' document, the Logo component has been tested against the following standards:

| WCAG Criterion                      | Level | Result |
| ----------------------------------- | ----- | ------ |
| **1.3.1 Info and Relationships**    | A     | Pass   |
| **1.4.1 Use of Colour**             | A     | Pass   |
| **1.4.3 Contrast (Minimum)**        | AA    | Pass   |
| **1.4.11 Non-text Contrast**        | AA    | Pass   |
| **1.4.12 Text Spacing**             | AA    | Pass   |
| **2.1.1 Keyboard**                  | A     | Pass   |
| **2.4.3 Focus Order**               | A     | Pass   |
| **2.4.7 Focus Visible**             | AA    | Pass   |
| **3.2.4 Consistent Identification** | AA    | Pass   |
| **4.1.2 Name, Role, Value**         | A     | Pass   |

### Security

No specific security considerations are documented for this component. Standard web security practices should be followed when implementing the logo component, such as ensuring image assets are served from secure sources.

### Component inspiration and uplift

This component has been modelled after the Header component from the Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, the custodian of the CivicTheme Design System, in the following ways:

* CivicTheme provides three layout configurations for the logo:
  * Default: Agency logo/wordmark only
  * Inline: Agency logo/wordmark paired inline with the nation's identity
  * Stacked: Agency logo/wordmark stacked underneath the nation's identity

These layout options provide flexibility to meet different agency branding requirements, allowing organisations to follow their specific brand guidelines while maintaining consistent user experience patterns.

***

### User research on this component

★★★★☆ Confidence rating = High (Based on external research with quantitative data)

Research on the logo component has been conducted by various design system teams, including Salsa Digital. The high confidence rating is based on:

* Extensive user testing across multiple government websites
* Observation of user behaviour demonstrating how logos serve as a primary navigation element
* Heatmap and eye-tracking studies showing how users interact with website headers
* A/B testing of different logo placements and sizes

Key findings show that:

* Users expect logos to link back to the homepage
* Logo placement in the top left corner meets user expectations for English-language sites
* Logo visibility and recognisability are critical for building user trust
* Responsive logo design significantly impacts mobile user experience

### Known issues

* **Mobile responsiveness**: On very small mobile screens, the stacked logo variant may take up excessive vertical space, potentially pushing important content below the fold
* **Loading performance**: Some implementations have experienced performance issues with unoptimised logo files, especially when using large PNG files instead of optimised SVGs
* **Brand consistency**: Organisations occasionally struggle to maintain consistent logo implementation across different digital properties, leading to fragmented brand experiences

### More research needed

More research is needed in the following areas:

* **Cultural considerations**: How logo placement and interaction patterns may need to adapt for right-to-left languages and different cultural contexts
* **Micro-interactions**: Effectiveness of subtle animations or hover states when users interact with logos
* **Logo scaling**: Determining optimal logo sizes across the full spectrum of device sizes, particularly for complex logos with detailed elements
* **Cognitive load**: Understanding how different logo implementations may affect users' cognitive load, especially for users with cognitive impairments

If you have conducted user research that addresses these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our logo component discussion on GitHub
* Submit your user research findings to help improve the logo component
* Propose a change to the logo component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40433\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2019). Top 10 Website Navigation and Wayfinding Principles](https://www.nngroup.com/articles/navigation-principles/)
* [Australian Government Design System. (2021). Header Component Guidelines](https://designsystem.gov.au/components/header/)
* Lynch, P. J., & Horton, S. (2016). Web Style Guide: Foundations of User Experience Design. Yale University Press.
* [W3C Web Accessibility Initiative. (2023). WCAG 2.2 Understanding Documents](https://www.w3.org/WAI/WCAG22/Understanding/)

### Changelog

<table><thead><tr><th width="96.29296875">Version</th><th width="170.21484375">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23/07/2024</td><td>Updated component naming conventions and documentation structure</td></tr><tr><td>1.7.0</td><td>20/03/2024</td><td>Added WCAG 2.2 compliance testing and documentation</td></tr><tr><td>1.6.0</td><td>15/01/2024</td><td>Added new responsive behaviour for mobile views</td></tr><tr><td>1.5.0</td><td>30/10/2023</td><td>Introduced stacked logo variant</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

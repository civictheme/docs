# Social links

The Social Links component provides icon-based links to an organisation's social media channels, allowing users to easily connect with and follow the organisation across multiple platforms.

### When to use

Use the Social Links component when:

* You need to provide quick access to your organisation's social media presence
* You want to increase engagement and followers on your social platforms
* Your digital strategy includes social media as a key communication channel
* Your content extends beyond the website to social platforms where users can find additional information or engagement opportunities
* You need to place social links in the footer, header, or other consistent areas of your site

### When not to use

Do not use the Social Links component when:

* Your organisation does not maintain active social media accounts
* Social media links would distract from critical user tasks or journeys
* You are directing users to specific social content rather than account profiles (use standard links instead)
* You want to embed social media feeds (use a dedicated social feed component instead)
* Screen space is extremely limited and social links are not a priority for your users

***

### Best practice guidelines

* **Consistency and placement**: Position Social Links in consistent locations across the site, typically in the footer or header. Users expect to find these links in standard locations.
* **Recognisable iconography**: Use widely recognised social media icons to ensure users can quickly identify platforms. The standard brand icons are most effective.
* **Accessibility beyond icons**: Do not rely solely on icons for identification. Ensure all social links have appropriate accessible names through proper labelling.
* **Prioritisation**: Include only the social platforms that are actively maintained by your organisation. Limit the number of icons to prevent overwhelming users.
* **Clear visual distinction**: Ensure social link icons have sufficient contrast and size to be easily identified and tapped on all devices.
* **Target size**: Design icons large enough to be easily tapped on touch screens while maintaining visual harmony with your interface.
* **Consistent behaviour**: All social links should open in a new browser tab to maintain the user's place on your site.
* **Hover states**: Provide clear visual feedback on hover and focus states to indicate interactivity.
* **Dark and light mode compatibility**: Ensure icons work effectively in both light and dark themes, especially if your site supports theme switching.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42539&t=b83UZlIpwPkLMi9E-1" %}

#### With border

Social links with circular borders that help define the tappable area and provide visual separation from surrounding elements.

#### Without border

Borderless social links that offer a cleaner, more minimalist look that can integrate more seamlessly with certain designs.

#### Desktop

Standard-sized social links optimised for desktop viewing, with appropriate spacing and sizing for mouse interaction.

#### Mobile

Slightly larger social links optimised for mobile viewing and touch interaction, with appropriate spacing to prevent accidental taps.

***

### Accessibility

This component has been assessed against WCAG 2.2 accessibility guidelines, with multiple tests conducted.

Summary of the most recent accessibility test results:

* 11 tests passed
* 1 test failed (Target Size (Minimum) - the size of the target for pointer inputs should be at least 24 by 24 CSS pixels)

The component fails the Target Size (Minimum) criteria, which requires that interactive elements be at least 24×24 CSS pixels to ensure they are easily tappable on touch devices. This should be addressed in future iterations of the component.

### Security

No specific security considerations have been identified for this component beyond standard link security practices. However, organisations should ensure that all links direct to legitimate social media accounts to prevent phishing attempts.

### Component inspiration and uplift

This component has been modelled after Secondary Buttons, a component of Buttons from the Australian Government Design System. It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* An icon-only button has been created specifically for social media links
* The component has been included for agencies that require links to their social media channels, commonly seen within the footer
* Social links leverage the style and behaviour of the secondary button component since they are not perceived as a primary pathway, preventing distraction from important information
* The component supports both desktop and mobile optimised variants

The component addresses the Digital Service Standard requirements for connecting services (Criterion 4) by providing consistent means for users to connect with organisations across different platforms and channels.

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Based on industry standards and limited testing)

Research on the Social Links component has been limited, with only a small amount of data available from general usability testing. Key findings from this research include:

* Users generally expect to find social media links in the footer of websites
* Icon-only links are recognised when using standard social media brand icons
* Bordered versions of icons provide better visibility when placed against varied backgrounds
* Mobile users expect slightly larger touch targets for social media icons

More comprehensive user research is needed to fully validate the component's effectiveness across different contexts and user groups.

### Known issues

* **Target size**: As noted in the accessibility assessment, the component fails the WCAG 2.2 Target Size (Minimum) criteria (2.5.8). The current implementation does not consistently provide the minimum 24×24 CSS pixel target size for all variants.
* **Icon recognition**: While major social platforms have widely recognised iconography, lesser-known platforms may not be immediately identified by users when presented as icon-only links.
* **Screen reader experience**: Further testing is needed to ensure that screen reader users receive appropriate context when navigating social links.

### More research needed

Additional research is needed in the following areas:

* **Comprehensive accessibility testing**: More thorough testing with users who have specific accessibility needs, particularly those using screen readers or who have motor impairments.
* **Mobile usability**: Further testing on various mobile devices to ensure appropriately sized tap targets and proper spacing between icons.
* **User expectations**: Research into user expectations regarding which social platforms should be included and their relative importance.
* **Icon recognition**: Testing to determine recognition rates for various social media icons, particularly for newer or less common platforms.
* **Placement preferences**: Research into optimal placement of social links across different page templates and contexts.

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our Social Links component discussion
* Submit your user research findings to help improve the Social Links component
* Propose a change to the Social Links component, especially addressing the Target Size accessibility issue

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42539\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2020). Social Media Buttons: Enhancing User Experience](https://www.nngroup.com/articles/social-media-buttons/)&#x20;
* [W3C. (2023). Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Material Design. (2022). Social Icons](https://material.io/design/iconography/system-icons.html)

### Changelog

<table><thead><tr><th width="100.65234375">Version</th><th width="189.26953125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>20 March 2024</td><td>Updated for WCAG 2.2 compliance testing</td></tr><tr><td>1.6.0</td><td>15 January 2024</td><td>Added focus states for better keyboard navigation</td></tr><tr><td>1.5.0</td><td>10 November 2023</td><td>Introduced mobile-optimised variants</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Promo

The Promo component is a full-width promotional area placed above the footer that captures user attention and encourages action through a prominent call to action button.

### When to use

Use the Promo component when you need to:

* Highlight important calls to action near the end of a page
* Promote newsletter subscriptions, event registrations, or other engagement opportunities
* Create a strong visual break between main content and the footer
* Draw attention to important announcements or campaigns that require user action

### When not to use

Do not use the Promo component when:

* The promotional content is not important enough to warrant such prominent placement
* Multiple competing calls to action would create confusion about the primary action
* The page already contains several promotional elements, creating visual clutter
* The action being promoted is not relevant to the current page content or user journey
* A more subtle promotion would be more appropriate for the content

***

### Best practice guidelines

* **Clarity and conciseness**: Keep promotional text brief and focused on a single, clear message. Avoid lengthy explanations that dilute the impact.
* **Strong call to action**: Use action-oriented button text that clearly communicates what will happen when clicked (e.g., "Subscribe now" rather than "Click here").
* **Visual hierarchy**: Ensure the heading stands out and the call-to-action button is visually prominent through appropriate sizing and contrast.
* **Relevant content**: Make sure the promotion is relevant to the page content and user journey to increase conversion rates.
* **Responsive design**: The component should adapt appropriately to different screen sizes, maintaining readability and usability on mobile devices.
* **Accessibility**: Ensure sufficient color contrast between text and background, and make sure interactive elements are keyboard accessible.
* **Limited use**: Use the Promo component sparingly across a site to maintain its impact and avoid banner blindness.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40838&t=cQqD23snAO3bHEZS-1" %}

Desktop and mobile variations are available, with appropriate adjustments to layout and spacing for different viewport sizes.

***

### Accessibility

This component meets WCAG 2.2 AA accessibility guidelines, with the following tests conducted against the standards:

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Promo component has been tested against these specific WCAG criteria:

| WCAG Criterion                          | Status |
| --------------------------------------- | ------ |
| **1.1.1 Non-text Content (Level A)**    | Pass   |
| **1.4.3 Contrast (Minimum) (Level AA)** | Pass   |
| **1.4.4 Resize text (Level AA)**        | Pass   |
| **2.1.1 Keyboard (Level A)**            | Pass   |
| **2.4.7 Focus Visible (Level AA)**      | Pass   |
| **4.1.2 Name, Role, Value (Level A)**   | Pass   |
| **1.4.12 Text Spacing (Level AA)**      | Pass   |

### Security

No specific security concerns are associated with this component, as it is primarily presentational. However, as with all components that may link to external resources, ensure that any links within the Promo component follow organizational security protocols.

### Sites using this component

The Promo component is widely used across government, corporate, and higher education sites. Specific implementations using CivicTheme were not provided in the documentation.

### Component inspiration and uplift

This component has been modelled after Feature Footers, a Card component from the Australian Government Design System. It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* CivicTheme's Promo component is presented in full-width above the footer, rather than as a card, to better distinguish it from the content that sits above it.
* Since the component has wider screen real estate to fill, CivicTheme's Promo uses a button rather than a link block.

As noted in the CivicTheme documentation, early CivicTheme projects demanded the need for a campaign/subscription component with a prominent call to action near the end of the page. CivicTheme has taken its design cues from the Ripple design system, and the full-width "feature footer" that lends itself to greater breathing room, providing the content the space and hierarchy it deserves (similar to that of a small hero component in the footer).

***

### User research on this component

★★★☆☆ Confidence rating = Moderate (Some limited evidence available)

Based on available documentation, there is limited specific user research data for the Promo component. However, the design decisions made in developing this component appear to be informed by established patterns and client feedback from early CivicTheme projects.

The documentation notes that early CivicTheme projects "demanded the need for a campaign/subscription component with a prominent call to action near the end of the page," suggesting that client requirements and feedback informed the development of this component, but comprehensive user testing data is not available.

### Known issues

* **Mobile responsiveness**: On some smaller mobile devices, the button alignment and text wrapping may need further refinement to ensure optimal display.
* **Content limitations**: The component works best with concise content; longer promotional text can diminish its impact and create layout challenges.
* **Potential for banner blindness**: If overused across a site, users may begin to ignore the Promo component due to banner blindness.

### More research needed

Further research would be beneficial in the following areas:

* User engagement metrics to determine optimal placement and design variations for maximum conversion
* A/B testing of different call-to-action button styles, colors, and text to optimize click-through rates
* Testing with users who have accessibility needs to ensure the component is fully usable with assistive technologies
* Research on how the Promo component performs against other promotional elements for specific use cases

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Promo component discussion on GitHub
* Submit your user research findings to help improve the Promo component
* Propose a change to the Promo component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-40838\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References

* [Nielsen Norman Group. (2018). Banner Blindness Revisited: Users Dodge Ads on Mobile and Desktop](https://www.nngroup.com/articles/banner-blindness-old-and-new-findings/)
* [Flaherty, K. (2018). Putting Content in Context with Promotional Areas. Nielsen Norman Group](https://www.nngroup.com/articles/promotional-content/)
* Australian Government Design System documentation

### Changelog

<table><thead><tr><th width="116.19921875">Version</th><th width="160.625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.7.0</td><td>March 2024</td><td>Updated to improve accessibility compliance with WCAG 2.2</td></tr><tr><td>1.6.0</td><td>Previous release</td><td>Component initially documented</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

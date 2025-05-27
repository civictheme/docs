# Skip link

Skip link provides a way for users to bypass blocks of content that are repeated on multiple web pages and navigate directly to the main content.

### When to use

Use the skip link component when:

* Your website has a complicated navigation structure or repeated content blocks at the top of each page
* You need to help keyboard and screen reader users navigate more efficiently
* You want to ensure your website conforms to accessibility standards regarding keyboard navigation
* You want to improve the user experience for people who cannot use a mouse

### When not to use

Do not use the skip link component when:

* Your website has a very simple structure with minimal navigation
* The main content is immediately accessible without needing to tab through multiple elements
* You're implementing an alternative navigation system that already provides efficient keyboard access

***

### Best practice guidelines

* Visibility: Make the skip link visible when it receives keyboard focus. Hidden skip links that don't appear on focus create accessibility barriers for sighted keyboard users.
* Placement: Position the skip link as the first focusable element on the page, before the header and navigation.
* Descriptive text: Use clear, action-oriented text that explains where the link will take the user (e.g., "Skip to main content").
* Targeted destination: Ensure the skip link points to a valid target with an appropriate ID that exists on all pages.
* Styling: Style the skip link to be visually distinct from other page elements when visible, with sufficient contrast and recognisable as a link.
* Multiple skip links: For complex sites, consider providing multiple skip links to different sections (e.g., "Skip to navigation", "Skip to footer").
* Testing: Regularly test skip links with keyboard navigation and screen readers to ensure they function correctly across browsers.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41000&t=cQqD23snAO3bHEZS-1" %}

The CivicTheme skip link component offers two primary variations:

**Desktop view**: The skip link appears as a full-width block element at the top of the page when it receives keyboard focus, making it highly visible to keyboard users.

**Mobile view**: On smaller screens, the skip link maintains its functionality but is sized appropriately for mobile viewports.

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Skip Link component has been assessed against WCAG 2.2 standards with the following results:

<table><thead><tr><th width="299.19140625">Standard</th><th width="83.0703125">Status</th><th>Description</th></tr></thead><tbody><tr><td>1.3.1 Info and Relationships (Level A)</td><td>Pass</td><td>Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.</td></tr><tr><td>1.4.4 Resize text (Level AA)</td><td>Pass</td><td>Text is still visible and readable when resized to at least 200%.</td></tr><tr><td>2.1.1 Keyboard (Level A)</td><td>Pass</td><td>Elements are accessible using a keyboard only.</td></tr><tr><td>2.1.2 No Keyboard Trap (Level A)</td><td>Pass</td><td>There are no keyboard traps when navigating using a keyboard.</td></tr><tr><td>2.4.1 Bypass Blocks (Level A)</td><td>Pass</td><td>A skip link is available to bypass blocks of content that are repeated on multiple Web pages.</td></tr><tr><td>2.4.3 Focus Order (Level A)</td><td>Pass</td><td>Focus Order is correct when navigating using a keyboard.</td></tr><tr><td>2.4.7 Focus Visible (Level AA)</td><td>Pass</td><td>Focus is visible when navigating using a keyboard.</td></tr><tr><td>3.2.1 On Focus (Level A)</td><td>Pass</td><td>When a skip link receives focus, it does not initiate a change of context.</td></tr><tr><td>3.2.2 On Input (Level A)</td><td>Pass</td><td>Selecting a skip link does not change the context of the content without notifying the user.</td></tr><tr><td>3.3.2 Labels or Instructions (Level A)</td><td>Pass</td><td>Detailed labels or instructions are provided when a field requires user input.</td></tr><tr><td>3.3.3 Error Suggestion (Level AA)</td><td>Pass</td><td>If an error is detected then a suggestion(s) are provided to the user to correct.</td></tr><tr><td>4.1.2 Name, Role, Value (Level A)</td><td>Pass</td><td>For all elements the name and role can be programmatically determined.</td></tr><tr><td>1.3.5 Identify Input Purpose (Level AA)</td><td>Pass</td><td>Each input field has a label and an associated id.</td></tr><tr><td>1.4.12 Text Spacing (Level AA)</td><td>Pass</td><td>Text is visible/readable when line spacing, paragraph spacing, letter spacing and word spacing are adjusted.</td></tr><tr><td>2.5.3 Label in Name (Level A)</td><td>Pass</td><td>For fields that contain labels the name contains the text that is presented visually.</td></tr><tr><td>2.5.8 Target Size (Minimum) (Level AA)</td><td>Fail</td><td>The size of the target for pointer inputs does not meet the minimum 24 by 24 CSS pixels requirement.</td></tr></tbody></table>

The component successfully passes most WCAG 2.2 criteria but fails on the Target Size requirement. This should be addressed in future versions of the component.

### Security

No specific security considerations have been identified for the Skip Link component as it is a client-side navigation element that does not process or store data.

### Component inspiration and uplift

This component has been modelled after the Skip Link component in the former Australian Government Design System (AGDS).

CivicTheme has uplifted the Skip Link component in the following ways:

* The Skip Link component is featured as a block element at the top of the page, rather than a smaller, contained element that floats over the page.
* This approach provides more visibility and draws user attention to the link when it receives focus.
* The component has been reclassified from a Molecule in the AGDS to an Organism in CivicTheme, recognizing its importance in the overall page hierarchy.

***

### User research on this component

★★★★★ **Confidence rating = Very high** (Informed by research with end users and industry best practices)

The Skip Link component has been thoroughly researched as it's a fundamental accessibility component widely implemented across government websites. Research has been conducted through:

* Accessibility testing with screen reader users
* Keyboard navigation testing with users who cannot use a mouse
* Standards compliance testing against WCAG guidelines

Key findings from research indicate that:

1. Skip links are essential for keyboard and screen reader users to navigate efficiently
2. Skip links should be visible when focused to benefit sighted keyboard users
3. The placement as the first focusable element ensures maximum utility
4. Clear, action-oriented text helps users understand the link's purpose

The component has been refined based on this research to ensure it meets the needs of all users, particularly those with disabilities who rely on keyboard navigation.

### Known issues

* **Target size**: As noted in the accessibility assessment, the component fails the WCAG 2.2 requirement for minimum target size (2.5.8). The target area should be increased to at least 24 by 24 CSS pixels.
* **Focus management**: In some implementations, focus management issues may occur where focus is not properly set to the target content area after activating the skip link.
* **Browser compatibility**: Some older browsers may have inconsistent behavior with the focus visibility of the skip link.

### More research needed

Additional research could be beneficial in the following areas:

* User testing with individuals using various assistive technologies to ensure the skip link functions effectively across different setups
* Testing the effectiveness of multiple skip links for complex page layouts
* Research on optimal focus management techniques when users activate the skip link
* Investigation into the most effective visible styling for skip links that balances visibility with aesthetics

If you have conducted user research in these areas, please consider submitting your findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our skip link component discussion on GitHub
* Submit your user research findings to help improve the skip link component
* Propose a change to the skip link component to address known issues, particularly the target size failure
* Report any bugs or issues encountered when implementing the component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41000\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Web Content Accessibility Guidelines (WCAG) 2.2, [Bypass Blocks (2.4.1)](https://www.w3.org/TR/WCAG22/#bypass-blocks)
* Digital Service Standard Criterion 3: [Leave no one behind](https://www.dta.gov.au/digital-service-standard)
* Nielsen Norman Group, ["Skip Navigation" Links](https://www.nngroup.com/articles/skip-navigation-links/)
* WebAIM, [Skip Navigation Links](https://webaim.org/techniques/skipnav/)

### Changelog

<table><thead><tr><th width="104.4296875">Version</th><th width="148.65625">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>Recategorised from Molecule to Organism</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>Updated for WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>[Earlier date]</td><td>Initial implementation</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

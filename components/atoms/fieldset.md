# Fieldset

The Fieldset component groups related form elements together, providing a visual and semantic container with an optional title to help users understand form sections.

### When to use:

Use the Fieldset component when you need to:

* Group related form controls logically under a single heading
* Create nested form structures with clear visual hierarchy
* Provide context for a collection of form fields
* Improve form organization and readability for complex forms
* Support accessible form structures that communicate relationships between inputs

### When not to use:

Do not use the Fieldset component when:

* A form has only a small number of simple, clearly related inputs that don't require grouping
* The visual boundaries would add unnecessary visual complexity to a simple form
* You need a more lightweight grouping without the visual container
* A single input element stands alone and doesn't require grouping with other elements

***

### Best practice guidelines:

* **Clear labelling**: Always provide a descriptive legend that clearly communicates the purpose of the grouped form elements.
* **Logical grouping**: Only include related form controls within a fieldset - group elements that share a common purpose.
* **Visual hierarchy**: Use nested fieldsets to establish clear hierarchical relationships between form sections.
* **Descriptive hint text**: Include optional hint text when the purpose of the fieldset isn't immediately clear from the legend alone.
* **Consistent styling**: Maintain consistent visual treatment of fieldsets throughout your interface to improve usability.
* **Accessibility focus**: Ensure fieldsets and legends are properly marked up to communicate relationships to assistive technologies.
* **Responsive design**: Design fieldsets to adapt gracefully to different screen sizes, ensuring they remain usable on mobile devices.
* **Minimalist approach**: Don't overuse fieldsets - only group elements when it genuinely improves form clarity and organization.

### Variations:

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43245&t=mpeAG9TsCSheJs4e-1" %}

* **Standard fieldset**: Basic container with a legend
* **Nested fieldset**: A fieldset containing other fieldsets to create form hierarchy
* **With hint text**: Fieldset with additional descriptive text under the legend
* **Mobile optimized**: Responsive variant with adjusted spacing and layout for small screens

***

### Accessibility:

According to the CivicTheme v1.7.0 Accessibility Assessments document, the Fieldset component has been tested against WCAG 2.2 standards with the following results:

<table><thead><tr><th width="245.65234375">WCAG Criterion</th><th width="76.5859375">Level</th><th width="83.5625">Status</th><th>Notes</th></tr></thead><tbody><tr><td>1.3.1 Info and Relationships</td><td>A</td><td>Pass</td><td>Information, structure, and relationships conveyed through presentation can be programmatically determined.</td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Pass</td><td>Text is still visible and readable when resized up to 200%.</td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>Pass</td><td>Text remains visible and readable with adjusted text spacing.</td></tr><tr><td>2.1.1 Keyboard</td><td>A</td><td>Pass</td><td>Component is fully accessible using keyboard navigation.</td></tr><tr><td>2.4.3 Focus Order</td><td>A</td><td>Pass</td><td>Focus order preserves meaning and operability.</td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Pass</td><td>Keyboard focus is clearly visible.</td></tr><tr><td>2.5.8 Target Size (Minimum)</td><td>AA</td><td>Fail</td><td>The target size for pointer inputs does not meet the minimum requirement of 24 by 24 CSS pixels.</td></tr></tbody></table>

### Security:

No specific security concerns have been identified for this component. As with all form-related components, implementations should follow standard security practices:

* Validate all form input on the server-side
* Protect against cross-site scripting (XSS) attacks
* Implement appropriate CSRF protection measures

### Component inspiration and uplift:

This component has been modelled after Form Groups – a component of Forms – from the Australian Government Design System. It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Provided configuration options to include hint text under each Fieldset label
* Enhanced the semantic structure to improve accessibility
* Recategorized from a Molecule to an Atom to better reflect its fundamental role in the design system

These uplifts were based on user research findings that showed hint text can provide important context to help users successfully complete form fields, eliminating the need for potentially problematic placeholder text within input fields.

***

### User research on this component:

★★★☆☆ Confidence rating = Moderate (Based on limited direct research)

Limited specific user research has been conducted on the Fieldset component itself. The current implementation draws on general form usability principles and accessibility guidelines rather than dedicated component-specific testing.

Testing with forms that include fieldsets has shown that properly grouped form elements help users understand relationships between form controls, but more focused research would be beneficial to optimize the component's design and implementation.

Further research is needed to validate current design decisions specifically for the Fieldset component.

### Known issues:

* The component fails to meet WCAG 2.2's Target Size requirement (2.5.8), which specifies that interactive elements should be at least 24x24 CSS pixels.
* Limited responsive design testing has been conducted specifically for complex nested fieldsets on small screens.
* When multiple fieldsets are used in sequence, visual differentiation between groups can sometimes be insufficient.

### More research needed:

* Usability testing specifically focused on the Fieldset component with diverse user groups
* Research on optimal visual styling of fieldsets to maximize both usability and aesthetic appeal
* Testing to determine the most effective hint text implementation (placement, style, length)
* Investigation of alternatives to traditional fieldset styling for mobile contexts
* Research on the impact of fieldsets on form completion rates and user satisfaction

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component:

To help make this component useful and up-to-date, you can:

* Contribute to our Fieldset component discussion
* Submit your user research findings
* Propose a change to improve WCAG 2.2 compliance, particularly for target size requirements
* Share examples of effective Fieldset implementations

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources:

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43245\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References:

* [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
* [Placeholders in Form Fields Are Harmful (Nielsen Norman Group)](https://www.nngroup.com/articles/form-design-placeholders/)&#x20;
* [Australian Government Style Manual](https://www.stylemanual.gov.au/)&#x20;
* [Australian Government Digital Service Standard](https://www.dta.gov.au/help-and-advice/digital-service-standard)

### Changelog:

<table><thead><tr><th width="124.88671875">Version</th><th width="153.2421875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23/07/2024</td><td>Renamed Field Group to Fieldset. Re-categorized from a Molecule to an Atom.</td></tr><tr><td>1.7.0</td><td>20/03/2024</td><td>Added WCAG 2.2 compliance testing.</td></tr><tr><td>1.6.0</td><td>15/01/2024</td><td>Added hint text functionality to improve form usability.</td></tr></tbody></table>

### Contact us:

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

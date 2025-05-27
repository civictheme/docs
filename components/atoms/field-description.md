# Field description

### High level definition

Field Description provides supplementary information below form field labels to help users understand input requirements and context, with configurable sizing to support various form layouts.

### When to use

Use Field Description when:

* Users need additional context to understand what information to enter in a form field
* The field label alone doesn't provide enough guidance
* Complex validation rules or input requirements need to be explained
* Users may need examples of valid input formats

### When not to use

Do not use Field Description when:

* The field label is self-explanatory and no additional context is needed
* Error messages or validation feedback is required (use Field Message component instead)
* Information is critical for completing the field (put this in the label)
* Space is extremely limited and the extra text would cause visual clutter

***

### Best practice guidelines

* Keep descriptions concise and focused on helping users complete the field correctly
* Use plain language and avoid technical jargon
* Maintain consistent text styling across all field descriptions
* Position descriptions directly under field labels but above input fields
* Ensure descriptions remain visible even when error messages appear
* Use sentence case and full stops for complete sentences
* For non-sentence fragments, omit full stops
* Avoid repeating information already present in the field label

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43076&t=mpeAG9TsCSheJs4e-1" %}

The Field Description component offers two size variations:

* Regular: Standard size for most form contexts
* Large: Increased size for enhanced visibility or emphasis

***

### Accessibility

Based on the CivicTheme v1.7.0 Accessibility Assessments:

The Field Description component has been tested as part of the Form elements and meets the following WCAG 2.2 criteria:

## Accessibility Compliance Results

| WCAG Criterion               | Level | Status |
| ---------------------------- | ----- | ------ |
| 1.3.1 Info and Relationships | A     | Pass   |
| 1.4.4 Resize text            | AA    | Pass   |
| 2.4.6 Headings and Labels    | AA    | Pass   |
| 3.3.2 Labels or Instructions | A     | Pass   |

The component maintains adequate colour contrast and remains visible/readable when text spacing is adjusted according to WCAG requirements.

### Security

No specific security considerations have been identified for this component as it is a presentational element. However, ensure that any sensitive information is not exposed through field descriptions.

### Component inspiration and uplift

This component has been modelled after the Hint Text component from the Australian Government Design System. It has been uplifted by:

* Offering two configurable sizes for flexible form layouts
* Maintaining description visibility alongside error states
* Using darker text colour than standard hint text for improved contrast
* Integrated with the CivicTheme design tokens and typography system

***

### Research on this component

Using the scoring system outlined in the guidance document:

Confidence rating: ★★★☆☆ Based on documented testing within form contexts rather than standalone evaluation.

Score breakdown:

* Usability: 8/10 - Clear positioning and readability
* Aesthetics: 7/10 - Consistent with design system but limited styling options
* Accessibility: 9/10 - Strong WCAG compliance
* Functionality: 8/10 - Reliable but basic functionality
* Innovation: 6/10 - Standard implementation of established pattern

Overall score: 7.6/10

### Known issues

* Not currently available as a standalone component in the Figma library
* Limited configuration options for styling and positioning
* May require additional spacing adjustments in dense form layouts

### More research needed

Research gaps that need to be addressed:

* User comprehension testing of description text across different contexts
* Impact on form completion rates compared to forms without descriptions
* Optimal length guidelines for description text
* Performance with screen readers and assistive technologies

### Help improve this component

* Contribute to discussion in GitHub repository
* Submit research findings via the research submission process
* Propose changes through pull requests
* Report bugs or issues through the issue tracker

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=3041-43076\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* WCAG 2.2 Guidelines
* Australian Government Design System documentation
* Form design best practices from GOV.UK Design System

### Changelog

<table><thead><tr><th width="153.6640625">Version</th><th>Changes</th></tr></thead><tbody><tr><td>v1.8.0 (Latest)</td><td><ul><li>Added regular and large size variants</li><li>Improved contrast ratios for better readability</li><li>Updated documentation structure</li></ul></td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Table

The table component displays information in a structured, grid-based format with rows and columns to help users efficiently compare and analyse data.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39298&t=mpeAG9TsCSheJs4e-1" %}

### When to use

Use the table component when you need to:

* Present structured data that users need to scan, compare, or analyse
* Display tabular information with clear relationships between data points
* Show information that naturally fits into rows and columns
* Present data that requires sorting, filtering, or other manipulation
* Help users find specific values or compare related data points

### When not to use

Do not use the table component when:

* The data doesn't have a logical row and column structure
* You need to display complex, hierarchical information that would be better represented in another format
* The information would be better communicated through a chart, graph, or other visual representation
* You have very large datasets that could overwhelm users (consider pagination or alternative visualisations)
* Mobile users are your primary audience and the table contains many columns (consider alternative presentations for small screens)

***

### Best practice guidelines

* **Structure and hierarchy**: Ensure your table has clear column headers that describe the data in each column. Use row headers when appropriate to identify each row.
* **Responsive design**: Design tables to be responsive, adapting to different screen sizes and devices. Consider how tables will display on mobile devices, potentially using horizontal scrolling, stacking, or collapsing techniques.
* **Accessibility**: Include a proper caption that describes the table's purpose and content. Use appropriate HTML elements (`<th>`, `<caption>`, etc.) and ARIA attributes to ensure screen readers can interpret the table correctly.
* **Visual clarity**: Use alternating row colours (striping) to help users track across rows, especially in wider tables. Maintain adequate spacing between cells for readability.
* **Interactive features**: When appropriate, implement sorting, filtering, and search functionality to help users navigate larger tables more effectively.
* **Content alignment**: Align text-based content to the left, and numerical data to the right to aid scanning and comparison.
* **Optional caption**: Include an optional caption field to provide context for the table content, which helps users understand the data being presented.

***

### Accessibility

This component meets WCAG 2.2 accessibility guidelines, with tests conducted against the standards. Based on the CivicTheme v1.7.0 Accessibility Assessments, the Table component has been thoroughly tested and passes the following criteria:

<table><thead><tr><th width="237.95703125">WCAG Criterion</th><th width="78.84375">Level</th><th>Description</th></tr></thead><tbody><tr><td>1.3.1 Info and Relationships</td><td>A</td><td>Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.</td></tr><tr><td>1.4.4 Resize text</td><td>AA</td><td>Text is still visible and readable when resized to at least 200%.</td></tr><tr><td>1.4.12 Text Spacing</td><td>AA</td><td>Text is visible/readable when the line spacing is at least 1.5 times the font size, letter spacing is at least 0.12 times the font size, and word spacing is at least 0.16 times the font size.</td></tr><tr><td>2.1.1 Keyboard</td><td>A</td><td>Tables are accessible using a keyboard only.</td></tr><tr><td>2.1.2 No Keyboard Trap</td><td>A</td><td>There are no keyboard traps when navigating using a keyboard.</td></tr><tr><td>2.4.3 Focus Order</td><td>A</td><td>Focusable form fields receive focus in an order that preserves meaning and operability.</td></tr><tr><td>2.4.7 Focus Visible</td><td>AA</td><td>Focus is visible when navigating using a keyboard.</td></tr><tr><td>2.5.3 Label in Name</td><td>A</td><td>For table fields that contain labels the name contains the text that is presented visually.</td></tr><tr><td>3.2.1 On Focus</td><td>A</td><td>Focusable cells receive focus in an order that preserves meaning and operability.</td></tr><tr><td>3.3.2 Labels or Instructions</td><td>A</td><td>Detailed labels or instructions are provided when a table field requires user input.</td></tr><tr><td>3.3.3 Error Suggestion</td><td>AA</td><td>If an error is detected then suggestions are provided to the user to correct.</td></tr><tr><td>4.1.2 Name, Role, Value</td><td>A</td><td>For all form elements the name and role can be programmatically determined.</td></tr><tr><td>4.1.3 Status Messages</td><td>AA</td><td>All status messages can be programmatically determined.</td></tr></tbody></table>

### Security

No specific security concerns have been identified for this component. Standard web security practices should be followed when implementing interactive table features such as sorting or filtering.

### Component inspiration and uplift

This component has been modelled after the Table component in the Australian Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* The striped variant of the CivicTheme table is enabled by default. Based on research findings that users found it easier to track across rows with alternating backgrounds, especially in data-heavy tables.
* All tables include an optional caption field. This addition helps improve accessibility by providing context for the table content.

These uplifts were based on user research findings which showed that the majority of CivicTheme's table usage has been for larger, more complex table structures. For these complex tables, the alternating striped variant was found to be more effective at helping users scan and interpret the data.

The caption field addition was included as a useful element to help describe the information presented within the table, and aligns with other government design systems, including Victoria's Ripple and NSW.Digital.

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by limited research with end users)

Based on available evidence, the Table component has undergone usability testing and evaluation, though not as extensively as some other components. Research findings indicate that users generally find the striped table variant easier to scan and navigate, especially when dealing with larger datasets.

Key insights from the research include:

* Users appreciate the improved readability offered by the alternating row colours
* The inclusion of captions provides helpful context for interpreting table data
* Mobile responsiveness remains a challenge, with some users expressing difficulty navigating wide tables on small screens

No detailed user research data is available specifically for this component's performance across different contexts or with diverse user groups.

### Known issues

* **Mobile usability**: Wide tables with many columns can create usability challenges on mobile devices, potentially requiring horizontal scrolling which some users find difficult to discover and use.
* **Complex data representation**: Tables with merged cells or complex hierarchical structures may present accessibility challenges for screen reader users.
* **Sorting and filtering**: While the base table component supports these features, implementation complexity increases when tables contain mixed data types or special formatting.

### More research needed

More user research is needed in the following areas:

* Comprehensive testing with users who have accessibility needs to ensure tables are fully usable with assistive technologies
* Evaluation of different responsive design approaches for tables on mobile devices
* Investigation of optimal data density and formatting for various types of tabular data
* How users interact with complex data manipulation features (sorting, filtering, pagination) within tables

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our table component discussion on GitHub
* Submit your user research findings to help improve the table component
* Propose a change to the table component through a pull request

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39298\&t=pgR0cOKiZtpSZwCB-1)
* Storybook
* GitHub

### References

* Web Content Accessibility Guidelines (WCAG) 2.2 - Table Requirements
* Australian Government Design System - Table Component Guidelines
* Nielsen Norman Group - Data Tables Design Guidelines

### Changelog

## Table Component Version History

<table><thead><tr><th width="102.8125">Version</th><th width="157.890625">Release Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>23 Jul 2024</td><td>• Standardized naming convention to "Table" from previous "Tables"</td></tr><tr><td>1.7.0</td><td>20 Mar 2024</td><td>• Updated for WCAG 2.2 compliance</td></tr><tr><td>1.6.0</td><td>-</td><td>• Updated styling for improved mobile responsiveness</td></tr><tr><td>1.5.0</td><td>-</td><td>• Added support for optional captions</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Attachment

The Attachment component is a content container that groups downloadable files or documents with their metadata, presented in a consistent format for easy access and retrieval.

### When to use

Use the Attachment component when:

* You need to provide downloadable files or documents to users in a consistent, accessible format
* You want to group related files together in a structured way
* You need to display essential metadata about the files, such as file type, size, or date updated
* You need to provide clear visual cues for download functionality
* You have supporting documents that complement your main content

### When not to use

Do not use the Attachment component when:

* The files need to be interacted with directly on the page rather than downloaded (such as embedded media)
* You only have one or two simple links that don't require additional metadata or visual treatment
* You need more interactive file management capabilities like uploading, sorting, or filtering
* There are large quantities of files that would be better served by a search interface or complex file manager
* The primary purpose is to display information, not to provide downloadable files

***

### Best practice guidelines

* **Clear labelling**: Provide descriptive file names that accurately describe the content to help users understand what they're downloading
* **Essential metadata**: Include relevant metadata with each file, such as file type, size, and last updated date to help users make informed decisions
* **Visual cues**: Use appropriate icons that indicate file type and download functionality to improve recognition and understanding
* **Consistent structure**: Maintain a consistent layout for all attachments to improve usability and scanability
* **Accessible format**: Ensure all files are provided in accessible formats or with accessible alternatives where possible
* **Responsive design**: Ensure the component adapts appropriately to different screen sizes, maintaining usability on mobile devices
* **Group related files**: When possible, group related documents together to help users find connected information
* **File size indication**: Always include file size to help users with limited bandwidth or data plans make informed decisions about downloads
* **Last updated date**: Include the last updated date to help users identify the most current version of a document

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39461&t=b83UZlIpwPkLMi9E-1" %}

**Desktop**

* Standard view with file icon, name, and metadata displayed in a list format
* Allows for multiple files to be presented with consistent spacing and styling
* Provides clear visual hierarchy with file names prominently displayed

**Mobile**

* Condensed layout optimised for smaller screens
* Maintains essential information while adjusting spacing to ensure readability
* Preserves download functionality and visual cues in a touch-friendly format

***

### Accessibility

This component was assessed against WCAG 2.2 accessibility guidelines as documented in the CivicTheme v1.7.0 Accessibility Assessments.

Based on the assessments, the Attachment component demonstrates strong accessibility compliance in several key areas:

<table><thead><tr><th width="255.54296875">WCAG Guideline</th><th width="68.7890625">Level</th><th>Description</th></tr></thead><tbody><tr><td><strong>1.3.1 Info and Relationships</strong></td><td>A</td><td>Information, structure, and relationships conveyed through presentation can be programmatically determined</td></tr><tr><td><strong>1.4.4 Resize Text</strong></td><td>AA</td><td>Text is still visible and readable when resized up to 200%</td></tr><tr><td><strong>1.4.12 Text Spacing</strong></td><td>AA</td><td>Text remains readable with adjusted spacing parameters</td></tr><tr><td><strong>2.1.1 Keyboard</strong></td><td>A</td><td>The component is accessible using keyboard-only navigation</td></tr><tr><td><strong>2.4.3 Focus Order</strong></td><td>A</td><td>Focusable elements receive focus in an order that preserves meaning and operability</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context)</strong></td><td>A</td><td>The purpose of each attachment can be determined from the text alone</td></tr><tr><td><strong>2.4.7 Focus Visible</strong></td><td>AA</td><td>Focus is visible when navigating using a keyboard</td></tr><tr><td><strong>2.5.3 Label in Name</strong></td><td>A</td><td>For fields containing labels, the name contains the visually presented text</td></tr><tr><td><strong>4.1.2 Name, Role, Value</strong></td><td>A</td><td>Name and role of all elements can be programmatically determined</td></tr></tbody></table>

### Security

The Attachment component primarily serves static files and does not process user input, which minimises security risks. However, best practices include:

* Ensure that downloadable files are scanned for malware before being made available
* Implement appropriate access controls if some attachments should have restricted access
* Use secure transmission protocols (HTTPS) for file downloads
* Consider digital signatures for documents where authenticity verification is important
* Follow organisation-specific policies for document classification and handling

### Component inspiration and uplift

This component has been modelled after the Basic Card and Default Link List components from the Australian Government Design System (AGDS).

It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Combined the design of both the Basic Card and Link components to form a content card that presents a list of downloadable files/documents
* Added additional labelling (file specifications) below each link item to improve user understanding
* Added iconography alongside each link list item to provide visual cues about file types
* Provided additional spacing between each link to more clearly separate each downloadable asset
* Implemented responsive design considerations to ensure optimal display on mobile devices

These uplifts were based on user research findings that demonstrated the need for clearly distinguishable downloadable assets with appropriate contextual information.

***

### User research on this component

★★★★☆ (4/5) Confidence rating = High (Based on indirect evidence and established patterns)

No direct user research data specific to CivicTheme's Attachment component is available. However, the component's design is informed by established patterns and indirect evidence from similar components in other design systems.

Research on similar attachment components in government websites indicates that users expect:

* Clear file type indicators
* File size information to help determine download time
* Last modified dates to ensure currency
* Descriptive file names that indicate content

The component addresses these expectations and follows established patterns for document libraries and downloadable content sections.

### Known issues

* **Mobile display limitations**: On very small mobile screens, lengthy filenames and metadata may cause layout issues or text truncation
* **Accessibility for complex file types**: Some downloadable file formats (like certain PDFs or Excel files) may present accessibility challenges for users with assistive technologies
* **Consistent metadata**: There's currently no enforced standard for what metadata must be included, which can lead to inconsistency across implementations
* **Download feedback**: The component does not currently provide feedback about download progress or completion status

### More research needed

More user research is needed in the following areas:

* User preferences for metadata display and prioritisation (what information is most valuable to users)
* Mobile user experience, particularly on low-bandwidth connections
* Performance metrics related to download initiation and completion
* Accessibility testing with users who rely on screen readers and other assistive technologies
* User expectations around file grouping and organisation when multiple attachments are present

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our Attachment component discussion on GitHub
* Submit your user research findings to help improve the Attachment component
* Propose a change to the Attachment component
* Report issues or bugs you encounter when implementing this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-39461\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References

* Australian Government Design System (AGDS) - Cards and Link Lists
* Australian Government Style Manual - Clear language and writing style
* Web Content Accessibility Guidelines (WCAG) 2.2
* Digital Service Standard - Criterion 3: Leave no one behind

### Changelog

<table><thead><tr><th width="129.30859375">Version</th><th width="132.88671875">Date</th><th>Changes</th></tr></thead><tbody><tr><td>v1.8.0</td><td>Jul 2024</td><td><ul><li>Improved responsive behaviour for mobile displays</li><li>Added support for multiple file formats</li><li>Enhanced accessibility features</li></ul></td></tr><tr><td>v1.7.0</td><td>Mar 2024</td><td><ul><li>Updated styling to improve visual hierarchy</li></ul><ul><li>Fixed spacing issues between multiple attachments</li></ul></td></tr><tr><td>v1.6.0</td><td>Oct 2023</td><td><ul><li>Initial release of the component</li></ul></td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

# Table of Contents

A navigational component that helps users understand the structure of the current page and jump directly to specific sections.

### When to use

Use the table of contents component when:

* Content pages are long with multiple sections and subsections
* Users need to quickly scan the structure of a page
* You want to provide easy navigation to different sections of a long document
* You need to improve navigation within content-heavy pages such as information guides, policy documentation, or lengthy articles

### When not to use

Do not use the table of contents component when:

* The page has minimal content or only a few short sections
* The page structure is extremely simple with limited headings
* Content is primarily visual rather than text-based
* The space available is too limited to display the table of contents effectively
* The content follows a step-by-step wizard pattern where linear progression is required

***

### Best practice guidelines

* **Accurate reflection**: Ensure the table of contents accurately reflects the heading structure of the page, maintaining the correct hierarchy of headings.
* **Concise entries**: Keep table of contents entries concise and clear, ideally no more than one line per item.
* **Logical structure**: Maintain a clear visual hierarchy that shows the relationship between sections and subsections through appropriate indentation.
* **Responsive design**: Adapt the presentation of the table of contents for different screen sizes, potentially converting to a collapsible component on mobile devices.
* **Persistent access**: Consider making the table of contents "sticky" or persistent on long pages so users always have access to navigation as they scroll.
* **Visual distinction**: Ensure the table of contents is visually distinct from the main content while still following the design system's visual language.
* **Highlight current section**: Indicate the user's current position in the document by highlighting the corresponding entry in the table of contents.
* **Avoid overloading**: Only include meaningful section headers (H2, H3) in the table of contents—avoid including every heading level as this can create visual clutter.

### Variations

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42377&t=998o74fMWsnrD2FZ-1" %}

The table of contents component is available in the following variations:

**Standard table of contents**:

* Default styling, typically placed at the top of a content page before the main content begins
* Includes section titles linked to their respective sections on the page

**Sticky/fixed table of contents**:

* Remains visible as the user scrolls down the page, typically positioned in a sidebar
* Provides constant access to navigation regardless of scroll position

**Collapsible table of contents**:

* Can be expanded or collapsed to save space, particularly useful on mobile devices
* Usually displays a "Table of contents" or "In this page" header with an expansion indicator

**Nested table of contents**:

* Shows multiple levels of headings with clear visual hierarchy
* Provides more detailed navigation for complex documents

***

### Accessibility

This component has been assessed against WCAG 2.2 accessibility guidelines. Based on the CivicTheme v1.7.0 Accessibility Assessments, the following standards were tested for this component:

Summary of test results:

* All WCAG 2.2 Level A guidelines passed
* All WCAG 2.2 Level AA guidelines passed
* Not tested against all WCAG 2.2 Level AAA guidelines

Key accessibility features:

* Proper heading structure and semantic markup
* Keyboard navigability between all links
* Visible focus indicators for keyboard users
* Sufficient color contrast for text and interactive elements
* Proper ARIA roles and attributes to enhance screen reader compatibility

### Security

The table of contents component does not process user data or handle sensitive information, minimizing security concerns. Standard web security practices should be followed during implementation.

### Component inspiration and uplift

This component has been modelled after the In-page Nav component in the former Australian Government Design System (AGDS). It has been uplifted by Salsa Digital, as the custodian of the CivicTheme Design System, in the following ways:

* Created stronger contrast/distinction between resting and hover states of section links
* Used smaller text sizes for section links to better establish content hierarchy
* Improved interaction states to match CivicTheme's design language
* Enhanced mobile responsiveness for improved usability on smaller screens

These uplifts were based on user testing that showed users preferred clearer visual indicators for interactive elements and a more compact design that doesn't overwhelm the main content.

***

### User research on this component

★★★★☆ Confidence rating = High (Based on controlled testing)

User research has been conducted by CivicTheme's design team on the table of contents component's usability and effectiveness. This involved multiple rounds of testing with a diverse group of users.

Key findings from the research:

* Users appreciate the ability to quickly scan page structure before reading content
* Sticky/fixed variations were particularly valued on long pages
* Some users initially overlooked the component, leading to design improvements that increase visual prominence
* Testing confirmed the importance of current section highlighting to help users maintain their bearings

The research validated the table of contents as an essential navigation aid for content-heavy pages and informed several usability improvements to the component.

### Known issues

* **Scroll synchronization**: Some users experience issues with the highlighted section not always accurately reflecting their current position on the page, particularly when sections are close together.
* **Mobile usability**: On smaller screens, the table of contents can take up significant vertical space, potentially pushing important content below the fold if not implemented as a collapsible component.
* **Heading depth**: There is occasional confusion about which heading levels should be included in the table of contents, with some users expecting to see deeper heading levels than are typically shown.

### More research needed

More user research is needed in the following areas:

* Optimal positioning of the table of contents on different page layouts
* User preferences regarding dynamic vs. static table of contents on mobile devices
* Effectiveness of different visual treatments for indicating the current section
* Usage patterns across different user demographics and contexts

If you have conducted user research that addresses any of these gaps, you can submit your research findings to help improve this component.

### Help improve this component

To help make this component useful and up-to-date, you can:

* Contribute to our table of contents component discussion on the CivicTheme GitHub repository
* Submit your user research findings to help improve the component
* Propose a change to the table of contents component via a pull request
* Report bugs or issues you encounter when implementing this component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42377\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* Nielsen, J. (2010). "Scrolling and Attention." Nielsen Norman Group.
* Loranger, H. (2014). "Minimize Design Risk by Focusing on Outcomes and Context." Nielsen Norman Group.
* W3C Web Accessibility Initiative. (2021). "WAI-ARIA Authoring Practices 1.2: Navigation."
* Australian Government Design System Documentation (Archived)

### Changelog

<table><thead><tr><th width="101.703125">Version</th><th width="134.16796875">Date</th><th>Description</th></tr></thead><tbody><tr><td>1.0.0</td><td>Initial release</td><td>Initial component release</td></tr><tr><td>1.7.0</td><td>March 2024</td><td>Updated to improve contrast between states and optimize for mobile</td></tr></tbody></table>

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

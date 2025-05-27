# Paragraph

Paragraph is a fundamental text element that presents content in structured blocks, enabling clear communication of information using CivicTheme's typography system.

### When to use:

Use the paragraph component when you need to present textual content in a structured format. Paragraphs are essential for:

* Main body content across web pages
* Descriptive text within components like cards, callouts, and banners
* Explanatory information alongside forms and interactive elements
* Terms and conditions, privacy policies, and other legal content
* Instructional content and step-by-step guides

### When not to use:

Do not use the paragraph component when:

* A heading would be more appropriate for section titles or page headings
* A list (ordered or unordered) would better present information in a scannable format
* Information can be better presented through tables, graphics, or other visual formats
* Content requires special formatting such as code snippets or blockquotes

***

### Best practice guidelines:

* Readability: Keep paragraphs concise—ideally 3-5 sentences—to improve readability and comprehension. Break longer content into multiple paragraphs.
* Logical structure: Start with the most important information and use paragraphs to group related ideas together, following a logical flow.
* Plain language: Write in plain language, avoiding jargon and complex terminology where possible. This aligns with the Australian Government Style Manual guidelines for clear communication.
* Appropriate styling: Use the right size and weight variant for the context. Lead copy (larger paragraphs) works well as introductions, while body copy is suitable for main content.
* Responsive considerations: Ensure paragraph text remains readable across all device sizes by maintaining appropriate line lengths (50-75 characters per line is ideal).
* White space: Maintain adequate spacing between paragraphs to create visual separation and improve readability.
* Consistency: Maintain consistent styling of paragraphs throughout your site to establish visual hierarchy and improve user comprehension.

### Variations:

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2947-38330&t=b83UZlIpwPkLMi9E-1" %}

CivicTheme provides various paragraph styles to serve different content needs:

* Size variants: Extra large, large, regular, small
* Weight variants: Regular, bold
* Style variants: Regular, underline

These variants can be combined to create different text presentations suitable for different contexts, such as lead paragraphs, body text, captions, and footnotes.

***

### Accessibility:

This component meets WCAG 2.2 AA accessibility guidelines according to the CivicTheme v1.7.0 Accessibility Assessments.

| WCAG 2.2 Criterion       | Status | Level    |
| ------------------------ | ------ | -------- |
| 1.4.3 Contrast (Minimum) | Pass   | Level AA |
| 1.4.4 Resize text        | Pass   | Level AA |
| 2.1.1 Keyboard           | Pass   | Level A  |
| 1.4.12 Text Spacing      | Pass   | Level AA |

This ensures all paragraph text has sufficient contrast, can be resized up to 200% without loss of content, and maintains readability when text spacing is adjusted.

### Security:

Security data not available for this component.

### Component inspiration and uplift:

This component has been modelled after the Body component in the former Australian Government Design System (AGDS). CivicTheme has uplifted the component in the following ways:

* All typography uses the commercially free Lexend font family as the primary web font, which is specifically designed to improve reading fluency and character recognition.
* Body copy is restricted to 12-15 words per line, in line with Web Content Accessibility Guidelines recommendations of 80 characters (or less) per line.
* Paragraph breaks have been refined to span 1.5 times the height of a traditional line break, improving readability through appropriate white space.
* Anchored links use a background colour on hover state, rather than a standard underline or colour change, enhancing visibility of interactive elements.

The sans-serif Lexend font family with variable, extended scaling specifically aims to improve reading fluency, addressing the finding that over 60% of people experience some reading difficulty.

***

### User research on this component:

★★★★☆ Confidence rating = High (Informed by design system best practices and accessibility standards)

While there is no specific user research data available exclusively for the paragraph component in CivicTheme, its design is informed by well-established typography and readability standards. The component incorporates research findings about reading patterns, optimal line length, and spacing considerations that have been validated across numerous studies.

The choice of the Lexend font family was backed by specific research showing its effectiveness for reading fluency. Research led by Dr. Bonnie Shaver-Troup in 2000 demonstrated that sans-serif fonts with expanded scaling improve character recognition and reduce cognitive noise, benefiting a wide range of readers.

### Known issues:

* Line height considerations: In some contexts, the standard line height may need adjustment when paragraph text is displayed alongside other components with specific spacing requirements.
* Mobile text scaling: On extremely small screens, some paragraph variations may benefit from further size adjustments to maintain optimal readability.
* Multilingual support: When displaying content in languages that use different writing systems, additional considerations for font rendering and spacing may be needed.

### More research needed:

More user research is needed in the following areas:

* Performance impact of font loading strategies for the Lexend variable font family across different browsers and devices
* User preferences regarding optimal line length across different contexts and content types
* Effectiveness of different paragraph styles for improving comprehension of complex information
* Reading patterns and preferences for multilingual users accessing content in multiple languages

### Help improve this component:

To help make this component useful and up-to-date, you can:

* Contribute to our paragraph component discussion
* Submit your user research findings to help improve the paragraph component
* Propose a change to the paragraph component

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources:

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2947-38330\&t=b83UZlIpwPkLMi9E-1)
* Storybook
* GitHub

### References:

* The Reading Teacher - Research on reading fluency and text formatting
* Lexend.com - Research on font readability and cognitive processing
* Australian Government Style Manual - Guidelines for clear writing and content structure
* Nielsen Norman Group - Research on reading patterns and optimal text presentation

### Changelog:

The paragraph component has evolved through various iterations of the CivicTheme design system to improve readability, accessibility and usability. Key changes include refinements to spacing, responsive behavior, and typography settings.

### Contact us:

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

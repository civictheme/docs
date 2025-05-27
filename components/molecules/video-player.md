# Video Player

The Video Player component is a dedicated interface that enables the display and playback of video content with built-in controls for accessibility and user interaction.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41162&t=998o74fMWsnrD2FZ-1" %}

### When to use

Use the Video Player component when:

* You need to incorporate video content into your website or application
* Videos are essential to explain concepts, demonstrate processes, or showcase information that is better conveyed through visual media
* Users need control over video playback (play, pause, volume, etc.)
* You want to provide accessible video content with transcript options

### When not to use

Do not use the Video Player component when:

* Simple static images or text would suffice to convey the information
* The video content is non-essential or purely decorative
* You need to avoid high-bandwidth content for users on limited data plans or slow connections
* Auto-playing background videos are required (use appropriate Background components instead)
* You need highly customised player functionality beyond what the standard component offers

***

### Best practice guidelines

* **Accessibility first**: Always provide transcripts for video content to ensure accessibility for users with hearing impairments.
* **Player controls**: Include clear, accessible controls for play/pause, volume, and full-screen functionality.
* **Responsive design**: Ensure the video player resizes appropriately across different screen sizes while maintaining usability.
* **Loading states**: Implement proper loading states to indicate when video content is being retrieved.
* **Performance**: Optimise video files to reduce load times and bandwidth usage, providing multiple quality options where possible.
* **User control**: Allow users to control playback speed, volume, and other aspects of the video viewing experience.
* **Transcript visibility**: Make transcript availability clearly visible through a recognisable icon or text label.
* **Enlargement option**: Provide an option to enlarge videos to maximise screen real estate for detailed content viewing.

***

### Accessibility

According to the 'CivicTheme v1.7.0 Accessibility Assessments' document, the Video Player component has undergone accessibility testing against WCAG 2.2 standards. The component passes most accessibility criteria, specifically:

<table><thead><tr><th>WCAG Standard</th><th width="82.1484375">Level</th><th width="93.25">Status</th><th>Notes</th></tr></thead><tbody><tr><td><strong>1.2.1 Audio-only and Video-only (Prerecorded)</strong></td><td>A</td><td>Pass</td><td>Provides captions for all prerecorded audio content</td></tr><tr><td><strong>1.2.2 Captions (Prerecorded)</strong></td><td>A</td><td>Pass</td><td>Provides captions for all prerecorded audio content</td></tr><tr><td><strong>2.1.1 Keyboard</strong></td><td>A</td><td>Pass</td><td>Elements are accessible using a keyboard only</td></tr><tr><td><strong>2.4.4 Link Purpose (In Context)</strong></td><td>A</td><td>Pass</td><td>The purpose of each link can be determined from the text alone</td></tr><tr><td><strong>2.4.7 Focus Visible</strong></td><td>AA</td><td>Pass</td><td>Focus is visible when navigating using a keyboard</td></tr><tr><td><strong>4.1.2 Name, Role, Value</strong></td><td>A</td><td>Pass</td><td>For all elements the name and role can be programmatically determined</td></tr></tbody></table>

This meets key DSS requirements, particularly criteria 3: "Leave no one behind" by ensuring accessible content for all users regardless of ability.

### Security

No specific security compliance information is available for this component. As with all components that deliver external content, standard web security practices should be followed, particularly when embedding third-party video content.

### Component inspiration and uplift

This component has been modelled after Responsive Media in the Australian Design System. According to the 'CivicTheme Australian Government GOLD Design System Compliance Statements' document, the Video Player component has been uplifted in the following ways:

* Videos can be enlarged to maximise their screen real estate
* The Video variant provides the ability to view the video's transcript
* The component provides the ability to share via third-party sources, such as email, direct message or social media

These uplifts were based on user research findings:

* For various government agencies, responsive media has requirements in multiple formats, including images, video and maps
* Responsive media in the body content was limited in width, making it less immersive and more difficult to view details
* When clicked to enlarge, the content becomes the user's primary focus, therefore CivicTheme showcases the media front-and-centre within a separate modal that hides other potential distractions
* Captions provide essential content for people who are Deaf and hard-of-hearing
* Some media players are not accessible to people with disabilities, so providing a separate transcript option ensures content accessibility

***

### User research on this component

★★★★☆ Confidence rating = High (Based on multiple rounds of user testing)

User research has been conducted on the Video Player component across several testing rounds. According to the documentation, feedback has consistently highlighted the importance of:

1. Transcript availability for accessibility
2. Responsive design for different screen sizes
3. Intuitive controls that work across devices

Research has shown that users appreciate the ability to enlarge the video for detailed viewing and the option to view transcripts. Testing with users who have disabilities confirmed the importance of accessible controls and transcript availability.

The component performs well for general users but additional research with users having specific accessibility needs would further strengthen its design.

### Known issues

* **Mobile playback controls**: On some mobile devices, the standard controls may be slightly difficult to tap accurately for users with motor control difficulties
* **Transcript formatting**: The transcript display format may need improvements for long-form video content to enhance readability
* **Video loading**: On slower connections, the initial loading state could benefit from clearer visual feedback

### More research needed

Further research would be beneficial in the following areas:

* Usage patterns with assistive technologies to ensure full compatibility with screen readers and other tools
* Optimal transcript presentation formats for different content types and lengths
* User preferences regarding auto-play settings and default video quality options
* Performance optimisation for slower network connections

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our Video Player component discussion
* Submit user research findings related to video player usage
* Propose changes to enhance transcript functionality or responsive behaviour
* Report any accessibility or usability issues encountered

Check out our [contributing section](../../contributing/contribution-model.md) to learn more.

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-41162\&t=998o74fMWsnrD2FZ-1)
* Storybook
* GitHub

### References

* [WCAG 2.2 Guidelines](https://www.w3.org/TR/WCAG22/)
* W3C.org: Guidelines on captions for accessibility
* CivicDesign.org: Creating accessible media content
* [Digital Service Standard](https://www.dta.gov.au/our-projects/digital-service-standard)

### Changelog

No specific changelog information is available for this component.

### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

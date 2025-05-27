# Mobile Navigation

The Mobile Navigation component provides a user-friendly, accessible menu system that helps users navigate websites on mobile devices while maintaining hierarchy and context.

{% embed url="https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42053&t=cQqD23snAO3bHEZS-1" %}

### When to use

Use the Mobile Navigation component when:

* Creating responsive websites or applications that need to work effectively on mobile devices
* You have complex navigation structures that need to be condensed for smaller screens
* Multiple levels of navigation need to be preserved in a space-efficient manner
* Users need clear contextual information about their location in the site hierarchy

### When not to use

Do not use the Mobile Navigation component when:

* The website has minimal navigation needs that can be easily accommodated with a simple horizontal menu
* A desktop-focused design doesn't require responsive adaptation for mobile devices
* You're developing a progressive web app with its own custom navigation patterns
* The navigation hierarchy is so flat that a simpler solution would be more appropriate

### Best practice guidelines

* **Clear hierarchy representation**: Mobile navigation should clearly display the hierarchy of the site, with distinct tiers for main navigation, subcategories, and detail pages.
* **Contextual cues**: Include visual and textual indicators to help users understand where they are in the navigation structure, such as headings for each navigation level.
* **Efficient back navigation**: Provide consistent "Back" or "Close" options that allow users to move up the hierarchy efficiently.
* **Visible active states**: Clearly indicate which navigation item is currently active or selected to help users maintain awareness of their location.
* **Logical grouping**: Group related navigation items together to aid understanding and create a more intuitive information architecture.
* **Minimise scrolling**: Limit the number of items at each level to reduce excessive scrolling, particularly on smaller screens.
* **Consistent positioning**: Place navigation controls in consistent locations to build user familiarity and improve usability.
* **Touch-friendly targets**: Ensure all interactive elements are large enough for comfortable touch interaction (at least 44×44px).
* **Visual distinction between levels**: Use clear visual cues to distinguish between different navigation levels.
* **Animated transitions**: Implement smooth transitions between navigation states to help users understand the relationship between levels.

### Variations

**Main menu (First tier)** A full-screen overlay presenting the primary navigation options, with utility links such as "Help" and "Contact us" at the bottom.

**Secondary level (Second tier)** Shows categories under a specific parent navigation item, displaying a header with the parent name for context.

**Tertiary level (Third tier)** Presents specific articles or pages within a selected category with appropriate contextual heading.

**Descendant Mobile Navigation** Shows parent and child links in default and pressed states for different interaction patterns.

***

### Accessibility

Based on the 'CivicTheme v1.7.0 Accessibility Assessments' file, the Mobile Navigation component meets WCAG 2.2 accessibility guidelines with the following results:

Summary of accessibility test results:

| WCAG Criterion                           | Status |
| ---------------------------------------- | ------ |
| **Info and Relationships (Level A)**     | Passed |
| **Resize text (Level AA)**               | Passed |
| **Keyboard (Level A)**                   | Passed |
| **Keyboard Trap (Level A)**              | Passed |
| **Focus Order (Level A)**                | Passed |
| **Visual Focus Indicator (Level AA)**    | Passed |
| **On Focus behavior (Level A)**          | Passed |
| **On Input behavior (Level A)**          | Passed |
| **Consistent identification (Level AA)** | Passed |

The component includes a visible heading above each navigation menu to provide context, and the Close button is positioned in the top right for consistent placement.

### Security

No specific security considerations have been identified for this component. Standard web application security practices should be followed when implementing the component.

### Sites using this component

The Mobile Navigation component is widely used across government, corporate, and educational sites that implement CivicTheme. As this is a core navigational component, it appears on virtually all CivicTheme implementations.

### Component inspiration and uplift

This component has been modelled after the Main Nav component in the former Australian Government Design System (AGDS). As described in the 'CivicTheme Australian Government GOLD Design System Compliance Statements' document, CivicTheme has uplifted this component in the following ways:

* Included a heading above each navigation menu (i.e., "Main Menu" or the category name)
* Moved the Close button to the top right of the mobile navigation
* Added a secondary "utility" navigation fixed at the bottom to accommodate secondary information
* Added right arrow icons by default for menu items that have child pages
* For deeper-level navigation, added a "back arrow" icon to allow users to navigate back one category

These uplifts were based on user research findings indicating that:

* The heading helps provide greater context on what menu/category the user had just clicked
* The Close button position reduces visual noise on the left side of navigation
* Right arrow icons communicate to users that they will navigate to the next level down
* Back arrow icons provide clear navigation cues for multi-level information architecture

***

### User research on this component

★★★★☆ Confidence rating = High (Informed by research)

The Mobile Navigation component has been tested in multiple rounds of usability testing across different CivicTheme implementations. Key findings include:

* Users appreciate the clear structure and visual hierarchy of the navigation system
* The consistent positioning of "Back" and "Close" buttons creates predictable navigation patterns
* The use of arrow icons effectively communicates the direction of navigation
* Most users intuitively understand the multi-tiered approach and can navigate effectively between levels
* Some users initially looked for a hamburger menu icon before recognizing the navigation pattern

Research has shown that mobile navigation is critical to the overall user experience on government sites, especially for task-focused visitors who rely on quick access to specific sections. The component meets the Digital Service Standard requirements for connecting services and building trust in design through its consistent and intuitive interface.

### Known issues

* **Performance on older devices**: Animations and transitions may cause slight lag on older mobile devices with limited processing power
* **Deep navigation challenges**: When sites have very deep hierarchies (4+ levels), the pattern can become confusing for users who may lose track of their location
* **Utility section visibility**: The utility links at the bottom can sometimes be overlooked by users focusing on the primary navigation items
* **Back button expectations**: Some users expect the device's back button to navigate between levels rather than using the component's built-in navigation controls

### More research needed

Further research would be beneficial in the following areas:

* How users with cognitive impairments navigate multi-level mobile navigation structures
* Optimal number of items per level before scrolling becomes problematic
* Effectiveness of including search functionality within the mobile navigation component
* User preferences for navigating between separate but related sections of a site

### Help improve this component

To help make this component more useful and up-to-date, you can:

* Contribute to our Mobile Navigation component discussion
* Submit your user research findings to help improve the Mobile Navigation component
* Propose a change to the Mobile Navigation component

***

### Resources

* [Figma](https://www.figma.com/design/nXTZFR1mKPLExtEbYtazzD/CivicTheme--Design-System-v1.9.0?node-id=2976-42053\&t=cQqD23snAO3bHEZS-1)
* Storybook
* GitHub

### References

* Nielsen Norman Group. (2016). Mobile Navigation Patterns. https://www.nngroup.com/articles/mobile-navigation-patterns/
* Baymard Institute. (2021). Mobile E-Commerce Navigation Usability. https://baymard.com/research/mobile-e-commerce-navigation
* Digital Transformation Agency. (2023). Digital Service Standard. https://www.dta.gov.au/help-and-advice/digital-service-standard

#### Changelog

<table><thead><tr><th width="100.58203125">Version</th><th width="119.01953125">Date</th><th>Changes</th></tr></thead><tbody><tr><td>1.8.0</td><td>Jul 2024</td><td>Renamed to "Mobile Navigation" from "Mobile Nav" for consistency</td></tr><tr><td>1.7.0</td><td>Mar 2024</td><td>Improved accessibility to meet WCAG 2.2 requirements</td></tr><tr><td>1.6.0</td><td>Nov 2023</td><td>Added consistent help section in main menu</td></tr><tr><td>1.5.0</td><td>Jun 2023</td><td>Enhanced navigation depth indicators</td></tr></tbody></table>

#### Contact us

If you have a question about the CivicTheme design system or need our help, visit the [Getting Help](../../getting-started/getting-help.md) page for guidance.

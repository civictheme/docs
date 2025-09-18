# Layout builder

CivicTheme provides one layout: **3 Columns Layout**

When managing your layout (layout builder) within display settings of your content type, you are able to configure whether the content is to be constrained or whether the content is to go page edge to page edge.

## Edge-to-edge vs Constrained Content

**Edge-to-edge content** means that the content and background elements extend the full width of the browser window, from the left edge to the right edge of the viewport. This creates an immersive, modern design where components can utilize the entire screen width. This style is commonly used for landing pages, hero sections, and full-width image galleries.

**Constrained content** limits the content width to a maximum container size (1248 pixels), centering it within the viewport with margins on either side on larger screens. 
This improves readability and provides a more traditional page layout that's easier to scan on wide displays.

## Sidebar Management

When using Layout Builder's sidebar columns, users need to be careful to ensure they don't conflict with theme region sidebar blocks. Blocks placed in the theme's left and right sidebars can overlap with blocks placed in Layout Builder's sidebars, potentially causing duplication or layout issues. It's important to have a clear strategy for managing which blocks appear in which system to maintain consistent layouts across your site.

## Deprecated Layouts

There are two deprecated layouts that should not be used:
* Single Column
* Single Column contained

These layouts are in the process of being removed in the coming release.

The layout configuration is defined in the `civictheme.info.yml`.

The layout can be viewed within [UI kit](https://uikit.civictheme.io/?path=/story/base-layout--layout).

# Menus

CivicTheme uses four different styles of menu in the base theme. These are placed by block in different regions of the 
page.

You can control the component / style for the menu with the theme hook suggestion which can be configured in the Block 
configuration form.

## Primary Navigation

The dropdown menu is the primary navigation for the site.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/primary-menu.png" alt="Primary Menu Configuration."><figcaption><p>Primary Menu Setup. Click on the image to zoom in.</p></figcaption></figure></div>

For this menu to be themed correctly the menu block must be configured with `menu__civictheme_primary_navigation` theme hook suggestion in the HTML and style options of the Block configuration form.
<div data-full-width="true"><figure><img src="../../.gitbook/assets/primary-navigation-menu-hook.png" alt="HTML and style options - Theme hook suggestion: civictheme_primary_navigation"><figcaption><p>Primary Navigation Theme Suggestion Hook Configuration. HTML and style options - Theme hook suggestion: civictheme_primary_navigation. Click on the image to zoom in.</p></figcaption></figure></div>

Settings for primary navigation used in CivicTheme are:
```yaml
settings:
  id: 'menu_block:civictheme-primary-navigation'
  label: 'Primary Navigation'
  label_display: ''
  provider: menu_block
  follow: false
  follow_parent: child
  label_link: false
  label_type: block
  level: 1
  depth: 3
  expand_all_items: false
  parent: 'civictheme-primary-navigation:'
  suggestion: civictheme_primary_navigation
```
These are set through the Menu Block configuration form.

## Secondary Navigation

The secondary navigation is a menu block placed in the top right of the page.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/secondary-menu.png" alt="Secondary Menu Configuration."><figcaption><p>Primary Menu Setup. Click on the image to zoom in.</p></figcaption></figure></div>

For this menu to be themed correctly the menu block must be configured with `menu__civictheme_secondary_navigation` theme hook suggestion in the HTML and style options of the Block configuration form.
<div data-full-width="true"><figure><img src="../../.gitbook/assets/secondary-navigation-menu-hook.png" alt="HTML and style options - Theme hook suggestion: civictheme_secondary_navigation"><figcaption><p>Secondary Navigation Theme Suggestion Hook Configuration. HTML and style options - Theme hook suggestion: civictheme_secondary_navigation. Click on the image to zoom in.</p></figcaption></figure></div>

Default settings for secondary navigation provided by CivicTheme are:
```yaml
settings:
  id: 'menu_block:civictheme-secondary-navigation'
  label: 'Secondary Navigation'
  label_display: ''
  provider: menu_block
  follow: false
  follow_parent: child
  label_link: false
  label_type: block
  level: 1
  depth: 0
  expand_all_items: false
  parent: 'civictheme-secondary-navigation:'
  suggestion: civictheme_secondary_navigation
```

## Mobile Navigation

The mobile navigation is a content block type. This block once created is placed is in the Header Middle 3 region.

There is no configuration needed for this block.

## Side Navigation

The side navigation is a menu block placed in the Side bar top left region of the page.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/side-navigation-menu.png" alt="Sidebar Navigation Menu."><figcaption><p>SideBar Navigation. Click on the image to zoom in.</p></figcaption></figure></div>

For this menu to be themed correctly the menu block must be configured with `menu__civictheme_sidebar_navigation` theme hook suggestion in the HTML and style options of the Block configuration form.
<div data-full-width="true"><figure><img src="../../.gitbook/assets/sidebar-navigation-menu-hook.png" alt="HTML and style options - Theme hook suggestion: civictheme_sidebar_navigation"><figcaption><p>Sidebar Navigation Theme Suggestion Hook Configuration. HTML and style options - Theme hook suggestion: civictheme_sidebar_navigation. Click on the image to zoom in.</p></figcaption></figure></div>

The settings for the side navigation used in CivicTheme are:
```yaml
settings:
  id: 'menu_block:civictheme-primary-navigation'
  label: 'Side Navigation'
  label_display: ''
  provider: menu_block
  follow: false
  follow_parent: child
  label_link: false
  label_type: block
  level: 1
  depth: 3
  expand_all_items: false
  parent: 'civictheme-primary-navigation:'
  suggestion: civictheme_sidebar_navigation
```

## Footer Navigation

The default setup for the footer navigation is a menu block placed in each of the four middle regions of the footer.
<div data-full-width="true"><figure><img src="../../.gitbook/assets/footer-menu.png" alt="Footer Menu Configuration."><figcaption><p>Footer Menu Setup. Click on the image to zoom in.</p></figcaption></figure></div>

For this menu to be themed correctly the menu block must be configured with `menu__civictheme_footer` theme hook suggestion in the HTML and style options of the Block configuration form.
<div data-full-width="true"><figure><img src="../../.gitbook/assets/footer-menu-theme-hook.png" alt="HTML and style options - Theme hook suggestion: civictheme_footer"><figcaption><p>Footer Theme Suggestion Hook Configuration. HTML and style options - Theme hook suggestion: civictheme_footer. Click on the image to zoom in.</p></figcaption></figure></div>

The settings for each footer menu are:

```yaml
settings:
  id: 'menu_block:civictheme-footer'
  label: 'Footer menu 1'
  label_display: visible
  provider: menu_block
  follow: false
  follow_parent: child
  label_link: false
  label_type: fixed
  level: 1
  depth: 1
  expand_all_items: false
  parent: '<set the parent>'
  suggestion: civictheme_footer
```

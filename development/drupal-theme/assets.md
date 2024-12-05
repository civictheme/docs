# Assets

Site assets refer to the collection of files and resources that are essential for the visual appearance, functionality, and overall user experience of a website.

This section explains working with assets in the context of your custom sub-theme. All commands and path are related to your sub-theme directory.

## Compiling and serving assets

All assets are compiled using `npm run dist` based on the supplied [Webpack configuration](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme_starter_kit/webpack/webpack.common.js).

{% hint style="info" %}
The Webpack and Storybook configuration may change between versions, so make sure to follow instructions in [Version update](broken-reference) section.
{% endhint %}

Assets are served from the `dist` directory and are inter-linked within your sub-theme.

The sub-theme uses 4 types of assets:

1. [CSS](assets.md#css)
2. [JS](assets.md#js)
3. [Fonts](assets.md#fonts)
4. [Images](assets.md#images)

### CSS

SASS styles are compiled into a single CSS file which is located in `dist/civictheme.css` and included into a theme as a library defined in `yourtheme.libraries.yml` file.

There are two categories of style files:

1. UI kit overrides or additional styles
2. Drupal styles

This distinction is made to provide a clear separation between UI kit-specific styles and those exclusive to Drupal.

#### UI kit overrides or additions styles

These reside in `components` directory and repeat the structure of the UI kit library. This allows you to create new or extend existing UI kit components.

See the [Demo button example](https://github.com/civictheme/monorepo-drupal/tree/develop/web/themes/contrib/civictheme/civictheme_starter_kit/components/01-atoms/demo-button) for more details.

#### Drupal styles

These reside in `assets/sass` directory and are intended to override or additionally style Drupal markup.

See the [Local task block styles override example](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme_starter_kit/assets/sass/block/_local-tasks.scss) for more details.

{% hint style="info" %}
Normally, there should be a very minimal number of Drupal style overrides as the whole front-end output is based on the UI kit.
{% endhint %}

### JS

JS files are compiled into a single file which is located in `dist/civictheme.js` and included into a theme as a library defined in `yourtheme.libraries.yml` file.

There are two categories of JS files:

1. UI kit overrides or additional JS files
2. Drupal JS files

This distinction is made to provide a clear separation between UI kit-specific JS behaviours and those exclusive to Drupal.

#### UI kit overrides or additions JS files

These reside in `components` directory and repeat the structure of the UI kit library. This allows to create new or extend existing UI kit components.

See the [Demo button example](https://github.com/civictheme/monorepo-drupal/tree/develop/web/themes/contrib/civictheme/civictheme_starter_kit/components/01-atoms/demo-button) for more details.

#### Drupal JS files

These reside in `assets/js` directory and are intended to override or provide additional behaviours for the Drupal functionality.

## Fonts

Font files are referenced from the SASS files.

They reside in `assets/fonts` directory.

Fonts can replace or extend the current font list provided by the UI kit.

See the [Fonts addition example](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme_starter_kit/components/variables.base.scss#L42) for more details.

## Images

#### Backgrounds and logos

Backgrounds and Logos are content uploaded through the [theme settings ](broken-reference)form for you sub-theme, therefore files placed in `assets/backgrounds` and `assets/logos` are used only in your sub-theme's Storybook for visual representation.

#### Icons

{% hint style="info" %}
Icons discussed here are the icons used in the UI elements and not the icons that can be uploaded as content in components such as [Navigation card](../../content-authoring/components/navigation-card.md) or [Social links](broken-reference/)
{% endhint %}

CivicTheme UI kit provides several icons out of the box.

The [design system file](https://civictheme.io/figma) provides more open source icons that can be exported in SVG format and added to your sub-theme.

Place or replace icons in `assets/icons` directory: new icons can be referred to from the SASS styles of your custom components; replaced icons will be picked up by the existing components, provided that their name has not changed.

If the icon file is referenced in the template but does not exist in the above directory, the icon will not render.

{% hint style="info" %}
It is recommended not to delete any of the default icons found in the starter theme, as they are used by the CivicTheme theme in the default templates.
{% endhint %}

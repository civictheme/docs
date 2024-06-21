# Drupal theme

### Installation

```
composer require drupal/civictheme
```

Alternatively, you can download the [latest version](https://www.drupal.org/project/civictheme/releases) from Drupal.org and place into the desired location.

{% hint style="info" %}
Note that Drupal core has a known [issue](https://www.drupal.org/node/3204271) and a [patch](https://www.drupal.org/files/issues/2023-07-16/3204271-20-missing-layout-exception.patch) would need to be installed on your site.
{% endhint %}

### Usage

CivicTheme can be used as a no-code Drupal theme with some of the configurations done on theme settings page.

Enable required modules (Drupal [allows themes to declare module dependencies](https://www.drupal.org/node/2937955), but [does not yet allow those modules to be enabled automatically](https://www.drupal.org/project/drupal/issues/3100374)):

```sh
drush ev "require_once dirname(\Drupal::getContainer()->get('theme_handler')->rebuildThemeData()['civictheme']->getPathname()) . '/theme-settings.provision.inc'; civictheme_enable_modules();"
```

Clear caches

```sh
drush cr
```

Enable the theme in UI or with Drush:

```sh
drush then civictheme
```

See [Sub-theme](sub-theme.md) section to create a sub-theme and use CivicTheme as a base theme.

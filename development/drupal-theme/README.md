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

CivicTheme can be used as a no-code Drupal theme with some of the configurations done on [theme settings](broken-reference) page.

Enable the theme in UI or with Drush:

```
drush then civictheme
```

See [Sub-theme](sub-theme.md) section to create a sub-theme and use CivicTheme as a base theme.

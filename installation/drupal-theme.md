# Drupal theme

## Install CivicTheme

```
composer require drupal/civictheme
```

Alternatively, you can download the [latest version](https://www.drupal.org/project/civictheme/releases) from Drupal.org and place into the desired location.

{% hint style="info" %}
Note that Drupal core has a known [issue](https://www.drupal.org/node/3204271) and a [patch](https://www.drupal.org/files/issues/2023-07-16/3204271-20-missing-layout-exception.patch) would need to be installed on your site.
{% endhint %}

## Install Contrib modules

CivicTheme has required dependencies on [contrib modules](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme.info.yml#L11) and optional dependencies on\
search\_api.

These dependencies need to be downloaded and installed before you are able to install CivicTheme.

### GovCMS SaaS specific installation instructions

{% hint style="info" %}
See [Using in GovCMS SaaS](govcms-saas.md) for specific GovCMS SaaS instructions.
{% endhint %}

### Usage

CivicTheme can be used as a no-code Drupal theme with some of the configurations done on theme settings page.

### Enabling contrib modules

Due to Drupal [allowing themes to declare module dependencies](https://www.drupal.org/node/2937955), but [does not yet allow those modules to be enabled automatically](https://www.drupal.org/project/drupal/issues/3100374)).

The contrib module dependencies need to enabled manually or with an automated script:

#### Enable required modules only

```sh
drush ev "require_once dirname(\Drupal::getContainer()->get('theme_handler')->rebuildThemeData()['civictheme']->getPathname()) . '/theme-settings.provision.inc'; civictheme_enable_modules(FALSE);"
```

#### Enable required and optional modules

```sh
drush ev "require_once dirname(\Drupal::getContainer()->get('theme_handler')->rebuildThemeData()['civictheme']->getPathname()) . '/theme-settings.provision.inc'; civictheme_enable_modules();"
```

### Clear caches

```sh
drush cr
```

### Enable CivicTheme

Enable the theme in UI or with Drush:

<pre class="language-sh"><code class="lang-sh"><strong>drush then civictheme
</strong></code></pre>

### Provision content

CivicTheme comes with pre-set Block Content blocks configuration. Since Drupal does not support running install hooks in themes, a custom content provisioning script has to be used.

1. Login to the local instance of your site.
2. Navigate to `/admin/appearance/settings/<SUBTHEME_MACHINE_NAME>`\\

<figure><img src="../.gitbook/assets/provision-content (1).png" alt=""><figcaption></figcaption></figure>

3. Press "Provision content" button.
4. Navigate to the homepage and observe that all blocks and menus are present.
5. Export config for created entities:

```sh
ahoy drush cex -y
```

Depending on your deployment workflow, you may need to repeat this step after deployment to your hosting provider environment.

{% hint style="info" %}
After deployment and provisioning your remote **feature environment** should look like a [default CivicTheme site](https://default.civictheme.io/) without homepage content.
{% endhint %}

### Setting up a sub-theme

See [Sub-theme](sub-theme.md) section to create a sub-theme and use CivicTheme as a base theme.

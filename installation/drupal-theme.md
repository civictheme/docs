---
description: This page explains how to install, update, and manage CivicTheme in Drupal
---

# Drupal Theme

## CivicTheme Drupal installation guide

CivicTheme is available as a Drupal theme that enables rapid creation of accessible and consistent digital experiences. This guide walks you through the steps to install and set up CivicTheme in a Drupal project using Composer, Drush, and other typical Drupal tools.



***

### 1. **Install CivicTheme via Composer**

To begin, you'll need to install CivicTheme using **Composer**, the recommended package manager for Drupal projects.

Run the following command in your Drupal root directory:

```bash
composer require drupal/civictheme
```

This command will add CivicTheme as a dependency in your project, download the theme, and ensure it’s available for use in your Drupal installation.



***

### 2. **Enable the CivicTheme theme**

Once CivicTheme is installed, you can enable it using **Drush** (Drupal's command-line tool). This will set CivicTheme as the default theme for your site.

Run the following Drush commands:

```bash
drush then civictheme
drush config-set system.theme default civictheme
```

* `drush then civictheme`: This command enables the CivicTheme theme.
* `drush config-set system.theme default civictheme`: This command sets CivicTheme as the default theme for your site.



***

### 3. **Compile frontend assets (optional)**

If you plan to modify the theme's frontend assets (like SCSS or JavaScript), you will need to install the theme’s dependencies and compile the assets.

Navigate to the CivicTheme directory:

```bash
cd themes/contrib/civictheme
```

Install the required Node.js packages:

```bash
npm install
```

Now, compile the assets using the build script:

```bash
npm run build
```

If you’re actively developing the theme and need live reloading, you can run the following to automatically recompile assets as you work:

```bash
npm run watch
```

> **Note**: The build process will generate CSS and JavaScript files based on the SCSS and JS located within the theme. If you're not planning to customize these files, this step is optional.



***

### 4. **Configure the theme (optional)**

CivicTheme includes a flexible **configuration system** that allows you to customize various theme settings through the Drupal UI.

To access these settings:

1. Go to **Appearance** in your Drupal admin.
2. Find **CivicTheme** and click on **Settings**.

Here, you can adjust layout options, branding (logos, colors), and other style settings to fit your specific project needs.



***

### 5. **Managing dependencies and updates**

As CivicTheme evolves, you’ll want to keep it up to date to receive the latest features and security fixes. You can update the theme through **Composer** by running the following command:

```bash
composer update drupal/civictheme
```

This will update the theme to the latest stable version available.



***

### 6. **Useful development commands**

**Clear Cache**: Drupal’s cache system may sometimes prevent immediate reflection of your changes. Clear the cache using:

```bash
drush cr
```

**Rebuild Theme Assets**: If you’ve modified SCSS or JS files and need to recompile assets:

```bash
npm run build
```

**Export Configuration**: If you've made theme configuration changes through the Drupal UI, don’t forget to export the configuration to keep everything in sync:

```bash
drush cex
```



***

### 7. **Explore CivicTheme components**

CivicTheme provides a collection of **atomic design components** that can be used across your Drupal site. Each component is designed to be accessible and customizable to meet your project’s needs.

You can explore CivicTheme’s components via its **Storybook** instance:

* [CivicTheme Storybook](https://storybook.civictheme.io) – A live, interactive environment where you can view and test all the components available within CivicTheme.

By integrating these components into your Drupal site, you ensure a consistent and accessible user experience that adheres to WCAG 2.2 AA standards.



***

## **Contributing to CivicTheme for Drupal**

CivicTheme is an **open-source** project that relies on community contributions. Whether you're fixing a bug, adding new components, or improving documentation, your help is appreciated.

To contribute, please read the [contribution docs](../contributing/contribution-model.md).



***

## Subtheme implementation

### Creating a sub-theme from the CivicTheme theme

CivicTheme provides a starter theme and a script to generate a child theme for you to get started with.

Run the following command from within `civictheme` theme directory:

```shell
php civictheme_create_subtheme.php <theme_machine_name> "Human theme name" "Human theme description" /path/to/theme_machine_name
```

This will generate a sub-theme in `path/to/theme_machine_name` theme directory with everything ready to be installed and compiled.

### Enabling sub-theme

Enable the theme in UI or with Drush:

```sh
drush theme:enable theme_machine_name
drush config-set system.theme default theme_machine_name
```

### Compiling sub-theme assets

Run the following command from within your sub-theme directory:

```sh
npm run build
```

{% hint style="info" %}
NodeJS version >=18.14 is required to compile front-end assets.
{% endhint %}



***

## Updating your Drupal theme

{% hint style="info" %}
Ensure that you always review the [release notes](https://www.drupal.org/project/civictheme/releases) prior to beginning the update process.
{% endhint %}

{% hint style="warning" %}
Always test your updates in non-production environments first.
{% endhint %}

{% hint style="info" %}
The updates may contain both _configuration_ and _content_ updates.

Updates would need to run in production environment.&#x20;
{% endhint %}

{% hint style="warning" %}
If configuration is managed through files, make sure that your database updates run **before** your configuration import in your **production** environment.
{% endhint %}

#### Run the below steps locally:

Update CivicTheme base theme code:

```sh
composer update drupal/civictheme
```

or download the [latest version](https://www.drupal.org/project/civictheme/releases) from Drupal.org and place into the desired location.

{% hint style="warning" %}
**Important! Do not skip the update step or you may miss the important schema changes.**
{% endhint %}

1.  Run updates and export the configuration

    ```sh
    drush updb
    drush cex
    ```
2. Re-provision the site with updated configuration.
3. Check that everything looks good.
4. Commit exported configuration files and deploy to the non-production environment for testing.

### Tooling update

CivicTheme comes with a starter kit, which contains tooling required to build and integrate sub-theme TWIG, CSS and JS assets into Drupal. This tooling is mostly JS-based and requires regular maintenance.

CivicTheme may ship an update to tooling requiring your sub-themes to update their own tooling. Refer to update notes and update tooling configuration as described.

{% hint style="warning" %}
Below is required only if the release notes explicitly call out tooling updates
{% endhint %}

Although unique scenarios may arise depending on your sub-theme customisations, the most common use case involves regenerating your sub-theme:

1. Move your custom sub-theme directory elsewhere
2. Run [sub-theme](../development/drupal-theme/sub-theme.md) creation script to create a new sub-theme with the same name
3. Commit changes
4. Copy your custom sub-theme back
5. Use your git diff tool to accept/decline changes

Usually, you would preserve your own `components` and `assets` directories, as they would contain most of the sub-theme customisations, and accept the rest of changed files as updates.



## Feedback

We're always looking at ways to improve our model for contributions, and rely on your feedback to ensure an enjoyable contribution experience. The best way to give us feedback is to join our [Slack channel ](https://drupal.slack.com/archives/C039UV0CQBZ)and chat to us there, or contact us via [email](mailto:support@civictheme.io)!

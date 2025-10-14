# Sub-theme

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
```

### Compiling sub-theme assets

Run the following command from within your sub-theme directory:

```sh
npm run build
```

{% hint style="info" %}
NodeJS version >=22 is required to compile front-end assets.
{% endhint %}



### Remove examples from civictheme_starter_kit

CivicTheme 1.11 saw the upgrade to SDCs which came with a namespace change.

The existing example components need to be removed so that civictheme sub-themes built with this tool work correctly.

We will address this issue in CivicTheme 1.12. As a workaround, please delete the following directories from your new sub-theme manually (unless you have added some code changes):

    /components/01-atoms/demo-button
    /components/01-atoms/demo-button
    /components/03-organisms/header

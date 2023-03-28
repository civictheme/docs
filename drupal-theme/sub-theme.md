# Sub-theme

### Creating a sub-theme from the CivicTheme theme

CivicTheme provides a starter theme and a script to generate a child theme for you to get started with.

Run the following command from within `civictheme` theme directory:

```
php civictheme_create_subtheme.php <theme_machine_name> "Human theme name" "Human theme description" /path/to/theme_machine_name
```

This will generate a sub-theme in `path/to/theme_machine_name` theme directory with everything ready to be installed and compiled.

### Enabling sub-theme

Enable the theme in UI or with Drush:

```
drush then theme_machine_name
```

### Compiling sub-theme assets

Run the following command from within your sub-theme directory:

```
npm run build
```

{% hint style="info" %}
NodeJS version 16 is required to compile front-end assets.
{% endhint %}

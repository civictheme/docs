# Version update

{% hint style="info" %}
Ensure that you always review the [release notes](https://www.drupal.org/project/civictheme/releases) prior to beginning the update process.
{% endhint %}

1.  Update CivicTheme base theme:

    ```sh
    composer update drupal/civictheme
    ```

    or\
    download the [latest version](https://www.drupal.org/project/civictheme/releases) from Drupal.org and place into the desired location
2.  Run updates

    ```sh
    drush updb
    ```
3.  Run configuration export

    ```sh
    drush cex
    ```
4. Check updated configuration files with a diff tool of your choice: resolve configuration overrides one-by-one; there could be cases where fields are renamed or removed -  these will be handled automatically in the update hooks.
5. Re-build local environment with updated configuration.
6. Check that everything looks good
7. If there are issues - repeat steps 2-6 until desired result is achieved.

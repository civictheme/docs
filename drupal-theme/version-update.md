# Version update

{% hint style="warning" %}
Always read release notes before starting the update
{% endhint %}

### Updating code

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
4. Check updated configuration with a diff tool of your choice.
5. Resolve configuration overrides one-by-one. There could be cases where fields are renamed or removed. These will be handled automatically in the update hooks.
6. Re-build local environment with updated configuration.
7. Check that everything looks good
8. If there are issues - repeat steps 2-7 until desired result is achieved.

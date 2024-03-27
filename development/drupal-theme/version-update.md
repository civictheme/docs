# Updating them

{% hint style="info" %}
Ensure that you always review the [release notes](https://www.drupal.org/project/civictheme/releases) prior to beginning the update process.
{% endhint %}

{% hint style="warning" %}
Always test your updates in non-production environments first.
{% endhint %}

### Drupal theme update

{% hint style="info" %}
The updates may contain both _configuration_ and _content_ updates.

Updates would need to run in production environment.&#x20;
{% endhint %}

{% hint style="warning" %}
If configuration is managed through files, make sure that your database updates run **before** your configuration import in your **production** environment.
{% endhint %}

Run the below steps locally:

1.  Update CivicTheme base theme code:

    ```sh
    composer update drupal/civictheme
    ```

    or\
    download the [latest version](https://www.drupal.org/project/civictheme/releases) from Drupal.org and place into the desired location
2.  Run updates and export the configuration

    ```sh
    drush updb
    drush cex
    ```

    **Important! Do not skip this step or you may miss the important schema changes.**
3. Re-provision the site with updated configuration.
4. Check that everything looks good.
5. Commit exported configuration files and deploy to the non-production environment for testing.

### Tooling update

CivicTheme comes with a starter kit, which contains tooling required to build and integrate sub-theme TWIG, CSS and JS assets into Drupal. This tooling is mostly JS-based and requires regular maintenance.

CivicTheme may ship an update to tooling requiring your sub-themes to update their own tooling. Refer to update notes and update tooling configuration as described.

{% hint style="warning" %}
Below is required only if the release notes explicitly call out tooling updates
{% endhint %}

Although unique scenarios may arise depending on your sub-theme customisations, the most common use case involves regenerating your sub-theme:

1. Move your custom sub-theme directory elsewhere
2. Run [sub-theme](sub-theme.md) creation script to create a new sub-theme with the same name
3. Commit changes
4. Copy your custom sub-theme back
5. Use your git diff tool to accept/decline changes

Usually, you would preserve your own `components` and `assets` directories, as they would contain most of the sub-theme customisations, and accept the rest of changed files as updates.

---
description: How to update CivicTheme in GovCMS SaaS
---

# Updating theme

{% hint style="info" %}
Ensure that you always review the [release notes](https://www.drupal.org/project/civictheme/releases) prior to beginning the update process.
**This documentation assumes you have config import enabled.**
TODO: Update steps to cater for not having config import enabled.
{% endhint %}

{% hint style="warning" %}
Always test your updates in non-production environments first.
{% endhint %}

### CivicTheme update

Run the below steps locally:

1.  Remove delete the existing civictheme core theme folder from your themes folder.
2.  Download the [latest version](https://www.drupal.org/project/civictheme/releases) from Drupal.org and place into the themes folder
3.  Run updates and export the configuration

    ```sh
    ahoy drush updb -y
    ahoy drush cex -y
    ahoy drush cr
    ```
4. (Optional) In YOUR-CUSTOM-CIVICTHEME.info.yml file, update the "version" and clear the Drupal cache.
5. Test your site locally to ensure nothing is broken. If something is broken, fix it in your CivicTheme subtheme. Do **NOT** fix it in the CivicTheme core theme. 

    **Important! Do not skip this step or you may miss the important schema changes.**
6. Run ```sh ahoy build``` to re-provision your local site with updated configuration and updated theme.
7. Check that everything looks good.
8. Commit all changed files and deploy to the non-production environment for testing.

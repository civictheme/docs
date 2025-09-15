# GovCMS Manual Installation

This guide provides step-by-step instructions for manually installing CivicTheme on GovCMS SaaS. Use this method if you prefer not to use the automated installation script.

## Prerequisites

Before beginning the manual installation, ensure you have:

* [ ] Access to GitLab project
* [ ] Support ticket to enable config imports actioned
* [ ] Production has your user added with administrator role
* [ ] All [GovCMS SaaS required software](https://github.com/govCMS/GovCMS/wiki/1.1-Local-setup#dependencies) installed
* [ ] NPM 10+ and NodeJS 22+ available on your machine
* [ ] **GovCMS project set up locally with:**
* [ ] Local environment running (`ahoy up`)
* [ ] Database installed

{% hint style="info" %}
If you haven't set up your GovCMS local environment yet, refer to the [GovCMS documentation](https://github.com/govCMS/GovCMS/wiki/1.1-Local-setup) for instructions on setting up your local development environment.
{% endhint %}

## Where to get help

See [Getting help](../getting-started/getting-help.md) section

## 1. CivicTheme setup

{% hint style="info" %}
It is advised to perform all changes in a dedicated (feature) branch to test this part before applying any customisations.
{% endhint %}

### 1.1 Download CivicTheme theme

Since GovCMS SaaS does not allow to install themes via Composer, CivicTheme source must be installed as a custom theme.

1. [Download the latest CivicTheme release](https://www.drupal.org/project/civictheme/releases) and extract into `themes/custom` directory, rename the directory to `civictheme`.

### 1.2 Enable required modules

Using an automated script to discover required modules from theme dependencies (Drupal does not support this OOTB):

```sh
ahoy drush ev "require_once dirname(\Drupal::getContainer()->get('theme_handler')->rebuildThemeData()['civictheme']->getPathname()) . '/theme-settings.provision.inc'; civictheme_enable_modules();"
```

### 1.3 Clear caches

{% hint style="warning" %}
Do not skip this step
{% endhint %}

```sh
ahoy drush cr
```

### 1.4 Enable admin and CivicTheme

{% hint style="warning" %}
CivicTheme MUST be enabled before your custom theme is enabled
{% endhint %}

```bash
# Clear Drupal cache.
ahoy drush cr
# Enable CivicTheme and set as default.
ahoy drush theme:enable civictheme
ahoy drush config-set -y system.theme default civictheme
ahoy drush config-set -y media.settings standalone_url true

# Enable admin theme and set as default (optional).
ahoy drush theme:enable adminimal_theme
ahoy drush config-set -y system.theme admin adminimal_theme
```

### 1.5 Remove GovCMS content types

CivicTheme GovCMS helper module `civictheme_govcms` serves the purpose to remove unnecessary entities and configuration that ships with GovCMS.

Install it locally to automatically remove the configuration from DB to later have it exported without GovCMS entities.

1.  Run in CLI container (`ahoy cli`):

    ```sh

    # If `web/modules/contrib` is not writable, you can use an alternative directory `web/themes/custom/civictheme` etc.
    mkdir -p /app/web/themes/custom/civictheme/modules
    cd /app/web/themes/custom/civictheme/modules

    # Download and extract the helper module.
    # Ensure to use the latest tag (not Release) https://github.com/civictheme/civictheme_govcms/tags
    wget https://github.com/civictheme/civictheme_govcms/archive/refs/tags/<latest-tag>.tar.gz && tar -xvf <latest-tag>.tar.gz && rm <latest-tag>.tar.gz && mv civictheme_govcms-<latest-tag> civictheme_govcms


    # Enable module, run the command to remove entities and uninstall a module.
    drush cr
    drush pm-enable -y civictheme_govcms
    drush civictheme_govcms:remove-config --preserve=user_roles
    drush pm-uninstall -y civictheme_govcms

    # Delete the module
    rm -Rf civictheme_govcms
    ```
2.  Export updated configuration

    ```sh
    ahoy drush cex -y
    ```

### 1.6 Generate a sub-theme

{% hint style="info" %}
Consider naming your theme as close as possible to the name of the site. Do not include `civic` or `civictheme` into name to avoid confusions in code when maintaining a theme in the future.
{% endhint %}

Run in CLI container (`ahoy cli`):

```sh
# Generate sub-theme (example overrides are removed using --remove-examples flag). 
# See php civictheme_create_subtheme.php --help
cd web/themes/custom/civictheme
php civictheme_create_subtheme.php <SUBTHEME_MACHINE_NAME> "<SUBTHEME HUMAN NAME>" "<SUBTHEME HUMAN DESCRIPTION>" ../<SUBTHEME_MACHINE_NAME> --remove-examples
```

This should result in 2 directories:

```
themes/civictheme
themes/<SUBTHEME_MACHINE_NAME>
```

### 1.7 Install sub-theme and set as default

```sh
# Enable sub-theme.
ahoy drush theme:enable <SUBTHEME_MACHINE_NAME> -y
# Set sub-theme as default.
ahoy drush config-set system.theme default <SUBTHEME_MACHINE_NAME> -y
```

### 1.8 Build front-end assets

1.  Run on your host:

    ```sh
    cd themes/<SUBTHEME_MACHINE_NAME>
    nvm use
    npm install
    npm run build
    ```
2. Check that directory `themes/<SUBTHEME_MACHINE_NAME>/dist` was created.
3. Navigate to your site and assert that default styling was applied.

### 1.9 Commit built assets

1.  Modify `.gitignore` file in your new theme and remove the following line:

    ```
    dist
    ```
2. Commit built assets.

### 1.10 Provision content

See [Content Provisioning for CivicTheme](govcms-content-provisioning.md) for detailed instructions on provisioning content blocks and menus.

{% hint style="success" %}
After deployment and provisioning your remote **feature environment** should look like a [default CivicTheme site](https://default.civictheme.io/) without homepage content.
{% endhint %}

## 2. Deployment

### 2.1 Deploy to (pre-)production

1. Merge feature branch to `master` (or `develop` and then to `master`).
2. Commit and push to remote.
3. Wait for deployment to finish and login to the Drupal instance.
4. Navigate to `/admin/appearance/settings/<SUBTHEME_MACHINE_NAME>`.
5. Press "Provision content" button.
6. Navigate to the homepage and observe that all blocks and menus are present.

{% hint style="success" %}
After deployment and provisioning your remote **(pre-)production** environment should look like a [default CivicTheme](https://default.civictheme.io/)[ site](https://default.civictheme.io/) without homepage content
{% endhint %}

### 2.2 Cleanup

{% hint style="warning" %}
Only run this step once everything is working and looking as expected.
{% endhint %}

1. ```sh
   # Remove unnecessary files.
   rm themes/civictheme/civictheme_create_subtheme.php
   rm -Rf themes/civictheme/civictheme_starter_kit
   ```
2. Commit and push to remote.

## 3. Customising CivicTheme

1. Replace sub-theme logos in repository `themes/<SUBTHEME_MACHINE_NAME>/assets/logos` with site-specific versions.
2. [Update the colour palette](../content-authoring/site-wide-configuration/colours.md) with your sub-theme.
3. Update sub-theme `screenshot.png` with something more appropriate (optional).
4. `npm run build` and commit changes.



## Resolving issues with roles

1. Enable `Role Delegation` module and allow `Site Administrator` to delegate both GovCMS and CivicTheme roles. Ensure that CivicTheme roles have the same permissions with their GovCMS counterparts.
2. Login to the site and re-assign existing users from GovCMS roles to relevant CivicTheme roles.
3. Remove GovCMS admin roles and re-export configuration.

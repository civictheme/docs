# GovCMS SaaS

CivicTheme can be installed on GovCMS SaaS using either an automated script or manual installation process.

## Installation methods

### [Automated installation (recommended)](govcms-saas-manual.md)

The automated installation script is the preferred method for setting up CivicTheme on new GovCMS SaaS project. It handles most of the setup process automatically, including:

* Downloading and extracting CivicTheme
* Configuring required modules
* Creating your custom subtheme
* Optionally provisioning content blocks

[**Start with automated installation →**](govcms-saas-automated.md)

### [Manual installation](govcms-saas-manual.md)

For those who prefer more control over the installation process or cannot use the automated script, the manual installation guide provides step-by-step instructions for:

* Setting up your local environment
* Installing CivicTheme and dependencies
* Creating and configuring your subtheme
* Building and deploying assets

[**View manual installation guide →**](govcms-saas-manual.md)

## Post-installation steps

### [Content provisioning](govcms-content-provisioning.md)

Instructions on how to provision CivicTheme's default content blocks and menus, whether you're using automated or manual installation.

## Before you begin

Regardless of which installation method you choose, ensure you have:

* [ ] Access to GitLab project
* [ ] Support ticket to enable config imports actioned
* [ ] Administrator role added to your user in production
* [ ] All [GovCMS SaaS required software](https://github.com/govCMS/GovCMS/wiki/1.1-Local-setup#dependencies) installed
* [ ] NPM 10+ and NodeJS 22+ available on your machine
* [ ] A GovCMS project already set up and installed locally

## Troubleshooting

### Content not appearing after provisioning

- Clear caches: `ahoy drush cr`
- Check that your sub-theme (not the base CivicTheme theme) is set as the default
- Verify all required modules are enabled

### Styling not applied

- Confirm the `dist` directory exists in your sub-theme
- Check that `.gitignore` is not excluding `dist`
- Clear caches and hard-refresh the browser

### Provisioning button not available

- Ensure you are logged in as an administrator
- Verify the theme is properly installed and enabled
- Clear caches and reload the theme settings page

## Where to get help

See [Getting help](../getting-started/getting-help.md) section for support options and resources.

## Next steps

After installation, it is recommended that you read the documents on how CivicTheme works and how to customise your sub-theme installation:

* [Customising your sub-theme](../development/drupal-theme/)

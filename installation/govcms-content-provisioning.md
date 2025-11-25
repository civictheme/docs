# GovCMS Content Provisioning

CivicTheme comes with pre-set Block Content blocks configuration. Since Drupal does not support running install hooks in themes, a custom content provisioning script has to be used.

## When to provision content

Content provisioning is needed in two scenarios:

1. **During initial setup** - When first installing CivicTheme
2. **After deployment** - When deploying to production environments

## Provisioning workflow

The provisioning needs to be run twice:

1. **Locally** - to capture created configuration for config entities (blocks, menus etc.)
2. **In production** - to populate the configuration with the default content

## Step-by-step instructions

### 1. Local provisioning

1. Login to the local instance of your site.
2.  Navigate to `/admin/appearance/settings/<SUBTHEME_MACHINE_NAME>`

    <figure><img src="../.gitbook/assets/provision-content (1).png" alt=""><figcaption></figcaption></figure>
3. Press "Provision content" button.
4. Navigate to the homepage and observe that all blocks and menus are present.
5.  Export config for created entities:

    ```sh
    ahoy drush cex -y
    ```
6. Commit and push to remote.

### 2. Production provisioning

1. Wait for deployment to finish and login to the Drupal instance.
2. Navigate to `/admin/appearance/settings/<SUBTHEME_MACHINE_NAME>`.
3. Press "Provision content" button.
4. Navigate to the homepage and observe that all blocks and menus are present.

## What gets provisioned

The content provisioning creates:

* **Block Content blocks** - Pre-configured content blocks for common page elements
* **Menu items** - Default menu structure
* **Configuration entities** - Required configuration for the theme to function properly

## Avoiding content forklift

If you want to avoid doing a full content migration (forklift) from local to production:

1. Use the `-n` flag when running the automated installation script
2. Provision content locally first
3. Export the configuration
4. Deploy configuration to production
5. Provision content in production

## Troubleshooting

### Content not appearing after provisioning

* Ensure caches are cleared: `ahoy drush cr`
* Check that the correct theme is set as default
* Verify that all required modules are enabled

### Provisioning button not available

* Ensure you're logged in as an administrator
* Check that the theme is properly installed and enabled
* Clear caches and try again

### Configuration export issues

* Make sure you have the correct permissions to export configuration
* Ensure that config imports are enabled (check with your GovCMS support ticket)

## Related documentation

* [Automated Installation](govcms-saas-automated.md)
* [Manual Installation](govcms-saas-manual.md)
* [Theme Settings](../content-authoring/site-wide-configuration/)

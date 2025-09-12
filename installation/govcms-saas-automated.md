# Automated Installation for GovCMS SaaS

This is the preferred installation method for setting up CivicTheme on GovCMS SaaS. The automated script handles most of the setup process for you.

## Before you begin

* [ ] Get access to GitLab project
* [ ] Check that support ticket to enable config imports was actioned
* [ ] Check that production has your user added with administrator role
* [ ] Check that you have all [GovCMS SaaS required software](https://github.com/govCMS/GovCMS/wiki/1.1-Local-setup#dependencies) available on your machine
* [ ] Check that you have NPM 10+ and NodeJS 22+ available on your machine
* [ ] Read this whole page to make sure you understand the steps

## Prerequisites

- **GovCMS Project**: You must have a GovCMS project / scaffold already set up and installed locally (i.e., you have run `ahoy install`).
- **Ahoy**: ahoy must be installed and configured for your project (i.e., you can run ahoy commands).
- **Docker**: Docker must be running, as ahoy typically interacts with Docker containers.
- **tar and curl**: These command-line utilities must be available in your shell environment where you run the script.
- **Bash**: The script is written for Bash.

## What the Script Does

The script will perform the following actions:

- Download and extract the specified CivicTheme version into themes/custom/civictheme.
- Run initial CivicTheme provisioning commands.
- Clear Drupal caches.
- Enable CivicTheme and set it as the default theme temporarily.
- Download, install, configure, and then uninstall and remove the civictheme_govcms module (as per the specified workflow).
- Generate a new subtheme based on CivicTheme using the provided names and description.
- Enable the new subtheme and set it as the site's default theme.
- Optionally provision content blocks (can be skipped with `-n` flag)

After the script completes successfully, your new subtheme will be active and ready for customisation in themes/custom/<your_subtheme_machine_name>.

## Download the script

From your GovCMS project root directory, run:

```bash
curl -o setup_civictheme.sh \
https://raw.githubusercontent.com/civictheme/civictheme_govcms/refs/heads/main/scripts/setup_civictheme.sh \
&& chmod +x setup_civictheme.sh
```

*Note*: Download the script to your GovCMS project root directory on your host machine (not inside a Docker container).

## Run the script

Execute the script from your GovCMS project's root directory. You'll need to provide values for all the required arguments.

### Command Structure:

```bash
./setup_civictheme.sh -c <civictheme_version> \
-g <govcms_module_ref> \
-m <subtheme_machine_name> \
-u "<subtheme_human_name>" \
-d "<subtheme_description>" \
[-p] \
[-n]
```

### Arguments:

| Argument | Required | Description | Example |
|----------|----------|-------------|---------|
| `-c <civictheme_version>` | Yes | The version of the CivicTheme base theme to download | `"1.11.0"` |
| `-g <govcms_module_ref>` | Yes | The Git reference (branch or tag) for the civictheme_govcms module | Branch: `"main"`<br>Tag: `"1.0.1"` or `"v1.0.1"` |
| `-m <subtheme_machine_name>` | Yes | The machine-readable name for your new subtheme. Use lowercase letters, numbers, and hyphens/underscores | `"my_custom_site_theme"` |
| `-u "<subtheme_human_name>"` | Yes | The human-readable name for your new subtheme. Enclose in quotes if it contains spaces | `"My Custom Site Theme"` |
| `-d "<subtheme_description>"` | Yes | A short description for your new subtheme. Enclose in quotes | `"A custom theme for My Awesome GovCMS Project"` |
| `-p` | No | Apply Drupal cache backend patch (drupal.org issue). This patches LayoutPluginManager to add cache tags for better cache invalidation | - |
| `-n` | No | Skip content provisioning. By default, content provisioning is enabled | - |

### Content Provisioning Option (`-n` flag)

The `-n` flag allows you to skip the automatic provisioning of content blocks during installation. This is particularly useful when you want to avoid performing a content forklift with GovCMS.

**When to use `-n`:**
- If you plan to manually provision blocks locally first, export the configuration, and then provision in production
- If you want to avoid doing a full content forklift migration
- If you prefer to have more control over when and how content blocks are created

**Workflow when using `-n`:**
1. Run the script with `-n` to skip content provisioning
2. Manually provision blocks through the theme settings locally
3. Export the block configuration using `drush cex`
4. Deploy the configuration to production
5. Provision the content in production through theme settings

For detailed instructions on content provisioning, see [Content Provisioning for CivicTheme](govcms-content-provisioning).

### Example Commands:

**Standard installation (with content provisioning):**
```bash
./setup_civictheme.sh -c "{{ CIVICTHEME VERSION - see project page }}" \
                      -g "main" \
                      -m "my_gov_project_theme" \
                      -u "My Gov Project Theme" \
                      -d "Custom theme for the My Gov Project website on GovCMS."
```

**Installation without content provisioning:**
```bash
./setup_civictheme.sh -c "{{ CIVICTHEME VERSION - see project page }}" \
                      -g "main" \
                      -m "my_gov_project_theme" \
                      -u "My Gov Project Theme" \
                      -d "Custom theme for the My Gov Project website on GovCMS." \
                      -n
```

## Post-Installation Steps

1. **Build front-end assets**:
   ```bash
   cd themes/<SUBTHEME_MACHINE_NAME>
   nvm use
   npm install
   npm run build
   ```

2. **Commit built assets**:
   - Modify `.gitignore` file in your new theme and remove the following line:
     ```
     dist
     ```
   - Commit the built assets to your repository

3. **Content Provisioning** (if skipped during installation):
   - See [Content Provisioning for CivicTheme](govcms-content-provisioning) for detailed instructions

## Deployment

1. Push your changes to the remote repository
2. Wait for deployment to complete
3. If you used the `-n` flag, provision content in production following the [Content Provisioning guide](govcms-content-provisioning)

## Next Steps

- [Customising CivicTheme / SubTheme Development](/development/drupal-theme/)
- [Manual Installation Guide](govcms-saas-manual) (alternative method)
- [Content Provisioning](govcms-content-provisioning)

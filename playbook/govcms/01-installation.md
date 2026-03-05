# Chapter 1: Installing CivicTheme on GovCMS SaaS

This chapter walks your team through getting CivicTheme installed and running on a GovCMS SaaS project. By the end, you will have CivicTheme enabled, a sub-theme generated, front-end assets built, and the site ready for customisation.

GovCMS SaaS does not support installing themes via Composer, so CivicTheme is installed as a custom theme. An automated script handles the heavy lifting, but a manual path is available if you need more control.

## Prerequisites

- [ ] Access to the GovCMS GitLab project
- [ ] A support ticket actioned to enable config imports
- [ ] Your user added with the administrator role in production
- [ ] All [GovCMS SaaS required software](https://github.com/govCMS/GovCMS/wiki/1.1-Local-setup#dependencies) installed (Docker, Ahoy, tar, curl, Bash)
- [ ] NodeJS 22+ and NPM 10+ available on your machine
- [ ] A GovCMS project already set up and installed locally (`ahoy install` completed)

## Step 1: Choose your installation method

| Method    | Best for                               | Time        |
| --------- | -------------------------------------- | ----------- |
| Automated | New projects, standard setups          | ~15 minutes |
| Manual    | Existing projects, custom requirements | ~45 minutes |

There are automated steps (a bash script that automates the steps and a follow along manual step process.

For an overview of both methods and when to choose each, see the [GovCMS SaaS installation overview](../../installation/govcms-saas.md).

## Step 2: Run the installation

### Option A: Automated installation (recommended)

The automated script downloads CivicTheme, configures modules, removes GovCMS default content types, generates your sub-theme, and optionally provisions content — all in one command.

The script arguments, flags, download instructions, and example commands are documented in the [automated installation guide](../../installation/govcms-saas-automated.md).

> **Naming tip**: Name your sub-theme after the site, not after CivicTheme. Avoid including "civic" or "civictheme" in the machine name — it creates confusion when maintaining the theme later.

### Option B: Manual installation

If you need more control, the manual process walks through each step individually: downloading CivicTheme, enabling modules, removing GovCMS default content types via the `civictheme_govcms` helper module, generating the sub-theme, and building assets.

The full step-by-step process is covered in the [manual installation guide](../../installation/govcms-saas-manual.md).

## Step 3: Build front-end assets

After installation (automated or manual), build your sub-theme's CSS, JavaScript, and assets:

```bash
cd themes/<SUBTHEME_MACHINE_NAME>
nvm use
npm install
npm run build
```

Verify that the `themes/<SUBTHEME_MACHINE_NAME>/dist` directory was created. Navigate to your site in the browser and confirm that default CivicTheme styling is applied.

### Commit built assets

GovCMS SaaS requires built assets to be committed to the repository. But it is important not to commit your `node_modules` and other developer tools.

**Review [committing built assets](../../installation/govcms-saas-manual.md#commit-built-assets) for managing your code repository.**

## Step 4: Provision content

CivicTheme includes pre-configured blocks, menus, and configuration entities that set up the default site structure (header, footer, navigation, etc.). 
Unless a database forklift is being undertaken, the provisioning needs to happen **twice** — once locally to capture the configuration, and once in production to populate it with content. 
Both are triggered via the **Provision content** button at `/admin/appearance/settings/<SUBTHEME_MACHINE_NAME>`.

The full provisioning workflow, what gets created, how to avoid content forklifts, and troubleshooting are documented in the [GovCMS content provisioning guide](../../installation/govcms-content-provisioning.md).

## Step 5: Verify the installation

After provisioning, your site should match the [default CivicTheme site](https://default.civictheme.io/) (without homepage content). Check that:

- [ ] The header displays with the CivicTheme logo and navigation
- [ ] The footer displays with default blocks (social links, footer navigation, acknowledgement, copyright)
- [ ] The site responds correctly on mobile (navigation collapses to mobile menu)
- [ ] The admin theme is accessible at `/admin`

## Troubleshooting

For common installation issues (content not appearing, styling not applied, provisioning button missing), see the troubleshooting section in the [GovCMS SaaS installation reference](../../installation/govcms-saas.md#troubleshooting).

## Where to get help

CivicTheme provides multiple support channels for installation issues. For all support options, see [Getting help](../../getting-started/getting-help.md).

## Next step

With CivicTheme installed and your sub-theme generated, the next step is to understand the sub-theme structure and set up your local development workflow.

Continue to [Chapter 2: Setting Up Your Sub-Theme](../shared/02-sub-theme-setup.md).

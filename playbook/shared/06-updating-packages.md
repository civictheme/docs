# Chapter 6: Updating Packages

This chapter covers keeping your CivicTheme site current after the initial build. It explains the dependency chain, walks through the update process for both the CivicTheme base theme and your sub-theme's Node.js packages, and covers regression testing to catch breaking changes.

## Prerequisites

- [ ] A working CivicTheme sub-theme (see [Chapter 2](02-sub-theme-setup.md))
- [ ] Composer access (for Drupal community sites) or GitLab access (for GovCMS SaaS)
- [ ] Familiarity with the build system (see [Chapter 2](02-sub-theme-setup.md))

## Understanding the dependency chain

Your site has three layers of dependencies, each updated independently:

| Layer | Manager | What it affects |
|-------|---------|-----------------|
| CivicTheme base theme | Composer (Drupal) or manual download (GovCMS) | Component library, preprocess hooks, Drupal config |
| Sub-theme Node packages | npm | Build system, Storybook, SCSS compilation, linting |
| Drupal core + contrib modules | Composer | CivicTheme's module dependencies |

Updates should flow top-down: update the base theme first, then sub-theme packages, then rebuild and test.

## Step 1: Update the CivicTheme base theme

### Drupal community sites

Update via Composer:

```bash
composer update drupal/civictheme
drush updatedb
drush cr
```

Review the release notes on the [CivicTheme project page](https://www.drupal.org/project/civictheme/releases) before updating. 

**Pay attention to breaking changes to component schemas, new module dependencies, changes to preprocess hooks or utility functions, and SCSS variable or mixin changes. 
Updates can be a painful process depending on customisations and how set on the exact look of your existing site you are.**

### GovCMS SaaS sites

GovCMS SaaS does not use Composer for theme management. Download the new version, replace the `themes/custom/civictheme` directory, run database updates, and export configuration.

The GovCMS-specific update procedure covers additional steps for updating the CivicTheme UI Kit's SCSS dependencies. See [Updating CivicTheme on GovCMS SaaS](../../development/drupal-theme/updating-civitheme-govcms-sass.md).

## Step 2: Update sub-theme Node.js dependencies

Check for outdated packages with `npx npm-check-updates`. Update minor/patch versions (generally safe) with `npx npm-check-updates -u --target minor && npm install`. Review changelogs before updating major versions, particularly for Storybook, sass-embedded, and Vite.

## Step 3: Rebuild and test

After any update, run a full rebuild and verification:

```bash
npm run dist
npm run build
npm run lint
drush cr
```

### Regression testing checklist

- [ ] **Build completes** — `npm run dist` and `npm run build` finish without errors
- [ ] **Linting passes** — `npm run lint` has no new errors
- [ ] **Storybook loads** — all components render correctly at `http://localhost:6006`
- [ ] **Header and footer** — render correctly with your theme settings
- [ ] **Navigation** — primary and secondary navigation function correctly
- [ ] **Cards and lists** — all card types display correctly in list views
- [ ] **Forms** — form elements render and submit correctly
- [ ] **Light/dark themes** — components switch correctly between themes
- [ ] **Responsive layout** — site looks correct at mobile, tablet, and desktop breakpoints
- [ ] **Content authoring** — paragraphs can be added and edited in the content editor

### Handling breaking changes

If the update breaks something:

1. Check the CivicTheme release notes for migration instructions
2. Look for changes to component `.component.yml` schemas — new required props may need values
3. Check for renamed or removed SCSS variables or mixins
4. Review any changes to preprocess utility functions
5. If a component override in your sub-theme conflicts with a base theme change, update your override to match the new interface

## Recommended update schedule

| What | Frequency | Why |
|------|-----------|-----|
| Drupal security updates | Within 1 week of release | Security advisories have public disclosure timelines |
| CivicTheme patch releases | Monthly | Bug fixes and minor improvements |
| CivicTheme minor releases | Quarterly review | New features and component improvements |
| Node.js package updates | Monthly | Security patches for build tools |
| CivicTheme major releases | As released (plan migration) | May require sub-theme changes |

## Next step

Package updates keep your site current. The next chapter covers the specific process for monitoring and applying security patches.

Continue to [Chapter 7: Security Updates](07-security-updates.md).

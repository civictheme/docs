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
| Drupal core + contrib modules | Composer (Drupal) or managed by platform team (GovCMS SaaS) | CivicTheme's module dependencies |

On GovCMS SaaS, Drupal core and contributed module updates are managed by the GovCMS platform team — you do not update these yourself. The platform team applies security patches and version upgrades on a managed schedule. Your responsibility on GovCMS SaaS is limited to the CivicTheme base theme and your sub-theme's Node packages. On standalone Drupal sites, you manage all three layers via Composer.

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

### Visual regression testing

Before applying any update, capture a visual baseline of your site so you can compare it against the upgraded version. This makes it possible to identify exactly what changed and work through each difference methodically.

**1. Capture a baseline**

Use a visual regression tool (such as BackstopJS, Percy, or Playwright's screenshot comparison) to take screenshots of key pages and components before the update. Cover:

- Homepage and major landing pages
- Content pages using each content type
- Pages with custom component overrides
- Header, footer, and navigation in both desktop and mobile viewports
- Light and dark theme variants

**2. Apply the update and capture again**

After updating and rebuilding, run the same screenshot suite against the updated site.

**3. Compare and triage**

Review the visual diff report and categorise each difference:

- **Expected changes** — improvements or intentional design changes documented in the release notes
- **Broken components** — components that no longer render correctly due to schema changes, removed variables, or markup updates
- **Page errors** — pages that fail to render or show PHP/Twig errors
- **Subtle regressions** — spacing, color, or typography shifts that may indicate a changed variable or mixin

**4. Work through differences methodically**

For each broken component or regression:

1. Check if the component has an override in your sub-theme — compare your override against the updated base component
2. Look for changes to the `.component.yml` schema (new required props, renamed props, changed enums)
3. Check for renamed or removed SCSS variables and mixins in the release notes
4. Update your sub-theme's override to match the new interface, rebuild, and verify

Visual regression testing is particularly valuable for CivicTheme updates because component changes can cascade through the site in ways that are difficult to catch with manual spot-checking alone.

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
| CivicTheme patch releases | Quarterly | Bug fixes and minor improvements |
| CivicTheme minor releases | Annual | New features and component improvements |
| Node.js package updates | Quarterly | Security patches for build tools |

## Next step

Package updates keep your site current. The next chapter covers the specific process for monitoring and applying security patches.

Continue to [Chapter 7: Security Updates](07-security-updates.md).

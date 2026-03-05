# Chapter 7: Security Updates

This chapter covers the ongoing responsibility of monitoring and applying security patches to your CivicTheme site. It explains how to subscribe to advisory channels, assess severity, and apply fixes on both GovCMS SaaS and standalone Drupal.

Security updates are time-sensitive. Public disclosure of vulnerabilities means attackers can act quickly, so your team needs a clear process for monitoring advisories and responding within appropriate timelines.

## Prerequisites

- [ ] A running CivicTheme site (GovCMS SaaS or standalone Drupal)
- [ ] Administrator access to the site
- [ ] Access to the deployment pipeline (GitLab for GovCMS, your CI/CD for Drupal)

## Step 1: Subscribe to security advisory channels

Set up monitoring so your team is notified when security updates are released. You need to watch three sources:

- **Drupal Security Advisories** — [subscribe to the mailing list](https://www.drupal.org/security). Core security releases follow a regular window (third Wednesday of the month), but critical releases can happen at any time.
- **CivicTheme releases** — watch the [CivicTheme project page](https://www.drupal.org/project/civictheme/releases) and the [GitHub monorepo](https://github.com/civictheme/monorepo-drupal/releases). The [#civictheme-designsystem](https://drupal.slack.com/archives/C039UV0CQBZ) Drupal Slack channel often has early announcements.
- **npm advisories** — run `npm audit` in your sub-theme directory to check for known vulnerabilities. Enable GitHub Dependabot alerts if your repository is on GitHub. Carry out developer dependency maintenance every quarter.

## Step 2: Assess severity and set response timelines

Drupal Security Advisories include a risk score (0-25) based on the [NIST Common Misuse Scoring System](https://www.drupal.org/drupal-security-team/security-risk-levels-defined). Higher scores require faster action. 
As a site manager you should have policies and procedures regarding the response timelines for security updates.

## Step 3: Apply security updates

Follow the same update process as [Chapter 6](06-updating-packages.md): update the base theme (Composer for Drupal, manual download for GovCMS SaaS), rebuild front-end assets with `npm run dist`, run database updates, and clear caches. For CivicTheme-specific update procedures on GovCMS SaaS, see [Updating CivicTheme on GovCMS SaaS](../../development/drupal-theme/updating-civitheme-govcms-sass.md).

For npm vulnerabilities in build dependencies:

```bash
npm audit
npm audit fix
```

## Step 4: Verify the update

- [ ] The site loads without errors
- [ ] Content pages render correctly (check multiple content types)
- [ ] Forms submit correctly
- [ ] User login and authentication work
- [ ] Admin pages are accessible
- [ ] No new errors in Drupal's Recent Log Messages (`/admin/reports/dblog`)
- [ ] Front-end assets load (no broken CSS or JS)
- [ ] Components render correctly in both light and dark themes
- [ ] Any overridden components in your sub-theme still work with the updated base
- [ ] Storybook builds without errors (`npm run build`)

## Step 5: Document the update

Record what was updated and when for your team's reference: version numbers (before and after), security advisory references (SA-CORE, SA-CONTRIB numbers), any manual steps required, and test results.

## CivicTheme's security framework

CivicTheme maintains a comprehensive security posture with continuous automated scanning and multiple validation layers. For the full security framework details, including how to report vulnerabilities responsibly, see [Security](../../getting-started/security-policy.md).

## Reporting vulnerabilities

If you discover a security vulnerability in CivicTheme, do not open a public issue. Report it through the [Drupal CivicTheme Design System security page](https://www.drupal.org/project/issues/civictheme), following Drupal's responsible disclosure process.

## Summary

| Task | Frequency | Owner |
|------|-----------|-------|
| Monitor Drupal security advisories | Ongoing (subscribe once) | Tech lead / site manager |
| Monitor CivicTheme releases | Ongoing (subscribe once) | Tech lead |
| Run `npm audit` | Monthly | Developer |
| Apply critical security updates | Within 24-48 hours | Developer |
| Apply routine security updates | Within 1 week | Developer |
| Document applied updates | After each update | Developer / site manager |

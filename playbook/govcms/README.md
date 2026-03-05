# CivicTheme Playbook: GovCMS SaaS

This playbook is a step-by-step guide for teams building and maintaining a CivicTheme site on GovCMS SaaS. It is written for tech leads, project managers, and site managers — people who need to understand the process of setting up, customising, and keeping a CivicTheme site running.

CivicTheme is an open-source, government-grade design system built as a Drupal theme. It provides a library of accessible, reusable components following atomic design principles. On GovCMS SaaS, CivicTheme is installed as a custom theme rather than via Composer, and built assets are committed to the repository. This playbook accounts for those platform-specific requirements.

## How to use this playbook

Work through the chapters in order. Each chapter builds on the previous one, following the natural lifecycle of a CivicTheme project: install, configure, customise, maintain.

The playbook provides the task-oriented workflow — the sequencing, decisions, and practical steps your team needs. Where detailed reference material already exists in the CivicTheme documentation, the playbook links to it rather than duplicating it. This keeps everything in one place and ensures the information stays current.

## Chapters

### Site Development

1. **[Installation](01-installation.md)** — Get CivicTheme installed on GovCMS SaaS using the automated script or manual process, generate your sub-theme, build assets, and provision content.

2. **[Setting Up Your Sub-Theme](../shared/02-sub-theme-setup.md)** — Understand the sub-theme directory structure, configure the build system, run Storybook locally, and connect your sub-theme to Drupal.

3. **[Configuring Colors and Theme Settings](../shared/03-colors-and-settings.md)** — Set up your brand colors, configure the header and footer, and understand how CivicTheme's color system derives a full palette from your brand values.

4. **[Overriding Existing Components](../shared/04-overriding-components.md)** — Change how an existing CivicTheme component looks or behaves by copying it into your sub-theme and modifying it there.

5. **[Creating New Components](../shared/05-creating-components.md)** — Build a new component from scratch following CivicTheme conventions, from atomic design placement through to Drupal integration.

### Site Maintenance

6. **[Updating Packages](../shared/06-updating-packages.md)** — Keep your CivicTheme base theme, sub-theme dependencies, and Node.js packages up to date with a clear update and rebuild workflow.

7. **[Security Updates](../shared/07-security-updates.md)** — Subscribe to security advisories, assess severity, and apply patches to your GovCMS SaaS site.

## Who is this for?

| Role | What you will get from this playbook |
|------|--------------------------------------|
| **Tech lead** | End-to-end process for setting up and customising a CivicTheme site, including component architecture and override patterns |
| **Project manager** | Understanding of the process of installing and managing a CivicTheme site, dependencies between steps, and what the team needs at each stage |
| **Site manager** | Understanding of the maintenance process for keeping the site secure and up to date after the initial build |

## Getting help

If you run into issues at any point, CivicTheme has active support channels including a Drupal Slack channel, issue queues, and email support. For all options, see [Getting help](../../getting-started/getting-help.md).

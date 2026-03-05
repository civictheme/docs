# Chapter 2: Setting Up Your Sub-Theme

This chapter walks through the sub-theme that was generated during installation and gets your local development environment ready. By the end, you will understand the sub-theme directory structure, have the build system running, and be able to view components in Storybook.

**CivicTheme must never be modified directly. Unless exceptional circumstances which must be logged in your project documentation as updates will wipe out these changes**

Your sub-theme inherits everything from CivicTheme and is where all custom work happens — overriding components, adding new ones, and adjusting styles. The build system merges your sub-theme's components with the base theme's components at compile time, so your overrides take priority automatically.

## Prerequisites

See the [sub-theme reference](../../development/drupal-theme/sub-theme.md#prerequisites).

## Step 1: Understand the sub-theme directory structure

The sub-theme creation script generates a complete project scaffold. Understanding this structure is essential before making any changes. The key directories you will work in most are `components/`, `assets/`, `templates/`, and the two variable files (`variables.base.scss` and `variables.components.scss`).

The full directory structure, library system, and placeholder asset replacement are documented in the [sub-theme reference](../../development/drupal-theme/sub-theme.md).

## Step 2: Understand the build system

The build system is a custom Node.js script (`build.js`) that compiles your sub-theme's SCSS, JavaScript, and assets. It is not webpack or gulp — it is purpose-built for CivicTheme's component architecture. The essential commands are:

```bash
npm run build          # Full build (assets + Storybook static site)
npm run dist           # Compile assets only (faster, no Storybook)
npm run dist:watch     # Watch mode (recompiles on file changes)
npm run lint           # Lint SCSS and JavaScript
```

The build pipeline, output files, and configuration are documented in the [build system reference](../../development/drupal-theme/systems/build.md).

## Step 3: Run Storybook

Storybook provides an interactive development environment where you can view, test, and document components in isolation — without needing a running Drupal site.

Start the development server:

```bash
npm run storybook
```

This runs `npm run dist` first to compile assets, then starts the Storybook dev server with file watching. Both the asset compilation and Storybook will watch for changes and hot-reload automatically.

## Step 4: Verify the development workflow

Run through this checklist to confirm your development environment is working:

- [ ] `npm run dist` completes without errors
- [ ] `npm run dev` starts storybook and watches for changes
- [ ] Components display correctly in Storybook with interactive controls
- [ ] Changes to a component's `.scss` file are reflected after running `npm run dist`
- [ ] The Drupal site displays your sub-theme correctly with the compiled assets
- [ ] `npm run lint` runs without errors

## Troubleshooting

If you encounter build, Storybook, or cache issues, see the troubleshooting section in the [sub-theme reference](../../development/drupal-theme/sub-theme.md#troubleshooting).

## Next step

With your sub-theme set up and the development workflow verified, the next step is to configure your site's visual identity — colors, header, footer, and other theme settings.

Continue to [Chapter 3: Configuring Colors and Theme Settings](03-colors-and-settings.md).

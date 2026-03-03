## Post-installation cleanup

1.  **Build front-end assets**

    ```bash
    cd themes/<SUBTHEME_MACHINE_NAME>
    nvm use
    npm install
    npm run build
    ```
2. **Commit built assets**
   *   Modify `.gitignore` file in your new theme and remove the following line:

       ```
       dist
       ```
   * Add the following to `.gitignore` in both sub-theme and CivicTheme:
       ```
       .components-civictheme
       .storybook-static
       components_combined
       node_modules
       ```
   * Commit the built assets to your repository
3. **Content Provisioning** (if skipped during installation):
   * See [Content provisioning for CivicTheme](govcms-content-provisioning.md) for detailed instructions
4. Delete the following from CivicTheme:
   - `civictheme_create_subtheme.php`
   - `civictheme_starter_kit` directory

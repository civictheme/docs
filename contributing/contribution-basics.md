---
description: This page outlines the basics for getting started with your contribution
---

# Contribution basics

When you’re ready to start contributing, follow CivicTheme's **contribution model** to ensure your work aligns with the standards for small, medium, or major contributions. Create a new branch to isolate your work:

```bash
git checkout -b feature/your-feature-name
```

* **Small contributions**: Small fixes, minor design tweaks, or documentation improvements.
* **Medium contributions**: Adding new features or extending components.
* **Major contributions**: Major changes requiring the RFC process.

Regardless of the contribution type, be sure to:

* Write **clean, modular code** that is easy to maintain.
* Follow **established design patterns** to ensure consistency with existing components.
* Prioritize **accessibility** and **usability** in your changes to meet CivicTheme’s government-grade standards.



***

### Viewing your changes

While developing, you can view your changes in real-time with the development server running:

```bash
npm run dev
```

Make sure to:

* Test your changes across multiple **devices** and **browsers**.
* Ensure that the new feature or bug fix works for both **desktop and mobile** experiences.
* Verify that your changes are **responsive** and maintain the same level of accessibility.



***

#### Commit and push your changes

Once you’ve completed your contribution and confirmed everything works as expected, commit your changes:

```bash
git add .
git commit -m "Add new button component with hover state"
```

Use descriptive commit messages to make it easy for others to understand the purpose of your changes. Then, push your branch to your GitHub repository:

```bash
git push origin feature/your-feature-name
```



***

### Creating a Pull Request (PR)

After pushing your branch, create a **pull request (PR)** on GitHub to submit your contribution. This will initiate the review process.

1. Navigate to the CivicTheme repository and click **New Pull Request**.
2. **Title** your PR clearly to describe what it addresses.
3. **Link any related issues** (e.g., "Fixes #123") to provide context.
4. **Describe the changes** in detail, explaining what was changed and why.
5. **Include screenshots or examples** if applicable, especially for design-related changes.

Once submitted, the CivicTheme core team will review your PR.



***

### Code review and feedback

Your PR will go through a review process, during which CivicTheme maintainers and contributors will provide feedback or suggestions. Be prepared to:

* **Address requested changes** promptly by making updates to your branch.
* Ensure you **re-test** after making changes to avoid breaking existing functionality.
* Be open to feedback and discussions to improve the quality of the contribution.

Once all feedback is addressed and tests are passing, your contribution will be merged into the main project.



***

### Stay updated

It’s important to keep your fork in sync with the latest updates from the CivicTheme repository to avoid conflicts and ensure you’re working with the most up-to-date code.

To pull the latest changes from upstream:

```bash
git fetch upstream
git merge upstream/main
```

Resolve any conflicts that may arise and push the updated branch back to your repository.



***

### Contributing further

CivicTheme encourages continuous contributions. Whether it’s adding new features, fixing issues, or improving documentation, your input helps the community grow. Regular contributions not only enhance CivicTheme but also give you the opportunity to:

* Build your skills.
* Learn from experienced developers and designers.
* Grow within the CivicTheme community.



***

### Summary of key commands

| **Action**                        | **Command**                                                 |
| --------------------------------- | ----------------------------------------------------------- |
| Clone the repository              | `git clone https://github.com/your-username/civictheme.git` |
| Install dependencies              | `npm install`                                               |
| Create a new branch               | `git checkout -b feature/your-feature-name`                 |
| Start the development server      | `npm run dev`                                               |
| Run tests                         | `npm test`                                                  |
| Commit your changes               | `git add . && git commit -m "commit message"`               |
| Push your branch                  | `git push origin feature/your-feature-name`                 |
| Pull latest changes from upstream | `git fetch upstream && git merge upstream/main`             |



***

## Feedback

We're always looking at ways to improve our documentation for contributions and rely on your feedback to ensure an enjoyable contribution experience. The best way to give us feedback is to join our [Slack channel ](https://drupal.slack.com/archives/C039UV0CQBZ)and chat to us there, or contact us via [email](mailto:support@civictheme.io)!


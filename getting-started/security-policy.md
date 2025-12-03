# Security framework

The CivicTheme security framework outlines the CivicTheme approach to developing, reviewing, and maintaining CivicTheme and its related assets in accordance with secure-by-design principles.&#x20;

It describes the measures, tools, and governance processes used to protect our codebase, users, and community from potential security threats.

CivicTheme is an open-source, government-grade design system comprising multiple components (design assets, UI Kit, and a Drupal theme). Security and compliance are fundamental to CivicTheme’s mission of enabling reliable, consistent, and accessible digital experiences for government and public services.

Note: CivicTheme is an open source codebase, not a hosted service. Implementing organisations are responsible for the security of their own infrastructure and deployments. This policy focuses on the security of CivicTheme’s code and release process.

### Supported versions <a href="#supported-versions" id="supported-versions"></a>

We support the current release of CivicTheme and the accompanying UI Kit.

### Continuous monitoring

Security monitoring is an integral part of the CivicTheme development process. GitHub’s built-in security scanning is enabled across repositories to automatically detect vulnerabilities in code and dependencies. Scans run regularly on commits and pull requests, generating alerts for review, prioritisation, and resolution.

### Linting and static code analysis tools

A suite of linting and static analysis tools supports ongoing quality assurance and helps maintain secure coding standards. These tools automatically run on every commit to detect coding and security issues early.

These include:

* Drupal Practice: ensures compliance with Drupal’s best practices and secure coding guidelines. This helps maintain a consistent, high-quality, and secure codebase.
* PHP CodeSniffer: automatically detects violations of coding standards in PHP, JavaScript, and CSS files. Helps ensure consistent code style, enforces best practices, and can catch potential issues early in development.
* ShipShape: Analyses Drupal code to ensure it follows Drupal coding standards and best practices. Helps detect errors, security risks, and maintainability issues, supporting consistent, high-quality code.
* PHPStan: a static analysis tool for PHP that detects errors in code without running it. Helps catch bugs, type mismatches, and potential issues early, improving code quality and reliability.
* PHP Mess Detector: Scans PHP code for potential problems such as bugs, suboptimal code, and maintainability issues. Helps to  identify complex, error-prone, or poorly structured code so it can be improved.
* PHP Rector: Automates PHP code refactoring and upgrades.Helps to modernise code, fix deprecated features, and enforce coding standards, improving maintainability and compatibility.
* Continuous Integration (CI): Every change is validated via automated testing, linting, and standards enforcement.

### Third-party validation

CivicTheme relies on external dependencies that are carefully managed to maintain a strong security posture. This proactive approach ensures that all third-party components meet the same high security standards as the rest of the CivicTheme codebase.

* **Dependabot:** GitHub Dependabot monitors third-party libraries, alerts the team to vulnerabilities, and automatically generates pull requests with safe updates. Front-end dependencies, such as those within the UI Kit, are also monitored through Dependabot to ensure they remain up to date and secure.&#x20;
* **Composer Security Checker:** works alongside Dependabot to scan PHP project dependencies for known security vulnerabilities and alert the team to packages that need updating.
* **CodeQL Scanning:** GitHub’s CodeQL engine runs static analysis on all commits and pull requests to detect common vulnerabilities in PHP and JavaScript.
* **AI Code Review (CodeRabbit)**: CodeRabbit enhances pull request reviews with automated security checks and best practice enforcement.

### Drupal Security Advisory

CivicTheme is committed to transparency and responsible disclosure when managing security vulnerabilities. As such, CivicTheme has opted into the Drupal Security Advisory. This ensures that vulnerabilities affecting the theme can be responsibly reported, tracked, and communicated to users. &#x20;

By participating in this program, we commit to following the Drupal Security Team’s processes for assessing, prioritising, and releasing security updates, helping maintain a secure environment for all users of the theme.

### Reporting a vulnerability

Find out how to report a vulnerability  on the [Drupal CivicTheme Design System](https://www.drupal.org/project/civictheme) page.<br>

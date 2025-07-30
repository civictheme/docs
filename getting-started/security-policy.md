---
description: >-
  This document outlines security procedures and general policies for the
  CivicTheme project.
---

# Security policy

### Supported versions <a href="#supported-versions" id="supported-versions"></a>

We follow a N and N-1 supported version model.

We support the current and prior minor release of CivicTheme and their accompanying UI Kit.\
This means that if the latest release is 1.8.1 we are supporting the following:

* 1.11.0 (latest release)
* 1.10.0 (last release)

But we are not supporting 1.8.0 or 1.7.3 and below.\
\
In addition to the above model, we will also make available security release patches for the 1.4 version of CivicTheme and 0.9 version due to the difficulty in updating from these models.



***

### Reporting a vulnerability <a href="#reporting-a-vulnerability" id="reporting-a-vulnerability"></a>

The CivicTheme team and community take all security bugs in CivicTheme seriously. We appreciate your efforts to responsibly disclose your findings, and will make every effort to acknowledge your contributions.

&#x20;If you’ve found a vulnerability, we would like to know so we can fix it. Email [civictheme@salsa.digital](mailto:civictheme@salsa.digital) with details of the vulnerability.

Alternatively, information is provided below for disclosing security vulnerability for the Drupal theme and UI Kit.



**How to report**&#x20;

* Use the GitHub Security Advisory "Report a Vulnerability" tab to report the ema
* Emailing us at [civictheme@salsa.digital](mailto:civictheme@salsa.digital)&#x20;
* Contacting us on [Slack](https://drupal.slack.com/archives/C039UV0CQBZ)

\
**What to detail in a disclosure**

* a brief description of the vulnerability
* the CivicTheme version(s) the vulnerability affects
* repository / website where the vulnerability can be observed
* non-destructive steps to replicate the bug

The security team will may ask for additional information or guidance. Report security bugs in third-party modules to the person or team maintaining the module.

***

### **Drupal Theme security disclosures**

Use the CivicTheme’s Drupal Project [Report a Security Issue](https://www.drupal.org/project/civictheme/report-security-issue) issue tracker.



***

### What happens when a vulnerability is reported <a href="#disclosure-policy-security-notifications" id="disclosure-policy-security-notifications"></a>

When the security team receives a security bug report, they will assign it to a primary handler. This person will coordinate the fix and release process, involving the following steps:

* Confirm the problem and determine the affected versions
* Audit code to find any potential similar problems
* Prepare security releases for supported versions
* Prepare patches for earlier supported versions\


**Notifications and releases**

We will provide notifications of security releases and vulnerabilities through the following channels:

* slack: [#civictheme-designsystem](https://drupal.slack.com/archives/C039UV0CQBZ)
* [CivicTheme Project on Drupal.org](https://www.drupal.org/project/civictheme/)
* [CivicTheme UI Kit on GitHub](https://github.com/civictheme/uikit)

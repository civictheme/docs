# Requirements and constraints

{% hint style="info" %}
Requirement levels (MUST, SHOULD, MAY) are used in accordance with [RFC2119](https://www.ietf.org/rfc/rfc2119.txt)
{% endhint %}

### Product requirements

* CivicTheme Drupal theme **MAY** be used out of the box without any customisations.
* CivicTheme Drupal theme **MUST NOT** be changed for customisations. If customisations are required - a consumer theme **MUST** be created and used as a sub-theme of the CivicTheme theme.
* CivicTheme Drupal theme **MUST** be fully compatible with GovCMS SaaS:
  * **MUST NOT** have any modules
  * **MUST NOT** rely on any libraries
  * **MUST NOT** rely on GovCMS content structures
  * **MUST** assume that FE compilation happens on local machine and then committed to the repository
  * **MUST** provide a static version of compiled Storybook for the CivicTheme-based consumer site.

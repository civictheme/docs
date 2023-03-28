# Variables

CivicTheme UI kit contains a large number of variables that modify all areas of the theme.

Variables allow for modification of:

* Theme and component specific colors
* Typography including `line-height`, `font-size`, `font-weight` and which fonts are used
* Spacing
* Grid system

Variables set within the CivicTheme UI kit has a corresponding variable with the `!default` flag that indicates conditional assignment to a variable — it assigns a value only if the variable was previously undefined or `null`. This allows consumer themes to override any the variable's value without needing to change CivicTheme UI kit SASS.

Copy and paste variables as needed into your child theme, modify their values, and remove the `!default` flag. If a variable has already been assigned in your child theme, then it won’t be re-assigned by the default values in CivicTheme component library.

#### Maps

Some of the variables, such as a list of breakpoints or list of colors, are implemented as SASS maps: this allows to override and/or extend the value list. It also provides a safe mechanism to prevent breakages in case if CivicTheme UI kit to introduce a change to the list.

### Where are the variables located

Variables are split into 2 files:

* `_variables.base.scss` - base variables that are used to calculate other variables' values.
* `_variables.components.scss` - variables that control the look of components.

These are split into 2 files to allow changing base variables without the need to provide component variables in custom themes (e.g., to override primary color in child theme and have it propagate to components).

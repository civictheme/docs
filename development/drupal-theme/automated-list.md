# Automated list

The Automated List Component enables editors to create content lists and embed them on any page.&#x20;

It uses a `civictheme_automated_list` paragraph, whose field values are processed by a View preprocessing function. This function maps these values as arguments to a pre-configured `civictheme_automated_list` view.

The component provides configurations via paragraph to a view allowing content type restrictions, show/hide pagination, altering the number of items and filter configuration options.

It is possible to replace the default `civictheme_automated_list` view with a more custom one required for a specific site via `hook_civictheme_automated_list_view_name_alter()` (see [civictheme.api.php](https://github.com/civictheme/monorepo-drupal/blob/develop/web/themes/contrib/civictheme/civictheme.api.php) for details).

CivicTheme also provides support for filters in an exposed form. For views with only 1 exposed filter, Single Filter component (tag based) is enabled, but as soon as there is more than one exposed filter - the Group Filter component (with dropdown filters) is enabled automatically.

{% hint style="info" %}
It is possible to opt-out from automated exposed filters conversion using the `views.CivicThemeOptoutViewsExposedFilter` flag on the theme settings page.
{% endhint %}

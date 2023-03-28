# Automated list

Listing component allows editors to build lists of contents and place them anywhere on the page as a component.

This is achieved by providing a `civictheme_automated_list` paragraph with field values passed to a preprocessing function that is mapped to a pre-configured `civictheme_automated_list` view.

The view provides configurations via paragraph to a view allowing content type restrictions, show/hide pagination, altering the number of items and filter configuration options.

It is possible to replace the default `civictheme_automated_list` view with a more custom one required for a specific site via `hook_civictheme_automated_list_view_name_alter()` (see [civictheme.api.php](https://github.com/salsadigitalauorg/civictheme\_source/blob/develop/docroot/themes/contrib/civictheme/civictheme.api.php) for details).

CivicTheme also provides support for filters in an exposed form. For views with only 1 exposed filter, `Basic Filter` component (tag based) is enabled, but as soon as there is more than one exposed filter - the Large Filter component (with dropdown filters) is enabled automatically.

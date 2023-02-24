# Automated list

### Summary <a href="#automatedlistcomponent-summary" id="automatedlistcomponent-summary"></a>

The Automated list component allows you to add a list of content. It can include any content type in your Drupal site.

The appearance of the content is configurable.

This article will guide you how to add an Automated list component and configure its settings.

### Step 1 - Add the Automated list component <a href="#automatedlistcomponent-step1-addtheautomatedlistcomponent" id="automatedlistcomponent-step1-addtheautomatedlistcomponent"></a>

Under the “Content” tab, click on “Add Automated list” as shown in Figure 1.



### Step 2 - Fill in the available fields in the “Content” tab <a href="#automatedlistcomponent-step2-fillintheavailablefieldsinthe-content-tab" id="automatedlistcomponent-step2-fillintheavailablefieldsinthe-content-tab"></a>

Figure 2 shows a numbered highlighting of the available fields



1.  List Type - The list type values are defined here: _\[your\_domain]/admin/structure/paragraphs\_type/civictheme\_automated\_list/fields/paragraph.civictheme\_automated\_list.field\_c\_p\_list\_type/storage_ (see Figure 3)\




    \
    The allowed values list are Views blocks. You can create custom View blocks and add it to the allowed values list if you need custom lists of content. Once added, it shows up as options as shown in Figure 4.\




    \
    At the Views page, you can duplicate these View blocks as a starter point. You can find the default View blocks here: _\[your\_domain]/admin/structure/views_ (search for “automated” as shown in Figure 5).\



2. Content type - This setting filters the results based on the type of content selected.
3. Metadata - Here you can filter the results based on terms from different taxonomy vocabularies
4.  Limit - This setting depicts how many results are returned. The settings are shown in Figure 6 and the different variations are shown in the table below.\




| **Limit Type**       | **Limit** | **The end result**                                                                                                  |
| -------------------- | --------- | ------------------------------------------------------------------------------------------------------------------- |
| Limited              | 12        | 12 results are displayed.                                                                                           |
| Unlimited            | 12        | 12 results are displayed per page. There will be a pager to take the user to the next page of 12 results and so on. |
| Limited or Unlimited | 0         | All results will be displayed on one page.                                                                          |

5\. Filters - Selecting a filter will expose this as a choice for the site visitor.\




In Figure 7, we selected “Type”. The end result is shown in Figure 8.\



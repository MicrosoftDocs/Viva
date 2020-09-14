---

title: Explore page settings
description: Describes the page settings for Explore pages in Workplace Analytics
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Settings and filters for Explore

You can select **Settings and filters** to view **Page settings** on the right side of the Explore pages in Workplace Analytics. You can use these settings to change the date range, the way to group time investors (a grouping of employees that is used in queries), and the filter for active, inactive, or all employees.

![Settings and filters](../images/wpa/use/settings-and-filters-2.png)

![Page settings](../Images/WpA/Overview/page-settings.png)

When you change the chart settings, they apply to all the charts on all **Explore** pages. For example, when you set the chart to group by *Organization*, all charts in all sections are grouped by organization.

### To apply or reset settings

After you change a setting or add a filter, select **Apply** at the upper-right to apply the settings to the Explore charts. Or to change back to the default settings, select **Reset**.

![Apply button](../images/wpa/use/apply-reset.png)

### To save custom settings and applied filters for later use

After you change page settings or filters:

* Select the **ellipsis** (**...**) next to **Page settings** > **Save current settings** to save them for later use.

![Save settings](../images/wpa/use/save-page-settings.png)

* In **Page settings**, select the **ellipsis** (**...**) next to **Chart settings** > **Apply to page settings** to save specific chart settings, such as with the drilldown or exclude chart tools.

![Chart settings](../images/wpa/use/chart-settings.png)

The next time you open Explore in Workplace Analytics, it shows the charts with the default page settings and filters. To view the custom chart settings saved from earlier, select the **ellipsis** (**...**) next to **Page settings** > **Load saved settings**.

### To change the date range

1. In **Page settings**, expand **Date range**.
2. In **Date range**, select a year and then select a month. 
3. The selected month shows more detail for selecting one or more weeks.
4. Select **Apply** (upper right) to apply these changes to all charts.

> [!Note]
> The date range options encompass the most recently uploaded and processed data with the following logic:
> 
> * A week is defined as Sunday to Saturday, and date ranges are adjusted to span the first Sunday to the last Saturday of the selected range.
> * For a week that starts in one month and ends in the following month, the data is associated with the month in which the week begins.

### To change or add filters

By default, the Explore pages are filtered to show active employees only. Active employees who sent at least one email or instant message during the set date range (the time period set for the query).

![Employee page filter in Explore](../images/wpa/use/explore-filter.png)

1. In **Page settings**, expand **Measured employees**.
2. In **Group by**, select the organizational attribute to use in all charts.
3. Next to **Filters**, select the **Edit** (pencil) icon.  
4. In **Edit page filters**, you can change the **Employees** filter: 

   * **All employees** - Includes inactive and active employees for the set date range.
   * **Active only** - Includes only active employees who have sent at least one email or instant message for the set date range.
   * **Inactive only** - Includes only those inactive employess who have not sent at least one email or instant message for the set date range.
 
5. Select **Add filter** to add one or more additional filters.
6. Select **Apply** (upper right) to apply these changes to all charts.

### To change the number of groups

1. To open the **Page settings** panel, expand **Max groups**.
2. Use **Max groups** to set the number of groups you want the charts to show.  
3. Select **Apply**.

> [!Note]
> The **Max groups** slider moves in increments of 5 (groups). The minimum setting is 10 and the maximum is 100. When you add or remove groups, the scroll bar under the chart adjusts accordingly.

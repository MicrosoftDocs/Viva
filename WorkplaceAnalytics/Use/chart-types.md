---
# Metadata Sample
# required metadata

title: Chart types in Workplace Analytics
description: This article describes the different chart types and how to use the chart features in Workplace Analytics dashboards.

author: rodonahu
ms.author: rodonahu
ms.date: 01/19/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Chart types in Workplace Analytics
This article describes the different chart types and how to use the chart features in Workplace Analytics dashboards.

## Chart types
Workplace Analytics has several different chart types to help visualize your data in a variety of ways.

## About chart data

  * By default, Workplace Analytics groups data by organization, and shows the average metric for the nine largest organizations in the chart, as well as the average for all groups (including any beyond the top nine)
  * Your administrator can set a minimum group size threshold required for data to show in the chart. If the group size is less than the minimum, the group will be disabled. You can see the name of the group, but not the values. When the size of a group equals zero, that group is not shown
  * To see different organizations, or other organizational attributes, use the filters in **Chart display**

## Bar charts
Bar charts compare data across groups. Each bar shows the average value for the metric such as email or meeting hours per person per week in each group for the period selected. 

![Bar chart](../Images/WpA/Use/Bar-chart.png)

### To view the specific values for a group 
* Hover over the bar for the group you want.

### To hide or unhide a metric from the bar chart 
* In the legend below the chart, click the name of the metric to hide it. Click again to show the metric.

## Trend line charts
Trend line charts compare metric values over time. The default trend line is the company average. Each line shows the weekly average for the month for the Group by attribute value you have selected, over a rolling 13-month period. 

![Trend line chart](../Images/WpA/Use/trend-line-chart.png)

### To add a group trend line to the chart  
* Click the corresponding group bar in the adjacent bar chart. 

### To remove a group trend line from the chart, but keep it in the legend
 * Click the corresponding text in the legend. 
 
 ### To remove a group trend line from the chart completely 
 * Click the corresponding bar in the adjacent bar chart. 
 
 ### To reset all added lines from the chart and return to the default view 
*  Click **Reset**. 
 
 ### To view the specific values for a date 
 * Hover over the line on the date you want.
 
 ### To switch between the metrics (such as Emails or Meetings) 
 * Click the text or menu above the chart.

## Distribution charts 
Distribution charts compare the distribution of metric values within a group. Each box plot shows the maximum, minimum, median, upper quartile, and lower quartile for the group for the period selected.

Each individual value within a group represents the average value for a person (for example: the person with the highest average is represented by the maximum point on the box plot).

![Distribution chart](../Images/WpA/Use/Distribution-chart.png)

### To view the distribution statistics for a group 
* Hover over the box plots for that group.

### To switch between the metrics (such as **Emails** or **Meetings**) 
* Click the text above the chart.

## Chart Settings and filters

Use the **Settings and filters** to change the time range of the data, change the attribute you want to see grouped in charts, and apply filters.

When you change chart display settings, your changes will apply to all the charts on all the tabs of **Explore Metrics**. 
For example: When you set chart display to group by _level_, all charts in all sections will be grouped by level.

### To change the date range 
1. If needed, click **Settings and filters**. 
2. Under **Chart display**, in the **Time range** menu, select the period you want and then click **Apply**. 

> [!NOTE]
> The time range options encompass the most recent data loaded and uses the following logic.<ul><li>A week is defined as Sunday to Saturday, and date ranges are adjusted to span the first Sunday to last Saturday of the selected range.</li><li>For a week which starts in one month and ends in the following month, the data is associated with the month in which the week begins.</li></ul>

### To change how the visuals grouped on the page 
1. If needed, click **Settings and filters**. 
2. Under **Chart display**, in the **Group by** menu, select the organizational attribute that you want and then click **Apply**.

### To add filters 
1. If needed, click **Settings and filters**.
2. Under **Filter summary**, click **Add filter**, 
3. Add the filters that you want, and then click **Apply**.



---
# Metadata Sample
# required metadata

title: Charts in Workplace Analytics
description: Describes the different chart types and how to use the chart features in Workplace Analytics. 
author: paul9955
ms.author: madehmer
ms.date: 12/11/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Charts in Workplace Analytics

The [Explore the metrics](explore-intro.md) pages of Workplace Analytics display information in charts. This topic describes those charts and provides information about how to configure and use them. See the following sections:

 * [Chart types](#chart-types). Descriptions of the four primary chart types.
 * [Chart features](#chart-features). Information to help you get the most out of the charts in **Explore**.
 * [Work with charts](#work-with-charts). How to configure the views and the data that charts display and how to download their data. 

## Chart types

[Explore the metrics](explore-intro.md) displays information primarily by using the following chart types:

![column graph](../images/wpa/use/a-column-graph.png) **Column graphs** compare data across groups. The columns run vertically. Each column shows the average value for the metric, such as email or meeting hours, per person, per week, in each group, and for the period selected. For an example, see [Meeting hours by number of attendees](explore-metrics-meetings-overview.md#meetings-hours-by-number-of-attendees).

<!-- ![Column graph](../images/wpa/use/bar-chart.png) -->

![bar chart](../images/wpa/use/b-bar-chart.png) **Bar charts** also compare data across groups. The bars run horizontally. Bar charts are used on the **External collaboration** page. Each bar shows the value for the metric, such as external network size, within a group, for the period selected. For an example, see [Top groups collaborating with external domains](explore-metrics-external-collaboration.md#top-groups-collaborating-with-external-domains). 

<!-- ![Bar chart](../images/wpa/use/19-discover-which-groups.png) -->

![box plot](../images/wpa/use/c-box-plot.png) **Box plots** (also known as distribution charts) show the distribution of metric values within a group. A box plot shows the maximum, minimum, median, upper quartile, and lower quartile for the group for the period selected. Each value within a group represents the average value for a person. For example, the person with the highest average is represented by the maximum point on each box plot in the chart. For example: 

![Box plot](../images/wpa/use/box-plot-general.png)

![line graph](../images/wpa/use/d-line-graph.png) **Line graphs** are used as trend-line charts in that they show metric values over time. The default trend line is the company average for the selected metric. Trend-line charts show one point per week for as many weeks as you have set in **Date range**, under **Page settings**. (See [Change the date range](#to-change-the-date-range)).

For an example, see the chart on the right in [Skip-level meeting hours](explore-metrics-management-and-coaching.md#skip-level-meeting-hours).

<!-- ![Line graph](../images/wpa/use/trend-line-chart.png) -->

## Chart features

### Chart pairs

In most cases, charts appear in pairs. The charts in a pair present related information and can interact with one another. Within a pair, the chart on the left appears by default as a column graph. (Exception: on the **External collaboration** page, the left chart in each pair is a bar chart.) The chart on the left is paired with a line graph:

![chart pair](../images/wpa/use/e-chart-pair.png)

   > [!Note]
   > Within a chart pair, you can [switch the display](#switch-between-chart-types) of the left chart between column graph and box plot.

The column graph displays metric data for groups and the related line graph displays trends, namely values of this metric over time for the selected groups. For example, here is the **Meeting hours by duration** pair of charts in the [Meetings overview](Explore-metrics-meetings-overview.md) tab of the **Explore** page:

![Meeting hours by duration](../images/wpa/use/08-meeting-hours-by-duration.png)

You could view this relationship between the charts in a pair as a sort of "chart workspace" in which you focus on a particular filtered data set and then apply different views to it to coax out different facts. If you sort data in the column chart and then switch it to a box plot, your sorting choices carry over to the display of the box plot. 

### Default display

By default, Workplace Analytics charts display data by employee groups within an organization. Charts show the average metric for each group. Changing the metric changes how the groups are sorted. To learn about changing metrics, see [Sort groups](#sort-groups). 

By default, a column chart (or box plot) displays 30 columns, where each column depicts a group of people. You can [change the number of groups (columns)](#change-the-number-of-groups) that a chart displays.

Charts also display the average for all groups, in the reference line. For more information, see [Reference line](#use-the-reference-line).

### Minimum group size

The Workplace Analytics admin can set a minimum group size threshold, which is required for the group's data to be included in the chart. If the group size is less than the minimum, the group's data is excluded. (The minimum group size can be raised or lowered, but it cannot be set to a number lower than five.)

In the display of a group whose size is smaller than the minimum, you can see the name of the group but not its values. If the size of a group equals zero, the name is also excluded. For more information about setting group size, see [Privacy settings](settings.md#privacy-settings).

### Use of filters

To change or add filters to see different organizations or other organizational attributes, use the available filters for the charts. Filters are set in the **Page settings** area. See [Chart settings and filters](#chart-settings-and-filters).

### Download

You can download any chart in the Explore dashboards as an image or as a .csv file. For more information, see [Download chart data](#to-download-chart-data).

## Work with charts

 * [Chart options](#chart-options). The charts are interactive. In the charts, you can change the chart type, sort the display, download chart data, and select groups for display in the adjacent trend chart.

 * [Chart settings and filters](#chart-settings-and-filters). Use **Page settings** to change the time range of the data, to change the attribute to group in the charts, and to apply filters.  

### Chart options

You can interact with charts in several ways. For example, use the icons above a chart to change its type or to download its data. Click the chart itself to select groups or to see data on the reference line. Click the metric names under the chart to change the display of metrics. 

#### Switch between chart types

In a pair of charts, the chart on the left can display either a column chart or a box plot. The chart on the right displays related trend lines. 

 * To switch to a box plot, select **Change chart type** and then select **Box plot**. 
 * To switch to a column chart, select **Change chart type** and then select **Column chart**. 

After you change chart types, data for the same groups still appears and any selected groups remain selected. This means that the adjacent line graph still displays the trend lines for those same selected groups.

#### Use the reference line to see averages

The height of the reference line shows the value of the metric that is shown in bold in the legend below the chart. For example, if that metric is "Average collaboration hours," the reference line indicates the average number of collaboration hours for the filter group during the time period indicated by the date range. 

 * To see more data about the information that the chart is displaying, hover over the left or right endpoint of the reference line:

   ![Hover over right endpoint of reference line](../images/wpa/use/hover-over-reference.png). 

   This opens a tooltip that displays the averages for the available metrics for this chart type. (These metrics are displayed in the chart legend.) 

#### Sort groups

You can sort any column chart or box plot alphabetically or by any metric that is available in the chart.

 * To sort, select **Sort groups** and then select a metric, such as **Meeting hours** or **Email hours**, or select **Alphabetical**. After you change the sort order, the chart automatically redisplays the data in the new sort order. 

 * To reverse the sort order while sorting by the same metric, select **Sort groups** and then re-select the metric (**Email hours** in the following example): 

   ![Reverse sort order](../images/wpa/use/re-sort-by-metric.png)

##### Sorting by a metric hides small groups

After you sort groups by a metric, an alert icon appears in the bottom-right corner of the chart. This is a tooltip that reminds you that the chart no longer displays groups that are below the minimum group size. 

This functionality protects the privacy of members of groups whose size is below the minimum group size. If a small group were displayed after sorting by a metric, an analyst could infer the small group's value for that metric from its position adjacent to or between other groups, whose values are displayed. If you sort alphabetically, such an inference is not possible, so small groups are not hidden. 

##### Sort order is retained within a chart pair 

A column chart and its related box plot work together. If you sort by a particular choice in the column chart and then switch to the box plot, your sorting choice is also used in the display of the box plot. 

### Work with trend lines

In a chart pair, you use the column chart or box plot on the left to change the display of trend lines in the line graph on the right. Each trend line corresponds to one group (column) in the left chart. 

#### To add a group trend line to the chart

* Select the corresponding group in the adjacent column chart.

#### To remove a group trend line from the chart, but keep it in the legend

* Select the corresponding group name in the legend of the trend chart (below the chart).

#### To remove a group trend line

* Select the corresponding column in the adjacent column chart to remove its line from the trend chart.

#### To reset to the default chart

* At the top of the trend chart, select **Reset**. This removes all added lines from the line graph and returns it to the default.

### Work with metrics

#### To hide or show a metric

* In the chart's legend (below the chart), select the metric name to hide it. Select the metric name again to show it.

<!-- THIS IS THE SAME AS HIDE OR SHOW, CORRECT?
#### To change metrics

 * To change metrics, click the name of a different metric in the legend, below the chart. 
-->

<!--  THIS CHANGED, RIGHT?
#### To switch between metrics

* At the top of the chart, select the metric that you want to show in the chart, such as email hours, meeting hours, percentages, or hours.
-->

### View or download data 

#### To view specific values for a group

* On the chart, hover your cursor over the group's bar to see its data.

#### To view chart value details

* On the chart line, hover the cursor on the date or data to see more details.

#### To view the distribution statistics for a group

* Hover over the chart data for that group.

#### To download chart data 

 * In the toolbar above a chart, select the **Download CSV** icon.

   This download contains the chart data exactly as the chart displays it. If you've applied any filters or [changed the number of groups]() to display, those changes are reflected in the data that is downloaded. 

   Because the download contains just what you see in the chart, you can use the downloaded .csv data in Excel or in Power BI to reproduce the chart that Workplace Analytics displays. 

   > [!Note]
   > Because **Download CSV** gives you only the summarized data shown in the chart, it does not include the query data that was used to generate the chart, so privacy and minimum aggregation rules are adhered to.

### Chart settings and filters

Use **Page settings** to change the time range of the data, to change the attribute to group in the charts, and to apply filters. In the following procedures, if the **Page settings** panel is not already open, open it by selecting **Settings and filters**:

![Settings and filters](../images/wpa/use/settings-and-filters-2.png)

When you change chart display settings, your changes apply to all the charts on all the tabs of **Explore Metrics**. For example, when you set the chart display to group by _level_, all charts in all sections are grouped by that level.

After you make settings, save them by selecting **Apply** in the upper-right corner of the page: 

![Apply button](../images/wpa/use/apply-reset.png)

#### To change the date range

1. Under **Page settings**, expand **Date range**.
2. Under **Date range**, select a year and then select a month. 
3. The selected month displays in more detail in a fly-out window. Use that window to select weeks in the month, one week at a time. 
4. Select **Apply**.

> [!Note]
> The date range options encompass the most recent data that has been loaded and use the following logic:
> * A week is defined as Sunday to Saturday, and date ranges are adjusted to span the first Sunday to last Saturday of the selected range.
> * For a week that starts in one month and ends in the following month, the data is associated with the month in which the week begins.

<!-- WHERE IS THIS?
#### To change how charts are grouped

1. To open the **Page settings** panel, select **Settings and filters**.
2. Under Chart display, in the **Group by** menu, select the organizational attribute to use, and then select **Apply**.
-->

#### To add filters

1. Under **Page settings**, expand **Measured employees**.
2. Next to **Filters**, select the pencil icon. This opens the **Edit page filters** area.  
3. Under **Edit page filters**, select **Add filter**.
4. Add the filters you want and then select **Apply**.

#### To change the number of groups

1. To open the **Page settings** panel, expand **Max groups**.
2. Use the **Max groups** slider to set the number of groups you want the charts to display.  
4. Select **Apply**.
 
The **Max groups** slider moves in increments of 5 (groups). The minimum number of groups that you can display is 10 and the maximum is 100. When you add or remove groups, the scroll bar under the chart adjusts accordingly.

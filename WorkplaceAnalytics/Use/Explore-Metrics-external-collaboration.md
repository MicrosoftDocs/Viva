---

title: Explore External collaboration metrics in Workplace Analytics
description: An overview of the External collaboration dashboards available in Workplace Analytics.
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# External collaboration

**External collaboration** in **Explore** provides a summary of your employees' network patterns with people outside the company. You can use this to understand how certain groups of people within your company spend their time interacting with external domains. Interaction with external domains typically implies collaboration with customers, business partners, or suppliers.  

>[!Note]
> All metrics are reported at a group level and cannot be traced back to any individual.

![External collaboration](../images/wpa/use/external-collab-top.png)

To open **External collaboration**:

1. Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page. If prompted, sign in with your work account.
2. Select **Analyze** > **Explore** > **External collaboration**.

External collaboration features various graphs whose titles suggest different ways to analyze your company's external collaboration activity. Each graph enables you to manipulate data based on menu settings you select and apply to view data in different ways, such as collaboration hours or collaboration cost.

![Explore filters](../images/wpa/use/19-discover-which-groups.png)

## Trend and distribution charts

Most graphs include Trend and Distribution charts also, with some exceptions.

**Trend** charts show changes over time, for example, the trend of the group average, month by month.

**Distribution charts** show the statistical distribution of metrics, such as the minimum, maximum, median, upper and lower percentiles for the group.  

Distribution charts can also tell you whether your data is symmetrical, or how tightly your data is grouped, or whether any outliers exist, and if so, what their values are.
For more information, see [Workplace Analytics Charts](../use/chart-types.md).

## Summary header

The summary header at the top of the external collaboration page provides a summary of the results of external collaboration during the selected period, as shown in the image.

![Collaboration summary](../images/wpa/use/ext-collab-summary.png)

Explanation of numbered sections:

1. This section shows a summary of the external collaboration and the level of engagement during the selected period.
2. **Measured employees** are those employees who have been assigned a Workplace Analytics license. (Any filters applied in [Page settings](#page-settings) do not change this number.)
3. The filter group comprises the number of employees who had some collaboration during the date range and who match the filter applied in [Page settings](#page-settings).
4. This number represents the estimated cost of external collaboration with external domains, calculated by using the formula: total external collaboration hours multiplied by the average hourly wage for your company. This is configured by your Workplace Analytics administrator.
5. This number represents the percentage of measured employees in your company who had one or more external interactions during the selected period.
6. This number represents external collaboration hours as a percentage of the total collaboration hours spent by the measured employees in your company.
7. This number represents the total number of external people with whom the measured employees have collaborated at least once during the selected period. This number does not change with any filter applied in [Page settings](#page-settings).

## Top external domains

The following graph shows the top external domains that people in the company spend the most time with. You can pivot the data by using various settings, such as total collaboration hours, total collaboration cost, or number of employees engaged.

>[!Note] 
> Personal email domains, for example, hotmail.com or live.com, are included in overall metric calculations but are hidden from the top external domains chart to reduce "noise."  

![External domains](../images/wpa/use/31-ext-domains-most-time.png)

**Bar chart**

The horizontal bar chart shows the top ten domains that your people collaborate with, sorted in descending order, based on the selected drop-down menu option. You can scroll to see more domains. 

*Total collaboration hours*

When you select this menu option, each bar in the graph represents the total number of hours that measured employees collaborated with a particular domain. For example, the first bar in the chart represents the number of hours of collaboration with contoso.com. The bars are sorted by hours (in descending order).

*Total collaboration cost*

When you select this menu option, each bar represents the total number of hours that measured employees collaborated with a domain, multiplied by the average hourly wage for your company, as configured by your Workplace Analytics administrator. For example, the first bar in the chart represents the total cost of collaboration with contoso.com. The bars are sorted by cost (in descending order).

*Total employees engaged*

When you select this menu option, each bar represents the total number of distinct measured employees from your company who have collaborated with a domain. For example, the first bar in the chart represents the number of measured employees who have interacted with contoso.com.

**Trend chart**

The "group total" in the trend chart represents the total weekly collaboration hours of all measured employees of your company with all external domains over the selected period in [Page settings](#page-settings). You can select additional domains in the bar chart to plot their trend over the selected period.

**Distribution chart**

Each box in this chart represents the five-number summary for the total collaboration hours or total collaboration cost spent by all measured employees with a particular domain,  for example, contoso.com. The five-number summary includes minimum, maximum, median, and upper and lower quartiles for the dataset. Distribution boxes are sorted by the maximum values descending.

The Distribution chart is not available when the "employees engaged" menu option is selected.

## Top groups collaborating with external domains

The following graph shows which groups in your company spend the most time collaborating with external domains, where the group-by attribute is defined in the Time investors section in [Page settings](#page-settings). For time investors, the default group-by attribute is "Organization."

You can pivot the data by using various settings, such as collaboration hours, meeting hours, meeting count, or collaboration cost.

![External group collaboration](../images/wpa/use/32-groups-most-time-collab-ext-people.png)

**Bar chart**

*Collaboration hours*

When you select this menu option, each bar represents the weekly average number of collaboration hours that measured employees in that group have spent with external domains, where the weekly average for each group represents the sum of collaboration hours during all selected weeks divided by the number of person-week records in the selected period for that group in Page settings.

Collaboration hours represents the sum of email collaboration hours and meeting collaboration hours spent with external domains. Bars are sorted by hours in descending order.

The Average line on bar charts represents the sum of all collaboration hours during all selected weeks divided by the number of person-week records in the selected period in Page settings.

*Meeting hours*

The same definition applies here as for collaboration hours, but in this case, only meeting hours are included.

*Email hours*

The same definition applies here as for collaboration hours, but in this case, only email hours are included.

*Meeting count*

When you select this menu option, each bar represents the weekly average meeting count that measured employees in that group have organized with external domains, where the weekly average for that group is the sum of meeting count during all selected weeks divided by the number of person-week records in the selected period for that group in [Page settings](#page-settings). Bars are sorted on count (descending).

The Average line on bar charts represents the sum of all meeting counts during all selected weeks divided by the number of person-week records in the selected period in **Page settings**.

*Email count*

The same definition applies here as for meeting count, but in this case, only email counts are included.

*Collaboration cost*

When you select this menu option, each bar represents the weekly average collaboration cost that measured employees in that group have incurred with external domains, where the weekly average for that group is the sum of the collaboration cost during all selected weeks divided by the number of person-week records in the selected period for that group in Page settings.  

Collaboration cost represents total collaboration hours multiplied by the average per-hour wage for your company. Bars are sorted on hours in descending order.

The Average line on bar charts represents the total collaboration cost during all selected weeks divided by the number of person-week records in the selected period in Page settings.

*Trend chart*

The group average point for a given week is the sum of all collaboration, meeting, email hours, count, and cost divided by the number of person-domain records for that week.

The group average point for a given week for a selected group is the sum of all collaboration/meeting/email hours, count, or cost for that group with external collaborators divided by the number of person-domain records for that week for that group.

*Distribution chart*

Each box in this chart represents the five-number summary of the number of hours or cost or count incurred by all measured employees with a particular group, for example, the Services organization. The summary includes minimum, maximum, median, upper and lower quartiles for the dataset. Distribution boxes are sorted by maximum values descending.

## Groups with most people collaborating with external domains

The following graph shows which groups in your company have the most people collaborating with external domains where the group-by attribute is defined in the Time investors section in [Page settings](#page-settings). By default, the group-by attribute is "Organization" for time investors.  

![External collaborators](../images/wpa/use/33-most-people-collab.png)

**Bar chart**

*Total employees engaged*

Each bar in the chart represents the total number of distinct measured employees in the group (grouped by the investor group-by attribute in page settings) who have collaborated with any external domain. For example, the first bar in the chart represents the number of employees in the Services organization who have collaborated with any external domain.

**Trend chart**

 In the trend chart, the "group total" represents the total count of distinct measured employees across all groups in your company (grouped by the time investor group-by attribute in [Page settings](#page-settings)) with all external domains over the selected period. You can select additional groups in the bar chart to plot their trends over the selected period.

## External network size and external network breadth

External network size and external network breadth show the extent to which persons within a company interact with people outside the company. For example, a sales person tends to have a greater external network size and breadth than a person whose company role is mainly internal.

### External network size

External network size refers to the number of people external to the company with whom a person had at least two meaningful interactions within the last 28 days (or if reported by month, within the last month).

![External connections](../images/wpa/use/34-groups-most-ext-people-conn.png)

**Bar chart**

Each bar in the graph represents the average external network size for each group (grouped by the investor group-by attribute in Page settings). Average external network size is defined as the total number of non-distinct external contacts with whom the measured employees from this group had two meaningful interactions in all selected weeks, divided by number of person-week records in the selected date range in Page settings. 

The Average line on this bar chart is the sum of the external network size during all selected weeks divided by the number of person-week records in the selected period in Page settings.

**Trend chart**

The group average point for a given week is the sum of the external network size divided by the number of person-domain records for that week.

**Distribution chart**

Each box in this chart represents the five-number summary of the external network size of the selected group, for example, the Purchasing organization. The five-number summary includes minimum, maximum, median, and upper and lower quartiles for the dataset. Distribution boxes are sorted by the maximum values in descending order.

### External network breadth

External network breadth refers to the number of distinct external domains with whom a person had at least two meaningful interactions within the last 28 days (or if reported by month, within the last month). (A meaningful interaction consists of an email, meeting, call, or three instant messages involving from two to eight people.)

![External network breadth](../images/wpa/use/35-ext-collab-network-breadth.png)

**Bar chart**

Each bar in the graph represents the total number of distinct external domains with whom measured employees from this group had two meaningful interactions in the selected date range in [Page settings](#page-settings).

The Average line on this bar chart represents the total number of distinct external domains with whom the measured employees in the company had at least two meaningful interactions in the selected date range divided by the total number of organizations.

**Trend chart**

The "group average" point for a given week in the trend chart represents the total number of distinct external domains with whom the measured employees in the company had at least two meaningful interactions in the selected date range divided by the total number of organizations for that week.

The "group average" point per week for each selected group in the trend chart represents the total number of distinct external domains with whom the measured employees in the selected group had at least two meaningful interactions in that week.

**Distribution chart**

Each box in this chart represents the five-number summary for the external network breadth for a particular group,  for example, the Purchasing organization. The five-number summary includes the minimum, maximum, median, and upper and lower quartiles for the dataset. Distribution boxes are sorted on maximum values descending.

### External network breadth compared to external network size

The graph for External network breadth compared to external network size shows how each group in the company (grouped by the Time investor group-by attribute in Page settings) compares to the company median for External network size and breadth. The size of the bubble in the chart represents the size of the organization.

![External group connections](../images/wpa/use/36-ext-collab-groups-ext-conn.png)

External network size shows the number of external people that persons in the company have connected with.

External network breadth shows the number of unique external domains that persons in the company have connected with.

The following example explains the distinction between external network size and external network breadth. If you are a sales employee, network size shows how many external people you talked to. If you talked to 20 people in contoso.com, then your network size would be equal to 20.

External network breadth shows how many outside groups or domains you talked to. For example, if you had only talked to contoso.com, then your external network breadth would be equal to one. If you had talked to both contoso.com and adatum.com, your external network breadth would be equal to two.

For example, the previous bubble graph poses a question about external network breadth compared to external network size. You could use this graph to help you determine whether small groups in your company might be making a significant number of external connections. Conversely, the graph could show you whether big groups are making relatively few external connections.  

In the bubble graph, if the bubble for your organization is found at the top right, this means that your organization has made the most external connections and contacted the greatest number of unique domains in the selected period.  

## Page settings

 You can use **Page settings**, which is common to all sections of Explore, to choose the date ranges for the various charts, to apply filters to a chart’s dataset or change filters. For more information, see [Settings and filters for explore](explore-page-settings.md).

![Page settings](../images/wpa/use/37-ext-collab-page-settings-home.png)

### Group by

You can use the Group by drop-down menu to determine how you want to group users by selecting and applying various settings.

The Group by menu is divided into two sections for two separate groups: **Time investors** and **Collaborators**. You can apply Group by menu settings to each of these groups independently.

![Group by menu](../images/wpa/use/38-ext-collab-group-by.png)

### Time investors

The **Time investors** section includes various settings for grouping Time investors, which refers to people in the organization who have been assigned a Workplace Analytics license.

By default, Time investors are grouped by organization, but you can also group them by domain, engagement, or other settings to retrieve the data you want. If you group by Time investors, the settings you select apply only to Time investors.  

![Time investors group](../images/wpa/use/39-ext-collab-page-settings-time-investors-dec.png)

### Collaborators

You can use the **Collaborators** section to group users by Collaborators, which refers to any person with whom Time investors have had an interaction. If you group by Collaborators, the settings you select only apply to Collaborators. Currently, the Collaborators section supports grouping by domain only.

![Collaborators group](../images/wpa/use/ext-collab-page-settings-collaborators.png)

>[!Note]
> Currently, you cannot apply the Collaborators filter for the External network size, External network breadth, and bubble charts in the Network section. However, it applies to all the other charts on the page.

## Related topics

* [Explore page settings](../use/explore-page-settings.md)
* [Workplace Analytics Charts](../use/chart-types.md)
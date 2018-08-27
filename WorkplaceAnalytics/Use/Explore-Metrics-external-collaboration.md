---
# Metadata Sample
# required metadata

title: Explore External collaboration metrics in Workplace Analytics
description: An overview of the External collaboration dashboards available in Workplace Analytics.
author: buntus
ms.author: v-johtob
ms.date: 08/08/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# External Collaboration

**External collaboration** in **Explore** provides a summary of your employees’ network patterns with people outside the company. You can use this to understand how certain groups of people within your company spend their time interacting with external domains. Interaction with external domains typically implies collaboration with customers, business partners, or suppliers.  

>[!Note]
>All metrics are reported at a group level and cannot be traced back to any individual.

[!INCLUDE [To open the Workplace Analytics Settings page](../includes/to-open-wpa-explore.md)]


External collaboration features various graphs whose titles suggest different ways to analyze your company's external collaboration activity. Each graph allows you to manipulate data based on menu settings you select and apply, such as collaboration hours or collaboration cost.

![Explore filters](../images//WpA/Use/groups-most-time-collab-ext-people.png)


## Trend and Distribution graphs

Most graphs also include Trend and Distribution graphs, with some exceptions.

**Trend** graphs show changes over time, for example, the trend of the group average, month by month.

Distribution graphs show the statistical distribution of metrics, such as the minimum, maximum,  median, upper and lower percentiles for the group.  

Distribution graphs can tell you whether your data is symmetrical, how tightly your data is grouped, or whether any outliers exist, and if so, what their values are.
For more information, see [Workplace Analytics Chart types](../Use/chart-types).

The header at the top of the External collaboration page provides a summary of the results of external collaboration during the selected period, as shown in the image.

![Collaboration summary](../images/WpA/Use/ext-collab-summary.png)

Explanation of numbered sections:  
1. This section shows a summary of the external collaboration and the level of engagement during the selected period. 
2. **Measured employees** are those employees who have been assigned a Workplace Analytics license. (This number does not change with any filter applied in [Page settings](#page-settings).
3. The filter group represents the number of employees who have had some collaboration during the date range and who match the filter applied in [Page settings](#page-settings).
4. This number represents the estimated cost of external collaboration with external domains, calculated by using the formula: total external collaboration hours multiplied by the average hourly wage for your company, which is configured by your Workplace Analytics administrator).
5. This number represents the percentage of measured employees in your company who had one or more external interactions during the selected period.
6. This number represents external collaboration hours as a percentage of the total collaboration hours spent by the measured employees in your company.

7. This number represents the total number of external people with whom the measured employees have collaborated at least once during the selected period. This number does not change with any filter applied in [Page settings](#page-settings).

## Top external domains

The following graph shows the top external domains that people in the company spend most time with. You can choose to pivot the data on various settings, such as total collaboration hours, total collaboration cost, or number of employees engaged.

![External domains](../images/WpA/Use/ext-domains-most-time.png)

**Bar chart**

The horizontal bar graph shows the top ten domains that your people  collaborate with, sorted in descending order, based on the selected drop-down menu option. You can scroll to see more domains. 

*Total collaboration hours*

When this menu option is selected, each bar in the graph represents the total number of hours that measured employees have collaborated with a particular domain. For example, the first bar in the chart represents the number of hours of collaboration with contoso.com. The bars are sorted  by hours (descending). 

*Total collaboration cost*

When this menu option is selected, each bar represents the total number of hours that measured employees have collaborated with contoso.com, multiplied by the average hourly wage for your company, as configured by your Workplace Analytics administrator. For example, the first bar in the chart represents the total cost of collaboration with contoso.com. Bars are sorted  by cost (descending).

*Total employees engaged*

When this menu option is selected, each bar represents the total number of distinct measured employees from your company who have collaborated with a particular domain (contoso.com). for example, the first bar in the chart represents the number of measured employees who have interacted with contoso.com. 

**Trend chart**

The ‘group total’ in the trend chart represents the total weekly collaboration hours of all measured employees of your company with all external domains over the selected period in Page settings. You can select additional domains in the bar chart to plot their trend over the selected period in the same chart.

**Distribution chart**

Each box in this chart represents the five-number summary for the total collaboration hours or total collaboration cost spent by all measured employees with a particular domain,  for example, contoso.com. The five-number summary includes: minimum, maximum, median, and upper and lower quartile for the dataset. Distribution boxes are sorted on maximum values descending.

The Distribution chart is not available when the ‘employees engaged’ menu option is selected.


## Top groups collaborating with external domains

The following graph shows you which groups in your company spend the most time collaborating with external domains, where the group-by criterion is defined in the ‘Time investors’ section in Page settings. By default, the group-by criterion is "Organization for time investors". 

You can choose to pivot the data on various settings, such as collaboration hours, meeting hours, meeting count, collaboration cost, and so forth.

![External group collaboration](../images/WpA/Use/groups-most-time-collab-ext-people.png)

**Bar chart**

*Collaboration hours*

When this menu option is selected, each bar represents the weekly average number of collaboration hours that measured employees in that group have spent with external domains, where weekly average is the sum of collaboration hours during all selected weeks divided by the number of weeks in the selected period in Page settings. Collaboration hours  represents the sum of email collaboration hours and meeting collaboration hours spent with external domains. Bars are sorted on hours (descending).

The Average line on bar charts represents the average of averages, which is the sum of the average collaboration hours for each group divided by the number of groups. The average for a group is the sum of collaboration hours during all selected weeks divided by the number of weeks in the selected period in Page settings.

*Meeting hours*

Same definition as for collaboration hours, but only meeting hours are considered in this case.

*Email hours*

Same definition as for collaboration hours, but only email hours are considered in this case.

*Meeting count*

When this menu option is selected, each bar represents the weekly average meeting count that measured employees in that group have organized with external domains, where weekly average is the sum of meeting count during all selected weeks divided by the number of weeks in the selected period in Page settings. Bars are sorted on hours (descending).

The Average line on bar charts represents the average of averages, which is the sum of the average of meeting count for each group divided by the number of groups. The average for a group is the sum of meeting count during all selected weeks divided by the number of weeks in the selected period in Page settings.

*Email count*

The same definition applies here as for meeting count, but in this case, only email counts are considered

*Collaboration cost*

When this menu option is selected, each bar represents the weekly average collaboration cost that measured employees in that group have incurred with external domains, where weekly average is the sum of collaboration cost during all selected weeks divided by the number of weeks in the selected period in Page settings.

Collaboration cost represents total collaboration hours multiplied by the average per hour wage for your company. Bars are sorted on hours (descending).

The Average line on bar charts represents the average of averages, which is the sum of the average of collaboration cost for each group divided by the number of groups. The Average for a group is the total collaboration cost during all selected weeks divided by the number of weeks in the selected period in Page settings.

*Trend chart*

The ‘group average’ in the trend chart represents the average of averages for a week, which is the sum of average hours, count, or cost for each organization divided by the number of organizations. The average for a group is the sum of hours, count, or cost during all selected weeks divided by the number of weeks in the selected period in Page settings.

*Distribution chart*

Each box in this chart represents the five-number summary of the number of hours or cost or count spent by all measured employees with a particular group,  for example, the Services organization. The five-number summary includes minimum, maximum, median, upper and lower quartiles for the dataset. Distribution boxes are sorted by maximum values descending.



The following graph shows you which groups in your company have the most number of people collaborating with external domains where the group-by criterion is defined in the ‘Time investors’ section in Page settings. By default, the group-by criterion is ‘organization’ for time investors. 

![External network size](../images//WpA/Use/most-people-collab.png)

**Bar chart**

*Total employees engaged*

Each bar in the graph represents the total number of distinct measured employees in the group (grouped by the investor group-by attribute in page settings) who have collaborated with any external domain. For example, the first bar in the chart represents the number of employees in the Services organization who have collaborated with any external domain.


**Trend chart**

The ‘group total’ in the trend chart represents the total count of distinct measured employees across all groups of your company (grouped by the investor group-by attribute in page settings) with all external domains over the selected period. You can select additional groups in the bar chart to plot their trend over the selected period in the same chart.


## External network size and external network breadth

External network size and external network breadth help to show the extent to which persons within a company interact with people outside the company. For example, a sales person tends to have a greater external network size and breadth than a person whose company role is mainly internal.  

## External network size

External network size refers to the number of people external to the company with whom a person had at least two meaningful interactions within the last 28 days (or if reported by month, within the last month).

![External network size](../images//WpA/Use/groups-most-ext-people-conn.png)



**Bar chart**

*External network size*

Each bar in the graph represents the average external network size for each group (grouped by the investor group-by attribute in Page settings). Average external network size is defined as the total number of non-distinct external contacts with whom the measured employees from this group had two meaningful interactions in all selected weeks, divided by number of weeks in the selected date range in Page settings.

The Average line on bar charts represents the average of averages external network size, which is the sum of average external network size for each organization divided by the total number of organizations.

**Trend chart**

The ‘group average’ in the trend chart represents the trend of average of averages of external network size, which is the sum of average external network size for each organization divided by the number of organizations.


**Distribution chart**

Each box in this chart represents the five-number summary of the external network size for a particular group, for example, the Purchasing organization. The five-number summary includes minimum, maximum, median, and upper and lower quartile for the dataset. Distribution boxes are sorted on maximum values descending.

>[!Note] 
> Collaboration filters cannot be currently applied for this chart.









**Bar chart**

*External network size*

This bar represents the average external network size for the organization, which is the total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions in all selected weeks, divided by number of weeks in the selected date range in the page filters on the right.

The Average line on bar charts represents the average of averages external network size, which is the sum of average external network size for each organization divided by the total number of organizations.
 
**Trend chart**

Group average is the trend of average of averages of external network size, which is the sum of average external network size for each organization divided by the number of organizations.

**Distribution chart**

Each box shows minimum, maximum, median, upper and lower quartile external network size for measured employees from each organization.

>[!Note]
> Collaboration filters cannot be applied for this chart.

## External network breadth

External network breadth refers to the number of distinct external domains with whom a person had at least two meaningful interactions within the last 28 days (or if reported by month, within the last month).

![External network breadth](../images/WpA/Use/ext-collab-network-breadth.png)

**Bar chart**

Each bar in the graph represents the average external network breadth for each group (grouped by the investor group-by attribute in Page settings). Average external network breadth is defined as the total number of distinct external domains with whom the measured employees from this group had two meaningful interactions in all selected weeks, divided by the number of weeks in the selected date range in Page settings.

The Average line on bar charts represents the average of averages external network breadth, which is the sum of average external network breadth for each organization divided by the total number of organizations.

 
**Trend chart**

The ‘group average’ in the trend chart represents the trend of average of averages of external network breadth, which is the sum of average external network breadth for each organization divided by the number of organizations.

**Distribution chart**

Each box in this chart represents the five-number summary for the external network breadth for a particular group,  for example, the Purchasing organization. The five-number summary includes: minimum, maximum, median, and upper and lower quartile for the dataset. Distribution boxes are sorted on maximum values descending.

>[!Note]
> Collaboration filters cannot be currently applied for this chart.


## External network breadth compared to external network size

The External network breadth compared to external network size graph shows how each group (grouped by the investor group-by attribute in page settings) in the company compares to the company median for External network size and breadth. The size of the bubble in the graph represents the size of the organization.

![External group connections](../images/WpA/Use/ext-collab-groups-ext-conn.png)

External network size shows you the number of external people that persons in the company have connected to.

External network breadth shows you the number of unique external domains that persons in the company have connected to.

An example illustrates the distinction between external network size and external network breadth. If you are a sales employee, network size shows how many people you have been talking to. If you had talked to 20 people in contoso.com, then your network size would be equal to 20.

External network breadth shows how many outside groups or domains you have been talking to. If you had only talked to contoso.com, then your external network breadth would be equal to one. If you had been talking to both contoso.com and adatum.com, your external network breadth would be equal to two.

For example, the previous bubble graph poses a question about external network breadth compared to external network size. You could use it to help you determine whether small groups in your company might be making a significant number of external connections. Conversely, the graph could show you whether big groups are making relatively few external connections. 

In the bubble graph, if the bubble for your organization is found at the top right, this means that your organization has made the most external connections and contacted the greatest number of unique domains.


## Page settings

[Page settings](#page-settings),  common to all sections of Explore, can help you choose the date ranges you want to see for the various charts, or apply filters to a chart’s dataset.

![Page settings](../images//WpA/Use/ext-collab-page-settings-home.png)

### Group by

In the Group by menu, you can select and apply various settings to determine how you want to group users.

![Group by menu](../images//WpA/Use/ext-collab-group-by.png)

The **Group by** drop-down menu is divided into two sections that represent two separate groups: **Time investors** and **Collaborators**. You can apply Group by menu settings to each of these groups independently.  

### Time investors
The **Time investors** section offers various options for grouping **Time investors**, which refers to people in the organization who have been assigned a Workplace Analytics license.

By default, Time investors are grouped by organization, but you can also group them by domain, engagement, or various other settings to retrieve the data you want. If you group by Time investors, the settings you select apply to Time investors only.

![Time investors group](../images//WpA/Use/ext-collab-page-settings-time-investors.png)

### Collaborators
You can use the Collaborators section to group users by Collaborators, which refers to any person with whom Time investors have had an interaction. If you group by Collaborators, the settings you select apply to Collaborators only. Currently, the Collaborators section supports grouping by domain only. 

![Collaborators group](../images//WpA/Use/ext-collab-page-settings-collaborators.png)


>[!Note]
> Applying Group by menu settings to the Collaborators group currently affects all the collaboration graphs simultaneously, with the exception of the domain-related graphs.

### Filters

In the Filters section of Page settings, you can apply filters by selecting **Edit**.

![Edit filters section](../images/WpA/Use/edit-filters.png)

Edit Page filters opens. opens. Here you can choose the filters you want. Selecting the **Apply** button activates the filter, which modifies individual graph results.

![Edit page filters](../images/WpA/Use/edit-page-filters.png)

































The next graph allows you to see which groups in your company have made the most connections with external people.

![Top group external connections](../images/WpA/Use/groups-most-people-conn.png)

**Bar chart**

*External network size*

This bar represents the average external network size for each organization, which is the total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions in all selected weeks divided by the number of weeks in the selected date range in the page filters on the right.

The average line on bar charts represents the average of averages external network size, which is the sum of the average external network size for each organization divided by total number of organizations.

The average external network size for each organization is the total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions divided by the number of measured employees in that organization.

> [!Note]
> Collaboration filters cannot be applied for this chart.

**Trend chart**

*Group average*

The group average is the trend of average of averages of external network size. This is the sum of the average external network size for each organization divided by the number of organizations, where the average external network size for each organization is total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions divided by number of measured employees in that organization.

**Distribution chart**

Each bar shows external network size (minimum, maximum, median, upper and lower quartile) for measured employees from each organization.



LOOSE CHART. MAYBE DELETE
The next graph shows you which groups in your organization are making the most external people connections.

![External network size](../images//WpA/Use/groups-most-ext-people-conn.png)

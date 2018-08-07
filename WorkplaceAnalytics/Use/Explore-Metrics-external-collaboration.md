---
# Metadata Sample
# required metadata

title: Explore External collaboration metrics in Workplace Analytics
description: An overview of the External collaboration dashboards available in Workplace Analytics.
author: buntus
ms.author: v-johtob
ms.date: 06/05/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# External Collaboration

**External collaboration** in **Explore** allows you to gain valuable insights into the  networking patterns of the people in your company by highlighting their connections and interactions with people and groups external to the company. 

[!INCLUDE [To open the Workplace Analytics Settings page](../includes/to-open-wpa-explore.md)]

**Explore** provides a summary of the results of external collaboration during the selected period as shown in the image.

![Collaboration summary](../images/WpA/Use/ext-collab-summary.png)

The numbered sections are explained as follows:  
1. This section shows a summary of the external collaboration and level of engagement during the selected period. 
2. **Measured employees** are those employees who have been assigned a Workplace Analytics license. This represents the number of measured employees in the tenant. (This number does not change with any filter applied in **Filters**).
 
3. The **filter group** represents the number of employees who match the filter applied in [Page settings](#page-settings).
4. This number represents the estimated total cost of external collaboration with external domains, calculated using the formula: total external collaboration hours x the average hourly wage for that tenant (from tenant's configuration).
5. This number represents the percentage of measured employees who have had one or more external contacts during the selected period. The percentage = the number of measured employees who had at least one external interaction (that is, external collaboration hours > 0/total measured employees) x 100.
6. This number represents external collaboration hours as a percentage of the total collaboration hours spent by measured employees. The percentage = number of external collaboration hours/number of total collaboration hours) x 100.
7. This number represents the total number of external people with whom the measured employees have collaborated at least once during the selected period. (that is, external collaboration hours > 0). (This number does not change with any filter applied in the filter pane).

**External collaboration** features various graphs whose titles suggest different ways to analyze your company's external collaboration activity.
Each graph allows you to manipulate data based on settings you can choose and apply from a drop-down menu, such as collaboration hours or collaboration cost.  

![Explore filters](../images//WpA/Use/groups-most-time-collab-ext-people.png)

## Trend and Distribution graphs

Each graph also contains **Trend** and **Distribution** graphs.

**Trend** graphs show changes over time, for example, the trend of the group average, month by month.
**Distribution** graphs show the statistical distribution of metrics, such as the minimum and maximum of the group, the median, and upper and lower percentiles. 

**Distribution graphs** can tell you whether your data is symmetrical, how tightly your data is grouped, or whether there are any outliers, and if so, what their values are. For more information, see [Workplace Analytics Chart types](../Use/chart-types).

## Page settings

**Page settings**, common to all sections in **Explore**, can help you gain further insights into your company's external networking patterns.

![Page settings](../images//WpA/Use/ext-collab-page-settings-home.png)

### Group by

**Page settings** features the **Group by** drop-down menu, from which you can select and apply various settings to determine how you want to group users.

![Group by menu](../images//WpA/Use/ext-collab-group-by.png)

The **Group by** drop-down menu is divided into two sections that represent two separate groups: **Time investors** and **Collaborators**. You can apply Group by menu settings to each of these groups independently.  

### Time investors
The **Time investors** section offers various options for grouping **Time investors**, which refers to people in the organization who have been assigned a Workplace Analytics license.

By default, **Time investors** are grouped by organization, but you can also group them by domain,  engagement, FunctionType, or other settings to retrieve the data you want. If you choose to group by **Time investors**, the settings you select here are applied to Time investors only.  

![Time investors group](../images//WpA/Use/ext-collab-page-settings-time-investors.png)

### Collaborators
The **Collaborators** section allows you to group users by **Collaborators**, which refers to any person with whom Time investors have had an interaction. The settings you select in **Collaborators** are applied to Collaborators only. Currently, Collaborators supports grouping by domain only.  

![Collaborators group](../images//WpA/Use/ext-collab-page-settings-collaborators.png)



>[!Note]
> Applying any **Group by** menu settings to the **Collaborators** group currently affects all the collaboration graphs simultaneously, with the exception of domain-related graphs.

### Filters

In the **Filters** section of **Page settings**, you can apply filters by selecting the **Edit** button. 

![Edit filters section](../images/WpA/Use/edit-filters.png)

**Edit Page filters** opens. Here you can choose the filters you want. Selecting the **Apply** button activates the filter, which modifies individual graph results.

![Edit page filters](../images/WpA/Use/edit-page-filters.png)

## External network size and external network breadth
External network size and external network breadth help show the extent to which persons within a company interact with people outside the company. For example, a sales person would tend to have a greater external network size and breadth than a person whose company role was purely internal.

## External network size 
External network size refers to the number of people external to the company with whom a person had at least two meaningful interactions within the last 28 days (or if reported by month, within the last month).

![External network size](../images//WpA/Use/most-people-collab.png)

**Bar chart**

*Total employees engaged*

This bar represents the total number of distinct tenant measured employees in an organization who have collaborated with any external domain.
There is no **Average** line on bar charts.

**Trend chart**

*Group total*

This represents the total count of distinct measured employees across all organizations who have engaged with any external domains in a week.
 
**Distribution chart**

For **number of employees engaged** there is no distribution to show.

The next graph allows you to see which groups in your organization are making the most external people connections.

![External network size](../images//WpA/Use/groups-most-ext-people-conn.png)

**Bar chart**

*External network size*

This bar represents the average external network size for the organization = the total number of external contacts with whom the measured employees from this organization had at least two meaningful interactions in all selected weeks divided by number of weeks in the selected date range in the page filters on the right.

*Average*
 
The Average line on bar charts represents the average of averages external network size = sum of average external network size for each organization divided by the total number of organizations.
 
**Trend chart**

Group average = trend of average of averages of external network size = sum of average external network size for each organization divided by the number of organizations.

**Distribution chart**

Each bar shows external network size (minimum, maximum, median, upper and lower quartile) for measured employees from each organization.

>[!Note]
> Collaboration filters cannot be applied for this chart.

## External network breadth
**External network breadth** refers to the number of distinct domains external to the company with whom a person had at least two meaningful interactions within the last 28 days (or if reported by month, within the last month).

![External network breadth](../images//WpA/Use/ext-collab-network-breadth.png)

**Bar chart**

This bar represents the average external network size for the organization = total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions in all the selected weeks divided by number of weeks in the selected date range in the page filters on the right.

*Average*
 
The Average line on bar charts represents the average of averages external network size = sum of average external network size for each organization divided by the total number of organizations.
 
**Trend chart**

Group average = trend of average of averages of external network size = sum of average external network size for each organization divided by the number of organizations.

**Distribution chart**

Each bar shows external network size (minimum, maximum, median, upper and lower quartile) for measured employees from each organization.

## External network breadth compared to external network size
The **External network breadth compared to external network size** graph shows how each organization in the company compares to the company median for **External network size and breadth**.

![External group connections](../images/WpA/Use/ext-collab-groups-ext-conn.png)

**External network size** shows you the number of external people that persons in the company have connected to. 

**External network breadth** shows you the number of unique domains that persons in the company have connected to.

An example illustrates the distinction between external network size and eternal network breadth. If you are a sales employee, network size shows how many people you have been talking to. If you had talked to 20 people in contoso.com, then your network size would be equal to 20.

External network breadth shows how many outside groups or domains you have been talking to. If you had only talked to contoso.com, then your external network breadth would be equal to one. If you had been talking to both contoso.com and adatum.com, your external network breadth would be equal to two.

For example, the previous bubble graph poses a question about external network breadth compared to external network size. You could use it to help you determine whether small groups in your company might be making a significant number of external connections. Conversely, the graph could show you whether big groups are making relatively few external connections.

In the bubble graph, if the bubble for your particular organization is found up towards the top right, this means that your organization has made the most external connections and has contacted the most unique domains.

## Top external domains
The following graph allows you to see which domains your people spend most time with. You can choose to pivot the data on various settings, such as total collaboration hours, total collaboration cost, or employee engagement.

![External domains](../images/WpA/Use/ext-domains-most-time.png)

**Bar chart**

The horizontal bar graph shows the top ten domains that your company people interact with. Scroll to see more domains.

*Total collaboration hours*

This bar represents the total number of hours that tenant measured employees have collaborated with an example domain, contoso.com. There is no average line on bar charts. The bars are sorted on hours (descending).

*Total collaboration cost*

This bar represents the total number of hours tenant measured employees have collaborated with contoso.com multiplied by the average hourly wage for that tenant (from tenant's configuration). Bars are sorted on cost (descending).

*Total employees engaged*

This bar represents the total number of distinct tenant measured employees who have collaborated with contoso.com.


**Trend chart**

*Group total*

The group total = sum of collaboration hours by measured employees with all external domains in a week multiplied by the average hourly wage for that tenant (from tenant's configuration).

**Distribution chart**

Each bar shows how much time (minimum, maximum, median, upper and lower quartile) people from the tenant have spent with contoso.com multiplied by the average hourly wage for that tenant (from tenant's configuration). Minimum, maximum, median, upper and lower quartile are shown. Distribution bars are sorted on maximum values descending.
There is no distribution to show for number of employees engaged.

The following graph allows you to see which groups spend most time with external people, in collaboration hours.

![External group collaboration](../images/WpA/Use/groups-most-time-collab-ext-people.png)


**Bar chart**

*Collaboration hours*

Collaboration hours = email plus meeting hours combined.
Each bar represents the average number of collaboration hours that tenant measured employees in that organization have collaborated with external domains, where average = sum of collaboration hours during all selected weeks divided by the number of weeks in the selected date range in the page filters on the right.
 
*Average*

The **Average** line on bar charts represents the average of averages = sum of average of collaboration hours for each organization divided by the number of organizations. Average collaboration hours for each organization = total collaboration hours for the organization divided by the number of measured employees in that organization.
Bars are sorted on hours (descending).
 
*Trend chart*

Group average = trend of average of averages for a week, where average of averages = sum of average collaboration hours for each organization divided by number of organizations.
 
The average collaboration hours for each organization = sum of collaboration hours for an organization divided by the number of measured employees in that organization.
 
*Distribution chart*

Each bar shows how many collaboration hours (minimum, maximum, median, upper and lower quartile) measured employees from each organization have spent with external domains.
Distribution bars are sorted on maximum values descending.
  
Collaboration cost =  Collaboration hours multiplied by the average hourly wage for that tenant (from tenant's configuration).

The next graph allows you to see which groups in your company have made the most connections with external people.

![Top group external connections](../images/WpA/Use/groups-most-people-conn.png)

**Bar chart**

*External network size*

This bar represents the average external network size for each organization = the total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions in all selected weeks divided by the number of weeks in the selected date range in the page filters on the right.
 
The average line on bar charts represents the average of averages external network size = the sum of the average external network size for each organization divided by total number of organizations.
 
The average external network size for each org = total number of non-distinct external contacts with whom the measured employees from this organization had two meaningful interactions divided by the number of measured employees in that organization.

> [!Note]
> Right-side collaboration filters cannot be applied for this chart.

**Trend chart**

*Group average*

The group average = the trend of average of averages of external network size = sum of average external network size for each organization divided by number of organizations, where the average external network size for each organization = total number of external contacts with whom the measured employees from this organization had at least two meaningful interactions divided by number of measured employees in that organization.

**Distribution chart**

Each bar shows external network size (minimum, maximum, median, upper and lower quartile) for measured employees from each organization.
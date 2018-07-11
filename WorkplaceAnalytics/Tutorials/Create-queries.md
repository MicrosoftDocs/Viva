---
# Metadata Sample
# required metadata

title: Create queries in Workplace Analytics
description: How to create custom queries in Workplace Analytics. 
author: buntus
ms.author: v-midehm
ms.date: 06/13/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Queries overview

You can create four types of queries in Workplace Analytics: **Person**, **Meeting**, **Group-to-group**, and **Person-to-group**.

![Ways to query data](../Images/WpA/Use/Ways-to-query-data-Create-queries.png)

[!INCLUDE [To open the Workplace Analytics Queries page](../includes/to-open-wpa-queries.md)]

Each query type can help answer specific questions you may be investigating. The different query types give you flexibility to look at data from multiple perspectives to generate insights. You can also use the query types together to gain even more powerful insights.

## Meeting exclusions

You can use Meeting exclusions to exclude meetings that fall outside relevant norms from the queries. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

### Related topics

[Understand meeting exclusions](../Use/Understand-meeting-exclusions.md)

[Create custom meeting exclusions rule](../Use/Create-custom-meeting-exclusions-rules.md)

## Business scenario

An analyst may start by looking at a [Person query](#person-query) to see trends of employees across the company related to meeting collaboration.

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a [Meeting query](#meeting-query) to investigate specific meetings in depth to uncover causes of the poor meeting behavior.

Additionally, the analyst could create a [Groups query](#groups-query)  to identify the groups involved in those meetings and further investigate potential causes that could be addressed.

There are three ways to create queries:

* Use and edit pre-defined query templates
* Create custom queries from scratch
* Open and edit a previously run query

When you create or edit a query, you will select the metrics that you want to include (many can be customized), and you can use filters to narrow the results and drill down on specific data of interest.

![Customize attributes and metrics](../Images/WpA/Use/Customize-attributes-and-metrics-Create-queries.png)

The following examples contain the steps to create custom **Person**, **Meeting**, and **Group** queries, as well as the steps to select and edit a query template.

## Person query

Use a Person query when you want to find broader trends in the organization by looking at aggregated metrics for a group of people.

Person query results show a de-identified list of the productivity metrics (such as time in meetings and email) of each measured employee. Each row of data represents one person, and you can select to aggregate the results by day, week, or month.

### How to create a Person query

During the process of creating a Person query, you will answer three questions:

1. Who (what type or group of people) do I want to analyze? (Filters)
2. What time frame do I want to analyze? (Group by and Date range)
3. What data do I want to know about these people for that period? (Metrics)

### Available data

Using a Person query, you can query the organizational data that was imported to Workplace Analytics by your company. Most organizational data comes from a company’s human resources information system.

Examples include: job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, manager, and so on.

### Business scenario example of long meetings

You can create a Person query to investigate if long meetings are a significant factor in the total number of meeting hours for Operations. The following custom query uses metrics and filters to customize the data.

**Query criteria**

* Time frame: Shows the data aggregated weekly
* Who: Filters on Operations
* What data: Metrics
  * Meeting hours are the total of all meeting hours
  * Long meeting hours that include long meetings that last 2 or more hours
  * Meetings is the total number of meetings
  * Emails sent is the total number of emails sent

### To create a custom Person query

1. On the Queries page, select **Person**.
2. In the **Enter query name here** box, enter **Operations long meetings**.
3. In the **Group by** menu, select **Week**, select the **Date range** you want, and in the **Meeting exclusions** menu, select the exclusion rule set that you want.
4. In the **Filters** section, select **Add filter**, and then in the menus, select **FunctionType** > **Equals** > **Operations**.
5. To add a metric for total meeting hours, in the **Metrics** section, select **Add metric**, and then select **Meeting hours**. Choose the Edit icon and change the metric's name to **Total meeting hours**.
6. To add a custom metric for long meeting hours, select **Add metric**, and then select **Meeting hours**. Choose the Edit icon and change the metric's name to **Long meeting hours**.

    a. To customize the Long meeting hours metric, select the Edit icon.

    b. Choose **Add filter**.

    c. In the **Long meeting hours where** section, select **Meeting**, select **Duration­Hours > >= > 2**, and then select **Confirm**.

7. To add a metric for total number of meetings, select **Add metric**, and then select **Meetings**. Choose the Edit icon and change the name to **Total number of meetings**.
8. To add a metric for sent email, select **Add metric**, and then select **Emails sent**. Choose the Edit icon and change the metric name to **Number of emails sent**.

    > [!Notes]
    > * If no data exists for a person/date combination for a metric, the query results will not have a row for that person/date combination.
    > * When aggregating data by the week or the month, you might want to include a metric that has a zero value.
    > * To make sure you have a line of data for every person/date combination for the metrics, add **Emails sent** as one of your metrics.
    > * After you export the results, replace all null values with zeros to ensure that calculations for averages and other statistics includes all person/date combinations.

9. Choose **Run query**.
10. On the Results page, view the query and its status. When the query results are complete, you can download them as a .csv file to continue your analysis.

**Person query results include the following columns**

* Person ID: De-identified ID number for the person represented in the metric.
* Date: The start date of the aggregation (i.e. if the week is 6/3 to 6/10, then it is 6/3. If it is a month, then it is the start of the month your data encompasses).
* Person Attributes: Each of the person attributes in the data set supplied by the organizational data.
* Metrics: Any other metrics that you included in the query.

**Person ID**|**Date**|**Person attribute 1 (department)**|**Person attribute 2 (role)**|**Metrics - Email hrs**|**Metrics Meeting hrs**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
A|3/1/2017|HR|Administrator|5|11
B|3/1/2017|Marketing|Executive|4|14

## Meeting query

Meeting query results show a list of all the meetings that meet the criteria you select when creating the query. Each row of data represents a single meeting. Use a Meeting query when you want to analyze individual meetings to find the broader meeting patterns within your company or organization.

### How to create a Meeting query

In the basic process to create a Meeting query, you will answer three questions:

1. What meeting properties do I want to analyze? (Filters section)
2. What time frame do I want to analyze? (Date range section)
3. What data do I want to know about those meetings for that period? (Metrics section)

### Available data

Using a Meeting query, you can query on the calendar metadata available from Office 365 for your company. Examples include: Attendee meeting hours, attendees, invitees, emails sent during meetings and so forth.

### Example: Business scenario – Long meetings, recurring

Continuing the example from the Person section above, to investigate long meetings that include Operations and identify other significant meeting factors, such as if long meetings are recurring, you can create a Meeting query using the following criteria:

* Time frame: Show the data aggregated weekly
* Meeting properties: Filters
  * Meetings include at least one person from Operations as attendee
  * Long meetings are two hours or more
  * Meeting are recurring
* What data: Metrics
* Attendees
* Attendee meeting hours

### To create a custom Meeting query

1. On the Queries page, select **Meeting**.
2. In the **Enter query name here** box, enter “Ops long recurring meetings.”
3. Enter the **Date range** you want, and then in the **Meeting exclusions** menu, select the exclusion rule set that you want.
4. To add a custom filter to include only meetings with at least one attendee from Operations, under **Filters**, select **Add filter**, select **Attendee**, and then select **Function** > **Equals** > **Operations**.
5. To add a custom filter to include only meetings that are two hours or longer, point to the plus sign, select **Meeting**, and then select **DurationHours** > **>=** > **2**.
6. To add a custom filter to include only meetings that are recurring, point to the plus sign, select **Meeting**, and then select **IsRecurring** > **=** > **True**.
7. To add a metric for the number of attendees, in Metrics, select **Add metric** and select **Attendees**, and then edit the display name to 'Total attendees'.
8. To add a metric for the total meeting hours of attendees, select **Add metric** and select **Attendee meeting hours**, and then edit the display name to 'Total attendee meeting hours.'
9. Choose **Run query**.
10. On the Results page, view the query and its status. When the query results are complete, you can download them as a .csv file to continue your analysis.

### Meeting query results include these columns

Each row of data represents a single meeting, and Meeting query results always contain the following information in columns.

* Meeting ID – Unique ID number of the specific meeting
* Start Date and Time – When the meeting started
* Duration Hours – The length of the meeting in hours
* Is Recurring – Whether the meeting is part of a recurring series, or not
* Is Cancelled – Whether the meeting was cancelled, or not
* Total Number of Emails Sent During Meeting – Number of emails sent by attendees during the meeting
* Subject – Subject line of the meeting
* Total Accepted – Number of invitees who accepted the meeting
* Total Declined – Number of invitees who declined the meeting
* Total Number of No Responses – Number of invitees who did not respond
* Total Number of Double-Booked – Number of invitees who were double-booked
* Metrics – Any other metrics that you included in the query

**Meeting ID**|**Start Date**|**Duration Hours**|**Is Recurring**|**Is Cancelled**|**Total # of emails sent during meeting**|**Subject**|**Metrics - Number of Attendees**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
1|3/1/2017 5:00PM|1|No|No|10|Process Meeting|10
2|3/2/2017 3:00PM|2|Yes|No|41|Marketing Meeting|15

## Group queries

Workplace Analytics offers two kinds of queries that report information about collaboration with groups. See the following topics for more information:

[Group-to-group queries](Group-to-group-queries.md)

[Person-to-group queries](Person-to-group-queries.md)


<!-- OLD CONTENT 
Group query results show the collaboration between two groups quantified by the productivity metrics (such as time spent in meetings and email) that you select. Each row shows the metrics that quantify the interactions of the two groups. You can aggregate group query results by day, week, or month.
Use a group query if you want to analyze how different groups are collaborating.
There are two types of metrics:
* Count: The total number of instances of the metric.
* Hour: The total number of hours for the metric (for example, meeting hours)
## Time allocation
To ensure that meeting hours in a group query are allocated to each group as an accurate representation of how the groups work together (and are not double-counted), the hours metrics are calculated using a specialized approach called time allocation. Time allocation is the logic used to define how the time of members from one group is distributed among the members of other groups that are in the metric being measured (for example, a meeting).

### How to create a Group query
In the basic process to create a Group query, you will answer these questions:
* What time frame do I want to analyze? (Date range section)
* What group do I want to analyze - Group A? (Groups section)
* What other group, Group B, do I want to compare with Group A?  (Groups section)
* Do I want to view metrics based on count or hours? (Metrics)
* Optional - Do I want to further limit the population included in the results? (Groups section)

### Example: Business scenario – How many meetings did Operations and Engineering attend together
You can create a Group query to identify how Operations is collaborating with another group, in this example, Engineering. This query will identify how many meetings Operations and Engineering attended together.

Query criteria
* Time frame: Show the data aggregated weekly
* Groups to compare: Operations and Engineering
* Metrics: Count

### To create a custom Group query
1. On the **Queries** page, click **Group**.
2. In the **Enter query name here** box, enter Ops Engineering collaboration.
3. In the **Group by** menu, select **Week**, and then select the **Date range** you want, and in the Meeting exclusions menu, select the exclusion rule set that you want.
4. Under **Groups**, click **Group A**, and then in the **Attribute** menu, select **Function**.
5. Under **Filters**, click **Add filter**, then in the filter menus, select **Function > Equals > Operations**.
6. Click **Group B**, and then in the **Attribute** menu, select **Function**.
7. Under **Filters**, click **Add filter**, then in the filter menus, select **Function > Equals > Engineering**.
8. To create a query that shows how many meetings Ops and Engineering attended together, under **Metrics**, make sure the toggle button is set to **Count**. The **Meetings attended together**, **Total attendees**, and the **Total invitees** metrics appear.
9. Optional: To further limit population included in the results, click **Limit population**, and then select the filter values that you want.
10. Click **Run query**.

**Group query results include the following columns:**
* Group A – The group you selected as Group A.
* Group B – The group you selected as Group B.
* Date – The start date of the aggregation (i.e. if the week is 6/3 to 6/10, then it is 6/3. If it is a month, then it is the start of the month your data encompasses.)
* Metrics – Any other metrics that you included in the query such as meetings attended together, total attendees, and so on.

**Group A**|**Group B**|**Date**|**Meetings attended together**
:-----:|:-----:|:-----:|:-----:
Operations|Engineering|3/5/2017|12
Operations|Engineering|3/12/2017|20
-->

### Related topic
[View, download, and export query results](../Use/View-download-and-export-query-results.md)

---
# Metadata Sample
# required metadata

title: Create queries in Workplace Analytics
description: This topic explains how to create custom queries in Workplace Analytics. 
author: v-leash
ms.author: v-leash
ms.date: 2/14/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Queries overview
You can create three types of queries in Workplace Analytics: **Person**, **Group**, and **Meeting**.

![Three types of queries](../Images/WpA/Use/Three-ways-to-query-data-Create-queries.png)

Each query type can help answer specific questions you may be investigating. The different query types give you flexibility to look at data from multiple perspectives to generate insights. You can also use the query types together to gain even more powerful insights.

## Meeting exclusions
You can use Meeting exclusions to exclude meetings that fall outside relevant norms from the queries. You can choose between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

**Related topics**

[Understand meeting exclusions](../Use/Understand-meeting-exclusions.md)

[Create custom meeting exclusions rule](../Use/Create-custom-meeting-exclusions-rules.md)


## Business scenario
An analyst may start by looking at a [**Person query**](#2-person-query)  to see trends of employees across the company related to meeting collaboration. 

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a [**Meeting query** ](#2-meeting-query) to investigate specific meetings in depth to uncover causes of the poor meeting behavior. 

Additionally, the analyst could create a [**Group query**](#2-group-query)  to identify the groups involved in those meetings and further investigate potential causes that could be addressed.

There are three ways to create queries:
* Use and edit pre-defined query templates
* Create custom queries from scratch
* Open and edit a previously run query

When you create or edit a query, you will select the metrics that you want to include (many can be customized), and you can use filters to narrow the results and drill down on specific data of interest.

![Customize attributes and metrics](../Images/WpA/Use/Customize-attributes-and-metrics-Create-queries.png)


The following examples contain the steps to create custom **Person**, **Meeting**, and **Group** queries, as well as the steps to select and edit a query template.

# Person query
Use a Person query when you want to find broader trends in the organization by looking at aggregated metrics for a group of people.

Person query results show a de-identified list of the productivity metrics (such as time in meetings and email) of each measured employee. Each row of data represents one person, and you can choose to aggregate the results by day, week, or month.

### How to create a Person query 
In the basic process to create a Person query, you will answer three questions:
1. Who (what type or group of people) do I want to analyze? (Filters section)
2. What time frame do I want to analyze? (Group by, Date range section)
3. What data do I want to know about those people for that period? (Metrics section)

### Available data
Using a Person query, you can query on the organizational data that was imported to Workplace Analytics by your company. Most organizational data comes from a company’s human resources information system.

Examples include: job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, manager, and so on.
### Example: Business scenario – Long meetings
You could create a Person query to investigate if long meetings are a significant factor in the total number of meeting hours for Operations. In this query, you will select your metrics and filters, and customize them to your needs.

**Query criteria**
* Time frame: Show the data aggregated weekly
* Who: Filter on Operations
* What data: Metrics
  * Meeting hours – the total of all meeting hours
  * Long meeting hours - customize to define long meetings as 2 hours or more
  * Meetings – a count of the total number of meetings
  * Emails sent

### To create a custom Person query
1. On the Queries page, click **Person**.
2. In the **Enter query name here** box, type 'Operations long meetings.'
3. In the** Group by** menu, select **Week**, and then select the** Date range** you want, and in the **Meeting exclusions** menu, select the exclusion rule set that you want.
4. Under **Filters**, click **Add filter**, and then in the menus, select **Function > Equals > Operations**.
5. To add a metric for total meeting hours, under **Metrics**, click** Add metric**, in the menu select** Meeting hours**, and then edit the name for the metric to ‘Total meeting hours.’
6. To add a custom metric for long meeting hours, click **Add metric**, in the menu select **Meeting hours**, and then edit the metric name ‘'Long meeting hours.’

    a. To customize the Long meeting hours metric, click the Edit icon.

    b. Click **Add filter**.

    c. Under **Long meeting hours where**, click **Meeting**, select **Duration­Hours > >= >** type 2, and then click **Confirm**.

7. To add a metric for total number of meetings, click **Add metric**, in the menu, select **Meetings**, and then edit the display name for the metric to ‘Total number of meetings'.
8. To include the Sent mail metric, click **Add metric**, in the menu select **Emails sent**, and then edit the metric name to ‘Number of emails sent.’

    **NOTES**
     * If there is no data for a person/date combination for a metric, there will be no row for that person/date combination in the query results.
    * When aggregating data by the week or the month, there may be instances when you want to include a metric that has a zero value.
    * To make sure that you have a line of data for every person/date combination for the metrics you are using, add Emails sent as one of your metrics.
    * Once you export your results, replace all null values with zeros to ensure that calculations for averages and other statistics includes all person/date combinations.

9. Click **Run query**.
10. On the **Results** page, you can see the status of your query, view the query, and, when your query results are complete, you can download the results as a csv file to continue your analysis.

**Person query results include the following columns**
* Person ID: De-identified ID number for the person represented in the metric.
* Date: The start date of the aggregation (i.e. if the week is 6/3 to 6/10, then it is 6/3. If it is a month, then it is the start of the month your data encompasses).
* Person Attributes: Each of the person attributes in the data set supplied by the organizational data.
* Metrics: Any other metrics that you included in the query.


**Person ID**|**Date**|**Person attribute 1 (department)**|**Person attribute 2 (role)**|**Metrics - Mail hrs**|**Metrics Meeting hrs**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
A|3/1/2017|HR|Administrator|5|11
B|3/1/2017|Marketing|Executive|4|14


# Meeting query
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
1. On the Queries page, click **Meeting**.
2. In the **Enter query name here** box, type “Ops long recurring meetings.”
3. Enter the **Date range** you want, and then in the **Meeting exclusions** menu, select the exclusion rule set that you want.
4. To add a custom filter to include only meetings with at least one attendee from Operations, under **Filters**, click **Add filter**, click **Attendee**, and then select **Function > Equals > Operations**.
5. To add a custom filter to include only meetings that are two hours or longer, point to the plus sign, click **Meeting**, and then select **DurationHours > >= **>type 2.
6. To add a custom filter to include only meetings that are recurring, point to the plus sign, click **Meeting**, and then select **IsRecurring > = > True**.
7. To add a metric for the number of attendees, under Metrics, click **Add metric** and select **Attendees**, and then edit the display name to 'Total attendees'.
8. To add a metric for the total meeting hours of attendees, click **Add metric** and select** Attendee meeting hours**, and then edit the display name to 'Total attendee meeting hours.'
9. Click **Run query**.
10. On the **Results** page, you can see the status of your query, view the query, and, when your query results are complete, you can download the results as a .csv file to continue your analysis.

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


# Groups query
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

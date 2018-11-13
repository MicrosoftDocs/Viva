---
# Metadata Sample
# required metadata

title: Meeting queries in Workplace Analytics
description: When to use a meeting query and the type of data available for analysis in Workplace Analytics.  
author: madehmer
ms.author: rodonahu
ms.date: 07/16/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Meeting queries

The Meeting query in Workplace Analytics gives you a list of all meetings that occurred during a specific period, along with their attributes.

## How to choose between a Meeting or Person query

Certain questions can be answered with either a meeting or person query.

 ![Meeting or Person query](../Images/WpA/Tutorials/person-or-meeting-query.png)

But for most questions you want to answer, the lines are more clear cut.

![Meeting query and Person query](../Images/WpA/Tutorials/meeting-or-person-query-2.png)

Use a meeting query when you want to understand the relationship between different meeting attributes.

Use a person query when you want to understand the relationship between a person’s organizational attributes – like their team, level, or location – and how they use their time, or when you want to know how one aspect of a person’s time use might influence another aspect of their time use.

## Create a meeting query

Setting up a meeting query is simple. Select whether you want the metrics for each meeting summarized by day, week, or month, and the time period you’d like to analyze.

If you want to exclude meetings from the calculations by using custom criteria, you can select your custom rule set or simply use the default.

 ![Create meeting query](../Images/WpA/Tutorials/create-meeting-query1.png)

By running this query with no exclusions, you will get an output file that can help you determine the right criteria to separate work-related activities from other calendar items.

 ![Meeting query no exclusions](../Images/WpA/Tutorials/meeting-no-exclusions.png)

## Add filters

You can add a filter to limit the list of meetings included in the output file. For example, the Meeting filter limits the query based on the size, duration, or other attributes related to meetings.

You can also limit the query based on organizer, attendee, and invitee attributes for meetings.

![Meeting query filter](../Images/WpA/Tutorials/meeting-filter.png)

## Add metrics

You can add base metrics to customize your meeting data. For example, select the Attendees metric to include the total number of people that attended meetings. You can add a metric filter to further customize the data. For example, the following metric filter will only show meetings that included attendees from the engineering group.

![Meeting query metric](../Images/WpA/Tutorials/meeting-metric.png)

To get more details on adding metric filters, see [Customize a metric](../Tutorials/customize-a-metric.md).

In the basic process to create a Meeting query, you will answer three questions:

1. What meeting properties do I want to analyze? (Filters section)
2. What time frame do I want to analyze? (Date range)
3. What data do I want to know about those meetings for that period? (Metrics section)

## Available data

Using a Meeting query, you can query on the calendar metadata available from Office 365 for your company. Examples include: Attendee meeting hours, attendees, invitees, emails sent during meetings, and so forth.

## Business scenario example of long recurring meetings

Continuing the example from the Person section above, to investigate long meetings that include Operations and identify other significant meeting factors, such as if long meetings are recurring, you can create a Meeting query with the following criteria:

* Time frame: Show the data aggregated weekly
* Meeting properties: Filters
  * Meetings include at least one person from Operations as attendee
  * Long meetings are two hours or more
  * Meetings are recurring
* What data: Metrics
  * Attendees
  * Attendee meeting hours

## To create a custom Meeting query

1. On the Queries page, select **Meeting**.
2. Select and change **Enter query name here** to **Long recurring Ops meetings**.
3. Enter the **Date range** you want, and then for **Meeting exclusions**, select the exclusion rule set that you want.
4. To add a custom filter to include only meetings with at least one attendee from Operations, under **Filters**, select **Add filter**, select **Attendee**, and then select **Function** > equals > **Operations**.
5. To add a custom filter to include only meetings that are two hours or longer, select the plus sign to add another filter, then select **Meeting** > **Duration (in hours)** > greater than or equal to > **2**.
6. To add a custom filter to include only meetings that are recurring, select the plus sign to add another filter, then select **Meeting** > **IsRecurring** > equals > **True**.
7. To add a metric for the number of attendees, in Metrics, select **Add metric**.
8. Select **Attendees**, and then select and change the metric's name to **Total attendees**.
9. To add a metric for the total meeting hours of attendees, select **Add metric** > **Attendee meeting hours**, and then select and change the metric's name to **Total attendee meeting hours**.
10. Select **Run** at the top right to run the query.
11. On the Results page, you can see the query and its status. When the query results are complete, you can download them as a .csv file to continue your analysis.

## Meeting query results

Each row of data represents a single meeting, and Meeting query results always contain the following information in columns:

* Meeting ID – Unique ID number of the specific meeting
* Start Date and Time – When the meeting started
* Duration Hours – The length of the meeting in hours
* Is Recurring – Whether the meeting is part of a recurring series, or not
* Is Cancelled – Whether the meeting was cancelled, or not
* Meeting Resource Ids Count - The number of meeting rooms reserved for each meeting  
* Meeting Resources - Is the alias portion of the meeting room’s primary SMTP address (a semi-colon delimited list for multiple rooms)
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

### Related topics

[Metric descriptions](../Use/Metric-definitions.md)
[View, download, and export query results](../Use/View-download-and-export-query-results.md)
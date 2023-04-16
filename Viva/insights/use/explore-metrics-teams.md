---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 04/01/2019
title: Explore Teams data in Viva Insights
description: Overview of Teams collaboration data in the advanced insights app with Viva Insights
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Teams collaboration

**Teams collaboration** shows communication trends about and insights into how your organization's employees use Teams for communication and collaboration. You can select what collaboration data to analyze on this page, either Teams' calls, instant messages, or both.

![Teams collaboration.](../images/wpa/use/teams-explore.png)

## Access to Teams collaboration

You can open [Teams collaboration](https://workplaceanalytics.office.com/en-us/Home/Agility/ChatsAndCalls)(if that link doesn't work, try [this link instead](https://workplaceanalytics-eu.office.com/en-us/Home/Agility/ChatsAndCalls)) in the advanced insights app to view it.

## Call hours

The **Call hours** graph shows the average and total number of hours each group spent in calls with at least one other person, as either initiators or participants, through Teams, including scheduled and unscheduled calls during and outside of working hours (as set in Outlook).

![Teams call hours.](../images/wpa/use/teams-explore-calls.png)

## Instant messaging hours

The **Instant messaging hours** graph shows average and total number of hours each group spent sending or receiving instant messages (IMs) through Teams with at least one other person, including IMs during and outside of working hours (as set in Outlook).

![Teams IMs.](../images/wpa/use/teams-explore-ims.png)

## Filters for Teams

You can use the **Call hours** and **IM hours** filters in the Charts and in Page Settings to filter and view Teams data.

![Teams filters.](../images/wpa/use/teams-filters.png)

## Data sources includes Teams

In **Sources** > **Microsoft 365 data**, you'll see an **Average weekly collaboration hours by type** chart that includes the average weekly Teams call hours and instant messaging hours over time. The "Week of" date on that page shows when the Teams data was last processed in Viva Insights.

Analysts can use these views to evaluate communication and collaboration trends and patterns for your organization.

![Teams summary in Data sources.](../images/wpa/Use/teams-data.png)

## Teams data in queries

You can also include and analyze data about Teams calls and instant messages in Person queries and data for Teams calls in Meeting queries. For example, you can customize a person or meeting query to show internal as compared to external number of calls.

For Meeting queries, meeting hours and related meeting metrics will include data about scheduled and unscheduled calls in Teams.

The following table provides details about Teams metrics in Person queries.

### Teams metrics in Person queries

|Metric |Description |Query type |Data type |Customizable |
|------|-----------|----------|---------|------------|
|After hours in calls| Number of hours a person spent in scheduled and unscheduled calls through Teams, with at lest one other person, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule (as set in Outlook).| Person| Hour| Yes|
|After hours instant messages| Number of hours a person spent in istant messages through Teams, outside of that person’s working hours. | Person| Hour| Yes|
|Call hours | Number of hours a person spent in scheduled and unscheduled calls through Teams, during and outside of working hours (as set in Outlook). | Person| Hour| Yes|
|Instant message hours | Number of hours a person spent in IMs through Teams, with at least one other person, during and outside of working hours (as set in Outlook). | Person| Hour| Yes|
|Instant messages sent | Total number of instant messages (IMs) or chats sent by a person through Teams, during and outside of working hours. | Person| Count| Yes|
|Total calls| Total number of calls a person joined through Teams, including scheduled and unscheduled calls, during and outside of working hours (as set in Outlook).| Person| Count| Yes |
|Working hours in calls| Number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. | Person| Hour| Yes|
|Working hours in instant messages| Number of hours a person spent in instant messages through Teams, during working hours. | Person| Hour| Yes|

## Related topics

* [Page settings](/viva/insights/use/explore-page-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Person queries](../tutorials/Person-queries.md)
* [Meeting queries](../tutorials/Meeting-queries.md)
* [Advanced insights charts](/viva/insights/use/chart-types?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Advanced insights metric descriptions](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)


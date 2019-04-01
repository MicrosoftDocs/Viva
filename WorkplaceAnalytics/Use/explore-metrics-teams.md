---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Explore Teams metrics in Workplace Analytics
description: Overview of meetings metrics on the Workplace Analytics Explore page
author: madehmer
ms.author: v-midehm
ms.date: 04/01/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---

# Teams collaboration

The **Microsoft Teams** page in **Explore** shows communication trends about and insights into how your organization's employees use Teams for communication and collaboration. You can select what collaboration data to analyze on this page, either Teams' calls, instant messages, or both.

![Teams collaboration](../images/wpa/use/teams-explore.png)

To open the **Microsoft Teams** page:

1. Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page. If prompted, sign in with your work account.
2. In the left navigation pane, select **Analyze** and then select **Explore**.
3. In **Explore**, select **Microsoft Teams**.

## Call hours

The **Call hours** graph shows the average and total number of hours each group spent in calls as initiators or participants, through Teams, including scheduled and impromptu calls during and outside of working hours (as set in Outlook).

![Teams call hours](../images/wpa/use/teams-explore-calls.png)


## Instant messaging hours

The **Instant messaging hours** graph shows average and total number of hours each group spent sending or receiving instant messages (IMs) through Teams, including scheduled and impromptu IMs during and outside of working hours (as set in Outlook).

![Teams IMs](../images/wpa/use/teams-explore-ims.png)


## Query metric definitions for Teams data

You can also include and analyze the following metrics for Teams in person, meeting, and group queries.

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
Calls| Total number of calls the person spent time in as initiator or participant, through Teams, during and outside of working hours.| Person| Count| Yes
IMs | Total number of instant messages (IMs) or chats sent by the person as the initiator, through Teams, during and outside of working hours. Note: Time in IM compose estimated to 22 seconds, Time in IM read estimated to 8 seconds| Person| Count| Yes
Time in calls after hours | Number of hours the person spent in calls, through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule (as set in Outlook).| Person| Hour| Yes
Time in IMs after hours| Number of hours the person spent in reading/sending Instant Messages in  Teams, outside of that person’s working hours. Note: Time in IM compose estimated to 22 seconds, Time in IM read estimated to 8 seconds| Person| Hour| Yes
Total call hours | Total number of hours the person spent in calls as initiator or participant, through Teams, including scheduled and impromptu calls during and outside of working hours (as set in Outlook). | Person| Hour| Yes
Total IM hours | Total number of hours the person spent in IMs as initiator or participant, through Teams, including scheduled and impromptu IMs during and outside of working hours (as set in Outlook).  Note: Time in IM compose estimated to 22 seconds, Time in IM read estimated to 8 seconds.| Person| Hour| Yes
Working hours in calls| Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. | Person| Hour| Yes


## Related topics

[Workplace Analytics Charts](../use/chart-types.md)
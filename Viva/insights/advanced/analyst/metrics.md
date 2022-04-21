---

title: Advanced insights metric descriptions
description: Describes the metrics for analysis data that are available in Microsoft Viva Insights, including query metrics and Power BI template metrics
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
manager: helayne
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 

---

# Advanced insights metrics

The following metrics are available when creating analysis in the Advanced insights app with Microsoft Viva Insights, including with queries and Power BI templates. The descriptions are listed by category:

* [Focus](#focus)
* [Collaboration activity](#collaboration)
* [Meeting type](#meeting)
* [After-hours collaboration](#after-hours-collaboration)
* [Working hours collaboration](#working-hours-collaboration)
* External collaboration
* Collaboration by day of the week
* Collaboration involving manager
* Collaboration in small groups
* Collaboration network
* Hybrid metrics
* Collaboration by time of day

## Focus

|Metric |Description           |Analysis type |Analysis components |
|------|----------------------|----------|---------|
| Available to focus | The number of hours that a person spent sending and reading posts and replies in Teams channels, outside of work hours. |Ways of working assessment template | Focus (Available to focus) |
| Uninterrupted time | Total number of hours where a person has more than or equal to a one-hour block of uninterrupted time to focus on work during their set working hours. It's only counted as uninterrupted time when the person has no collaboration activity, including attending a meeting or an unscheduled Teams call, sending an email, or sending a Teams instant message. | Ways of working assessment, Business resilience, and Wellbeing templates |Focus (Uninterrupted time) |

## Collaboration activity

|Metric |Description            |Analysis type |Analysis components |
|------|----------------------|----------|---------|
| Collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). |Ways of working assessment, Business resilience, Manager effectiveness, Hybrid workforce experience, and Wellbeing templates |Collaboration activity |

## Meeting types

|Metric |Description           |Analysis type |Analysis components |
|------|----------------------|----------|---------|
| Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.) |Meeting queries |Collaboration activity where **Is Conflicting** = **TRUE** |
| Decision making meeting hours |Meeting hours with a duration of one hour or less and at least three up to eight participants. |Meeting queries and Ways of working assessment template | Collaboration activity where: <br>**Total meeting attendees** > **2** <br> AND **Total meeting attendees** <= **8** <br>AND **Meeting duration (in hours)** <= **1** |

## After-hours collaboration

|Metric |Description             |Analysis type |Analysis components |
|------|----------------------|----------|---------|
|After-hours collaboration hours | The total number of channel posts and replies sent on Teams channels by the time investor to one or more people in the collaborator group. |Ways of working assessment, Business resilience, Manager effectiveness, Hybrid workforce experience, and Wellbeing templates | **During working hours** = **FALSE** |

## Working hours collaboration

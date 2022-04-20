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

The metrics in this table are used both in [person queries](../tutorials/person-queries.md) and in [peer-comparison](../tutorials/comparison-query.md) queries.

|Metric |Description |Tags |Analysis |
|------|-----------|----------|---------|
| Available to focus | The number of hours that a person spent sending and reading posts and replies in Teams channels, outside of work hours. |Ways of working assessment  | Focus (Available to focus) |

## Collaboration activity

|Metric |Description |Tags |Analysis |
|------|-----------|----------|---------|
| Collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). |Ways of working assessment, Business resilience, Manager effectiveness, Hybrid workforce experience, and Wellbeing |Collaboration activity |


## Meeting types

|Metric |Description |Tags |Analysis |
|------|-----------|----------|---------|
| Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.) |Meeting |Collaboration activity where "Is Conflicting" equals "True" |

## After-hours collaboration

|Metric |Description |Tags |Analysis |
|------|-----------|----------|---------|
|After-hours collaboration hours | The total number of channel posts and replies sent on Teams channels by the time investor to one or more people in the collaborator group. |Ways of working assessment, Business resilience, Manager effectiveness, Hybrid workforce experience, and Wellbeing | "During working hours" equals "False" |

## Working hours collaboration

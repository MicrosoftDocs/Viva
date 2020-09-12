---

ROBOTS: NOINDEX,NOFOLLOW
title: Instant message metrics for Workplace Analytics Data export
description: One row for each collaboration event
author: paul9955
ms.author: v-mideh
ms.topic: article
ms.prod: wpa
---

# InstantMessages (.csv)

This file includes one row for each instant message with the following metrics.

|Column name|Data type|Description|
|-----------|---------|------------|
| InstantMessageId |string |Unique identifier for each instant message; foreign key matching InstantMessage table |
| AppName |string |Name of the source app (for example: Teams, Skype) |
| SentTime |datetime |Sent time of the instant message in the participant's local time |
| InteractionType |enumerated |The type of instant message received by a person: GroupChat, OneOnOneChat |
| TotalParticipants |double |Sum of total IM participants (includes sender) |

## Related topics

[Data export](./data-access.md)

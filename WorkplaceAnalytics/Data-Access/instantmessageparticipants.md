---

ROBOTS: NOINDEX,NOFOLLOW
title: Instant message participant metrics for Workplace Analytics Data export
description: A collaboration event row for each participant in an instant message
author: paul9955
ms.author: v-mideh
ms.topic: article
ms.prod: wpa
---

# InstantMessageParticipants (.csv)

This file includes one row for each participant in an instant message with the following metrics.

|Column name |Data type |Description |
|-----------|----------|-----------|
|InstantMessageId |string |Unique identifier for each instant message; foreign key matching [InstantMessage](./InstantMessages.md) table |
|PersonHistoricalId |string |Unique value for a participant any time an HR attribute changes; foreign key matching [PersonHistorical](./PersonHistorical.md) table |
|isAfterHours |boolean |True if this instant message was sent after hours |
|IsSender |boolean |True if this person was the instant message sender |
|LocalSentTime |datetime |Sent time of the instant message in the participant's local time |
|SenderTimeSpentInMinutes |double |Time spent in instant message, approximation |

## Related topics

[Data export](./data-access.md)

---

ROBOTS: NOINDEX,NOFOLLOW
title: Email participant metrics for Workplace Analytics Data export
description: One row for every email sent and received
author: paul9955
ms.author: v-mideh
ms.topic: article
ms.prod: wpa
---

# MailParticipants (.csv)

This file includes one row for every email sent and received with the following metrics.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|MailId|string|Unique identifier for every email sent; foreign key matching primary key of the [Mails table](./mails.md)|
|PersonHistoricalId:|string|Unique identifer for every person; foreign key matching [PersonHistorical](./PersonHistorical.md) table primary key|  
|IsSender|boolean|True if this person sent the email|
|LocalSentTime|datetime|Local time when the email was sent|
|PersonTimeSpentInHours|double|Time spent reading or writing email in hours (heuristic estimated value)|
|PersonTimeSpentInMinutes|double|Time spent reading or writing email in minutes (heuristic estimated value)|

## Related topics

[Data export](./data-access.md)
---

ROBOTS: NOINDEX,NOFOLLOW
title: Calls metrics for Workplace Analytics Data export
description: One row for each collaboration event
author: paul9955
ms.author: v-pascha
ms.topic: article
ms.prod: wpa
---

# Calls (.csv)
 
This file includes one row for each call with the following metrics. Recurring, scheduled calls (also referred to as _meetings_) result in a row for each occurrence.

|Column name |Data type |Description |
|-----------------|---------------|-----------------|
|CallRecordId |string |Unique identifier for each call (including scheduled calls); primary key  |
|MeetingId |string |Meeting calendar ID (iCalUID + StartDate) associated metadata found on the mapped MeetingId (if a scheduled call/meeting) |
|AppName | string |Name of the source app (for example: Teams, Skype) |
|IsScheduledCall |boolean |True if this is a scheduled call |
|TotalParticipants |integer |Sum of total participants for the call |
|InteractionType |enumerated |Invitee's response to the call: joined or attended, tentative, accepted, or no response |

## Related topics

[Data export](./data-access.md)

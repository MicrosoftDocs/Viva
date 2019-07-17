---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Meeting participant metrics for Workplace Analytics Data export
description: One row for each participant in a calendar meeting
author: paul9955
ms.author: v-midehm
ms.date: 06/26/2019
ms.topic: article
ms.prod: wpa
---

# MeetingParticipants (.csv)

This file has one row for each participant in a calendar meeting with the following metrics:
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MeetingId**|**string**|Unique identifier for each meeting (including recurring meetings); foreign key matching [Meetings](./Meetings.md) table|
|**PersonHistoricalId**|**string**|Unique value for a participant any time an HR attribute changes; foreign key matching [PersonHistorical](./PersonHistorical.md) table|  
|**IsOrganizer**|**boolean**|True if this participant organized the meeting|
|**IsDoubleBooked**|**boolean**|True if this person has more than one meeting at this time in their calendar|
|**Response**|**enumerated**|Invitee's response to the meeting: declined, tentative, accepted, or no response|
|**LocalStartTime**|**datetime**|Start time of the meeting in the participant's local time|
|**DurationMinutesAdjusted**|**double**|Time spent in meeting, adjusted if double booked|
|**EmailsSentDuringMeeting**|**integer**|The number of meetings sent by this participant in this meeting|

## Related topics

[Data export](./data-access.md)
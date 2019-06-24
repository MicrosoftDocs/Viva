---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Teams metrics for Workplace Analytics Data export
description: One row for each participant in a calendar meeting
author: paul9955
ms.author: v-pascha
ms.date: 06/24/2019
ms.topic: article
ms.prod: wpa
---

# Teams (.csv)

This file includes one row for each Teams collaboration event with the following metrics. 
  
NOTE: THE FOLLOWING TABLE WAS COPIED FROM ANOTHER FILE. IT IS AN EXAMPLE ONLY. 
TEAMS DATA (COLUMNS, TYPES, DESCRIPTIONS) WILL GO HERE. 

|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MeetingId**|**string**|Unique identifier for each meeting (including recurring meetings); primary key|
|**ICalUid**|**string**|Meeting calendar ID|  
|**Subject**|**string**|Meeting subject (rRespects tenant privacy settings; see [Workplace Analytics Privacy settings](../use/settings.md#privacy-settings))|
|**IsRecurring**|**boolean**|True if this is a recurring meeting|
|**IsCanceled**|**boolean**|True if the meeting was canceled|
|**StartTime**|**datetime**|Meeting start time|
|**DurationMinutes**|**integer**|Meeting length in minutes|
|**TotalAccept**|**integer**|Total number of meeting acceptances|
|**TotalDecline**|**integer**|Total number of meeting declines|
|**TotalNoResponse**|**integer**|Total number of invitees who did not respond to the meeting invite|
|**TotalAttendees**|**integer**|Sum of total accept, total no-response, plus organizer|
|**TotalDoubleBooked**|**integer**|Number of attendees who had conflicting meetings or appointments on their calendar|
|**TotalEmailsDuringMeeting**|**integer**|Number of emails sent during the meeting by all attendees who did not decline the meeting invitation|

## Related topics

[Data access](./data-access.md)

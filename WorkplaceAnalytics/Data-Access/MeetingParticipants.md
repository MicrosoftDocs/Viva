---
# Metadata Sample
# required metadata

title: MeetingParticipants table (WPA Data Access)
description: One row for each meeting and appointment
author: gbowerman
ms.author: guybo
ms.date: 05/11/2018
ms.topic: language-reference
ms.prod: wpa
---

# MeetingParticipants table (CSV)


  Contains one row for each participant in a calendar meeting.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MeetingId**|**string**|Unique identifier for each meeting (including recurring meetings). Foreign key matching Meetings table.|
|**PersonHistoricalId**|**string**|Unique value for a participant any time an HR attribute changes. Foreign key matching PersonHistorical table.|  
|**IsOrganizer**|**boolean**|True if this participant organized the meeting.|
|**IsDoubleBooked**|**boolean**|True if this person has more than one meeting at this time in their calendar.|
|**Response**|**enum**|User's response to the meeting, one of: declined/tentative/accepted/noresponse.|
|**LocalStartTime**|**datetime**|Start time of the meeting in participant's local time.|
|**DurationMinutesAdjusted**|**double**|Time spent in meeting, adjusted if double booked.|
|**EmailsSentDuringMeeting**|**int**|The number of meetings sent by this participant in this meeting.|


  

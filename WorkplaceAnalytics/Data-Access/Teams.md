---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Teams metrics for Workplace Analytics Data export
description: One row for each collaboration event
author: paul9955
ms.author: v-pascha
ms.date: 06/26/2019
ms.topic: article
ms.prod: wpa
---

# Teams (.csv)

This file includes one row for each Teams collaboration event with the following metrics. 
  
## InstantMessageParticipants (.csv)      
      
|Column name|Data type|Description|      
|-----------------|---------------|-----------------|      
| InstantMessageId | string | Unique identifier for each instant message; foreign key matching InstantMessage table |
| PersonHistoricalId | string | Unique value for a participant any time an HR attribute changes; foreign key matching PersonHistorical table |
| isAfterHours | boolean | True if this instant message was sent after hours |
| IsSender | boolean | True if this person was the instant message sender |
| LocalSentTime | datetime | Sent time of the instant message in the participant's local time |
| SenderTimeSpentInMinutes | double | Time spent in instant message, approximation |
      
## InstantMessages (.csv)  
    
|Column name|Data type|Description|      
|-----------------|---------------|-----------------|      
| InstantMessageId | string | Unique identifier for each instant message; foreign key matching InstantMessage table |
| AppName | string | Name of the source app (e.g. Teams, Skype) |
| SentTime | datetime | Sent time of the instant message in the participant's local time |
| InteractionType | enumerated | Sendee's type of instant message: GroupChat, OneOnOneChat |
| TotalParticipants | double | Sum of total IM participants (includes sender) |
      
## Calls (.csv)     
 
|Column name|Data type|Description|      
|-----------------|---------------|-----------------|      
| CallRecordId | string | Unique identifier for each call (including scheduled calls); primary key  |
| MeetingId | string | Meeting calendar ID (iCalUID + StartDate) associated metadata found on the mapped MeetingId (if a scheduled call/meeting) |
| AppName | string | Name of the source app (e.g. Teams, Skype) |
| IsScheduledCall | boolean | True if this is a scheduled call |
| TotalParticipants | integer | Sum of total particpants for the call |
| InteractionType | enumerated | Invitee's response to the call: joined/attended, tentative, accepted, or no response |
						
## CallsParticipants (.csv)    
  
|Column name|Data type|Description|      
|-----------------|---------------|-----------------|      
| CallRecordId | string | Unique identifier for each call (including scheduled calls); primary key  |
| PersonHistoricalId | string | Unique value for a participant any time an HR attribute changes; foreign key matching PersonHistorical table |
| IsOrganizer | boolean | True if this participant organized the call |
| LocalStartTime | datetime | Start time of the call in the participant's local time |
| LocalEndTime | datetime | End time of the call in the participant's local time |


## Related topics

[Data access](./data-access.md)


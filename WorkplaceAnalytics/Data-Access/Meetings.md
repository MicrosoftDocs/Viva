---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Meetings for Workplace Analytics Data Export
description: One row for each meeting and appointment
author: madehmer
ms.author: madehmer
ms.date: 2/19/2019
ms.topic: article
localization_priority: normal
ms.prod: wpa
---
# Meetings (.csv)

This file includes one row for each meeting and appointment with the following metrics. Recurring meetings result in a row for each occurrence.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MeetingId**|**string**|Unique identifier for each meeting (including recurring meetings). Primary key.|
|**ICalUid**|**string**|Meeting calendar ID.|  
|**Subject**|**string**|Meeting subject. Respects tenant privacy settings. See [Workplace Analytics settings](../use/settings.md#privacy-settings).|
|**IsRecurring**|**boolean**|True if this is a recurring meeting.|
|**IsCanceled**|**boolean**|True if the meeting was canceled.|
|**StartTime**|**datetime**|Meeting start time.|
|**DurationMinutes**|**int**|Meeting length in minutes.|
|**TotalAccept**|**int**|Total number of meeting acceptances.|
|**TotalDecline**|**int**|Total number of meeting declines.|
|**TotalNoResponse**|**int**|Total number of invitees who did not respond to the meeting invite.|
|**TotalAttendees**|**int**|Sum of total accept, total no-response, plus organizer.|
|**TotalDoubleBooked**|**int**|Number of attendees who had conflicting meetings or appointments on their calendar.|
|**TotalEmailsDuringMeeting**|**int**|Number of emails sent during the meeting by every attendee who did not decline.|

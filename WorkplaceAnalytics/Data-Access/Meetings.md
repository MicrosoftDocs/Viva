---
# Metadata Sample
# required metadata

title: Meetings table (WPA Data Access)
description: One row for each meeting and appointment
author: gbowerman
ms.author: guybo
ms.date: 05/11/2018
ms.topic: language-reference
ms.prod: wpa
---
# Meetings table (CSV)


  Contains one row for each meeting and appointment. Recurring meetings will result in a row for each occurrence.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MeetingId**|**string**|Unique identifier for each meeting (including recurring meetings). Primary key.|
|**ICalUid**|**string**|Meeting calender ID.|  
|**Subject**|**string**|Meeting subject. Respects tenant privacy settings - see [Workplace Analytics settings](https://docs.microsoft.com/workplace-analytics/setup/set-up-workplace-analytics#step-four-configure-workplace-analytics-settings).|
|**IsRecurring**|**boolean**|True if this is a recurring meeting.|
|**IsCanceled**|**boolean**|True if the meeting was canceled.|
|**StartTime**|**datetime**|Meeting start time.|
|**DurationMinutes**|**int**|Meeting length in minutes.|
|**TotalAccept**|**int**|Total number of meeting acceptances.|
|**TotalDecline**|**int**|Total number of meeting declines.|
|**TotalNoResponse**|**int**|Total number of invitees who did not respond to the meeting invite.|
|**TotalAttendees**|**int**|Sum of total accept, total no-response, plus organizer.|
|**TotalDoubleBooked**|**int**|Number of attendees who had clashing meetings or appointments on their calendar.|
|**TotalEmailsDuringMeeting**|**int**|Number of emails sent during the meeting by every attendee who did not decline.|

  
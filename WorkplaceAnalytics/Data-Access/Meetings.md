---

ROBOTS: NOINDEX,NOFOLLOW
title: Meetings for Workplace Analytics Data export
description: One row for each meeting or appointment
author: paul9955
ms.author: v-mideh
ms.topic: article
ms.prod: wpa
---

# Meetings (.csv)

This file includes one row for each meeting or appointment with the following metrics. Recurring meetings result in a row for each occurrence.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|MeetingId|string|Unique identifier for each meeting (including recurring meetings); primary key|
|ICalUid|string|Meeting calendar ID|  
|Subject|string|Meeting subject (respects tenant privacy settings; see [Workplace Analytics Privacy settings](../use/settings.md#privacy-settings))|
|IsRecurring|boolean|True if this is a recurring meeting|
|IsCanceled|boolean|True if the meeting was canceled|
|StartTime|datetime|Meeting start time|
|DurationMinutes|integer|Meeting length in minutes|
|TotalAccept|integer|Total number of meeting acceptances|
|TotalDecline|integer|Total number of meeting declines|
|TotalNoResponse|integer|Total number of invitees who did not respond to the meeting invite|
|TotalAttendees|integer|Sum of total accept, total no-response, plus organizer|
|TotalDoubleBooked|integer|Number of attendees who had conflicting meetings or appointments on their calendar|
|TotalEmailsDuringMeeting|integer|Number of emails sent during the meeting by all attendees who did not decline the meeting invitation|
|TotalTentativelyAccepted|integer|Total number of invitees who tentatively accepted|

## Related topics

[Data export](./data-access.md)
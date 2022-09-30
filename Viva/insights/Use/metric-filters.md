---
ROBOTS: NOINDEX,NOFOLLOW
title: Advanced insights metric filters 
description: Describes the filters that analysts can use to refine metrics in queries in the advanced insights app with Microsoft Viva Insights
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
manager: scott.ruble
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 

---

# Advanced insights metric filters

To customize the results from [queries](/viva/insights/tutorials/query-basics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), you use metrics (see [metric definitions](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)).

After you select a metric for a Viva Insights query, you can narrow the focus of that metric by applying filters. You can also rename the metric to indicate the new focus that you gave when you applied filters; its new name will appear in the query results. See [Apply a metric filter](#apply-a-metric-filter).

## Call filters

| Filter | Description |
| ------ | ----------- |
| Day of week | The day of the week during which the call was placed |
| Duration (in hours)  | The amount of time, in hours, that the call lasted |
| Included multitasking | Filters the call counts to only count activity during which the person sent one or more emails or instant messages, excluding instant messages sent within the related Teams meeting chat room during the meeting or call. |
| Is organizer  | True means that this person initiated the call; <br>False means that this person did not initiate the call. |
| IsScheduledCall  | True means that this call is scheduled on someone's Outlook calendar; <br>False means that this call is not scheduled on any person's Outlook calendar. |
| Time of day started &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  | The time of day that the call began |
| TotalParticipants  | The number of participants in the call |

## Email filters

| Filter | Description |
| ------ | ----------- |
| Day of week | Day of the week on which the email was sent |
| IsSender | True means that this person sent the email; <br>False means that this person did not send the email. |
| Is sent during meeting | Counts emails that a person sends during a meeting |
| Is sent during unscheduled call | Counts emails sent during an unscheduled Teams call. |
| Time of day | Time of day on which the email was sent |
| Number of recipients | Number of the recipients on which the email was sent |
| Subject | The Subject line of the email |

## Instant messages (IM) filters

| Filter | Description |
| ------ | ----------- |
| Day of week  | The day of the week on which the IM was sent. |
| InteractionType | The type of chat in which the IM appears, namely in a one-on-one chat or in a group chat. |
| IsAfterHours | True means that the IM was sent during the recipient's after-hours period; <br>False means that it was not sent during that period. |
| IsSender | True means that this person sent the IM; <br>False means that this person did not send the IM. |
| Is sent during meeting | Counts Teams IMs that a person sends during a meeting. |
| Is sent during unscheduled call | Counts Teams IMs sent during an unscheduled Teams call.|
| Time of day &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Time at which the IM was sent. |
| TotalParticipants | Number of people who participated in the IM thread, including the sender of the initial IM. |

<!-- Still need in this table: 'Time (hours)'  -->

## Meeting filters

| Filter | Description |
| ------ | ----------- |
| Duration (in hours) &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Duration of the meeting. |
| Included multitasking | Filters the count of meetings to only count activity during which the person sent one or more emails or instant messages, excluding instant messages sent within the related Teams meeting chat room during the meeting or call. |
| Is recurring    | True means that this meeting is set to recur; <br>False means that this meeting is not set to recur. |
| IsCancelled     | True means that this meeting has been cancelled; <br>False means that this meeting has not been canceled. |
| Subject         | Subject line of the meeting invitation. |
| Total accepted  | Number of invitees who have accepted the meeting invitation. |
| Total attendees | Total attendees can be configured at the report level by using an [attendee-exclusion rule](/viva/insights/tutorials/attendee-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). When you select an attendee-exclusion rule, you redefine meeting attendance to include or exclude the cases of “tentative” and “no response.” Therefore, based on the attendee-exclusion rule that you have selected, Total attendees can mean one of the following: <br> <ul> <li>Total attendees = Total accepted </li> <li>Total attendees = Total accepted + Total no response </li> <li>Total attendees = Total accepted + Total tentatively accepted </li> <li>Total attendees = Total accepted + Total no response + Total tentatively accepted </li> </ul> |
| Total declined  | Number of invitees who have declined the meeting invitation. |
| Total double booked  | Number of invitees who have accepted this meeting invitation and the invitation of another meeting that is scheduled to overlap with this one. |
| Total emails sent during meeting   | Number of emails sent by all participants during the meeting. |
| Total no responses   | Number of invitees who did not respond to the meeting invitation. |
| Day of week          | Day of the week for which the meeting is scheduled. |
| Is organizer         | The person who invited others to the meeting. |
| <a name="time-of-day-started-filter-define"></a>Time of day started  | Time of day that the meeting was scheduled (in Outlook) to start. |  

<!-- Still need in this table: 'MeetingResources'  -->

## Participant filters

Filters of the following types can be used in various query types to filter participants in collaboration activities &ndash; that is, in emails, IMs, calls, or meetings.

### Individual participant filters

| Filter &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; | Description |
| ------ | ----------- |
| Is Manager Present   | A Boolean that indicates that the participant is the direct manager of the measured user. | 
| Is Direct Report Present  | Indicates that the participant is the direct report of the measured user. | 

### Groups of participant filters

Organizational-data attributes and CRM attributes can also be used as participant filters. 


| Filter  | Description |
| ------ | ----------- |
| Organizational attributes (required) | Organizational attributes that are [required](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#required-attributes) are always available for use as participant filters. |
| Organizational attributes (optional) | Also available for use as participant filters are optional organizational attributes ([reserved optional attributes](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#reserved-optional-attributes) and [custom attributes](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#custom-attributes)) that have been uploaded in an [organizational data upload](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). |
| CRM attributes (required) | CRM attributes that are [required](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#required-and-reserved-attributes) are available for use as participant filters in query types that permit both organizational and CRM data analysis (person, person-to-group, and group-to-group queries). | 
| CRM attributes (optional) | Optional CRM attributes ([reserved optional attributes](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#required-and-reserved-attributes) and [custom attributes](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#custom-attributes)) are available for use as participant filters in query types that permit both organizational and CRM data analysis (person, person-to-group, and group-to-group queries). |

## Teams channel metric filters

### Filters for channel messages

These filters can be used to customize the following Teams channel metrics:

* Channel message hours
* After hours channel message hours
* Working hours channel message hours
* Channel messages sent
* Channel visits
* Channel reactions

| Filter | Description |
| ------ | ----------- |
| Channel member count | If the selected Channel member count > "X", return a metric for posts or replies that were sent or read on channels with a number of channel members > "X". |
| Channel name | If the selected Channel name = "X", return a metric for posts or replies that were sent or read on channel "X". |
| Day of week | If the selected Day of week = "Monday" (or any other day), returns a metric for posts or replies that were sent or read on Monday using the time zone of the person. |
| Device | If the selected Device = Mobile/ Desktop/Web, return metric for posts/replies made from Mobile/ Desktop/Web. |
| Interaction type | <ul><li>If Interaction type = “Post sent”, returns metric for only sent post messages.</li><li>If Interaction type = "Reply sent", returns metric for only sent reply messages.</li><li>If Interaction type = “Channel visit”, returns metric for only Channel Visits.</li></ul> |
| Team name | If the selected Team name = "X", return metric for posts/replies that are sent/read on Team "X". |
| Time of day | The time of day the activity occurred using the time zone of the person.  |
| Total participants | If the selected Participant count > "X", return metric with total number participants >"X". |

### Filters for channel activity

These filters can be used to customize the following Teams channel metrics:

* Teams with active engagement
* Channels with active engagement

| Filter | Description |
| ------ | ----------- |
| Channel member count  | If the selected Channel member count > "X", return an active Teams or channel metric for channels with the number of channel members > "X". |
| Channel name | If the selected Channel name = "X", return an active Teams or channel metric with the channel name "X". |
| Interaction type | <ul><li>If the Interaction type = “Post sent”, return a metric only for active Teams or channels in which person sent post messages.</li><li>If the Interaction type = “Reply sent”, returns a metric only for active Teams or channels in which reply messages were sent.</li><li>If the Interaction type = "Channel visit", returns a metric only for active Teams or channels in which the person had Channel visits.</li><li>If the Interaction type = “Reaction”, returns a metric only for active Teams or channels in which the person sent reactions.</li></ul> |
| Team name | If the selected team name = "X", return an active Teams or channel metric with the Team name "X". |

## Apply a metric filter

In this example procedure, you apply a filter to a metric in a person query. Specifically, you restrict the _Email sent_ metric to include only email that was sent during a particular time of day. Then, for the population of employees that you specify, the query results will show the number of emails that were sent during the time of day that you selected.

1. In **Analyze** > **Query designer**, select **Get started** under **Query**, and then select the type of query you want to create.

2. Under **Select metrics**, select **Emails sent**:

   ![Select emails sent.](../images/wpa/use/emails-sent.png)

3. Select edit (the pencil icon):

   ![Select pencil to edit.](../images/wpa/use/emails-sent-edit-pencil.png)

4. Under **Emails sent where**, select **Add filter** and then select **Email**:

   ![Select email.](../images/wpa/use/add-filter-email.png)

5. Next to **Email's**, select **Time of day**:

   ![Select time of day.](../images/wpa/use/email-sent-time-of-day.png)

6. In the adjacent fields, select "<" (before) and specify 7:00 PM.

   ![Sent before 7:00 PM.](../images/wpa/use/sent-before-7pm.png)

7. You have now filtered your base metric. You can optionally change the display name of this new filtered metric. In the field under **Display Name**, change **Emails sent** to **Emails sent before 7 PM** and then click outside the field to save the new name:

   ![Edit the metric name.](../images/wpa/use/edit-metric-name.png)

   After you run the query, the edited metric name will appear as a header in the query results:

   ![Edited metric name.](../images/wpa/use/edited-metric-name.png)

## Related topic

* [Metric descriptions](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)

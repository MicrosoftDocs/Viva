---

title: Workplace Analytics metric filters 
description: Describes the filters that analysts can use to refine metrics in queries 
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---

# Metric filters

To customize Workplace Analytics [queries](../tutorials/query-basics.md), you use metrics (see [metric definitions](metric-definitions.md)). After you select a metric for a query, you can narrow the focus of that metric by [applying filters](#to-apply-a-metric-filter). 

## Metric filters, by type

### Filters for calls

| Filter | Description |
| ------ | ----------- |
| Day of week | The day of the week during which the call was placed | 
| Duration (in hours)  | The amount of time, in hours, that the call lasted | 
| Is organizer  | True = this person initiated the call; False = this person did not initiate the call | 
| IsScheduledCall  | True = this call is scheduled on someone's Outlook calendar; False = this call is not scheduled on any person's Outlook calendar | 
| Time of day started &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  | The time of day that the call began | 
| TotalParticipants  | The number of participants in the call | 

### Filters for emails

| Filter | Description |
| ------ | ----------- |
| Day of week | Day of the week on which the email was sent | 
| IsSender | True = this person sent the email; False = this person did not send the email | 
| Time of day | Time of day the sent on which the email was sent | 
| Number of recipients | Number of the recipients on which the email was sent | 
| Subject | The Subject line of the email | 

### Filters for instant messages

| Filter | Description |
| ------ | ----------- |
| Day of week  | The day of the week on which the IM was sent | 
| IsAfterHours | True = This IM was sent during  the recipient's after-hours period | 
| InteractionType | The type of chat in which the instant message (IM) appears, namely 1:1 IMs or group chats. (The possible values are _OneToOneChat_ and _GroupChat_).  | 
| IsSender | True = this person sent the email; False = this person did not send the email | 
| Time of day sent &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Time at which the IM was sent | 
| TotalParticipants | Number of people who participated in the IM thread, including the sender of the initial IM | 

### Filters for meetings 

| Filter | Description |
| ------ | ----------- |
| Duration (in hours) &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Duration of the meeting | 
| Is recurring | True = this meeting is set to recur; False = this meeting is not set to recur | 
| IsCancelled   | True = this meeting has been cancelled; False = this meeting has not been cancelled | 
| Subject         | Subject line of the meeting invitation | 
| Total accepted  | Number of invitees who have accepted the meeting invitation | 
| Total declined  | Number of invitees who have declined the meeting invitation | 
| Total double booked  | Number of invitees who have accepted this meeting invitation and the invitation of another meeting that is scheduled to overlap with this one | 
| Total emails sent during meeting   | Number of emails sent by all participants during the meeting | 
| Total no responses   | Number of invitees who did not respond to the meeting invitation | 
| Day of week   | Day of the week for which the meeting is scheduled | 
| Is organizer   | The person who invited others to the meeting | 
| Time of day started   | Time of day that the meeting actually started | 
| Total attendees   | Total attendees can be configured at the report level by using an [attendee-exclusion rule](../tutorials/attendee-exclusion-rules.md). When you select an attendee-exclusion rule, you redefine meeting attendance to include or exclude the cases of “tentative” and “no response.” Therefore, based on the attendee-exclusion rule that you have selected, Total attendees can mean one of the following: <br> <ul> <li>Total attendees = Total accepted </li> <li>Total attendees = Total accepted + Total no response </li> <li>Total attendees = Total accepted + Total tentatively accepted </li> <li>Total attendees = Total accepted + Total no response + Total tentatively accepted </li> </ul> | 

<!-- Still need in this table: MeetingResources  -->



## To apply a metric filter

In this example, you apply a filter to a metric in a person query.

1. In Workplace Analytics, select **Analyze** > **Queries** > **Person**.

2. Under **Select metrics**, select **Emails sent**:
   
   ![Select emails sent](../images/wpa/use/emails-sent.png)

3. Select edit (the pencil icon):

   ![Select pencil to edit](../images/wpa/use/emails-sent-edit-pencil.png)

4. Under **Emails sent where**, select **Add filter** and then select **Email**:

   ![Select email](../images/wpa/use/add-filter-email.png)

5. Next to **Email's**, select **Time of day**:

   ![Select time of day](../images/wpa/use/email-sent-time-of-day.png)

6. In the adjacent fields, select "<" (before) and specify 7:00 PM. 

   ![Sent before 7:00 PM](../images/wpa/use/sent-before-7pm.png)

7. You have now filtered your base metric. To indicate its new state, you can now optionally change its display name. In the field under **Display Name**, change **Emails sent** to **Emails sent before 7 PM** and then click outside the field to save the new name:

   ![Edited metric name](../images/wpa/use/edit-metric-name.png)

   Now, after you run the query, the edited metric name will appear as a header in the query results: 

      ![Edited metric name](../images/wpa/use/edited-metric-name.png)

## Related topics

* [Metric descriptions](metric-definitions.md)

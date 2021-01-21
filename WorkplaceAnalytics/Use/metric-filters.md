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

To customize the results from Workplace Analytics [queries](../tutorials/query-basics.md), you use metrics (see [metric definitions](metric-definitions.md)). 

After you select a metric for a query, you can narrow the focus of that metric by applying filters. You can also rename the metric to indicate the new focus that you gave when you applied filters; its new name will appear in the query results. See [Apply a metric filter](#apply-a-metric-filter).

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

### Filters for instant messages (IMs)

| Filter | Description |
| ------ | ----------- |
| Day of week  | The day of the week on which the IM was sent | 
| IsAfterHours | True = This IM was sent during  the recipient's after-hours period | 
| InteractionType | The type of chat in which the IM appears, namely in a _OneToOneChat_ or in a  _GroupChat_ | 
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


### Filters for participants

The following tables list filters that can be used in various query types to filter participants in collaboration activities &ndash; that is, in emails, IMs, calls, or meetings. 

#### Individual filters

| Filter &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; | Description |
| ------ | ----------- |
| Is Manager Present   | A Boolean that indicates that the participant is the direct manager of the measured user. | 
| Is Direct Report Present  | Indicates that the participant is the direct report of the measured user. | 
 
#### Groups of filters

Organizational-data attributes and CRM attributes can also be used as participant filters. 

| Filter &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; | Description |
| ------ | ----------- |
| Organizational attributes (required) | Organizational attributes that are [required](../setup/prepare-organizational-data.md#required-attributes) are always available for use as participant filters. | 
| Organizational attributes (optional) | Also available for use as participant filters are optional organizational attributes ([reserved optional attributes](../setup/prepare-organizational-data.md#reserved-optional-attributes) and [custom attributes](../setup/prepare-organizational-data.md#custom-attributes)) that have been uploaded in an [organizational data upload](../setup/upload-organizational-data.md). | 
| CRM attributes (required) | CRM attributes that are [required](../setup/crm-data-upload.md#required-and-reserved-attributes) are always available for use as participant filters. | 
| CRM attributes (optional) | Optional CRM attributes ([reserved optional attributes](../setup/crm-data-upload.md#required-and-reserved-attributes) and [custom attributes](../setup/crm-data-upload.md#custom-attributes)) are also available for use as participant filters. | 

## Apply a metric filter

In this example procedure, you apply a filter to a metric in a person query. Specifically, you restrict the _Email sent_ metric to include only email that was sent during a particular time of day. Then, for the population of employees that you specify, the query results will show the number of emails that were sent during the time of day that you selected.   

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

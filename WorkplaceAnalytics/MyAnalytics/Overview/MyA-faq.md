---
# Metadata Sample
# required metadata

title: MyAnalytics FAQ
description: Frequently asked questions about MyAnalytics
author: paul9955
ms.author: madehmer
ms.date: 2/1/2019
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
localization_priority: Once
---

# Frequently asked questions for MyAnalytics

> [!Note] 
> Productivity insights that are powered by MyAnalytics are becoming broadly available for Office 365 users. [Learn more](./plans-environments.md) about the experiences that users will get in each plan.

The sets of questions and answers in this topic apply to different sets of readers.

  * The [Privacy](#privacy) section is for everyone.

Two later sections are grouped by role:

   * For [MyAnalytics users](#for-myanalytics-users)
   * For [IT administrators](#for-it-administrators)

## Privacy  

### Where does MyAnalytics get my data?

MyAnalytics uses data from your Office 365 mailbox, namely data about your email and your meetings plus data about your calls and chats in Teams or in Skype for Business. Every calculation that MyAnalytics performs is based on data that you, yourself, could obtain by gathering and examining metadata of your emails, meetings, calls, and chats, such as their start and end times and their subject lines. In other words, MyAnalytics automates what would otherwise be a painstaking task; these automatic calculations provide you with transparency into your workplace collaboration habits.

MyAnalytics does not have any tracking software running on your computer.

### What data does MyAnalytics use and not use?

#### MyAnalytics uses

 * Information from email items:

   * Metadata. This includes the email's timestamp, sender, recipients, and "read" signal. 
   * Statements that people have made in email body text. These statements are used to create [To-do cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) for your use. 
   * Actions of other users who receive your email -- for example, whether or not they have opened your email. (This would be used only in aggregate form, to protect individual privacy.) 

 * Information from calendar items:
   * Type (meeting or appointment)
   * Status (busy, free, out-of-office, tentative)
   * Category
   * Subject
   * Duration
   * Attendees

 * Information from Teams and from Skype for Business:
   * MyAnalytics counts audio calls, video calls, and chats that people make in Teams and in Skype for Business as collaboration activities.

#### MyAnalytics does not use

 * Data derived from activities on your computer, such as applications that you've used and websites that you've visited.
 * Email and calendar data from people outside of your organization, with the following exception: MyAnalytics uses data that is present in your own Office 365 mailbox. For example, if you conduct a meeting with a person outside of your organization, the start and end times of that meeting can be found in your mailbox and therefore are visible to you. This data, therefore, can be used in computations about your collaboration history.  

### Who can see my data?

Only you can see the statistics and insights that are generated from your data. Your manager or system administrator cannot see these statistics and insights. Your data might be used in aggregate, de-identified form to calculate email read rates, for example.
 
For more details, see [Privacy](Privacy-Guide.md).

## For MyAnalytics users

### Metrics

#### Data sources

##### Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

#### Meetings

##### Do "Meeting Hours" include time that I block out for personal work on my calendar?

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/en-us/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time does not count as meeting hours.

##### Why is my total meeting hours (that's included as part of working hours and after hours work) larger than my total meeting hours for the week?

This can occur because of the way MyAnalytics calculates meeting hours:

* The meeting hours total includes *adjusted* hours for *attended* meetings.  
* As compared to total working hours and after-hours work, which includes the number of meeting hours (not adjusted) for *scheduled* meetings.

This discrepancy can occur when meetings overlap and MyAnalytics doesn’t know which meetings were attended, so the meeting hours total will include *adjusted* hours, which are an estimate of time actually spent in meetings. For example, let's say you’re double booked for two meetings from 4:30 to 5:30 PM, and your work day ends at 5 PM. For this scenario, MyAnalytics adjusts the meeting hours to one hour, since you cannot attend two meetings at the same time. However, MyAnalytics does not adjust for the two scheduled meetings, which results in MyAnalytics adding one hour to total working hours and one hour to after-hours work. You can avoid this discrepancy by declining any scheduled meetings you do not attend.

#### Email

##### Do “Email Hours” count emails that I read or send on my mobile device, even if it’s the default iPhone app?

Yes. We calculate email hours based on how many emails you read and send (as well as the time at which they are read and sent). For more information, see [Email hours](../Use/MyA-Dashboard/MyA-DB-Emails.md).

#### Focus hours

##### Do “Focus hours” exclude time that I block out for personal work on my calendar?

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/en-us/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time can count as focus hours. For more information, see [Focus hours](../Use/MyA-Dashboard/MyA-DB-Focus-hours.md). To exclude focus hours, right-click the appointment and set Show As to “Out of Office."

##### Can I change my settings to make "After Hours" more accurate?

Yes. You can change your time zone and your work hours in your [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).

##### Why do my Focus hours not seem correct?

Try the following to troubleshoot your focus-time totals:

1. Verify that your work hours and time zone settings are correct. (See  [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).)
2. For more information about focus hours, see [Focus hours](../Use/MyA-Dashboard/MyA-DB-Focus-hours.md).  

##### How do I tell MyAnalytics that I am on vacation?

If you plan to go on vacation, create a calendar event that includes the days of your vacation and set its status to “Out of Office." This causes your focus hours and your meeting hours to both count as zero during your vacation.  

### Usage

<!-- To be written

#### What should be my goal be for Meeting Hours, email, focus and after hours? 
 
#### How can I engage my supervisor on on goals and expectations? 
 
#### How can I help my team reduce meeting time? 

-->

##### How do I track my team’s progress?

You can track your teams progress if the team has conducted a program to change its collaboration habits. During such a program, its statistics, and thus its progress towards its improvement goals, are tracked. For information about starting such a program, see [Get started](../use/mya-adoption/team-adopt-intro.md). For information about tracking the progress that your team made, see [Measure](../use/mya-adoption/team-adopt-measure.md).

### Outlook add-in

##### The Outlook add-in displays To-do cards (commitments). Are they available in all languages, or just in English?

The [to-do cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) of the Outlook add-in are available only in English.

##### Can I get email read rates for shared or secondary mailboxes?

MyAnalytics does not use data from shared or secondary mailboxes.

##### Why are my email read statistics not available?

To see read statistics for an email that you sent, you must have sent it within the past 14 days to at least five recipients. 

## For IT administrators

#### Where is user data stored?

User metrics data is stored in users' mailboxes.

<!-- REMOVED 26 OCTOBER PER PARAMA and PBergen
An exception is the signal that an email has been delivered, read, replied to, or forwarded. This signal is copied to a transient store. All data in the transient store is deleted after 14 days.
-->

#### How long does it take for the personal dashboard to become available?

The personal dashboard is available to a MyAnalytics user as soon as they receive their [welcome email](../setup/MyA-Welcome-email.md). This happens about three days after the MyAnalytics license was assigned to the participant. For more information, see [Assign MyAnalytics licenses to users](../setup/assign-licenses.md).

#### When the dashboard is activated, does it show any historical data or does it start 'from scratch'?

Upon activation, MyAnalytics processes historical data for 80 days before the date of activation. No data from before this 80-day limit is displayed in the dashboard.

#### Can MyAnalytics licenses be assigned to shared mailboxes?

No, currently MyAnalytics licenses cannot be assigned to shared mailboxes.

##### Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

#### I have not received my Skype for Business data. It seems to have gone missing. Where is it?

Skype for Business data is usually prompt. However, in rare instances, users can experience delays of from two to four days. User actions completed on a Friday might not be included in MyAnalytics computations that are executed the following Monday. In such cases, "after hours," which includes Teams data, is updated later. Similarly, certain meetings might be marked as "Late start" after a day or two, or a digest email sent on a Monday or Tuesday, might not immediately include the data. In all such cases, the metrics are updated as soon as the data comes in.

#### Can I remove the company-averages metrics from the personal dashboard?

Yes. It is possible to remove this field so that MyAnalytics users do not see it. For more information, contact your Microsoft account team or file a service request. Note that you can also limit which users are included in this field, by using PowerShell. Also see [MyAnalytics setup](../setup/mya-setup-checklist.md).

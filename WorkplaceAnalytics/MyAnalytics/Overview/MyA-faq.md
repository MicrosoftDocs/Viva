---
# Metadata Sample
# required metadata

title: MyAnalytics FAQ
description: MyAnalytics FAQ
author: paul9955
ms.author: v-pascha
ms.date: 04/10/2018
ms.topic: get-started-article
ms.prod: mya
localization_priority: Once
---

# MyAnalytics: Frequently asked questions

The following questions and answers are grouped by role, for [MyAnalytics users](MyA-faq.md#for-myanalytics-users) and for [IT administrators](MyA-faq.md#for-it-administrators).  

<!-- [Pending review from Parama]

## Privacy  
 
### Where does MyAnalytics get my data? 

We use email and calendar activity data that already exists in your Office 365 mailbox. MyAnalytics does not have a tracking software running on your computer 
 
### What data does MyAnalytics use and not use? 

#### MyAnalytics uses 

 * Email 
   * Metadata, including timestamp, sender, recipients, and read signal 
   * Statement that user makes in emails 
   * Actions of other users who receive your email, e.g. whether they have opened your email or not (in aggregate form to protect individual privacy) 
 * Calendar 
   * Type (meeting or appointment) 
   * Status (busy, free, out-of-office, tentative) 
   * Category 
   * Subject 
   * Duration 
   * Attendees 

#### MyAnalytics does not use 

 * Activity data on your computer, such as applications used and websites visited 
 * Email and calendar data from people outside of your organization 
 
### Who can see my data? 

Only you can see statistics and insights generated from your data. Your manager or system administrator cannot see them. Your data may be used in aggregate, de-identified form to calculate company-wide average, for example. 
 
For more details, see Privacy [link to privacy docs]  

-->

# For MyAnalytics users

## Metrics 

### Meetings

#### Does “Meeting Hours” include time that I block out for personal work on my calendar? 

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/en-us/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time does not count as meeting hours. 

### Email
 
#### Does “Email Hours” count emails that I read or send on my mobile device, even if it’s the default iPhone app? 

Yes. We calculate email hours based on how many emails you read and send (as well as the time at which they are read and sent). For more information, see [Email hours](../Use/MyA-Dashboard/MyA-DB-Emails.md). 

### Focus hours
 
#### Does “Focus hours” exclude time that I block out for personal work on my calendar? 

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/en-us/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time can count as focus hours. For more information, see [Focus hours](../Use/MyA-Dashboard/MyA-DB-Focus-hours.md). To exclude focus hours, right-click the appointment and set Show As to “Out of Office." 
 
#### Can I change my settings to make “After Hours” more accurate? 

Yes. You can change your time zone and your work hours in your [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).

#### Why do my Focus hours not seem correct? 

Try the following to troubleshoot your focus-time totals:

1. Verify that your work hours and time zone settings are correct. (See  [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).)
2. For more information about focus hours, see [Focus hours](../Use/MyA-Dashboard/MyA-DB-Focus-hours.md).  
 
#### How do I tell MyAnalytics that I am on vacation? 

If you plan to go on vacation, create a calendar event that includes the days of your vacation and set its status to “Out of Office." This causes your focus hours and your meeting hours to both count as zero during your vacation.  
 
## Usage 

<!-- To be written

#### What should be my goal be for Meeting Hours, email, focus and after hours? 
 
#### How can I engage my supervisor on on goals and expectations? 
 
#### How can I help my team reduce meeting time? 

-->
 
#### How do I track my team’s progress? 

You can track your teams progress if the team has conducted a program to change its collaboration habits. During such a program, its statistics, and thus its progress towards its improvement goals, are tracked. For information about starting such a program, see [Get started](../use/mya-adoption/team-adopt-intro.md). For information about tracking the progress that your team made, see [Measure](../use/mya-adoption/team-adopt-measure.md).

## Outlook add-in 

#### The Outlook add-in displays To-do cards (commitments). Are they available in all languages, or just in English? 

The [to-do cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) of the Outlook add-in are available only in English.
 
#### Can I obtain email read rates for shared or secondary mailboxes? 

MyAnalytics does not use data from shared or secondary mailboxes. 
 
#### Why are my email read statistics not available? 

To see read statistics for an email that you sent, you must have sent it within the past 14 days to at least five recipients. 
 
## For IT administrators

#### Where is user data stored? 

User metrics data is stored in users’ mailboxes. An exception is the signal that an email has been delivered, read, replied to, or forwarded. This signal is copied to a transient store. All data in the transient store is deleted after 14 days. 
 
#### How long does it take for the personal dashboard to become available? 

The personal dashboard is available to a MyAnalytics user as soon as they receive their [welcome email](../setup/MyA-Welcome-email.md). This happens about three days after the MyAnalytics license was assigned to the participant. For more information, see [Assign MyAnalytics licenses to users](../setup/assign-licenses.md).
 
#### When the dashboard is activated, does it show any historical data or does it start ‘from scratch’? 

Upon activation, MyAnalytics processes historical data for 80 days before the date of activation. No data from before this 80-day limit is displayed in the dashboard. 

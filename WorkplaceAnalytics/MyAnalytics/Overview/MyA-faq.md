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
---

# MyAnalytics: Frequently asked questions

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

A team can implement a multi-week program to change its collaboration habits for the better. During such a program, its statistics, and thus its progress towards its improvement goals, are tracked. For information about starting such a program, see [Get started](../use/mya-adoption/team-adopt-intro.md). For information about tracking your team's progress, see [Measure](../use/mya-adoption/team-adopt-measure.md).

## Add-in / Nudges 

#### Are commitments available in all languages, or just English? 

Add-in’s Commitment<link to add-in commitment doc> feature only supports English today. 
 
#### Can I get email read rates for shared or secondary mailboxes? 

MyAnalytics does not take shared mailboxes into account. 
 
#### Why are my email read statistics not available? 

Your email must be sent to at least 5 recipients and less than 14 days old for read statistics to be available. 
 
## IT Administrator 

#### Where is the data stored? 

All user’s metrics data are stored in each user’s mailbox. An exception is the signal that an email has been delivered/read/replied/forwarded. This signal is copied to a transient store. All data in the transient store is deleted after 14 days. 
 
#### Why does it take 2 weeks for the personal dashboard to become available? 
This question is no longer applicable. It’s now available on-the-fly but takes 3 days for the data to be fully stored.  
 
#### Will the dashboard show any historic data upon activation, or does it start ‘from scratch’? 

Upon activation, MyAnalytics will process historical data for 80 days prior to the date of activation. Data from earlier period will not be available in the dashboard 


---
# Metadata Sample
# required metadata

title: MyAnalytics FAQ
description: Frequently asked questions about MyAnalytics
author: madehmer
ms.author: v-midehm
ms.date: 04/03/2019
ms.topic: article
localization_priority: once
ms.prod: mya

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

MyAnalytics uses data from your Office 365 mailbox, namely data about your email and your meetings plus data about your calls and chats in Teams or in Skype for Business.

MyAnalytics data is stored in your mailbox itself, and gets the same protection that your email and calendar itself gets. 

Every calculation that MyAnalytics performs is based on data that you, yourself, can get by gathering and examining metadata of your emails, meetings, calls, and chats, such as their start and end times and their subject lines. In other words, MyAnalytics automates what would otherwise be a painstaking task; these automatic calculations provide you with transparency into your workplace collaboration habits.

MyAnalytics does not have any tracking software running on your computer.

### What data does MyAnalytics use and not use?

#### MyAnalytics uses

 * Information from email items:

   * Metadata - which includes the email's timestamp, sender, recipients, and "read" signal
   * Statements that people have made in email body text - these statements are used to create [task cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) for your use only
   * Actions of other users who receive your email - for example, whether or not they have opened your email. (This would be used only in aggregate form, to protect individual privacy.)

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

##### Q1. Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

#### Meetings

##### Q1. Does "meeting time" include time that I block out for personal work on my calendar?

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/en-us/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time does not count as meeting time and will count as focus time.

#### Focus time

##### Q1. Does “focus time” exclude time that I block out for personal work on my calendar?

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/en-us/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time can count as focus time. For more information, see [Focus](../Use/focus.md). To exclude focus time, right-click the appointment and set **Show As** to **Out of Office**.

##### Q2. Can I change my settings to make time outside of work more accurate?

Yes. You can change your time zone and your working time in your [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).

##### Q3. Why do my focus time seem incorrect or inaccurate?

Try the following to troubleshoot your focus-time totals:

1. Verify that your work time and time zone settings are correct. (See  [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance).)
2. For more information about focus time, see [Focus](../Use/focus.md).  

##### Q4. How do I tell MyAnalytics that I am on vacation?

If you plan to go on vacation, create a calendar event that includes the days of your vacation and set its status to **Out of Office**. This causes your focus time and meeting time to both count as zero during your vacation.  

### Usage

<!-- To be written

#### What should my goal be for Meeting Hours, email, focus and after hours? 
 
#### How can I engage my supervisor on goals and expectations? 
 
#### How can I help my team reduce meeting time? 

-->

##### Q1. How do I track my team’s progress?

You can track your teams progress if the team has conducted a program to change its collaboration habits. During such a program, its statistics, and thus its progress towards its improvement goals, are tracked. For information about starting such a program, see [Get started](../use/mya-adoption/team-adopt-intro.md). For information about tracking the progress that your team made, see [Measure](../use/mya-adoption/team-adopt-measure.md).

### Insights Outlook add-in

##### Q1. The Insights Outlook add-in displays task cards (commitments). Are they available in all languages, or just in English?

The [task cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) of the Outlook add-in are available only in English.

##### Q2. Can I get email read rates for shared or secondary mailboxes?

MyAnalytics does not use data from shared or secondary mailboxes.

##### Q3. Why are my email read statistics not available?

To see read statistics for an email that you sent, you must have sent it within the past 14 days to at least five recipients. 

##### Q4. Can I turn off email digests? 

Yes, follow the steps in [To opt out of email digests](../use/email-digest-2.md#opt-out-of-email-digests).

##### Q5. Can I opt out of MyAnalytics? 

Yes, follow the steps in [To opt out of MyAnalytics](../use/dashboard-2.md#can-i-opt-out-of-myanalytics).

##### Q6. Can I turn off nudges? 

Yes, follow the steps in [To opt out of nudges](../use/mya-notifications.md#to-opt-out-of-nudges).

## For IT administrators

#### Q1. Where is user data stored?

User metrics data is stored in users' mailboxes.

#### Q2. How long does it take for the personal dashboard to become available?

The personal dashboard is available to MyAnalytics users as soon as they receive their [welcome email](../Use/MyA-Welcome-email.md). This happens up to four weeks after licenses with the MyAnalytics service are assigned to the participants. For more information, see [Assign licenses with MyAnalytics](../setup/Mya-setup-checklist.md#step-2-assign-licenses-with-myanalytics).

#### Q3. When the dashboard is activated, does it show any historical data or does it start 'from scratch'?

Upon activation, MyAnalytics processes historical data for 80 days before the date of activation. No data from before this 80-day limit is displayed in the dashboard.

#### Q4. Will MyAnalytics work for shared mailboxes?

No, currently the MyAnalytics service cannot be used with shared mailboxes.

#### Q5. Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

#### Q6. I have not received my Skype for Business data. It seems to have gone missing. Where is it?

Skype for Business data is usually prompt. However, in rare instances, users can experience delays of from two to four days. User actions completed on a Friday might not be included in MyAnalytics computations that are executed the following Monday. In such cases, non-working time, which includes Teams data, is updated later. Similarly, certain meetings might be marked as "Late start" after a day or two, or a digest email sent on a Monday or Tuesday, might not immediately include the data. In all such cases, the metrics are updated as soon as the data is updated.

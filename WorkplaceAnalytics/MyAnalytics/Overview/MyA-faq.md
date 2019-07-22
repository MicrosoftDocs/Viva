---
# Metadata Sample
# required metadata

title: MyAnalytics FAQ
description: Frequently asked questions about MyAnalytics
author: paul9955
ms.author: v-midehm
ms.date: 07/19/2019
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

### Q1 Who can see my data?

Only you can see your data. The statistics and insights that are generated from your data are for your eyes only. Your manager or system administrator cannot view your personal data.

For more details, see the [MyAnalytics privacy guide](Privacy-Guide.md).

### Q2 How does MyAnalytics protect my data?

MyAnalytics uses data from your Office 365 mailbox, namely data about your email and your meetings plus data about your calls and chats in Teams or in Skype for Business.

MyAnalytics stores your data in your mailbox itself, and gets the same protection that your email and calendar itself gets. This means your data is protected the same way your email and calendar information is kept private and protected.

Every calculation that MyAnalytics performs is based on data that you, yourself, can get by gathering and examining metadata of your email, meetings, calls, and instant messages, such as their start and end times and their subject lines. In other words, MyAnalytics automates what would otherwise be a painstaking task; these automatic calculations provide you with transparency into your workplace collaboration habits.

MyAnalytics does not have any tracking software running on your computer.

### Q3 What data does MyAnalytics use?

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

 * OneDrive SharePoint data: MyAnalytics shows a count of OneDrive and SharePoint documents that you have worked on. 

 * _Used only if you have opted in_: Data derived from activities on your computer, such as applications that you've used and websites that you've visited.

#### MyAnalytics does not use

 * Email and calendar data from people outside of your organization, with the following exception: MyAnalytics uses data that is present in your own Office 365 mailbox. For example, if you conduct a meeting with a person outside of your organization, the start and end times of that meeting can be found in your mailbox and therefore are visible to you. This data, therefore, can be used in computations about your collaboration history.  


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

### Opt out

#### Q1. Can I opt out of MyAnalytics? And if I do, can I opt back in later?

Yes to both questions. You can opt out of access to individual parts of MyAnalytics or out of all of MyAnalytics at once. And you can opt back in again later, if you want. 

See the following sections for more information:

##### Opt out of all of MyAnalytics

 * [Opt out of MyAnalytics](../use/opt-out-of-mya.md)

##### Opt out of individual parts of MyAnalytics

 * [Opt out of the MyAnalytics dashboard](../use/dashboard-2.md#opt-out-of-the-myanalytics-dashboard)
 * [Opt out of the weekly email digest](../use/email-digest-2.md#opt-out-of-email-digests)
 * [Remove Insights add-in from Outlook](../use/add-in.md#remove-the-insights-add-in-from-outlook)
 * [Opt out of inline suggestions](../use/mya-notifications.md#opt-out-of-inline-suggestions)

##### Q2. Why can I not see the MyAnalytics dashboard to opt-out?

To opt out, you use the MyAnalytics dashboard. The dashboard is available only if your organization has a _qualifying plan_. (All of the plans listed in the table under [Availability of features](../../myanalytics/overview/plans-environments.md#availability-of-features) are qualifying plans.) If an organization has no _qualifying plan_, its members see no elements of MyAnalytics and their data is not processed. 

### Insights Outlook add-in

##### Q1. The Insights Outlook add-in displays task cards (commitments). Are they available in all languages, or just in English?

The [task cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) of the Outlook add-in are available only in English.

##### Q2. Can I get email read rates for shared or secondary mailboxes?

MyAnalytics does not use data from shared or secondary mailboxes.

##### Q3. Why are my email read statistics not available?

To see read statistics for an email that you sent, you must have sent it within the past 14 days to at least five recipients.

## For IT administrators

#### Q1. How do I manage the MyAnalytics experience for users?

You can manage the experience in two ways: 
 * Turn on or off particular MyAnalytics elements for your entire organization. For more information, see [Configure access at the tenant level](../setup/configure-myanalytics.md#configure-access-at-the-tenant-level). 
 * Turn MyAnalytics access on or off for individual users. For more information, see [Configure access at the user level](../setup/configure-myanalytics.md#configure-access-at-the-user-level). 

#### Q2. Where is user data stored?

User metrics data is stored in users' mailboxes.

#### Q3. How long does it take for the personal dashboard to become available?

The personal dashboard is available to MyAnalytics users as soon as they receive their [welcome email](../Use/MyA-Welcome-email.md). This happens up to four weeks after licenses with the MyAnalytics service plan are assigned to the participants. For more information, see [Assign licenses with the MyAnalytics service plan](../setup/configure-myanalytics.md#assign-licenses-with-the-myanalytics-service-plan).

#### Q4. When the dashboard is activated, does it show any historical data or does it start 'from scratch'?

Upon activation, MyAnalytics processes historical data for 80 days before the date of activation. No data from before this 80-day limit is displayed in the dashboard.

#### Q5. Will MyAnalytics work for shared mailboxes?

No, currently the MyAnalytics service plan cannot be used with shared mailboxes.

#### Q6. Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

#### Q7. I have not received my Skype for Business data. It seems to have gone missing. Where is it?

Skype for Business data is usually prompt. However, in rare instances, users can experience delays of from two to four days. User actions completed on a Friday might not be included in MyAnalytics computations that are executed the following Monday. In such cases, non-working time, which includes Teams data, is updated later. Similarly, certain meetings might be marked as "Late start" after a day or two, or a digest email sent on a Monday or Tuesday, might not immediately include the data. In all such cases, the metrics are updated as soon as the data is updated.

#### Q8. Which MyAnalytics features are _not_ available to users who have the "Insights by MyAnalytics" plan?

 * The dashboard button will not appear until the dashboard becomes available to E3/E1 users, to take place later in 2019.
 * The cards that show email read statistics are not available. This capability is available to E5 users only.

   > [!Note]
   > All MyAnalytics features are available to users who have the MyAnalytics (full) plan.

#### Q8. How can I confirm that the Insights Outlook add-in is installed?

See [Confirm installation of the Insights Outlook add-in](../setup/verify-add-in.md) to confirm it's installed.

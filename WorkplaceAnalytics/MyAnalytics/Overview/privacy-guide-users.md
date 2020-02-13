---
# Metadata Sample
# required metadata

title: Privacy guide for MyAnalytics users
description: Overview of MyAnalytics privacy features, including information about de-identification of data, privacy of data, minimum group size for reporting, admin choices and default settings, and users in sensitive roles
author: paul9955
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: mya
ms.collection: M365-analytics
manager: scott.ruble
audience: user
---

# Privacy guide for MyAnalytics users

MyAnalytics helps you find opportunities to build better habits and get back in control of your time. This article describes how MyAnalytics works, what data it uses, where it stores that data, and the ways in which it was designed to keep that data safe. It also describes how MyAnalytics complies with GDPR regulations.

## Summary of key points

<ul><li> 

**MyAnalytics is not designed to enable evaluation, tracking, automated decision-making, profiling, or monitoring**.
MyAnalytics provides you with insights through a personalized dashboard, a weekly digest, the Insights Outlook add-in, and inline suggestions in Outlook. MyAnalytics has no mechanism or option that allows anyone but you to access the personalized information that is displayed through these surfaces, unless you purposefully and independently share it. Insights provided by MyAnalytics cannot be used for automated decision-making or for profiling. </li>

<li>

**MyAnalytics does not give employees access to new personally-identifiable information on other coworkers**.
MyAnalytics converts data into insights by performing calculations on information that you generate just by going about your work day. The majority of the data that you see in MyAnalytics is simply an aggregation of information to which you already have access, but that you wouldn’t be able to quickly perform calculations on without some support.</li>

<li>

**MyAnalytics data is processed and stored in the employee’s Exchange Online mailbox**.
MyAnalytics processes data from these sources: Exchange Online email and calendar data, chat and call signals from Skype for Business and from Teams, and—if both you and your organization's IT administrator opt you in—Windows 10 application activity history. MyAnalytics stores and processes this data inside each employee’s Exchange Online mailbox.</li>

<li>

**MyAnalytics supports General Data Protection Regulation (GDPR) compliance**.
Microsoft has designed MyAnalytics to support your organization’s needs to comply with  [GDPR requirements](https://www.microsoft.com/trustCenter/privacy/gdpr).</li>

</ul>

## How MyAnalytics works

MyAnalytics presents insights in the following ways:

1. [Personal dashboard](https://docs.microsoft.com/workplace-analytics/myanalytics/use/dashboard-2)

2. [Insights Outlook add-in](https://docs.microsoft.com/workplace-analytics/myanalytics/use/add-in)

3. [Weekly digest](https://docs.microsoft.com/workplace-analytics/myanalytics/use/email-digest-2)
 
4. [Inline suggestions in Outlook](https://docs.microsoft.com/workplace-analytics/myanalytics/use/mya-notifications)

MyAnalytics provides insights with the following types of data.

1. **Mailbox data:** Email, calendar, chat, and call activity that you generate by using Office 365, such as time that you spend in meetings or emails that you send to a specific person or group.

2. **Windows 10 activity history data:** Data on your usage of apps and services on your device: whether you worked on a document and whether you browsed the web.

3. **Incremental data:** Data that would otherwise be unavailable to you but is presented in an aggregated form designed to protect individual privacy.

## Mailbox data

Mailbox data represents information that you already have access to simply by going about your job, such as sending emails, arranging meetings, or chatting with coworkers. MyAnalytics processes and displays this information in ways that make it actionable.

For example, MyAnalytics provides views that allow you to quickly understand how much time you spend in meetings and in email every day, who you collaborate with the most, who you are losing touch with, and to whom you have made commitments and requests.

You can take action on this information. You might decide that you spend too much time in meetings, for example, and adopt a personal goal of running more efficient meetings.

Note that these insights are derived from data that is already available to you in the following places:

 * your Exchange Online mailbox
 * your activity in OneDrive and SharePoint documents
 * your chat and call history from Teams and from Skype for Business

MyAnalytics simply applies some basic calculations and rules to make this data more actionable. Mailbox data is stored directly in your Exchange Online mailbox.

For example, if you want to determine which colleagues sent you the most email over the past week, you could technically do so without MyAnalytics by manually counting emails from coworkers in your inbox. Similarly, you could determine your coworkers’ average response time to the emails that you sent them by using the timestamp information readily available in your mailbox. MyAnalytics saves you the trouble of having to perform these tedious calculations.


## Windows 10 Activity History data

Windows 10 activity history data refers to the things you do on your device, such as the apps and services you used, whether you worked on a document, and whether you browsed the web. The activity history is stored locally on the device, and if you are signed in to the device with a Microsoft account and you give permission, Windows sends the activity history to Microsoft.

MyAnalytics uses Windows 10 activity history data to compute insights (for example, time spent in apps, multi-tasking in meetings) about your work habits. These insights are private and stored in your Exchange Online mailbox.

Also note that, if you choose to send Windows 10 activity history to MyAnalytics,  activity data is saved even if you use a non-work or non-school account (for example, a personal live.com or facebook.com account) to connect to the app or service. However, activity data is not saved when you browse with InPrivate tabs or windows in the Microsoft Edge web browser.


## Incremental data

In a few cases, MyAnalytics provides you with de-identified information on other people that would not have otherwise been available to them, such as for Email read rates.

### Email read rates

MyAnalytics tracks the percentage of recipients who opened an email message (in the Outlook add-in) for email that you’ve sent to five or more people.

However, to preserve privacy, MyAnalytics does not track read rates for messages sent to fewer than five people. Also, MyAnalytics does not show read rates of 0% or 100%, as that would allow you to make definitive conclusions about individual coworker actions. Instead, the read rate renders as "Low" or "High."

This metric is calculated based on the "read" flag in Exchange Online. For some people, messages are flagged as "read" when you open a message in the Outlook preview pane. For others, you might need to double-click to open the message to mark it as "read."

You can control this setting in your Outlook settings. To show these signals in the sender’s mailbox, the “read” flag is copied within the Office 365 environment, and then delivered to the sender’s mailbox.

### How you can opt-in and opt-out

You can opt-in or opt-out of MyAnalytics through **Settings**. For details, see [Opt out of MyAnalytics](../use/opt-out-of-mya.md).

## GDPR Compliance

As is the case with the full Office 365 suite, MyAnalytics helps support compliance with GDPR requirements. For example, MyAnalytics supports the following:

 * **Secure and protect personal data**. Because all MyAnalytics data is stored in your Exchange Online mailbox, MyAnalytics meets this security obligation by virtue of Exchange Online also meeting the obligation.

 * **Requests to export, delete, or restrict processing personal data**. Microsoft supports user requests, such as requests for export of or deletion of data.

For more information, see [GDPR compliance](https://www.microsoft.com/trustCenter/privacy/gdpr).
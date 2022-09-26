---
title: Privacy guide 
description: Overview of privacy features for personal insights, including info about data de-identification and privacy, minimum group size for reporting, admin settings, and users in sensitive roles
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: high
ms.service: viva 
ms.subservice: viva-insights 
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: helayne
audience: user
---

# Privacy guide for personal insights

Personal insights in Microsoft Viva Insights help you find opportunities to build better habits and get back in control of your time. This article describes how Viva Insights uses personal data for personal insights, where it stores that data, and the ways in which it was designed to keep that data safe. It also describes how Viva Insights complies with GDPR regulations.

## Summary of key points

* **Personal insights in Viva Insights is not designed to enable evaluation, tracking, automated decision making, profiling, or monitoring**. Viva Insights provides you with personal insights through the Viva Insights app in Microsoft Teams and on the web, the Insights Outlook add-in, a cloud-based dashboard, Viva digest emails, Briefing emails, and inline suggestions in Outlook. Personal insights in Viva Insights has no mechanism or option that allows anyone but you to access the personalized information that is displayed through these surfaces, unless you purposefully and independently share it. Personal insights data provided by Viva Insights cannot be used for automated decision making or for profiling.
* **Personal insights in Viva Insights does not give employees access to new personally identifiable information on other coworkers**. Viva Insights converts data into personal insights by doing calculations on information that you generate just by going about your workday. Most of the data that you see in personal insights from Viva Insights is simply an aggregation of information to which you already have access, but that you wouldn’t be able to quickly perform calculations on without some support.
* **Personal insights in Viva Insights data is processed and stored in the employee’s Exchange Online mailbox**. Viva Insights processes data from these sources for personal insights: Exchange Online email and calendar data, chat and call signals from Skype for Business and from Teams, and—if both you and your organization's IT administrator opt you in—Windows 10 application activity history. Viva Insights stores and processes this data inside each employee’s Exchange Online mailbox.
* **Personal insights in Viva Insights supports General Data Protection Regulation (GDPR) compliance**. Microsoft has designed Personal insights in Viva Insights to support your organization’s needs to follow [GDPR requirements](https://www.microsoft.com/trustCenter/privacy/gdpr).

<!--## Architecture

In the following architecture illustration, note the relationship of Personal insights in Viva Insights to Exchange Online. This placement underscores the fact that any personal insights data that you can view in Viva Insights is the same data that's visible in your Exchange mailbox, as described in the following principles about data privacy.-->

## Key principles

* As a Viva Insights user, only you can see your own data.
* Your data is stored and computed in your Exchange Online mailbox.
* You can opt in and opt out at any time.
* Personal insights in Viva Insights shows you no personally identifiable info of co-workers beyond what you can already see in Outlook and Teams.

## Where to see personal insights

Personal insights in Viva Insights are available as follows:

* [Viva Insights in Teams](../teams/viva-insights-home.md)
* [Viva Insights in Outlook](../use/add-in.md)
* [Viva Insights dashboard](../Use/dashboard-2.md)
* [Briefing emails in Outlook](../Briefing/be-overview.md)
* [Digest emails in Outlook](../use/email-digests-3.md)
* [Inline suggestions in Outlook](../use/mya-notifications.md)

## Data types

Viva Insights provides personal insights with the following types of data.

* [Mailbox data](#mailbox-data) - Email, calendar, chat, and call activity that you generate by using Microsoft 365, such as time that you spend in meetings or emails that you send to a specific person or group.
* [Windows 10 activity history data](#windows-10-activity-history-data) - Data on your usage of apps and services on your device: whether you worked on a document and whether you browsed the web.
* [Incremental data](#incremental-data) - Data that would otherwise be unavailable to you but is presented in an aggregated form designed to protect individual privacy.

### Mailbox data

Mailbox data represents information that you already have access to simply by going about your job, such as sending emails, arranging meetings, or chatting with coworkers. Viva Insights processes and shows the information in ways that make it actionable.

For example, Viva Insights provides views that allow you to quickly understand how much time you spend in meetings and in email every day, who you collaborate with the most, who you are losing touch with, and to whom you have made commitments and requests.

You can take action on this information. You might decide that you spend too much time in meetings, for example, and adopt a personal goal of running more efficient meetings.

Personal insights are derived from data that is already available to you in the following places:

* Your Exchange Online mailbox
* Your activity in OneDrive and SharePoint documents
* Your chat and call history from Teams and from Skype for Business

Viva Insights simply applies some basic calculations and rules to make this data more actionable. Mailbox data is stored directly in your Exchange Online mailbox.

For example, if you want to determine which colleagues sent you the most email over the past week, you could technically do so without Viva Insights by manually counting emails from coworkers in your inbox. Similarly, you could determine your coworkers’ average response time to the emails that you sent them by using the timestamp information readily available in your mailbox. Viva Insights saves you the trouble of having to perform these tedious calculations.

### Windows 10 activity history data

Windows 10 activity history data refers to the things you do on your device, such as the apps and services you used, whether you worked on a document, and whether you browsed the web. The activity history is stored locally on the device, and if you're signed in to the device with a Microsoft account and you give permission, Windows sends the activity history to Microsoft.

Viva Insights uses Windows 10 activity history data to compute the personal insights (for example, time spent in apps, multi-tasking in meetings) about your work habits. These personal insights are private and stored in your Exchange Online mailbox.

Also note that, if you choose to send Windows 10 activity history to Viva Insights, activity data is saved even if you use a non-work or non-school account (for example, a personal live.com or facebook.com account) to connect to the app or service. However, activity data is not saved when you browse with InPrivate tabs or windows in the Microsoft Edge web browser.

### Incremental data

In a few cases, Personal insights in Viva Insights provides you with de-identified information on other people that would not have otherwise been available to them, such as for Email read rates.

#### Email read rates

Viva Insights tracks the percentage of recipients who opened an email message (in the Outlook add-in) for email that you’ve sent to five or more people.

To preserve privacy, Viva Insights does not track read rates for messages sent to fewer than five people. Viva Insights also doesn't show read rates of "0 percent" or "100 percent," as that would allow people to make definitive conclusions about individual coworker actions. Instead, the read rate in these cases is displayed as a range that encompasses a threshold value that depends on the number of recipients of the email.

This metric is calculated based on the "read" flag in Exchange Online. For some people, messages are flagged as "read" when you open a message in the Outlook preview pane. For others, you might need to double-click to open the message to mark it as "read."

You can control this setting in your Outlook settings. To show these signals in the sender’s mailbox, the “read” flag is copied within the Microsoft 365 environment, and then delivered to the sender’s mailbox.

## GDPR Compliance

As is the case with the full Microsoft 365 suite, Viva Insights helps support compliance with GDPR requirements. For example, Viva Insights supports the following:

* **Secure and protect personal data**. Because all Personal insights data in Viva Insights is stored in your Exchange Online mailbox, Viva Insights meets this security obligation by virtue of Exchange Online also meeting the obligation.
* **Requests to export, delete, or restrict processing personal data**. Microsoft supports user requests, such as requests for export of or deletion of data.

For more information, see [GDPR compliance](https://www.microsoft.com/trustCenter/privacy/gdpr).

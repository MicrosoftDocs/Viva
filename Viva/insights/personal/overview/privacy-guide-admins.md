---

ms.date: 09/16/2021
title: Personal insights in Viva Insights privacy guide for admins
description: Overview of Personal insights in Viva Insights privacy features for admins, including info about data de-identification and privacy, minimum group size for reporting, admin choices and default settings, and users in sensitive roles
author: madehmer
ms.author: helayne
ms.topic: concept-article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva-insights
ms.collection: 
- M365-analytics
- viva-insights-personal
- essentials-privacy
- essentials-compliance
- essentials-security
manager: helayne
audience: Admin
---

# Privacy guide for admins

>[!Important]
>This article discusses the Briefing email. We've paused sending Briefing emails to make some improvements. Users can still access the [Viva Insights Outlook add-in](../use/add-in.md) or [Viva Insights app in Teams](../teams/introduction.md) for key functionality until this service resumes. For more information about this change, see [Briefing pause](../reference/briefing-pause.md).

>[!Important]
>This article also discusses the Digest email. Beginning at the end of March 2024, we’ll be pausing the digest email, which is typically sent twice a month. All the content from digest emails will still be available within the [Viva Insights app in Teams or on the web.](https://support.microsoft.com/topic/viva-insights-app-in-teams-and-on-the-web-f07f80a1-177d-4541-9185-31493b74fc0f) You can continue to explore and analyze your data insights seamlessly. To learn more about this change, refer to the [Digest email pause.](/Viva/insights/personal/reference/digest-pause)

By using the data that is generated from everyday work in Microsoft 365, personal insights in Microsoft Viva Insights help people understand how they spend their limited time and who they spend it with. Then it provides intelligent tips on how to work smarter.

This guide answers key questions on how Viva Insights processes information in a manner that protects employee privacy and supports compliance with local regulations, such as [General Data Protection Regulation (GDPR)](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).

## Summary of key points

* **Personal insights in Viva Insights is not designed to enable employee evaluation, tracking, automated decision making, profiling, or monitoring**.
Viva Insights provides personal insights to individuals through an app in Teams and on the web, Briefing and Viva digest emails, Viva Insights Outlook add-in, and inline suggestions in Outlook. Viva Insights has no mechanism or option that allows anyone but the user to access the personalized information shown through these surfaces unless that person purposefully and independently shares that information. Personal insights provided by Viva Insights can't be used for automated decision making or for profiling.

* **Personal insights in Viva Insights does not give employees access to new personally identifiable information on other coworkers**.
Viva Insights converts data into personal insights by doing calculations on information that people generate just by going about their workday. Most of the personal insights data that employees see in Viva Insights is an aggregation of information to which they already have access. The advantage is that they can quickly perform calculations on the data without support.

* **Personal insights in Viva Insights data is processed and stored in the employee’s Exchange Online mailbox**.
Viva Insights processes data from these sources for personal insights: Exchange Online email and calendar data, chat, and call signals from Skype for Business and from Teams. Viva Insights stores and processes this personal insights data inside each employee’s Exchange Online mailbox.

* **Personal insights in Viva Insights supports General Data Protection Regulation (GDPR) compliance**.
Personal insights in Viva Insights is designed to support customers’ needs by following [GDPR requirements](https://www.microsoft.com/trustCenter/privacy/gdpr).

* **Personal insights in Viva Insights can be configured so that individuals must purposefully opt in**.
By default, anytime a license with the Viva Insights service is assigned to a person, that person is automatically opted in. However, admins can configure Viva Insights to be "default off," so that people can choose for themselves whether to opt in after being assigned a license.

* **Personal insights in Viva Insights reminds people that their data is private and secure**.
A few days after a license with the Viva Insights service is assigned to a person, that person receives a welcome email that clearly lays out how Viva Insights works with a reminder that all of their data is private. The other Viva Insights surfaces, such as digest emails and Briefing emails, and Viva Insights app in Teams and on the web, reinforce this message.


## How Personal insights in Viva Insights works

Personal insights in Viva Insights are shown in the following ways:

* [Viva Insights in Teams and on the web](../teams/home.md)
* [Briefing emails](../Briefing/be-overview.md)
* [Viva Insights in Outlook](../use/add-in.md)
* [Digest emails in Outlook](../use/email-digests-3.md)
* [Inline suggestions in Outlook](../use/mya-notifications.md)

Personal insights in Viva Insights uses the following types of data.

* **Mailbox data** - Email, calendar, chat, and call activity that people generate by using Microsoft 365, such as time spent in meetings or emails sent to a specific person or group.
* **Incremental data** - Data that would otherwise be unavailable to the employee but is presented in an aggregated form designed to protect individual privacy.

## Mailbox data

Mailbox data represents information that people can already access by going about their job, such as sending emails, arranging meetings, or chatting with coworkers. Viva Insights processes and shows this information in new ways that make it actionable.

For example, Viva Insights provides views that allow people to understand how much time they spend in meetings and in email each day, who they collaborate with the most, who they're losing touch with, and who they've have made commitments and requests to.

People can take action on this information. They might decide that they spend too much time in meetings, for example, and adopt a personal goal of running more efficient meetings.

These insights are derived from data that is *already available* to people in the following places:

* Their Exchange Online mailbox
* Their activity in OneDrive and SharePoint documents
* Their chat and call history from Teams and from Skype for Business

Viva Insights simply applies some basic calculations and rules to make the personal insights more actionable. Mailbox data is stored directly in each employee's Exchange Online mailbox.

For example, if people want to determine which colleagues sent them the most email over the past week, they could technically do so without Viva Insights by manually counting emails from coworkers in their inbox. Similarly, people could determine their coworkers’ average response time to the emails that they send by using timestamp information readily available in their mailbox. Viva Insights saves people the trouble of having to perform these tedious calculations.

## Incremental data

In a few cases, Personal insights in Viva Insights provides people with *de-identified* information on other people that wouldn't otherwise be available to them, such as for email read rates.

### Email read rates and document open rates

Personal insights in Viva Insights tracks the percentage of recipients who opened an email message (in the Outlook add-in) for email that a person sends to five or more people.

To preserve privacy, Viva Insights doesn't track read rates for messages sent to fewer than five people. Viva Insights also doesn't show read rates of "0 percent" or "100 percent," as that would allow people to make definitive conclusions about individual coworker actions. Instead, the read rate in these cases is displayed as a range that encompasses a threshold value that depends on the number of recipients of the email.

This metric is calculated based on a person's Outlook setting for when an [email is marked as read](https://support.office.com/article/mark-a-message-as-read-or-unread-59b44298-08c2-4eb7-8128-ea0fb7f52720). When Outlook marks an email as "read," that information is saved within the person’s mailbox, then delivered to the sender's mailbox if that person has opted in to using Viva Insights.

In an email that is sent to five or more people, Viva Insights tracks the percentage of recipients who opened a document that was shared as a link or as an attachment in the email. This metric calculation is based on whether recipients have opened shared documents that are stored in SharePoint or in OneDrive for Business.

## Privacy settings

Personal insights in Viva Insights provides flexible and configurable controls that are designed to enable organizations and their members to address varying legal and policy needs regarding privacy and use of employee data. When enabling Personal insights in Viva Insights for the organization, admins can make the following choices:

* **Determine which people have access to Viva Insights** &ndash; Admins can determine which people can access and use Viva Insights by issuing licenses to only those people who should have access.

* **Determine default opt-in settings** &ndash; Admins can configure Personal insights in Viva Insights to be "default off," which means that licensed employees must individually opt in to Viva Insights to gain access to their Viva Insights app and Outlook add-in and to contribute to incremental data. Alternatively, Viva Insights can be configured to be "default on," which means that licensed employees automatically contribute to incremental data and have access to their app and to the Outlook add-in, but can later opt out through the **Settings** menu. To learn more, see [Configure access at the user level](../../advanced/setup-maint/configure-personal-insights.md#configure-access-at-the-user-level).

If default settings are used, the following applies:

* All employees in your organization contribute to [incremental data](../Overview/privacy-guide-users.md#incremental-data) whether or not they have been issued licenses with the Viva Insights service.
* Personal insights in Viva Insights is automatically enabled for employees after a license is assigned to them. If, instead, you want licensed employees to have the choice to opt in, you must change the default settings.

## Opt in or out

Employees can opt themselves out of Viva Insights. Opting out causes them to lose access to the Viva Insights [elements](../use/mya-elements.md) and it also has [data-processing consequences](#data-processing-consequences). Admins can also [opt out employees](../../advanced/setup-maint/configure-personal-insights.md#configure-access-at-the-user-level), but employees can override the admin setting and opt back in, as described in [How employees can opt in or out](#how-employees-opt-in-or-out).

### Data processing consequences

The processing of an employee's personal data ceases when they're opted out, whether they opt themselves out or an admin opts them out.

### How employees opt in or out

End users can opt in or out of Viva Insights via the **Settings > Privacy** menu in the Viva Insights app in Teams or on the web, as shown in this example:

![Opt out](../teams/images/opt-out.png)

## Microsoft Graph

Personal insights in Microsoft Viva Insights is a first-party application that's built on Microsoft Graph. Microsoft Graph consists of a set of REST-based API calls that allow developers to interact with the Microsoft technologies that a given organization uses. In order to use these API calls, developers must have specific permissions to access any data they request. Administrators control both the deployment of any Microsoft Graph application and permissions to access these applications.

The Microsoft Graph can't be turned on or off globally through the Microsoft 365 Admin Center, but administrators can achieve this effect by blocking employees’ ability to install third-party apps or by restricting developer access permissions. Learn more about [Microsoft Graph](https://developer.microsoft.com/graph).

## Employee experience with Viva Insights

### App and Outlook add-in

Within a few days of the assignment of a license with the Viva Insights service to an employee&mdash;either as part of an overall Microsoft 365 Enterprise license or as an add-in license&mdash;the user’s Viva Insights [app in Teams and on the web](../teams/introduction.md) and [Outlook Add-in](../use/add-in.md) become available.

### Welcome email

To notify employees that their app and Outlook add-in have been enabled, Viva Insights delivers a welcome email within a few days of license assignment. The email introduces people to the application and has a reminder that Viva Insights is private and personal.

### Digest emails

A few days after the welcome email is delivered, users begin to receive the [Digest emails](../use/email-digests-3.md).

## GDPR Compliance

As is the case with the full Microsoft 365 suite, Personal insights in Viva Insights helps support compliance with GDPR requirements. Microsoft helps data controllers meet the following obligations for Viva Insights:

1. **Secure and protect personal data of users**.
    All Personal insights in Viva Insights data is stored in the employees’ Exchange Online mailbox. Viva Insights appends computed metrics such as “Meeting hours” to the mailbox. Thus, Viva Insights meets this obligation by virtue of Exchange Online also meeting the obligation:

    * Microsoft will not mine customer data in Exchange Online for advertising.
    * Microsoft will not voluntarily disclose Exchange Online customer data to law enforcement agencies.
    * Microsoft meets all requirements related to encryption of Exchange Online data and implements controls to reduce security risks to help ensure business continuity, as described in ISO 27001 and 27018.

2. **Notify users in the event that a breach is detected**.
   Microsoft notifies customer privacy contacts within 72 hours of Microsoft becoming aware of a breach by using [Microsoft 365 incident response](/office365/securitycompliance/office365-security-incident-response-overview) standard operating procedures.

3. **Honor user requests (DSRs) to export, delete, or restrict processing personal data**.
    Microsoft supports your need to honor user requests in the following ways.

    * **Data export request**: Users can go to the Viva Insights app while signed in to their Microsoft 365 account to view the insights that are generated about how they spend their time at work. They can take screenshots of Viva Insights insights if they want to have permanent copies of their information.
    * **Request to restrict processing**:

      * Use PowerShell to opt employees out of Viva Insights.

         >[!Note]
         >The processing of an employee's personal data ceases when they are opted out, whether an admin opts them out (see [Configure access at the user level](../../advanced/setup-maint/configure-personal-insights.md#configure-access-at-the-user-level)) or they opt themselves out (see [How employees opt in or out](#how-employees-opt-in-or-out)).

      * Delete employee data by signing in to [Microsoft Entra admin center](https://aad.portal.azure.com) and removing the employee through the User Management Portal, which will remove all of the employee's data within 30 days. However, if you want to permanently delete the user immediately, follow the steps in [Permanently delete a user](/azure/active-directory/fundamentals/active-directory-users-restore#permanently-delete-a-user).

To learn more, see [GDPR compliance](https://www.microsoft.com/trustCenter/privacy/gdpr).

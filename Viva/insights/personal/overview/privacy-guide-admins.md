---

title: Personal insights in Viva Insights privacy guide for admins
description: Overview of Personal insights in Viva Insights privacy features for admins, including info about data de-identification and privacy, minimum group size for reporting, admin choices and default settings, and users in sensitive roles
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights 
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: helayne
audience: Admin
---

# Privacy guide for admins

By using data generated from everyday work in Microsoft 365, personal insights in Microsoft Viva Insights help people understand how they spend their limited time and who they spend it with, and then presents intelligent tips on how to work smarter.

This guide answers key questions on how Viva Insights processes information in a manner that protects employee privacy and supports compliance with local regulations, such as [General Data Protection Regulation (GDPR)](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).

## Summary of key points

* **Personal insights in Viva Insights is not designed to enable employee evaluation, tracking, automated decision making, profiling, or monitoring**.
Viva Insights provides personal insights to individuals through a personalized dashboard, Briefing and Viva digest emails, Viva Insights Outlook add-in, and inline suggestions in Outlook. Viva Insights has no mechanism or option that allows anyone but the user to access the personalized information that is shown through these surfaces, unless that person purposefully and independently shares that information. Personal insights provided by Viva Insights cannot be used for automated decision making or for profiling.

* **Personal insights in Viva Insights does not give employees access to new personally identifiable information on other coworkers**.
Viva Insights converts data into personal insights by doing calculations on information that people generate just by going about their workday. Most of the personal insights data that employees see in Viva Insights is simply an aggregation of information to which they already have access, but that they wouldn’t be able to quickly perform calculations on without some support.

* **Personal insights in Viva Insights data is processed and stored in the employee’s Exchange Online mailbox**.
Viva Insights processes data from these sources for personal insights: Exchange Online email and calendar data, chat, and call signals from Skype for Business and from Teams, and&mdash;if both the organization's IT administrator and an individual opt in&mdash;Windows 10 application activity history. Viva Insights stores and processes this personal insights data inside each employee’s Exchange Online mailbox.

* **Personal insights in Viva Insights supports General Data Protection Regulation (GDPR) compliance**.
Microsoft has designed Personal insights in Viva Insights to support customers’ needs by following [GDPR requirements](https://www.microsoft.com/trustCenter/privacy/gdpr).

* **Personal insights in Viva Insights can be configured so that individuals must purposefully opt in**.
By default, any time a license with the Viva Insights service is assigned to a person, that person is automatically opted in. However, admins can configure Viva Insights to be "default off," so that people can choose for themselves whether to opt in after being assigned a license.

* **Personal insights in Viva Insights reminds people that their data is private and secure**.
A few days after a license with the Viva Insights service is assigned to a person, that person receives a welcome email that clearly lays out how Viva Insights works, with a reminder that all of their data is private. The other Viva Insights surfaces, such as digest emails and Briefing emails, and the personal dashboard, reinforce this message.

## How Personal insights in Viva Insights works

Personal insights in Viva Insights are shown in the following ways:

* [Viva Insights in Teams](../teams/viva-insights-home.md)
* [Personal dashboard](../use/dashboard-2.md)
* [Briefing emails](../Briefing/be-overview.md)
* [Viva Insights in Outlook](../use/add-in.md)
* [Digest emails in Outlook](../use/email-digests-3.md)
* [Inline suggestions in Outlook](../use/mya-notifications.md)

Personal insights in Viva Insights uses the following types of data.

* **Mailbox data** - Email, calendar, chat, and call activity that people generate by using Microsoft 365, such as time spent in meetings or emails sent to a specific person or group.
* **Windows 10 activity history data** - Data on people's usage of apps and services on their device: whether they worked on a document and whether they browsed the web.
* **Incremental data** - Data that would otherwise be unavailable to the employee but is presented in an aggregated form designed to protect individual privacy.

## Mailbox data

Mailbox data represents information that people already have access to simply by going about their job, such as sending emails, arranging meetings, or chatting with coworkers. Viva Insights processes and shows this information in new ways that make it actionable.

For example, Viva Insights provides views that allow people to quickly understand how much time they spend in meetings, and in email every day, who they collaborate with the most, who they are losing touch with, and to whom they have made commitments and requests.

People can take action on this information. They might decide that they spend too much time in meetings, for example, and adopt a personal goal of running more efficient meetings.

These insights are derived from data that is *already available* to people in the following places:

* Their Exchange Online mailbox
* Their activity in OneDrive and SharePoint documents
* Their chat and call history from Teams and from Skype for Business

Viva Insights simply applies some basic calculations and rules to make the personal insights more actionable. Mailbox data is stored directly in each employee's Exchange Online mailbox.

For example, if people want to determine which colleagues sent them the most email over the past week, they could technically do so without Viva Insights by manually counting emails from coworkers in their inbox. Similarly, people could determine their coworkers’ average response time to the emails that they send by using timestamp information readily available in their mailbox. Viva Insights saves people the trouble of having to perform these tedious calculations.

## Windows 10 activity history data

Windows 10 activity history data refers to the things people do on their device, such as the apps and services they used, whether they worked on a document, and whether they browsed the web. The activity history is stored locally on the device, and if the employee is signed in to the device with a Microsoft account and gives permission, Windows sends the activity history to Microsoft.

Viva Insights uses Windows 10 activity history data to compute personal insights (for example, time spent in apps, multi-tasking in meetings) about the person's work habits. These insights are private and stored in the person's Exchange Online mailbox.

Also note that, if the person chooses to send Windows 10 activity history to Viva Insights, activity data is saved even if they use a non-work or non-school account (for example, a personal live.com or facebook.com account) to connect to the app or service. However, activity data is not saved when they browse with InPrivate tabs or windows in the Microsoft Edge web browser.

## Incremental data

In a few cases, Personal insights in Viva Insights provides people with *de-identified* information on other people that would not have otherwise been available to them, such as for email read rates.

### Email read rates and document open rates

Personal insights in Viva Insights tracks the percentage of recipients who opened an email message (in the Outlook add-in) for email that a person sends to five or more people.

To preserve privacy, Viva Insights does not track read rates for messages sent to fewer than five people. Viva Insights also doesn't show read rates of "0 percent" or "100 percent," as that would allow people to make definitive conclusions about individual coworker actions. Instead, the read rate in these cases is displayed as a range that encompasses a threshold value that depends on the number of recipients of the email.

This metric is calculated based on a person's Outlook setting for when an [email is marked as read](https://support.office.com/article/mark-a-message-as-read-or-unread-59b44298-08c2-4eb7-8128-ea0fb7f52720). When Outlook marks an email as "read," that information is saved within the person’s mailbox. This is then delivered to the sender's mailbox if that person has opted in to using Viva Insights.

Similarly, Viva Insights tracks the percentage of recipients who opened a document that was shared as a link or as an attachment in an email that a person sends to five or more people. This metric calculation is based on whether recipients have opened shared documents that are stored in SharePoint or in OneDrive for Business.

## Assistance for people managers

People managers often have hectic schedules and it can be tough to stay in close contact with each team member. Viva Insights brings together all the information managers need to stay caught up and respond quickly to important requests.

<!--For example, the [Catch up with your team](../use/use-the-insights.md#catch-up-with-your-team) feature in the [Insights add-in](../use/add-in.md) helps managers schedule regular 1:1 time, respond quickly to unread emails, close out important tasks, and more.
-->
All assistance for managers in Viva Insights relies exclusively on information from the manager's own mailbox; managers do not receive any incremental information from team members' mailboxes that could be used for performance management. For example: managers can use this feature to review important unread emails in their inbox _from_ team members, but they cannot see whether team members have read emails that the manager has sent.

Managers are identified by using Azure Active Directory<!-- REMOVING (12/4/2020) FOR NOW. REINSTATE PERHAPS IN JANUARY 2021.  or Workplace Analytics-->. The feature is only available to users who have direct reports listed in Azure AD.<!-- REMOVING (12/4/2020) FOR NOW. REINSTATE PERHAPS IN JANUARY 2021.  or in Workplace Analytics. (The Workplace Analytics organizational hierarchy is used for a tenant only if **Insights and plans** is turned on in the [Manager settings](../../use/settings.md#manager-settings) of Workplace Analytics.)-->

Managers have the option to [edit their team list](../use/use-the-insights.md#to-edit-your-team-list) if they notice any inaccuracies. Any changes the manager makes are used only in their Viva Insights experience, and are not synchronized back to Azure AD.

## Privacy settings

Personal insights in Viva Insights provides flexible and configurable controls that are designed to enable organizations and their members to address varying legal and policy needs regarding privacy and use of employee data. When enabling Personal insights in Viva Insights for the organization, admins can make the following choices:

* **Determine which people have access to Viva Insights** &ndash; Admins can determine which people can access and use Viva Insights by issuing licenses to only those people who should have access.

* **Determine default opt-in settings** &ndash; Admins can configure Personal insights in Viva Insights to be "default off," which means that licensed employees must individually opt in to Viva Insights to gain access to their dashboard and Outlook add-in and to contribute to incremental data. Alternatively, Viva Insights can be configured to be "default on," which means that licensed employees automatically contribute to incremental data and have access to their dashboard and to the Outlook add-in, but can subsequently opt out through the **Settings** menu. To learn more, see [Configure access at the user level](../setup/configure.md#configure-access-at-the-user-level).

* **Determine whether employees can opt-in to receive insights on Windows 10 application usage** &ndash; Admins must consent before Viva Insights users can opt in to receive personal insights derived from Windows 10 activity history data.

<!-- DELETE PER MATHEW 1 JUNE 2021: 
* **Determine which employees in sensitive roles should be excluded from incremental data** &ndash; Some organizations may have employees in sensitive roles who should never contribute to incremental data. To support this, Viva Insights provides admins with the ability to mark these people as “excluded.” Excluded users cannot opt in to contribute to incremental data. However, the Viva Insights experience will still be available to these users provided that they are licensed. -->

Note that if default settings are used, the following applies:

* All employees in your organization contribute to [incremental data](../Overview/privacy-guide-users.md#incremental-data) whether or not they have been issued licenses with the Viva Insights service.
* Personal insights in Viva Insights is automatically enabled for employees after a license is assigned to them. If, instead, you want licensed employees to have the choice to opt in, you must change the default settings.

## Opt in or out

Employees can opt themselves out of Viva Insights. This causes them to lose access to the Viva Insights [elements](../use/mya-elements.md) and it also has [data-processing consequences](#data-processing-consequences). Admins can also [opt out employees](../setup/configure.md#configure-access-at-the-user-level), but employees can override the admin setting and opt back in, as described in [How employees can opt in or out](#how-employees-opt-in-or-out).

### Data processing consequences

The processing of an employee's personal data ceases when they are opted out, whether they opt themselves out or an admin opts them out.

### How employees opt in or out

>[!IMPORTANT]
> The dashboard will be retired soon, but users can [opt out through their Viva Insights app in Teams or on the web](../use/home-web.md#opt-in-or-out-of-features), on the **Settings** page. [Read more about this change](../reference/mya-retirement.md). 

End users can opt in or out of Viva Insights via the **Feature settings** menu in Microsoft 365, as shown in this example:

:::image type="content" source="../../images/mya/use/dashboard-settings.png" alt-text="Screenshot that shows opening the Settings window" lightbox="../../images/mya/use/dashboard-settings-expanded.png":::

## Microsoft Graph

Personal insights in Microsoft Viva Insights is a first-party application that's built on Microsoft Graph. Microsoft Graph consists of a set of REST-based API calls that allow developers to interact with the Microsoft technologies that a given organization uses. In order to use these API calls, developers must have specific permissions to access any data they request. Administrators control both the deployment of any Microsoft Graph application and permissions to access these applications.

The Microsoft Graph cannot be turned on or off globally through the Microsoft 365 Admin Center, but administrators can achieve this effect by blocking employees’ ability to install third-party apps or by restricting developer access permissions. Learn more about [Microsoft Graph](https://developer.microsoft.com/graph).

## Employee experience with Viva Insights

### Dashboard and Outlook add-in

Within a few days of the assignment of a license with the Viva Insights service to an employee&mdash;either as part of an overall Microsoft 365 Enterprise license or as an add-in license&mdash;the user’s Viva Insights [dashboard](../use/dashboard-2.md) and [Outlook Add-in](../use/add-in.md) become available.

### Welcome email

To notify employees that their dashboard and Outlook add-in have been enabled, Viva Insights delivers a welcome email within a few days of license assignment. The email introduces people to the application and has a reminder that Viva Insights is private and personal.

### Digest emails

A few days after the welcome email is delivered, users begin to receive the [Digest emails](../use/email-digests-3.md).

## GDPR Compliance

As is the case with the full Microsoft 365 suite, Personal insights in Viva Insights helps support compliance with GDPR requirements. Microsoft helps data controllers meet the following obligations for Viva Insights:

1. **Secure and protect personal data of users**.
    All Personal insights in Viva Insights data is stored in the employees’ Exchange Online mailbox. Viva Insights appends computed metrics such as “Meeting hours” to the mailbox. Thus, Viva Insights meets this obligation by virtue of Exchange Online also meeting the obligation:

    * Microsoft will not mine customer data in Exchange Online for advertising.
    * Microsoft will not voluntarily disclose Exchange Online customer data to law enforcement agencies.
    * Microsoft will meet all requirements related to encryption of Exchange Online data and implement controls to reduce security risks and help ensure business continuity, as described in ISO 27001 and 27018.

2. **Notify users in the event that a breach is detected**.
   Microsoft will notify customer privacy contacts within 72 hours of Microsoft becoming aware of a breach by using [Microsoft 365 incident response](/office365/securitycompliance/office365-security-incident-response-overview) standard operating procedures.

3. **Honor user requests (DSRs) to export, delete, or restrict processing personal data**.
    Microsoft supports your need to honor user requests in the following ways.

    * **Data export request**: Users can go to the Viva Insights dashboard while signed in to their Microsoft 365 account to view the insights that are generated about how they spend their time at work. They can take screenshots of Viva Insights insights if they want to have permanent copies of their information.
    * **Request to restrict processing**:

      * Use PowerShell to opt employees out of Viva Insights.

         >[!Note]
         >The processing of an employee's personal data ceases when they are opted out, whether an admin opts them out (see [Configure access at the user level](../setup/configure.md#configure-access-at-the-user-level)) or they opt themselves out (see [How employees opt in or out](#how-employees-opt-in-or-out)).

      * Delete employee data by signing in to [Azure Active Directory admin center](https://aad.portal.azure.com) and removing the employee through the User Management Portal, which will remove all of the employee's data within 30 days. However, if you want to permanently delete the user immediately, follow the steps in [Permanently delete a user](/azure/active-directory/fundamentals/active-directory-users-restore#permanently-delete-a-user).

To learn more, see [GDPR compliance](https://www.microsoft.com/trustCenter/privacy/gdpr).

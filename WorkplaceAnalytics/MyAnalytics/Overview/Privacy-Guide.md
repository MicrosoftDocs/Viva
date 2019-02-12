---
# Metadata Sample
# required metadata

title: Privacy guide for Microsoft MyAnalytics
description: Overview of MyAnalytics privacy features, including information about de-identification of data, privacy of data, minimum group size for reporting, admin choices and default settings, and users in sensitive roles.
author: madehmer
ms.author: madehmer
ms.date: 1/31/2019
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

# MyAnalytics privacy guide

MyAnalytics is best thought of as a “fitness tracker for the workplace.” By using data generated from everyday work in Office 365, MyAnalytics helps people understand how they spend their limited time and who they spend it with, and then presents intelligent tips on how to work smarter.

This page answers key questions on how MyAnalytics processes information in a manner that protects employee privacy and supports compliance with local regulations, such as [General Data Protection Regulation (GDPR)](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).

## Summary of key points

<ul><li>

**MyAnalytics is not designed to enable employee evaluation, tracking, or monitoring**.
MyAnalytics provides insights to individuals through a personalized dashboard, a weekly email digest, an Outlook Add-in, and nudges in Outlook. MyAnalytics has no mechanism or option that allows anyone but the user to access the personalized information that is displayed through these surfaces, unless that person purposefully and independently shares that information.</li>

<li>

**MyAnalytics does not give employees access to new personally-identifiable information on other coworkers**.
MyAnalytics converts data into insights by performing calculations on information that people generate just by going about their work day. The majority of the data that employees see in MyAnalytics is simply an aggregation of information to which they already have access, but that they wouldn’t be able to quickly perform calculations on without some support.</li>

<li>

**MyAnalytics data is processed and stored in the employee’s Exchange Online mailbox**.
MyAnalytics processes data from these sources: Exchange Online email and calendar data, and chat and call signals from Skype for Business and from Teams. MyAnalytics stores and processes this data inside each employee’s Exchange Online mailbox.</li>

<li>

**MyAnalytics supports General Data Protection Regulation (GDPR) compliance**.
Microsoft has designed MyAnalytics to support customers’ needs to comply with [GDPR requirements](https://www.microsoft.com/trustCenter/privacy/gdpr).</li>

<li>

**MyAnalytics can be configured so that individuals must purposefully opt in**.
By default, any time a MyAnalytics license is assigned to a person, that person is automatically opted in. However, administrators can configure MyAnalytics to be "default off," so that people can choose for themselves whether to opt in after the license has been assigned to them.</li>

<li>

**MyAnalytics and Delve are separate applications with no interdependencies**.
MyAnalytics and Delve are both first-party Microsoft Graph applications and have no overlap. These applications can be managed and licensed separately, without settings from one impacting the settings of the other.</li>

<li>

**MyAnalytics reminds people that their data is private and secure**.
Three days after a MyAnalytics license is assigned to a person, that person receives a welcome email that clearly lays out how MyAnalytics works, with a reminder that all of their data is private. The other MyAnalytics user interfaces, such as the weekly email digest and personal dashboard, reinforce this message.</li>
</ul>

## How MyAnalytics works

MyAnalytics presents insights through four different surfaces:

1. [Personal dashboard](https://docs.microsoft.com/workplace-analytics/myanalytics/use/dashboard)

2. [Outlook Add-in](https://docs.microsoft.com/workplace-analytics/myanalytics/use/add-in)

3. [Weekly email digest](https://docs.microsoft.com/workplace-analytics/myanalytics/use/email-digest)
 
4.	[Nudges in Outlook](https://docs.microsoft.com/workplace-analytics/myanalytics/use/mya-notifications)

MyAnalytics provides insights with the following types of data.

1. **Mailbox data**: Email, calendar, chat, and call activity that people generate by using Office 365, such as time spent in meetings or emails sent to a specific person or group.

2. **Incremental data**: Data that would otherwise be unavailable to the employee but is presented in an aggregated form designed to protect individual privacy.

## Mailbox data

Mailbox data represents information that people already have access to simply by going about their job, such as sending emails, arranging meetings, or chatting with coworkers. MyAnalytics processes and displays this information in new ways that make it actionable.

For example, MyAnalytics provides views that allow people to quickly understand how much time they spend in meetings, and in email every day, who they collaborate with the most, who they are losing touch with, and to whom they have made commitments and requests.

People can take action on this information —they might decide that they spend too much time in meetings, for example, and adopt a personal goal of running more efficient meetings.

These insights are derived from data that is *already available* to people in their Exchange Online mailbox and in their chat or call history from Teams and from Skype for Business. MyAnalytics simply applies some basic calculations and rules to make that data more actionable. Mailbox data is stored directly in each employee's Exchange Online mailbox.

For example, if people want to determine which colleagues sent them the most email over the past week, they could technically do so without MyAnalytics by manually counting emails from coworkers in their inbox. Similarly, people could determine their coworkers’ average response time to the emails that they send by using timestamp information readily available in their mailbox. MyAnalytics saves people the trouble of having to perform these tedious calculations.

## Incremental data

In a few cases, MyAnalytics provides people with *de-identified* information on other people that would not have otherwise been available to them, such as for Email read rates.

### Email read rates

MyAnalytics tracks the percentage of recipients who opened an email message (in the Outlook Add-in) for email that a person sends to five or more people.

However, to preserve privacy, MyAnalytics does not track read rates for messages sent to fewer than five people. Also, MyAnalytics does not show read rates of 0% or 100%, as that would allow people to make definitive conclusions about individual coworker actions. Instead, the read rate renders as “Low” or “High.”

![Email read rates](../../Images/mya/use/email-read-rates-2.png)

This metric is calculated based on the “read” flag in Exchange Online. For some people, messages are flagged as “read” when they open a message in the Outlook preview pane. For others, they might need to double-click to open the message to mark it as "read."

People can control this setting in their Outlook settings. To show these signals in the sender’s mailbox, the “read” flag is copied within the Office 365 environment, and then delivered to the sender’s mailbox.

## Privacy settings
MyAnalytics provides flexible and configurable controls that are designed to enable organizations and their members to address varying legal and policy needs regarding privacy and use of employee data. When enabling MyAnalytics for the organization, admins can make the following choices:

* **Determine which people have access to MyAnalytics**
  Admins can determine which people can access and use MyAnalytics by issuing licenses to only those people who should have access.

* **Determine default opt-in settings**
   Admins can configure MyAnalytics to be "default off," which means that licensed employees must individually opt in to MyAnalytics to gain access to their dashboard and Outlook add-in and to contribute to incremental data. Alternatively, MyAnalytics can be configured to be "default on," which means that licensed employees automatically contribute to incremental data and have access to their dashboard and to the Outlook add-in, but can subsequently opt out through the Settings menu. To learn more, see [Configure user settings](https://docs.microsoft.com/workplace-analytics/myanalytics/setup/mya-setup-checklist#step-1-configure-user-settings).

* **Determine which employees in sensitive roles should be excluded from incremental data**
  Some organizations may have employees in sensitive roles who should never contribute to incremental data. To support this, MyAnalytics provides admins with the ability to mark these people as “excluded.” Excluded users cannot opt in to contribute to incremental data. However, the MyAnalytics experience will still be available to such users provided that they are licensed.

 Note that if default settings are used, the following applies:

1. All employees in your organization contribute to [incremental data](../Overview/privacy-guide.md#incremental-data) whether or not they have been issued MyAnalytics licenses. 
2. MyAnalytics is automatically enabled for employees after a license is assigned to them. If, instead, you want licensed employees to have the choice to opt in, you must change the default settings.

### How employees can opt-in and opt-out

 End users can opt-in or opt-out of MyAnalytics via the Feature Settings menu in Office 365, as shown here:

![Email read rates](../../Images/mya/use/mya-opt-in-out-3.png)


## MyAnalytics vs. Workplace Analytics, Delve, and the Microsoft Graph

The following describes the differences between these Microsoft products:

### MyAnalytics vs. Workplace Analytics

Although MyAnalytics is an individual productivity tool, [Workplace Analytics](https://docs.microsoft.com/en-us/workplace-analytics/) enables organizations to view aggregated, de-identified collaboration data of employees. The applications are purchased and licensed separately. If an employee opts out of MyAnalytics, this does not impact the opt-in status for Workplace Analytics (and vice versa).

### MyAnalytics vs. Delve

MyAnalytics and Delve are both first-party applications based on the Microsoft Graph, and are independent applications with different use cases. Delve uses intelligence to help employees discover relevant content and people across their organization. Each application is licensed separately and settings from one do not impact the settings of the other.

There may be some confusion about this, because MyAnalytics used to be called “Delve Analytics” but was rebranded in fall 2016. The MyAnalytics personal dashboard still shows up in the Delve user interface. However, MyAnalytics will eventually be decoupled from Delve and have its own unique URL.

> [!Note] 
> Administrators and individuals can disable Delve content-discovery functionality without impacting access to MyAnalytics, and vice-versa. The personal dashboard and all other MyAnalytics surfaces will remain functional. To learn more, see [Delve administration](https://docs.microsoft.com/sharepoint/delve-for-office-365-admins).

### Microsoft Graph

MyAnalytics and Delve are first-party applications built on the Microsoft Graph. The Microsoft Graph consists of a set of REST-based API calls that allow developers to interact with the Microsoft technologies that a given organization uses. In order to use these API calls, developers must have specific permissions to access any data they request. Administrators control both the deployment of any Microsoft Graph application and permissions to access these applications.

The Microsoft Graph cannot be turned on or off globally through the Office 365 Admin Center, but administrators can achieve this effect by blocking employees’ ability to install third-party apps or by restricting developer access permissions. Learn more about [Microsoft Graph](https://developer.microsoft.com/graph).

## Employee experience of MyAnalytics

### Dashboard and Outlook Add-in

Within one to three days of the assignment of a MyAnalytics license to an employee —either as part of an overall E5 license or as an add-on license —the user’s MyAnalytics [personal dashboard](https://docs.microsoft.com/workplace-analytics/myanalytics/use/dashboard) and [Outlook Add-in](https://docs.microsoft.com/workplace-analytics/myanalytics/use/add-in) become available.

### Welcome email

To notify employees that their dashboard and Outlook Add-in have been enabled, MyAnalytics delivers a 
[Welcome email](https://docs.microsoft.com/workplace-analytics/myanalytics/setup/mya-welcome-email) within three days of license assignment. The email introduces people to the application and contains a reminder that MyAnalytics is private and personal.

### Weekly digest email

The week after the welcome email is delivered, users  begin to receive the [weekly digest email](https://docs.microsoft.com/workplace-analytics/myanalytics/use/email-digest).

## GDPR Compliance

As is the case with the full Office 365 suite, MyAnalytics helps support compliance with GDPR requirements. Microsoft helps data controllers meet the following obligations for MyAnalytics: 

1. **Secure and protect personal data of data subjects**.

    All MyAnalytics data is stored in the employees’ Exchange Online mailbox. MyAnalytics appends computed metrics such as “Meeting hours” to the mailbox. Thus, MyAnalytics meets this obligation by virtue of Exchange Online also meeting the obligation:
    * Microsoft will not mine customer data in Exchange Online for advertising. 
    * Microsoft will not voluntarily disclose Exchange Online customer data to law enforcement agencies.
    * Microsoft will meet all requirements related to encryption of Exchange Online data and implement controls to reduce security risks and help ensure business continuity, as described in ISO 27001 and 27018.

2. **Notify data subjects in the event that a breach is detected**.
   Microsoft will notify customer privacy contacts within 72 hours of Microsoft becoming aware of a breach by using [Office 365 incident response](https://docs.microsoft.com/office365/securitycompliance/office365-security-incident-response-overview) standard operating procedures.

3. **Honor data subject requests (DSRs) to export, delete, or restrict processing personal data**.
    Microsoft supports your need to honor data subject requests in the following ways:
    * Data export requests: submit data export requests via the Microsoft [Service Trust Portal](https://servicetrust.microsoft.com/ViewPage/GDPRDSR). Separately, people can also take screenshots of their MyAnalytics dashboards.
    * Request to restrict processing:
      * Use PowerShell to opt employees out of MyAnalytics 
      * Delete employee data: sign in to [Azure Active Directory admin center](https://aad.portal.azure.com) and then remove the employee's data through the User Management Portal.

To learn more, see [GDPR compliance](https://www.microsoft.com/trustCenter/privacy/gdpr).
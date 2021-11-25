---

title: Privacy and data access
description: About the privacy and data access controls available in Microsoft Viva Insights 
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
ms.localizationpriority: medium
search.appverid:
- MET150 
ms.prod: wpa
ms.collection: M365-analytics, m365initiative-viva-insights
manager: scott.ruble
audience: Admin
---

# Privacy and data access

Being aware of employees' rights is a key component to ensuring a successful program using Microsoft Viva Insights. It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using the Viva Insights web features.

Viva Insights does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in the app.

>[!Important]
>Consult with your legal and human resources teams before enabling Microsoft Viva Insights for your organization.

## You decide who gets to see what data

Organizations decide who has access to what Viva Insights data. You should ensure that primary users receive suitable training in privacy, and in your company’s policies and other applicable subject areas, before being granted access to the data.

The following levels of permission provide access to the Viva Insights data:

* **Analyst (Limited Access)** has access to the Organizational insights in Microsoft Teams and Viva Insights with analysis features where the minimum group size is enforced.
* **Analyst** has full access to all product features except the administrator features.
* **Administrator role** has access to administrator features only (such as some of the **Analyst settings** and **Data Source** in Viva Insights).
* **Program manager** has access to Viva Insights in Teams and in Viva Insights, where program managers can also explore metrics in cases where the minimum group size is enforced. They also have access to **Plans** in Viva Insights and its **Manage** and **Track** pages, where they can set up plans and track the progress of active or ended plans.
* **People managers** who meet the minimum team size can get access to Viva Insights in Teams and in Viva Insights through [Manager settings](../use/manager-settings.md). They can also explore metrics about their specific team and access **Plans** in Viva Insights, where they can set up plans and track plan progress.

## You control the data that Viva Insights uses

You retain full control over what data is used and how it is used within Viva Insights. Viva Insights uses Microsoft 365 email and calendar metadata and external data defined by your organization (usually exported from an HR system) to compute how much time groups within your organization spend in meetings, emails, calls, and chats, and with whom.

Viva Insights processes data sourced with [organizational data](#organizational-data) from your own HR system and [collaboration data from Microsoft 365](#collaboration-data-from-microsoft-365) to provide analysts with a unified pool of data on which to perform analyses.

### Organizational data

Organizational data is contextual information about your employees (for example: job title, level, location) and can come from human resources, information systems, or other line-of-business data stores. Viva Insights combines Microsoft 365 email, calendar, call, and instant message metadata with the organizational data that you choose to use to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

The organizational data set is combined with the Microsoft 365 metadata to produce the complete dataset that is analyzed for insights. The data sets are combined using the email addresses of the users, but the email addresses are never shown in Viva Insights through dashboards or query results.

Note that other information provided in the organizational data set is exposed in Viva Insights and in Viva Insights. Take care to ensure that the data set does not include personal data (such as the employee ID).
For more details, see [Prepare organizational data](../setup/prepare-organizational-data.md).

### Collaboration data from Microsoft 365

Microsoft 365 email, calendar, call, and instant message metadata provides the foundation for all analysis in Viva Insights, so the first step is to determine which users you want to include. When you choose a user to be included, Viva Insights uses the following information about items in that user's mailbox and calendar:

 | item | originator | recipient | subject | chronology | status | venue |
 | ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
 | **email** | sender | recipients | subject line | sent time |  |  | 
 | **meeting** | organizer | invitees | subject line | scheduled time | attendee status | scheduled location | 
 | **call** | organizer | invitees |  | scheduled time, <br>call joined time, <br>call duration | call/join status |  | 
 | **chat** | sender of <br>initial IM | recipients |  | IM sent time |  |  | 

>[!Important]
>Attachments and text in the body of email and meetings are never used by Viva Insights. Furthermore, rights-managed, confidential, and private email and meetings are excluded altogether.

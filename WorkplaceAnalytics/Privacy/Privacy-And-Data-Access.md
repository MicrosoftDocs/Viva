---

title: Workplace Analytics privacy and data access
description: Discusses the privacy and data access controls available in Workplace Analytics  
author: paul9955
ms.author: v-mideh
ms.topic: conceptual
localization_priority: normal
search.appverid:
- MET150 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Workplace Analytics privacy and data access

Being aware of employees' rights is a key component to ensuring a successful program using Workplace Analytics. It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Workplace Analytics.

>[!Important]
> Consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

This document introduces the privacy controls available to Workplace Analytics administrators. You control both the data and access to the data in Workplace Analytics.

## You decide who gets to see what data

Organizations decide who can have access to see the data in Workplace Analytics. You should ensure that primary users receive suitable training in privacy, and in your company’s policies and other applicable subject areas, before being granted access to the data. The following levels of permission provide access to the data:

* **Analyst (Limited Access)** has access to the Workplace Analytics **Home** page and explore metrics features where minimum group size is enforced.
* **Analyst** has full access to all product features except the administrator features.
* **Administrator role** has access to administrator features only (**Settings** and **Data Source** pages).
* **Program manager** has access to the Workplace Analytics **Home** page and lets program managers explore metrics in cases where the minimum group size is enforced. They also have access to **Plans** and its **Manage** and **Track** pages, where they can set up plans and track the progress of active or ended plans.
* **People managers** can get access to Workplace Analytics through [Manager settings](../use/manager-settings.md). If they meet the minimum team size, they can see the **Home** page and explore metrics about their specific team. They also have access to **Plans** and its **Manage** and **Track** pages, where they can set up plans and track the progress of active or ended plans.

## You control the data that Workplace Analytics uses

You retain full control over what data is used and how it is used within Workplace Analytics. Workplace Analytics uses Office 365 email and calendar metadata and external data defined by your organization (usually exported from an HR system) to compute how much time groups within your organization spend in meetings, emails, calls, and chats, and with whom.

Workplace Analytics processes data from these two sources&mdash;[organizational data](#organizational-data) from your own HR system and [collaboration data from Office 365](#collaboration-data-from-office-365)&mdash;to provide your analysts with a unified pool of data on which to perform analyses. The following sections describe these two data sources:

### Organizational data

Organizational data is contextual information about your employees (for example: job title, level, location) and can come from human resources, information systems, or other line-of-business data stores. Workplace Analytics combines Office 365 email, calendar, call, and instant message metadata with the organizational data that you choose to use to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

The organizational data set is combined with the Office 365 metadata to produce the complete dataset that is analyzed for insights. The data sets are combined using the email addresses of the users, but the email addresses are never shown in Workplace Analytics through dashboards or query results.

Note that other information provided in the organizational data set is exposed in Workplace Analytics dashboards and reports. Take care to ensure that the data set does not include personal data (such as the employee ID).
For more information about organizational data, see [Prepare organizational data](~/setup/prepare-organizational-data.md).

### Collaboration data from Office 365

Office 365 email, calendar, call, and instant message metadata provides the foundation for all Workplace Analytics analysis, so the first step is to determine which users you want to include. When you choose a user to be included, Workplace Analytics uses the following information about items in that user's mailbox and calendar:

 | item | originator | recipient | subject | chronology | status | venue |
 | ---- | ---- | ---- | ---- | ---- | ---- | ---- | 
 | **email** | sender | recipient | subject line | sent time |  |  | 
 | **meeting** | organizer | invitees | subject line | scheduled time | attendee status | scheduled location | 
 | **call** | organizer | invitees |  | scheduled time, <br>call joined time, <br>call duration | call/join status |  | 
 | **chat** | sender of <br>initial IM | recipient |  | IM sent time |  |  | 

<!-- THE ABOVE TABLE MIGHT REPLACE THE FOLLOWING SECTIONS 
#### Header information from email

* Who the sender is
* Who the recipient is
* When was the email sent
* What the subject line is

#### Header information from meetings

* Who organized the meeting
* Who the invitees are and what their attendee status is
* When the meeting was scheduled
* Where the meeting was scheduled to be held
* What the subject line is

#### Header information from instant messages

* Who sent the instant message
* Who received the instant message
* When the instant message was sent

#### Header information from calls

* Who organized the call
* When the call was joined
* Who the invitees were and what their attendee/call join status was
* When the call was scheduled (if it was a scheduled call)
* The duration of the call

-->

> [!Important]
> Attachments and text in the body of email and meetings are never used by Workplace Analytics. Furthermore, rights-managed, confidential, and private email and meetings are excluded altogether.

## Related topic

[Workplace Analytics privacy settings](../use/privacy-settings.md)

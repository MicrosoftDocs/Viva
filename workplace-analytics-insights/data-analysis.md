---
ROBOTS: NOINDEX,NOFOLLOW
title: Insights data access and analysis
description: More details about what data is accessed and analyzed in Insights
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa

---

# Data access and analysis

*This experience is only available through private preview at this time.*

Being aware of employees' rights is a key component to ensuring success in using Insights. It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Insights.

Insights does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies.

>[!Important]
> Consult with your legal and human resources teams before enabling Insights for your organization.

## Who sees the data

Your organization decides who gets access to Insights. You ensure that employees receive suitable training in privacy, and in your company’s policies and other applicable subject areas, before granting them access to the data in Insights.

## Organizational data

Organizational data is contextual information about your employees (such as manager and department) that comes from information your organization provided in Microsoft Azure Active Directory (AD).

## Collaboration data

Insights combines the organizational data in Azure AD with Microsoft 365 metadata to compute how much time groups of employees within your organization spend in meetings, emails, calls, and chats, and with whom.

This Microsoft 365 metadata provides the foundation for the analysis in Insights. The analysis uses the following information about items in employee mailboxes and calendars.

 | Item | Originator | Recipient | Subject | Chronology | Status | Venue |
 | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
 | **email** | sender | recipient | subject line | sent time |  |  |
 | **meeting** | organizer | invitees | subject line | scheduled time | attendee status | scheduled location |
 | **call** | organizer | invitees |  | scheduled time, <br>call joined time, <br>call duration | call/join status |  |
 | **chat** | sender of <br>initial IM | recipient |  | IM sent time |  |  |

---
# Metadata Sample
# required metadata

title: MyAnalytics plans and environments
description: MyAnalytics supported plans and environment requirements
author: paul9955
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: mya
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# MyAnalytics plans and environments

## Availability of features

The MyAnalytics [Dashboard](../use/dashboard-2.md), [Digests](../use/email-digest-2.md), [Insights Outlook Add-in](../use/add-in.md), and [Inline suggestions](../use/mya-notifications.md) are available to users whose organization uses the following Microsoft 365 or Office 365 plans:

| Plan  | Service plan | 
| ----- | ----- |
| <li>Microsoft 365 E3  <li>Microsoft 365 Business     <li>Microsoft 365 A3 for faculty/students <li>Office 365 E3  <li>Office 365 E1 <li>Office 365 A3 for faculty/students  <li>Office 365 E3 Developer <li>Office 365 G3   <li>Office 365 G1 <li>Business Premium <li>Business Essentials |  Insights by MyAnalytics |
| <li>Microsoft 365 E5 <li>Microsoft 365 E5 without Audio Conferencing &nbsp; &nbsp; &nbsp; <li>Office 365 Enterprise E5 <li>Office 365 Nonprofit E5 <li>Office 365 G5<li>MyAnalytics add-on | MyAnalytics (Full) and   Insights by MyAnalytics | 
| <li>Microsoft 365 A5 for faculty/students <li>Office 365 A5 for faculty/students | MyAnalytics (Full) | 
 
> [!Note]
> * To find out how to determine your own plan and service plan, see [How do I find my plan?](../overview/mya-faq.md#q4-how-can-i-find-out-what-my-plan-is) 
> * [Email read statistics](../use/add-in.md#email-read-statistics) are available only in the MyAnalytics (Full) service plan. 

For more information about the plans that offer these user experiences, see [Office 365 business plans](https://products.office.com/business/compare-more-office-365-for-business-plans).

## Access to MyAnalytics elements

After users get assigned licenses with a MyAnalytics service plan, they get access to the following MyAnalytics elements based on their service plan.

| Element | Approximate timeframe |
| ------- | ------------------|
|  [Welcome email](../use/mya-welcome-email.md)| Sent to existing Office 365 users a few days (up to four weeks) after license assignment; sent to new users approximately four weeks after license assignment|
|  [Dashboard](../use/dashboard-2.md)  | Available a few days after license assignment |
|  [Digests](../use/email-digest-2.md)  | Sent the Monday of the first week after the welcome email |
|  [Inline suggestions](../use/mya-notifications.md)  | Available about one day after license assignment |
|  [Insights Outlook add-in](../use/add-in.md)  | Available about one day after license assignment |


> [!Note]  
> * _Licensed users_ have MyAnalytics automatically enabled after license assignment. 
> * _All users_ in your organization are opted-in, whether or not they have licenses with a MyAnalytics service plan. If you want one or more licensed users to be opted _out_ by default, see [Set MyAnalytics access for one user](../setup/configure-myanalytics.md#set-myanalytics-access-for-one-user) and [Set MyAnalytics access for multiple users](../setup/configure-myanalytics.md#set-myanalytics-access-for-multiple-users).

## Environment support

### Office 365 environments that are supported

* Worldwide Multi-tenant
* Dedicated Multi-tenant
* Government Community Cloud (GCC)

### Office 365 environments that are not supported

* GCC-High
* DoD
* Office 365 Germany
* Office 365 Operated by 21Vianet

### Browser support

You can use the following web browsers to view your MyAnalytics dashboard:

* Microsoft Edge or Edge Chromium (coming soon)
* Microsoft Internet Explorer version 10 or 11
* Google Chrome (latest version)
* Apple Safari (latest version)
* Mozilla Firefox (latest version)

As an Outlook Add-in, the Insights Outlook Add-in requires a browser compatible with your system's platform and operating system. For details, see [Browsers used by Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins).

## Language support

MyAnalytics is available in the same languages as Microsoft Office. See [What languages is Office available in](https://support.office.com/en-ie/article/what-languages-is-office-available-in-26d30382-9fba-45dd-bf55-02ab03e2a7ec)?

## Prerequisites and exclusions

* [Microsoft Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-service-description) is required for MyAnalytics and the Outlook add-in.

* **Licensing exclusion:** Shared mailboxes cannot use and are not supported by the MyAnalytics service plan.

### Outlook support and prerequisites

MyAnalytics feature | Supported in Outlook 2013? | Supported in Outlook 2016? | Mobile support?
 ----- | ----- |----- | ----
Outlook Add-in | Yes, when the add-in commands are enabled for the Outlook add-in. For details, see [Add-in commands for Outlook](https://docs.microsoft.com/outlook/add-ins/add-in-commands-for-outlook). | Yes | No
Inline suggestions | No | Yes, when actionable messages are supported and enabled. For details, see [Actionable messages in Outlook and Office 365 Groups](https://docs.microsoft.com/outlook/actionable-messages/). | No  

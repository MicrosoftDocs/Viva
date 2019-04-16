---
# Metadata Sample
# required metadata

title: MyAnalytics environment requirements
description: MyAnalytics environment requirements
author: madehmer
ms.author: v-midehm
ms.date: 04/11/2019
ms.topic: article
localization_priority: normal 
ms.prod: mya
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

## Availability of features

The following table lists which user experiences are available depending on what Microsoft 365 or Office 365 plan your organization uses.

| Plan | Service plan | User experience available |
| ----- | ----- |----- |
| <li>Microsoft 365 E3    <li>Microsoft 365 Business     <li>Office 365 E3     <li>Office 365 E1     <li>Business Premium     <li>Business Essentials    <br> <br> | <br> <br> Insights by MyAnalytics| <br> <br>[Insights Outlook Add-in](../use/add-in.md)   (This feature will be rolled out beginning in May 2019. No welcome email will be sent to introduce this feature.) |
|<li>Microsoft 365 E5     <li>Office 365 Enterprise E5     <li>Office 365 A5     <li>Office 365 Nonprofit E5      <li>MyAnalytics add-on | <br> <br> MyAnalytics (Full) and Insights by MyAnalytics | <br> <br> [Dashboard](../use/dashboard-2.md), [Add-in](../use/add-in.md), [Email digest](../use/email-digest-2.md), and [Nudges](../use/mya-notifications.md) |

> [!Note]
> To provide a great experience for users and customers, we are rolling out the features of MyAnalytics gradually, with the ultimate goal of achieving feature parity among all plans. We will announce each new feature release in the [Message center](https://docs.microsoft.com/en-us/office365/admin/manage/message-center?view=o365-worldwide).

For more information about the plans that offer these user experiences, see [Office 365 business plans](https://products.office.com/en-us/business/compare-more-office-365-for-business-plans).

## Support of environments

### Office 365 environments that are supported

* Worldwide Multi-tenant
* Dedicated Multi-tenant
* GCC

### Office 365 environments that are not supported

* GCC-High
* DoD
* Office 365 Germany
* Office 365 Operated by 21Vianet

## Prerequisites and exclusions

* [Microsoft Exchange Online](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/exchange-online-service-description) is required for MyAnalytics and the Outlook add-in.

* **Licensing exclusion:** Shared mailboxes cannot use and are not supported by the MyAnalytics service plan.

#### Outlook support and requirements for MyAnalytics

MyAnalytics feature | Supported in Outlook 2016? | Supported in Outlook 2013? | Mobile support?
 ----- | ----- |----- | ----
Outlook Add-in | Yes, when the add-in commands are enabled for the Outlook add-in. For details, see [Add-in commands for Outlook](https://docs.microsoft.com/en-us/outlook/add-ins/add-in-commands-for-outlook). | Yes | No
Nudges | No | Yes, when actionable messages are supported and enabled. For details, see [Actionable messages in Outlook and Office 365 Groups](https://docs.microsoft.com/outlook/actionable-messages/). | No  

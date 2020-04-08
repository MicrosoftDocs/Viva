---
# Metadata Sample
# required metadata

title: Environment and support aspects of Workplace Analytics 
description: Describes the system requirements for setting up and using Workplace Analytics
author: paul9955
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Environment requirements for Workplace Analytics

### Office 365 tenant requirements

Workplace Analytics requires an Office 365 tenant with Exchange Online.  Mailboxes must have [Exchange Online Plan 1 or Plan 2 licenses assigned](https://products.office.com/exchange/compare-microsoft-exchange-online-plans).

Currently, Workplace Analytics supports multi-tenant, multi-geo tenant, and vNext environments. Each mailbox that you want to license must have its data stored in Exchange Online.

### Workplace Analytics licenses and trials

Workplace Analytics is licensed as an add-on to existing Office 365 subscriptions. These are the plans to which Workplace Analytics can be added: 

 * Exchange Online (EXO) Plan 1 (Office 365 Enterprise plan E1)
 * Exchange Online (EXO) Plan 2 (Office 365 Enterprise plans E3, E4, or E5).

Licenses cost $2/license per month for Office 365 Enterprise E5 subscriptions and $6/license per month for all other qualifying Office 365 subscriptions. Licensing Workplace Analytics does not change the end-user experience in Office 365.

Workplace Analytics licenses are applied to the mailboxes that you want to analyze. This can be all the employees in your organization or a specific subset. The population of employees that you license are referred to in Workplace Analytics as _measured employees_. Because Workplace Analytics insights are de-identified and aggregated, measured-employee populations typically benefit the most if they consist of at least several hundred people.

Microsoft does not currently offer trials of Workplace Analytics. For more information about Workplace Analytics and how to purchase it, contact your Microsoft account team. 

### Supported browsers

Safari and Firefox are not preferred browsers for Workplace Analytics. As of June 2019, Internet Explorer is no longer a supported browser for Workplace Analytics 

For the best experience, please use Edge or Chrome.

## Related topics

[Get support](../overview/getting-support.md)

<!-- REMOVING FOR NOW 
### FastTrack qualification

FastTrack services for Workplace Analytics onboarding and training are available to customers who purchase at least 1,000 licenses.
-->
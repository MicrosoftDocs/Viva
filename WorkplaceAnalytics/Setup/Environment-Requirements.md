---

title: Requirements for Workplace Analytics 
description: Describes the system requirements for obtaining Workplace Analytics
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Requirements for Workplace Analytics

## Licensing checklist

With the proper licensing, your company can acquire Workplace Analytics as an add-on to its licensing agreement. To be able to purchase Workplace Analytics licenses, your company needs the following:

   ![checkbox 1](../images/wpa/setup/team-adopt-plan-checklist-box.png) An [Enterprise Agreement](#enterprise-agreements) (EA) with Microsoft 

   ![checkbox 2](../images/wpa/setup/team-adopt-plan-checklist-box.png) An Office 365 or Microsoft 365 product that contains either [Exchange Online Plan 1 or Exchange Online Plan 2](#exchange-online-plans). 

### Enterprise Agreements

To obtain Workplace Analytics, you must have an Enterprise Agreement (EA) in place. Other channels such as Cloud Solution Provider (CSP) do not support the addition of Workplace Analytics at this time. Also, note the following circumstances for various types of customers:

|  Type  | Notes |  
| ---- | ---- |
| Government | Government Community Cloud (GCC) does not currently support the addition of Workplace Analytics. |
| Education | Supported only for the analysis of faculty at this time, not for students. |
| Commercial | You can add Workplace Analytics with commercial enrollments. | 
| Non-profit | Workplace Analytics under a commercial EA can be used by non-profits but non-profit pricing is not available. |
| Firstline workers | Workplace Analytics does not support analysis of Firstline workers that use Microsoft Firstline Worker SKUs (F1, F3, F5) at this time. |

### Exchange Online plans

Microsoft Exchange Online provides much of the collaboration data that Workplace Analytics uses. For this reason, you must have an Office 365 or Microsoft 365 product that contains Exchange Online (EXO) Plan 1 or EXO Plan 2 on your enrollment.

In other words, only if a user has an Exchange Online mailbox can you assign a Workplace Analytics license to that user.

## Tenant environments and user licenses

### Tenants

Workplace Analytics requires an Office 365 tenant with Exchange Online. Workplace Analytics currently supports organizations with more than one tenant and tenants that are based in multiple geographic locations.

### Workplace Analytics licenses

[Assign Workplace Analytics licenses](assign-licenses-to-population.md) to the users whose mailboxes you want to analyze. This can mean all the employees in your organization or a specific subset. To ensure statistical significance and meaningful comparative analysis, companies obtain the most benefit when they deploy Workplace Analytics to the entire company or to a large group of employees.

>[!Important]
>Workplace Analytics is not yet supported for users whose mailboxes are in the following geo locations: Brazil, Germany, and Norway. For more details about geo locations, see [Moving core data to new Microsoft 365 datacenter geos](https://docs.microsoft.com/microsoft-365/enterprise/moving-data-to-new-datacenter-geos) and [Find the geo location of a mailbox](https://docs.microsoft.com/microsoft-365/enterprise/administering-exchange-online-multi-geo#find-the-geo-location-of-a-mailbox).

### Pricing

Contact your Microsoft account team for pricing.

<!-- REMOVED 17 Sept 2020
### Trials

Trials of Workplace Analytics are made available to select customers. Please work with your account team to develop a scenario for the valuable use of Workplace Analytics.
-->

### Supported Browsers

For the best experience, use Microsoft Edge or Google Chrome. 

Apple Safari and Mozilla Firefox are not preferred browsers for Workplace Analytics. Internet Explorer is no longer a supported browser for Workplace Analytics.

## Further questions

If you have questions about licensing, such as "How can I obtain Workplace Analytics for my business, school, or non-profit?" have your admin reach out to your Microsoft account team, or use [this form](https://resources.office.com/ww-landing-workplace-analytics.html?LCID=EN-US) to inquire about Workplace Analytics.

## Related topics

[Get support](../overview/getting-support.md)

Under [Powerful tools to support your enterprise](https://www.microsoft.com/en-us/microsoft-365/business/compare-more-office-365-for-business-plans), see **Looking for more** for more details about the available plans.

To provide feedback, go to [Microsoft uservoice for Office 365](https://office365.uservoice.com/).  


<!-- FORMER CONTENT 

### Workplace Analytics licenses and trials

Licenses cost $2/license per month for Office 365 Enterprise E5 subscriptions and $6/license per month for all other qualifying Office 365 subscriptions. Licensing Workplace Analytics does not change the end-user experience in Office 365.

Workplace Analytics licenses are applied to the mailboxes that you want to analyze. This can be all the employees in your organization or a specific subset. The population of employees that you license are referred to in Workplace Analytics as _measured employees_. Because Workplace Analytics insights are de-identified and aggregated, measured-employee populations typically benefit the most if they consist of at least several hundred people.

Microsoft does not currently offer trials of Workplace Analytics. For more information about Workplace Analytics and how to purchase it, contact your Microsoft account team.

### Supported browsers

Apple Safari and Mozilla Firefox are not preferred browsers for Workplace Analytics. As of June 2019, Internet Explorer is no longer a supported browser for Workplace Analytics.

For the best experience, please use Microsoft Edge or Google Chrome.

-->

<!-- REMOVING FOR NOW 
### FastTrack qualification

FastTrack services for Workplace Analytics onboarding and training are available to customers who purchase at least 1,000 licenses.
-->
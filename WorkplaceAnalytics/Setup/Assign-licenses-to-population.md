---
# Metadata Sample
# required metadata

title: Workplace Analytics setup steps for meeting exclusions
description: Set up Workplace Analytics licenses for population in scope for Analysis
author: paul9955
ms.author: v-leash
ms.date: 04/19/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator
* **Task** - Determine population in scope for analysis and assign licenses via Office 365
* **Outcome** - Office 365 licenses are assigned for the population that will be analyzed

The Workplace Analytics sponsor will work with the Workplace Analytics administrator and Office 365 Global administrator to identify the population (the people in your company) whose Office 365 collaboration activity you want to analyze. These people are referred to as _measured employees_ within Workplace Analytics. Employees in your organization that are not licensed for analysis but may have meeting and email collaboration with measured employees are called _other internal collaborators_.

Some organizations will analyze the entire population, while others will use sub-populations for specific analysis scenarios and sections of the organization.

Once you have identified the population in scope, the Office 365 Global administrator will assign Workplace Analytics licenses to users in this population.  

#### Related topics

Workplace Analytics licenses are assigned just like any other Microsoft 365 product license. You can assign licenses by using the following:​

 * <u>The Office 365 Admin Center​</u>
 * <u>PowerShell​</u>
 * <u>Group-Based Licensing​:</u> Note theat Group-based licensing is currently available only through teh Azure portal. If you primarily use other management portals for your and group management, such as the Office 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level. 

For more information: 

[Use the the Office 365 Admin Center to assign licenses](https://support.office.com/en-us/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc?ui=en-US&rs=en-US&ad=US)

[Use PowerShell to assign licenses](https://docs.microsoft.com/en-us/office365/enterprise/powershell/assign-licenses-to-user-accounts-with-office-365-powershell)

[Use Group-based licensing to assign licenses](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/licensing-groups-assign)

### Mailboxes not fully migrated to Office 365 Exchange Online

If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with the following options.

### Options for mailboxes hosted using Exchange on-premises

* Migrate these mailboxes to Office 365 Exchange Online
* Contact the FastTrack team to understand the process for analyzing these mailboxes (this requires additional work streams within your organization).
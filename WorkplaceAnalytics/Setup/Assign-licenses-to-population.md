---

title: Introduction to assigning licenses for Workplace Analytics users
description: Assign Workplace Analytics licenses for population in scope for analysis
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Assign licenses

The following describes who does what to assign licenses to Workplace Analytics users:

* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, and/or Exchange administrator
* **Task** - Determine population in scope for analysis and assign licenses through Microsoft 365 or Office 365
* **Outcome** - Office 365 licenses are assigned for the population that will be analyzed

The Workplace Analytics sponsor works with the Workplace Analytics administrator and Office 365 Global administrator to identify the population (the people in your company) whose Office 365 collaboration activity you want to analyze. These people are referred to as _measured employees_ within Workplace Analytics.

Employees in your organization who are not licensed for analysis but might collaborate with your measured employees, through meetings, email, unscheduled calls, or instant messages, are called _other internal collaborators_. Some organizations analyze the entire population, while others use population subsets for specific analysis scenarios.

After you have identified the population in scope, the Office 365 Global administrator assigns Workplace Analytics licenses to users in this population.

> [!Note]
> Workplace Analytics is licensed as an add-on to existing Office 365 subscriptions. For more details, see [Environment requirements for Workplace Analytics](environment-requirements.md).

### Video: Assign licenses

<!-- Intro text out for now:
Watch this video to learn how Workplace Analytics licenses work and how the Office 365 admin can assign Workplace Analytics licenses.
-->

<!-- old link, with thumbnail
[<img src="../Images/WpA/setup/Assign-licenses.png" alt="Assign licenses video">](https://aka.ms/AssignWpALicenses_Video)
-->

<iframe width="640" height="564" src="https://player.vimeo.com/video/282896938" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

### License assignment options

Workplace Analytics licenses are assigned just like any other Microsoft 365 product license. You can assign licenses in the following ways:​

* [Group-based licensing](../Use/Group-Based-Licensing.md)
* [Office 365 Admin Center​](https://aka.ms/Instructions_AssignLicenseUsingO365AdminCenter)
* [PowerShell](../Use/Assigning-licenses-with-powershell.md)

   > [!Note]
   > Group-based licensing is currently available only through the Azure portal. If you primarily use other management portals for user and group management, such as the Office 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level.

#### If mailboxes are not fully migrated to Office 365 Exchange Online

If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with migrating these mailboxes to Office 365 Exchange Online.

## Related topics

* [Environment requirements for Workplace Analytics](environment-requirements.md)
* [Office 365 data](../use/office-365-data.md)

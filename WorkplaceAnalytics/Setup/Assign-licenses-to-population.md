---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup -- Assign licenses to Workplace Analytics users
description: Set up Workplace Analytics licenses for population in scope for Analysis
author: madehmer
ms.author: madehmer
ms.date: 08/08/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Assign licenses 

* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator
* **Task** - Determine population in scope for analysis and assign licenses via Office 365
* **Outcome** - Office 365 licenses are assigned for the population that will be analyzed

The Workplace Analytics sponsor will work with the Workplace Analytics administrator and Office 365 Global administrator to identify the population (the people in your company) whose Office 365 collaboration activity you want to analyze. These people are referred to as _measured employees_ within Workplace Analytics. Employees in your organization who are not licensed for analysis but might have meeting, email, or Skype for Business Online collaboration with measured employees are called _other internal collaborators_.

Some organizations analyze the entire population, while others use sub-populations for specific analysis scenarios.

Once you have identified the population in scope, the Office 365 Global administrator assigns Workplace Analytics licenses to users in this population.  

### Video: Assign licenses

<!-- Intro text out for now:
Watch this video to learn how Workplace Analytics licenses work and how the Office 365 admin can assign Workplace Analytics licenses.
-->

<!-- old link, with thumbnail
[<img src="../Images/WpA/setup/Assign-licenses.png" alt="Assign licenses video">](https://aka.ms/AssignWpALicenses_Video)
-->

<iframe width="640" height="564" src="https://player.vimeo.com/video/282896938" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

### License assignment options

Workplace Analytics licenses are assigned just like any other Microsoft 365 product license. You can assign licenses the following ways:​

* [Office 365 Admin Center​](https://aka.ms/Instructions_AssignLicenseUsingO365AdminCenter)
* [PowerShell](https://aka.ms/Instructions_AssignLicenseUsingPowerShell)
* [Group-based licensing](https://aka.ms/Instructions_AssignLicenseUsingGBL)

   > [!Note]
   > Group-based licensing is currently available only through the Azure portal. If you primarily use other management portals for user and group management, such as the Office 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level.

#### If mailboxes are not fully migrated to Office 365 Exchange Online

If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with the following options:

* Migrate these mailboxes to Office 365 Exchange Online.
* Contact the FastTrack team to understand the process for analyzing these mailboxes; this will require additional work streams within your organization.

### Related topics

[Group-based licenses in Workplace Analytics](../Use/Group-Based-Licensing.md)
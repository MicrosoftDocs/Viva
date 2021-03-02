---

title: Introduction to assigning licenses for Workplace Analytics users
description: Assign Workplace Analytics licenses for population in scope for analysis
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Assign licenses

The following describes who does what to assign licenses to Workplace Analytics users:

* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator, Microsoft 365 Global administrator, and/or Exchange administrator
* **Task** - Determine population in scope for analysis and assign licenses through Microsoft 365 or Office 365
* **Outcome** - Microsoft 365 licenses are assigned for the population that will be analyzed

The Workplace Analytics sponsor works with the Workplace Analytics administrator and Microsoft 365 Global administrator to identify the population (the people in your company) whose Microsoft 365 collaboration activity you want to analyze. These people are referred to as _measured employees_ within Workplace Analytics.

Employees in your organization who are not licensed for analysis but might collaborate with your measured employees, through meetings, email, unscheduled calls, or instant messages, are called _other internal collaborators_. Some organizations analyze the entire population, while others use population subsets for specific analysis scenarios.

After you have identified the population in scope, the Microsoft 365 Global administrator assigns Workplace Analytics licenses to users in this population. Note that users can find out for themselves whether they've been assigned a license; see [Users can view their subscription status](#users-can-view-their-subscription-status).

The assignment of licenses affects the user counts that are shown in the Workplace Analytics **Data sources** pages; see [Origin of data counts](../use/office-365-data.md#origin-of-data-counts). 

> [!Note]
> Workplace Analytics is licensed as an add-on to existing Microsoft 365 subscriptions. For more details, see [Environment requirements for Workplace Analytics](environment-requirements.md).

### Users can view their subscription status

Microsoft 365 users might want to find out whether their collaboration data is being processed. First, they should know that Workplace Analytics processes data only for users who've been assigned Workplace Analytics licenses. Next, they need to determine whether they have a license. They can determine this by completing the following steps.

#### To find out if I have a Workplace Analytics license

**Role:** Microsoft 365 user 

1. Open the [Microsoft 365 portal](https://portal.office.com).
2. Sign in to your Microsoft 365 account.
3. View your account settings.
4. Open the **Subscriptions** page. If you've been assigned a Workplace Analytics license, "Workplace Analytics" appears as one of your Microsoft 365 subscriptions. This means that your data is being processed.

## Video: Assign licenses

<!-- Intro text out for now:
Watch this video to learn how Workplace Analytics licenses work and how the Microsoft 365 admin can assign Workplace Analytics licenses.
-->

<!-- old link, with thumbnail
[<img src="../Images/WpA/setup/Assign-licenses.png" alt="Assign licenses video">](https://aka.ms/AssignWpALicenses_Video)
-->

<iframe width="640" height="564" src="https://player.vimeo.com/video/282896938" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## License assignment options

Workplace Analytics licenses are assigned just like other Microsoft 365 product licenses. You can assign them by using the Microsoft 365 Admin Center, PowerShell, or Azure group-based licensing:

* [Group-based licensing](../Use/Group-Based-Licensing.md)
* [Microsoft 365 Admin Center​](https://aka.ms/Instructions_AssignLicenseUsingO365AdminCenter)
* [PowerShell](../Use/Assigning-licenses-with-powershell.md)

   > [!Note]
   > Group-based licensing is currently available only through the Azure portal. If you primarily use other management portals for user and group management, such as the Microsoft 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level.

#### If mailboxes are not fully migrated to Microsoft 365 Exchange Online

If your organization has not fully migrated to Microsoft 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Microsoft 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with migrating these mailboxes to Microsoft 365 Exchange Online.

## Appearance of newly licensed users 

The data that Workplace Analytics uses is refreshed once a week, on Sunday. Workplace Analytics then processes the new data, which appears one day later, on Monday. This includes the data records for licensed users. Therefore, if you add a user license on a Tuesday, that person will not show up in Workplace Analytics until the following Monday. After this weekly refresh and processing, data that pertains to the newly licensed user appears in Workplace Analytics in the following ways:

 * The user is represented in the user counts that are displayed on the [Workplace Analytics Insights](../use/insights.md) page under **My organization's data**.
 * [Queries](../tutorials/query-basics.md) that analysts run can return results that include data about this user's activities.
 * [Explore the stats](../use/explore-intro.md) can reflect data that includes a newly licensed employee.

Azure Active Directory (AAD) is the single source of truth for licensing statuses. After a user license is added in AAD, that user will appear in AAD but not in Workplace Analytics until the next data refresh cycle is complete the following Monday.

## Related topics

* [Environment requirements for Workplace Analytics](environment-requirements.md)
* [Microsoft 365 data](../use/office-365-data.md)

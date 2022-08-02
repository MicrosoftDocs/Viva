---
ROBOTS: NOINDEX,FOLLOW
title: Assigning licenses overview
description: Assign Microsoft Viva Insights licenses for population in scope for analysis
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Assign licenses overview

The following describes who does what to assign licenses to users for Microsoft Viva Insights.

* **Owner** &ndash; Viva Insights sponsor, Viva Insights Administrator, Azure Active Directory (AD) [Application Administrator](/azure/active-directory/roles/permissions-reference#application-administrator), or [Exchange admin](/azure/active-directory/roles/permissions-reference#exchange-administrator). For more information, see [About admin roles](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide&preserve-view=true).
* **Task** &ndash; Determine population in scope for analysis and assign licenses through Microsoft 365 or Office 365
* **Outcome** &ndash; Microsoft 365 licenses are assigned for the population that will be analyzed

The Viva Insights sponsor works with the Viva Insights Administrator, Microsoft 365 global admin, and Azure AD Application Administrator to identify the population (the people in your company) whose Microsoft 365 collaboration activity you want to analyze. These people are referred to as _measured employees_.

Employees in your organization who are not licensed for analysis but might collaborate with your measured employees, through meetings, email, unscheduled calls, or instant messages, are called _other internal collaborators_. Some organizations analyze the entire population, while others use population subsets for specific analysis scenarios.

After you have identified the population in scope, the global admin assigns Viva Insights licenses to users in this population. Note that people can find out if they've been assigned a license; see [Subscription status](#subscription-status).

The assignment of licenses affects the measured population that is shown in **Data sources**. See [Origin of data counts](../use/office-365-data.md#origin-of-data-counts) for details.

>[!Note]
>Viva Insights is licensed as an add-on to existing Microsoft 365 subscriptions. For more details, see [Environment requirements](environment-requirements.md).

### Subscription status

Microsoft 365 users might want to find out whether their collaboration data is being processed. First, they should know that the advanced insights app with Viva Insights processes data only for users who've been assigned licenses. Next, they can determine if they have a license with the following steps.

#### Confirm an assigned license

**Role** - Microsoft 365 user

1. Open the [Microsoft 365 portal](https://portal.office.com).
2. Sign in to your Microsoft 365 account.
3. View your account settings.
4. Open the **Subscriptions** page. If you've been assigned a license, "Viva Insights" or "Workplace Analytics" shows as one of your Microsoft 365 subscriptions, then your data is being processed for Viva Insights.

>[!Note]
>Workplace Analytic licenses were sold prior to October 2021 and will continue to be active until updated to a Viva Insights license. As of October 2021, you can only purchase or assign Viva Insights licenses for your organization. Different licenses and role assignments give you access to different features. For details, see [User roles in Viva Insights](../use/user-roles.md).

<!--## Video: Assign licenses
Intro text out for now:
Watch this video to learn how Workplace Analytics licenses work and how the Microsoft 365 admin can assign Workplace Analytics licenses. old link, with thumbnail
[<img src="../Images/WpA/setup/Assign-licenses.png" alt="Assign licenses video">](https://aka.ms/AssignWpALicenses_Video)

<iframe width="640" height="564" src="https://player.vimeo.com/video/282896938" frameborder="0" allowFullScreen></iframe>
-->
## License assignment options

Viva Insights licenses are assigned just like other Microsoft 365 product licenses. You can assign them by using the Microsoft 365 admin center, PowerShell, or Azure group-based licensing:

* [Group-based licensing](/azure/active-directory/enterprise-users/licensing-groups-assign)
* [Microsoft 365 admin center​](/microsoft-365/admin/add-users/add-users)
* [PowerShell](../Use/Assigning-licenses-with-powershell.md)

>[!Note]
>Group-based licensing is currently available only through the Azure portal. If you primarily use other management portals for user and group management, such as the Microsoft 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level.

### If mailboxes are not fully migrated to Microsoft 365 Exchange Online

If your organization has not fully migrated to Microsoft 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Azure AD [Global Admin](/azure/active-directory/roles/permissions-reference#global-administrator) or [Exchange admin](/azure/active-directory/roles/permissions-reference#exchange-administrator) can help to determine if you will encounter this scenario, and assist you with migrating these mailboxes to Microsoft 365 Exchange Online.

## Appearance of newly licensed users

The data that the advanced insights app with Viva Insights uses is refreshed once a week, on Sunday. The new data is then processed, which appears one day later, on Monday. This includes the data records for licensed users. Therefore, if you add a user license on a Tuesday, that person will not show up in Viva Insights data until the following Monday. After this weekly refresh and processing, data that pertains to the newly licensed user appears in Viva Insights in the following ways:

* The user is represented in the user counts that are shown in [Insights](../use/insights.md) under **My organization's data**.
* Analysts can use [Query designer](../tutorials/query-designer.md) to get results that include data about this user's activities.
* [Explore the stats](../use/explore-intro.md) can reflect data that includes a newly licensed employee.

Azure AD is the single source of truth for licensing statuses. After a user license is added in Azure AD, that user shows up in Azure AD but not in Viva Insights until the next data refresh cycle is complete the following Monday.

## Related topics

* [Environment requirements](environment-requirements.md)
* [Microsoft 365 data](../use/office-365-data.md)
* [About admin roles](/microsoft-365/admin/add-users/about-admin-roles)

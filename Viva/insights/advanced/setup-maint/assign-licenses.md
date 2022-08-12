---
ROBOTS: NOINDEX,FOLLOW
title: Assign licenses overview
description: Get an overview about assigning licenses to Microsoft Viva Insights users 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Assign licenses overview

The following describes who does what to assign licenses to users for Microsoft Viva Insights.

* **Owner** – Viva Insights sponsor, Viva Insights Administrator, Microsoft 365 [global admin](/microsoft-365/admin/add-users/about-admin-roles), or [Exchange admin](/azure/active-directory/roles/permissions-reference#exchange-administrator). For more information, see [About admin roles](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide&preserve-view=true).
* **Task** – Determine population in scope for analysis and assign licenses through Microsoft 365 or Office 365
* **Outcome** – Microsoft 365 licenses are assigned for the population that will be analyzed. Refer to [Plans and environments](/viva/insights/personal/overview/plans-environments#additional-features).

The Viva Insights sponsor works with the Viva Insights Administrator and Microsoft 365 global admin to identify the population (the people in your company) whose Microsoft 365 collaboration activity you want to analyze. These people are *measured employees*.

Employees in your organization who aren't licensed for analysis—but might collaborate with your measured employees through meetings, email, unscheduled calls, or Teams chats—are *other internal collaborators*. Some organizations analyze the entire population, while others use population subsets for specific analysis scenarios.

After you've identified the population in scope, the Microsoft 365 global admin assigns Viva Insights licenses to users in that population. Note that people can find out whether they've been assigned a license; see [Subscription status](#subscription-status).

The assignment of licenses affects the measured population that is shown in **Organizational data > Data quality**.

>[!Note]
>Viva Insights is licensed as an add-on to existing Microsoft 365 subscriptions. For more details, see [Environment requirements](/viva/insights/Setup/Environment-Requirements?toc=/viva/insights/advanced/toc.json&bc=/viva/insights/breadcrumb/toc.json).

### Subscription status

Microsoft 365 users might want to find out whether their collaboration data is being processed. First, they should know that the advanced insights app with Viva Insights processes data only for users who've been assigned licenses. Next, they can determine whether they have a license with the following steps.

#### Confirm an assigned license

**Role** - Microsoft 365 user

1. Open the [Microsoft 365 portal](https://portal.office.com).
2. Sign in to your Microsoft 365 account.
3. View your account settings.
4. Open the **Subscriptions** page. If you've been assigned a license, "Viva Insights" shows as one of your Microsoft 365 subscriptions, then your data is being processed for Viva Insights.

## License assignment options

Viva Insights licenses are assigned just like other Microsoft 365 product licenses. You can assign them by using the [Microsoft 365 admin center​](/microsoft-365/admin/add-users/add-users), PowerShell, or Azure [group-based licensing](/azure/active-directory/enterprise-users/licensing-groups-assign):

>[!Note]
>Group-based licensing is currently available only through the Azure portal. If you primarily use other management portals for user and group management, such as the Microsoft 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level.

### If mailboxes are not fully migrated to Microsoft 365 Exchange Online

If your organization hasn't fully migrated to Microsoft 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Azure AD [Global Admin](/azure/active-directory/roles/permissions-reference#global-administrator) or [Exchange admin](/azure/active-directory/roles/permissions-reference#exchange-administrator) can help to determine if you will encounter this scenario, and assist you with migrating these mailboxes to Microsoft 365 Exchange Online. 

## Appearance of newly licensed users

The data that the advanced insights app with Viva Insights uses is refreshed once a week, on Sunday. The new data is then processed, which appears one day later, on Monday. This data includes the data records for licensed users. So, if you add a user license on a Tuesday, that person won't show up in Viva Insights data until the following Monday. After this weekly refresh and processing, data that pertains to the newly licensed user appears in Viva Insights in the following ways:

* The user is represented in the user counts that are shown in **Organizational data > Data quality**.
* When analysts run [queries](/analyst/person-query.md), results include data about this user's activities.

Azure AD is the single source of truth for licensing statuses. After a user license is added in Azure AD, that user shows up in Azure AD but not in Viva Insights until the next data-refresh cycle is complete the following Monday.

## Related topics

[About admin roles](/microsoft-365/admin/add-users/about-admin-roles)

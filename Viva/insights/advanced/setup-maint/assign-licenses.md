---
ms.date: 10/17/2024
title: Assign licenses
description: Assign Viva Insights licenses to users in your organization
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Assign licenses for Viva Insights

>[!Note]
>Viva Insights is licensed as an add-on to existing Microsoft 365 subscriptions. For more details, refer to [Environment requirements](environment-requirements.md).

When you assign somebody a license for Viva Insights, you do two things:

* Add them into aggregated data, which analysts can run queries on and managers can view in organization insights.
* Make them eligible for premium personal insights experiences, including organization insights for managers.

The license-assignment process for Viva Insights has two main steps:

1. Determine the analyzed population.
1. Assign licenses through the Microsoft 365 admin center, PowerShell, or Azure.

## Determine the analyzed population

Before you can assign licenses, the Microsoft 365 Global Administrator, the Viva Insights sponsor, and the Insights Administrator work together to identify the analyzed population. This population consists of the people in your company—called *measured employees*—whose Microsoft 365 collaboration activity you want to analyze. Some organizations choose to analyze the entire population, while others use population subsets for specific analysis scenarios. If you want to get insights that reflect all people in the company, you'll need to assign everyone a license.

>[!Note]
>Employees in your organization who aren't licensed for analysis—but might collaborate with your measured employees through meetings, email, unscheduled calls, or Teams chats—are called *other internal collaborators*. You might encounter this term while using Viva Insights.

 People can find out whether they've been assigned a license; refer to [FAQ](../../personal/overview/mya-faq.md#q2-how-can-i-find-out-what-my-plan-is). 

For more information on licensing and user configuration, refer to [Configure personal insights](configure-personal-insights.md).

## Assign licenses

After you've identified the population in scope, the license admin or user admin assign Viva Insights licenses to users in that population.

>[!Note]
>A minimum of 10 licenses is required to be assigned in order for data processing to kick off. Data processing takes an estimated 3-5 days from license assignment.

Viva Insights licenses are assigned just like other Microsoft 365 product licenses. Assign licenses by using one of these options:

>[!Note]
>To start data processing, you'll need to assign at least 10 licenses. Once you do that, the process will take about three to five days. 

* The [Microsoft 365 admin center​](/microsoft-365/admin/add-users/add-users)
* [PowerShell](/microsoft-365/enterprise/assign-licenses-to-user-accounts-with-microsoft-365-powershell)
* Azure [group-based licensing](/azure/active-directory/enterprise-users/licensing-groups-assign)

>[!Note]
>Group-based licensing is currently available only through the Azure portal. If you primarily use other management portals for user and group management, like the Microsoft 365 portal, you can continue to do so. But you should use the Azure portal to manage licenses at the group level.

### If mailboxes are not fully migrated to Microsoft 365 Exchange Online

If your organization hasn't fully migrated to Microsoft 365 Exchange Online, you might encounter mailboxes that are hosted using Exchange on-premises. Your Microsoft Entra ID [Exchange admin](/azure/active-directory/roles/permissions-reference#exchange-administrator) can help to determine if you will encounter this scenario, and assist you with migrating these mailboxes to Microsoft 365 Exchange Online.

## When newly licensed users show up in data

The data that the advanced insights app uses refreshes once a week, during the first part of the week. This data includes the data records for licensed users. So, if you add a user license, it's possible that person won't show up in Viva Insights data until the following week. After this weekly refresh and processing, data that pertains to the newly licensed user appears in Viva Insights in the following ways:

* The user is represented in the user counts that are shown in **Organizational data > Data quality**.
* When analysts run [queries](../analyst/person-query.md), results include data about this user's activities.

The Microsoft admin center and Microsoft Entra tell you whether a user is licensed. After a user is assigned a license, that user shows up in Microsoft Entra ID and the Microsoft admin center, but not in Viva Insights until the next data-refresh cycle is complete during the first part of the following week.

### When users show up in query results

For a user to appear in query results, that user needs to have a license at the time the query is run.

Let's say an employee was licensed from January 1 through March 31. Here are three different scenarios and whether the user would be included in query results:

|Query time period| Query run date| Is the user included in query results?|
|-----------------|-------------|-----|
|January 1 through March 31|March 31 |**Yes.** The user was licensed at the time the query was run. |
|January 1 through March 31|April 2|**No.** The user wasn't licensed at the time the query was run.|
|December 1 through March 31 |March 31|**Yes.** The user was licensed at the time the query was run, even though they didn't have a license for the first month of the time period.|

## Next steps

> [!div class="nextstepaction"]
> [Assign user roles](./assign-user-roles.md)

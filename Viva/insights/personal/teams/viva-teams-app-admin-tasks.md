---

title: Admin tasks for the Viva Insights app
description: Admin tasks for the Microsoft Viva Insights app available for Microsoft Teams
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.collection: 
- viva-insights-manager
- viva-insights-leader
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: helayne
audience: Admin

---

# Admin tasks for Viva Insights

As a [Teams Service Administrator](/microsoftteams/using-admin-roles#teams-roles-and-capabilities), you can deploy and pin the Microsoft Viva Insights app in Microsoft Teams for all the users or for specific groups in your organization [through custom policies](/microsoftteams/teams-app-setup-policies).

## Prerequisites

Before people in your organization can use the Viva Insights app, they must have the following:

* Access to Microsoft Teams
* An Exchange Online account

## Install the app

Complete the steps in the following playbooks to get the Viva Insights app up and running for people in your organization.

1. Confirm they have a [Viva Insights service plan](../overview/plans-environments.md).
2. In the [Teams admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), add the Viva Insights app to the list of allowed apps within the organization, as follows:
[Release the Viva Insights app within your organization](https://download.microsoft.com/download/1/b/9/1b980a29-f166-4b72-8d8e-d1126f4028c7/Release-the-Insights-app.pdf).

   >[!Note]
   >To allow or block specific users in your organization from using Viva Insights, do the following:
   >
   >1. Confirm that Viva Insights is turned on for your organization on the [Manage apps](/microsoftteams/manage-apps) page.
   >2. Create a custom app permission policy and assign it to those users. For details, see [Manage app permission](/microsoftteams/manage-apps) policies in Teams.

3. In Teams, pin the Viva Insights app in the left app bar for all users in your organization: [Pin the Viva Insights app](https://download.microsoft.com/download/5/d/f/5df6c702-58f2-4768-b8e5-26ffd2c78b80/Pin-the-Insights-app.pdf).
4. Now that Viva Insights is available, all users can follow these steps to [Discover and pin the Viva Insights app](viva-teams-app-install.md).

>[!Important]
>If your organization assigned licenses before July 2021 (under the Workplace Analytics SKU), follow [these steps](#access-to-premium-features) to enable or disable access to the Viva Insights premium features released starting in November 2021.

## Disable Headspace

When the Headspace feature is enabled, users can find it on the [Home](viva-insights-home.md) page of Viva Insights. As an admin, you can disable this feature by using PowerShell cmdlets.

The PowerShell commands for working with Viva Insights features are described in [Set-VivaInsightsSettings](/powershell/module/exchange/set-vivainsightssettings). To disable Headspace, see [Example 1](/powershell/module/exchange/set-vivainsightssettings).

## Premium access for licenses assigned before July 2021

The following steps are only applicable to organizations who assigned licenses prior to July 2021. You need to confirm the following assignment options in Azure Active Directory for the Microsoft Viva Insights SKU:

* **Microsoft Viva Insights** - Enables access to premium personal and manager features released starting in November 2021, including the updated [My team](../../use/myteam.md) page in the Viva Insights app in Teams.
* **Microsoft Viva Insights (WpA transition)** – This option is only applicable for organizations who assigned licenses before July 2021 and want to keep their access to the advanced analyst features. If this is the only option enabled, then their access to advanced insights will continue unchanged. However, you must enable the first app option for access to the premium features released starting in November 2021.

>[!Important]
>If your organization assigned Viva Insights licenses starting in July 2021, the Microsoft Viva Insights assignment option controls access to all premium personal, manager, and advanced analyst features. Enabling or disabling the Microsoft Viva Insights (WpA transition) option in Azure Active Directory will not affect their access to these features.

### Access to premium features

To confirm, enable, or disable access to premium features for users with licenses assigned before July 2021, complete the following steps.

1. Go to [Azure portal](https://portal.azure.com/) > **Azure Active Directory**.
2. In the left navigation, select **Licenses** > **All products**.
3. Search for and select **Microsoft Viva Insights**.
4. In the left navigation, for groups, select **Licensed groups** or for individual users, select **Licensed users**.
5. At the top, select **+Assign**.
6. In **Users and groups**, select the group or individual to add, which will then show up under **Name**.
7. Select **Assignment options**, and then select **On** to enable or **Off** to disable the following:

   * **Microsoft Viva Insights** – Enables access to premium features that were released starting in November 2021.
   * **Microsoft Viva Insights (WpA transition)** – Only applicable to users who were assigned licenses **before July 2021**.

    ![Azure AD license app options for Viva Insights](./images/wpa-transition-app-option.png)

8. Select **Review + assign**, and then near the bottom, select **Assign** to apply the changes.

## Related topics

[Viva Insights introduction](viva-teams-app.md)

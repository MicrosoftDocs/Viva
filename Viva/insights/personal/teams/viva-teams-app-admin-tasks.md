---

title: Admin tasks for the Viva Insights app
description: Admin tasks for the Microsoft Viva Insights (personal insights) app
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.collection: m365initiative-viva-insights
ms.localizationpriority: medium 
ms.prod: Mya
manager: scott.ruble
audience: Admin

---

# Admin tasks for Viva Insights

As a [Teams Service Administrator](/microsoftteams/using-admin-roles#teams-roles-and-capabilities), you can deploy and pin the Microsoft Viva Insights app in Microsoft Teams for all the users or for specific groups in your organization [through custom policies](/microsoftteams/teams-app-setup-policies).

Complete the steps in the following playbooks to get the Viva Insights app up and running for people in your organization.

1. Confirm that the employees who want to use the Viva Insights app in Microsoft Teams have the Microsoft Viva Insights license with the [MyAnalytics (Full) service plan](../overview/plans-environments.md).
2. Turn on the Viva Insights app for your organization:
[Release the Insights app within your organization](https://download.microsoft.com/download/1/b/9/1b980a29-f166-4b72-8d8e-d1126f4028c7/Release-the-Insights-app.pdf).

   >[!Note]
   >To allow or block specific users in your organization from using Insights, do the following:
   >
   >1. Make sure that Viva Insights is turned On or Off for your organization on the [Manage apps](/microsoftteams/manage-apps) page.
   >2. Create a custom-app permission policy and assign it to those users. For details, see [Manage app permission](/microsoftteams/manage-apps) policies in Teams.

3. Pin the Viva Insights app in Teams left navigation for all users in your organization: [Pin the Viva Insights app](https://download.microsoft.com/download/5/d/f/5df6c702-58f2-4768-b8e5-26ffd2c78b80/Pin-the-Insights-app.pdf).
4. Now that the Viva Insights app is available for employees, they can follow these steps to locate and open it: [Find and open the Insights app](https://download.microsoft.com/download/c/a/6/ca665366-e059-4977-8175-04461af196c1/Find-and-open-the-Insights-app.pdf).

>[!Note]
>If your organization purchased licenses before **July 2021** (under the Workplace Analytics SKU), follow the steps in the next section to enable or disable access to Viva Insights premium features.

## Admin tasks for earlier licenses to get premium features

For users with licenses purchased before **July 2021**, you’ll need to enable them access to the premium features available within the Microsoft Viva Insights apps. The Microsoft Viva Insights SKU includes the following app options in the Microsoft Azure Active Directory:

* **Microsoft Viva Insights** - Enables access to premium features within personal and manager insights on the *updated* [My team](../../use/myteam.md) page in the Viva Insights in Microsoft Teams app.
* **Microsoft Viva Insights (WpA transition)** – Only relevant for users with licenses purchased **_before July 2021_** and are using the Workplace Analytics app. If this is the only app that is enabled, this group or individual will continue to have access (as assigned) to the advanced analyst features in Workplace Analytics but they will not have access to the premium features available for personal and manager insights, such as for the *updated* [My team](../../use/myteam.md) page in the Viva Insights in Teams app.

>[!Important]
>If your organization purchased Viva Insights licenses starting in July 2021, all the regular and premium features are available within your employees’ personal, team lead, manager, and leader insights in the Viva Insights in Teams app. Enabling or disabling the WpA transition app option in Azure Active Directory will not change their access to Viva Insights in Teams.

If your organization purchased Workplace Analytics **before July 2021**, you might have accidentally assigned the Microsoft Viva Insights in Teams app to your employees, which enables them to see the premium features in Viva Insights in Teams. To confirm this possibility and to enable or disable access to the app as applicable, complete the following steps.

### Set up access to premium features

1. Go to [Azure portal](https://portal.azure.com/) > **Azure Active Directory**.
2. In the left navigation, select **Licenses** > **All products**.
3. Search for and select **Microsoft Viva Insights**.
4. In the left navigation, for groups, select **Licensed groups** or for individual users, select **Licensed users**.
5. At the top, select **+Assign**.
6. In **Users and groups**, select the group or individual to add, which will then show up under **Name**.
7. Select **Assignment options**, and then select **On** to enable or **Off** to disable the following:

   * **Microsoft Viva Insights** – Select to enable the Viva Insights in Teams app.
   * **Microsoft Viva Insights (WpA transition)** – This setting is only applicable to groups or individuals with managers who were assigned licenses that were purchased **before July 2021**.

    ![Azure AD license app options for Viva Insights](../images/wpa/setup/wpa-transition-app-option.png)

8. Select **Review + assign**, and then near the bottom, select **Assign** to apply the changes.

## Disable Headspace

When the Headspace feature is enabled, users can find it on the [Home](viva-insights-home.md) page of Viva Insights. As an admin, you can disable this feature by using PowerShell cmdlets.

The PowerShell commands for working with Viva Insights features are described in [Set-VivaInsightsSettings](/powershell/module/exchange/set-vivainsightssettings). To disable Headspace, see [Example 1](/powershell/module/exchange/set-vivainsightssettings).

## Related topics

[Viva Insights introduction](viva-teams-app.md)

---

title: Admin tasks for the Viva Insights app
description: Admin tasks for the Microsoft Viva Insights (personal insights) app
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
ms.prod: Mya
manager: scott.ruble
audience: Admin

---

# Admin tasks for Viva Insights

[Teams Service Administrators](/microsoftteams/using-admin-roles#teams-roles-and-capabilities) can choose to deploy and pin the Microsoft Viva Insights app in Microsoft Teams for all users or specific departments [through custom policies](/microsoftteams/teams-app-setup-policies).

Complete the steps in the following four mini-playbooks to get the Viva Insights app up and running for people in your organization.

1. Turn on the Viva Insights app for your organization:
[Release the Insights app within your organization](https://download.microsoft.com/download/1/b/9/1b980a29-f166-4b72-8d8e-d1126f4028c7/Release-the-Insights-app.pdf).

   >[!Note]
   >To allow or block specific users in your organization from using Insights, do the following:
   >
   >1. Make sure that Insights is turned on for your organization on the [Manage apps](/microsoftteams/manage-apps) page.
   >
   >2. Create a custom-app permission policy and assign it to those users. To learn more, see [Manage app permission](/microsoftteams/manage-apps) policies in Teams.

2. Pin the Viva Insights app to the left navigation pane of Teams for all employees in your organization: [Pin the Viva Insights app](https://download.microsoft.com/download/5/d/f/5df6c702-58f2-4768-b8e5-26ffd2c78b80/Pin-the-Insights-app.pdf).

3. Now that the Viva Insights app is available for employees, they can follow these steps to locate and open it: [Find and open the Insights app](https://download.microsoft.com/download/c/a/6/ca665366-e059-4977-8175-04461af196c1/Find-and-open-the-Insights-app.pdf).

## Disable Headspace

When the Headspace feature is enabled, users can find it on the [Home](viva-insights-home.md) page of Viva Insights. Admins can disable this feature by using PowerShell cmdlets.

The PowerShell commands for working with Viva Insights features are described in [Set-VivaInsightsSettings](/powershell/module/exchange/set-vivainsightssettings). To disable Headspace, see [Example 1](/powershell/module/exchange/set-vivainsightssettings).

## Related topics

[Viva Insights introduction](viva-teams-app.md)

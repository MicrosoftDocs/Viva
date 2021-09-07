---
ROBOTS: NOINDEX,NOFOLLOW
title: Set up Microsoft 365 Insights
description: Steps to set up Microsoft 365 Insights
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
ms.localizationpriority: null
ms.prod: wpa
manager: scott.ruble
audience: Admin
---
# Set up insights

*This experience is only available through private preview at this time.*

Before people in your organization can view and use Microsoft 365 Insights, your Microsoft 365 global admin needs to do the following for them:

* [Activate promotional codes](#activate-promotional-codes)
* [Assign licenses](#assign-licenses)
* [Assign roles](assign-roles.md)
* [Deploy the app](#deploy-the-app)

This new release is currently limited to Microsoft 365 or Office 365 E5 or E3 plan subscribers through their Microsoft service representative.

You can request access and get more information at [Microsoft Workplace Analytics](https://www.microsoft.com/microsoft-365/business/workplace-analytics). Select **Contact us** and complete the form to request access and get more information about Microsoft 365 Insights.

## Activate promotional codes

1. Depending on which browser you are using, on the Windows taskbar or Start menu, right-click the browser application and select **Start InPrivate Browsing**, **New InPrivate window**, **New incognito window**, or **New private window**.
2. Copy the **activation code link** that Microsoft sent you for Microsoft 365 Insights, paste it into the URL section of the private or incognito browser window, and then press **Enter** to open the link.

   ![Activation code link.](./images/sign-in.png)

3. When prompted, enter your email address.
4. Sign in with your Microsoft 365 or Office 365 global admin credentials, and then select **Next**.
5. In **Check out** > **confirm you order** > **Microsoft Microsoft 365 Insights trial**, select **Try now**.
6. When prompted in **order receipt**, select **Continue**.

## Assign licenses

You can assign licenses to people in your organization who subscribe to a Microsoft 365 or Office 365 E5 or E3 plan. To do this, you sign in to the Microsoft admin center as a global Microsoft 365 admin.

<!-- KEEPING ORIGINAL TEXT IN CASE WE NEED IT AGAIN (BECAUSE OF SWEDEN) AT END OF 2021: 
You must be able to sign in as a global Microsoft 365 admin to use the Microsoft admin center to assign licenses to people in your organization who subscribe to Microsoft 365 or Office 365 E5 or E3 plan whose [Microsoft 365 datacenter geo location is North America](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo#microsoft-365-multi-geo-availability). -->

You can assign licenses as follows:

* [Assign licenses to individual users with the Microsoft 365 admin center](assign-licenses.md)
* [Assign licenses to security groups with Azure AD](assign-licenses.md)
* [Assign licenses to users with Microsoft PowerShell](assign-licenses-pshell.md)

## Deploy the app

[Teams Service Administrators](/microsoftteams/using-admin-roles#teams-roles-and-capabilities) can choose to deploy and pin the app for all users or particular departments [through custom policies](/microsoftteams/teams-app-setup-policies).

Complete the steps in the following mini-playbooks to get the Microsoft Viva Insights app up and running for people in your organization.

1. Turn on the Viva Insights app for your organization:
[Release the Insights app within your organization](../workplaceanalytics/myanalytics/use/release-the-Insights-app.pdf).

   >[!Note]
   >To allow or block specific users in your organization from using Insights, do the following:
   >
   >1. Make sure that Viva Insights is turned on for your organization on the [Manage apps](/microsoftteams/manage-apps) page.
   >
   >2. Create a custom-app permission policy and assign it to those users. To learn more, see [Manage app permission](/microsoftteams/manage-apps) policies in Teams.

2. Install the Viva Insights app for all employees in your organization: [Install the Insights app](../workplaceanalytics/myanalytics/use/install-the-Insights-app.pdf).
3. Pin the Insights app to the left navigation pane of Teams for all employees in your organization: [Pin the Insights app](../workplaceanalytics/myanalytics/use/pin-the-Insights-app.pdf).
4. Now that the Insights app is available for employees, they can follow these steps to locate and open it: [Find and open the Insights app](../workplaceanalytics/myanalytics/use/find-and-open-the-Insights-app.pdf).
5. To give a person access to leader insights, assign the _Analyst (Limited)_ role in Workplace Analytics to that person. (See [Assign roles](../workplaceanalytics/setup/assign-roles-to-wpa-admins.md) for admin procedures; for general information about roles, see [Role descriptions and access levels](../workplaceanalytics/use/user-roles.md#role-descriptions-and-access-levels).)

## Access to Insights

After assigning licenses and deploying the app, the data for insights might take up to a week to process and become available. After [assigning roles](assign-roles.md) and allowing for data processing, refer your organization's leaders to [Install and pin the app](install.md) to open and use them. Also, refer them to [Viva Insights introduction](./intro.md) to learn more about how to use them.

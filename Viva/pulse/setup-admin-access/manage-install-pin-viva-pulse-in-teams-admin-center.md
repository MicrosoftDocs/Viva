---
title: Manage, install, and pin Viva Pulse in the Teams admin center
description: "Manage, install, and pin Viva Pulse in the Teams admin center"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.collection:
 - essentials-manage
ms.date: 07/12/2023
ms.topic: article
ms.service: viva-pulse
ms.localizationpriority: medium
search.appverid: MET150
---

# Manage, install, and pin Viva Pulse in the Teams admin center

The following settings are optional and are not required to be completed before users in the organization can start using Viva Pulse. You must be a Microsoft 365 Global Admin or a Teams Admin for the following tasks.

## Control access to Viva Pulse

To allow access to Viva Pulse or to block specific users from using Viva Pulse, you can create a custom app permission policy. You can only control access to Viva Pulse for the Teams experience. You cannot control access for the web experience.

For more information, see [Manage app permission policies in Teams](/microsoftteams/teams-app-permission-policies).

## Install the Viva Pulse app using an app setup policy

You can choose to deploy and pin the Viva Pulse app for all users or for specific departments through a [Teams app setup policy](/microsoftteams/teams-app-setup-policies).

To install apps using an app setup policy, follow these steps:

1. Sign into the Teams admin center, access **Teams apps**, and select [Setup policies](https://admin.teams.microsoft.com/policies/app-setup).
2. Select **Add**.
3. Enter a name and description for the policy.
4. Under **Installed apps**, select **Add apps**.
5. In the **Add installed apps** pane, search for the apps that you’d like to install for users. You can also filter apps by app permission policy.
6. Select **Add**.

For more information, see [Learn more about installing apps in Teams](/microsoftteams/teams-app-setup-policies#install-apps).

## Pin Viva Pulse in Microsoft Teams

Use the Teams app to set up policies to pin this app by default in the left rail of the Teams app and apply this policy to a batch of users.

To create an app setup policy to pin apps, follow these steps:

1. In the left navigation of the Microsoft Teams admin center, go to **Teams apps** and select [Setup policies](https://admin.teams.microsoft.com/policies/app-setup).
2. Select **Add**.
3. Enter a name and description for the policy.
4. Optionally, turn on **User pinning** to allow users to pin apps and change the order of the pinned apps to personalize their app bar.
5. Under **Pinned apps**, select **Add apps**.
6. In the **Add pinned apps** pane, search for the apps you want to add, and then select **Add**. You can also filter apps by app permission policy.
7. Select **Add**.
8. Arrange the apps in the order that you want them to appear in Teams.
9. Select **Save**.
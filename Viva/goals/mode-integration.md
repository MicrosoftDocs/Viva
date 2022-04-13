---
title: Mode integration
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Automate your OKR progress by connecting OKRs with Mode reports."
---

# Mode integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Who can use this feature?  

All Users and Admins (Admins also have permissions to manage the integration from the admin dashboard) 

## About Mode integration

Viva Goals Mode integration allows you to link your OKRs to reports in Mode for automatic real-time updates on your objectives. For example, if you have an objective to increase user adoption to a feature by 30% then you can directly link this objective with the relevant data in a report. Whenever there’s an update in the report, your OKR’s status gets automatically updated. With Mode integration, Viva Goals continues to offer you flexibility and real-time clarity in your company’s OKR journey. 

## Connect Mode to your Viva Goals account

1. The first step in setting up the Mode integration is to connect your Mode account to Viva Goals. Navigate to your sidebar and select **Admin** and then select **Integrations**.

    :::image type="content" source="../media/goals/goals-integrations-mode.gif" alt-text="Image of Admin dashboard Integrations":::

2. In the integrations section, go to Mode and then select **Manage**.

    :::image type="content" source="../media/goals/goals-integrations-mode-manage.png" alt-text="Image of Manage"::: 

3. Select **New Connection** and in the pop-up dialog box, sign in to your Mode account using your credentials to authenticate the connection. 

    :::image type="content" source="../media/goals/goals-integrations-new-connection.png" alt-text="Image of new connection":::

## Get your Mode workspace ID and API token

Workspace ID: To get your Mode Workspace ID, select your **My Work** in the side navigation bar and copy the workspace ID from the URL. For example: if your URL is ```https://app.mode.com/home/vivagoals/search```, vivagoals is the Workspace ID.  

:::image type="content" source="../media/goals/goals-workspace-ID-API-token.png" alt-text="Image of Workspace ID":::

Mode API Token: To create your mode API token, select your profile and select **My Account**. On your account page, navigate to 'API Tokens' under Community. Select **Create token** to create a new mode API token.

:::image type="content" source="../media/goals/goals-create-token.png" alt-text="Image of Mode API Token"::: 

Once you have your Mode workspace ID and API Token, add it to the connection page in Viva Goals. 

Name your connection, add your organization name (this is your Mode Workspace ID), Token (this is your Mode API Token), and then select Next to complete the new account setup. 

:::image type="content" source="../media/goals/goals-create-connection.png" alt-text="Image of name your connection":::

:::image type="content" source="../media/goals/goals-new-setup.png" alt-text="Image of new setup ":::

## Editing an existing Mode connection

Admins can also edit an existing Mode connection, including the integration’s name and shared state that you’ve created, from the Mode integration’s view. 

1. Start in the Integrations section in the Admin Dashboard and select **Mode**. 

2. Select the **Edit** icon next to the Mode connection. In the pop-up dialog box that displays, you can edit the connection’s name, token, organization domain, password and select or clear the Share connection with all users checkbox. 

    :::image type="content" source="../media/goals/goals-edit-mode-connection.gif" alt-text="Image of editing an existing mode connection":::

## Using the Mode integration

Once the Mode integration is set up, you can measure your OKR progress by connecting your new or existing OKRs in Viva Goals with a corresponding report in Mode. 

1. Go to the list of integrations available and select Mode. If there are multiple Mode connections listed, choose a connection you’d like to use. 

2. Next, map the OKR to the report and query of your choice. 

3. Select Next to finish and save your OKR. You’ll now see the Mode icon next to the OKR‘s progress indicator, which means Viva Goals will automatically measure the progress based on the updates in the corresponding report in Mode. 

    > [!NOTE]
    > Viva Goals will sync data from Mode at every one-hour interval.

    :::image type="content" source="../media/goals/goals-using-mode.gif" alt-text="Image of sync data ":::

    You can also configure a scheduler in Mode to make sure Viva Goals syncs the latest data from your Mode Report.  

    :::image type="content" source="../media/goals/goals-create-new-schedule.png" alt-text="Image of create a new schedule":::

    :::image type="content" source="../media/goals/goals-create-schedule.png" alt-text="Image of create schedule":::

## Disabling the integration

The Mode integration may also be disabled by an Admin at any time. To disable the integration, as an Admin go to Mode in the Integrations section and select on Manage. In the Mode Configurations page, select the Change dropdown, select Disable and confirm the action. 

:::image type="content" source="../media/goals/goals-disabling-mode.gif" alt-text="Image of disabling the integration":::


Learn more about other integrations available in Viva Goals [ here.](https://help.ally.io/en/collections/30526-integrations)
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

## About the Mode integration

The Viva Goals Mode integration allows you to link your OKRs to reports in Mode for automatic real-time updates on your objectives. 

For example, if you have an objective to increase user adoption to a feature by 30%, you can directly link this objective with the relevant data in a Mode report. Whenever there is an update in the report, your OKR status gets automatically updated. 

With the Mode integration, Viva Goals continues to offer you flexibility and real-time clarity in your company’s OKR journey. 

All users and admins have access to this integration. Admins also have permissions to manage the integration from the admin dashboard. 

## How to connect Mode to your Viva Goals account

1. The first step in setting up the Mode integration is to connect your Mode account to Viva Goals. Navigate to your sidebar and select **Admin** and then select **Integrations**.

    :::image type="content" source="../media/goals/11/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/11/viva-goals-integrations-page.png":::

2. In the integrations section, go to Mode and then select **Manage**.

    :::image type="content" source="../media/goals/11/mode-manage-button.png" alt-text="Managing Mode in Viva Goals." lightbox="../media/goals/11/mode-manage-button.png":::

3. Select **New Connection** and in the pop-up dialog box, sign in to your Mode account using your credentials to authenticate the connection. 

    :::image type="content" source="../media/goals/11/mode-configure-new-connection.png" alt-text="Configuring a new Mode connection in Viva goals." lightbox="../media/goals/11/mode-configure-new-connection.png":::

## How to get your Mode workspace ID and API token

1. To get your Mode Workspace ID, select your **My Work** in the side navigation bar and copy the workspace ID from the URL. For example: if your URL is ```https://app.mode.com/home/relecloud/search```, relecloud is the Workspace ID.  

2. To create your mode API token, select your profile and select **My Account Settings**. On your account page, navigate to 'API Tokens' under Community. Select **Create token** to create a new mode API token.

    :::image type="content" source="../media/goals/11/mode-create-token.png" alt-text="Creating API token in Mode for Viva Goals." lightbox="../media/goals/11/mode-create-token.png":::

3. Once you have your Mode workspace ID and API Token, add it to the connection page in Viva Goals. 

4. Name your connection, add your organization name (this is your Mode Workspace ID), Token (this is your Mode API Token), and then select Next to complete the new account setup. 

## How to edit an existing Mode connection

Admins can also edit an existing Mode connection, including the integration’s name and shared state that you’ve created, from the Mode integration’s view. 

1. Start in the Integrations section in the Admin Dashboard and select **Mode**. 

2. Select the **Edit** icon next to the Mode connection. In the pop-up dialog box that displays, you can edit the connection’s name, token, organization domain, password and select or clear the Share connection with all users checkbox. 

## How to use the Mode integration

Once the Mode integration is set up, you can measure your OKR progress by connecting your new or existing OKRs in Viva Goals with a corresponding report in Mode. 

1. Go to the list of integrations available and select Mode. If there are multiple Mode connections listed, choose a connection you’d like to use. 

    :::image type="content" source="../media/goals/11/mode-datasource.png" alt-text="Selecting Mode from the list of data sources in Viva Goals." lightbox="../media/goals/11/mode-datasource.png":::

2. Next, map the OKR to the report and query of your choice. 

    :::image type="content" source="../media/goals/11/mode-connection-details.png" alt-text="Adding new Mode connection to OKRs in Viva goals." lightbox="../media/goals/11/mode-connection-details.png":::

3. Select Next to finish and save your OKR. You’ll now see the Mode icon next to the OKR‘s progress indicator, which means Viva Goals will automatically measure the progress based on the updates in the corresponding report in Mode. 

    > [!NOTE]
    > Viva Goals will sync data from Mode at every one-hour interval. You can also configure a scheduler in Mode to make sure Viva Goals syncs the latest data from your Mode Report.  

## How to disable the Mode integration

The Mode integration can be disabled by an Admin at any time. 

1. To disable the integration as an Admin, go to Mode in the Integrations section and select on Manage. 
2. In the Mode Configurations page, select the Change dropdown, select Disable and confirm the action.

    :::image type="content" source="../media/goals/11/mode-disable-button.png" alt-text="Disabling Mode in Viva Goals." lightbox="../media/goals/11/mode-disable-button.png":::

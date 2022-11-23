---
title: Mode integration
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Automate your OKR progress by connecting OKRs with Mode reports."
---

# Mode integration

## About Mode integration

Viva Goals Mode integration lets you link your OKRs to reports in Mode for automatic real-time updates on your objectives. 

For example, say you have an objective to increase user adoption to a certain feature by 30 percent. You can directly link this objective to the relevant data in a Mode report. Whenever there's an update in the report, your OKR status gets automatically updated. 

With Mode integration, Viva Goals offers flexibility and real-time clarity in your company’s OKR journey.

All users and admins have access to this integration. Admins have permissions to manage the integration from the admin dashboard. 

## How to connect Mode to your Viva Goals account

1. The first step to set up the Mode integration is to connect your Mode account to Viva Goals. In the sidebar, select **Admin** and then **Integrations**.

    :::image type="content" source="../media/goals/11/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/11/viva-goals-integrations-page.png":::

2. In the integrations section, go to **Mode** and select **Manage**.

    :::image type="content" source="../media/goals/11/mode-manage-button.png" alt-text="Screenshot shows where to select Range for Mode in Viva Goals." lightbox="../media/goals/11/mode-manage-button.png":::

3. Select **New Connection**. In the pop-up dialog, sign in to your Mode account. 

    :::image type="content" source="../media/goals/11/mode-configure-new-connection.png" alt-text="Screenshot shows the mode sign-in dialog box." lightbox="../media/goals/11/mode-configure-new-connection.png":::

## How to get your Mode workspace ID and API token

1. To get your Mode workspace ID, select **My Work** in the side navigation bar and copy the workspace ID from the URL. For example, if your URL is ```https://app.mode.com/home/relecloud/search```, *relecloud* is the Workspace ID.  

2. To create your mode API token, select your profile and then select **My Account Settings**. On your account page, go to **API Tokens** under **Community**. Select **Create token** to create a new mode API token.

    :::image type="content" source="../media/goals/11/mode-create-token.png" alt-text="Screenshot shows where you select Create token for Mode." lightbox="../media/goals/11/mode-create-token.png":::

3. After you have your Mode workspace ID and API token, add the token to the connection page in Viva Goals. 

4. Name your connection, add your **organization name**, which is your Mode Workspace ID, and **token**, which is your Mode API token). Then select **Next** to complete new account setup. 

## How to edit an existing Mode connection

Admins can edit an existing Mode connection, including the integration’s name any shared state that you’ve created, from the Mode integration's view. 

1. Start in the **Integrations** section in the Admin Dashboard and select **Mode**. 

2. Select the **Edit** icon next to the Mode connection. In the dialog box that appears, you can edit the connection's name, token, organization domain, and password and select or clear the **Share connection with all users** checkbox.

## How to use Mode integration

After Mode integration is set up, connect your OKRs in Viva Goals with a corresponding report in Mode to measure OKR progress: 

1. Go to the list of integrations available and select **Mode**. If multiple Mode connections are listed, choose the connection you want to use. 

    :::image type="content" source="../media/goals/11/mode-datasource.png" alt-text="Screenshot shows where you select Mode as your date source in Viva Goals." lightbox="../media/goals/11/mode-datasource.png":::

2. Next, map the OKR to the report and query of your choice. 

    :::image type="content" source="../media/goals/11/mode-connection-details.png" alt-text="Screenshot show where you add a new Mode connection to OKRs in Viva goals." lightbox="../media/goals/11/mode-connection-details.png":::

3. Select **Next** to finish and save your OKR. You'll now see the Mode icon next to the OKR's progress indicator, which means Viva Goals will automatically measure the progress based on the updates in the corresponding report in Mode. 

    > [!NOTE]
    > Viva Goals will sync data from Mode every hour. You can also configure a scheduler in Mode to make sure Viva Goals syncs the latest data from your Mode Report.  

## How to disable Mode integration

An admin can disable Mode integration at any time: 

1. Go to **Mode** in the integrations section and select **Manage**. 
2. On the Mode Configurations page, select the **Change** dropdown, select **Disable**, and then confirm the action.

    :::image type="content" source="../media/goals/11/mode-disable-button.png" alt-text="Screenshot shows how to disable Mode in Viva Goals." lightbox="../media/goals/11/mode-disable-button.png":::

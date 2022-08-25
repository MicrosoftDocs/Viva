---
title: monday.com integration
ms.reviewer: 
ms.author: ranjaliroy
author: ranjali-MS
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
description: "Learn how to connect your projects in monday.com with Viva Goals."
---

# monday.com integration

## About monday.com integration

Viva Goals monday.com integration lets you link your OKRs to monday.com boards for automatic real-time updates on your objectives. 

For example, if you have an objective to "Become the market leader," you can directly link this objective with the relevant items on a board on monday.com. Whenever there's an update in the status of items on monday.com, your OKR status will automatically get updated.

All users and admins can use the monday.com integration. Admins also have permissions to manage the integration from the admin dashboard. 

## How to install the Viva Goals app for monday.com

Before you set up the integration connection, [reach out to your monday.com administrator](https://auth.monday.com/auth/login_monday/enter_slug?force_existing_account=true&oauth_payload_token=eyJhbGciOiJIUzI1NiJ9.eyJjbGllbnRfaWQiOiJiMTFlMmUxMDljOTdiMzcxYzAzYTk0YzRlNWQ4ZWNmZSIsInJlc3BvbnNlX3R5cGUiOiJpbnN0YWxsIiwib2F1dGhfdmVyc2lvbiI6Mn0.ld79ozTcYkdq5gD2eu60HSLoDeuNB_nb2bsOsmJzqyM) to install the Viva Goals app by using this [link.](https://auth.monday.com/oauth2/authorize?client_id=1d353d6e717b0b9329a61b0a264499b4&response_type=install) 

## Connect monday.com to your Viva Goals account from the admin dashboard

1. The first step to set up the monday.com integration is to connect your monday.com account to Viva Goals. From the sidebar, select **Admin** and then **Integrations**.

    :::image type="content" source="../media/goals/11/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/11/viva-goals-integrations-page.png":::

2. In the **Integrations** section, go to **monday.com** and then select **Manage**. 

    :::image type="content" source="../media/goals/11/monday-manage-button.png" alt-text="Screenshot shows where you choose to manage monday.com in Viva Goals." lightbox="../media/goals/11/monday-manage-button.png":::

3. Select **New Connection**. In the pop-up dialog, sign in to your monday.com account. 

    :::image type="content" source="../media/goals/11/monday-new-connection-button.png" alt-text="Screenshot shows where you choose to create a new connection for monday.com in Viva goals." lightbox="../media/goals/11/monday-new-connection-button.png":::

4. Name your connection, and then select **Next** to complete new account setup.

    :::image type="content" source="../media/goals/11/monday-configure-new-connection.png" alt-text="Screenshot shows where you name your new monday.com connection." lightbox="../media/goals/11/monday-configure-new-connection.png":::

## How to edit an existing monday.com connection

Admins can also edit an existing monday.com connection, including the integration’s name and any shared state that you created, from the monday.com integration view: 

1. Start in the **Integrations** section in the Admin Dashboard. Select **monday.com**. 

2. Select the **Edit** icon next to the monday.com connection. In the pop-up dialog box that appears, you can edit the connection's name or clear the **Share connection with all users** checkbox. 

## How to use the monday.com integration

After the monday.com integration is set up, you can connect your Viva Goals OKRs with a corresponding board in monday.com to measure your OKR progress:

1. Go to the OKR of your choice. In the **Progress** section, select the **Automatically from a data source** option.

1. Select **monday.com** from the list of integrations available. If multiple monday.com connections are listed, choose the connection you want to use or create a new one. 

    :::image type="content" source="../media/goals/11/monday-datasource.png" alt-text="Screenshot shows where you select monday.com as the data source to update progress." lightbox="../media/goals/11/monday-datasource.png":::

1. Select the board, group, and assignee you want to connect to and map the status column based on which OKR progress should be tracked. 

    :::image type="content" source="../media/goals/11/monday-connection-details.png" alt-text="Screenshot shows where you specify monday.com connection details for an OKR." lightbox="../media/goals/11/monday-connection-details.png":::

1. Select **Next** to finish and save your OKR. You'll now see the monday.com icon next to the OKR's progress indicator, which means Viva Goals will automatically measure the progress based on item updates in the corresponding board in monday.com. 

    > [!NOTE]
    >
    > - If an item in your monday.com has status indicated only by color but no labels, Viva Goals will consider that item incomplete even though the specific color is considered as done in the board column settings.
    > - If a monday.com doesn't have the default completion status, items that have status as *Done* will be considered complete.
    > - The **assignee** field in Viva Goals will be mapped to the **Owner** field in monday.com by default. You can also search and add assignees to list their items. The **Preview** option will show the total number of items that remaine and that are completed. For KPI-based OKRs, the Preview option will just show the total number of items available in the mapped board.
    > - Viva Goals will sync data from monday.com at one-hour intervals. 

## How to disable the monday.com integration

An admin can disable the monday.com integration at any time: 

1. Go to monday.com. In the **Integrations** section, select **Manage**. 

2. On the monday.com Configurations page, select the **Change** dropdown, select **Disable** and confirm. 

    :::image type="content" source="../media/goals/11/monday-disable-button.png" alt-text="Screenshot shows how to disable monday.com in Viva Goals." lightbox="../media/goals/11/monday-disable-button.png":::



---
title: monday.com integration
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
description: "Learn how to connect your projects in monday.com with Viva Goals."
---

# monday.com integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## About the monday.com integration

The Viva Goals monday.com integration allows you to link your OKRs to monday.com boards for automatic real-time updates on your objectives. 

For example, if you have an objective 'Become the Market Leader,' you can directly link this objective with the relevant items on a board on monday.com. Whenever there’s an update in the status of items on monday.com, your OKR status gets automatically updated. 

All users and admins can use the monday.com integration. Admins also have permissions to manage the integration from the admin dashboard. 

## How to install the Viva Goals app for monday.com

Before setting up the integration connection, reach out to your monday.com administrator to install the Viva Goals app using this [link.](https://auth.monday.com/auth/login_monday/enter_slug?force_existing_account=true&oauth_payload_token=eyJhbGciOiJIUzI1NiJ9.eyJjbGllbnRfaWQiOiJiMTFlMmUxMDljOTdiMzcxYzAzYTk0YzRlNWQ4ZWNmZSIsInJlc3BvbnNlX3R5cGUiOiJpbnN0YWxsIiwib2F1dGhfdmVyc2lvbiI6Mn0.ld79ozTcYkdq5gD2eu60HSLoDeuNB_nb2bsOsmJzqyM) 

## Connect monday.com to your Viva Goals account from the admin dashboard

1. The first step in setting up the monday.com integration is to connect your monday.com account to Viva Goals. Navigate to your sidebar and select **Admin** and then select **Integrations**.

2. In the integrations section, go to monday.com and then select **Manage**. 

3. Select **New Connection** and in the pop-up dialog box, sign in to your monday.com account using your credentials to authenticate the connection. 

4. Name your connection and then select **Next** to complete the new account setup.

## Editing an existing monday.com connection

Admins can also edit an existing monday.com connection, including the integration’s name and shared state that you’ve created, from the monday.com integration’s view. 

1. Start in the Integrations section in the Admin Dashboard and select **monday.com**. 

2. Select the **Edit** icon next to the monday.com connection. In the pop-up dialog box that displays, you can edit the connection’s name or clear the **Share connection with all users** checkbox. 

## How to use the monday.com integration

1. Once the monday.com integration is set up, you can measure your OKR progress by connecting your new or existing OKRs in Viva Goals with a corresponding board in monday.com

2. Go to the OKR of your choice and in the **Progress** section choose the option **Automatically from a data source**. 

3. Select monday.com from the list of integrations available and if there are multiple monday.com connections listed, choose a connection you’d like to use or create a new one. 

4. Select the board, group, and assignee you want to connect to and map the status column based on which OKR progress should be tracked. 

5. Select **Next** to finish and save your OKR. You’ll now see the monday.com icon next to the OKR‘s progress indicator, which means Viva Goals will automatically measure the progress based on the item updates in the corresponding board in monday.com. 

    > [!NOTE]
    >
    > - If an item in your monday.com has status indicated only by color and no labels, Viva Goals will consider that item incomplete even though the specific color is considered as done in board column settings.
    > - If a monday.com doesn’t have the default completion status, items that have status as **Done** will be considered complete.
    > - The assignee field in Viva Goals will be mapped to the Owner field on monday.com by default. You can also search and add assignees to list their items. The ‘Preview’ option will show the total number of items that are remaining and completed. For KPI-based OKRs the Preview option will just show the total number of items available in the mapped board.
    > - Viva Goals will sync data from monday.com at every one-hour interval. 

## How to disable the monday.com integration

The monday.com integration may be disabled by an Admin at any time. To disable the integration, go to monday.com. In the Integrations section, select **Manage**. 

In the monday.com Configurations page, select the Change dropdown, select Disable and confirm the action. 

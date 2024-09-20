---
ms.date: 04/13/2022
title: Amazon RedShift integration
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals 
- vg-integration 
search.appverid:
- MET150
description: "Sync data updates from Amazon Redshift with Viva Goals to update OKR progress"
---

# Amazon RedShift integration

## About Amazon RedShift integration

Viva Goals integration with Amazon Redshift allows you to link your OKRs in Viva Goals to datasets in Amazon Redshift to provide automatic, real-time updates on your objectives.

Say you have an objective to increase user adoption by 60 percent. You can link this objective with relevant data in Amazon Redshift. Then, whenever there's a change in the dataset and an update in the report, the data is automatically synced with Viva Goals, and the OKR status is updated.

All users and admins can use this integration. Admins manage the integration from the admin dashboard.

## How to set up Amazon RedShift integration

1. Connect Amazon Redshift to your Viva Goals account.

2. The first step to set up Amazon Redshift integration is to connect your account to Viva Goals. In the sidebar, select **Admin**, and then select **Integrations**.

    :::image type="content" source="../media/goals/12/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/12/viva-goals-integrations-page.png":::

3. In the Integrations section, go to Amazon Redshift and select **Manage**.

    :::image type="content" source="../media/goals/12/amazonredshift-manage-button.png" alt-text="Screenshot of the Manage window for Amazon RedShift Server in Viva Goals." lightbox="../media/goals/12/amazonredshift-manage-button.png":::

4. Select **New Connection**. In the dialog box that opens, enter a name for your connection, your Amazon Redshift hostname, and the port, user, password, and database to connect to authenticate the connection.

    :::image type="content" source="../media/goals/12/amazonredshift-configure-new-connection.png" alt-text="Screenshot of the dialog where you configure a new Amazon RedShift connection in Viva goals." lightbox="../media/goals/12/amazonredshift-configure-new-connection.png":::

5. Select **Next** to complete connection setup.

## How to edit an existing connection

To edit an existing connection’s name and shared state from the Amazon Redshift integration’s view, an admin can select the **Edit** icon next to the Amazon Redshift connection. In the dialog box that opens, edit the connection’s name and other fields and select or clear the **Share connection with all users** checkbox.

## How to use Amazon RedShift integration

Once integration is set up, you can measure your OKR progress by connecting your new or existing OKRs to an Amazon Redshift dataset.  

1. Select **Amazon Redshift** from the list of integrations available. If there are multiple connections listed, choose the connection that you want to use.

    :::image type="content" source="../media/goals/12/amazonredshift-datasource.png" alt-text="Screenshot of the dialog box where you select Amazon RedShift from the list of data sources in Viva Goals." lightbox="../media/goals/12/amazonredshift-datasource.png":::

2. Next, add your query and validate the response.

    :::image type="content" source="../media/goals/12/amazonredshift-connection-details.png" alt-text="Screenshot of the dialog box where you add new Amazon RedShift connection to OKRs in Viva goals." lightbox="../media/goals/12/amazonredshift-connection-details.png":::

3. Select **Next** to finish and save your OKR. You’ll now see the Amazon Redshift icon next to the OKR's progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report.

> [!NOTE]
> Viva Goals will sync data from Amazon Redshift at one-hour intervals. 

## How to disable Amazon RedShift integration

The admin can disable Amazon Redshift integration:
1. Go to Amazon Redshift in the **Integrations** section. Select **Amazon Redshift**, and then select **Manage**. 
2. On the configurations page, select the **Change** dropdown, select **Disable**, and then confirm.

    :::image type="content" source="../media/goals/12/amazonredshift-disable-button.png" alt-text="Screenshot of the dialog box where you disable Amazon RedShift in Viva Goals." lightbox="../media/goals/12/amazonredshift-disable-button.png":::



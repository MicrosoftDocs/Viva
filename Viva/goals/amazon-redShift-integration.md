---
title: Amazon RedShift integration
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
description: "Sync data updates from Amazon Redshift with Viva Goals to update OKR progress"
---

# Amazon RedShift integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Who can use this feature? 

All Users and Admins (Admins also have permissions to manage the integration from the admin dashboard)

## About the Amazon Redshift Integration

Viva Goals' Integration with Amazon Redshift allows you to link your OKRs in Viva Goals to datasets in Amazon Redshift to provide automatic, real-time updates on your objectives. For example, if you have an objective to increase user adoption by 60% then you can directly link this objective with the relevant data in Amazon Redshift. Whenever there’s a change in the dataset and the report is updated, this data is automatically synced with  Viva Goals every hour and the OKR status updated. 

### Set up

1. Connect Amazon Redshift to your Viva Goals account.

2. The first step in setting up the Amazon Redshift integration is to connect your account to Viva Goals. Navigate to your sidebar and select **Admin** and then select **Integrations**.

3. In the integrations section, go to Amazon Redshift and then select **Manage**. 

    :::image type="content" source="../media/goals/goals-amazon-redshift-integration.gif" alt-text="Image of integrations section":::

4. Select **New Connection** and in the pop-up dialog box, name your connection, give your Amazon Redshift hostname, port, user, password, the database you'd like to connect to authenticate the connection. 

    :::image type="content" source="../media/goals/goals-amazon-redshift-new-connection.png" alt-text="Image of new connection":::


5. Select **Next** to complete the new connection setup. 

    :::image type="content" source="../media/goals/goals-amazon-redshift-new-connection-complete.png" alt-text="Image of connection set up":::

## Edit an existing connection

Admins can edit an existing connection’s name and shared state that you’ve created from the Amazon Redshift integration’s view. 

Select the **Edit** icon next to the Amazon Redshift connection.  In the pop-up dialog box that follows, you can edit the connection’s name and other fields and select or clear the **Share connection with all users** checkbox. 

:::image type="content" source="../media/goals/goals-edit-amazon-redshift.gif" alt-text="Image of edit an existing connection":::

## Using the Amazon Redshift Integration

Once your integration is set up, you can measure your OKRs progress by connecting your new or existing OKRs with an Amazon Redshift dataset.  

1. Select **Amazon Redshift** from the list of integrations available. If there are multiple connections listed, choose the connection that you would like to use. 

2. Next, add your query and validate the response. 

3. Select **Next** to finish and save your OKR. You’ll now see the Amazon Redshift icon next to the OKR‘s progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report.

    :::image type="content" source="../media/goals/goals-using-amazin-redshift.gif" alt-text="Image of Using the Amazon Redshift Integration ":::

> [!NOTE]
> Viva Goals will sync data from Amazon Redshift at every one-hour interval. 

## Disabling the integration

The Amazon Redshift integration may also be disabled by an Admin at any time. To disable the integration, as an Admin go to Amazon Redshift in the Integrations section. Select Amazon Redshift in the integrations section and select Manage. In the configurations page, select the **Change dropdown**, select **Disable** and confirm the action.

:::image type="content" source="../media/goals/goals-disabling-amazon-redshift.gif" alt-text="Image of disabling the integration":::

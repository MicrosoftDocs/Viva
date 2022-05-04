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

## About the Amazon RedShift Integration

Viva Goals' Integration with Amazon Redshift allows you to link your OKRs in Viva Goals to datasets in Amazon Redshift to provide automatic, real-time updates on your objectives. 

For example, if you have an objective to increase user adoption by 60%, you can directly link this objective with relevant data in Amazon Redshift. Whenever there is a change in the dataset and the report is updated, this data is automatically synced with Viva Goals and the OKR status is updated. 

All users and admins can use this integration. Admins also have permissions to manage the integration from the admin dashboard. 

## How to set up the Amazon RedShift Integration

1. Connect Amazon Redshift to your Viva Goals account.

2. The first step in setting up the Amazon Redshift integration is to connect your account to Viva Goals. Navigate to your sidebar and select **Admin** and then select **Integrations**.

3. In the integrations section, go to Amazon Redshift and then select **Manage**. 

4. Select **New Connection** and in the pop-up dialog box, name your connection, give your Amazon Redshift hostname, port, user, password, the database you'd like to connect to authenticate the connection.

5. Select **Next** to complete the new connection setup. 

## How to edit an existing connection

Admins can edit an existing connection’s name and shared state from the Amazon Redshift integration’s view. 

Select the **Edit** icon next to the Amazon Redshift connection.  In the pop-up dialog box that follows, you can edit the connection’s name and other fields and select or clear the **Share connection with all users** checkbox. 

## How to use the Amazon RedShift Integration

Once your integration is set up, you can measure your OKR progress by connecting your new or existing OKRs with an Amazon Redshift dataset.  

1. Select **Amazon Redshift** from the list of integrations available. If there are multiple connections listed, choose the connection that you would like to use. 

2. Next, add your query and validate the response. 

3. Select **Next** to finish and save your OKR. You’ll now see the Amazon Redshift icon next to the OKR‘s progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report.

> [!NOTE]
> Viva Goals will sync data from Amazon Redshift at every one-hour interval. 

## How to disable the RedShift integration

The Amazon Redshift integration can be disabled by an Admin at any time. To disable the integration go to Amazon Redshift in the Integrations section. Select Amazon Redshift and select Manage. On the configurations page, select the **Change dropdown**, select **Disable** and confirm the action.

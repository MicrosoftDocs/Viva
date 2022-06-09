---
title: MS SQL Server integration
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
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Keep track of your OKR progress by automating key updates from your MS SQL server database."
---

# MS SQL Server integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## About the MS SQL integration

The Viva Goals integration with MS SQL Server allows you to link your OKRs in Viva Goals to a server database in MS SQL and provides automatic, real-time updates on your objectives. 

For example, if you have an objective to increase visits and the time spent in your app by 60% then you can directly link this objective with the relevant data in MS SQL Server. Whenever there’s a change in the dataset and the database is updated, this data is automatically synced with  Viva Goals every hour and the OKR status updated.

All users and admins have access to this integration. Admins also have permissions to manage the integration from the admin dashboard.

## How to connect the MS SQLServer to your Viva Goals account

1. The first step in setting up the MS SQL integration is to connect your account to Viva Goals Navigate to your sidebar and select **Admin** and then select **Integrations**.

    :::image type="content" source="../media/goals/12/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/12/viva-goals-integrations-page.png":::

2. In the integrations section, go to MS SQL Server and then select **Enable** if this is the first time, or **Manage** if an integration has already been established.

    :::image type="content" source="../media/goals/12/sqlserver-enable-button.png" alt-text="Enabling MS SQL Server in Viva Goals." lightbox="../media/goals/12/sqlserver-enable-button.png":::

3. Select **New Connection** and in the pop-up dialog box, name your connection, give your MS SQL Server hostname, port, user, password, and add the database you'd like to connect to authenticate the connection. 

    :::image type="content" source="../media/goals/12/sqlserver-configure-new-connection.png" alt-text="Configuring a new MS SQL Server connection in Viva goals." lightbox="../media/goals/12/sqlserver-configure-new-connection.png":::

    > [!NOTE]
    > Viva Goals uses **SQL authentication** to create an integration connection.

4. Then select **Next** to complete the new connection setup. 

## How to edit an existing connection

Admins can edit an existing connection’s name and shared state that you’ve created from the MS SQL Server integration’s view. 

Select the **Edit** icon next to the MS SQL connection.  In the pop-up dialog box that follows, you can edit the connection’s name and other fields and **select** or clear the **Share connection with all users** checkboxes.

## How to use the MS SQL Server integration

Once your integration is set up, you can measure your OKRs progress by connecting your new or existing OKRs with an MS SQL server database.  

1. Select **MS SQL Server** from the list of integrations available. If there are multiple connections listed, choose the connection that you would like to use. 

    :::image type="content" source="../media/goals/12/sqlserver-datasource.png" alt-text="Selecting MS SQL Server from the list of data sources in Viva Goals." lightbox="../media/goals/12/sqlserver-datasource.png":::

2. Next, choose your query type. You can choose to add your query directly by selecting the **SQL Query** option or choose the **Stored Procedure** to add in a stored procedure query from your end. 

    :::image type="content" source="../media/goals/12/sqlserver-connection-details.png" alt-text="Adding new MS SQL Server connection to OKRs in Viva goals." lightbox="../media/goals/12/sqlserver-connection-details.png":::

3. Next, add your query and validate the response. 

4. Select **Next** to finish and save your OKR. You’ll now see the MS SQL Server icon next to the OKR‘s progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report. 

## How to disable the integration

The MS SQL Server can be disabled by an admin at any time. To disable the integration, go to MS SQL in the Integrations section. Select MS SQL Server in the integrations section and select **Manage**. In the configurations page, select the Change dropdown, select **Disable and confirm the action**. 

:::image type="content" source="../media/goals/12/sqlserver-disable-button.png" alt-text="Disabling MS SQL Server in Viva Goals." lightbox="../media/goals/12/sqlserver-disable-button.png":::

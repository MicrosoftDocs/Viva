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
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Keep track of your OKR progress by automating key updates from your MS SQL server database."
---

# MS SQL Server integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Who can use this feature?

All Users and Admins (Admins also have permissions to manage the integration from the admin dashboard)

## About the MS SQL integration

Viva Goals’ Integration with MS SQL Server allows you to link your OKRs in Viva Goals to a server database in MS SQL and provides automatic, real-time updates on your objectives. For example, if you have an objective to increase visits and the time spent in your app by 60% then you can directly link this objective with the relevant data in MS SQL Server. Whenever there’s a change in the dataset and the database is updated, this data is automatically synced with  Viva Goals every hour and the OKR status updated.

## Set up

## Connect MS SQLServer to your Viva Goals account

1. The first step in setting up the MS SQL integration is to connect your account to Viva Goals Navigate to your sidebar and select **Admin** and then select **Integrations**.

2. In the integrations section, go to MS SQL Server and then select **Manage**. 

    :::image type="content" source="../media/goals/goals-creating-ms-sql-conn.gif" alt-text="Image of SQL integrations section":::

3. Select **New Connection** and in the pop-up dialog box, name your connection, give your MS SQL Server hostname, port, user, password, and add the database you'd like to connect to authenticate the connection. 

    > [!NOTE]
    > Viva Goals uses **SQL authentication** to create an integration connection.

    :::image type="content" source="../media/goals/goals-ms-sql-connection-screen.png" alt-text="Image of SQL authentication":::

4. Then select **Next** to complete the new connection setup. 

    :::image type="content" source="../media/goals/goals-ms-sql-connection-complete.png" alt-text="Image of complete connection set up":::

## Edit an existing connection

Admins can edit an existing connection’s name and shared state that you’ve created from the MS SQL Server integration’s view. 

Select the **Edit** icon next to the MS SQL connection.  In the pop-up dialog box that follows, you can edit the connection’s name and other fields and **select** or clear the **Share connection with all users** checkboxes.

:::image type="content" source="../media/goals/goals-edit-ms-sql-conn.gif" alt-text="Image of edit an existing connection "::: 

## Using the MS SQL Server Integration

Once your integration is set up, you can measure your OKRs progress by connecting your new or existing OKRs with an MS SQL server database.  

1. Select **MS SQL Server** from the list of integrations available. If there are multiple connections listed, choose the connection that you would like to use. 

2. Next, choose your query type. You can choose to add your query directly by selecting the **SQL Query** option or choose the **Stored Procedure** to add in a stored procedure query from your end. 

    :::image type="content" source="../media/goals/goals-using-ms-sql-server-integration.png" alt-text="Image of using the MS SQL server integration ":::

3. Next, add your query and validate the response. 

4. Select **Next** to finish and save your OKR. You’ll now see the MS SQL Server icon next to the OKR‘s progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report. 

    :::image type="content" source="../media/goals/goals-add-query-sql-conn.gif" alt-text="Image of add your query and validate the response":::

> [!NOTE]
> -  Viva Goals will sync data from your MS SQL Server at every one-hour interval.
> -  If your MS SQL Server is behind a firewall, you will have to add the following IPs to the allowlist:<p>
>     54.243.192.208 <p>
>     3.225.237.0 <p>
>     107.20.38.17 <p>
>     23.21.1.160     

## Disabling the integration

The MS SQL Server may also be disabled by an Admin at any time. To disable the integration, as an Admin go to MS SQL in the Integrations section. Select MS SQL Server in the integrations section and select **Manage**. In the configurations page, select the Change dropdown, select **Disable and confirm the action**. 

:::image type="content" source="../media/goals/goals-delete-ms-sql-conn.gif" alt-text="Image of disabling the integration"::: 


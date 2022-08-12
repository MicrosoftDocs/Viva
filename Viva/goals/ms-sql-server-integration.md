---
title: Microsoft SQL Server integration
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

# Microsoft SQL Server integration

## About the MS SQL integration

Viva Goals integration with Microsoft SQL Server lets you link your OKRs in Viva Goals to a server database in Microsoft SQL Server and provides automatic, real-time updates on your objectives. 

For example, if you have an objective to increase visits and the time spent in your app by 60 percent, directly link this objective with the relevant data in SQL Server. Whenever there's a change in the dataset and the database is updated, this data is automatically synced with Viva Goals every hour, and the OKR status updated.

All users and admins have access to this integration. Admins also have permissions to manage the integration from the admin dashboard.

## How to connect Microsoft SQLServer to your Viva Goals account

1. The first step to set up the Microsoft SQL integration is to connect your account to Viva Goals. Go to the sidebar and select **Admin** and then select **Integrations**.

    :::image type="content" source="../media/goals/12/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/12/viva-goals-integrations-page.png":::

2. In the **Integrations** section, go to **MS SQL Server** and then select **Enable** if this is the first time, or select **Manage** if the integration was previously established.

    :::image type="content" source="../media/goals/12/sqlserver-enable-button.png" alt-text="Enabling MS SQL Server in Viva Goals." lightbox="../media/goals/12/sqlserver-enable-button.png":::

3. Select **New Connection**. In the pop-up dialog, name your connection; enter your Microsoft SQL Server hostname, port, user, and password; and enter the database you want like to connect to authenticate the connection. 

    :::image type="content" source="../media/goals/12/sqlserver-configure-new-connection.png" alt-text="Screenshot shows where you configure a new SQL Server connection in Viva goals." lightbox="../media/goals/12/sqlserver-configure-new-connection.png":::

    > [!NOTE]
    > Viva Goals uses **SQL authentication** to create an integration connection.

4. Select **Next** to complete connection setup. 

## How to edit an existing connection

Admins can edit an existing connection's name and shared state that you created from the MS SQL Server integration view: 

Select the **Edit** icon next to the MS SQL connection.  In the pop-up dialog box that appears, you can edit the connection’s name and other fields and **select** or clear the **Share connection with all users** checkbox.

## How to use the SQL Server integration

after your integration is set up, you can measure your OKR progress by connecting your OKRs with a Microsoft SQL Server database.  

1. Select **MS SQL Server** from the list of integrations available. If there are multiple connections listed, choose the connection that you want to use. 

    :::image type="content" source="../media/goals/12/sqlserver-datasource.png" alt-text="Screenshot shows where you select SQL Server from the list of data sources in Viva Goals." lightbox="../media/goals/12/sqlserver-datasource.png":::

2. Next, choose your query type. To add your query directly, select the **SQL Query** option. Or choose the **Stored Procedure** to add a stored procedure query. 

    :::image type="content" source="../media/goals/12/sqlserver-connection-details.png" alt-text="Screenshot shows where you add a new  SQL Server connection to OKRs in Viva goals." lightbox="../media/goals/12/sqlserver-connection-details.png":::

3. Next, add your query and validate the response. 

4. Select **Next** to finish and save your OKR. You'll now see the MS SQL Server icon next to the OKR's progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report. 

## How to disable the integration

Microsoft SQL Server integrations can be disabled by an admin at any time. To disable the integration, go to **MS SQL** in the **Integrations** section. Select **Manage**. On the configurations page, select the **Change** dropdown, select **Disable** and then confirm. 

:::image type="content" source="../media/goals/12/sqlserver-disable-button.png" alt-text="Screenshot shows how you disable MS SQL Server in Viva Goals." lightbox="../media/goals/12/sqlserver-disable-button.png":::

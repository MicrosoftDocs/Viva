---
ms.date: 04/18/2022
title: "MySQL integration"
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals
- vg-integration
search.appverid:
- MET150

description: "Learn how to integrate your MySQL database with OKRs in Viva Goals."
---

# MySQL integration

## Introduction to MySQL integration

The Viva Goals MySQL integration lets you update your objectives and key result (OKR) progress automatically based on data in your MySQL database. 

Let's consider this example: You use MySQL databases to store information on leads from multiple sources. You have an objective in Viva Goals to increase qualified leads by 40 percent every quarter. When you link this objective to the corresponding database in MySQL, the status of your OKR will be updated based on the data in your database. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.

## How to enable the MySQL integration

Admins follow these steps to enable this integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
  
    :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

2. Against **MySQL**, select the option to **Enable** the integration. If a connection was made previously or if the integration was already enabled, you can **Manage** the integration.
  
    :::image type="content" source="../media/goals/10/mysql-enable-button.png" alt-text="Screenshot shows where you enable MySQL in Viva Goals." lightbox="../media/goals/10/mysql-enable-button.png":::

3. This integration can also be disabled from the same section: Go to **Change** and select **Disable integration** from the dropdown.
  
    :::image type="content" source="../media/goals/10/mysql-disable-button.png" alt-text="Screenshot shows how to disable MySQL in Viva Goals." lightbox="../media/goals/10/mysql-disable-button.png":::

## How to configure the MySQL connection

After you enable the integration, the first step is to configure a MySQL connection:

1. Select **New Connection**, and provide a **Connection Name**.
  
    :::image type="content" source="../media/goals/10/mysql-new-connection-button.png" alt-text="Screenshot shows where you choose to add a new MySQL connection in Viva Goals." lightbox="../media/goals/10/mysql-new-connection-button.png"::: 

1. Provide the **Hostname/IP address** of the database server and the **Port** number that the server is listening on.
  
    :::image type="content" source="../media/goals/10/mysql-configure-new-connection.png" alt-text="Screenshot shows where you configure your new MySQL connection in Viva Goals." lightbox="../media/goals/10/mysql-configure-new-connection.png":::

1. Enter **User** and **Password** details. After authentication, the associated databases will be populated automatically. Select your **Database** from the dropdown menu.

1. Optionally, share this connection with other users in the organization. 

1. Select **Next** to get this integration running. You can edit the saved connection at any time.

Viva Goals allows you to connect with multiple databases. Select **New Connection** to connect to another database. Differentiate these connections by name. The names will be displayed to other users when they link their OKRs with MySQL databases.

## How to connect the MySQL connection to an OKR

After you configure the connection, the next step is to link OKRs to your MySQL databases.

1. When you create or edit an OKR, select **Connect data source to auto-update progress**. From the drop-down menu, select **MySQL**.
  
    :::image type="content" source="../media/goals/10/mysql-datasource.png" alt-text="Screenshot shows where you select MySQL as your data source." lightbox="../media/goals/10/mysql-datasource.png":::

2. If you already created a connection, or if your admin shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

3. Select the method you want to use to measure progress, **percent complete** or **KPI (success metric)**. If you choose KPI, provide a metric, starting value, and target value.

4. Select a connection, and provide the **MySQL query**. This query will return a single numeric value, and this value will be tied to OKR progress.
  
    :::image type="content" source="../media/goals/10/mysql-connection-details.png" alt-text="Screenshot shows where you specify a query and query type for your new MySQL connection." lightbox="../media/goals/10/mysql-connection-details.png":::

5. Validate the query by using the query result.

6. Go to **Next** > **Save**. You should see the MySQL icon right next to your OKR. Sync occurs every hour. To manually initiate the sync, select the MySQL icon, and then the refresh icon.

You've now linked your objective to a database in MySQL to update the status of the corresponding OKR automatically based on the data present in the connected database.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 to 25 percent less than the expected progress at any point in time, the OKR status is *behind*, and the progress bar will be orange.

- If the progress is more than 25 percent less than the expected progress at any point, the OKR status is *at risk*, and the progress bar will be red.


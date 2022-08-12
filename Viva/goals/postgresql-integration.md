---
title: PostgreSQL integration
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
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to integrate your PostgreSQL database with OKRs in Viva Goals."
---

# PostgreSQL integration

Viva Goals PostgreSQL integration lets you update your OKR progress automatically based the data fetched from your PostgreSQL database. 

Let's consider this example: You use PostgreSQL databases to store information on leads from multiple sources. You have an objective in Viva Goals to increasing the number of qualified leads by 40 percent every quarter. When you link this objective to the corresponding database in PostgreSQL, the status of your OKR will be updated based on the data in your database. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current. 

## How to enable PostgreSQL integration

Admins follow these steps to enable this integration: 

1. From the sidebar, select **Admin > Integrations** tab. 

    :::image type="content" source="../media/goals/11/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/11/viva-goals-integrations-page.png":::

2. In **PostgreSQL**, you will have an option to **Enable** the integration. If a connection was made previously or if the integration was already enabled, you'll have the option to **Manage** the enabled integration. 

    :::image type="content" source="../media/goals/11/postgres-enable-button.png" alt-text="Screenshot shows where to enabling PostgreSQL in Viva Goals." lightbox="../media/goals/11/postgres-enable-button.png":::

3. This integration can also be disabled from the same section: Selecting **Change**, and then choose **Disable integration** from the dropdown. 

    :::image type="content" source="../media/goals/11/postgres-disable-button.png" alt-text="Screenshot shows how to disable PostgreSQL in Viva Goals." lightbox="../media/goals/11/postgres-disable-button.png":::

## How to configure the PostgreSQL connection 

After you enable the integration, the first step is to configure a PostgreSQL connection:

1. Select **New Connection**, and provide a **name for the connection**. 

    :::image type="content" source="../media/goals/11/postgres-new-connection-button.png" alt-text="Screenshot shows where you adding a new PostgreSQL connection in Viva Goals." lightbox="../media/goals/11/postgres-new-connection-button.png":::

1. Provide the **hostname or IP address** of the database server and the **port number** that the server is listening on. 

    :::image type="content" source="../media/goals/11/postgres-configure-new-connection.png" alt-text="Screenshot shows where you configuring a new PostgreSQL connection." lightbox="../media/goals/11/postgres-configure-new-connection.png":::

1. Provide the **username and password**. Upon authentication, the associated databases will be populated automatically. **Choose your database** from the dropdown menu. 

1. Optionally, share this connection with other users in the organization.

1.  Select **Next** to get up and running with this integration. You can edit the saved connection at any time. 

Viva Goals allows you to connect with multiple databases. Select **New Connection** to connect to another database. You differentiate these connections by name. The names a redisplayed to other users when they link their OKRs with PostgreSQL databases.

## How to connect the PostgreSQL connection to an OKR

After you configure the connection, the next step is link OKRs to the PostgreSQL databases: 

1. When you create or edit an OKR, select **Automatically from a data source** to Microsoft AutoUpdate progress. From the drop-down menu, select **PostgreSQL**. 

    :::image type="content" source="../media/goals/11/postgresql-datasource.png" alt-text="Screenshot shows where you select PostgreSQL from the list of data sources in Viva Goals." lightbox="../media/goals/11/postgresql-datasource.png":::

2. If you already created a connection or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if no connections were previously created or shared. 

3. Choose the method that you want to use to measure progress, **percent complete** or **KPI** (success metric). If you choose KPI, provide a metric, starting value, and target value.

4. Select a **connection** and provide the **PostgreSQL query**. This query will return a single numeric value, and this value will be tied to the OKR progress.

    :::image type="content" source="../media/goals/11/postgresql-connection-details.png" alt-text="Screenshot shows where you add a new PostgreSQL connection to OKRs in Viva goals." lightbox="../media/goals/11/postgresql-connection-details.png":::

5. **Validate** the query by using the **Query Result**.

6. Select **Next** > **Save**. You should be able to see the PostgreSQL icon next to your OKR. The sync happens once every hour. You can also select the PostgreSQL icon and then the refresh icon to initiate a manual sync.

You've  linked your objective to a database in PostgreSQL to update the status of the corresponding OKR automatically based on the data present in the connected database. 

The colors of the progress bar indicated the status of the objective:

- If the progress is 0 to 25 percent less than expected at any point in time, the OKR status is *behind*, and the progress bar color will be orange. 

- If the progress is more than 25 percent less than expected progress at any point in time, the OKR status is *at risk*, and the progress bar color will be red. 

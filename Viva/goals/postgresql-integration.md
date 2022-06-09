---
title: PostgreSQL Integration
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
description: "Learn how to integrate your PostgreSQL database with OKRs in Viva Goals."
---

# PostgreSQL integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

The Viva Goals PostgreSQL integration allows you to update your OKR progress automatically depending on the data fetched from your PostgreSQL database. 

Let’s take this example: you use PostgreSQL databases to store information on leads from multiple sources. You also have an objective in Viva Goals for increasing the number of qualified leads by 40% every quarter. When you link this objective to the corresponding database in PostgreSQL, the status of your OKR will be updated based on the data in your database. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current. 

## How to enable the PostgreSQL integration

Admins can enable this integration, and here’s how it can be done: 

1. From the sidebar, select **Admin >** select the **Integrations** tab. 

    :::image type="content" source="../media/goals/11/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/11/viva-goals-integrations-page.png":::

2. In **PostgreSQL**, you will have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled, you'll have the option to **Manage** the enabled integration. 

    :::image type="content" source="../media/goals/11/postgres-enable-button.png" alt-text="Enabling PostgreSQL in Viva Goals." lightbox="../media/goals/11/postgres-enable-button.png":::

3. This integration can also be disabled from the same section by selecting **Change**, and choosing **Disable integration** from the dropdown. 

    :::image type="content" source="../media/goals/11/postgres-disable-button.png" alt-text="Disabling PostgreSQL in Viva Goals." lightbox="../media/goals/11/postgres-disable-button.png":::

## How to configure the PostgreSQL connection 

1. After enabling the integration, the first step is to configure a PostgreSQL connection. 

2. Select **New Connection**, and provide a **name for the connection**. 

    :::image type="content" source="../media/goals/11/postgres-new-connection-button.png" alt-text="Adding a new PostgreSQL connection in Viva Goals." lightbox="../media/goals/11/postgres-new-connection-button.png":::

3. Provide the **hostname or IP address** of the database server, the **port number** that the server is listening on. 

    :::image type="content" source="../media/goals/11/postgres-configure-new-connection.png" alt-text="Configuring a new PostgreSQL connection in Viva goals." lightbox="../media/goals/11/postgres-configure-new-connection.png":::

4. Provide the **username and password**. Upon authentication, the associated databases will be populated automatically. **Choose your database** from the dropdown menu. 

5. It is optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time. 

Viva Goals allows you to connect with multiple databases. Select **New Connection** to connect to another database. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with PostgreSQL databases. 

## How to connect the PostgreSQL connection to an OKR

Once you have configured the connection, the next step is to start linking OKRs to the PostgreSQL databases. 

1. While creating or editing an OKR, select **Automatically from a data source** to auto-update progress. From the drop-down menu, select **PostgreSQL**. 

    :::image type="content" source="../media/goals/11/postgresql-datasource.png" alt-text="Selecting PostgreSQL from the list of data sources in Viva Goals." lightbox="../media/goals/11/postgresql-datasource.png":::

2. If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared. 

3. Choose the method using which you want to measure the progress — **percent complete or KPI** (success metric). If you're choosing KPI, provide a metric, starting value, and target value. 

4. Select a **connection**, and provide the **PostgreSQL query**. This query will return a single numeric value, and this value will be tied to the OKR progress.

    :::image type="content" source="../media/goals/11/postgresql-connection-details.png" alt-text="Adding new PostgreSQL connection to OKRs in Viva goals." lightbox="../media/goals/11/postgresql-connection-details.png":::

5. **Validate** the query using the **Query Result**.

6. Select **Next > Save**. You should be able to see the PostgreSQL icon right next to your OKR. The sync happens once every hour. However, if you would like to initiate the sync manually, select the PostgreSQL icon, and select refresh icon.

You have successfully linked your objective to a database in PostgreSQL to update the status of the corresponding OKR automatically based on the data present in the connected database. 

The colors of the progress bar indicated the status of the objective. 

- If the progress is 0 - 25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange. 

- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red. 

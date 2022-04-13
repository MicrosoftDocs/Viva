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

# Introduction to PostgreSQL integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals’ PostgreSQL integration allows you to update your OKR progress automatically depending on the data fetched from your PostgreSQL database. Let’s say you use PostgreSQL databases to store information  on the number of leads that is garnered from multiple sources, and you have an objective in Viva Goals for increasing the number of qualified leads by 40% every quarter. When you link this objective to the corresponding database in PostgreSQL, the status of your OKR will be updated based on the data in your database. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current. 

## Enabling the PostgreSQL integration

Admins can enable this integration, and here’s how it can be done: 

- From the sidebar, select **Admin >** select the **Integrations** tab. 

- Against **PostgreSQL**, you'll have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled, you'll have the option to **Manage** the enabled integration. 

- This integration can also be disabled from the same section by selecting **Change**, and choosing **Disable integration** from the dropdown. 

## Configuring the PostgreSQL connection 

- After enabling the integration, the first step is to configure a PostgreSQL connection. 

- Select **New Connection**, and provide a **name for the connection**. 

- Provide the **hostname or IP address** of the database server, the **port number** that the server is listening on. 

- Furnish the **username and password**. Upon authentication, the associated databases will be populated automatically. **Choose your database** from the dropdown menu. 

    > [!NOTE]
    > It is recommended to create a new user/role with read-only permissions to specific databases that will be connected to the objectives in [Viva Goals](https://ally.io/) for enhanced security.

- It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time. 

    :::image type="content" source="../media/goals/goals-configuring-the-postgreSQL-connection.gif" alt-text="Image of Configuring the PostgreSQL connection":::

Viva Goals allows you to connect with multiple databases. Select **New Connection** to connect to another database. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with PostgreSQL databases. 

## Connecting the PostgreSQL connection to an OKR

Once you've configured the connection, the next step is to start linking OKRs to the PostgreSQL databases. 

- While creating or editing an OKR, select **Connect data source to auto-update progress**. From the drop-down menu, select **PostgreSQL**. 

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared. 

- Choose the method using which you want to measure the progress — **percent complete or KPI** (success metric). If you're choosing KPI, provide a metric, starting value, and target value. 

- Select a **connection**, and provide the **PostgreSQL query**. This query will return a single numeric value, and this value will be tied to the OKR progress.

- **Validate** the query using the **Query Result**.

- Select **Next > Save**. You should be able to see the PostgreSQL icon right next to your OKR. The sync happens once every hour, however, if you would like to initiate the sync manually, select the PostgreSQL icon, and select refresh icon.

    :::image type="content" source="../media/goals/goals-connecting-postgresql-connection-to-an-okr.gif" alt-text="Image of connecting the PostgreSQL connection"::: 

You've successfully linked your objective to a database in PostgreSQL to update the status of the corresponding OKR automatically based on the data present in the connected database. 

The colors of the progress bar indicated the status of the objective. 

- If the progress is 0 - 25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange. 

- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red. 

To learn more about Viva Goals other integrations, please visit our [Integrations page](https://help.ally.io/en/collections/30526-integrations). 
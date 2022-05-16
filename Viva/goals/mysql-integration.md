---
title: "MySQL Integration"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
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

description: "Learn how to integrate your MySQL database with OKRs in Viva Goals."
---

# MySQL Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to MySQL integration

The Viva Goals MySQL integration allows you to update your Objectives and Key Results (OKR) progress automatically depending on the data fetched from your MySQL database. 

Let's take this example: you use MySQL databases to store information on leads from multiple sources. You also have an objective in Viva Goals for increasing the number of qualified leads by 40% every quarter. When you link this objective to the corresponding database in MySQL, the status of your OKR will be updated based on the data in your database. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## How to enable the MySQL integration

Admins can perform the following steps to enable this integration:

- From the sidebar, go to **Admin** and select the **Integrations** tab.

- Against **MySQL**, you'll have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled, you'll have the option to **Manage** the enabled integration.

- This integration can also be disabled from the same section. Go to **Change** and select **Disable integration** from the dropdown to disable this integration.

## How to configure the MySQL connection?

- After you enable the integration, the first step is to configure a MySQL connection.

- Select **New Connection**, and provide a **Connection Name**.

- Provide the **Hostname/IP address** of the database server, the **Port** number that the server is listening on.

- Furnish the **User** and **Password** details. Upon authentication, the associated databases will be populated automatically. Select your **Database** from the dropdown menu.

- It is optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

Viva Goals allows you to connect with multiple databases. Select **New Connection** to connect to another database. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with MySQL databases.

## How to connect the MySQL connection to an OKR

Once you have configured the connection, the next step is to start linking OKRs to the MySQL databases.

- While creating or editing an OKR, select **Connect data source to auto-update progress**. From the drop-down menu, select **MySQL**.

- If you have already created a connection, or if your admin has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Select the method using which you want to measure the progress — **percent complete** or **KPI (success metric)**. If you're choosing key performance indicator (KPI), provide a metric, starting value, and target value.

- Select a connection, and provide the **MySQL query**. This query will return a single numeric value, and this value will be tied to the OKR progress.

- Validate the query using the query result.

- Go to **Next > Save**. You should be able to see the MySQL icon right next to your OKR. The sync happens once every hour, however, if you would like to initiate the sync manually, select the MySQL icon, and select the refresh icon.

You have now successfully linked your objective to a database in MySQL to update the status of the corresponding OKR automatically based on the data present in the connected database.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 - 25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange.

- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red.

---
title: Snowflake integration
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
description: "Learn how to integrate your Viva Goals OKRs with Data in Snowflake."
---

# Snowflake integration

Viva Goals can integrate with Snowflake to automatically update your OKRs. 

Let's consider this example: You have data in your Snowflake warehouse to track leads generated across multiple channels. Your goal is to generate 4000 qualified leads from SEO By implementing a Snowflake integration. You can save yourself the hassle of going back and forth between Snowflake and Viva Goals to update your progress. Viva Goals will sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.

## How to set up the Snowflake integration 

An admin follows these steps to set up the Snowflake integration in Viva Goals: 

1. Go to the Viva Goals integrations page at **Admin** > **Integrations**.

    :::image type="content" source="../media/goals/6/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/6/viva-goals-integrations-page.png":::

2. Scroll through the integration options to locate **Snowflake**. Select **enable** if this is the first time or select **manage** if an integration was previously established.

    :::image type="content" source="../media/goals/6/snowflake-enable-button.png" alt-text="Screenshot shows where you enable Snowflake in Viva Goals." lightbox="../media/goals/6/snowflake-enable-button.png":::

3. Select **New Connection**. In the dialog that appears, enter the connection name, account URL, user name, password, and warehouse. The warehouses list should populate automatically to choose among if the credentials you entered are correct.

    :::image type="content" source="../media/goals/6/snowflake-configure-new-connection.png" alt-text="Screenshot shows where you create a new Snowflake connection in Viva Goals." lightbox="../media/goals/6/snowflake-configure-new-connection.png":::

4. Select **Next** to finish setup.

Viva Goals lets you connect with multiple Snowflake warehouses. Select **New connection** to add another. You differentiate them by name. These names are displayed to members when they link their OKRs to Snowflake data.

## How to use the Snowflake integration

Once setup is complete, users in your organization can link the success of their OKRs directly to the data inside a Snowflake warehouse.

1. When you create (or edit) an objective or key result, select **Connect data source to auto-update progress**.
2. From the list of integrations, pick **Snowflake**.

    :::image type="content" source="../media/goals/6/snowflake-datasource.png" alt-text="Screenshot shows where you select Snowflake from the list of data sources." lightbox="../media/goals/6/snowflake-datasource.png":::

3. If you already created a Snowflake connection, or an administrator in your organization shared a Snowflake connection with you, that connection will be automatically selected for you. If there are no connections previously created or shared, Viva Goals will prompt you to add a new connection.
4. Add the Snowflake SQL query that will return a single-valued numeric value. This value will be connected to the OKR's progress or KPI depending on how the OKR is measured.

    :::image type="content" source="../media/goals/6/snowflake-connection-details.png" alt-text="Screenshot shows where you add a Snowflake connection to your OKRs in Viva goals.png." lightbox="../media/goals/6/snowflake-connection-details.png":::

5. Select **next** to finish and save your OKR. You should now see a Snowflake icon next to the OKR. The OKR will sync automatically every hour. You can also select **refresh** to refresh it manually.

The colors of the progress bars indicate the status of the objective.

 - If the progress is 0 to 25 percent less than expected at any point in time, the status is *behind* (orange).
 - If the progress is more than 25 less than expected at any point in time, the status is *at-risk* (red).

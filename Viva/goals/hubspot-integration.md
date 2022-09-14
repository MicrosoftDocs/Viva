---
title: "Hubspot Integration"
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
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to base your OKR progress in Viva Goals by connecting with significant HubSpot metrics."
---

# Hubspot integration

## About HubSpot integration
    
Viva Goals HubSpot integration enables you to link objectives and key results (OKRs) to HubSpot sales and marketing metrics for automatic real-time updates on progress. 

Let's use this example: You have an objective to increase the number of marketing qualified leads (MQLs) this quarter. You can use HubSpot integration to save yourself the hassle of going back and forth between HubSpot and Viva Goals to update progress. Viva Goals will sync values for you, saving time while keeping your OKRs current.
    
All users and admins can use the HubSpot integration. Admins also have permissions to manage the integration from the admin dashboard.

## How to connect HubSpot to your Viva Goals account

1. Go to the Viva Goals integrations page at **Admin** > **Integrations**.  
    
    :::image type="content" source="../media/goals/7/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/7/viva-goals-integrations-page.png":::

2. In the **Integrations** section, go to **Hubspot**, and then select **Manage**.

    :::image type="content" source="../media/goals/7/hubspot-manage-button-in-viva-goals.png" alt-text="Screenshot shows where you choose to manage Hubspot in Viva Goals." lightbox="../media/goals/7/viva-goals-integrations-page.png":::

3. Select **New Connection**. In the dialog that opens, sign in to your Hubspot account.
    
    :::image type="content" source="../media/goals/7/hubspot-new-connection-button-in-viva-goals.png" alt-text="Screenshot shows where you choose to create a new Hubspot connection in Viva Goals." lightbox="../media/goals/7/hubspot-new-connection-button-in-viva-goals.png":::

4. Name your connection and select **Next** to complete setup.
    
    :::image type="content" source="../media/goals/7/creating-a-new-hubpot-connection.png" alt-text="Screenshot shows where you enter Hubspot connection details in Viva Goals." lightbox="../media/goals/7/creating-a-new-hubpot-connection.png":::

5. Viva Goals lets you connect with multiple Hubspot accounts. Select **New connection** to add another instance. You use names to differentiate connections. The names are displayed to members when they link their OKRs to Hubspot.

## How to edit an existing Hubspot connection

Admins can also edit an existing Hubspot connection, including the integration’s name and shared state  from the Hubspot integration view: 

1. Start in the **Integrations** section in the Admin Dashboard. Select **Hubspot**.  

2. Select the **Edit** icon next to the Hubspot connection. In the dialog box that appears, you can edit the **Connection Name** and select or clear the **Share connection with all users** checkbox.

## How to use Hubspot integration

Now that the integration is enabled, your team can link a Hubspot metric with an OKR:

1. When you add or edit an objective or key result, you can choose to measure progress by **KPI** or **% complete**. Select **HubSpot** from the list of integrations available.
    
    :::image type="content" source="../media/goals/7/hubspot-integrations-in-the-list-of-datasources-in-viva-goals.png" alt-text="Screenshot shows where you select Hubspot as your data source." lightbox="../media/goals/7/hubspot-integrations-in-the-list-of-datasources-in-viva-goals.png":::

2. Create or select a connection. If multiple connections are listed, select the connection that you want to use.
    
    :::image type="content" source="../media/goals/7/hubspot-multiple-connections-in-viva-goals.png" alt-text="Screenshot shows where you select a Hubspot connection from multiple connections available in Viva goals.png." lightbox="../media/goals/7/hubspot-multiple-connections-in-viva-goals.png":::

3. Select the product type that you want to integrate with. Currently, Viva Goals integrates with Marketing Hub and Sales Hub.
    
    :::image type="content" source="../media/goals/7/hubspot-new-connection-details-in-viva-goals.png" alt-text="Screenshot shows where you select a Hubspot product type." lightbox="../media/goals/7/hubspot-new-connection-details-in-viva-goals.png":::

    > [!NOTE]
    > If you select **Sales Hub** as the product type, addition fields become available, including **Pipeline**, **Stage**, **Owner**, and **Team**.

    **HubSpot Marketing Hub metrics you can track in Viva Goals**

    | HubSpot Marketing Hub metrics | OKR progress type (KPI, % complete) |
    |---------|---------|
    | % New sessions | KPI, % complete |
    | % Session to contact | KPI, % complete |
    | % Contact to customer | KPI, % complete |
    | % Bounce rate | KPI, % complete |
    | Average page views per session | KPI |
    | Number of contacts | KPI |
    | Number of customers | KPI |
    | Number of leads | KPI |
    | Number of MQLs | KPI |
    | Number of opportunities | KPI |
    | Number of raw views | KPI |
    | Number of SQLs | KPI |
    | Number of subscribers | KPI |
    | Number of visitors | KPI |
    | Number of visits | KPI |
    | Time per session (in seconds) | KPI |

    **HubSpot Sales Hub Metrics that you can track in Viva Goals**

    | % complete OKRs | OKR progress type (KPI, % complete) |
    |---------|---------|
    | % deals closed (close ratio) | KPI, % complete |
    | % deals won (win rate) | KPI, % complete |
    | Average deal size | KPI |
    | Average number of activities | KPI |
    | Average sales cycle in days (lost) | KPI |
    | Average sales cycle in days (won & lost) | KPI |
    | Average sales cycle in days (won) | KPI |
    | Number of deals | KPI |
    | Sales velocity | KPI |
    | Total deal value | KPI |
    | Total number of activities | KPI |

    In the following example, we count the number of marketing qualified leads in HubSpot in the specified time period.

4. Select **Next** to finish and save your OKR. You should now see a HubSpot icon next to the OKR. Viva Goals will now automatically count marketing qualified leads. The OKR syncs automatically every hour. To refresh it manually select **refresh**.

> [!NOTE]
> Your access to Marketing Hub and Sales Hub metrics will depend on your HubSpot license.

### How to disable HubSpot integration 
The admin can disable Hubspot at any time: Go to **HubSpot** in the **Integrations** section and select **Manage**. On the **Hubspot Configurations** page, go to the **Change** dropdown, select **Disable**, and then confirm the action.
    
:::image type="content" source="../media/goals/7/disabling-hubspot-in-viva-goals.png" alt-text="Screenshot shows where you disable integration for Hubspot." lightbox="../media/goals/7/disabling-hubspot-in-viva-goals.png"::: 

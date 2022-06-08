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

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## About the HubSpot integration
    
The Viva Goals HubSpot integration allows you to link Objectives and Key Results (OKRs) to HubSpot Sales and Marketing metrics for automatic real-time updates on the progress. 

Let's take this example: you have an objective to increase the number of Marketing Qualified Leads(MQLs) this quarter. You can use the HubSpot integration to save yourself the hassle of going back and forth between HubSpot and Viva Goals to update progress. Viva Goals will sync values for you, saving time while keeping your OKRs current.
    
All users and admins can use the HubSpot integration. Admins also have permissions to manage the integration from the admin dashboard. 

## How to connect HubSpot to your Viva Goals account

1. Navigate to Viva Goals’ integrations page through **Admin > Integrations**.  

2. In the **Integrations** section, go to **Hubspot** and then select **Manage**.

    :::image type="content" source="../media/goals/hubspot-viva-goals-connection.gif" alt-text="Hubspot Integration 1":::

3. Select **New Connection** and in the popup that follows, sign into your Hubspot account.

4. Name your connection and select **Next** to complete the setup.

5. Viva Goals allows you to connect with multiple Hubspot accounts. Select **New connection** to add another instance and use names to differentiate them. These names are displayed to members when they link their OKRs to Hubspot.

## How to edit an existing Hubspot connection

Admins can also edit an existing Hubspot connection, including the integration’s name and shared state that you’ve created, from the Hubspot integration’s view. 

1. Start in the **Integrations** section in the Admin Dashboard and select **Hubspot**.  

2. Select the **Edit** icon next to the Hubspot connection. In the pop-up dialog box that displays, you can edit the **Connection Name** and select or clear the **Share connection with all users** checkbox.

## How to use the Hubspot Integration

Now that the integration is enabled, your team can link a Hubspot metric with an OKR.

1. While adding or editing an Objective or Key Result, you should choose to measure progress by **KPI** or **% complete**. Select HubSpot from the list of integrations available.

2. Create a connection or select the connection. If there are multiple connections listed, select the connection that you would like to use.

3. Select the product type you’d like to integrate with. Currently, Viva Goals integrates with Marketing Hub and Sales Hub.

    > [!NOTE]
    > If you select **Sales Hub** as the Product Type, there’re a couple of additional fields such as **Pipeline**, **Stage**, **Owner**, and **Team**.

    **HubSpot Marketing Hub Metrics that you can track in Viva Goals**

    | HubSpot Marketing Hub Metrics | OKR Progress Type (KPI, % Complete) |
    |---------|---------|
    | % New Sessions | KPI, % Complete |
    | % Session to Contact | KPI, % Complete |
    | % Contact to Customer | KPI, % Complete |
    | % Bounce Rate | KPI, % Complete |
    | Average page views per session | KPI |
    | Number of contacts | KPI |
    | Number of customers | KPI |
    | Number of leads | KPI |
    | Number of MQLs | KPI |
    | Number of Opportunities | KPI |
    | Number of Raw Views | KPI |
    | Number of SQLs | KPI |
    | Number of Subscribers | KPI |
    | Number of Visitors | KPI |
    | Number of Visits | KPI |
    | Time per session (in seconds) | KPI |

    **HubSpot Sales Hub Metrics that you can track in Viva Goals**

    | % Complete OKRs | OKR Progress Type (KPI, % Complete) |
    |---------|---------|
    | % Deals Closed (Close Ratio) | KPI, % Complete |
    | % Deals Won (Win Rate) | KPI, % Complete |
    | Average Deal Size | KPI |
    | Average Number of Activities | KPI |
    | Average Sales Cycle in Days (Lost) | KPI |
    | Average Sales Cycle in Days (Won & Lost) | KPI |
    | Average Sales Cycle in Days (Won) | KPI |
    | Number of Deals | KPI |
    | Sales Velocity | KPI |
    | Total Deal Value | KPI |
    | Total Number of Activities | KPI |

    In the following example, we're counting the number of Marketing Qualified Leads inside HubSpot between the specified time period.

4. Select **Next** to finish and save your OKR. You should now see a HubSpot icon next to the OKR - now Viva Goals will automatically count up the marketing qualified leads. The OKR syncs automatically every hour, but to refresh it manually select **refresh**.

> [!NOTE]
> Your access to Marketing hub and Sales hub metrics will depend on your HubSpot license.

### How to disable the HubSpot integration 

The Hubspot integration may also be disabled by an admin at any time. To disable the integration, go to HubSpot in the **Integrations** section and select **Manage**. In the **Hubspot Configurations** page, go to the **Change** dropdown, select **Disable** and confirm the action.

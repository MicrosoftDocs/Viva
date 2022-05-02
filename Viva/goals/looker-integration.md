---
title: "Looker Integration"
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

description: "Learn how to integrate your Looker KPIs with OKRs in Viva Goals."
---

# Looker Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals' Looker integration allows automated real-time tracking of Objectives and Key Results (OKR) progress. For example, you maintain the sales reports inside Looker dashboards and you have an objective to achieve a target of 50 Sales Demos within a specific time period. Using the Looker integration, you can set up a connection to an OKR in Viva Goals with a **demos booked** metric. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## How to enable the Looker Integration?

A Viva Goals Admin can perform the following steps to enable the Looker Integration in Viva Goals:

1. Navigate to Viva Goals’ integrations page through **Admin > Integrations**.

2. Scroll through the list until you reach Looker. Select **Enable** (Or **Manage** if a connection has been made previously).

3. The integration can also be disabled at any time from the same section.

## How to configure the Looker Connection?

In the **Connections** section, select **New Connection** and in the popup that appears, follow the prompt to enter the name of the connection and the Application Programming Interface (API) credentials provided to you by your Looker administrator. You can optionally choose to share the connection with other users in the organization and select **Save**. You can edit the saved connection anytime.

## How to connect the Looker Integration to an OKR?

Once the setup is complete, users in your organization can link their OKRs to Looker dashboards and looks.

1. While creating (or editing) an OKR, select **Connect data source to auto-update progress**.
  
2. From the list of integrations, select **Looker**.

    :::image type="content" source="../media/goals/viva-goals-looker-integration-1.png" alt-text="Looker Integration 1":::

3. If you already created a Looker connection or an administrator in your organization shared a Looker connection with you, that will automatically be selected. If there are no connections created or shared already, Viva Goals will prompt you to add a new connection. If you've more than one connection with Looker, you can choose the connection you’d like to use.

    > [!NOTE]
    > Looker Integration is available only for the **KPI (success metric)** method of measuring OKR success and not available for the **% completion** method.
  
4. Once the connection is selected, you can choose to **Track KPI from** either a dashboard or a look. Once you've chosen a dashboard or a look, you can further narrow it down to a specific dashboard tile or a look name. Select the tile or look that has the data you want to be connected to the OKR.

    :::image type="content" source="../media/goals/viva-goals-looker-integration-2.png" alt-text="Looker Integration 2":::

5. Select a key performance indicator (KPI) metric that is available from the selected tile or look. Depending on the type of visualization, there could be multiple values for the KPI, broken down by a dimension. For example, if you have the demos set up metric broken down by your sales team members as part of the Looker tile, you can choose to apply a metric/sum/average/count on the set of values (or) filter out by a particular person or any available filter field.

    :::image type="content" source="../media/goals/viva-goals-looker-integration-3.png" alt-text="Looker Integration 3":::

6. Viva Goals displays the selected value for your reference before you save the data link set-up.
  
7. Once you're satisfied, select **Save** and continue to save your OKR. You should now see a Looker icon next to the OKR. Viva Goals will automatically count up the finished number of demos setup. The OKR syncs automatically every hour, but to refresh it manually, you can go to the Looker icon and select the **Sync Now** option.

The following colors of the progress bar indicate the status of the Objective:

- If the progress is 0-25% less than expected progress at any point in time, the status is Behind (orange).

- If the progress is over 25% less than expected progress at any point in time, the status is At-Risk (red).

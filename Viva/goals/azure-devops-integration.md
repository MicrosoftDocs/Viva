---
title: Azure DevOps integration
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
description: "Learn how to integrate your work items with OKRs in Viva Goals"
---

# Azure DevOps integration

## Introduction to Azure DevOps integration

The Viva Goals Azure DevOps integration lets you update your OKR progress automatically based on the progress of work items in your Azure DevOps Projects. 

For example, say you use Azure DevOps to track the status of issues, and you have an objective in Viva Goals for resolving 30 issues every quarter. When you link your objective to the corresponding project in Azure DevOps, the status of your OKR will be updated as the work items under the associated project get resolved. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.


## How to enable Azure DevOps integration

Admins can follow these steps to enable this integration: 

1. In the sidebar, select on **Admin** and then select the **Integrations** tab. 

   :::image type="content" source="../media/goals/6/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/6/viva-goals-integrations-page.png":::

1.  Under Azure DevOps, you can **enable** the integration. If a connection was made previously or if the integration was already enabled, you'll see the option to **Manage** the integration. 

    :::image type="content" source="../media/goals/6/azure-devops-enable-button.png" alt-text="Enabling Azure DevOps in Viva Goals." lightbox="../media/goals/6/azure-devops-enable-button.png":::

    To dispable the integration from the same section, select **Change** and then select **Disable integration** from the dropdown.

    :::image type="content" source="../media/goals/6/azure-devops-disable-button.png" alt-text="Disabling Azure DevOps in Viva Goals." lightbox="../media/goals/6/azure-devops-disable-button.png":::

## How to configure the Azure DevOps connection 

After you enabling the integration, the first step is to configure an Azure DevOps connection: 

1. Select **New Connection**, and sign in to your Azure DevOps account. 

   :::image type="content" source="../media/goals/6/azure-devops-new-connection-button.png" alt-text="Screenshot shows where you create a new Azure DevOps connection in Viva goals.png." lightbox="../media/goals/6/azure-devops-new-connection-button.png":::

2. Provide a name for the connection, and furnish the **Account Name** and the **Project Name**. 

   :::image type="content" source="../media/goals/6/azure-devops-configure-new-connection.png" alt-text="Filling in details for the new Azure DevOps connection in Viva goals.png." lightbox="../media/goals/6/azure-devops-configure-new-connection.png":::

1. It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

   Viva Goals allows you to connect with multiple projects. Select **New Connection** to fetch data from another project. You differentiate these connections by name. The names will be displayed to other users when they link their OKRs with Azure DevOps data.

## How to connect the Azure DevOps connection to an OKR

Once you've configured the connection, the next step is to start linking OKRs to the Azure DevOps projects.

The option to connect to a data source will appear only for key results, not for objectives.

  :::image type="content" source="../media/goals/6/azure-devops-datasource.png" alt-text="Selecting Azure DevOps from the list of data sources in Viva goals.png." lightbox="../media/goals/6/azure-devops-datasource.png":::

1. If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared. 

1.  Choose the method you want to measure the progress—percent complete or KPI (success metric). If you choose KPI, provide a metric, starting value, and target value. 

1.  Select a connection, and choose the **Query**. As soon as you choose a query, the **count of matching work items** will be displayed. 

    :::image type="content" source="../media/goals/6/azure-devops-connection-details.png" alt-text="Adding Azure DevOps connection to your OKRs in Viva goals.png." lightbox="../media/goals/6/azure-devops-connection-details.png":::

    Progress will be calculated based on the count of tickets completed under the chosen query if you've chosen KPI metric to track progress. It will be calculated based on the percentage of tickets closed if you've chosen percent complete to track progress).

1. Click **Next > Save**.

You've now successfully linked your objective to a query in Azure DevOps to track the progress of your work items and automatically  update the status of the corresponding OKR.

The colors of the progress bar indicate the status of the objective.

- If the progress is 0-25 percent less than the expected progress at any given point in time, the OKR status is *behind*, and the progress bar color will be orange.
- If the progress is more than 25 percent less than the expected progress at any given point in time, the OKR status is *at risk*, and the progress bar color will be red.

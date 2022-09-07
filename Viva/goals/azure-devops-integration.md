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

Viva Goals Azure DevOps integration lets you update your OKR progress automatically based on the progress of work items in your Azure DevOps Projects. 

For example, say you use Azure DevOps to track the status of issues, and you have an objective in Viva Goals to resolve 30 issues every quarter. When you link your objective to the corresponding project in Azure DevOps, the status of your OKR will be updated as work items under the associated project get resolved. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time and keeping your OKRs current.


## How to enable Azure DevOps integration

Admins can follow these steps to enable this integration: 

1. In the sidebar, select **Admin** and then select the **Integrations** tab. 

   :::image type="content" source="../media/goals/6/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/6/viva-goals-integrations-page.png":::

1.  Under Azure DevOps, choose to **enable** the integration. If a connection was made previously or if the integration was already enabled, you'll instead see the option to **Manage** the integration. 

    :::image type="content" source="../media/goals/6/azure-devops-enable-button.png" alt-text="Screenshot highlights the Enable button for Azure DevOps in Viva Goals." lightbox="../media/goals/6/azure-devops-enable-button.png":::

    To disable the integration from the same section, select **Change** and then select **Disable integration** from the dropdown.

    :::image type="content" source="../media/goals/6/azure-devops-disable-button.png" alt-text="Screenshot highlights the option to disable Azure DevOps in Viva Goals." lightbox="../media/goals/6/azure-devops-disable-button.png":::

## How to configure the Azure DevOps connection 

After you enable the integration, the next step is to configure an Azure DevOps connection: 

1. Select **New Connection**, and sign in to your Azure DevOps organization. 

   :::image type="content" source="../media/goals/6/azure-devops-new-connection-button.png" alt-text="Screenshot shows where you create a new Azure DevOps connection in Viva goals.png." lightbox="../media/goals/6/azure-devops-new-connection-button.png":::

2. Enter a name for the new connection, and furnish the **Account Name** and **Project Name**. 

   :::image type="content" source="../media/goals/6/azure-devops-configure-new-connection.png" alt-text="Screenshot shows where you fill in details for a new Azure DevOps connection in Viva goals.png." lightbox="../media/goals/6/azure-devops-configure-new-connection.png":::

   It's optional to share connections with other users in the organization.
1. Select **Next** to get the connection up and running. You can edit the saved connection at any time.

Viva Goals lets you connect with multiple projects. Select **New Connection** to fetch data from another project. You differentiate connections by name. The names will be displayed to other users when they link their OKRs with Azure DevOps data.

## How to connect the Azure DevOps connection to an OKR

After you configure the connection, the next step is to start linking OKRs to Azure DevOps Projects.

The option to connect to a data source will appear only for key results, not for objectives.

  :::image type="content" source="../media/goals/6/azure-devops-datasource.png" alt-text="Screenshot shows where you select Azure DevOps from the list of data sources in Viva goals.png." lightbox="../media/goals/6/azure-devops-datasource.png":::

1. If you already created a connection or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

1.  Choose the method you want to measure progress, percent complete or KPI (success metric). If you choose KPI, provide a metric, starting value, and target value.

1.  Select a connection, and choose the **Query**. When you choose a query, the **count of matching work items** will be displayed. 

    :::image type="content" source="../media/goals/6/azure-devops-connection-details.png" alt-text="Screenshot shows where you add an Azure DevOps connection to your OKRs in Viva goals.png." lightbox="../media/goals/6/azure-devops-connection-details.png":::

    Progress will be calculated based on the count of tickets completed under the chosen query if you chose KPI metric to track progress. It will be calculated based on the percentage of tickets closed if you chose percent complete to track progress).

1. Select **Next > Save**.

Your objective is now linked to a query in Azure DevOps to track the progress of your work items and automatically update the status of the corresponding OKR.

The colors of the progress bar indicate the status of the objective:

- If progress is 0 to 25 percent less than expected progress at any point in time, the OKR status is *behind*, and the progress bar be orange.
- If progress is more than 25 percent less than expected progress at any point, the OKR status is *at risk*, and the progress bar will be red.

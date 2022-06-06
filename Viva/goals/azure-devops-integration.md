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
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to integrate your work items with OKRs in Viva Goals"
---

# Azure DevOps integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to Azure DevOps integration

The Viva Goals Azure DevOps integration allows you to update your OKR progress automatically depending on the progress of work items in your Azure DevOps projects. 

As an example, if you use Azure DevOps to track the status of issues, and you have an objective in Viva Goals for resolving 30 issues every quarter, when you link your objective to the corresponding project in Azure DevOps, the status of your OKR will be updated as the work items under the associated project get resolved. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## How to enable the Azure DevOps integration

Admins can enable this integration by taking the following steps: 

- From the sidebar, click on **Admin** and select the **Integrations** tab. 

   :::image type="content" source="../media/goals/6/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/6/viva-goals-integrations-page.png":::

- Under Azure DevOps, you can **enable** the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration. 

   :::image type="content" source="../media/goals/6/enabling-azure-devops-in-viva-goals.png" alt-text="Enabling Azure DevOps in Viva Goals." lightbox="../media/goals/6/enabling-azure-devops-in-viva-goals.png":::

- This integration can also be **disabled** from the same section by clicking on **Change**, and choosing**Disable integration** from the dropdown.

  :::image type="content" source="../media/goals/6/disabling-azure-devops-in-viva-goals.png" alt-text="Disabling Azure DevOps in Viva Goals." lightbox="../media/goals/6/disabling-azure-devops-in-viva-goals.png":::

## How to configure the Azure DevOps connection 

- After enabling the integration, the first step is to configure an Azure DevOps connection. 
- Select **New Connection**, and sign into your Azure DevOps account. 

  :::image type="content" source="../media/goals/6/creating-azure-devops-new-connection-in-viva-goals.png" alt-text="Creating a new Azure DevOps connection in Viva goals.png." lightbox="../media/goals/6/creating-azure-devops-new-connection-in-viva-goals.png":::

- Provide a name for the connection, and furnish the **Account Name** and the **Project Name**. 

  :::image type="content" source="../media/goals/6/azure-devops-new-connection-details.png" alt-text="Filling in details for the new Azure DevOps connection in Viva goals.png." lightbox="../media/goals/6/azure-devops-new-connection-details.png":::

- It's optional to share this connection with other users in the organization. Click on Next to get up and running with this integration. You can edit the saved connection at any time.

Viva Goals allows you to connect with multiple projects. Select New Connection to fetch data from another project. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with Azure DevOps data.

## How to connect the Azure DevOps connection to an OKR

Once you've configured the connection, the next step is to start linking OKRs to the Azure DevOps projects.

- The option to connect to a data source will appear only for Key Results and not for Objectives.

  :::image type="content" source="../media/goals/6/azure-devops-data-source-from-list-of-integrations-in-viva-goals.png" alt-text="Selecting Azure DevOps from the list of data sources in Viva goals.png." lightbox="../media/goals/6/azure-devops-data-source-from-list-of-integrations-in-viva-goals.png":::

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared. 
- Choose the method using which you want to measure the progress—percent complete or KPI (success metric). If you're choosing KPI, provide a metric, starting value, and target value. 
- Select a connection, and choose the **Query**. As soon as you choose a query, the **count of matching work items** will be displayed. 

  :::image type="content" source="../media/goals/6/azure-devops-connection-details-in-viva-goals.png" alt-text="Adding Azure DevOps connection to your OKRs in Viva goals.png." lightbox="../media/goals/6/azure-devops-connection-details-in-viva-goals.png":::

- The progress will be calculated based on the count of tickets completed under the chosen query (if you've chosen KPI metric to track progress), or will be calculated based on the percentage of tickets closed (if you've chosen percent complete to track progress). 
- Click **Next > Save**.

Now you've successfully linked your objective to a query in Azure DevOps to track the progress of your work items, and update the status of the corresponding OKR automatically.

The colors of the progress bar indicate the status of the objective.

- If the progress is 0-25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange.
- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red.

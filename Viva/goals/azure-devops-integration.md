---
title: Azure DevOps integration
ms.reviewer: 
ms.author: ranjaliroy
author: ranjali-MS
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
description: "Learn how to integrate your Azure DevOps work items with OKRs in Viva Goals"
---

# Azure DevOps integration

## Introduction to Azure DevOps integration

The Viva Goals Azure DevOps data integration allows you to automatically update your Key Results or Projects based on the status of work items in Azure DevOps. While the structure and nature of the Azure DevOps data that is synced with Viva Goals is different for Key Results versus Projects, they both leverage the same data connection. 

The Viva Goals Azure DevOps data integration connects to a shared query in a specific Azure DevOps Organization + Project. The user who sets up the connection must have access to the Azure DevOps Organization, Project, and the shared query that is being accessed. In addition, the Azure DevOps Organization policy must allow for OAuth access (further details are described below).  

## Project vs OKRs 

One of the fundamental tenets of OKRs is distinguishing between outcomes versus outputs.  OKRs, and specifically Key Results, are focused on driving impact (aka outcomes), while Viva Goals [Projects](/viva/goals/projects) are focused on outputs – the initiatives or work that you believe is needed to drive the Key Results.  Both are important to track, but they are measuring different things.  While you can integrate both Viva Goals Key Results and Projects with your Azure DevOps work items, it is important to understand the difference. Azure DevOps primarily focuses on tracking work, so it is more common to integrate Viva Goals Projects with Azure DevOps, though there are certainly examples where Azure DevOps data can be aligned with Outcomes as well.  

Viva Goals data integration returns different data for Key Results and Projects. For Key Results, the integration returns a single number, either a percentage or count of completed work items. For Projects, the integration returns the actual work items from Azure DevOps along with percentage complete information. 

## How to enable Azure DevOps integration

Admins can follow these steps to enable this integration: 

1. In the sidebar, select **Admin** and then select the **Integrations** tab. 

   :::image type="content" source="../media/goals/6/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/6/viva-goals-integrations-page.png":::

1.  Under Azure DevOps, choose to **enable** the integration. If a connection was made previously or if the integration was already enabled, you'll instead see the option to **Manage** the integration. 

    :::image type="content" source="../media/goals/6/azure-devops-enable-button.png" alt-text="Screenshot highlights the Enable button for Azure DevOps in Viva Goals." lightbox="../media/goals/6/azure-devops-enable-button.png":::

    To disable the integration from the same section, select **Change** and then select **Disable integration** from the dropdown.

    :::image type="content" source="../media/goals/6/azure-devops-disable-button.png" alt-text="Screenshot highlights the option to disable Azure DevOps in Viva Goals." lightbox="../media/goals/6/azure-devops-disable-button.png":::

## How to configure the Azure DevOps connection from the Organization Admin Integrations Tab  

>[!Note] 
>While these instructions are specific to creating new connections via the Viva Goals Organization Admin Integrations menu, end users can set up new connections directly during the create/edit Key Result or Project workflows. See below for more details.

After you enable the integration, the next step is to configure an Azure DevOps connection: 

1. Select **New Connection**, and sign-in to your Azure DevOps organization. 

   :::image type="content" source="../media/goals/6/azure-devops-new-connection-button.png" alt-text="Screenshot shows where you create a new Azure DevOps connection in Viva goals" lightbox="../media/goals/6/azure-devops-new-connection-button.png":::

2. Enter a name for the new connection, and furnish the **Account Name** and **Project Name**. 

   :::image type="content" source="../media/goals/ado-images/connect-to-ado.png" alt-text="Screenshot shows where you fill in details for a new Azure DevOps connection in Viva goals." lightbox="../media/goals/ado-images/connect-to-ado.png":::
   
3. Select **Next** to get the connection up and running. You can edit the saved connection at any time.

Viva Goals allows you to connect with multiple Azure DevOps projects. Select **New Connection** to get data from another Azure DevOps project. We recommend using the connection name to differentiate these connections (Azure DevOps Organization + Project name).

## How to connect Azure DevOps to a Viva Goals Project 

1. Go to Outcome. 

      :::image type="content" source="../media/goals/6/azure-devops-projects-outcome-button.png" alt-text="Screenshot shows where you create a new Azure DevOps connection to a project in Viva goals." lightbox="../media/goals/6/azure-devops-projects-outcome-button.png":::

2. Select Show More Options. 

      :::image type="content" source="../media/goals/6/azure-devops-projects-show-more.png" alt-text="Screenshot shows the Show more options button." lightbox="../media/goals/6/azure-devops-projects-show-more.png":::

3. Select Add Tasks. 

      :::image type="content" source="../media/goals/6/azure-devops-projects-add-tasks.png" alt-text="Screenshot shows the Add tasks button." lightbox="../media/goals/6/azure-devops-projects-add-tasks.png":::

4. Select **Automatically from a data source**, and then select **Azure DevOps** 

5. If you've already created a connection, that connection will be selected automatically. Viva Goals will prompt you to create a new connection if you have no existing connections. You can also create a new Azure DevOps connection by selecting the dropdown carrot and selecting **Add a new connection**. 

      :::image type="content" source="../media/goals/6/azure-devops-projects-connection-dropdown.png" alt-text="Screenshot shows how to create or select connections" lightbox="../media/goals/6/azure-devops-projects-connection-dropdown.png":::
      
6. Select a connection and search for the query by query name.  You can search by query name.  When you select a query, the count of matching work items is displayed.

      :::image type="content" source="../media/goals/6/azure-devops-projects-query-details.png" alt-text="Screenshot shows how to search and add query details." lightbox="../media/goals/6/azure-devops-projects-query-details.png":::
      
7. Select **Next** and then **Save**. 

Now that the Viva Goals Project is linked to a shared query in Azure DevOps, the work items in the shared query are automatically synced to Viva Goals.  Viva Goals will show a maximum of 3 levels of your Azure DevOps tree structure query in Viva Goals Project views.  Progress calculations based on the completion of the child work items are shown at each level of the query hierarchy and rolled up the Viva Goals Project progress percentage.  Hyperlinks connect you back to the shared query in Azure DevOps, as well as to the individual work items, enabling you to quickly see in-depth information for the supporting work. 

>[!Note] 
>While creating the Azure DevOps connection, ensure that the Third-party application access via OAuth setting is enabled. 

:::image type="content" source="../media/goals/6/azure-devops-oauth.png" alt-text="Screenshot shows where you can enable oauth access for Azure DevOps." lightbox="../media/goals/6/azure-devops-oauth.png":::

## How to connect the Azure DevOps connection to a Key Result

1. During the create / edit Key Result flow, you will have the ability to connect your Key Result to Azure DevOps. You have two options on how you measure progress from the data in your Azure DevOps query: 

   1. % of completed work items – this yields a percentage of work items in the underlying query that are completed.  You can also restrict the results to a specific work item type. 

         :::image type="content" source="../media/goals/6/azure-devops-percentage-progress.png" alt-text="Screenshot shows progress measured by percentage of completed work items." lightbox="../media/goals/6/azure-devops-percentage-progress.png":::

   2. Count of work items –this yields a count of the number work items (total or completed) in the underlying query.  This requires setting up a metric.  You can also restrict the results to a specific work item type. 
   
   >[!Note] 
    >It is recommended that your Azure DevOps query return a flat list of work items as opposed to a tree-structure. This is because Viva Goals counts each work item, regardless of where the item happens to sit in the hierarchy.  

      :::image type="content" source="../media/goals/6/azure-devops-work-items-progress.png" alt-text="Screenshot shows progress measured by tracking the number of work items." lightbox="../media/goals/6/azure-devops-work-items-progress.png":::

2. The option to connect to a data source will appear only for Key Results and not for Objectives.  The option can be found under Progress. 

      :::image type="content" source="../media/goals/6/azure-devops-datasource.png" alt-text="Screenshot shows where you select Azure DevOps from the list of data sources in Viva goals." lightbox="../media/goals/6/azure-devops-datasource.png":::
  
3. If you've already created a connection, that connection will be selected automatically. Viva Goals will prompt you to create a new connection if you have no existing connections. You can also create a new Azure DevOps connection by selecting the dropdown carrot and selecting **Add a new connection**.
 
4. Select a connection and search for the Azure DevOps query by name. When you choose a query, the **count of matching work items** will be displayed. 

    :::image type="content" source="../media/goals/6/azure-devops-connection-details.png" alt-text="Screenshot shows where you add an Azure DevOps connection to your OKRs in Viva goals." lightbox="../media/goals/6/azure-devops-connection-details.png":::

5. Select **Next > Save**.

Now that the Key Result is linked to a query in Azure DevOps, you can track the progress of your work items and update the status of the corresponding KR automatically. 

>[!Note] 
>While creating the Azure DevOps connection, ensure that the Third-party application access via OAuth setting is enabled. 

>[!Note] 
>Viva Goals will update the KRs and/or Projects hourly from their Azure DevOps sources  

:::image type="content" source="../media/goals/6/azure-devops-oauth.png" alt-text="Screenshot shows where you can enable oauth access for Azure DevOps." lightbox="../media/goals/6/azure-devops-oauth.png":::

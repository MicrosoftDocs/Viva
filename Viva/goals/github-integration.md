---
title: "GitHub Integration"
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

description: "Learn how to integrate your GitHub repositories with OKRs in Viva Goals."
---

# GitHub integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to the GitHub integration

The Viva Goal GitHub integration allows you to update your Objectives and Key Results (OKR) progress automatically depending on the progress of issues in your GitHub repositories. 

Let's use this example: you use GitHub to track the status of issues, and you have an objective in Viva Goals for resolving 30 issues every quarter. When you link this objective to the corresponding repository in GitHub, the status of your OKR will be updated as the issues under the associated repository get resolved. You can also track the progress of issues being handled by a specific user for objectives that are user-centric. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.

## How to enable the GitHub integration

Admins can perform the following steps to enable this integration:

- From the sidebar, go to **Admin** and select the **Integrations** tab.
    
    :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

- Against **GitHub**, you'll have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration.
    
    :::image type="content" source="../media/goals/10/github-enable-button.png" alt-text="Enabling GitHub in Viva Goals." lightbox="../media/goals/10/github-enable-button.png":::

- This integration can also be **disabled** from the same section. Go to **Change** and select **Disable integration** from the dropdown to disable this integration.
    
   :::image type="content" source="../media/goals/10/github-disable-button.png" alt-text="Disabling GitHub in Viva Goals." lightbox="../media/goals/10/github-disable-button.png"::: 

## How to configure the GitHub connection

- After enabling the integration, the first step is to configure a GitHub connection.

- Select **New Connection**, and sign into your GitHub account.
    
    :::image type="content" source="../media/goals/10/github-new-connection-button.png" alt-text="Adding a new GitHub connection in Viva Goals." lightbox="../media/goals/10/github-new-connection-button.png"::: 

- Provide a name for the connection.
    
    :::image type="content" source="../media/goals/10/github-configure-new-connection.png" alt-text="Configuring a new GitHub connection in Viva Goals." lightbox="../media/goals/10/github-configure-new-connection.png"::: 

- It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

> [!NOTE]
> Viva Goals allows you to connect with multiple repositories. Select **New Connection** to fetch data from another repository. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with GitHub data.

## How to connect the GitHub connection to an OKR

Once you have configured the connection, the next step is to start linking OKRs to the GitHub repositories.

- While **creating or editing an OKR**, select **Connect data source to auto-update progress**. From the drop-down menu, select **GitHub**.
    
    :::image type="content" source="../media/goals/10/github-datasource.png" alt-text="Selecting GitHub from the list of data sources in Viva Goals." lightbox="../media/goals/10/github-datasource.png":::

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Select the method using which you want to measure the progress — **percent complete** or **KPI (success metric)**. If you're choosing key performance indicator (KPI), provide a metric, starting value, and target value.

- Select a connection, and all the **associated repositories** will be available in the drop-down. Select a repository and select a **Milestone**.
    
     :::image type="content" source="../media/goals/10/github-new-connection-details.png" alt-text="Adding new GitHub connection to OKRs in Viva goals." lightbox="../media/goals/10/github-new-connection-details.png":::

- Select an **Assignee** to keep tabs on the issues being handled by a specific user. Select the **custom labels** as applicable.

- You can track the status of issues that are closed and open. Select an appropriate status.

- The progress will be computed based on the count of issues (if you have chosen KPI metric to track progress), or will be calculated based on the percentage of issues closed (if you have chosen percent complete to track progress).

    > [!NOTE]
    > If you choose percent complete to track progress, the progress will be computed only based on the percentage of issues resolved. On the other hand, if you want to keep track of the issues that are open as well, you will have to choose a KPI metric to track progress.

- Go to **Next** and select **Save**.

You have now successfully linked your objective to a repository in GitHub to track the progress of your issues, and updated the status of the corresponding OKR automatically.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 - 25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange.

- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red.

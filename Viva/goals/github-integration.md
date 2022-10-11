---
title: "GitHub Integration"
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
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

description: "Learn how to integrate your GitHub repositories with OKRs in Viva Goals."
---

# GitHub integration

## Introduction to the GitHub integration

Viva Goal GitHub integration enables you to update your objective and key result (OKR) progress automatically based on the progress of issues in  GitHub repositories. 

Let's use this example: You use GitHub to track the status of issues, and you have an objective in Viva Goals to resolve 30 issues every quarter. When you link this objective to the corresponding repository in GitHub, the status of your OKR will be updated as the issues in the associated repository get resolved. You can also track the progress of issues being handled by a specific user for objectives that are user-centric. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.

## How to enable the GitHub integration

Admins can follow these steps to enable the integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
    
    :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

2. For **GitHub**, you'll have an option to **Enable** the integration. If a connection was previously made or if the integration was already enabled, you'll have the option to **Manage** the enabled integration.
    
    :::image type="content" source="../media/goals/10/github-enable-button.png" alt-text="Screenshot shows the enable option highlighted on the integrations page.." lightbox="../media/goals/10/github-enable-button.png":::

   You can also disable the integration from the same section: Go to **Change** and select **Disable integration** from the dropdown.
    
   :::image type="content" source="../media/goals/10/github-disable-button.png" alt-text="Screenshot shows where you disable GitHub in Viva Goals." lightbox="../media/goals/10/github-disable-button.png"::: 

## How to configure the GitHub connection

After you enable the integration, the next step is to configure a GitHub connection.

1. Select **New Connection**, and sign in to your GitHub account.
    
    :::image type="content" source="../media/goals/10/github-new-connection-button.png" alt-text="Screenshot shows where you add a new GitHub connection in Viva Goals." lightbox="../media/goals/10/github-new-connection-button.png"::: 

1. Provide a name for the connection.
    
    :::image type="content" source="../media/goals/10/github-configure-new-connection.png" alt-text="Screenshot shows where you enter a name for your new GitHub connection in Viva Goals." lightbox="../media/goals/10/github-configure-new-connection.png"::: 

1. You have the option to share the connection with other users in the organization.

1. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

> [!NOTE]
> Viva Goals lets you connect to multiple repositories. Select **New Connection** to fetch data from another repository. You differentiate these connections by name. The names will be displayed to other users when they link their OKRs with GitHub data.

## How to connect the GitHub connection to an OKR

After you configure the connection, the next step is to link OKRs to GitHub repositories.

1. When you create or edit an OKR, select **Connect data source to auto-update progress**. From the drop-down menu, select **GitHub**.
    
    :::image type="content" source="../media/goals/10/github-datasource.png" alt-text="Screenshot shows where you select GitHub as the data source." lightbox="../media/goals/10/github-datasource.png":::

2. If you already created a connection, or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

3. Select the method that you want to use to measure progress, **percent complete** or **KPI (success metric)**. If you choose KPI, provide a metric, starting value, and target value.

4. Select a connection, and all the **associated repositories** will be available in the dropdown. Select a repository and a **Milestone**.
    
     :::image type="content" source="../media/goals/10/github-new-connection-details.png" alt-text="Screenshot shows where you add GitHub connection details." lightbox="../media/goals/10/github-new-connection-details.png":::

5. Select an **Assignee** for issues that are being handled by a specific user. Select the **custom labels** as applicable.

6. You can track the status of issues that are closed and open. Select an appropriate status.

   The progress will be computed based on the count of issues, if you chose KPI metric to track progress, or based on the percentage of issues closed, if you chose percent complete to track progress.

    > [!NOTE]
    > If you choose percent complete to track progress, the progress will be computed only based on the percentage of issues resolved. On the other hand, if you want to keep track of the issues that are open as well, you will have to choose a KPI metric to track progress.

8. Go to **Next** and select **Save**.

You've now linked your objective to a repository in GitHub to track the progress of your issues and automatically update the status of the corresponding OKR.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 to 25 percent less than the expected progress at any point in time, the OKR status is *behind*, and the progress bar will be orange.

- If the progress is more than 25-percent less than expected at any point, the OKR status is *at risk*, and the progress bar will be red.

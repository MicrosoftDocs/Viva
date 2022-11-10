---
title: "GitLab Integration"
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

description: "Learn how to integrate your GitLab projects with OKRs in Viva Goals."
---

# GitLab integration

## About GitLab integration

Viva Goals GitLab integration enables you to update your objective and key result (OKR) progress automatically based on the progress of issues in your GitLab projects.
  
Let's use this example: You use GitLab to track your projects. You have an objective in Viva Goals to resolve 30 issues every quarter. When you link this objective to the corresponding project in GitLab, the status of your OKR will be updated as the issues under the associated project get resolved. You can also track the progress of issues that are being handled by a specific user for objectives that are user-centric. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.
  
All users and admins can use this feature. Admins can manage the integration from the admin dashboard.

## How to enable GitLab integration

Admins can follow these steps to enable this integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
  
    :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

2. For **GitLab**, you'll have an option to **Enable** the integration. If you already created a connection, you'll have an option to **Manage** the integration.
  
    :::image type="content" source="../media/goals/10/gitlab-enable-button.png" alt-text="Screenshot highlights the enable option for GitLab in Viva Goals." lightbox="../media/goals/10/gitlab-enable-button.png":::
  
   You can also disable the integration from the same section: Go to **Change** and select **Disable integration** from the dropdown.
    
   :::image type="content" source="../media/goals/10/gitlab-disable-button.png" alt-text="Screenshot shows where you select Disable Integration for GitLab in Viva Goals." lightbox="../media/goals/10/gitlab-disable-button.png"::: 

## For admins: How to connect GitLab to your Viva Goals account

1. After you enable the integration as an admin, you need to configure a GitLab connection from the **GitLab configuration** page.

2. Select **New Connection**, and sign in to your GitLab account.
  
    :::image type="content" source="../media/goals/10/gitlab-new-connection-button.png" alt-text="Screenshot shows where you choose to add a new GitLab connection in Viva Goals." lightbox="../media/goals/10/gitlab-new-connection-button.png":::

3. Enter a name for the connection.
  
    :::image type="content" source="../media/goals/10/gitlab-configure-new-connection.png" alt-text="Screenshot shows where you name your new GitLab connection in Viva goals." lightbox="../media/goals/10/gitlab-configure-new-connection.png":::

4. It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

5. Viva Goals allows you to connect with multiple projects. Select **New Connection** to fetch data from another project. You differentiate these connections by name. The names will be displayed to other users when they link their OKRs with GitLab data.

## How to use GitLab integration and connect GitLab projects to an OKR

After you configure the connection, the next step is link OKRs to your GitLab projects.

1. When you create or edit an OKR, select **Automatically from a data source**. From the drop-down menu, select **GitLab**.
  
    :::image type="content" source="../media/goals/10/gitlab-datasource.png" alt-text="Screenshot shows where you select GitLab as the data source." lightbox="../media/goals/10/gitlab-datasource.png":::

2. If you already created a connection, or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

3. Select the method  you want to use measure progress, **percent complete** or **KPI (success metric)**. If you choose KPI, provide a metric, starting value, and target value.

4. Select a connection, if there are multiple connections. All *associated projects* will be available in the drop-down. Choose a **project** and select a **Milestone**.
  
    :::image type="content" source="../media/goals/10/gitlab-new-connection-details.png" alt-text="Screenshot shows where you add GitLab connection details." lightbox="../media/goals/10/gitlab-new-connection-details.png":::

5. Select an **Assignee** to track issues that being handled by a specific user. Select the **custom labels** as applicable.

6. Select an appropriate status to track the status of issues that are closed/open. This option is applicable only to KPI-type OKRs.

7. You can also directly search issues by typing in the issue ID or issue title or select them from the dropdown in the **Issues** field. You can also select multiple issues and connect them to the OKR.

## How to calculate progress with the GitLab integration

The progress of your OKR will be computed based on the count of issues, if you chose KPI metric to track progress. If you chose percent complete to track progress, the percent will be calculated based on the number of issues closed.

If you have subtasks added under each issue, the progress will be calculated based on the status of the subtasks as well. For example, if you connected two issues that each have two subtasks each to your OKR, when you close subtask 1 in issue 1, the progress will be updated to 25 percent. When you close subtask 2 in issue 1, your OKR progress will be 50 percent.

> [!NOTE]
> If you select percent complete to track progress, the progress will be computed only based on the percentage of issues closed. If you also want to keep track of issues that are open, you must select a KPI metric to track progress.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 to 25 percent less than the expected progress at any point in time, the OKR status is *behind*, and the progress bar will be orange.

- If the progress is more than 25 percent less than expected at any point, the OKR status is *at risk*, and the progress bar will be red.

## How to disable GitLab integration

Admins can disable GitLab integration at any time: Go to **GitLab** in the **Integrations** section and select **Manage**. On the **GitLab Configurations** page, go to the **Change** dropdown, select **Disable**, and confirm.

> [!NOTE]
> If a project in Gitlab is closed without all sub-tasks marked as **complete**, Viva Goals will consider the project completed since it was closed.

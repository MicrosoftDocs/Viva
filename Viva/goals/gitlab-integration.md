---
ms.date: 05/15/2024
title: GitLab integration
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- vg-integration
search.appverid:
- MET150
description: "Learn how to integrate your GitLab projects with OKRs in Viva Goals."
---

# GitLab integration

Viva Goals GitLab integration enables you to update your objective and key result (OKR) progress automatically based on the progress of issues in your GitLab projects.
  
Suppose you use GitLab to track your projects and you have an objective in Viva Goals to resolve 30 issues every quarter. When you link this objective to the corresponding project in GitLab, the status of your OKR will be updated as the issues under the associated project are resolved. You can also track the progress of issues that are being handled by a specific user for objectives that are user-centric. Viva Goals will automatically sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.
  
All users and admins can use this feature. Admins can manage the integration from the admin dashboard.

## Enable GitLab integration

Admins can follow these steps to enable this integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.

1. Search for **GitLab**, or find it under the **Data Integrations** section.

1. Select **Enable** next to **GitLab**. If you already created a connection, you'll have an option to **Manage** the integration instead.
  
   You can disable the integration by selecting **Manage** > **Change** > **Disable Integration**.

## Connect GitLab to your Viva Goals account as an admin

1. After you enable the integration as an admin, you need to configure a GitLab connection from the **GitLab Configure** page. You can access this page by going to **Admin** > **Integrations** and selecting **Manage** next to **GitLab**.

1. Select **New Connection** and sign in to your GitLab account.

1. Enter a name for the connection.
  
1. It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

1. Viva Goals allows you to connect with multiple projects. Select **New Connection** to fetch data from another project. You differentiate these connections by name. The names will be displayed to other users when they link their OKRs with GitLab data.

## Connect GitLab projects to an OKR

After you configure the connection, the next step is to link OKRs to your GitLab projects.

1. When you create or edit an OKR, open the **Progress and Status** dropdown. In the section with the text "Connect to a data source for automatic progress updates", find and select the icon for **GitLab**.

1. If you already created a connection, or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

1. Select the method you want to use measure progress: **percent complete** or **KPI (success metric)**. If you choose KPI, provide a metric, starting value, and target value.

1. If there are multiple connections, select one. All *associated projects* will be available in the drop-down. Choose a **Project** and select a **Milestone**.

1. Pick an entry in the **Assigned to** field to track issues that being handled by a specific user. Select **Labels** as appropriate.

1. Select an appropriate status to track the status of issues that are closed/open. This option is applicable only to KPI-type OKRs.

1. You can directly search for issues by typing in the issue ID or issue title; alternatively, you can select them from the dropdown in the **Issues** field. You can also select multiple issues and connect them to the OKR.

## Calculate progress made on an OKR

If you're using a KPI metric to track progress, the progress of your OKR will be computed based on the count of issues. If you're using percent complete to track progress, the percent will be calculated based on the number of issues closed.

If you have subtasks added under each issue, the progress will be calculated based on the status of the subtasks as well. For example, if you connected two issues that each have two subtasks each to your OKR, when you close subtask 1 in issue 1, the progress will be updated to 25 percent. When you later close subtask 2 in issue 1, your OKR progress will be 50 percent.

> [!NOTE]
> If you select percent complete to track progress, the progress will be computed only based on the percentage of issues closed. If you also want to keep track of issues that are open, you must select a KPI metric to track progress.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 to 25 percent less than the expected progress at any point in time, the OKR status is *behind*, and the progress bar will be orange.

- If the progress is more than 25 percent less than expected at any point, the OKR status is *at risk*, and the progress bar will be red.

## Disable GitLab integration

Admins can disable GitLab integration at any time: Go to **GitLab** in the **Integrations** section and select **Manage**. On the **GitLab Configuration** page, select **Change** > **Disable Integration**.

> [!NOTE]
> If a project in Gitlab is closed without all sub-tasks marked as complete, Viva Goals will nonetheless consider the project completed because it was closed.

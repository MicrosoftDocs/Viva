---
title: "GitLab Integration"
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

description: "Learn how to integrate your GitLab projects with OKRs in Viva Goals."
---

# GitLab Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Who can use this feature?

All Users and Admins (Admins also have permissions to manage the integration from the admin dashboard) can use this feature.

## About the GitLab integration

Viva Goals’ GitLab integration allows you to update your Objectives and Key Results (OKR) progress automatically depending on the progress of issues in your GitLab projects. Let’s say you use GitLab to track your projects, and you have an objective in Viva Goals for resolving 30 issues every quarter. When you link this objective to the corresponding project in GitLab, the status of your OKR will be updated as the issues under the associated project get resolved. You can also track the progress of issues being handled by a specific user for objectives that are user-centric. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## How to enable the GitLab integration?

Admins can enable this integration, by performing the following steps:

- From the sidebar, go to **Admin** and select the **Integrations** tab.

- Against **GitLab**, you'll have an option to **Enable** the integration. If you have a connection already created, you'll have an option to **Manage** the integration.

    :::image type="content" source="../media/goals/viva-goals-gitlab-integration-1.png" alt-text="GitLab Integration 1":::

## Connect GitLab to your Viva Goals account - Admins

- After enabling the integration, as an admin, the first step is to configure a GitLab connection from the **GitLab configuration** page.

- Select **New Connection**, and sign in to your GitLab account.

    :::image type="content" source="../media/goals/gitlab-connection-creat.gif" alt-text="GitLab Integration 2":::

- Provide a name for the connection.

- It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

    :::image type="content" source="../media/goals/viva-goals-gitlab-integration-3.png" alt-text="GitLab Integration 3":::

- Viva Goals allows you to connect with multiple projects. Select **New Connection** to fetch data from another project. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with GitLab data.

## How to use the GitLab integration and connect GitLab Projects to an OKR

Once you've configured the connection, the next step is to start linking OKRs to the GitLab projects.

- While **creating or editing an OKR**, select **Automatically from a data source**. From the drop-down menu, select **GitLab**.

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Select the method using which you want to measure the progress — **percent complete** or **KPI (success metric)**. If you're choosing key performance indicator (KPI), provide a metric, starting value, and target value.

- Select a connection in case of multiple connections, and all the **associated projects** will be available in the drop-down. Choose a **project** and select a **Milestone**.

- Select an **Assignee** to keep tabs on the issues being handled by a specific user. Select the **custom labels** as applicable.

- Select an appropriate status to track the status of issues that are closed and open. This will be applicable only for the KPI type OKRs.

- You can also directly search issues by typing in the issue ID or issue title or select them from the dropdown in the **Issues** field. You can also select multiple issues and connect them to the OKR.

## How is progress calculated?

- The progress of your OKR will be computed based on the count of issues (if you have chosen KPI metric to track progress), or if you have chosen percent complete to track progress, the % will be calculated based on the number of issues closed.

- If you have subtasks added under each issue, the progress will be calculated based on the status of the subtasks as well.

For example, if you've connected two issues that have two subtasks each to your OKR, once you close subtask 1 in issue 1, the progress will be updated as 25% and on closing subtask 2 in issue 1, your OKR progress will be 50%.

> [!NOTE]
> If you select percent complete to track progress, the progress will be computed only based on the percentage of issues closed. On the other hand, if you want to keep track of the issues that are open as well, you will have to select a KPI metric to track progress.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 - 25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange.

- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red.

## How to disable the integration

The GitLab integration may also be disabled by an Admin at any time. To disable the integration as an Admin, go to **GitLab** in the **Integrations** section and select **Manage**. In the **GitLab Configurations** page, go to the **Change** dropdown, select **Disable** and confirm the action.

:::image type="content" source="../media/goals/viva-goals-gitlab-integration-5.png" alt-text="GitLb Integration 5":::

> [!NOTE]
> If a project in Gitlab is closed without even marking all the sub-tasks as **complete**, it will drive a 100% progress on Viva Goals considering the project is completed since it was closed.
>
> The rationale is that we did not want users to check-off all the sub-tasks in the checklist to ensure Viva Goals tracks the progress as 100%. If it's a 100 item checklist and 50 were completed but they have really completed the project, we did not want to force the user to mandatorily check off all the items in the checklist to achieve that.

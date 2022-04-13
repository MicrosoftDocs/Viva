---
title: Wrike projects in Viva Goals
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
description: "View your Wrike project execution directly in Viva Goals. "
---

# Wrike projects in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## What are Projects in Viva Goals?

Projects help you keep track of all the work your organization is executing to achieve your OKRs. While key results track outcomes, projects track the output that helps you achieve your key results. For more details and best practices, see [What are Projects?](https://help.ally.io/en/articles/4224975-what-are-projects)

## Viva Goals projects and Wrike

You can now view your Wrike projects and tasks in Viva Goals, and connect the progress of these projects and tasks to projects and OKRs in Viva Goals. 

## How do I set up Wrike integration? 

1. From the navigation menu, select **Admin >** select the **Integrations** tab.

2. Against Wrike, you'll have an option to **Enable**the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration.

3. This integration can also be **disabled** from the same section by selecting **Change**, and choosing **Disable integration** from the dropdown.

    :::image type="content" source="../media/goals/goals-set-up-wrike-integration.gif" alt-text="Image of Wrike integration":::

Viva Goals allows you to create multiple connections to Wrike. Select **New Connection** to use a different set of Wrike credentials to connect — different Wrike users might have access to different Wrike projects. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with Wrike projects.

## How do I start populating Wrike projects?

Every folder, project, and task in Wrike will have a permalink. To be able to track the status of Wrike projects and tasks within Viva Goals, you should provide the permalink of the project and/or the task you want to connect to. 

To fetch the permalink, here's what you need to do: 

1. **Project**: Right-click on the project to copy the permalink.

    :::image type="content" source="../media/goals/goals-wrike-project-permalink.png" alt-text="Image of copy the permalink":::


2. **Task**: Select the task from the List **View panel**> from the top-right corner of the Task View panel (right of the List View) > select the link icon to copy the permalink of the task.

    :::image type="content" source="../media/goals/goals-wrike-task-permalink.png" alt-text="Image og permalink of the task":::  

3. While **creating or editing a project in Viva Goals**, select **Select an option to add tasks to project**. From the drop down menu, select **Wrike**.

4. If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

5. Paste the **permalink of the Wrike project or the task** you want to associate it with. Select **Preview**. 

    If you're mapping to a Wrike project, Viva Goals will automatically fetch the details of the tasks that are a part of the connected Wrike project — name of the task, progress, assignee, and due date.

    > [!NOTE]
    > Only the top-level tasks of a project will be displayed here, and the sub-tasks won't be displayed. However, the progress shown for each top level task is based on the percentage of its subtasks that are complete. Intermediate tasks -  ones which have children, don't count towards top-level task progress.

    If you're mapping to a Wrike task within a project, Viva Goals will automatically fetch the details of the subtasks that are a part of the connected Wrike task.

6. Select **Next > Save**.

    :::image type="content" source="../media/goals/goals-wrike-integration.gif" alt-text="Image of Wrike integration save":::

You've successfully linked your project in Viva Goals to a Wrike project or a Wrike task. Viva Goals will now update the progress as tasks and subtasks are completed in Wrike, through hourly syncs. The updates for a project in Viva Goals activity log call out what has changed since the last check-in, tagged with the number of top-level tasks that are added, removed or completed.

## Integrating Key Results in Viva Goals with Wrike projects and tasks 

The progress of key results in VIav Goals can be measured either by percent complete or a KPI metric.

### Measure progress by percent complete 

If you choose to measure the progress of key results by percent complete, this implies that the key result progress is measured by the percent complete of Wrike project or task that is linked to the particular key result. 

### Measure progress by KPI metric 

If you choose to measure the progress of key results by a KPI metric, you'll determine the target value for this metric, and this implies that the key result progress is measured by the starting value and target value of the KPI metric. 

There are two options to track the progress of the KPI metric  — **number of completed tasks in Wrike, and custom fields in Wrike**.  

1. While **creating or editing an OKR** (note: OKR, not project), select **Connect data source to auto-update progress**. From the drop down menu, select **Wrike**.

    :::image type="content" source="../media/goals/goals-wrike-projects-integration-dropdown.png" alt-text="Image of Wrike integration dropdown":::

    If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

2. Choose the method using which you want to measure the progress — KPI (success metric) and provide a metric, starting value, and target value.

3. Provide the permalink of the Wrike project or Wrike task. 

4. From the dropdown menu of **Track progress by**, choose between **Number of completed tasks** and **Custom field value**. 

    If you choose 'Number of completed tasks' to the track the progress of the key result, the tasks (in case of a Wrike project), and subtasks (in case of a Wrike task) will be populated automatically. 

5. If you choose  **Custom field value** to the track the progress of the key result, all the corresponding custom fields of the Wrike project or task will be populated automatically. Choose a custom field that should be considered for updating the progress of the key result. 

    > [!NOTE]
    > Only custom fields that have values set in Wrike will appear in the list. Further, only custom fields with numerical values in Wrike will be shown. 

    :::image type="content" source="../media/goals/goals-wrike-custom-field-selection.png" alt-text="Image of Wrike custom field selection":::

6. Tick the box if you want to use the same field name as the metric name in Viva Goals. 

    :::image type="content" source="../media/goals/goals-wrike-custom-fields-numerical-values.png" alt-text="Image of Wrike custom fields numerical values":::

7. In addition, you can choose the target custom field as well. This is useful for scenarios where you're recording both the current value and the target in separate custom fields in the Wrike project.

8. Select **Next**. Make sure you set a value for **Starting** for KPI depending on whether the metric has to increase or decrease to hit the target. Then select **Save**.

    :::image type="content" source="../media/goals/goals-save-wrike-projects.gif" alt-text="Image of save Wrike project":::

You've successfully linked your key result in Viva Goals to a Wrike project or Wrike task. Viva Goals will now update the key result through hourly syncs. 

Projects in Viva Goals are available across all our pricing plans. If you would like to have Projects enabled for your organization, please have an account admin reach out to support@xxxxxx with your request.    
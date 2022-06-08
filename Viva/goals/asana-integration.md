---
title: "Asana Integration"
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

description: "Learn how to use the Asana integration with your OKRs."
---

# Asana integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## About the Asana integration

Viva Goals can integrate with Asana projects to automatically update your Objectives and Key Results (OKRs) in Viva Goals. The OKRs progress is calculated by the number of tasks or subtasks that have been completed in Asana. This integration works for both types of measuring progress: Percentage Completed or key performance indicator (KPI) progress.

Let's take this example: you're a marketer using Asana to work on a customer advisory project. You would set an objective to curate a list of customer executives onboard from different regions. Use the Asana integration to easily keep track of the completed list. Viva Goals will sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.

## How to set up the Asana integration

An admin can set up the Asana integration in Viva Goals. 

1. Navigate to the Viva Goals integrations page through **Admin -> Integrations**.
    
    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/8/viva-goals-integrations-page.png":::

2. **Enable** the Asana integration.
    
    :::image type="content" source="../media/goals/8/asana-enable-button.png" alt-text="Enabling Asana in Viva Goals." lightbox="../media/goals/8/asana-enable-button.png":::

3. Select **New Connection** and in the popup that follows, sign in to your Asana account. Next, configure Asana connections that can be used by Viva Goals users to link their OKRs and update progress.
    
    :::image type="content" source="../media/goals/8/asana-configure-new-connection.png" alt-text="Configuring new Asana connection in Viva Goals." lightbox="../media/goals/8/asana-configure-new-connection.png":::

4. Select‘**Next** to finish the setup.

Viva Goals allows you to connect with multiple Asana accounts. Select **New connection** to add another and differentiate them using names. These names are displayed to members when they link their OKRs to Asana projects.

## How to use the Asana integration

Once the setup is complete, users in your organization can link their OKRs to Asana projects by performing the following steps:

1. While creating (or editing) an Objective or Key Result, select **Add an integration**.

2. From the list of integrations, pick **Asana**.
    
     :::image type="content" source="../media/goals/8/asana-datasource.png" alt-text="Selecting Asana from the list of data sources in Viva goals." lightbox="../media/goals/8/asana-datasource.png":::

3. Next, select the **Connection**, if multiple exist, and link a project to the objective. To do so, select the name of the project.
    
    :::image type="content" source="../media/goals/8/asana-new-connection-details-viva-goals.png" alt-text="Adding new Asana connection to OKRs in Viva goals." lightbox="../media/goals/8/asana-new-connection-details-viva-goals.png":::

4. To further filter the list of tasks or subtasks, select tasks assigned to a user or pick tasks with a specific status.

5. Select **Next** to finish and save your OKR. You should now see an Asana icon next to the OKR. Viva Goals will automatically count up the finished blog posts. The OKR syncs automatically every hour, but to refresh manually, select **refresh**.

## How to decide between using % Completed vs. KPIs in the Asana integration 

The difference between % Completed and KPI is that with the KPI option you can set a target higher or lower than completing all the tasks in the project.

Let's take this example: you have a project with 100 tasks that spans the entire year. You may choose to use the KPI option and set the target at 25 because each OKR period is only a quarter-long. You would want to track the completion of tasks, but only against the target of 25, not the entire 100 of project completion. 

## How to set up Asana Projects as Projects in Viva Goals

Projects help you keep track of all the work your organization is executing to achieve your Objectives and Key Results (OKRs). Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. Select Add project under the appropriate objective or key result to create a project.

With Viva Goals projects, you can now view your Asana projects inside of Viva Goals. Viva Goals will show you the tasks within the project, and calculate the progress of the project as a percentage based on completed tasks vs. total.

**Viva Goals supports two ways of doing this:**

1. See all the tasks from an Asana project

2. Use a specific Asana task as the project, with its subtasks as the task list

### See all the tasks from an Asana project

Setting up the project in Viva Goals is as easy as connecting to Asana, picking the project, and optionally filtering to a subset of tasks on the project that you care about.

### Use a specific Asana task as the project, with its subtasks as the task list

Some customers like to use a specific task in Asana as their project, with the subtasks as the task list. We support this as well, and you can set your project name in Viva Goals to the name of your Asana task. 

1. Start by adding a project, and select **Add tasks** under **Outcome**.
    
    :::image type="content" source="../media/goals/8/asana-add-tasks-button.png" alt-text="Add tasks button under Progress in Viva goals." lightbox="../media/goals/8/asana-add-tasks-button.png":::

2. In the Tasks field, select the Automatically from a data source option and select Asana as your data source.
    
    :::image type="content" source="../media/goals/8/asana-tasks-connection.png" alt-text="Adding Asana from the list of datasources to Projects in Viva goals." lightbox="../media/goals/8/asana-tasks-connection.png":::

3. Select if you’d like to track progress by the % of tasks completed or by the % of subtasks completed.

4. Search and select the Asana project you’d like to track.

5. Select the Task assigned to field as Any or Unassigned, then select Next and Save.

6. If you’ve chosen to track progress by % of subtasks completed, then enable the Use this task name as the project name in Viva Goals checkbox and save your project.
    
    :::image type="content" source="../media/goals/8/asana-task-connection-details.png" alt-text="Adding an Asana task as a Project in Viva goals." lightbox="../media/goals/8/asana-task-connection-details.png":::

This will create the specific Asana task or subtasks as the project and pull in the subtasks as the task list in Viva Goals.

While Viva Goals supports an Asana integration for OKRs, projects let you see the individual tasks and their completion state, helping you understand your execution at a much deeper level. The updates for a project also call out what has changed since the last check-in - which tasks were completed, were any tasks added or removed.

Viva Goals will periodically check on project progress in Asana, and update status. Progress and Status are calculated for projects exactly like key results. Similar to key results, you can also check in on a project, where you can temporarily override the status. However, this will last only as long as Viva Goals doesn't detect a change in the completion status of the project in Asana, at which point, it will overwrite your check-in with an automated update.

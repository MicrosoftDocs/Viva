---
ms.date: 06/17/2024
title: Asana integration
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
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
description: "Learn how to integrate Asana with your OKRs."
---

# Asana integration

## About Asana integration

Viva Goals can integrate with Asana projects to automatically update your objectives and key results (OKRs) in Viva Goals. OKR progress is calculated by the number of tasks or subtasks that have been completed in Asana. This integration works for both types of measuring progress: percentage completed or key performance indicator (KPI) progress.

Let's take this example: You're a marketer who uses Asana to work on a customer advisory project. You set an objective to curate a list of customer executives onboarded from different regions. Use Asana integration to easily keep track of the completed list. Viva Goals will sync the values for you and chart your progress toward the goal, saving time while keeping your OKRs current.

## How to set up Asana integration

An admin can set up Asana integration in Viva Goals:

1. Go to the Viva Goals integrations page through **Admin** > **Integrations**.

    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/8/viva-goals-integrations-page.png":::

1. **Enable** Asana integration.

1. Select **New Connection**. In the dialog box that opens, sign in to your Asana account. Next, configure Asana connections that can be used by Viva Goals users to link their OKRs and update progress.

    :::image type="content" source="../media/goals/8/asana-configure-new-connection.png" alt-text="Screenshot of the new connection dialog box for Asana in Viva Goals." lightbox="../media/goals/8/asana-configure-new-connection.png":::

1. Select **Next** to finish setup.

Viva Goals lets you connect with multiple Asana accounts. Select **New connection** to add another connection. Connection names are displayed to members when they link their OKRs to Asana projects.

## How to use Asana integration

Once setup is complete, users in your organization can follow these steps to link their OKRs to Asana projects:

1. While creating (or editing) an objective or key result, select **Add an integration**.

2. From the list of integrations, choose **Asana**.

     :::image type="content" source="../media/goals/8/asana-datasource.png" alt-text="Screenshot of the dialog box where you select Asana from the list of data sources in Viva goals." lightbox="../media/goals/8/asana-datasource.png":::

3. Next, select the **Connection**. If there are multiple connections, select the name of the project to link that project to the objective.

    :::image type="content" source="../media/goals/8/asana-new-connection-details-viva-goals.png" alt-text="Screenshot of the dialog box where you add a new Asana connection to OKRs in Viva goals." lightbox="../media/goals/8/asana-new-connection-details-viva-goals.png":::

4. To further filter the list of tasks or subtasks, select tasks assigned to a user or pick tasks that have a specific status.

5. Select **Next** to finish and save your OKR. You should now see an Asana icon next to the OKR. Viva Goals will automatically count the finished blog posts. The OKR syncs automatically every hour. To refresh manually, select **refresh**.

## Decide between using percent completed and KPIs in Asana integration

The difference between percent completed and KPI is that with the KPI option you can set a target higher or lower than completion of all tasks in the project.

Let's consider this example: You have a project with 100 tasks that spans the entire year. You can choose to use the KPI option and set the target at 25 because each OKR period is only a quarter long. You would want to track the completion of tasks but only against the target of 25, not the entire 100.

## How to set up Asana projects as initiatives in Viva Goals

Initiatives help you keep track of all the work your organization is doing to achieve your objectives and key results. Like key results, initiatives can also be created under objectives and under other key results in Viva Goals, depending on which outcome they help to achieve. Select **Add initiative** under the appropriate objective or key result to create an initiative.

With Viva Goals initiatives, you can now view your Asana projects inside Viva Goals. Viva Goals will show you the tasks in the initiative and calculate the progress of the initiative as a percentage based on completed tasks versus the total.

**Viva Goals supports two ways of doing this:**

- See all the tasks from an Asana project

- Use a specific Asana task as the project, with its subtasks as the task list

### See all the tasks from an Asana project

To set up the initiative in Viva Goals, you just connect to Asana, pick the project, and optionally filter to a subset of tasks on the project that you care about.

### Use a specific Asana task as the initiative, with its subtasks as the task list

Some customers like to use a specific task in Asana as their initiative, with the subtasks as the task list. We support this option as well, and you can set your initiative name in Viva Goals to the name of your Asana task.

1. To start, add an initiative, and select **Add tasks** under **Outcome**.

    :::image type="content" source="../media/goals/8/asana-add-tasks-button.png" alt-text="Screenshot shows the add tasks button under Progress in Viva goals." lightbox="../media/goals/8/asana-add-tasks-button.png":::

2. In the Tasks field, select **Automatically from a data source** and select **Asana** as your data source.

    :::image type="content" source="../media/goals/8/asana-tasks-connection.png" alt-text="Screenshot of the dialog box where you add Asana from the list of datasources to initiatives in Viva goals." lightbox="../media/goals/8/asana-tasks-connection.png":::

3. Select whether you’d like to track progress by percent of tasks completed or by percent of subtasks completed.

4. Search and select the Asana project you want to track.

5. Set the **Task assigned to** field to **Any** or **Unassigned**, and then select **Next** and **Save**.

6. If you chose to track progress by percent of subtasks completed, select the **Use this task name as the initiative name in Viva Goals** checkbox, and save your initiative.

    :::image type="content" source="../media/goals/8/asana-task-connection-details.png" alt-text="Screenshot of the final dialog when you add an Asana task as an initiative in Viva goals." lightbox="../media/goals/8/asana-task-connection-details.png":::

This option will create the specific Asana task or subtasks as the initiative and pull in the subtasks as the task list in Viva Goals.

While Viva Goals supports an Asana integration for OKRs, initiatives let you see the individual tasks and their completion state. This helps you understand your execution at a much deeper level. The updates for an initiative also call out what has changed since the last check-in⏤which tasks were completed and whether any tasks were added or removed.

Viva Goals will periodically check on project progress in Asana and update the status. Progress and status are calculated for initiatives exactly like key results. Similar to key results, you can also check in on an initiative, and you can temporarily override the status. This override will last only as long as Viva Goals doesn't detect a change in the completion status of the project in Asana. When that occurs, an automated update will overwrite your check-in.

---
title: "Asana Projects in Viva Goals"
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

description: "Learn how Projects help you keep track of all the work your organization is executing to achieve your OKRs."
---

# Asana Projects in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Projects help you keep track of all the work your organization is executing to achieve your Objectives and Key Results (OKRs). Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. Select **Add project** under the appropriate objective or key result to create a project.

## What are Asana projects in Viva Goals?

With Viva Goals projects, you can now view your Asana projects inside of Viva Goals. Viva Goals will show you the tasks within the project, and calculate the progress of the project as a percentage based on completed tasks vs total.

Viva Goals supports two ways of doing this: See all the tasks from an Asana project, and use a specific Asana task as the project, with its subtasks as the task list.

## See all the tasks from an Asana project

Setting up the project is as easy as connecting to Asana, picking the project, and optionally filtering to a subset of tasks on the project that you care about.

:::image type="content" source="../media/goals/ally-asana-integ-1.gif" alt-text="See tasks from Asana project":::

## Use a specific Asana task as the project, with its subtasks as the task list

Sometimes, our customers like to use a specific task in Asana as their project, with the subtasks as the task list. We support this as well, and you can set your project name in Viva Goals to the name of your Asana task. To do so:

1. Start by adding a project, and select the **Automatically based on completed tasks** option to calculate progress.

2. In the **Tasks** field, select the **Automatically from a data source** option and select **Asana** as your data source.

3. Select if you’d like to track progress by the % of tasks completed or by the % of subtasks completed.

4. Search and select the Asana project you’d like to track.

5. Select the **Task assigned to** field as **Any** or **Unassigned**, then select **Next** and **Save**.
  
If you’ve chosen to track progress by % of subtasks completed, then:

1. Enable the **Use this task name as the project name in Viva Goals** checkbox.

2. Select **Next** and **Save** to save your project! This will create the specific Asana task or subtasks as the project and pull in the subtasks as the task list in Viva Goals.

:::image type="content" source="../media/goals/ally-asana-project-subtask.gif" alt-text="Project Subtask":::

:::image type="content" source="../media/goals/viva-goals-create-asana-task.png" alt-text="Create Asana task":::

While Viva Goals supports an [Asana integration](https://help.ally.io/en/articles/2615109-asana-integration) for OKRs, projects let you see the individual tasks and their completion state, helping you understand your execution at a much deeper level. The updates for a project also call out what has changed since the last check-in - which tasks were completed, were any tasks added or removed.

:::image type="content" source="../media/goals/viva-goals-task-completion-state.png" alt-text="Task completion state":::

:::image type="content" source="../media/goals/viva-goals-task-completed-status.png" alt-text="Task completed status":::

Viva Goals will periodically check on project progress in Asana, and update status. Progress and Status are calculated for projects exactly like [key results](https://help.ally.io/en/articles/3065807-okr-status-indicators). Similar to key results, you can also check in on a project, where you can temporarily override the status. However, this will last only as long as Viva Goals doesn't detect a change in the completion status of the project in Asana, at which point, it will overwrite your check-in with an automated update.

:::image type="content" source="../media/goals/viva-goals-periodic-progress-check.png" alt-text="Periodic progress check":::

Now you can understand how your teams are executing to meet your OKRs, and dive in to unblock them. In the future, we plan to add other popular project management systems, so that Viva Goals can give you a holistic view of your business.

Projects in Viva Goals are available across all our pricing plans. If you would like to have Projects enabled for your organization, please have an account admin reach out to [support@ally.io](mailto:support@ally.io) with your request.

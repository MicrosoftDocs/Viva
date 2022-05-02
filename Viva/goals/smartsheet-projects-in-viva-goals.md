---
title: "Smartsheet Projects in Viva Goals"
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

description: "Learn how to view your Smartsheet project execution directly in Viva Goals."
---

# Smartsheet Projects in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## What are Projects in Viva Goals?

Projects help you keep track of all the work your organization is executing to achieve your Objectives and Key Results (OKRs). While key results track outcomes, projects track the output that helps you achieve your key results. For more information and best practices, see [What are Projects?](https://help.ally.io/en/articles/4224975-what-are-projects)

## Viva Goals Projects and Smartsheet

You can now view your Smartsheet projects, and the tasks within the project in Viva Goals. You can treat the entire sheet as a project, or use a specific Smartsheet row as the project, with its children as the task list. If progress is available in Smartsheet, Viva Goals will use it. Otherwise, it will compute it from the child tasks.

## How do I set up Smartsheet integration?

- From the navigation menu, go to **Admin** and select the **Integrations** tab.

- Against Smartsheet, you'll have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration.

- Select **New Connection** and follow the prompt to sign into Smartsheet.

- Name your connection, and select **Next** to complete the setup.

- This integration can also be **disabled** from the same section. Go to **Change**  and select **Disable integration** from the dropdown.

    :::image type="content" source="../media/goals/Enabling Smartsheet integration.gif" alt-text="Smartsheet-projects-1":::

Viva Goals allows you to connect with multiple Smartsheet accounts. Select **New Connection** to add another instance and use names to differentiate them. These names are displayed to members when they link their OKRs to Smartsheet cells.

> [!NOTE]
> All connections are publicly available for use by everyone in the organization.

## How do I start populating Smartsheet Projects?

How Viva Goals tracks progress of projects in Smartsheets is called out in the **Calculating Project Progress** section. Regarding what can be considered a project, Viva Goals supports two modes for Smartsheet projects:

1. **Treat the entire sheet as the project**: Here Viva Goals would show the top-most level of tasks from the Smartsheet in Viva Goals, with progress rolled up from the children. The project name is taken from the sheet's name.

    :::image type="content" source="../media/goals/viva-goals-smartsheet-projects-2.png" alt-text="Smartsheet Projects 2":::

    :::image type="content" source="../media/goals/Smartsheet as project in Viva Goals.gif" alt-text="Smartsheet Projects 3":::

2. **Use a specific Smartsheet row as the project, with its children as the task list**: Sometimes, our customers like to have several projects in the same Smartsheet. We support this as well. The name of the task becomes the project name in Viva Goals and its direct children become the task list.

    :::image type="content" source="../media/goals/viva-goals-smartsheet-projects-4.png" alt-text="Smartsheet Projects 4":::

    :::image type="content" source="../media/goals/Smartsheet-Row as project in Viva Goals.gif" alt-text="Smartsheet Projects 5":::

## How to calculate Project Progress?

Viva Goals supports the standard project template in Smartsheet, but is flexible to allow sheets that don't use this template.

If your Smartsheet uses the Project template, Smartsheet can automatically roll up task progress based on subtask percent complete and duration. You can tell if your sheet uses the template by checking if there's a Project Settings (gear) icon under the **Share** button on the top-right of the sheet. Within the Project Settings, if Dependencies are enabled, a Duration column will also be set which will be used to weight task progress by duration - longer tasks count more towards parent task progress. Details on how Smartsheet does these rollups and calculates progress can be found [here](https://help.smartsheet.com/articles/765753-parent-rollup-functionality).

:::image type="content" source="../media/goals/Project settings in Smartsheet.gif" alt-text="Smartsheet Projects 6":::

The following table shows the various possibilities and how Viva Goals calculates progress in each case. Overall, if a Duration field is specified when the connection is set up in Viva Goals, Viva Goals will use it to weight task progress: the contribution is the duration of the task relative to the sum of all task durations. If there's no Duration field, Viva Goals will fall back to calculating the average percentage progress across all tasks.

### Case 1

- Project template: Enabled

- Dependencies: Enabled

- Duration field: Mapped (mandatory when dependencies are enabled)

The progress of the parent task in Smartsheet isn't editable, and is calculated by Smartsheet. Viva Goals will mirror the progress.  

Viva Goals calculates the sheet-level progress the same way Smartsheet calculates the progress of parent task (the progress of top-level tasks in the Sheet).  

If more than 50% of the **Duration** field or the **% complete** field for top-level tasks can't be parsed, Viva Goals will show a sync error.

### Case 2

- Project template: Enabled

- Dependencies: Disabled

- Duration field: Mapped

If Dependencies is disabled, Smartsheet won't roll up progress to the parent tasks. If the **Duration** column has raw numbers, Viva Goals will assume they are days. However, Viva Goals still supports the Smartsheet notation of days and weeks (for instance, 4d for four days, 2w for two weeks).  

When a task is used as the project with subtasks as the project's tasks, if there's no **% complete** filled in for the task, Viva Goals will calculate it. However, even if one is filled in, Viva Goals will assume the user knows best, and will use the value as is for the project progress. If the value is filled in but not parseable, Viva Goals will show the project progress as 0%.

If more than 50% of the **Duration** field or the **% complete** field for top-level tasks can't be parsed, Viva Goals will show a sync error.

### Case 3

- Project template: Enabled

- Dependencies: Disabled

- Duration field: Not Mapped

If Dependencies is disabled, Smartsheet won't roll up the progress to parent tasks. Since a duration column isn't mapped, Viva Goals will assume the parent task's progress is just the average of the first-level of child tasks' progress. The same logic is applied while calculating the progress at a sheet-level (if the entire sheet is a project).  
  
If more than 50% of the **% complete** field for top-level tasks can't be parsed, Viva Goals will show a sync error.

### Case 4

- Project template: Disabled

- Dependencies: Doesn't Apply

- Duration field: Mapped

If the **Duration** column has raw numbers, Viva Goals will assume they are days. However, Viva Goals still supports the Smartsheet notation of days and weeks (for instance, 4d for four days, 2w for two weeks).

When a task is used as the project with subtasks as the project's tasks, if there's no **% complete** filled in for the task, Viva Goals will calculate it. However, even if one is filled in, Viva Goals will assume the user knows best, and will use the value as is for the project progress. If the value is filled in but not parseable, Viva Goals will show the project progress as 0%.  
  
If more than 50% of the **Duration** field for top-level tasks can't be parsed, Viva Goals will show a sync error.

### Case 5

- Project template: Disabled

- Dependencies: Doesn't Apply

- Duration field: Not Mapped

Since a duration column isn't mapped, Viva Goals will assume the parent task's progress is just the average of the first-level of child tasks' progress. The same logic is applied while calculating the progress at a sheet-level (if the entire sheet is a project).  
  
If more than 50% of the **% complete** field for top-level tasks can't be parsed, Viva Goals will show a sync error.

> [!NOTE]
> Top-level tasks, here, is relative to whether the entire sheet is a project, or if a specific row is a project.

## Smartsheet Key Result Integration vs Projects

Viva Goals supports a [Smartsheet integration](https://help.ally.io/en/articles/2392879-smartsheet-integration) for Key Results as well, which lets you map a single cell of the Smartsheet to a success metric for a key result. The progress of the key result is updated in real time as the cell value changes. This makes sense when you use Smarthsheet as a spreadsheet, not really for project tracking.

The Projects Smartsheet integration, however, lets you see the individual tasks and their completion state for a Smartsheet, helping you understand your execution at a much deeper level. The updates for a project also call out what has changed since the last check-in - which tasks were completed, were any tasks added or removed. You can also directly jump to the row in Smartsheet from the task in Viva Goals.

:::image type="content" source="../media/goals/Update progress from Smartsheet.gif" alt-text="Smartsheet Projects 7":::

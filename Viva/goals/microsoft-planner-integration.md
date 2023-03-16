---
ms.date: 12/21/2022
title: "Microsoft Planner Integration"
ms.reviewer: 
ms.author: rasanders
author: rasanders
manager: Liz.Pierce
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

description: "Learn how to integrate your Viva Goals OKRs with Microsoft Planner."
---

# Microsoft Planner Integration

Viva Goals integrates with Microsoft Planner to automatically update key results and projects in Viva Goals. OKR and project progress is automatically calculated based on the completion of tasks in Planner. You can connect to Planner as a data source to automatically update three different capabilities in Viva Goals: track progress for a key result, project, and project KPI. View examples below of how the MS Planner integration works for each of these capabilities. 

## When to use the Microsoft Planner Integration  

Track progress for a key result: Use the Planner integration to automatically track progress towards your key results. For example, if your key result is “Deliver new ad campaign,” you can show the progress towards delivering the new ad campaign by connecting to the plan where you track your marketing tasks. 

Track progress for a project with tasks: Use this option when you want to track progress based on completion of all tasks in the project and have visibility to your Planner tasks in Viva Goals. For example, if your project is to “Update marketing materials,” you can connect to the plan where you track marketing content tasks to automatically update your project in Viva Goals. After you connect to Planner as a data source for tasks, you will be able to select how you want to automatically track progress from your plan and view the tasks from that plan within Viva Goals. 

Track progress for a project with project KPIs: Project KPIs give you the ability to set targets for task completion in Planner that are higher or lower than the completion of all tasks in a plan. For example, if you have a project KPI to “Add 5 product videos to your website,” you can add a metric in your project to reach 5 completed tasks in your plan.  

## How to set up Microsoft Planner Integration 

By default, Microsoft Planner is available as an integration in Viva Goals. Tenant admins should follow the instructions in [Enable Integrations in Viva Goals | Microsoft Learn](vg-integrations-administration-overview.md) to manage the Planner integration. 

### How to use Microsoft Planner to track progress for a key result  

1. While creating or editing a key result, select **Progress**. 
1. Select **Automatically from a data source**. 
1. Select **Planner** from the list of available integrations. 
1. The first time you connect to Planner from Viva Goals, you may be prompted to sign into Planner. Sign in and select Next. 
1. Select the name of the Plan you want to connect to your key result. 
1. Optional: select if you want to filter tracking progress based on who the tasks are assigned to. 
1. Select how you want to track progress from two options: 
    1. **Number of tasks completed:** Use this selection to update progress of the key result when task progress is updated to Completed in Planner.
    1. **Percentage of tasks completed:** Use this selection to update progress of the key result when task progress is updated to In Progress and Completed in Planner. If a task is updated to In Progress, Viva Goals will calculate that 50% of the task is complete and reflect that in the progress of the key result.
1. Select **Next**. 
1. Select **Create** or **Save** to save your key result. You should now see the Planner icon next to your key result. Viva Goals will now automatically update this Key Result once per hour based on the progress of the tasks in Planner. 

### How to use Microsoft Planner to track progress for a Project with tasks

1. Select **Add Project** in Viva Goals or edit an existing project. 
1. Select **Outcome**. 
1. Select **Add tasks**. 
1. Select **Automatically from a data source**. 
1. Select **Planner** from the list of available integrations. 
1. The first time you connect to Planner from Viva Goals, you may be prompted to sign into Planner. Sign in and select Next. 
1. Select the name of the plan you want to connect to your project. 
1. Optional: select if you want to filter tracking progress based on who the tasks are assigned to 
1. Select how you want to track progress from two options:
    1. **Number of tasks completed:** Use this selection to update progress of the project when task progress is updated to Completed in Planner.
    1. **Percentage of tasks completed:** Use this selection to update progress of the project when task progress is updated to In Progress and Completed in Planner. If a task is updated to In Progress, Viva Goals will calculate that 50% of the task is complete and reflect that in the progress of the key result. When a task is updated to Complete, Viva Goals will calculate that 100% of that task is complete.
1. Select **Next**. 
1. Select **Save** to save your project. You should now see the Planner icon next to your project. Viva Goals will now automatically update this project once per hour based on the progress of the tasks in Planner. 

You can view the tasks from Planner in Viva Goals by selecting Tasks or Open detail view from the project overview. 

### How to use Microsoft Planner to track progress with a project KPI 

1. Select **Add Project** in Viva Goals or edit an existing project. 
1. Select **Outcome**. 
1. Select **Add Metric**. 
1. Add details for the Metric name and target. 
1. Select **Progress**.  
1. Select **Automatically from a data source** (KPI). 
1. Select **Planner** from the list of available integrations. 
1. The first time you connect to Planner from Viva Goals, you may be prompted to sign into Planner. Sign in and select Next. 
1. Select the name of the plan you want to connect to your project. 
1. Optional: select if you want to filter tracking progress based on who the tasks are assigned to 
1. Select how you want to track progress from two options:
    1. **Number of tasks completed:** Use this selection to update progress of the project when task progress is updated to Completed in Planner.
    1. **Percentage of tasks completed:** Use this selection to update progress of the project when task progress is updated to In Progress and Completed in Planner. If a task is updated to In Progress, Viva Goals will calculate that 50% of the task is complete and reflect that in the progress of the key result. When a task is updated to Complete, Viva Goals will calculate that 100% of that task is complete.
1. Select **Next**. 
1. Select **Save** to save your project. You should now see the Planner icon next to your project. Viva Goals will now automatically update this KPI once per hour based on the progress of the tasks in Planner.  

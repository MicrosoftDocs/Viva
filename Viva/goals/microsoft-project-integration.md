---
ms.date: 08/02/2023
title: "Microsoft Project for the Web Integration with Viva Goals"
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

description: "Learn how to integrate your Microsoft Project for the Web with Viva Goals."
---

# Microsoft Project for the web integration

Viva Goals integrates with Microsoft Project for the Web to automatically update key results and initiatives in Viva Goals. OKR and initiatives progress is automatically calculated based on the completion of tasks in Project.  

You can connect to Project for the Web as a data source to automatically update three different capabilities in Viva Goals: track progress for a key result, track progress for an initiative, and track progress for an initiative’s KPI. View examples below of how the MS Project for the Web integration works for each of these capabilities. 

## When to use the Microsoft Project for the web integration 

**Track progress for an initiative with tasks (recommended):** Use this option when you want to track progress based on completion of all tasks in the initiative and have visibility to your Project tasks in Viva Goals. For example, if your initiative is to “Update marketing materials,” you can connect to the plan where you track marketing content tasks to automatically update your initiative in Viva Goals. After you connect to Project for the Web as a data source for tasks, you'll be able to select how you want to automatically track progress from your plan and view the tasks from that plan within Viva Goals. 

**Track progress for an initiative with initiative KPIs:** initiative KPIs give you the ability to set targets for task completion in Project that are higher or lower than the completion of all tasks in a plan. For example, if you have an initiative KPI to “Add 5 product videos to your website,” you can add a metric in your initiative to reach five completed tasks in your Project. 

**Track progress for a key result:** Use the Project for the Web integration to automatically track progress towards your key results. For example, if your key result is “Deliver new ad campaign,” you can show the progress towards delivering the new ad campaign by connecting to the Project where you track your marketing tasks. 

## How to set up the Microsoft Project Integration 

By default, Microsoft Project for the Web is available as an integration in Viva Goals. Tenant admins should follow the instructions in [Enable Integrations in Viva Goals | Microsoft Learn](vg-integrations-administration-overview.md) to manage the Project integration. 

## How to use Microsoft Project for the Web to track progress for Initiatives with tasks 

1. Select **Add initiatives** in Viva Goals or edit an existing initiative. 
1. Select **Outcome**. 
1. Select **Add tasks**. 
1. Select **Automatically from a data source**. 
1. Select **Project** from the list of available integrations. 
1. The first time you connect to Project for the Web from Viva Goals, you may be prompted to sign into Project. Sign in and select Next. 
1. Select the name of the [Environment](/azure/deployment-environments/overview-what-is-azure-deployment-environments) to fetch the list of Projects. Note: Most Projects are in the default environment. If you don't know the environment your Project is in, it's likely in the default environment.
1. Select the name of Project you want to connect to your Key Result
1. **Optional**: Select the Bucket to filter tasks within a Project.
1. **Optional**: Select if you want to filter tracking progress based on who the tasks are assigned to. Unassigned can also be used to select all unassigned tasks in the Project.
1. Select how you want to track progress from two options: 
    1. **Number of tasks completed:** Use this selection to update progress of the initiative when task progress is updated to Completed in Project. 
    1. **Percentage of tasks completed**: Use this selection to update progress of the initiative when task progress is updated to In Progress and Completed in Project. If a task is updated to In Progress, Viva Goals will calculate that 50% of the task is complete and reflect that in the progress of the key result. When a task is updated to Complete, Viva Goals will calculate that 100% of that task is complete. 
1. Select **Next**. 
1. Select **Save** to save your initiative. You should now see the Project for the Web icon next to your initiative. Viva Goals will now automatically update this initiative once per hour based on the progress of the tasks in Project. 

You can view the tasks and due date for tasks from Project in Viva Goals by selecting Tasks or Open detail view from the initiative overview. 

## How to use Microsoft Project to track progress with an initiative KPI 

1. Select **Add initiative** in Viva Goals or edit an existing initiative. 
1. Select **Outcome**. 
1. Select **Add Metric**. 
1. Add details for the Metric name and target. 
1. Select **Progress**. 
1. Select **Automatically from a data source (KPI)**. 
1. Select **Project** for the Web from the list of available integrations. 
1. The first time you connect to Project from Viva Goals, you may be prompted to sign into Project. Sign in and select Next. 
1. Select the name of Project you want to connect to your Key Result 
1. **Optional**: Select the Bucket to filter tasks within a Project 
1. **Optional**: Select if you want to filter tracking progress based on who the tasks are assigned to. Unassigned can also be used to select all unassigned tasks in the Project 
1. Select how you want to track progress from two options: 
    1.**Number of tasks completed:** Use this selection to update progress of the initiative when task progress is updated to Completed in Project. 
    1. **Percentage of tasks completed:** Use this selection to update progress of the initiative when task progress is updated to In Progress and Completed in Project. If a task is updated to In Progress, Viva Goals will calculate that 50% of the task is complete and reflect that in the progress of the key result. When a task is updated to Complete, Viva Goals will calculate that 100% of that task is complete. 
1. Select **Next**. 
1. Select **Save** to save your initiative. You should now see the Project for the Web icon next to your initiative. Viva Goals will now automatically update this KPI once per hour based on the progress of the tasks in Project.

## How to use Microsoft Project to track progress for a key result 

1. While creating or editing a key result, select **Progress**. 
1. Select **Automatically from a data source**. 
1. Select **Project for the Web** from the list of available integrations. 
1. The first time you connect to Project from Viva Goals, you'll be prompted to sign into Project for the Web. Sign in and select Next. 
1. Select the name of the [Environment](/azure/deployment-environments/overview-what-is-azure-deployment-environments) to fetch the list of Projects.
1. Select the name of Project you want to connect to your Key Result.
1. **Optional**: Select the Bucket to filter tasks within a Project.
1. **Optional**: Select if you want to filter tracking progress based on who the tasks are assigned to. Unassigned can also be used to select all unassigned tasks in the Project.
1. Select how you want to track progress from two options: 
    1. **Number of tasks completed:** Use this selection to update progress of the key result when task progress is updated to Completed in Project. 
    1. **Percentage of tasks completed:** Use this selection to update progress of the key result when task progress is updated to In Progress and Completed in Project. If a task is updated to In Progress, Viva Goals will calculate that 50% of the task is complete and reflect that in the progress of the key result. 
1. Select **Next**. 
1. Select **Create** or **Save** to save your key result. You should now see the Project for the Web icon next to your key result. Viva Goals will now automatically update this Key Result once per hour based on the progress of the tasks in Project. 
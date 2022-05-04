---
title: Configure your OKR rules in Viva Goals
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
description: "Learn how to configure your OKR rules in Viva Goals"
---

# Configure your OKR model in Viva Goals

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals understands that every business has its own set of processes, and lets you configure and create your own OKR rules to fit your business needs. 

## Configure your OKR Rules 

1.	On the left panel of the Viva Goals application, select **Admin**.
2. In the **Admin Dashboard** section, select the **OKR Model Configuration** tab. 
2.	Define your Objectives, Key Results, and Projects as laid out in the following sections.

### Define objectives

By default, objectives are defined as aspirational with measurable key results.

Having your objectives defined as aspirational with measurable key results is the classic style of doing OKRs. Your objectives will record progress from 0% to 100%; progress will by default be rolled up from key results, or you can choose to update progress manually. Your key results will have a metric associated with them.

:::image type="content" source="../media/goals/Goals-classic.png" alt-text="Image of the classic":::

Once you define your objectives as aspirational and key results as measurable, you'll find the following set of options: 

#### Allow objectives to be nested under key results

You can decide if you wouldlike to nest your objectives under key results. Enable this option when your organization often defines metrics to drive that are large enough in scope to require a set of objectives.

#### Block objectives from ever contributing to the progress of their parent

Enable the 'Block objectives' option if you never want child objectives in your organization to contribute to the progress of their parents. Users will never be able to override and edit the contribution settings. 

> [!NOTE]
> Existing objectives that are already contributing to their parents will remain untouched. If you edit such objectives, the only option allowed would be to set the contribution to 0.

:::image type="content" source="../media/goals/Goals-configure-objectives.png" alt-text="Image of the Configuring objectives":::

### Define key results 

#### Allow key results to be nested under key results.

Select this option if your organization often breaks down a key result’s metrics into parts.

 :::image type="content" source="../media/goals/Goals-configure-keyresults.png" alt-text="Image of the Configuring key results":::

### Define projects

The Projects section covers project enablement, alignment, and contribution options.

:::image type="content" source="../media/goals/Goals-configure-projects.png" alt-text="Image of the define projects":::

#### Enable projects

Projects are the activities which drive towards your key results (your outcomes). Enable this option if you want projects reflected in your instance of Viva Goals.

- **Enable projects for specific users**

    Select this checkbox if you want a few users in your organization to try out the projects feature before you roll it out more broadly. Only these specific users will be able to add projects. The projects created by these users will be visible to everyone. Search and select the list of users you’d want to enable projects for and save. 

- **Allow projects to be nested under key results**

    Select this option if you want users to be able to create projects focused on moving a single key result, rather than the overall objective.

- **Define how projects should contribute**

    Select how projects should contribute to the progress of its parent. 

     - Projects contribute to the progress of their parent by default 
            
     - Projects do not contribute to the progress of their parent by default 
            
     - Block projects from ever contributing to the progress of their parent

- **Rename projects**

    Define what you want projects to be called. You can rename the default label and call projects Initiatives, Tactics, or anything else. This changr will be reflected across your instance of Viva Goals.

## Saving your OKR Model Configuration Settings

Select **Save** once you have chosen the settings that define your objectives, key results, and projects. The changes will take effect once you select **Yes, Switch** in the confirmation pop-up. 

> [!NOTE]
> Existing OKRs and Projects will remain untouched. Changes will be applied only to OKRs and Projects created after new settings are saved.

:::image type="content" source="../media/goals/Goals-OKR-model-configuration-setting.png" alt-text="Image of the OKR model configuration":::

## Objectives and Key Results (OKR) progress bar customization

Viva Goals supports a progress bar customization setting. This allows admins to override the current automatic scoring system.

Viva Goals assesses progress in two ways: Actual and Expected. By default, Viva Goals calculates the expected progress percentage based on the 'Start date' and 'End date' as specified by the user for the OKR. The actual progress is updated automatically via a data integration or the roll-up of key results to an objective for auto computed OKRs.

The default progress ranges within Viva Goals are:

- If the difference between expected progress and aggregate progress is greater than 25%, then the status will be mapped as **At Risk**.

- If the difference between expected progress and aggregate progress is between 0% & less than or equal to 25%, then the status will be mapped as **Behind**.

- If the difference between expected progress and aggregate progress is less than or equal to 0%, then the status will be mapped as **On Track**.

However, admins no longer need to stick to these progress ranges and can custom configure them based on the guidelines and policies that they follow within their respective organizations.

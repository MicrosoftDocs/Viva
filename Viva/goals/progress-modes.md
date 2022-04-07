---
title: Progress modes
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
description: "Learn how OKRs are updated, and have greater control over updating the progress"
---

# Progress Modes

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Engaging everyone with the company goals and driving greater OKR adoption is the primary responsibility of OKR champions and team managers. Better visibility into how the progress is updated will help them understand the user’s engagement with the objective.

## Types of progress modes

Progress mode indicates how the progress of an OKR is updated. Increased visibility of the progress update helps users in better understanding their engagement with an objective. In addition, you can have greater control over determining the progress mode of an objective, and change it as you see fit. There are three methods of updating the progress, which are described in the following table:

|Method  |Description  |
|---------|---------|
|Manually     |  Progress of the objective will be determined by the objective owner through a registration made manually.        |
|Automatic via rollup from children     |     Progress of the objective will be rolled up automatically from the key results.     |
|Automatically from a data source     |     Progress of the objective will be updated automatically based on the data from an integration.     |

### Identifying the progress mode

If your OKR is measuring progress by percent of completion, it can be in one of the three progress modes described in the following table:

|Mode  |Description  |
|---------|---------|
|Manual     |  In this mode, the progress and status can only be changed by the users making registrations.        |
|Automatic via rollup from children     |     In this mode, the progress and status will be updated as children update their progress and status. This mode is the default mode every OKR starts in.     |
|Automatically from a data source     |     In this mode, progress will come from an integrated data source, and status updates will be based on the progress.     |

> [!NOTE]
> If you have Projects in Viva Goals, you can register yourself on these projects manually. When you switch to the automated mode, the progress will roll up from tasks beneath the projects — these tasks can either be added in Viva Goals directly, or through an integration. For more information on the Projects integrations supported, see [Projects](https://help.ally.io/en/articles/4224975-what-are-projects).

:::image type="content" source="../media/goals/identifying-progress-mode.gif" alt-text="Identifying the progress mode":::

## Setting the progress mode for an OKR

**When creating or editing your objective**

When you create or edit an objective, you can determine how the progress will be updated. If your objective is measured by percent of completion, you'll have three progress modes to choose from — manually, automatic via roll-up from children, automatically from a data source. However, if your objective is measured with a KPI, you won't be able to update the progress via roll-up because we don't want to override the metric. You''ll have to automate the update through an integration, or register manually.

:::image type="content" source="../media/goals/create-or-edit-objective.gif" alt-text="Create or edit an objective":::

**From the list view**

The icon to the left of the progress bar is indicative of the progress mode. You can select the icon to change the progress mode, or you can make a registration instantly by leveraging the slider progress bar.

:::image type="content" source="../media/goals/list-view.gif" alt-text="List view":::

**When making a registration**

If the progress of your objective is updated automatically, you can make a registration and switch to the manual progress mode in which case, the automatic progress will be overridden by the manual registration. You can always switch back to previous progress mode to resume updating the progress automatically from the children or the connected data source.

If the progress is rolled up automatically from the key results, perform the following steps:

1. Select the rollup icon and select the **Check-in** button.
1. Make a registration as you see fit and save it. You'll notice the change in the icon that represents the manual mode.
1. To switch back to the previous mode, select the manual icon and select the **Check-in** button.
1. Save this registration as you'll have the option to resume updating the progress from key results.

If the progress is rolled up automatically through an integration, perform the following steps:

1. Select the integration icon and select the **Check-in** button.
1. Make a registration as you see fit and save it. You'll notice the change in the icon that represents the manual mode.
1. To switch back to the previous mode, select the manual icon and select the **Check-in** button.
1. Save this registration as you'll have the option to resume updating the progress through the connected data source.

## Check-in reminders

If you switch an OKR or a project into the manual override progress mode, you'll receive registration reminders for it as long as it stays in the manual mode. Once you revert it to the automated progress mode, whether by rollup or from integration, you'll no longer receive reminders for registration.

### Common questions

1. When would I want to keep my objective in manual progress mode instead of having it update automatically?

   When you choose to update the progress automatically (through an integration or a rollup from children), the progress of the objective will be updated automatically based on the data fetched from the data source, or will roll up based on the progress of children. However, in some cases, this automated progress update might not accurately reflect the progress made on the objective. In such cases, you can override the automated progress update, and make a registration as you see fit. This registration that you make manually will not be overridden by the data from the integrated source or from the children until you change the progress mode back to automated. This registration will give you the much-needed control over progress updates to present accurate data during reviews.

2. Can I make a check-in by simply adding a note and changing the values of progress and status, without changing the progress mode?

   Yes, you can make a manual registration to override the automatic values, and still choose to retain the automated progress mode. When you make a manual registration, you'll find a checkbox to stop updating the progress automatically. By not checking this checkbox, you can retain the automated progress mode.
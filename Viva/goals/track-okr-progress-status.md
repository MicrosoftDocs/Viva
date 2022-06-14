---
title: Track OKR progress status in Viva Goals
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
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how progress status is calculated in Viva Goals and how to track it. "
---

# Track progress status in Viva Goals 

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## OKR Progress

Each OKR in Viva Goals contains a progress bar that displays the last identified progress. Viva Goals assesses progress in 2 ways: Actual and Expected. 

- **Actual Progress**:  Indicated by the progress bar itself and the % denoted against it. You will also find the actual progress percentage right below the progress bar as well. 

- **Expected Progress**: Indicated by the grey vertical line on the progress bar.

## How expected progress is calculated

Viva Goals calculates the expected progress % based on the 'Start date' and 'End date' specified by the owner of the OKR. The progress bar and graph below is found on the objectives' quick view. (Click on the objective name to open up the objective’s quick view). You can also click on the ‘full view’ of the OKR to view the progress graph. 

> Note: 

> On the first day of the time period, the expected progress would be 0%.

> On the final day of the time period, the expected progress would be 100%.

## How Actual Progress is calculated

Actual Progress is determined when the user makes a check-in to the OKR either automatically via a data integration or via the roll-up of Key Results to an objective. 

For manual check-ins, a progress % or KPI value must be explicitly added by the user.

You will also see under the progress bar how and when the last update was made, the % complete or KPI,  along with the notes left at the time of check-in and who made the update when the 'Show more info' on the dashboard list view is turned on.

## How to manually override OKR progress and status

While it is highly recommended to automate OKR progress updates either through an integrated data source, or via rollup from children objectives, the OKR owner might have better context on progress. In such cases, you can manually override the automated progress and status, and set them as you see fit. 

1. To the left of the progress bar, you'll find an icon that is indicative of the current progress mode. 

2. Upon clicking this icon, you'll find the option to make a check-in. Here, you'll find the current progress and status of the objective based on the automatic update. Select ‘Edit progress and status’ to make a manual check-in. 

3. Set the progress and status as you see fit. If you want to continue making manual check-ins, and choose to stop the automatic updates for this objective, tick the checkbox that’s right underneath to stop updating via rollup from children or an integrated source. 

4. If you don't tick this checkbox, you're choosing to stay in the automated progress mode but you'll manually override the progress and status as a one-off instance. The next automatic update will override the manual check-in you're making. 

5. Save your check-in. 

When you manually override the progress and status and choose to stop the automatic updates, the next automatic update will not take effect unless you choose to do so. 

However, every time you make a check-in, Viva Goals will show you what the automatic values would be. You can decide whether to continue making manual check-ins or revert to the automated mode of updating progress.

### How to resume automatic updates

You can exit from the manual override mode and resume automatic updates by following these steps: 

1. Select the manual progress mode icon, and start a check-in.

2. You will be shown the automatic values, and you will see an option to resume the automated updates. 

3. Select **Resume updating automatically from key results** (in case of progress rolled up from children) or ‘Resume updating automatically from an integrated data source’ (in case progress is updated through the integration). 

4. The progress and status will take the automatic values, and the progress mode will be reverted to automated mode.

5. Save your check-in.

## Status

Viva Goals lets you validate and indicate the progress of your OKRs with a status. OKR statuses are color-coded and below are the definitions of the different status colors:

:::image type="content" source="../media/goals/status-colours-viva-goals.png" alt-text="Different OKR colours in Viva Goals." lightbox="../media/goals/status-colours-viva-goals.png":::

When the status is manually set by a user, say, for example, a user checks in and marks status as ‘On Track’, the progress bar will show status as ‘On Track’.
 
When the status is automatically set by Viva Goals (for data integrated OKRs or parent objectives having progress rolled up from key results), there are two ways in which the status can get updated currently.

- Status derived based on Progress

- Status derived based on Key Results

### Status derived based on 'Progress'

Status will be calculated based on the progress updates of that particular objective or key result.

In cases where all the key results of an objective have 'Postponed' or 'Closed' as the status, then the parent objective’s status will automatically be marked as 'Postponed' or 'Closed' respectively irrespective of the Progress %. Here’s how status is calculated based on the progress updates for an OKR: 

- If (Expected Progress - Aggregate Progress > 25%) , then At Risk

- If (Expected Progress - Aggregate Progress > 0% & <=25%) , then Behind

- If (Expected Progress - Aggregate Progress <= 0%) , then On Track

For example, the objective ‘Wow the market with a revolutionary product’ has three key results that contribute to its progress. The objective’s status will be derived on the progress %. In the example, the expected progress of the objective is at 52% and the actual progress is at 47%. Since (Expected Progress - Aggregate Progress > 0% & <=25%)  the status is derived as ‘Behind’. 

### Status derived based on 'Key Results'

When the status is derived based on ‘key results’, the status of the parent objective is set based on the status of the key result. If key results have Closed or Not Started status, the parent objective’s status is calculated as follows: 

- If (Expected Progress - Aggregate Progress > 25%) , then At Risk

- If (Expected Progress - Aggregate Progress > 0% & <=25%) , then Behind

- If (Expected Progress - Aggregate Progress <= 0%) , then On Track

When any of the key results do not have Closed or Not Started status, and have any of the below statuses in order of precedence, the parent objective's status sets to this value:

1. At Risk

2. Behind

3. On Track

4. Not Started

In cases where all the key results of an objective have 'Postponed' or 'Closed' or ‘Not Started’ as the status, then the parent objective’s status will automatically be marked as 'Postponed' or 'Closed' or ‘Not Started’. 

## OKR Progress Bar Customization

Viva Goals now supports a progress bar customization setting using which admins can now override the current automatic scoring system.
 
The default progress ranges within Ally.io are calculated as follows:

If (Expected Progress - Aggregate Progress > 25%) , then At Risk

If (Expected Progress - Aggregate Progress > 0% & <=25%) , then Behind

If (Expected Progress - Aggregate Progress <= 0%) , then On Track

However, admins no longer need to stick to these progress ranges and can now customize and define the ranges for the respective progress status that they need to set for tracking the OKR progress. 

## How to manage objective status alerts 

Alerts automatically indicate when an objective needs attention or is at risk. Alerts are enabled for all objectives by default. Each user can manage how alerts are displayed for their account.

:::image type="content" source="../media/goals/3/35/goals-manage-alerts.png" alt-text="Image of Managing Alerts"::: 

To manage alerts, select your Avatar, then select **Account Settings** -> **Manage Alerts** and choose your preference. 

:::image type="content" source="../media/goals/goals-manage-alerts.png" alt-text="screenshot of managing alerts."::: 

### Status indicators

Alerts are displayed in orange or red for each objective. A solid indicator refers to the listed objective, and an outlined indicator refers to a child objective (or even a grandchild objective). 

Select the indicator to see the alert message. 

**Needs Attention**: Shows that an objective (or its child objectives) appear to fall outside of OKR best practices. Indicators include: 

- Not started yet, seven days past the start date.

- Not aligned to any objectives: 
    Objective doesn't have key results and is a team or individual level objective.

- Objective has too many results. Best practice is to have 3-5 key results.

- Score is higher than 0.8. Consider setting the goal higher next time.  

**At Risk**: Shows that an objective (or its child objectives) appear to have a significant issue with configuration or progress. Indicators include: 

- Progress off by more than 25% from expected progress based on start and due date of OKR.

- Objective is past its due date.

- Doesn't have an owner.

- Key Result and Objective time periods don't align.

- Objective dates don't align with period dates.

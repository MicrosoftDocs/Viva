---
ms.date: 06/24/2024
title: Track OKR progress status
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
- highpri
search.appverid:
- MET150
description: "Learn how progress status is calculated in Viva Goals and how to track it."
---

# Track OKR progress status

## How to track OKR progress in Viva Goals

Each OKR in Viva Goals contains a progress bar that displays the last identified progress. Viva Goals assesses progress in 2 ways: Actual and Expected.

:::image type="content" source="../media/goals/okr-progress-bar.png" alt-text="Example showing OKR progress Bar." lightbox="../media/goals/okr-progress-bar.png":::

- **Actual Progress:** Indicated by the progress bar and the percentage of it that has been completed. The percentage is listed directly below the progress bar.

- **Expected Progress:** Indicated by the grey vertical line on the progress bar.

### How actual progress is calculated

Actual Progress is calculated when a user makes a check-in to the OKR, either automatically via a data integration or via the roll-up of Key Results to an objective.

For manual check-ins, a progress % or KPI value must be added explicitly by the user.

When **Show more info** on the dashboard list view is turned on, you can see all of the following below the progress bar:

- How and when the last update was made
- The % complete or KPI
- Any notes left at the time of the check-in
- Who made the update

### How expected progress is calculated

Viva Goals calculates the expected progress % based on the **Start date** and **End date** specified by the owner of the OKR. The progress bar and graph below are found on the objective's quick view (you can open the quick view by selecting the objective's name). You can also select the "full view" of the OKR to view the progress graph.

:::image type="content" source="../media/goals/okr-progress-graph.png" alt-text="OKR progress graph." lightbox="../media/goals/okr-progress-graph.png":::

> Note:
> On the first day of the time period, the expected progress would be 0%.
> On the final day of the time period, the expected progress would be 100%.

### Manually override OKR progress and status

While it is highly recommended to automate OKR progress updates, either through an integrated data source or via rollup from child objectives, the OKR owner might have a better context for progress. In such cases, you can manually override the automated progress and status, setting them as you see fit.

1. When hovering over an OKR in the view, you will see a check-in icon:

    :::image type="content" source="../media/goals/current-progress-mode-icon.png" alt-text="Icon indicating current progress mode." lightbox="../media/goals/current-progress-mode-icon.png":::

1. Upon selecting this icon, you'll see the option to make a check-in. Here, you'll find the current progress and status of the objective based on the automatic update. Select the pencil icon next to them to make a manual check-in.

    :::image type="content" source="../media/goals/current-progress-mode-icon-check-in.png" alt-text="OKR manual progress update." lightbox="../media/goals/current-progress-mode-icon-check-in.png":::

1. Set the progress and status as you see fit.

1. Save your check-in.

When you manually override the progress and status and choose to stop the automatic updates, the next automatic update will not take effect unless you edit the OKR.

## Status

Viva Goals lets you validate and indicate the progress of your OKRs with a status. OKR statuses are color-coded, as shown below:

:::image type="content" source="../media/goals/viva-goals-status-colours.png" alt-text="Different OKR colors in Viva Goals." lightbox="../media/goals/viva-goals-status-colours.png":::

When the status is manually set by a user (such as when a user checks in and marks the status as **On Track**) the progress bar will show the manually set status (in this case, **On Track**).

### Status derived based on progress

Status will be calculated based on the progress updates of the particular objective or key result.

In cases where all the key results of an objective have **Postponed** or **Closed** as their status, the parent objective's status will automatically be marked as **Postponed** or **Closed** respectively, regardless of the Progress %. Here's how status is calculated based on an OKR's progress updates:

- If (Expected Progress - Aggregate Progress > 25%), then **At Risk**

- If (Expected Progress - Aggregate Progress > 0% & <=25%), then **Behind**

- If (Expected Progress - Aggregate Progress <= 0%), then **On Track**

For example, the objective "Successfully launch version 3 of our main product" has four key results and one initiative that contribute to its progress. The objective's status will be derived based on the progress %. In the example, the expected progress of the objective is at 82% and the actual progress is at 56%. Because (Expected Progress - Aggregate Progress > 0% & <=25%), the derived status is **Behind**.

:::image type="content" source="../media/goals/my-okrs-tab-expected-progress.png" alt-text="Example showing Behind status calculation." lightbox="../media/goals/my-okrs-tab-expected-progress.png":::

### OKR progress bar customization

Viva Goals has a progress bar customization setting admins can use to override the automatic scoring system.

By default, the progress ranges within Viva Goals are calculated as follows:

- If (Expected Progress - Aggregate Progress > 25%), then **At Risk**

- If (Expected Progress - Aggregate Progress > 0% & <=25%), then **Behind**

- If (Expected Progress - Aggregate Progress <= 0%), then **On Track**

However, admins no longer need to stick to these progress ranges: instead, they can define their own custom ranges for tracking OKR progress.

### Manage objective status alerts

You can set up alerts to automatically indicate when an objective needs attention or is at risk. To enable OKR alerts, visit **Admin** > **OKRs and Projects** and enable the **OKR Health Indicators** setting.

:::image type="content" source="../media/goals/3/35/okr-health-indicators-enabled.png" alt-text="Screenshot highlighting the OKR Health Indicators setting with the relevant checkbox selected." lightbox="../media/goals/3/35/okr-health-indicators-enabled.png":::

Each user can manage how alerts are displayed for their account. To manage alerts, select your Avatar, then select **Preferences** > **Manage Alerts** and choose your preference.

:::image type="content" source="../media/goals/3/35/goals-manage-alerts.png" alt-text="Image of Managing Alerts" lightbox="../media/goals/3/35/goals-manage-alerts.png":::

### Status indicators

Alerts are displayed in orange or red for each objective. A solid indicator refers to the listed objective, and an outlined indicator refers to a child or grandchild objective.

Select the indicator to see the alert message.

**Needs Attention:** Shows that an objective (or its child objectives) appear to fall outside of OKR best practices. Indicators include:

- As of seven days past the start date, the objective hasn't been started.

- The objective isn't aligned: it doesn't have key results and is a team- or individual-level objective.

- The objective has too many results. The best practice is to have 3 to 5 key results.

- The score is higher than 0.8. Consider setting the goal higher next time.

**At Risk:** Shows that an objective (or its child objectives) appear to have a significant issue with configuration or progress. Indicators include:

- Progress is off by more than 25% from expected progress based on the OKR's start date and due date.

- The objective is past its due date.

- The objective doesn't have an owner.

- The Key Result and Objective time periods don't align.

- The objective dates don't align with period dates.

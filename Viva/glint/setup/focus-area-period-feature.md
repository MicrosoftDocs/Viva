---
title: Focus Area period feature setup
description: Viva Glint admins can manage Focus Area periods directly from the platform. A Focus Area period is the timeframe (or window) from the time the Focus Area is created through when action taking should be completed.. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: focus area periods
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 02/07/2024
---

# Focus Area period feature setup

Viva Glint admins can manage Focus Area periods directly from the platform. A Focus Area period is the timeframe (or window) from when the Focus Area is created through when action taking should be completed.

Managing Focus Area periods allow admins to determine how often to survey based on the needs of their organization. From the Configuration page, users with permissions see a Focus Areas section with an option for managing Focus Area periods. 

:::image type="content" source="../../media/glint/reports/focus-area-periods-access.png" alt-text="Screenshot of how to access Focus Area Periods from the admin dashboard.":::

>[!NOTE]
>Users need *Manage Focus Area Periods* permission to configure them. Set that up within **User Roles** from your Viva Glint dashboard.

## Add a Focus Area Period

1. Select **+ New Period** to open the Create Period slider window.

   :::image type="content" source="../../media/glint/reports/focus-areas-create-period.png" alt-text="Screenshot of the Create Period slider window.":::

2. Select a language. Each language will save as they are selected.
1. Select a cadence: monthly, quarterly, semi-annually, annually, weekly.
1. Name the period.
1. Choose a start date. 
1. Choose an end date. The end date is the date that all actions are expected to be completed by. Managers see this expected date on their action plan.
1. Enable the Focus Area period.
1. Select **Save Changes.**

## Focus Area Periods have a built-in 90-day logic

When a manager creates a Focus Area period, the system checks to find if another Focus Area period with at least 90 days left from this Focus Area due date exists. If one does exist, the system creates a new Focus Area period to allow users enough time to complete all actions.

> [!TIP]
> When configuring this window, realize that action plan strategies are built around a 90-day completion plan. Create the time period to allow 90 days from the day the manager establishes their action its due date.

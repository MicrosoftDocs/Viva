---
title: "Weighted Objectives"
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

description: "Learn how with Viva Goals Weighted Objectives feature, you can fine tune your scoring."
---

# Weighted Objectives

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## What are Weighted Objectives?

Viva Goals' Weighted Objectives feature allows objective owners and creators to assign specific weights to define how scoring and progress roll up to parent Objectives.

If your organization has Weighted Objectives enabled you may see objective weights displayed like this:

:::image type="content" source="../media/goals/viva-goals-weighted-objectives-1.png" alt-text="Weighted Objectives 1":::

- In this example, the Key Result *Encourage Engagement through Polls* has a weight of 2x. This means it will account for twice the progress of it sibling Key Results. Since there are four Key Results, it will account for 50% of the parent Objective progress instead of the normal 25%

- The Project *Perform a KB. Audit* shows that its progress doesn't contribute to the progress of its parent. This amounts to a weight of 0x.

> [!NOTE]
>
> 1. If your organization has **% OKR Weights and Contribution** enabled, then head over to this [article](https://help.ally.io/en/articles/5362460-manage-okr-contribution).  
>
> 2. **Weights for key performance indicator (KPI) numeric Objectives and Key Results (OKRs):** For KPI numeric-based parent OKRs that have progress roll-ups from KPI numeric-based child OKRs, these weights (0.5x, 1x, 2x, 4x) will not be available.

## How to add weights?

To set or edit weights from the action dropdown, select **Weight** and then select your appropriate weight.

:::image type="content" source="../media/goals/viva-goals-weighted-objectives-2.png" alt-text="Weighted Objectives 2":::

:::image type="content" source="../media/goals/viva-goals-weighted-objectives-3.png" alt-text="Weighted Objectives 3":::

:::image type="content" source="../media/goals/weighted-kr-contribution.gif" alt-text="Weighted Objectives 4":::

You also can access weighting from the edit page.

:::image type="content" source="../media/goals/add-weights-edit.gif" alt-text="Weighted Objectives 5":::

All subscriptions have the ability to set key result progress to not contribute to its parent.

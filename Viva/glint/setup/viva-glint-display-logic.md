---
title: Assign the right survey items to users with Viva Glint Display Logic
description: Viva Glint Display Logic makes it easy to assign relevant survey items to the right survey taker.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: Conditional logic, branch logic, skip logic, display logic
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 10/17/2023
---

# Assign the right survey items to users with Viva Glint Display Logic

Microsoft Viva Glint admins can set up survey items with conditions that personalize surveys for users by applying display rules. Display logic rules allow you to show or hide survey items depending on the survey taker’s previous responses. For example, if a person answers “No” to item 4 on your survey, and the following items 5-7 no longer apply to them, these items can be automatically hidden, and the survey taker moves to item 8.

> [!NOTE]
> This feature will be available in Viva Glint after **October 28th, 2023**.

## Scenarios for Display Logic

Display Logic can be applied based on:

- Answers to previous multiple-choice/multi-select questions
- Answers to previous rating questions
- Whether a user skipped an optional question

> [!IMPORTANT]
> A question will always display unless it has display logic defined, in which case it displays only when display logic rules are met.

## Set up Display Logic in your survey program

From the admin dashboard, go to the survey you want to edit. Display logic can be set up in the **Questions** section in **Program Summary**.

1. Arrange your survey items in the order you want them before adding Display Logic.

   > [!CAUTION]
   > Display Logic only works correctly when all survey items are added to your program in the exact order that should appear for survey takers.

1. Select the **vertical ellipses** next to a survey item to display the dropdown menu.
1. Select **Edit Display Logic** to open the Display Logic slider window.

   :::image type="content" source="../../media/glint/setup/glint-dropdown-display-logic-2.png" alt-text="Screenshot of question setup display logic dropdown menu item.":::

1. Choose the **overall logic for conditions**, using the dropdown menu.
1. Next, choose the **condition** and **subcondition** using the corresponding dropdown menus.
   1. The subcondition opens the Question box where you can choose the survey item that the display logic is dependent upon.
   1. **Select an operator** – the instance that is to be acted upon.
   2. Add additional subconditions as desired.
1. Add additional conditions as needed.
2. Select **Save Changes**.

   :::image type="content" source="../../media/glint/setup/glint-display-logic-pane-2.png" alt-text="Screenshot of display logic setup pane.":::

   > [!IMPORTANT]
   > The first item in your survey can’t have display logic, which is based on responses to previous survey items.

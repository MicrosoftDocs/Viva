---
title: Tailor users' survey experience with Viva Glint Display Logic
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
ms.localizationpriority: high
ms.date: 01/18/2024
---

# Tailor users' survey experience with Viva Glint Display Logic

Microsoft Viva Glint admins can set up survey items with conditions that personalize surveys for users by applying display rules. Display logic rules allow you to show or hide survey items depending on the survey taker’s responses to previous questions in a survey.

## Display Logic options

Display Logic can be applied based on:

- Answers to previous multiple-choice/multi-select questions
- Answers to previous rating questions
- Whether a user skipped an optional question

> [!IMPORTANT]
> A question will always display unless it has display logic defined, in which case it displays only when display logic rules are met.

## Set up Display Logic in your survey program

From the admin dashboard, go to the survey you want to edit. Display logic can be set up in the **Questions** section in **Program Summary**.

Learn more about how to set up Display Logic with this video and the guidance in this article:
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1jZyp]

1. Arrange your survey items in the order you want them before adding Display Logic.

   > [!CAUTION]
   > Display Logic only works correctly when all survey items are added to your program in the exact order that should appear for survey takers.

1. Select the **horizontal ellipses** next to a survey item to display the dropdown menu.
1. Select **Edit Display Logic** to open the Display Logic slider window.

   :::image type="content" source="../../media/glint/setup/glint-dropdown-display-logic-2.png" alt-text="Screenshot of question setup display logic dropdown menu item.":::

1. Choose the **overall logic for conditions**, using the dropdown menu.
   1. Use **All of the following conditions are met (AND)** when you have multiple conditions that all need to be met to display or hide an item.
   2.  Use **Any of the following conditions are met (OR)** when you have multiple conditions but only one needs to be met to display or hide an item.
1. Next, choose the **Display if** setting for Condition 1. Within each condition:
   1. Use **All of the following conditions are met (AND)** when you have multiple conditions that all need to be met to display or hide an item.
   2.  Use **Any of the following conditions are met (OR)** when you have multiple conditions but only one needs to be met to display or hide an item.
1. Select an item from the **Question** dropdown menu. All items that come before the item with display logic rules are available in this menu.
2. Select an operator in the **Operator** dropdown menu to determine how response values to previous questions should be evaluated. For example, "is equal to" or "is smaller than."
3. Select a response value from the **Answer** dropdown.
4. Add additional conditions as needed by selecting **+ Add new condition**.
5. Select **Save Changes** in the slider window.
6. Select **Save Changes** in the top right of the Questions section in your survey program.
7. [Preview your survey](https://go.microsoft.com/fwlink/?linkid=2230749) to see how different responses hide or display the item with Display Logic.

   :::image type="content" source="../../media/glint/setup/glint-display-logic-pane-2.png" alt-text="Screenshot of display logic setup pane.":::

   > [!IMPORTANT]
   > The first item in your survey can’t have display logic, which is based on responses to previous survey items.

## Scenario

Contoso includes the following questions in their employee survey, but only want survey takers to see Job Feedback if they select Agree or Strongly Agree for the Coaching item:

- **Coaching**: I have ongoing conversations with my manager about my performance.
- **Job Feedback**: My manager provides me with feedback about my performance to help me do my job better.

To hide Job Feedback from users who disagree with or select a neutral response for the Coaching item, create a condition that only displays Job Feedback when the response value to Coaching is bigger than 3 (responses 1, 2, and 3 are equal to Strongly Disagree, Disagree, and Neither).

:::image type="content" source="../../media/glint/setup/display-logic-example-setup.png" alt-text="Screenshot of display logic setup pane for Coaching and Job Feedback.":::

After adding Display Logic to Job Feedback, a symbol will appear on the item in your survey program:

:::image type="content" source="../../media/glint/setup/display-logic-example-items.png" alt-text="Screenshot of display logic symbol on Job Feedback.":::




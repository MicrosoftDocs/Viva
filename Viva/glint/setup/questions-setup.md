---
title: Questions setup in Program Summary of Viva Glint
description: On the Questions page admins, add or modify items prepopulated into survey templates.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: edit questions, survey items, question targeting, item targeting
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/09/2024
---

# Questions setup in Program Summary

The Questions page allows you to add or modify the items included in a survey. Refer to the [Learn about Viva Glint program design](/training/modules/viva-glint-learn-about-viva-glint-program-design) module to learn how to implement your organization's listening strategy in your survey program question setup.

:::image type="content" source="../../media/glint/setup/program-summary-questions.png" alt-text="Screenshot of where to access Questions setup from Program Summary." lightbox="../../media/glint/setup/program-summary-questions.png":::

> [!IMPORTANT]
> The term **item** refers to any *question or statement* posed to a survey taker.

## Use Viva Glint's prepopulated survey templates

Standard templates provide prepopulated questions and survey items, along with introductory and "thank you" text that admins can customize. The Viva Glint People Science Team researches and substantiates prepopulated survey items.

:::image type="content" source="../../media/glint/setup/program-summary-questions-text.png" alt-text="Screenshot of where to customize introductory and thank you text for survey takers." lightbox="../../media/glint/setup/program-summary-questions-text.png":::

## Edit the survey introduction message

Customize the introduction message for the survey by hovering over the box with the "Hello" message and select it. 

In the window that opens:
- Select languages from the **Language** dropdown menu. Languages selected in General Settings are available here.
- Edit **Greeting** - "Hello" is prepopulated, but can be customized for your organization.
- Edit **Text** - You see default text in the **Text** box.
  - All default text can be edited.
  - The Text field also includes placeholders, called macros, that pull in values based on your employee data or Glint-generated items. Delete macros or add new macros by selecting the blue plus sign (+) in the Text box.

When finished, select **Save Changes**.

## Add a logo to the survey introduction

To add your organization's logo to the survey introduction:

> [!TIP]
> Ensure that logos are horizontally oriented, have a transparent background, and 16MB or smaller in file size.

1. Go to **Configuration** and in the **Action Taking** section, select **Content Resources**.
1. Select **+ New** to add a new resource and select **OK** in the languages message that appears.
1. Add a new title in the **Untitled Resource** and **Title** fields.

   Survey intro logos can be unique to each survey program. Include the survey name in the title if needed.

1. In the **Type** field, select **Image**.
1. Optionally, add a **Description**.
1. In the File field, select **Choose File** and browse to choose the image file on your device.
1. When selected, a preview of the image appears. If the image appears as expected, select **Save**.
1. Select **Publish** in the top right of the screen and then select **Publish** again in the **Publish Resource** dialog that appears.
1. On the **Resources** page, filter to Image in the left menu and copy the text of the recently added image name from the **Name** column.
1. Replace "logo-name" in this text with the exact name of your uploaded logo: `![logo-name](logo-name "logo-name")`
1. Copy and paste the `![logo-name](logo-name "logo-name")` text (with your logo name added) and paste into the end of the Text field in the survey introduction message and **Save Changes**.
1. [Preview your survey](/viva/glint/setup/preview-manage-enable-engage-programs) to confirm that the logo appears as expected.

## Edit survey items

This important topic has its own guidance page! [Read about survey item editing](/viva/glint/setup/question-edit).
> [!NOTE]
> Survey items can be edited during the initial survey configuration *and* sometimes during a live survey, as needed.

## Survey item targeting

Add a target to a specific item to ensure that only the population targeted sees it in the survey. Using the search box, select one or more **User Role** to include or exclude. 
When finished, select **Save Changes**.

## Delete survey items

Remove an item from the program by selecting **Yes, delete it** in the box that displays. If you don't want to delete, select **No, I changed my mind.**

## Edit the "Thank You!" message people see when submitting their survey

Customize the 'Thank You!' message for the survey by hovering over the box and selecting it. In the window that opens you can:

- Select languages from the **Language** dropdown menu. Languages already permissioned for your organization in General Settings are available here.
- Edit **Greeting** - "Thank you!" is prepopulated, but customize the greeting in a way that's comfortable for you. 
- Edit **Text** - You see dummy text in the **Text** box.
  - All dummy text can be edited.
  - The Text field also includes placeholders, called macros, that pull in values based on your employee data or Glint-generated items. Delete macros or add new macros by selecting the blue plus sign (+) in the Text box.

When finished, select **Save Changes**.

## Edit Question cycles

You don't have to use all of the items programmed for a survey during each survey cycle. Choose survey items per program cycle by selecting the corresponding cycle number next to the item. For example, if you only want a certain item asked on the first survey, deselect all numbers except for the number 1.

## Add new items and section breaks to a program

To add rating questions, multiple choice questions, open-ended questions, or section breaks (to give your people time to take a natural pause), follow this guidance: [Adding items to a prepopulated survey](/../../viva/glint/setup/add-new-questions).

## Edit Display Logic

>[!TIP]
> Wait to add display logic until after you've arranged your sections and items in the order you want.

In the Display Logic window, set the following fields:
- The **Overall logic for conditions** and subsequent **Conditions** or **Subconditions**. Select **+ Add new condition** to add more.

**[Use this guidance to manage display logic](/../../viva/glint/setup/viva-glint-display-logic)**


## Next Step
> [!div class="nextstepaction"]
> [Reporting setup in Program Summary](/../../viva/glint/setup/reporting-setup).




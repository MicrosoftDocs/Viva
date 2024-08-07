---
title: Questions setup in Program Summary of Viva Glint
description: On the Questions page admins, add or modify items prepopulated into survey templates.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: edit questions, survey items, question targeting
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 08/07/2024
---

# Questions setup in Program Summary

The Questions page allows you to add or modify the items included in a survey. Refer to the [Learn about Viva Glint program design](/training/modules/viva-glint-learn-about-viva-glint-program-design) module to learn how to implement your organization's listening strategy in your survey program question setup.

:::image type="content" source="../../media/glint/setup/program-summary-questions.png" alt-text="Screenshot of where to access Questions setup from Program Summary.":::

> [!IMPORTANT]
> The term "survey item" refers to any question or statement posed to a survey taker.

## Use Viva Glint's prepopulated survey templates

Standard templates provide prepopulated questions and survey items, along with introductory and "thank you" text that admins can customize. The Viva Glint People Science Team researches and substantiates prepopulated survey items.

:::image type="content" source="../../media/glint/setup/program-summary-questions-text.png" alt-text="Screenshot of where to customize introductory and thank you text for survey takers.":::

## Edit the survey introduction message

Customize the introduction message for the survey by hovering over the box with the "Hello" message and select it. 

In the window that opens:
- Select languages from the **Language** dropdown menu. Languages selected in General Settings are available here.
- Edit **Greeting** - "Hello" is prepopulated, but can be customized for your organization.
- Edit **Text** - You see default text in the **Text** box.
  - All default text can be edited.
  - The Text field also includes placeholders, called macros, that pull in values based on your employee data or Glint-generated items. Delete macros or add new macros by selecting the blue plus sign (+) in the Text box.

When finished, select **Save Changes**.

### Add a logo to the survey introduction

To add your organization's logo to the survey introduction:

> [!TIP]
> Ensure that logos are horizontally oriented, have a transparent background, and 16MB or smaller in file size.

1. Go to **Configuration** and in the **Action Taking **section, select **Content Resources**.
1. Select **+ New** to add a new resource and select **OK** in the languages message that appears.
1. Add a new title in the **Untitled Resource** and **Title** fields.
   1. Survey intro logos can be unique to each survey program. Include the survey name in the title if needed.
1. In the **Type** field, select **Image**.
2. Optionally, add a **Description**.
3. In the File field, select **Choose File** and browse to choose the image file on your device.
4. When selected, a preview of the image appears. If the image appears as expected, select **Save**.
5. Select **Publish** in the top right of the screen and then select **Publish** again in the **Publish Resource** dialog that appears.
6. On the **Resources** page, filter to Image in the left menu and copy the text of the recently added image name from the **Name** column.
7. Replace "logo-name" in this text with the exact name of your uploaded logo: `![logo-name](logo-name "logo-name")`
8. Copy and paste the `![logo-name](logo-name "logo-name")` text (with your logo name added) and paste into the end of the Text field in the survey introduction message and **Save Changes**.
9. [Preview your survey](/viva/glint/setup/preview-manage-enable-engage-programs) to confirm that the logo appears as expected.

## Edit survey items using the horizontal ellipses

:::image type="content" source="../../media/glint/setup/program-summary-questions-ellipses.png" alt-text="Screenshot of ellipses dropdown menu next to each survey item.":::

Hover over the horizontal ellipses next to any survey item to select one of the following options:

### Edit Targeting

Adding a target to a specific question ensures that only the population targeted sees it within the survey. Using the search boxes, select one or more **User Role** to include or exclude. When finished, select **Save Changes**.

### Edit Question
The Edit Question slider window provides two tabs for setup:
- Question Configuration
- Associated Programs

#### Question Configuration

You may edit the following fields:
- Select a **Language** from languages prepopulated in the dropdown menu
- See the **Question Type** - rating, multiple choice, open-ended
- Assign a **Reporting Label** for easy identification of your item
- Consider if the **Question Text** is as it should be - The wording for this item appears verbatim. The **+ button** allows you to edit the question. 
  
   >[!IMPORTANT]
   > Try not to edit our standard survey items! Item edits may impact language translations and the item's intention, which can subsequentlly affect the accuracy of the benchmark tied to the question.

- Consider providing **Instruction Text** - Use this space to provide survey takers with helpful information about how to answer this item
- Consider providing **Comment Placeholder Text** - "Leave your comments here" appears by default, but this text can be customized
- View the **Rating Scale** for the item - 5 or 7 points
- Decide whether to include the rating **Label for all options** - The **Low Value** (1-strongly disagree) and **High Value** (5- strongly agree) appear by default. To define values 2, 3, and 4, toggle to YES and then assign their meaning. For example: 2 = disagree
- Decide whether to **Allow Comments** - Toggle to Yes or No
- Decide whether this item can be an **Optional Question** - Toggle to Yes or No
- Choose a **Suggested Action Template** - Use the dropdown menu to attach this survey item to a previously configured Suggested Action Template to help your managers act on feedback

Select **Save Changes** when editing is complete.

#### Associated Programs

A list of program names previously used or in use that include this survey item can be viewed here.

### Edit Display Logic

>[!TIP]
> Wait to add display logic until after you've arranged your sections and items in the order you want.

In the Display Logic window that opens, set the following fields:
- The **Overall logic for conditions** and subsequent **Conditions** or **Subconditions**. Select **+ Add new condition** to add more.

**[Use this guidance to manage display logic](/../../viva/glint/setup/viva-glint-display-logic)**

### Delete survey items

Remove the question (item) from the program by selecting **Yes, delete it** in the box that displays. If you don't want to delete, select **No, I changed my mind.**

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

To add rating questions, multiple choice questions, open-ended questions, or section breaks (to give your people time to take a natural pause), follow the guidance for **Adding items to a prepopulated survey.**

## Next Step
> [!div class="nextstepaction"]
> [Reporting setup in Program Summary](https://go.microsoft.com/fwlink/?linkid=2230977).




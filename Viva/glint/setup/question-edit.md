---
title: Edit survey items in a Viva Glint survey
description: On the Questions page admins, add or modify items prepopulated into survey templates.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: edit questions, survey items, question targeting, edit items
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/09/2024
---

#  Edit survey items in a Viva Glint survey

:::image type="content" source="../../media/glint/setup/program-summary-questions-ellipses.png" alt-text="Screenshot of ellipses dropdown menu next to each survey item." lightbox="../../media/glint/setup/program-summary-questions-ellipses.png":::

Hover over the horizontal ellipses next to any survey item to select one of the following options: Edit Targeting, Edit Question, Edit Display Logic, or Delete survey items.

The Edit Question slider window provides these tabs for setup:
- Question Configuration
- Associated Programs

## Survey item Configuration

You can edit the following fields:
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

## Edit items in a live survey

In many instances, admins can make changes to a live survey, but only make them when necessary.
Preview your changes before launching and follow these practices:
<br>
 - **Don't stop the survey.** Unless you need to completely replace a survey cycle, never stop a survey. Many edits can be made while the survey is enabled.
 - **Make email and reminder edits only at the cycle level.** Changes at the program level don't apply to a live survey.
 - **Always leave the meaning of a question intact.** You may need to fix spelling, grammatical or translation errors.
   - The adjusted question's/item's meaning should remain the same before and after edits.
   - To ensure the integrity of the survey results, don't adjust any rating scale or multiple-choice options.
- Always **Save** and **(re)Approve**. When making live edits, save changes and reapprove the survey before ending your session. [Use this guidance for approving, previewing, enabling, and disabling your survey](/viva/glint/setup/preview-manage-enable-engage-programs).
- Be consistent across languages. Make text changes uniformly, across all languages included in the survey.
  
## Edit considerations 
For item edits during draft, scheduled, or live status, always consider:

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| The text at the beginning (top) and end (bottom) of the survey | The *Intro* or *Thank You* text needs adjustments or corrections. | Newly edited text will be featured immediately and *only* on surveys that haven't started. |
| Question text | The phrasing of a question needs to be edited. | [Use this guide](https://go.microsoft.com/fwlink/?linkid=2230918). Glint pushes your edits into production (that is, live survey and reporting).<br><p>**Note:** Republishing can cause a disruption to employees taking the survey at the moment this change is implemented. They can start over by refreshing their page.|
| Adding or removing a question/item | You want to add a new question/item or remove a question/item from a live survey. | A question/item *can't* be added or removed from a live survey except in an *Always-On*, Onboarding, or Exit pulse program. |
| Question/item order | The questions need to be reordered. | The newly edited question/item order is featured immediately and *only* on surveys that haven't yet been started. |

## Process to edit a live survey item

There are three entry points to do this from:
-	From the Question Library on your admin dashboard (doesn't require survey to go into unapproved state)
-	From the *Survey Programs, Live* section
-	From the *Survey Programs, Upcoming* section

**Allow Survey Resubmission** in the *Program Setup* section of *Program Summary* must be toggled to **Yes.** <br>
If not toggled to **Yes**, a pop-up informs you that the change to **Yes** is made automatically when your edits are saved.

## Inform survey takers of a live edit

>[!IMPORTANT]
>All survey participants must be made aware of the opportunity to retake a survey if a question is changed while the survey is live. They must further understand that if they retake a survey, their original answers are replaced.

**Enabling Survey Resubmission ensures that Entra ID and survey takers invited to take the survey through a personalized email, receive platform-generated email notification of a change in the survey.** This notification is required to meet Microsoft privacy policies and allows the survey taker to retake the survey if they choose to.

**If your organization uses attribute-based access, you are responsible to notify participants about any change and provide instructions on how to do so.** Survey retake access:
-	Survey takers can use the link from their original survey invitation email 
-	Use this guidance to resend survey invites

For participants who haven't started the survey, the survey is automatically updated with the new version of all questions and no notification is generated or required.

## Associated Programs

A list of program names previously used or in use that include this survey item can be viewed here. You may see an alert cautioning you that this question is being used in one or more live surveys. 

- If you don't want to make this change, choose **Cancel.**
- You can edit language text, instruction text, and comment placeholder text only. Other fields are disabled and can't be edited until the survey is no longer live.
- Make your changes and select **Save.**

:::image type="content" source="../../media/glint/setup/change-live-q-tooltips.png" alt-text="Screenshot of warning and tips about editing a question during a live survey." lightbox="../../media/glint/setup/change-live-q-tooltips.png":::

## Confirm edits 
Review your edits to make sure your employees receive appropriate notice. 
 
1. Review the **Confirm your changes** window that opens.

:::image type="content" source="../../media/glint/setup/live-confirm-changes.png" lightbox="../../media/glint/setup/live-confirm-changes.png" alt-text="Screenshot of the confirmation box for editing live survey questions.":::

>[!IMPORTANT]

> - If your organization uses Entra ID or personalized links for survey access, participants who have started or already completed the survey will be notified in email.

> -  If your organization uses attribute-based survey access, notify participants about these changes and ask them to retake the survey, if needed. 

2. If everything is as expected, select **Confirm.**

3. A one-time notification confirms that your question is updated.





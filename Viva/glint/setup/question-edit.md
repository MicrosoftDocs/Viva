---
title: Edit items in a live Viva Glint survey
description: In some instances, admins can make changes to live surveys. It's critical to follow established guidelines.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: survey items, edit items
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/19/2024
---

#  Edit items in a live Viva Glint survey

> [!IMPORTANT]
> Viva Glint uses the term "item" to refer to questions and statements in a Glint program. 

In some instances, admins can make changes to questions and statements in a live survey. Make them only when necessary.
<br></br>
Preview your changes before launching and follow these practices:
<br>
 - **Don't stop the survey.** Unless you need to completely replace a survey cycle, never stop a survey. Many edits can be made while the survey is enabled.
 - **Make email and reminder edits only at the cycle level.** Changes at the program level don't apply to a live survey.
 - **Always leave the meaning of a question intact.** You may need to fix spelling, grammatical or translation errors.
   - The adjusted question's/item's meaning should remain the same before and after edits.
   - To ensure the integrity of the survey results, don't adjust any rating scale or multiple-choice options.
- Always **Save** and **(re)Approve**. When making live edits, save changes and reapprove the survey before ending your session. [Use this guidance for approving, previewing, enabling, and disabling your survey](/viva/glint/setup/preview-manage-enable-engage-programs).
- **Make text changes uniformly, across all languages included in the survey.**

## Scenarios and considerations for live item edits

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| Question text | The phrasing of a question needs to be edited. | Glint pushes your edits into production (that is, live survey and reporting).<br><p>**Note:** Republishing can cause a disruption to employees taking the survey at the moment this change is implemented. They can start over by refreshing their page.|
| Adding or removing a question/item | You want to add a new question/item or remove a question/item from a live survey. | A question/item *can't* be added or removed from a live survey except in an *Always-On*, Onboarding, or Exit pulse program. |
| Question/item order | The questions need to be reordered. | The newly edited question/item order is featured immediately and *only* on surveys that haven't yet been started. |

## Item edit access

There are two access points:
-	From the **Question Library** on your admin dashboard (doesn't require survey to go into unapproved state)
-	From **Survey Programs, Live** 

**Allow Survey Resubmission** in the **Program Setup** section of **Program Summary** must be toggled to **Yes.** <br>
If not toggled to **Yes**, a pop-up informs you that the change to **Yes** happens automatically when edits are saved.

Hover over the **horizontal ellipses** next to any survey item to select **Edit Question**.

The Edit Question slider window includes these setup tabs:
- Question Configuration
- Associated Programs

:::image type="content" source="../../media/glint/setup/program-summary-questions-ellipses.png" alt-text="Screenshot of ellipses dropdown menu next to each survey item." lightbox="../../media/glint/setup/program-summary-questions-ellipses.png":::

:::image type="content" source="../../media/glint/setup/before-question-edit.png" alt-text="Screenshot of alert box for live item editing." lightbox="../../media/glint/setup/before-question-edit.png":::

## Inform survey takers of a live edit

>[!IMPORTANT]
>All survey participants must be made aware of the opportunity to retake a survey if a question is changed while the survey is live. They must further understand that if they retake a survey, their original answers are replaced.

**Enabling Survey Resubmission ensures that Entra ID and survey takers invited to take the survey through a personalized email, receive platform-generated email notification of a change in the survey.** This notification is required to meet Microsoft privacy policies and allows the survey taker to retake the survey if they choose to.

**If your organization uses attribute-based access, you are responsible to notify participants about any change and provide instructions on how to do so.** Survey retake access:
-	Survey takers can use the link from their original survey invitation email 
-	Use this guidance to resend survey invites

For participants who haven't started the survey, the survey is automatically updated with the new version of all questions and no notification is generated or required.

:::image type="content" source="../../media/glint/setup/live-edit-email.png" alt-text="Screenshot of the email a survey taker receives to inform of a live survey edit."::: 

## Associated programs

A list of program names previously used or in use that include this survey item can be viewed here. You may see an alert cautioning you that this question is being used in one or more live surveys. 

- If you don't want to make this change, choose **Cancel.**
- You can edit language text, instruction text, and comment placeholder text only. Other fields are disabled and can't be edited until the survey is no longer live.
- Make your changes and select **Save.**

:::image type="content" source="../../media/glint/setup/change-live-q-tooltips.png" alt-text="Screenshot of warning and tips about editing a question during a live survey." lightbox="../../media/glint/setup/change-live-q-tooltips.png":::

## Confirm edits 
Review your edits to make sure your employees receive appropriate notice. 
 
1. Review the **Confirm your changes** window that opens.

   >[!IMPORTANT]
   >
   > - If your organization uses Entra ID or personalized links for survey access, participants who have started or already completed the survey will be notified in email.
   > - If your organization uses attribute-based survey access, notify participants about these changes and ask them to retake the survey, if needed. 

2. If everything is as expected, select **Confirm.**

3. A one-time notification confirms that your question is updated.





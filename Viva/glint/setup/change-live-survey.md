---
title: Make changes to a live Viva Glint survey
description: Viva Glint suggests changing a live survey only when necessary.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Edit live survey, edit program summary
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/00/2024
---

# Make changes to a live Viva Glint survey

While some elements of a live survey can be adjusted, only make live edits when necessary.

Preview your survey before launching. Follow these practices:

 - **Don't stop the survey**. Unless you need to completely replace a survey cycle, never *stop* a survey. Many edits can be made while the survey is enabled.
 - **Make email and reminder edits only at the cycle level.** Program level changes don't apply to a live survey.
 - **Leave the meaning of a question intact.** If you need to fix spelling, grammatical or translation errors:
   - The adjusted question's/item's meaning should remain the same before and after edits.
   - To ensure the integrity of the survey results, don't adjust any rating scale or multiple-choice options.
 - **Always Save and re-approve.** When making live edits, save changes and *reapprove* the survey before ending your session. [Use this guidance for approving, previewing, enabling, and disabling your survey](https://go.microsoft.com/fwlink/?linkid=2230749).
 - **Be consistent across languages.** Make text changes uniformly, across all languages included in the survey.

Use the following information to edit a live survey. The information is broken out across ***Program Summary*** setup pages.

## Program Setup

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| Various | You want to edit the *Program Name* or *Allow Survey Resubmission* items*.* | Edits are only visible to users who haven't started their survey. |
| Additional languages | You want to add a new language as a survey option. | If custom translation text isn't provided, Glint's standard text translations are featured. |

## Distribution

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| Adding users | Employees not yet included in your Employee Attribute *File* need to participate in the survey. | From the admin dashboard, select the **People** section and select **Send Survey**. Each new user is sent the email invitation immediately. From then on, new users receive reminders according to the same schedule as all other users. |
| Editing a Distribution List | The list of which employees are included/excluded in the survey needs adjustment. | A Distribution List can be adjusted at any time, but doesn't automatically send a survey invitation to new users. Those invites have to be sent manually. |

## Schedule

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| Survey launch date | You need to postpone the launch date of the survey. | To avoid potential challenges, make this update a minimum of 24 hours before the survey was scheduled to go live. |
| Response window | You want to decrease/increase the number of days within the survey window. | Adjust a minimum of 48 hours before the original survey end date.<br>Also, make sure your *Communications* emails align with any updated survey window planning.<br><p>**Note** : Live *Schedule* edits are applied at the cycle level. |

## Questions

[Read extended guidance on live survey item edits here.](/viva/glint/question-edit)

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| The text at the beginning (top) and end (bottom) of the survey | The *Intro* or *Thank You* text needs adjustments or corrections. | Newly edited text will be featured immediately and *only* on surveys that haven't started. |
| Question text | The phrasing of a question needs to be edited. |Survey item rephrasing propagates to future programs only. A live program is not affected by any edit.|
| Adding or removing a question/item | You want to add a new question/item or remove a question/item from a live survey. | A question/item *can't* be added or removed from a live survey except in an *Always-On*, Onboarding, or Exit pulse program. |
| Question/item order | The questions need to be reordered. | The newly edited question/item order is featured immediately and *only* on surveys that haven't yet been started. |

## Reporting

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| All items in the *Reporting* section | Any section in the *Reporting* section needs adjustment. | Save all changes, then return to the **Program Summary** and adjust the Approve toggle to **Yes**. |
| Benchmark update | Your external comparison benchmark was updated. | If changes are made to the benchmark in a live program, be certain any user with live access is aware so they aren't confused by results that don't mirror what they saw during their last viewing. |
| Aggregate Indices | You need to edit or add an aggregate index. | If changes are made to indices in a live program, be certain any user with live access is aware so they aren't confused by results that are different their last viewing. |
| Driver Impact Outcomes | You need to edit or add Driver Impact Outcomes. | If changes are made to Driver Impact Outcomes, be certain any user with live access is aware so they aren't confused by different outcome options available in the Driver Impact report. |

## Communications

Live *Communications* edits will only apply when made at the cycle level.

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| Reminders | You need to add or delete email reminders, or otherwise edit existing text. | Future reminders can be added, edited, or deleted if adjusted at least the day before they're scheduled to be sent. Reminders can't be added, edited, or deleted, on the day that they're scheduled to be sent. |
| Results Notification | You want to turn this feature on/off, edit existing text or adjust the number of days until the message is sent. | To avoid potential challenges, make changes at least 48 hours before the closing of the survey window. |

## Live changes in other survey settings

| **Topic** | **Scenario** | **Considerations** |
| --- | --- | --- |
| Driver labels | The reporting label for a question/item needs adjustment. | Proceed as needed. |
| Manager hierarchies | Your reporting is displaying incorrect leadership hierarchies or due to errors in your Employee Attribute File. | Change only after the close of the survey window. |
| Adding survey participants | You've discovered that an extra group of employees needs to be added to the platform. | Submit a delta file of the employees to be added. Then, manually send them the survey invite from within the **People** configuration page > Send Survey. |
| Adding users not in the Distribution List | You've discovered that employees outside of the Distribution List need to be included. | Navigate to the admin Configuration dashboard, then **People** , then **Employee** , then **Action** , then **Send Survey**. |
| Email timing | You want to adjust the time in which emails are sent. | Adjust timing at the cycle level only and consider the user time zones. |



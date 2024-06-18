---
title: Viva Glint Post-Survey Conversation Usage report
description: As an admin, use the Microsoft Viva Glint Post-Survey Conversation Usage report to track how many leaders have completed their Team Conversations and created Focus Areas to improve their team's employee experience.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: team conversations, conversation usage report, focus areas, action items, admin report
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 06/18/2024
---

# Viva Glint Post-Survey Conversation Usage report

As an admin, use the Microsoft Viva Glint Post-Survey Conversation Usage report to track how many leaders have completed their Team Conversations and created Focus Areas to improve their team's employee experience. To learn more about setting up Team Conversations for your organization, see: [Admin setup for Viva Glint Team Conversations](/viva/glint/reports/team-conversations-administrator-setup).

The Post-Survey Conversation Usage report is available:  

- After a survey cycle is closed.
- When Team Conversations are enabled for the survey program and for desired User Roles.
- When Team Conversations are generated: Seven days after User Roles are granted live access to results.
   - Team Conversations are available immediately after survey close for User Roles that have live access while a survey is live.

## How to access the report

To access the Post-Survey Conversation Usage report:

1. From the admin dashboard, select **Configuration** and then choose **Survey Programs**.
1. Select the survey that you want to view a usage report for.
1. Select the **Completed** tab and select the closed survey cycle that you want to see usage information for.
1. The Post-Survey Conversation Usage report appears at the bottom of the survey cycle page. 

:::image type="content" source="../../media/glint/reports/convo-usage-some-complete.png" alt-text="Screenshot of the post-survey conversation usage report for an engagement survey cycle.":::

## Report metrics

Use this guidance to understand different items in the Post-Survey Conversation Usage report and how they're calculated.

|Section  |Item   |Description|
|:----------|:-----------|:------------|
|**Conversation Completion**     |Conversation Completion %      |Percentage of conversations completed. Completed conversations divided by the total conversations.       |
|**Conversation Statuses** |Conversations not viewed  | Percentage of conversations that leaders haven't viewed yet. Conversations not viewed divided by total conversations.        |
| |Bar chart: Open  |Percentage of conversations that are still open. Open conversations divided by total conversations.        |
|  |Bar chart: Skipped  |Percentage of conversations that are skipped. Conversations unopened after the conversation window divided by total conversations.        |
|  |Bar chart: Complete   |Percentage of conversations that are complete. Completed conversations divided by total conversations.        |
| **Conversation Actions** |Average per manager  | Average Focus Areas per manager. Unique Focus Areas divided by total conversations, rounded to the nearest whole number (usually 0).       |
| |Added Focus Areas  |Conversations with a Focus Area divided by total conversations.        |
|  |Added action items   |Total action items divided by total conversations.        |
|  |Committed to Focus Areas  |Focus Areas not in draft status divided by total conversations.        |
|  |Shared conversations   |Conversations that are shared via email divided by total conversations. Displays even when sharing isn't enabled.        |

Hover over each of the bars in the Conversation Statuses bar chart to view conversation counts used to calculate percentages for each status.

## Download to .csv

Use the **Download Full CSV** option in the Post-Survey Conversation Usage report to download a detailed report to your device that includes:

- Program Name
- Cycle Name
- Conversation Status
- Conversation Shared?
- Number of Unique People Conversation Shared With
- Number of Focus Area(s) Selected
- Number of Action Item(s) Added
- Number of Focus Area(s) Committed To
- Conversation Due Date
- Conversation Completed Date
- Conversation Created Date
- Employee ID
- Email
- First Name
- Last Name
- Status
- (columns for all of your organization's employee attributes)

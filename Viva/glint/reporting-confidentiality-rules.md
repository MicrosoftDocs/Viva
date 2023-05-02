---
ms.date: 03/29/2023
title: Viva Glint reporting and confidentiality
ms.reviewer: 
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Data privacy and trust are key priorities, and we're constantly evolving ways to protect confidentiality to encourage elevated levels of survey participation and honest and helpful feedback."
---

# Viva Glint reporting and confidentiality

Data privacy and trust are key priorities, and we're constantly evolving ways to protect confidentiality to encourage elevated levels of survey participation and honest and helpful feedback.  

## Understand the terminology 

Use this table to understand logic used throughout the reporting experience: 

| **Term** | **Definition** | 
|---|---|
| **Confidentiality threshold** | The minimum number of survey responses required to show **data**. Viva Glint’s default confidentiality threshold is five responses. |
| **Confidentiality threshold for comments** | The minimum number of survey responses required to show **comments**. Viva Glint’s default confidentiality threshold for comments is 10 responses. Example: if a group of 10 responses provide only three comments, those comments are displayed as written.  |
| **Response rate** | Response rate is the percentage of people who submitted a survey response out of the total number of survey invitations sent.|
| **Suppression** | To prevent guessing the scores of respondent groups with insufficient data using simple math - when group(s) have total respondent counts that don't meet the suppression threshold of 2 - the next smallest group is also suppressed until that threshold is met. *This rule won't be applied when the parent group size is above 400*.  |
| **Suppressed or Suppressed data** | Indicates when data isn't displayed even though it has met the confidentiality threshold. This is because it hasn't met the suppression threshold.  |

## How are data reported? 

Each survey has a minimum number of responses required before calculated results are shown. Viva Glint aggregates (combines) ratings and comments to ensure confidentiality.  

By default, to report numerical scores, at least 5 responses are required (confidentiality threshold) and to report open-ended feedback (comments), 10 respondents are required (confidentiality threshold for comments). Your company’s survey administrator configures these thresholds before launching the survey and are noted before you respond to any survey. Additionally, survey results tied to your personal identity may be available to your employer and is noted, if applicable. 

   > [!NOTE]
   > Take care not to identify yourself in comments by the language you use or what you decide to write. 

## How do thresholds differ for scores and comments? 

Within reporting, a group’s score is visible when there are enough respondents to meet the confidentiality threshold. To protect the confidentiality of small groups and avoid scenarios where scores might be guessed or calculated, scores of groups, which don't meet this threshold aren't displayed. 

A group’s comments are visible when there are enough respondents to meet the confidentiality threshold (typically 10 or more).  To protect the confidentiality of small groups and avoid scenarios where comments might be identifiable, comments of groups, which don't meet this threshold aren't displayed. 

Example: A manager who had seven (7) responses within their team would see a calculated score but not see any comments. A manager with 20 responses would see a calculated score and the comments provided, regardless of how many comments were provided. 

## What is suppression? 

In most scenarios, a manager viewing their own team’s scores will see those scores displayed provided the confidentiality threshold is met. However, when groups’ scores are being compared next to one another, certain confidentiality implications must also be addressed. Viva Glint does this through suppression - a way of hiding groups that may meet the confidentiality threshold but in doing so would mathematically expose an insufficient group. 

Example: A manager receives seven (7) responses from five people in a full-time role and two people in a part-time role. In reporting, the manager will see the aggregated responses for the seven (7), but not be allowed to view the data for the full-time employees, even though they earned the minimum number of responses, because mathematically the responses for those two part-timers would be exposed.  
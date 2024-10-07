---
title: Privacy protection within feedback reporting
description: Survey takers' privacy is protected by setting and communicating a minimum number of responses used in reporting, as well as management of roles and permissions. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
ms.collection: 
- essentials-privacy
f1.keywords: NOCSH
keywords: Thresholds, suppression, response rate, suppressed data, comments threshold, survey items threshold
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: concept-article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/07/2024
---

# Privacy protection within feedback reporting

Survey takers' privacy is protected by setting and communicating a minimum number of responses used in reporting, as well as management of roles and permissions. Your organization configures which roles can access survey data and establishes the minimum response thresholds for each survey program.

A **minimum response threshold** is the lowest number of responses a survey item must receive for its results to be reported. The higher the threshold, the less likely it is that users reviewing a survey report are able to infer the identity of an individual survey taker.

- By default, the minimum response threshold for rating or multiple-choice items is five. 
- For comments, the minimum response threshold is 10.

Your organization can adjust the thresholds, higher or lower, for each survey program, and these thresholds are noted to survey takers.

> [!IMPORTANT]
> Thresholds can't be lowered or raised for programs or cycles after it's launched.
> 
> At the beginning of a survey, the privacy statement informs the participants whether the survey is confidential or identifiable and specifies its minimum response thresholds. Once a program is launched, response thresholds can't be changed. **Changing or altering a minimum response threshold requires a new survey program.** The previous program with the original confidentiality threshold can, however, be drawn into reports for comparison against new results with the new threshold.

## Privacy is protected by managing reporting roles and permissions

Your organization configures who views and configures survey reports at various levels. 

**Example:** 
Your organization might use this reporting hierarchy for its marketing organization and assign permissions accordingly:
- Marketing program managers (PMs) can only view survey results from the team they manage.
- Marketing directors (to whom marketing PMs report) can view survey results for all teams reporting up to them.
- The Chief Marketing Officer (to whom the marketing director reports) can view survey data for the entire marketing organization.

Each reporting group feeds into a hierarchy level, or rollup, giving users visibility related to their role and authority. If the minimum response threshold isn't met for a user's team, their responses aren't reported. Instead, responses are aggregated with and rolled up to the next level.

**Example:**
Consider a survey of the marketing organization in the example above - with the minimum reporting threshold set to five (5). A marketing PM can see aggregated survey responses for any item to which at least five team members responded. But if only four (4) responded to a specific item, the responses for that item aren't shown to the marketing PM. Instead, the responses are combined with those of other employees reporting up through the *marketing director* and rolled in to the next reporting level - the *marketing director*.

## Comments threshold versus survey items threshold

The default minimum response threshold for survey items is five (5), but for comments the default threshold is 10. 

Comments are easier to identify to a respondent. The report user might notice a writing style that is unique to a specific person. The smaller the group, the larger the potential to deduce the survey respondent.

**Example:**
If a manager receives seven (7) responses from their team, they'll see an aggregated score but not the comments. On the other hand, if a manager receives 20 responses, they'll see the calculated score *and* the comments, regardless of the number of comments received.

## Suppression thresholds add protection

In some cases, even when the minimum response threshold is met, the ability to filter a report by attributes might allow a responder to be identified. In these cases, responses are **suppressed**,— they aren't reported even if the minimum response threshold is met. 

> [!IMPORTANT]
> The suppression threshold requires two (2) or more responses that separate the smallest attribute group from the next smallest group that meets the minimum response threshold.

**Example - Marketing PM**
- Five (5) of the six (6) team members are in North America; one (1) is in Europe.
- The organization configured Glint to allow filtering of responses by survey taker region.
- The survey's minimum response threshold is five (5).
- All six (6) team members respond to an item that asks them to rate their manager's communication skills, from 'Very Good' to 'Very Poor.'
- The North America team members all provide a rating of 'Very Good;' the European team member provide a rating of 'Very Poor.'

In this case, the marketing PM can't see the European score because, with only one (1) response from European employees, the minimum response threshold isn't met. But the PM can view the teamwide score (based on six responses) and North American-only score (based on five responses)—right? **No!** Those results are **suppressed**.

**Why?**

By comparing the teamwide score to the North American score, the PM might mathematically be able to determine the score received from the single European team member. When the PM sees that the North American score is 'Very Good,' but the teamwide score isn't, the user might infer that the European team member brought the average down. With a little math, the PM could calculate the exact score the European team member provided.
 
For the North American score to be displayed, there must be more than two (2) responses within the overall team score that aren't within the North American group. So, if the overall team earned eight (8) responses where five (5) were from North America and three (3) were from Europe, the PM sees both the overall team score and the North American score. The, suppression threshold was met.

> [!IMPORTANT]
> The suppression threshold requires two (2) or more responses that separate the smallest attribute group from the next smallest group that meets the minimum response threshold.

**Example - Marketing PM**
- Five (5) of the six (6) team members are in North America; one (1) is in Europe.
- The organization configured Glint to allow filtering of responses by survey taker region.
- The survey's minimum response threshold is five (5).
- All six (6) team members respond to an item that asks them to rate their manager's communication skills, from 'Very Good' to 'Very Poor.'
- The North America team members all provide a rating of 'Very Good;' the European team member provide a rating of 'Very Poor.'

In this case, the marketing PM can't see the European score because, with only one (1) response from European employees, the minimum response threshold isn't met. But the PM can view the teamwide score (based on six responses) and North American-only score (based on five responses)—right? **No!** Those results are **suppressed**.

**Why?**

By comparing the teamwide score to the North American score, the PM might mathematically be able to determine the score received from the single European team member. When the PM sees that the North American score is 'Very Good,' but the teamwide score isn't, the user might infer that the European team member brought the average down. With a little math, the PM could calculate the exact score the European team member provided.

For the North American score to be displayed, there must be more than two (2) responses within the overall team score that aren't within the North American group. So, if the overall team earned eight (8) responses where five (5) were from North America and three (3) were from Europe, the PM sees both the overall team score and the North American score. The, suppression threshold was met.

## More resources

[Understand Glint reporting and confidentiality](/viva/glint/reports/confidentiality-suppression-reports)








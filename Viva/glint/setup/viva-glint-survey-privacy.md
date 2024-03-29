---
title: How Viva Glint helps you protect your privacy
description: Data privacy and trust are key priorities, and Viva Glint is constantly evolving ways to protect confidentiality to encourage elevated levels of survey participation and honest and helpful feedback.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
ms.collection: 
- essentials-privacy
f1.keywords: NOCSH
keywords: Thresholds, suppression, response rate, suppressed data, identifiable surveys
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/21/2024
---

# How Viva Glint helps you protect your privacy

Data privacy and trust are key priorities for Microsoft Viva Glint. Individual privacy is a core Viva Glint value. When survey respondents feel confident that their privacy is protected, they're more likely to participate in surveys and provide honest and constructive feedback. This allows our customers to get the most out of Viva Glint.

## Choose the survey type that meets your needs

Viva Glint uses several methods to inform you about what level of privacy users can expect when responding, starting with the survey types. Viva Glint offers two types of surveys: confidential and identifiable.

### Confidential surveys

For confidential surveys, Viva Glint aggregates (group averages) responses before reporting results. Because it's easier to guess a survey taker's identity when there are just a few responses, confidential survey responses are reported only when an item receives a minimum number of responses. Your organization chooses this number and it might differ for rating/multiple choice questions versus comments. For a survey to be confidential, this minimum number of responses can't be set at less than three (3). 

> [!NOTE]
> Viva Glint surveys might contain three types of items/questions:
>
> - Ratings: Survey takers choose a score on a numerical scale.
> - Multiple choice: Survey takers choose from pre-populated options
> - Comments: Survey takers write in freeform comments.

### Identifiable surveys

In Identifiable surveys, survey takers' identities might be directly or indirectly available within reporting. The minimum response threshold for these surveys is less than three. An example of an identifiable survey could be a company's exit survey, where viewing responses for each departing employee is desired.

## Use your organization's statement about privacy

At the beginning of each Viva Glint survey, survey takers are presented with a statement configured by your organization. 

### How does a statement about privacy help?

This statement provides information about who can see survey takers' identifiable responses and under what circumstances. It specifies whether the survey is confidential or identifiable, and the minimum response threshold set by your organization. It also notifies survey takers of any potential admin access to identifiable survey responses and provides links to more Microsoft privacy documentation (more on this follows). Your organization can also choose to include a link to its employee privacy policy or other documentation about how it handles survey data.

### A statement about privacy advises access and data handling of survey responses

Even for confidential surveys, your organization's customer admin might be able to access identifiable survey responses. This access might be necessary for an organization to meet its legal obligations, such as [Data Subject Rights under GDPR](/microsoft-365/admin/security-and-compliance/gdpr-compliance?view=o365-worldwide&preserve-view=true). However, your organization can choose to opt out of this access on a survey-by-survey basis using admin controls. 

> [!IMPORTANT]
> A statement is automatically selected based on your program setup configurations.

## Confidential surveys that do not support raw survey responses export
If your organization chooses to restrict the export of raw survey responses for confidential surveys, the following statement is applied to surveys. 

> Your responses are confidential and reported to Contoso in aggregate groups of 5 or more respondents. Write-in comments are reported verbatim if at least 10 people respond to a question. Take care not to identify yourself in the comments. Microsoft Viva Glint Reporting and Confidentiality Rules describe other ways your data might be accessed and your organization's Privacy Policy also has more information.

## Confidential surveys that do support raw survey responses export

If your organization approved making raw survey responses available for a particular survey, survey takers are informed in this statement:

> Your responses are confidential and reported to Contoso in aggregate groups of 5 or more respondents. Write-in comments are reported verbatim if at least 10 people respond to a question. Take care not to identify yourself in the comments. A limited number of people at [organization name@email address] will have access to your identifiable survey responses. See [Microsoft Viva Glint Reporting and Confidentiality Rules](https://go.microsoft.com/fwlink/?linkid=2230922), which describes other ways your data may be accessed and your organization's privacy policy for more information.

## Identifiable surveys

If your organization opts to create an identifiable survey, this statement is applied:

> Note that this is an identifiable survey, which means Contoso will be able to see that your survey responses came from you. See your organization's Privacy Policy for more information. Learn how Viva Glint handles survey responses in [Microsoft Viva Glint Reporting and Confidentiality Rules](https://go.microsoft.com/fwlink/?linkid=2230922).

> [!NOTE]
> The Confidentiality and Comments Threshold set for the survey program will automatically become the default statement for your programs.

## How is privacy protected within survey results reporting?

Survey takers' privacy is protected by setting and communicating a minimum number of responses used in reporting, as well as management of roles and permissions. Your organization configures who has access to survey data and establishes the minimum response thresholds for each survey program.

A minimum response threshold is the minimum number of responses a survey item must receive for its results to be reported. The higher the level of aggregation, the less likely it is that users reviewing a survey report will be able to infer the identity of an individual survey taker.

By default, the minimum response threshold for rating or multiple-choice items is set at five, while for open-ended comments, it's set at 10. Your organization can adjust the thresholds, either higher or lower, for each survey program, and these thresholds are noted to survey takers.

> [!NOTE]
> To be classified as a confidential survey, the minimum number of responses must be three (3) or higher. If the threshold is below three (3), the survey is identifiable.

At the beginning of each survey, the privacy statement informs survey takers whether the survey is confidential or identifiable and specify its minimum response thresholds, if any. Once a survey program is launched, its minimum response thresholds can't be changed. Changing or altering a minimum response threshold requires a new survey program. The previous program with the original confidentiality could, however, be drawn into reports for comparison against new results with the new threshold.

## Privacy is protected by managing reporting roles and permissions

Your organization configures who might view and configure survey reports at various levels. For instance, your organization might use the following reporting hierarchy for its marketing organization and assign permissions accordingly:

1. Marketing program managers (PMs) can only view survey results from the team they manage.
2. Marketing directors (to whom marketing PMs report) can view survey results for all the teams reporting up through them.
3. The Chief Marketing Officer (to whom the marketing director reports) can view survey data for the entire marketing organization.

Each of these reporting groups feeds into a hierarchy level, or roll up, giving users visibility commensurate with their scope and authority.

If the minimum response threshold isn't met at for a user's team, their responses won't be reported at that level; instead, they'll be aggregated with extra responses and rolled up to the next level.

Consider a survey of the marketing organization described above with the minimum reporting threshold set to five (5). A marketing PM is able to see aggregated survey responses for any item to which at least five (5) of their team members responded. But if only four (4) responded to a specific item, the responses for that item aren't shown to the marketing PM. Instead, the responses are combined with those of other employees reporting up through the marketing director and rolled up the next reporting level - the marketing director. The PM won't see survey data for that item because the minimum response threshold wasn't met. As the threshold was met at the reporting level above, the survey data is included in the director's report.

## Why does the comments threshold differ from the survey items threshold?

The default minimum response thresholds for ratings and multiple-choice questions are five (5) but for comments the default threshold is 10. Comments are easier to identify to a respondent. The report user might notice a writing or grammatical style that is unique to a specific person. The smaller the group, the larger the potential to deduce the survey respondent.

**Example:** If a manager receives seven (7) responses from their team, they'll see an aggregated score but not the comments. On the other hand, if a manager receives 20 responses, they'll see both the calculated score and the comments, regardless of the number of comments received.

## Suppression thresholds add further protection

In some cases, even when the minimum response threshold is met, the ability to filter reporting by responder attributes and then compare those filtered results to nonfiltered results might allow a responder to be identified. In these cases, responses are **suppressed**,—meaning they aren't reported even if the minimum response threshold is met. The suppression threshold requires more than two responses that separate the smallest attribute group from the smallest group that meets the minimum response threshold.

Consider a marketing PM from the example above, given the following:

- Five (5) of the six (6) team members are in North America; one (1) is in Europe.
- The organization has configured Viva Glint to allow filtering of responses by survey taker region.
- The survey's minimum response threshold is set to five (5).
- All six (6) team members respond to a question that asks them to rate their manager's communication skills from 'Very Good' to 'Very Poor.'
- The North America team members all provided a rating of 'Very Good;' the European team member provided a rating of 'Very Poor.'

In this case, the marketing PM can't see the European score because, with only one (1) response from European employees, the minimum response threshold isn't met. But the PM can view the teamwide score (based on six responses) and North American-only score (based on five responses)—right? **No!** Those results are **suppressed**.

**Why?**

> By comparing the teamwide score to the North American score, the marketing PM might be mathematically able to determine the score received from just the single European team member. When the PM sees that the North American score is 'Very Good' but the teamwide score isn't, the user might correctly infer that the European team member brought the average down. With a little math, the marketing PM might be able to calculate the exact score the European team member provided. For the North American score to be displayed, there needs to be more than two responses within the overall team score that aren't within the North American group. So, if the overall team earned eight responses where five were from North America and three were from Europe, the marketing PM sees both the overall team score and the North American score, having exceeded the suppression threshold.

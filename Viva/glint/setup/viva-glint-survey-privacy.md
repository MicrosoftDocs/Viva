---
title: How Viva Glint helps you protect your privacy
description: Data privacy and trust are key priorities, and Viva Glint is constantly evolving ways to protect confidentiality to encourage elevated levels of survey participation and honest and helpful feedback.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: Thresholds, suppression, response rate, suppressed data, identifiable surveys
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 04/10/2023
---

# How Viva Glint helps you protect your privacy

Data privacy and trust are key priorities for Microsoft Viva Glint. Not only is individual privacy a core Viva Glint value, when survey respondents feel confident that their privacy will be protected, they're more likely to participate in surveys and provide honest and constructive feedback, allowing our customers to get the most out of Viva Glint.

## Choose the survey type that meets your needs

Viva Glint uses several methods to inform you about what level of privacy users can expect when responding, starting with the survey types. Viva Glint offers two types of surveys: confidential and identifiable.

### Confidential surveys

For confidential surveys, Viva Glint aggregates (group averages) responses before reporting results. Because it's easier to guess a survey taker's identity when there are few responses, confidential survey responses are only reported when a survey item (question) receives a minimum number of responses. This number is set by your organization and may differ for rating/multiple choice questions versus comments. For a survey to be confidential, this minimum number of responses can't be set below three. More information on "minimum response thresholds" is provided below.

> [!NOTE]
> Viva Glint surveys may contain three types of questions:
>
> - Ratings: Survey takers choose a score on a numerical scale.
> - Multiple choice: Survey takers choose from pre-populated options
> - Comments: Survey takers write in freeform comments.

### Identifiable surveys

In Identifiable surveys, survey takers' identities may be directly or indirectly available within reporting. The minimum response threshold for these surveys is below three. An example of an identifiable survey could be a company's exit survey, where viewing responses for each departing employee is desired.

## Use your organization's privacy statement

### How can a privacy statement help?

At the beginning of each Viva Glint survey, survey takers are presented with a privacy statement, tailored to the specific survey as configured by your organization. This statement provides information about who can see survey takers' identifiable responses and under what circumstances. It specifies whether the survey is confidential or identifiable, and the minimum response threshold set by your organization. It also notifies survey takers of any potential admin access to identifiable survey responses (see more on this below) and provides links to more Microsoft privacy documentation. Your organization can also choose to include a link to its employee privacy policy or other documentation about how it handles survey data.

### A privacy statement advises access and data handling of survey responses

Even for confidential surveys, your organization's customer admin may be able to access identifiable survey responses. This access may be necessary for an organization to meet its legal obligations, such as [Data Subject Rights under GDPR](/microsoft-365/admin/security-and-compliance/gdpr-compliance?view=o365-worldwide&preserve-view=true). However, your organization can choose to opt out of this on a survey-by-survey basis using Viva Glint admin controls. If your organization has approved making raw survey responses available for a particular survey, survey takers will be informed in the privacy statement, which will state, in part: "A limited number of people at [your organization's name**]** will have access to your identifiable survey responses."

In addition, your organization will have access to identifiable survey responses if it determines that such access is necessitated by "extreme circumstances," such as suspected illegal activity, fraud, threats of physical harm, or legal obligation. The confidentiality statement will make this clear to survey takers, stating [Your organization's name] may access your identifiable survey responses if it determines that extreme circumstances exist." In addition, logs will be generated and available to your organization when survey responses are accessed in this way.

## How is privacy protected within survey results reporting?

Survey takers' privacy is protected by setting and communicating a minimum number of responses used in reporting, as well as management of roles and permissions. Your organization configures who has access to survey data and establishes the minimum response thresholds for each survey program.

A minimum response threshold is the minimum number of responses a survey item must receive for its results to be reported. The higher the level of aggregation, the less likely it is that users reviewing a survey report will be able to infer the identity of an individual survey taker.

By default, the minimum response threshold for rating or multiple-choice items is set at five, while for open-ended comments, it's set at 10. Your organization can adjust the thresholds, either higher or lower, for each survey program, and these thresholds are noted to survey takers.

> [!NOTE]
> To be classified as a confidential survey, the minimum number of responses must be three or higher. If the threshold is below three, the survey is identifiable.

At the beginning of each survey, the privacy statement will inform survey takers whether the survey is confidential or identifiable and specify its minimum response thresholds, if any. Once a survey program has been launched, its minimum response thresholds can't be changed. Changing or altering a minimum response threshold requires a new survey program. The previous program with the original confidentiality could, however, be drawn into reports for comparison against new results with the new threshold.

## Privacy is protected by managing reporting roles and permissions

Your organization can configure who may view and configure survey reports at various levels. For instance, your organization might use the following reporting hierarchy for its marketing organization and assign permissions accordingly:

1. Marketing program managers (PMs) can only view survey results from the team they manage.
2. Marketing directors (to whom marketing PMs report) can view survey results for all the teams reporting up through them.
3. The Chief Marketing Officer (to whom the marketing director reports) can view survey data for the entire marketing organization.

Each of these reporting groups feeds into the hierarchy level above, or roll up, giving users in your organization visibility commensurate with their scope and authority.

If the minimum response threshold isn't met at for a user's team, their responses won't be reported at that level; instead, they'll be aggregated with extra responses and rolled up to the next level.

For example, consider a survey of the marketing organization described above with the minimum reporting threshold set to five. A marketing PM would be able to see aggregated survey responses for any question to which at least five of their team members responded. But if only four responded to a specific question, the responses for that question wouldn't be shown to the marketing PM. Instead, the responses would be combined with those of other employees reporting up through the marketing director and rolled up the next reporting level - the marketing director's report. The PM wouldn't be able to see survey data for that question because the minimum response threshold wasn't met. However, because the threshold was met at the reporting level above, the survey data would be included in the director's report.

## Why does the comments threshold differ from the survey items threshold?

As stated above, the default minimum response thresholds for ratings and multiple-choice questions are five but for the comments the default threshold is 10. The reason for the higher threshold is due to comments being easier for the user to infer which survey respondent provided the feedback. As comments are reported as written (verbatim), the report user may notice a writing or grammatical style that is unique to a specific person. The smaller the group, the larger the potential to deduce the survey respondent.

**Example:** If a manager receives seven (7) responses from their team, they'll see an aggregated score but not the comments. On the other hand, if a manager receives 20 responses, they'll see both the calculated score and the comments provided, regardless of the number of comments received.

## Suppression thresholds add further protection

In some cases, even when the minimum response threshold is met, the ability to filter reporting by survey responder attributes (like title or location) and then compares those filtered results to nonfiltered results may allow a survey responder's identify to be inferred. In these cases, responses are "suppressed"—meaning, not reported even if the minimum response threshold was met. The suppression threshold requires more than two responses that separate the smallest attribute group from the smallest group that meets the minimum response threshold.

Consider a marketing PM from the example above, given the following:

- Five of the six team members are in North America; one is in Europe.
- The organization has configured Viva Glint to allow filtering of responses by survey taker region.
- The survey's minimum response threshold is set to five.
- All six team members respond to a question that asks them to rate their manager's communication skills from 'Very Good' to 'Very Poor.'
- The North America team members all provided a rating of 'Very Good;' the European team member provided a rating of 'Very Poor.'

In this case, the marketing PM can't see the European score because, with only one response from European employees, the minimum response threshold isn't met. But the PM can view the teamwide score (based on six responses) and North American-only score (based on five responses)—right? No! Those results are **suppressed**.

Why? Because, by comparing the teamwide score to the North American score, the marketing PM may be mathematically able to determine the score received from just the single European team member. When the PM sees that the North American score is 'Very Good' but the teamwide score isn't, the user may correctly infer that the European team member brought the average down. With a little math, the marketing PM may be able to calculate the exact score the European team member provided. For the North American score to be displayed, there needs to be more than two responses within the overall team score that aren't within the North American group. So, if the overall team earned eight responses where five were from North America and three were from Europe, the marketing PM sees both the overall team score and the North American score, having exceeded the suppression threshold.
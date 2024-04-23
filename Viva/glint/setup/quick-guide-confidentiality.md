---
title: Manager Quick Guide - Confidentiality
description: Suppression thresholds add a layer of protection to your peoples' privacy. Learn about data suppression and insufficient data suppression.
author: JudyWeiner
ms.author: JudithWeiner
manager: MelissaBarry
audience: admin
f1.keywords: insufficient responses, insufficient data, confidentiality
keywords: Microsoft Privacy Statement 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 12/05/2023
---

# Manager Quick Guide - Confidentiality
Suppression thresholds add a layer of protection to your peoples' privacy. In some cases, even when the **response threshold** is met, the ability to filter results by responder attributes and might allow a responder's identify to be inferred by comparing results. 

In these cases, responses are "suppressed" — not reported even if the minimum response threshold was met. The *suppression threshold* requires more than two responses that separate the smallest attribute group from the smallest group that meets the minimum response threshold.

## Understand insufficient and sufficient data suppression
**Viva Glint protects the confidentiality of individual survey responses** 

- For confidential surveys, Viva Glint doesn't show individual responses. Within reports, scores are only shown in combined totals. 
- To analyze data by different populations, Viva Glint needs to connect scores to individuals, but this data can only be seen in a restricted raw data file. Data is private and can only be pulled by system administrators. 
- Viva Glint doesn't show scores for teams or groups that fall below the confidentiality threshold and limits the use of filters that could inadvertently reveal confidential information. 

**Viva Glint’s sets standard confidentiality thresholds** 
- 5 respondents per reporting group to display scores 
- 10 respondents per reporting group (not 10 comments) to display open- ended comments (if a manager’s team had 10 responses but only 1 comment, that comment shows) 

**The difference between insufficient data and suppressed data** 
- A manager sees an insufficient data message if the number of respondents or total group size doesn’t meet the minimum threshold set. 
- To prevent guessing the scores of respondent groups with insufficient data using simple math, the next smallest group is also suppressed.  

Let’s check out an example... 

Michelle’s team has five (5) or more respondents, but their score is not displayed. Why?

| Group | All | Amy's team | Mike's team | Michelle's team | Dave's team |
|:-------:|:-----:|:------------:|:-------------:|:-----------------:|:-------------:|
|**Respondents**|23|10|7|5|1|
|**Score**|73|76|76|~~76~~|?|
|**Display Status**|Displayed|Displayed|Displayed|Suppressed|Insufficient|

The chart tells us that:
- Dave’s team, with only one (1) respondent, is insufficient. It does not meet the minimum confidentiality threshold of five (5) required respondents, therefore, the score from Dave’s team is not displayed. 
- Michelle’s team has the next smallest number of respondents, and her team met the minimum threshold of five (5) required respondents. However, by displaying Michelle’s team’s score, it may become possible to deduce Dave’s team score using simple math. With calculation, the one respondent on Dave’s team can be discovered, breaching that individual respondent’s confidentiality. In turn, Michelle’s team scores are suppressed and not visible. 
- If Dave’s team had two (2) respondents it would be difficult to calculate both individual scores, so Michelle’s team’s score would be displayed. 
> [!NOTE]
> Dave’s team score, even with two (2) respondents, won't be shown because it still doesn't meet the confidentiality threshold. 

## More Resources
Refer to the following pages for additional guidance:
>**Microsoft Learn Documentation** 
- [How Viva Glint helps you protect your data privacy](viva-glint-survey-privacy.md)
>**Microsoft Learn Training**
- [What are the basics of how Viva Glint emphasizes confidentiality?](/training/modules/viva-glint-learn-how-setup-viva-glint/4-what-basics-viva-glint-emphasizes-confidentiality)
- [What is Viva Glint confidentiality and how do I navigate the Viva Glint app?](/training/modules/viva-glint-navigate-share-viva-glint-results/1-describe-confidentiality-navigate-viva-glint)


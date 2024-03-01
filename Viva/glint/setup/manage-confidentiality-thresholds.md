---
title: Manage Viva Glint confidentiality thresholds
description: Use the guidance in this article to adjust confidentiality thresholds at the overall level or at the survey program level and understand the impact of those changes.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: privacy, confidentiality threshold, survey threshold, overall threshold, suppression
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/01/2024
---

# Manage Viva Glint confidentiality thresholds

Data privacy and trust are key priorities for Microsoft Viva Glint. Several methods are used to inform you, as the Glint Admin, about what level of privacy users can expect when responding. Viva Glint offers confidential surveys, where scores only display with at least three (3) responses, and identifiable surveys for Lifecycle survey types, where the response threshold is less than three (3). [Learn more](https://go.microsoft.com/fwlink/?linkid=2238614). Use the guidance in this article to adjust confidentiality thresholds at the overall level or at the survey program level and understand the impact of those changes.

> [!NOTE]
> To use Viva Glint default confidentiality thresholds, no action is needed.

## Understand confidentiality thresholds

Threshold settings determine how items scores, response rates, and comments display for Viva Glint users. Read threshold descriptions to understand each setting and determine if and how to adjust thresholds for confidential surveys where the default threshold to display scores is five (5) but can be adjusted to as low as three (3) responses.

### Rated question scores

Review the following information for thresholds related to confidentiality and suppression. These thresholds determine how Viva Glint evaluates scores and respondent groups as insufficient or suppressed in reports. Use the adjusted setting options information as a guide for updating values from Viva Glint default settings.

> [!NOTE]
> Affected Viva Glint reports: Dashboard, Executive Summary, Heat Map, Overall Results, Manager Report, Team Summary, Multi-Attribute Export

|Threshold   |Description  |Default setting|Adjusted setting options|
|----------|-----------|------------|------------|
|Rated Confidentiality     |Also known as: Minimum Sample Size. Numerical scores for rated questions aren’t displayed for respondent groups smaller than this threshold.       |5        |3 or 4        |
|Suppression|Also known as: Minimum Group Size. To prevent guessing the scores of respondent groups with insufficient data using simple math, the next biggest group is suppressed until the total number of insufficient + suppressed responses equal or exceed this number.  |2|1 or 2|
|Parent Team Suppression     |Also known as: No Suppression Parent Team Size. Allow users to access results for parent teams that would have been suppressed where the parent team respondents count is larger than or equal to this threshold.       |400        |200x the selected Suppression threshold        |

### Response rates

Match this threshold to the Rated Confidentiality threshold for a consistent reporting experience across question scores and response rates.

|Threshold   |Description  |Default setting|Adjusted setting options|
|----------|-----------|------------|------------|
|Response Rate  |Also known as: Minimum Sample Size Survey Stats. Response rate (percentage and counts) can't be displayed for groups smaller than this number.       |5        |Match the Rated Confidentiality threshold: 3 or 4        |

### Comments

Determine how open-ended feedback displays for users depending on how many survey responses Viva Glint receives. Match these thresholds for a consistent comments report experience. Comments thresholds don’t necessarily need to match other reporting thresholds

|Threshold   |Description  |Default setting|Adjusted setting options|
|----------|-----------|------------|------------|
|Comments Search    |Also known as: Minimum Respondent Size for Comments. Minimum number of responses (not comments) to a survey before comments are viewable and searchable.      |10        |Increase or decrease based on the level of confidentiality needed in the comments report       |
|Comments Confidentiality    |Also known as: Minimum Group Size for Comments. Comments aren't displayed for respondent groups smaller than this threshold for the specific grouping selected in reporting, based on attribute or topic filtering.      |10        |Increase or decrease based on the level of confidentiality needed in the comments report       |

## Examples

### Viva Glint default settings

When Viva Glint default confidentiality thresholds are in place for rated questions, here's an example of how manager team scores display in reporting.

 - Rated Confidentiality: 5
 - Suppression: 2
 - Parent Team Suppression: 400

|Team   |Score  |Respondents|Insufficient or suppressed|
|----------|-----------|------------|------------|
|Manager A's Team     |--       |0        |insufficient        |
|Manager B's Team     |--      |0|insufficient|
|Manager C's Team     |--      |1        |insufficient        |
|Manager D's Team     |--      |350        |suppressed        |
|Manager E's Team     |83      |405        |        |
|Manager F's Team     |80       |425        |        |

In this case, all teams with insufficient respondents are 0 + 0 + 1, which is less than the suppression threshold of two (2). The next largest team, Manager D’s Team, is suppressed because the respondent count doesn’t meet the Parent Team Suppression threshold of 400.

### Adjusted settings

When adjusted confidentiality thresholds are in place for rated questions, here's an example of how manager team scores display in reporting.

 - Rated Confidentiality: 3
 - Suppression: 1
 - Parent Team Suppression: 200

|Team   |Score  |Respondents|Insufficient or suppressed|
|----------|-----------|------------|------------|
|Manager A's Team     |--       |0        |insufficient        |
|Manager B's Team     |--      |0|insufficient|
|Manager C's Team     |--      |1        |insufficient        |
|Manager D's Team     |100      |3        |        |
|Manager E's Team     |83      |7        |        |
|Manager F's Team     |80       |10       |        |

In this case, all teams with insufficient respondents are 0 + 0 + 1, which meets the suppression threshold of one (1). The rated confidentiality is also set to 3, so the next largest team, Manager D’s team, displays in reporting. Parent team suppression is only factored in when the Suppression threshold isn't met.

## Update overall or survey thresholds
Thresholds set the number of survey responses that are needed for data to display. For example, when Viva Glint default settings are in place, a manager who has 10 total employees with 5 respondents sees their aggregated scores. However, if that same manager had only 1 employee respond, the survey responses are insufficient and don’t display in reports. These thresholds prevent a situation where a manager can identify the respondent based on their responses. Given this potential impact, Human Resources, Privacy, and Legal teams may have input about how these thresholds are adjusted.

### Overall thresholds
If all your Viva Glint survey programs will have the same level of confidentiality, select threshold values at the overall level on the **Advanced Configuration Details** page.

> [!IMPORTANT]
> Changes to these thresholds impacts closed and active surveys.

To edit threshold values:

1. From the admin dashboard, select **Configuration**, then in **Service Configuration**, choose **Advanced Configuration**.
1. On the **Details** page, enter new values in each threshold field for rated question scores, response rates, and comments.
   1.  Use the information in the [Understand confidentiality thresholds](#understand-confidentiality-thresholds) section to find descriptions of thresholds, default values, and impacted reports.
1. Select **Save Changes** at the bottom of the page.

### Survey thresholds

If your Viva Glint survey programs will have different levels of confidentiality, select threshold values at the survey level from the Advanced Configuration Surveys page.

> [!IMPORTANT]
> - Survey-level reporting thresholds can only be adjusted before a survey is live and enabled.
> - When survey-level reporting thresholds are in place, they override settings at the overall level.

To edit threshold values:

1. From the admin dashboard, select **Configuration**, then in **Service Configuration**, choose **Advanced Configuration**.
1. In the menu on the left, select **Surveys** and choose a survey from the list.
2. On the **Survey Details** page, enter new values in each threshold field for rated question scores, response rates, and comments.

   > [!NOTE]
   > The survey must be in DRAFT state to make any edits. Undo the **Approved** toggle in Program Summary to make changes.

   2.  Use the information in the [Understand confidentiality thresholds](#understand-confidentiality-thresholds) section to find descriptions of thresholds, default values, and impacted reports.
1. Select **Save Changes** at the bottom of the page.

## Identifiable surveys

> [!NOTE]
> This feature is planned to be available after March 9, 2024.

Viva Glint Lifecycle surveys, Exit and Onboarding, can be made identifiable during [program setup](https://go.microsoft.com/fwlink/?linkid=2238328) with the **Confidential Responses** setting, which automatically updates thresholds at the survey level. Consider this confidentiality level for this survey type, which has typically lower respondent counts and may lead to follow-up with individual employees based on their exit or new hire experiences.

---
title: Understand Viva Glint confidentiality and suppression in reports
description: Threshold settings determine how items scores, response rates, and comments display for Microsoft Viva Glint users.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: privacy, confidentiality, suppression, threshold, filter suppression, comments suppression when using a question response filter
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 08/14/2024
---

# Understand Viva Glint confidentiality and suppression in reports

Threshold settings determine how item scores, response rates, and comments display for Microsoft Viva Glint users. Use this guidance to understand each threshold and gain a better understanding of how users' confidentiality is protected in different reports based on these settings. For more information on adjusting confidentiality thresholds, see: [Manage Viva Glint confidentiality thresholds](/viva/glint/setup/manage-confidentiality-thresholds).

> [!IMPORTANT]
> Images that include teams and attributes noted as "Not displayed" are for illustrative purposes only. Scores, response rates, and comments that don't meet Viva Glint confidentiality and suppression thresholds aren't displayed in reports.

## Rated Confidentiality Threshold

|Definition  |Default setting   |
|:----------|:-----------|
|The minimum number of responses required to show scores and response counts for rated items.   |Viva Glint’s default Confidentiality Threshold is five (5).       |

### Related terms

**Insufficient:** Indicates that the Confidentiality Threshold isn't met and a group’s scores don't display.

### Example

Two of Ángel Valádez’s teams don’t have enough respondents to meet the rated confidentiality of five (5), so their respondent counts and scores don’t display in reporting.

- **Rated Confidentiality Threshold:** 5
- **Suppression Threshold:** 2
- **Parent Team Suppression Threshold:** 400

:::image type="content" source="../../media/glint/reports/heat-map-mgr-insufficient.png" alt-text="Screenshot of a heat map report where a manager team has insufficient results.":::

## Suppression Threshold

|Definition  |Default setting   |
|:----------|:-----------|
|To protect the identity of groups whose responses are insufficient, the Suppression Threshold suppresses the next smallest group until the total responses of the insufficient groups meet this threshold.    |Viva Glint’s default Suppression Threshold is two (2).       |

### Related terms

**Filter suppression:** To add another layer of protection, admins can enable filter suppression, which prevents users from isolating what should be suppressed groups with report filtering. To enable, go to **Configuration**, choose **Advanced Configuration**, and in the **Details** section select the checkbox next to **Enable Filter Suppression on Scores** and **Save Changes**.

### Examples

#### Example 1

Ana Bowman’s team doesn't meet the rated confidentiality of five (5) and Ángel Valádez’s directs are suppressed to protect the identity of Ana Bowman’s team respondent.

- **Rated Confidentiality Threshold:** 5
- **Suppression Threshold:** 2
- **Parent Team Suppression Threshold:** 400

:::image type="content" source="../../media/glint/reports/heat-map-mgr-suppressed.png" alt-text="Screenshot of a heat map report where a manager team has insufficient results and another manager team is suppressed.":::

#### Example 2

When a user views Department scores side by side, Executives and Support aren't displayed in reports. The Executives department doesn’t meet the rated confidentiality threshold with a respondent count of one (1). To protect the identity of the respondent for the Executives department, the next largest team, Support, is suppressed.

- **Rated Confidentiality Threshold:** 5
- **Suppression Threshold:** 2
- **Parent Team Suppression Threshold:** 400

:::image type="content" source="../../media/glint/reports/heat-map-dept-suppressed.png" alt-text="Screenshot of a heat map report where an Executives Department has insufficient results and the Support Department is suppressed.":::

## Parent Team Suppression Threshold

|Definition  |Default setting   |
|:----------|:-----------|
|This threshold acts as an exception to allow what would be suppressed data to display when the group's response count meets the threshold.    |Viva Glint’s default Parent Team Suppression Threshold is 400 (200 times the Suppression Threshold).       |

### Example

When a user views Department scores side by side, Executives isn't displayed in reports. The Executives department doesn’t meet the rated confidentiality threshold with a respondent count of one (1). Support’s respondent count exceeds the parent team suppression threshold of 400, so data isn’t suppressed, and scores display for Support.

- **Rated Confidentiality Threshold:** 5
- **Suppression Threshold:** 2
- **Parent Team Suppression Threshold:** 400

:::image type="content" source="../../media/glint/reports/heat-map-dept-insufficient.png" alt-text="Screenshot of a heat map report where an Executives Department has insufficient results.":::

## Response Rate Threshold

|Definition  |Default setting   |
|:----------|:-----------|
|Response rates (percentages and counts) can't be displayed for groups smaller than this number. For a consistent reporting experience across item scores and response rates in reports, this threshold matches the Rated Confidentiality Threshold.    |Viva Glint’s default Response Rate Threshold is five (5).    |

### Example

Ana Bowman's Team is flagged as insufficient in the Response Rate report because the team didn't meet the response threshold of five (5).

:::image type="content" source="../../media/glint/reports/response-rate-insufficient.png" alt-text="Screenshot of a response rate report with an insufficient team.":::

## Comments Confidentiality Threshold

|Definition  |Default setting   |
|:----------|:-----------|
|To avoid scenarios where comments might be tied back to the respondent, comments for groups that don't meet this survey response (not comments) threshold aren't displayed.   |Viva Glint’s default Comments Confidentiality Threshold is 10.    |

### Example

Ana Bowman's team doesn't have enough responses to meet the Comments Confidentiality Threshold of 10, so filtering to the team in the Comments report gives an insufficient data message.

:::image type="content" source="../../media/glint/reports/comments-insufficient.png" alt-text="Screenshot of a comments report with an insufficient data message.":::

## Comments Search Threshold

|Definition  |Default setting   |
|:----------|:-----------|
|To avoid scenarios where comments might be tied back to the respondent, comments for filtered groups aren't visible or searchable until survey responses (not comments) meet this number.  |Viva Glint’s default Comments Search Threshold is 10.   |

### Example

This manager's team has 13 respondents (not comments or commenters), which allows the four comments left by these users to be viewed by their manager. But, when their manager filters to the topic of teamwork, they see a message that data is insufficient. The topic of teamwork doesn't meet the Comment Search Threshold of 10 respondents.

:::image type="content" source="../../media/glint/reports/comments-topic-insufficient.png" alt-text="Screenshot of a comments report with an insufficient data message when filtering to a specific topic.":::

## Comment Suppression Thresholds when using a question response as a filter 

In addition to filtering cross program, users can filter by question responses (e.g. users who responded favorably to the eSat question). To ensure additional protection in instances where results are filtered by responses, a minimum threshold of **10 for scores** and **20 for comments** is enforced. 

When reporting in a program with a lower threshold, this threshold (10 for scores, 20 for comments) only applies when using a question response filter. If your thresholds are already higher than these thresholds, the system picks the largest threshold across the programs being reported on.

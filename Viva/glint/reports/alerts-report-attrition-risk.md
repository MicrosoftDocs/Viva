---
title: The Viva Glint Alerts report and Attrition Risk Index
description: The Alerts report finds statistically significant patterns, outliers, and deviations from past scores to surface populations or demographic groups that have opportunities for improvement.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: driver impact report
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 06/18/2024
---

# The Viva Glint Alerts report and Attrition Risk Index

Microsoft Viva Glint's Alerts algorithm finds statistically significant patterns, outliers, and deviations from the scores in survey data and surfaces populations or demographic groups that have:

- Low or high scores
- Notable changes in scores

The Alerts report is found on the **Reports** tab of the admin dashboard. Alerts are visible only to admins.

>[!NOTE]
> To qualify for an alert, statistically notable insights are determined using p-value (default: 0.05), select thresholds for the minimum population size (default: 20 respondents), and the minimum score difference or change (default: 8 points).

## Select attributes in General Settings to generate an Alerts report

>[!IMPORTANT]
>Attributes must be preselected in [General Settings](https://go.microsoft.com/fwlink/?linkid=2230744) for an Alerts report to generate. Create alerts based on specific user attribute combinations. If no attributes are selected, no alerts are created.

:::image type="content" source="../../media/glint/reports/reports-alerts-attributes.png" alt-text="Screenshot of the dropdown box in General Settings to choose attributes that will trigger Alert reporting." lightbox="../../media/glint/reports/reports-alerts-attributes.png":::

Populations are defined by the attributes in your Employee Attribute File. The alerts algorithm searches for patterns within single attributes (for example, Team: Sales > Corporate Sales) and combinations of attributes (for example, gender and tenure > 5 years). If a population or demographic group has scores for items that are statistically significant, that group is tagged for an alert.

Configure which demographic attributes are used by the alerts algorithm:

- **Alerts for low and high scores:** For low and high scores, the algorithm uses comparisons against the external benchmark and Company average.
- **Alerts for changes to scores:** The algorithm looks for notable changes to scores between the current survey and the last time each item appeared on a survey.
- **Hierarchies:** Alerts are smart about hierarchies and display only the highest relevant level for any given survey item.

### Learn from working examples

Example #1:

If all the subpopulations in Engineering have low scores on *Purpose* and *Role*, but one subpopulation of Engineering (for example, *Engineering & Tenure > 5 years*) has low scores for *Career*, then two Alert populations will be visible:

- Engineering for both questions – *Purpose and Role*
- Engineering & Tenure > 5 years for the question on Career

>[!NOTE]
> If certain demographic groups are highly correlated with other demographics, multiple alerts may be generated for the same underlying population.

Example #2:

Consider that everyone in *Sales in Location (California)* was hired in the last year and also that everyone hired in the last year in sales went to California. If this group had a low score, the algorithm may generate two Alerts - one for *Sales in California*, and *Sales in California with Tenure < 1 year*, since the two groups are the same.

### Attrition Risk Index

The Elevated Attrition Risk, part of the Alerts report, is key for providing information about populations that may be at elevated risk for turnover.

Glint can predict the effect of score differences and overall response profiles of each population for employee attrition. The Attrition Risk Index is a model trained on aggregated turnover data across all Glint clients and predicts elevated risk for voluntary attrition based on standard item scores.

Populations identified with elevated attrition risk are those that show a higher future attrition rate than your company's average.

Based on extensive cross-validation studies, when using our standard survey questions/items, risk alerts have a precision of at least 80% and in many cases, even higher. If a population is flagged for elevated attrition risk, there is at least an 80% chance that attrition will be elevated.

The model uses Glint standard items in making predictions to allow for the most useful information to be available. Outcome items - eSat and Recommend - are immensely powerful and are a proxy for many insights, so a minimal set of items should include at least eSat and Recommend.

>[!TIP]
> Regularly incorporate the Alerts report into your Viva Glint dashboard.

>[!NOTE]
>The Elevated Attrition Risk model was updated in October 2022.

## Set up the Alerts report

Configure which demographic attributes you want to include in **Alerts** from **General Settings** on the admin dashboard. To configure them initially, or to change them over time:

1. Navigate to **Reporting,** then **Attributes for Alerts.**
2. From the attributes you have preselected in your Employee Attribute File, narrow down to those items *most important to attrition risk* within your organization.
    - Use the Search box to add attributes.
    - Delete attributes by choosing the **X** next to those you don't want on the report.

 >[!TIP]
 > Select only attributes that are necessary for Alerts, such as important hierarchies, tenure, and generation. Avoid  attributes with many values that can't be grouped, such as hire date, birth date and manager email. Using all attributes doesn't surface helpful insights.

3. Select thresholds for the minimum population size (default is 20 respondents) and the minimum score differences (default is eight points) that qualifies for an alert. You may choose not to see alerts for populations smaller than 25 respondents or score differences smaller than 10 points. Filter the populations by size, using the slider in the Alerts report.

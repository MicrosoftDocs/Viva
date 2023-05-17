---
title: Use the Viva Glint Alerts and Attrition Risk report
description: The Alerts report finds statistically significant patterns, outliers, and deviations from past scores to surface populations or demographic groups that have opportunities for improvement.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: driver impact report
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/28/2023
---

# Use the Viva Glint Alerts and Attrition Risk report

Microsoft Viva Glint's Alerts algorithm finds statistically significant patterns, outliers, and deviations from the scores in survey data and surfaces populations or demographic groups that have:

- Low or high scores
- Notable changes in scores

>[!NOTE]
> Statistically significant/notable insights are gathered using p-value, as well as select thresholds for the minimum population size (defaults to 20 respondents) and the minimum score difference or change (defaults to 8 points) to qualify for an alert. The defaults are configurable at the client level (p-value = 0.05, min N = 20, and delta = 8).

The Alerts report is found on the **Reports** tab of the admin dashboard. Alerts are only visible to admins.

## How is the Alerts report generated?

Populations are defined by the attributes supplied within your Employee Attribute File. The alerts algorithm searches for patterns within single attributes (for example, Team: Sales > Corporate Sales) and combinations of attributes (for example, gender and tenure > 5 years).

If a population or demographic group has scores for items that are different from a comparison point in a statistically significant way, that population is tagged for an alert.

You can configure which demographic attributes are used by the alerts algorithm.

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

### Attrition Model Attrition Risk Index

The Elevated Attrition Risk, part of the Alerts report, is key for providing information about populations that may be at elevated risk for turnover.

#### What is the Attrition Risk Index?

Viva Glint can predict the effect of score differences and overall response profiles of each population for employee attrition. The Attrition Risk Index is a model trained on aggregated turnover data across all Viva Glint clients and can predict elevated risk for voluntary attrition based on scores for standard items.

Populations identified with elevated attrition risk are those that show a higher future attrition rate than your company's average.

Based on extensive cross-validation studies, when using our standard survey questions/items, risk alerts have a precision of at least 80% and in many cases, even higher. If a population is flagged for elevated attrition risk, there is at least an 80% chance that attrition will be elevated.

The model uses Viva Glint standard items in making predictions to allow for the most useful information to be available. The model is structured in a way that recognizes if nonstandard items are used - the use of custom items degrades the model. Outcome items - eSat and Recommend - are immensely powerful and are a proxy for many insights, so a minimal set of items should include at least eSat and Recommend.

>[!TIP]
> Regularly incorporate the Alerts report into your Viva Glint dashboard.

>[!NOTE]
>
> - The Elevated Attrition Risk model was updated in October 2022.
> - If you have worked to implement a custom model, platform alerts remain unchanged.

## Set up the Alerts report

Configure which demographic attributes you want to include in **Alerts** from **General Settings** on the admin dashboard. To configure them initially, or to change them over time:

1. Navigate to **Reporting,** then **Attributes for Alerts.**
2. From the attributes you have sent in your Employee Attribute File, narrow down which you'll see in the Alerts report to those items *most important to attrition risk* within your organization.
    - Use the Search box to add attributes if you're making changes.
    - Delete attributes by choosing the **X** next to those you don't wish to see on the report.
     >[!TIP]
     >  Select only attributes that are necessary for Alerts, such as important hierarchies, tenure, and generation. Avoid attributes with many values that cannot be grouped, such as hire date, birth date and manager email. Using all attributes cannot surface helpful insights.

3. Select thresholds for the minimum population size (default is 20 respondents) and the minimum score differences (default is eight points) that will qualify for an alert. You may choose not to see alerts for populations smaller than 25 respondents or score differences smaller than 10 points. Filter the populations by size using the slider in the Alerts report.

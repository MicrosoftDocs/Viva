---
title: Use the Viva Glint Driver Impact report
description: An engagement driver—a key driver—is a factor that directly correlates to an organization's employees' happiness at work. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: driver impact report, broader team insights, strengths, opportunities, key drivers, graph view, table view, executive summary report
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/08/2024
---

# Use the Viva Glint Driver Impact report

Drivers are factors that affect employee engagement; a driver's *impact* is described as its correlation with employee engagement in the current world of work. Strengths and Opportunities (S&Os) for creating focus areas and action plans are derived from driver impact data.

There can be a significant difference in how important a specific driver of engagement is to one team compared to another team, or to the rest of the company. For example, the engineering team's engagement level may be highly impacted by a lack of career growth opportunities, whereas the finance team may have been overworked this quarter and thus work-life balance impacts them the most. Key drivers vary within organizations and populations.

[Watch this video about using the driver impact report.](https://www.microsoft.com/en-us/videoplayer/embed?partnerName=learn&powerCmsVideoId=RW1dOXU)

## Strengths and Opportunities are derived from the Driver Impact report

The algorithm used to identify S&Os is composed of item scores, impact on engagement, and relativity of the score to a comparison point. This comparison could be internal company scores, an external benchmark, or the score for the average question for that survey.

Strengths are areas that the team should celebrate, and opportunities are areas the team should work on to improve overall engagement (or the key outcome).

[Watch videos for a quick and comprehensive summary of strengths and opportunities and learn more](/viva/glint/reports/act-strengths-opportunities)

To determine a driver's impact, individual survey responses are analyzed to determine how closely aligned scores are for each driver and the outcome variable (typically engagement). A driver's impact is classified as *high* when this is true:

- Employees who rate a driver high, also rate engagement high
- Employees who rate a driver low, also rate engagement low

If a driver's score isn't related to engagement, then it has low or zero impact. Knowing which drivers have a high impact allows managers to focus on improving the scores of drivers that matter the most.

## View the Driver Impact Report

Choose from these formats to view your report:

### Graph view

When a user navigates to the Driver Impact report, the first view is in graph format.

The graph plots each driver's impact on the x-axis and the selected comparison on the y-axis. The comparison can include:

- An internal comparison, such as the overall company
- An external benchmark
- The average question score for the survey

Items on the right side of the graph have a high statistical correlation with the selected outcome (typically engagement or eSat) across all the respondents in a group. Often a person rates a driver and its corresponding outcome the same. For this reason, acting on those items likely has the biggest impact on engagement (or the selected outcome).

In determining strengths and opportunities, the platform considers the distance to the comparison point and the impact on the key outcome. Only items with a **High** or **Very High** impact are considered when determining strengths and opportunities. Of these, the ones relatively highest in relation to the comparison are marked as Strengths, and the ones relatively lowest in relation to the comparison are marked as Opportunities. Based on this analysis, a rank ordered list of items is displayed:

- Relative Strengths are indicated by points with a **bold white dot**.
- Relative Opportunities are indicated by a **red dot**.

> [!NOTE]
> If there are less than two eligible items ranked, the Strengths & Opportunities section is hidden on a user's dashboard. This happens when:
> - There are insufficient results
> - All items have low or medium impact
> - A user is on a report filtered to only one item

### Table view

The Driver Impact table view displays the top three strengths and opportunities, exactly as managers see them on their Strengths & Opportunities report. Selecting  **Show more** displays all strengths and opportunities. Select **Show less** to hide them.

The circle next to each driver's name indicates the impact level and score in relation to the comparison:

- A filled circle indicates the highest impact
- A partially filled circle indicates relatively lower impact
- Blue indicates that the item scored above the comparison
- Red indicates that the item scored below the comparison

 Table view example:

 :::image type="content" source="../../media/glint/reports/driver-impact-example.png" alt-text="Screenshot of a table view of the Driver Impact report.":::

## Settings on the Driver Impact report

The default driver impact report is set at the client level and is either an internal comparison, such as the *Total Company* or an external *Benchmark*. This comparison dictates what appears on the dashboard for all reports, across all programs. Comparison groups can be changed, but the views revert to the default settings upon logging off or changing views.

If you're looking at *Total Company* results *and* the default comparison is *Total Company*, the driver analysis shows *Average Question* as the comparison - otherwise there would be no comparison ratio.

## Apply filters

Applying filters allows admins to look at strengths and opportunities for specific groups. To apply a filter:

1. Select the filter symbol at the top of the page.
2. Select  **+ Add Filters.**
3. From the dropdown menu, choose a filter from the **People** or **Question Responses** section.

Reference **Reports Filtering** for detailed information.

## Strengths & Opportunities on the Executive Summary report

The view on the Executive Summary report provides a ranked list of both strengths (areas to celebrate) and opportunities (areas to focus on) for improvement.

>[!TIP]
> For administrators, the first look at S&O should be versus *Benchmark* to understand which areas can help improve your organization's competitive advantage to attract and retain talent. Only items with a benchmark are part of this view.
>
>If there are multiple items without a benchmark, change to view S&Os versus *Average Question*. This view shows the comparison to the average score of all selected survey items. This comparison indicates a team's strengths and opportunities compared to the *company mean*.
>
>Example:
>
>*If there are 10 rating questions in a survey and the average of all the question scores is 75, then the difference between a question with score 70 versus the question average is calculated as 70 - 75 = -5.*

## View Strengths & Opportunities versus Company

Managers should first look at the Strength & Opportunity report *vs. Company (or other internal comparison, if available, such as Division)*. While Benchmark is a valuable comparison, most often Company is more informative because the comparison is internal.

A manager with scores *below* company average should focus on the items with the biggest gaps as those reflect the greatest opportunity for improvement. For this reason, the **Take Action** button defaults to the Opportunities section of the S&O report.

Managers with scores *above* Company can change to view S&O vs. Benchmark to gain a sense of what areas may help to close gaps.

## Small teams can use the Driver Impact report

The algorithm used to determine driver impact scores includes a statistical test to determine if it has enough data points to establish a significant correlation. 

**A minimum number of 20 respondents is the default threshold to determine whether to show impact scores for a team.** Managers of teams that don't meet the minimum number of respondents see their S&Os based on the impact calculated at the *Company level*. This method provides the most statistically sound results.

Key points for managers with fewer than 20 respondents:

- S&Os on the dashboard are the areas a manager's team scored relatively high or low in relation to the comparison. These areas have the strongest impact on engagement at the larger company level; they impact isn't reflective of your team specifically. The dashboard doesn't show impact scores at the team level if there are fewer than 20 respondents.
- One manager's S&Os may be different from other leaders within their organization.
- If enabled, including [Broader Team Insights (BTI)](/viva/glint/reports/broader-team-insights into conversations provides understanding for what drives engagement closer to the manager's own level in their organization.


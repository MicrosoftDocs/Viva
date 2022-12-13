---
title: Organization insights FAQs
description: Get answers to frequently asked questions about organization insights in Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Organization insights FAQs

## Q1 – Can I opt in or opt out of seeing organization insights?

To opt out or back into seeing organizational insights, your Viva Insights administrator needs to unassign or reassign you the group manager role. They can assign you this role by following the directions in [Manager settings](../../advanced/setup-maint/manager-settings.md).

<!--Diego to verify?-->

## Q2 – Why don’t I see cards showing peer comparison in my organization insights?

To show you peer organization comparisons, Viva Insights looks for people who don’t report up to you, but do report up to your manager or skip-level manager. Viva Insights also checks the size of the peer organization group against the minimum group size to protect individual privacy. If you aren't seeing a peer comparison in your organization insights, it’s because not enough people meet the definition for a peer organization.

If you're looking at the Insights business leader view and seeing results for everyone in the company, peer comparison insights won't appear; no one's left in the measured population to compare against.

<!--Is the IBL view controlled through the dropdown menu at the top right of the org insights card?-->


## Q3 – There are data points missing from my trendline visuals. Why?

To protect individual privacy when a group average appears in an organizational insight, Viva Insights checks to make sure the group is larger than the minimum group size.   

The measured group only counts people who are active in Outlook or Teams during the week, so the group size might be lower some weeks than others. For example, the group size is more likely to decrease during the holidays. That means that you might see a result for a particular group for one week, but not for a different week when the group size has gone below the minimum. As a result, you might sometimes see broken or incomplete trendlines.

## Q4 – I don’t see all of the teams reporting to me in my organization breakdown visual. Why?

To protect individual privacy when a group average appears in an organizational insight, Viva Insights checks to make sure the number of measured people active in Outlook and Teams is larger than the minimum group size. We won't show any groups smaller than the minimum group size.

Additionally, if you have more than six groups larger than the minimum group size that report to you, all other people in your organization will be grouped together in a single “everyone else” group. If this "everyone else" group is smaller than the minimum group size, Viva Insights won't show it. 

## Q5 – Why doesn’t the trendline chart show the most recent week of data?

Viva Insights aggregates new data every week. Usually, the most recent week of data in a trendline is labeled with the first day of the last complete week. For example, if someone viewed their data on Wednesday, October 5, 2022, they'd see the most recent week of data labeled September 25, 2022. This data represents activity between September 25 and October 1.

If the most recent week of data in the trendline is labeled earlier than the first day of the last complete week, it might be because:

* The group size has fallen below the minimum in the most recent week.
* If it’s a Monday, processing and aggregation of the new data may have been slightly delayed.

## Q6 – What happens if I have fewer people reporting to me than I used to?

If you're no longer a people manager and have no one directly or indirectly reporting to you, you won't be able to access organization insights.

To be able to access organization trends, you need to have a certain number of direct and indirect reports in the most recent week of available data. This number needs to be above the minimum that your administrator set. 

Here's what this means:

If your *total* number of direct and indirect reports falls below this set minimum, organization insights won't be available to you. If this number seems like an error, your Insights administrator can validate your group against the organization hierarchy.

Viva Insights bases your eligibility to view organization insights on the *total* size of your group, not just the number of employees in your group actively using Outlook and Teams. If the number of your direct and indirect reports who actively use  Outlook and Teams falls below the minimum in the most recent week, you'll still be able to access organization insights. The insights will just show data for the last period when your active group size was above the minimum. You won’t see insights for the week when the active group size was below the minimum. 

## Q7 – What is the employee experience Power BI report and how can I get it?

Microsoft Power BI provides greater flexibility to explore your organization insights. For more insights, filters, and grouping options, you can download the employee experience Power BI report. To find this report, open an organization insight page. You can find these pages by selecting **Explore more** <!--Show details?--> on any organization insight card. The link to the employee experience Power BI report is in the **Related insights** section of each organization insight page. 

This report automatically draws in data for your organization. You'll only see results for your own direct and indirect reports, and it includes the same protections for individual privacy (like minimum group size and differential privacy) as the organization insights in the Viva Insights app in Teams and on the web.

<!--does this open in PBI? Not able to replicate these instructions in my PPE tenant.-->

## Q8 – How do I share my insights with others?

Before sharing your organization insights with others, consider first whether you would be sharing any sensitive information. If you do want to share your insights, you have two options:

1. Select the share icon from any insight to open a chat with a screenshot of that card.
1. Select the **Download as PowerPoint** link from the **Related insights** section of an organization insights page. This option creates a PowerPoint document with all the visuals and insights from all of the organization insights available to you in the Viva Insights Teams app.

<!--Not able to replicate these instructions in my PPE tenant.-->


## Q9 – Can I send feedback about these features?

We would love to hear from you! To send feedback, select the **Is this helpful?** link at the bottom of any page.









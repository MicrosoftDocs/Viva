---
ROBOTS: NOINDEX,NOFOLLOW
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

## Q1. Can I opt in or opt out of seeing organization insights?

To opt out or back into seeing organizational insights, your Viva Insights administrator needs to enable or disable group manager permissions for you. They can enable these permissions by following the directions in [Manager settings](../../advanced/setup-maint/manager-settings.md).

## Q2. I see my organization insights cards, but the current week values are just “—“. What’s happening?

Viva Insights only reports on activity for employees who are “active” in a week—that is, people who sent at least one message in Outlook or Teams or joined at least one meeting. This method improves accuracy by leaving out people who are away from work for an extended period, like when they're on vacation or taking a leave of absence.

To protect individual privacy, you'll only see organization insights when the number of active group members meets the minimum group size your Insights admin set. Some groups might have a group size close to the minimum. In these cases, if enough people are away from work and the number of active people dips below the minimum, you won't be able to access organization insights for that week. However, you can still refer to trend charts on the **Wellbeing**, **Productivity**, and **Teamwork** tabs. These charts show results for previous weeks when your active group met the minimum privacy threshold. 

## Q3. How do organization insights handle holiday weeks?

Generally, organization insights show lower activity during weeks with holidays, as the measured results aren't adjusted to make up for the holiday. If an employee takes the entire week off from work during the holiday week, they'll be excluded from the measured result. For employees who don't take the week off, Viva Insights measures the activity that *did* occur over the course of the week.

As discussed in Q2, you might not see results during holiday weeks if enough of your group takes the week off from work and the active group size falls below the minimum privacy threshold.


## Q4. Why don’t I see cards showing peer comparison in my organization insights?

To show you peer organization comparisons, Viva Insights looks for people who don’t report up to you, but do report up to your manager or skip-level manager. Viva Insights also checks the size of the peer organization group against the minimum group size to protect individual privacy. If you aren't seeing a peer comparison in your organization insights, it’s because not enough people meet the definition for a peer organization.

If you're in the **Your company** view, peer comparison insights won't appear; no one's left in the measured population to compare against.

## Q5. There are data points missing from my trendline visuals. Why?

To protect individual privacy when a group average appears in an organizational insight, Viva Insights checks to make sure the group is larger than the minimum group size.

The measured group only counts people who are active in Outlook or Teams during the week, so the group size might be lower some weeks than others. For example, the group size is more likely to decrease during the holidays. That means that you might see a result for a particular group for one week, but not for a different week when the group size has gone below the minimum. As a result, you might sometimes see broken or incomplete trendlines.

## Q6. I don’t see all of the teams reporting to me in my organization breakdown visual. Why?

To protect individual privacy when a group average appears in an organizational insight, Viva Insights checks to make sure the number of measured people active in Outlook and Teams is larger than the minimum group size. We won't show any groups smaller than the minimum group size.

Additionally, if you have more than six groups larger than the minimum group size that report to you, all other people in your organization will be grouped together in a single “everyone else” group. If this "everyone else" group is smaller than the minimum group size, Viva Insights won't show it. 

## Q7. Why doesn’t the trendline chart show the most recent week of data?

Viva Insights aggregates new data every week. Usually, the most recent week of data in a trendline is labeled with the first day of the last complete week. For example, if someone viewed their data on Wednesday, October 5, 2022, they'd see the most recent week of data labeled September 25, 2022. This data represents activity between September 25 and October 1.

If the most recent week of data in the trendline is labeled earlier than the first day of the last complete week, it might be because:

* The group size has fallen below the minimum in the most recent week.
* If it’s a Monday, processing and aggregation of the new data may have been slightly delayed.

## Q8. What happens if I have fewer people reporting to me than I used to?

If you're no longer a people manager and have no one directly or indirectly reporting to you, you won't be able to access organization insights.

To be able to access organization trends, you need to have a certain number of direct and indirect reports in the most recent week of available data. This number needs to be above the minimum that your administrator set. 

Here's what this means:

If your *total* number of direct and indirect reports falls below this set minimum, organization insights won't be available to you. If this number seems like an error, your Insights administrator can validate your group against the organization hierarchy.

Viva Insights bases your eligibility to view organization insights on the *total* size of your group, not just the number of employees in your group actively using Outlook and Teams. If the number of your direct and indirect reports who actively use  Outlook and Teams falls below the minimum in the most recent week, you'll still be able to access organization insights. The insights will just show data for the last period when your active group size was above the minimum. You won’t see insights for the week when the active group size was below the minimum. If the number of your direct and indirect reports who actively use Outlook and Teams falls below the minimum in the most recent week, you'll still be able to access organization insights. You won’t see insights for weeks when the active group size falls below the minimum.

## Q9. How do I share my insights with others?

Before sharing your organization insights with others, consider first whether you would be sharing any sensitive information. If you do want to share your insights, select the share icon on any insight. Then, you can either share through a chat or a link. Refer to [Organization insights](org-insights.md#using-organization-insights) for more information on sharing.


## Q10. Can I send feedback about these features?

We would love to hear from you! To send feedback, select the **Is this helpful?** link at the bottom of any page.

## Related topics

[Organization insights](org-insights.md)
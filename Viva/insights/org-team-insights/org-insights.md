---
ms.date: 09/30/2024
title: Organization insights in the Viva Insights app
description: Find Organization insights in Microsoft Viva Insights 
author: zachminers
ms.author: v-zachminers
ms.topic: concept-article
ms.collection: 
- viva-insights-personal
- essentials-manage
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anirudhbajaj
audience: user
---

# Organization insights in Viva Insights

Organization insights help leaders and managers build high performing teams. Leaders and managers can see key indicators of their organization’s wellbeing, productivity, and team culture, and they can find features and tools to help support their teams.

## Subscriptions, roles, and access

To view organization insights:

* You need to have a Viva Insights subscription (that is, a premium license).
* To view organization insights for your team (direct and indirect reports), your Insights admin needs to assign you the [Group Manager](../advanced/setup-maint/manager-settings.md#configure-manager-settings) role in Viva Insights. And, you need to have a number of direct and indirect reports that meets or exceeds the [minimum group size](../advanced/setup-maint/privacy-settings.md#minimum-group-size) your Insights admin set.
* To view organization insights for the entire company, your Insights admin needs to assign you the [**Insights Business Leader** role](../advanced/setup-maint/assign-user-roles.md).
* You can also view organization insights if you're given "delegate access" by a group manager. [See how delegate access works](./delegate-access.md).

People in your organization also need to have a Viva Insights subscription so they can be measured in organizational insights. These employees are referred to as "measured employees." If you want to see an insight that reflects your entire company, everyone in the company needs to have a Viva Insights subscription.

>[!Important]
>Early next year, the **Business Leader** role will no longer be available. At that point, people who previously had this role won’t be able to access organizational insights. Employees with delegate access, however, will be able to view organizational insights. [Learn more about how delegate access works](..//org-team-insights/delegate-access.md).

### Insights by role

People with the **Insights Business Leader** role assigned to them can access organization insights that include every measured employee in their tenant. 

People enabled as Group Managers can access organization insights that include people who report to them directly or indirectly. Your Insights admin maintains this reporting hierarchy. If your admin assigned you the Insights Business Leader role and also enabled you as a Group Manager, you can toggle between the two organization insights views.

## Data and privacy

Viva Insights commits that no user will discover information about another identified individual that they couldn't already know. This principle applies to every feature in Viva Insights, including organization insights.

For further detail about privacy and organization insights, refer to our [privacy information](../advanced/privacy/privacy.md).

## Using organization insights

>[!Note]
>If a group manager gives you delegate access to view organization insights, you can’t see the manager’s personal insights.

Organization insights are divided into two sections: **Team insights**, which are focused on your organization and teams; and **Your insights**, which are focused on your own personal working habits and productivity. Let’s start with looking at **Team insights**.

### Team insights

#### The Home tab

Organization insights are more than just a dashboard—they also provide helpful features to share insights and actions with your organization. Here's what you might see in the Home tab when you open your Viva Insights app:

:::image type="complex" source="images/org-insights-home-tab.png" alt-text="Screenshot that shows the organization insights Home tab." lightbox="images/org-insights-home-tab.png":::
   Screenshot of the "Your organization insights" Home tab in the Viva Insights app.
:::image-end:::

In the Home tab, you’ll find cards for reports covering different types of trends across the groups you manage, such as new hire onboarding and external focus. Each of these cards corresponds to a broader report, which you can explore further by selecting it from the list on the left. Or you can select the card itself to dive deeper.

[Learn more about these reports for leaders](./leader-reports.md).

#### The Library tab

The Library tab, meanwhile, provides a snapshot view of various other metrics related to team collaboration, such as collaboration time and uninterrupted focus hours. In the Library tab, you can also filter these insights based on specific teams and time periods.

:::image type="complex" source="images/leader-homepage-new-library.png" alt-text="Screenshot that shows the organization insights Library tab." lightbox="images/leader-homepage-new-library.png":::
   Screenshot of the "Your organization insights" Library tab in the Viva Insights app.
:::image-end:::

Let's take a look at how to use these features:

1. **Scope information**

     At the top-left, an indicator shows how many people the insights are measuring.

    The measured group reflects people who:

    * Are in your reporting hierarchy, based on the organizational structure that your Insights admin maintains.
    * Have a Viva Insights subscription (that is, a premium license) applied to their account.
    * Employees were active in Outlook or Teams during the past 12 weeks.

    People need to meet *all* of these criteria to be part of the measured group reflected here—that is, your scope.

    **If you're enabled as a Group Manager:** On the left, select the dropdown menu to toggle between viewing insights for your organization, or different subgroups within your team. Teams with less than the minimum team size will be colored gray and their insights won't be visible.

    :::image type="complex" source="images/org-insights-scope-group-manager.png" alt-text="Screenshot that shows the organization insights drilldown for group managers." lightbox="images/org-insights-scope-group-manager.png":::
   Screenshot of the "Your organization insights" drilldown section for group managers.
    :::image-end:::

    **If you have the Insights Business Leader role assigned:** You can view insights only for your entire company.

    :::image type="complex" source="images/org-insights-scope-biz-leader.png" alt-text="Screenshot that shows the organization insights drilldown for Insights Business Leaders." lightbox="images/org-insights-scope-biz-leader.png":::
   Screenshot of the "Your organization insights" drilldown section for Insights Business Leaders.
    :::image-end:::

    **If you're enabled as a Group Manager *and* you're an Insights Business Leader:** You can use the toggle to view insights either for your team and subgroups, or for the entire company.

1. **Time filter**

    Each report provides insights related to the previous four-week period. You can’t change this filter.

     :::image type="complex" source="images/org-insights-time-period-filter.png" alt-text="Screenshot that shows the organization insights time filter." lightbox="images/org-insights-time-period-filter.png":::
   Screenshot of the "Your organization insights" time filter.
    :::image-end:::

1. **Details**

   Select **View report** on the card to dive deeper into the measured results. When you select the card, Viva Insights brings you to the insight drill-down page. This page contains information like trend lines, details for individual groups, and related metrics.

1. **Three-dot menu for sharing** 

    Sharing is available for most insight cards. You can share an insight in one of two ways:
    
    * **As an image** - Select the three dots at the bottom right, then select **Copy as image**. You’ll see a preview of a screenshot of the insight. Select **Copy image to clipboard**. You can then paste and share the image with anyone, anywhere you want, such as in an email message or on Teams.

    :::image type="complex" source="images/sharing-copyimage-01.png" alt-text="Screenshot that shows how to share an insight as an image.":::
    Screenshot that shows how to share an insight as an image.
    :::image-end:::

    * **In a Teams chat** – Select the three dots at the bottom right, then select **Share via Teams**. When you share through a chat, you'll have the option to add a custom message. You'll share the insight as a screenshot.
    
        :::image type="complex" source="images/sharing-teamschat.png" alt-text="Screenshot that shows sharing an insight via Teams.":::
           Screenshot that shows sharing an insight via Teams.
        :::image-end:::

#### Insight drill-down page

If you want to dive deeper into an insight, select the insight card. You'll arrive at a report page, which gives you more information about the metric that your insight's based on.

Here's what you can do on each report page:

##### Past four weeks at a glance

See how activities related to your select metric compare to the previous four weeks.

##### Trend graph 

Learn how your selected metric averages have changed over time. View a four-month distribution of averages for:

* Your whole organization (that is, your company).
* Groups within your organization (that is, different reporting hierarchies within your company). Use the icons below the graph to toggle individual groups on or off.

To protect individual privacy, we don't show organizational insights if your organization is smaller than the minimum group size.

##### Weekly averages by group

Depending on the metric, view an average count, hours, rate, or size here for groups within your organization. For example, if you were viewing information about uninterrupted focus hours, you'd see how many hours on average each group in your organization kept for focus time without interruptions every week.

This number includes everyone in your reporting hierarchy or your company, depending on how your [scope toggle](#using-organization-insights) is set. 

##### Related metrics

Browse insights about other metrics related to the one you're viewing on this page. If you're viewing **Long and large meeting hours**, you might find **Join on time rate**, **Multitasking hours**, or **Recurring meeting hours** here. Use the arrows in this section's top-right to scroll through all related insights.

## Related information

### Helpful terms

* <a name="current-period-define"></a> **Current period** – Unless otherwise stated, most insights are showing the result for the most recent period—that usually means the most recent complete week of data. A few insights use a four-week or rolling four-week window instead, to smooth normal variability and make it easier to understand the insight. If an insight uses something other than the most recent week for the current period, you will see it called out on the insight card. 
* <a name="employees-define"></a> **Employees** – Organization insights provide measures for groups of employees, and are meant to capture what typical workday activity looks like for those employees. To avoid skewing the averages by including people who are not at work during the week (for example, they are on holiday or out sick), organization insights only measure people who have some activity in Outlook or Teams during the week.
* <a name="organization-breakdown-define"></a> **Organization breakdown** – The groups displayed in the organization breakdown are based on your reporting hierarchy, which your Insights admin [maintains](../advanced/setup-maint/upload-data.md). Each group includes people who report directly or indirectly to a person who reports to you. The insights represent the activity of the group, not just that person who reports to you, even though their name is used to label the group. 

    Insight Business Leaders who are viewing the insights for the entire company will see the organization breakdown by organizations reporting to top-layer leaders.
* <a name="peer-organization-define"></a>**Peer organization** – Peer organization includes groups near your own group in the reporting hierarchy. If available, the peer organization includes people who report directly or indirectly up to your manager, but not up to you. If there aren't any groups like this, or they don’t meet the minimum group size, the peer organization includes people who report directly or indirectly up to your skip-level manager but not up to you. If there’s not enough people who meet that definition either, you won't see peer organization insights. 

    Insights Business Leaders who are viewing insights for the entire company will also not see peer organization insights.
* <a name="prior-period-define"></a>**Prior period** – The prior period is the period immediately before the most recent period – usually the week before the most recent completed week. 
* <a name="reporting-hierarchy-define"></a>**Reporting hierarchy** – Your Insights administrator manages the reporting hierarchy. This hierarchy identifies reporting relationships throughout the company: people who are managers, and the people who report to them. The reporting hierarchy might be sourced from Microsoft Entra ID or from a manual upload from your company’s HR information system. Viva Insights uses this information to identify people in your organization, your peer organization, and any organizations that might report up to you.
* <a name="your-organization-define"></a>**Your organization** – If the insight scope selector says **Your organization**, this group includes everyone who reports to you directly or indirectly. This group is based on your organization’s reporting hierarchy, your Insights administrator manages. If the insights scope selector says **[Your company name]**, this group includes everyone who has been set up as part of the premium insights group by your Insights administrator.


### Control access to Insights features

*Applies to: Insights administrators*

To control access to certain Insights features, like the [Meeting Cost and Quality](https://support.microsoft.com/topic/meeting-review-card-d484f75f-ff64-4be5-86a8-597a4eebead7) features, Insights administrators can use the [Viva feature access management platform](/viva/feature-access-management). This platform provides a flexible approach to deployment by letting you enable or disable individual premium features through multiple access policies for the tenant, users, and groups. 

Policy settings apply any time a user signs in, allowing the user access to all enabled features. Because you can set multiple access policies -- targeting the tenant, groups, and individual users -- a user might be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. For instructions, see [Control access to features in Viva](/viva/feature-access-management).

| Insights feature | State | Description |
|----|----|----|
|Meeting cost and quality | Enabled | When this feature is enabled, leaders can see the Meeting Cost and Quality report in the Insights app, and individual users can see the [meeting review card](https://support.microsoft.com/topic/meeting-review-card-d484f75f-ff64-4be5-86a8-597a4eebead7) and Outlook nudges with insights about the cost and quality of their large and long meetings. |
|   | Disabled | These features are not available to the Insights user. |


## Metric definitions

Refer to [Metric definitions](../advanced/reference/metrics.md) for all Viva Insights metric definitions. You can also access metric definitions while you're using Viva Insights—just select the (i) icon next to the organization insight card or organization insight page title.

## FAQs

###### Q1. Can I opt in or opt out of seeing organization insights?

To opt out or back into seeing organizational insights, your Viva Insights administrator needs to enable or disable group manager permissions for you. They can enable these permissions by following the directions in [Manager settings](../advanced/setup-maint/manager-settings.md).

###### Q2. How do I get access to organization insights?

Refer to Subscriptions, roles, and access in [Organization insights](org-insights.md#subscriptions-roles-and-access).

###### Q3. I see my organization insights cards, but the current week values are just “—“. What’s happening?

Viva Insights only reports on activity for employees who are “active” in a week—that is, people who sent at least one message in Outlook or Teams or joined at least one meeting. This method improves accuracy by leaving out people who are away from work for an extended period, like when they're on vacation or taking a leave of absence.

To protect individual privacy, you'll only see organization insights when the number of active group members meets the minimum group size your Insights admin set. Some groups might have a group size close to the minimum. In these cases, if enough people are away from work and the number of active people dips below the minimum, you won't be able to access organization insights for that week. However, you can still refer to trend charts on the **Wellbeing**, **Productivity**, and **Teamwork** tabs. These charts show results for previous weeks when your active group met the minimum privacy threshold. 

###### Q4. How do organization insights handle holiday weeks?

Generally, organization insights show lower activity during weeks with holidays, as the measured results aren't adjusted to make up for the holiday. If an employee takes the entire week off from work during the holiday week, they'll be excluded from the measured result. For employees who don't take the week off, Viva Insights measures the activity that *did* occur over the course of the week.

As discussed in Q2, you might not see results during holiday weeks if enough of your group takes the week off from work and the active group size falls below the minimum privacy threshold.


###### Q5. Why don’t I see cards showing peer comparison in my organization insights?

To show you peer organization comparisons, Viva Insights looks for people who don’t report up to you, but do report up to your manager or skip-level manager. Viva Insights also checks the size of the peer organization group against the minimum group size to protect individual privacy. If you aren't seeing a peer comparison in your organization insights, it’s because not enough people meet the definition for a peer organization.

If you're in the **Your company** view, peer comparison insights won't appear; no one's left in the measured population to compare against.

###### Q6. There are data points missing from my trendline visuals. Why?

To protect individual privacy when a group average appears in an organizational insight, Viva Insights checks to make sure the group is larger than the minimum group size.

The measured group only counts people who are active in Outlook or Teams during the week, so the group size might be lower some weeks than others. For example, the group size is more likely to decrease during the holidays. That means that you might see a result for a particular group for one week, but not for a different week when the group size has gone below the minimum. As a result, you might sometimes see broken or incomplete trendlines.

###### Q7. I don’t see all of the teams reporting to me in my organization breakdown visual. Why?

To protect individual privacy when a group average appears in an organizational insight, Viva Insights checks to make sure the number of measured people active in Outlook and Teams is larger than the minimum group size. We won't show any groups smaller than the minimum group size.

The [trend graph](org-insights.md#trend-graph) can show up to 20 groups that report up to you. You'll see organization insights for each group larger than the minimum group size.

###### Q8. Why doesn’t the trendline chart show the most recent week of data?

Viva Insights aggregates new data every week. Usually, the most recent week of data in a trendline is labeled with the first day of the last complete week. For example, if someone viewed their data on Wednesday, October 5, 2022, they'd see the most recent week of data labeled September 25, 2022. This data represents activity between September 25 and October 1.

If the most recent week of data in the trendline is labeled earlier than the first day of the last complete week, it might be because:

* The group size has fallen below the minimum in the most recent week.
* If it’s early in the week, processing and aggregation of the new data may have been slightly delayed.

###### Q9. What happens if I have fewer people reporting to me than I used to?

If you're no longer a people manager and have no one directly or indirectly reporting to you, you won't be able to access organization insights.

To be able to access organization trends, you need to have a certain number of direct and indirect reports in the most recent week of available data. This number needs to be above the minimum that your administrator set. 

Here's what this means:

If your *total* number of direct and indirect reports falls below this set minimum, organization insights won't be available to you. If this number seems like an error, your Insights administrator can validate your group against the organization hierarchy.

Viva Insights bases your eligibility to view organization insights on the *total* size of your group, not just the number of employees in your group actively using Outlook and Teams. If the number of your direct and indirect reports who actively use  Outlook and Teams falls below the minimum in the most recent week, you'll still be able to access organization insights. The insights will just show data for the last period when your active group size was above the minimum. You won’t see insights for the week when the active group size was below the minimum. If the number of your direct and indirect reports who actively use Outlook and Teams falls below the minimum in the most recent week, you'll still be able to access organization insights. You won’t see insights for weeks when the active group size falls below the minimum.

###### Q10. Can I send feedback about these features?

We would love to hear from you! To send feedback, select the **Is this helpful?** link at the bottom of any page.

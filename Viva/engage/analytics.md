---
title: "View and manage analytics in Viva Engage"
description: "Viva Engage analytics lets user monitor their engagement metrics and leaders monitor engagement across the organization."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 6/18/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---


# View and manage analytics in Viva Engage

Advanced analytics capabilities in Viva Engage enable the following scenarios:

- Users can monitor their own engagement metrics through _personal_ and _Answers analytics_
- Leaders and their delegates can monitor engagement for their audiences through _audience analytics_
- Corporate communicators and campaign coorganizers can manage campaign engagement through _campaign analytics_
- Knowledge admins can monitor Answer engagement through global _Answers analytics_
- Network admins and corporate communicators can track organization-wide engagement through _network analytics_

Analytics features are available in [all languages that Viva Engage supports](https://support.microsoft.com/en-us/office/which-languages-is-viva-engage-available-in-14dd5886-d48d-4d6d-a583-4273a2538540).

## View analytics

>[!NOTE]
>To view premium analytics features, users must have Viva Engage Premium which is bundled with the _Viva Suite_ and _Employee Communications and Communities_ license. Conversation, live event, and some community analytics are available without a premium license. Audience analytics are only viewable by leaders that have at least one primary assigned audience and their delegates.

- To open analytics, select the analytics icon on the top navigation bar in Viva Engage.

Most analytics data is refreshed every 24 hours. Conversation and community analytics update in near real time. If you don’t see changes reflected immediately, check back the next day.

## Manage analytics

Only users assigned the Network admin role can turn analytics features on or off. To enable or disable metrics from the **Manage analytics** interface of the Viva Engage admin center, follow these steps.

1. From [Viva Engage on the web](https://engage.cloud.microsoft/main/admin), go to the gear icon in the top navigation menu and select **Admin center**. From the Viva Engage Teams app, select the ellipses button from the top navigation menu, and then select **Admin**.

    :::image type="content" source="../media/engage/admin/web-admin-entry.png" alt-text="Screenshot shows the entry point to the Viva Engage admin center on the web at engage.cloud.microsoft/main/admin." lightbox="../media/engage/admin/web-admin-entry.png":::

2. Select the **Setup & configuration** tab, and select **Manage analytics**.

   [![Screenshot of the Viva Engage admin center for managing Analytics.](/Viva/media/engage/admin/manage-analytics-eac.png)](/Viva/media/engage/admin/manage-analytics-eac.png#lightbox)

3. From the **Analytics settings** page, network admins can select the **Feature access management** link to implement AI-related features, like sentiment analysis and theme extraction in Microsoft 365. See the next section for details.

   [![Screenshot of settings to manage Analytics.](/Viva/media/engage/admin/analytics-admin-settings.png)](/Viva/media/engage/admin/analytics-admin-settings.png#lightbox)


## Manage AI Summarization in Microsoft 365

When the AI Summarization service is enabled, it processes Viva Engage threads in the background to provide a richer data experience for Network analytics. AI Summarization data is used for network theme extraction, conversation summarization, and network sentiment analysis.

Engage admins can manage AI Summarization for their network through Viva Feature access management in the Microsoft 365 admin center. Feature access management offers a more flexible approach to deployment by allowing admins to enable or disable this service for specific users and groups in the tenant. To learn more, see [Viva Feature access management](/viva/feature-access-management) and [AI Summarization enablement states](/viva/engage/engage-ai-summarization).

## Network analytics

>[!NOTE] 
>For the **Network analytics** dashboard to be available, at least 50% of the network’s users must be licensed for _Viva Suite_ or _Employee Communications and Communities_.

Network analytics provide valuable insights into employee engagement and communication across your organization through sentiment, retention, and community activity data. Data insights help Network admins and corporate communicators make more informed decisions toward improving the health of their network.

*Employee retention* shows the difference in the 28-day employee retention rates of employees who do and don't use Viva Engage. For details, see [Employee retention](/viva/engage/employee-retention-metric).

:::image type="content" source="../media/engage/admin/engage-network-analytics.png" alt-text="Screenshot of the Viva Engage admin center for viewing and managing Network analytics." lightbox="../media/engage/admin/engage-network-analytics.png":::

Learn more about metrics featured in the Network analytics dashboard on the [Viva Engage blog](https://techcommunity.microsoft.com/t5/viva-engage-blog/network-analytics-available-now-in-viva-engage/ba-p/4030771).

## Audience analytics  

>[!NOTE]
>Audience analytics are only viewable by leaders who have at least one primary assigned audience (minumum audience size of 5) and their delegates.

In the **Manage analytics** interface shown earlier, the Engage admin can adjust the level of sentiment analysis that's available to leaders and their delegates through the **Audience analytics** dashboard. This functionality enables unique levels of sentiment collection at the audience, theme, or conversation level.

Access is through the analytics icon on the top navigation bar or on the leader's storyline page.

[![Screenshot of the Audience analytics landing page.](/Viva/media/engage/admin/audience-analytics.png)](/Viva/media/engage/admin/audience-analytics.png#lightbox)

*Audience analytics* help leaders and delegates monitor engagement of their audiences on Viva Engage. This dashboard surfaces the most actively engaged communities within their audiences that have at least 50 members and one active member. An _active community_ has reactions and replies from at least 5% of its membership. An _idle community_ has reactions and replies from less than 5% of its membership.

*Sentiment analysis* uses Azure Cognitive Services (ACS) to aggregate and analyze posts, while *themes analysis* draws from LLM (large language model), storyline comments, and public posts. Posts and comments from private communities are included in the aggregate only if the leader is a member and has permission to view them. Individual messages are never shown. Learn more about [Sentiment analysis in Viva Engage](https://support.microsoft.com/en-us/topic/sentiment-and-theme-analysis-in-viva-engage-065c3355-d156-4bf8-afdb-663b0724befd).

- **Audience-level sentiment** controls the *Sentiment* metric. When this toggle is turned off, leaders and their delegates have no access to sentiment analysis features and past data for all audiences is deleted.

- **Theme-level sentiment** controls the *Themes* metric. When this toggle is turned off, leaders and their delegates won’t see results indicating sentiment toward frequently discussed subjects in their audience.

## Global Answers analytics

Engage admins who have the knowledge license can manage metrics for **Answers** in their organization.

[![Screenshot of Global Answers analytics landing page.](/Viva/media/engage/admin/global-answers-analytics.png)](/Viva/media/engage/admin/global-answers-analytics.png#lightbox)

In the **Manage analytics** interface of the Viva Engage admin center, admin can enable or disable advanced metrics such as **time saved** and **people helped**.  

Learn more about the metrics available for [Global Answers analytics and Answers-specific actions for admins](/Viva/engage/eac-answers-admin-scenarios).

## Personal analytics  

All licensed users have access to personal analytics that help monitor the engagement on any of their storylines or community posts in Viva Engage.

[![Screenshot of the Personal analytics landing page.](/Viva/media/engage/admin/personal-analytics-admin.png)](/Viva/media/engage/admin/personal-analytics-admin.png#lightbox)

## Campaign analytics  

Engage admins and corporate communicators have access to analytics to monitor campaign engagement to improve future campaigns. You can access campaign analytics from the **Campaign management** dashboard, the campaign landing page, or the analytics icon on the main navigation menu of Viva Engage.

[![Screenshot of the Campaign analytics landing page.](/Viva/media/engage/admin/campaign-analytics.png)](/Viva/media/engage/admin/campaign-analytics.png#lightbox)

In the **Manage analytics** interface, the Engage admin can enable or disable the top content creator feature for the organization. This feature displays employees and leaders who create the most campaign posts.

## See also

[Monitor engagement in Viva Engage with analytics](https://support.microsoft.com/en-us/office/view-insights-about-questions-and-answers-in-viva-engage-fcde33cf-ee3f-4cc8-aa47-c6d0f3fc5dc0?storagetype=live)

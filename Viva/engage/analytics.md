---
title: "View and manage analytics in Viva Engage"
description: "Viva Engage analytics lets user monitor their engagement metrics and leaders monitor audience engagement (audience analytics), campaign engagement, and monitor engagement in Answers."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 10/16/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---


# View and manage analytics in Viva Engage

Advanced analytics capabilities in Viva Engage enable:
- Users to monitor their own engagement metrics through _personal_ and _Answers analytics_
- Leaders and their delegates to monitor their audiences' engagement through _audience analytics_
- Corporate communicators and campaign co-organizers to manage campaign engagement through _campaign analytics_
- Knowledge admins to monitor engagement in Answers through global _Answers analytics_
- Network admins and corporate communicators to monitor organization-wide engagement through _network analytics_

## Access analytics

>[!NOTE]
>To view analytics, users must have Viva Engage Premium which is bundled with the _Viva Suite_ and _Employee Communications and Communities_ license. Audience analytics are only viewable by leaders that have at least one primary assigned audience and their delegates.

- To open analytics, select the analytics icon on the top navigation bar in Viva Engage.

Analytics data is refreshed every 24 hours. If you don’t see changes reflected immediately, check back the next day.

## Manage analytics

Only users assigned the Network admin role can turn analytics features on or off.  

Enable or disable metrics from the **Manage analytics** interface of the Viva Engage admin center:

1. From [Viva Engage on the web](https://engage.cloud.microsoft/main/admin), go to the gear icon in the top navigation menu and select **Admin center**. From the Viva Engage Teams app, select the ellipses button from the top navigation menu, and then select **Admin**.

    :::image type="content" source="../media/engage/admin/web-admin-entry.png" alt-text="Screenshot shows the entry point to the Viva Engage admin center on the web at engage.cloud.microsoft/main/admin.":::

1. Select the **Setup & configuration** tab, and select **Manage analytics**.

    [![Screenshot of the Viva Engage admin center for managing Analytics.](/Viva/media/engage/admin/manage-analytics-eac.png)](/Viva/media/engage/admin/manage-analytics-eac.png#lightbox)

    [![Screenshot of settings to manage Analytics.](/Viva/media/engage/admin/analytics-admin-settings.png)](/Viva/media/engage/admin/analytics-admin-settings.png#lightbox)

## Network analytics

>[!NOTE] 
>For the **Network analytics** dashboard to be available, at least 50% of the network’s users must be licensed for Viva Suite or Employee Communications and Communities.

Network analytics provide valuable insights into employee engagement and communication across your organization. With the ability to track sentiment, retention, and community activity, network admins and corporate communicators can make informed decisions and take targeted actions to improve the overall health of their network.

**Employee retention** shows the difference in the 28-day employee retention rates of employees who do and don't use Viva Engage. For details, see [Employee Retention](/purview/retention-policies-viva-engage) and [Sentiment and theme analysis in Viva Engage](https://support.microsoft.com/en-us/topic/sentiment-and-theme-analysis-in-viva-engage-065c3355-d156-4bf8-afdb-663b0724befd).

:::image type="content" source="../media/engage/admin/engage-network-analytics.png" alt-text="Screenshot of the Viva Engage admin center for viewing and managing Network analytics.":::

Learn more about metrics featured in the Network analytics dashboard on the [Viva Engage blog](https://techcommunity.microsoft.com/t5/viva-engage-blog/bg-p/Viva_Engage_Blog).

## Audience analytics  

>[!NOTE]
>Audience analytics are only viewable by leaders who have at least one primary assigned audience (minumum audience size of 5) and their delegates.

In the **Manage analytics** interface shown earlier, the Engage admin can adjust the level of sentiment analysis that's available to leaders and their delegates through the **Audience analytics** dashboard. This functionality enables unique levels of sentiment collection at the audience, theme, or conversation level.

Access is through the analytics icon on the top navigation bar or on the leader's storyline page.

[![Screenshot of the Audience analytics landing page.](/Viva/media/engage/admin/audience-analytics.png)](/Viva/media/engage/admin/audience-analytics.png#lightbox)

*Audience analytics* help leaders and delegates monitor engagement of their audiences on Viva Engage. This dashboard surfaces the most actively engaged communities within their audiences that have at least 50 members and one active member. A community is considered active if at least 5% of its members have reacted or replied to posts, while a community is considered idle if less than 5% of its members have engaged in this way.

*Sentiment and theme analysis* uses Azure Cognitive Services (ACS) to aggregate and analyze posts and comments from storylines and public posts. Private community posts and comments are included in the aggregate if the leader is a member of a private community (that is, the leader has permission to view private posts). Individual messages are never shown.

- **Audience-level sentiment** controls the *Sentiment* metric. When this toggle is turned off, leaders and their delegates have no access to sentiment analysis features and past data for all audiences is deleted.

-	**Theme-level sentiment** controls the *Themes* metric. When this toggle is turned off, leaders and their delegates won’t see results indicating sentiment toward frequently discussed subjects in their audience.

## Global Answers analytics

Engage admins who have the knowledge license can manage metrics for **Answers** in their organization.

[![Screenshot of Global Answers analytics landing page.](/Viva/media/engage/admin/global-answers-analytics.png)](/Viva/media/engage/admin/global-answers-analytics.png#lightbox)

In the **Manage analytics** interface of the Viva Engage admin center, admin can choose to enable or disable of advanced metrics such as **time saved** and **people helped**.  

To learn more about the metrics available for Global Answers analytics and Answers-specific actions for admin, see [Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios).

## Personal analytics  

All licensed users have access to personal analytics that help monitor the engagement on any of their storylines or community posts in Viva Engage.

[![Screenshot of the Personal analytics landing page.](/Viva/media/engage/admin/personal-analytics-admin.png)](/Viva/media/engage/admin/personal-analytics-admin.png#lightbox)

## Campaign analytics  

Engage admins and corporate communicators have access to analytics to monitor campaign engagement to improve future campaigns. You can access campaign analytics from the **Campaign management** dashboard, the campaign landing page, or the analytics icon on the main navigation menu of Viva Engage.

[![Screenshot of the Campaign analytics landing page.](/Viva/media/engage/admin/campaign-analytics.png)](/Viva/media/engage/admin/campaign-analytics.png#lightbox)

In the **Manage analytics** interface, the Engage admin can enable or disable the top content creator feature for the organization. This feature displays employees and leaders who create the most campaign posts.

## See also

[Set up and manage campaigns in Viva Engage](/viva/engage/campaigns)

[Manage administrator roles in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)

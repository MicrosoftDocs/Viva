---
ms.date: 07/14/2023
title: "Viva Connections Mobile News Notifications"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Learn how notifications are presented in Viva Connections mobile"
---

# Viva Connections mobile News notifications

The Viva Connections mobile app delivers News notifications via Teams mobile and will link users to the Viva Connections app through the notification. This document describes when notifications are sent, and the conditions that need to be met for receiving notifications.

## When notifications are sent via Teams
News notifications are delivered via Teams mobile in the following scenarios:

- News is published to a SharePoint Team or Communication site a user follows or by someone a user works closely with.
- Someone comments on a new News post.
- Someone ‘Likes’ a News post.
- Someone is @mentioned in a comment on a news post. 

> [!NOTE]
>
> - Notifications are pulled from the top 100 collaborators that an author works with. If an author works with more than 100 collaborators, the most relevant notifications will be pulled.
> - Authors can set an audience on their news posts and notifications will honor the audience that is set. Only users part of the selected Microsoft 365 audience(s) specified will receive notifications. Learn more about [audience targeting](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293#bmstep2) in SharePoint.
> - At this time, news notifications will only appear in Viva Connections via the Teams mobile app. 

Learn more about [Microsoft Viva](https://www.microsoft.com/microsoft-viva) and [Viva licensing](https://www.microsoft.com/microsoft-viva/pricing).

## Who receives notifications and when
End-users only receive notifications when the following conditions are met:

1. The Viva Connections app is installed in Teams.
2. Notifications are enabled in the Teams mobile app.
3. The notification is outside of the user's configured Teams quiet hours.
4. The user has access to the news post.
5. If audience targeting is enabled for the news post, the user must be a part of the selected Microsoft 365 audience. 

Once these conditions are met, end-users will receive a notification when news is published by someone they work closely with, or a site they follow. Authors will also receive notifications when posts they publish are liked or commented on.

### End-users receive notifications when
- A SharePoint news page is published to [a site you follow](https://support.microsoft.com/office/find-and-follow-sites-news-and-content-4411e38f-9bc5-4ecc-bd33-3dbe939ac84c).
- A SharePoint news page is published by [someone you work closely with](/graph/people-insights-overview).
- You're ‘@mentioned’ in a comment left on a SharePoint news page.

Authors can receive additional notifications when posts they publish are liked or commented on.

### Authors receive notifications when
- A user 'likes' a SharePoint news page the author created.
- A user comments on a SharePoint news page the author created.

After receiving a notification of either of these type, Viva Connections will batch additional notifications of the same type.  After the first comment notification to a user, Comments are batched in 20-min intervals. After the first like to a user, likes are batched in 60-min intervals.  

## Frequently Asked Questions

**What controls are there for notifications from Viva Connections?**

Viva Connections notifications follow Teams notification settings, including Quiet Hours settings and are only sent if users have the Viva Connections app installed.

**Can I selectively enable or disable some of these notifications?**

Notifications can't be selectively enabled or disabled, but users can toggle push notifications in Teams mobile for all apps (including Viva Connections) under **Settings** > **Notifications** > **General Activity** > **Apps on Teams**. Notifications will still be visible under the Teams Activity Feed.

**What defines ‘people I work with’?**

You can read more about how this list of people is determined and how to disable it [in this documentation](/graph/people-insights-overview).

**How often are like and comment notifications batched?**

After the first comment notification to a user, Comments are batched in 20-min intervals. After the first like to a user, likes are batched in 60-min intervals.  

**How do notifications work?**

Selecting a notification from your mobile home screen within Teams, or from the Teams activity feed, will take users directly to the source news post within Viva Connections.

**Will Viva Connections users be notified every time a user reacts to a news post?**

No. Only authors who created the news post receive notifications when someone likes or comments on a post.

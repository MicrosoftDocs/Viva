---
title: Manage content in the admin tab
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 11/23/2021
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.custom: admindeeplinkTEAMS
ms.localizationpriority: medium
description: Learn how to configure and view content in the Admin and My Learning tabs in Viva Learning.
---

# Manage content in the admin tab

You can manage some of your Viva Learning content from within the app in Teams. Use the **Admin** tab to control Viva Learning configurations and different features. This requires knowledge manager access.  

> [!NOTE]
> Features in the Admin tab require a Viva Suite or Viva Learning license.

Review this article to [Learn how to assign roles](/exchange/permissions/role-group-members).

To create a set of featured content that will show up for your users, select the **Create featured set** in the top left corner.

![Screenshot shows the feature set inside the new admin tab for Viva Learning.](../media/learning/new-admin-tab.png)

## Managing Providers

Navigate to **manage providers** for a detailed view of all configured learning providers and to manage the learning providers and respective offerings. Refer to [Manage learning management systems](../learning/configure-lms.md) and [Add other content providers](../learning/configure-other-content-sources.md) for more information.

The following features are accessible by the listed admin roles: 

**Manage Providers**: global admin, knowledge admin, knowledge manager
**Admin Tab**: global admin, knowledge admin, knowledge manager 

Once an admin configures a learning source on the M365 Admin center, the configured provider is reflected immediately in the **manage providers** section in the Viva Learning admin tab. 


:::image type="content" source="../media/learning/admin-tab-manage-providers.png" alt-text="Screenshot shows the manage providers options inside the new admin tab for Viva Learning." lightbox="../media/learning/admin-tab-manage-providers.png":::

>[!NOTE]
> Set up the learning provider and manage content sources for Microsoft Viva Learning in the Microsoft 365 Admin center.


Track the current sync status, last successful sync time, ingestion logs, and trigger full sync for each component in the expanded view:

- **Sync status and timestamp**: Check the current sync status (success/failed/in progress) of content, learner record sync, and catalog permissions sync for a specific source. Admins can see the sync status and sync completion timestamp for the following:
    - **Content sync:** Content sync, sync status, and sync status are available for all providers (LMS, 3P, Global, and SharePoint).
    - **Learning record sync**: LRS status and sync completion timestamp are currently only available for SAP SuccessFactors. We will be extending this to Saba and Cornerstone in upcoming releases.

- **Manual sync trigger**: Trigger the full sync manually for SuccessFactors (content, LRS) and Workday (content). Once a full sync is triggered, the current sync status will be updated accordingly.

- **Export log**: Admins can refer to the **export log file** for a summary of details successful or failed content ingestion for LMS, 3Ps, and SharePoint. Export logs are not yet available for LRS and catalog permissions sync.

## How content shows up in the My Learning page

The **My Learning** tab helps users take control of their learning journey. Users will be able to track assignments, recommendations, bookmarks, recent history, and completed courses on this page.

- **Recommended to you**: Recommendations from your peers will show up here.

- **Bookmarks**: Content bookmarked by the user will be shown here.

- **Recently viewed**: The user's 20 most recently viewed items will be shown under this tab. The most recently viewed item is shown first.

- **Completed**: Courses completed by the user will show under this tab.

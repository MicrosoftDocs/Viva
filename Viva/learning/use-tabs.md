---
title: Manage providers in Viva Learning
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

You can configure providers from **Manage Providers** in Viva Learning Admin. 

The **Add Provider** list shows you the available providers for configuration. Once a provider is confirmed, it appears on the **Configured Providers** list. 



> [!NOTE]
> Features in the Admin tab require both:
> - Viva Suite or Viva Learning license
> - Global admin, knowledge admin, or knowledge manage role
  
Review this article to [Learn how to assign roles](/exchange/permissions/role-group-members).

To create a set of featured content that will show up for your users, select the **Create featured set** in the top left corner.


## Managing Providers

Navigate to **Manage Providers** for a detailed view of all configured learning providers and to manage the learning providers and respective offerings. Refer to [Manage learning management systems](../learning/configure-lms.md) and [Add other content providers](../learning/configure-other-content-sources.md) for more information.

The following features are accessible by the listed admin roles: 

**Manage Providers**: global admin, knowledge admin, knowledge manager (read only)
**Admin Tab**: global admin, knowledge admin, knowledge manager 


### Manage Providers Configuration 

You can edit or deleted directly from Manage provider. 

> [!NOTE]
> If you delete all content sources, the Viva Learning Teams app will be empty.

![Image of the Manage Providers options inside Viva Learning](../media/learning/admin-tab-manage-providers.png) 

Track the current sync status, last successful sync time, ingestion logs, and trigger full sync for each component in the expanded view:

- **Sync status and timestamp**: Check the current sync status (success/failed/in progress) of content, learner record sync, and catalog permissions sync for a specific source.
First time configurations display the default sync stamp of 1/1/1

- **Manual sync trigger**: Trigger the full sync manually for a delta or full sync. Once a full sync is triggered, the current sync status will be updated accordingly.

- **Export log**: Admins can refer to the **export log file** for a summary of details successful or failed sync cycles.

> [!NOTE]
> The sync status, sync time stamp and export logs are only currently available for catalog sync for all providers. 
Sync status and sync timestamp for learner records are only available for SAP SuccessFactor. Manual sync trigger is only available for catalog in SharePoint and SAP SuccessFactor.

## How content shows up in the My Learning page

The **My Learning** tab helps users take control of their learning journey. Users will be able to track assignments, recommendations, bookmarks, recent history, and completed courses on this page.

- **Recommended to you**: Recommendations from your peers will show up here.

- **Bookmarks**: Content bookmarked by the user will be shown here.

- **Recently viewed**: The user's 20 most recently viewed items will be shown under this tab. The most recently viewed item is shown first.

- **Completed**: Courses completed by the user will show under this tab.

## Featue sets

To create a set of featured content that will show up for your users, select **Create featured set** in the top left corner. 

![Image of the create feature set within Viva Learning](../media/learning/feature-set.png)
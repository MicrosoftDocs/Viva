---
title: How to update reporting data in closed Viva Glint surveys
description: For highly trained users, Microsoft Viva Glint Advanced Configuration Uploads and Data Apps allow you to perform complex data updates. Use this guidance to determine which retroactive update option best meets your needs.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: advanced configuration, uploads, retroactive update
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 09/15/2023
---

# How to update reporting data in closed Viva Glint surveys

For highly trained users, Microsoft Viva Glint Advanced Configuration Uploads and Data Apps allow you to perform retroactive updates to survey data. Use this guidance to determine which retroactive update option best meets your needs.

> [!CAUTION]
> Do not perform a retroactive update while a Viva Glint survey is live.

## Attributes that don't require retroactive updates

Some attributes in Viva Glint always reference the most current information and don't require retroactive updates. These include:

- First Name
- Last Name
- Email Address
- Employee ID
- Time Zone
- Survey Language
- Dashboard Language
- Personal Email

## Factor in Survey Program type

Recurring and Ad-Hoc survey programs represent a point in time for all respondents, and updates for multiple users for one time period can be applied in bulk with Viva Glint retroactive update options. Lifecycle and Always-On survey programs, however, are ongoing. Surveys generate for individual users at many points throughout the lifetime of these surveys, making it difficult to pinpoint users' data in the past and apply updates, especially for Manager Hierarchy data.

## Uploads: Retroactive User Updates

Upload a file of all or some users in your closed survey to apply new values to past versions of data without touching current employee information. This option is the simplest and can be used for most retroactive updates, including non-managerial reporting hierarchy updates. [Learn more](https://go.microsoft.com/fwlink/?linkid=2247341).

> [!IMPORTANT]
> To retroactively update a Manager Hierarchy, always use the RETROACTIVE_PULSE_UPDATE Data App and not the Retroactive USERS_UPLOAD option. [Learn more](https://go.microsoft.com/fwlink/?linkid=2245700).


## Data Apps: RETROACTIVE_PULSE_UPDATE

Update Manager Hierarchy information for closed surveys by uploading corrected users to Viva Glint, running the RETROACTIVE_PULSE_UPDATE Data App, and reverting user data to current information after the update. [Learn more](https://go.microsoft.com/fwlink/?linkid=2245700).

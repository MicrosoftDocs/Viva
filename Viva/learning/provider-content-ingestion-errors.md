---
title: Fix content ingestion errors when adding content providers
description: Lists common content ingestion errors when adding content providers for Viva Learning. Provides actions to be taken to fix these errors.
ms.author: luche
author: helenclu
manager: dcscontentpm
ms.reviewer: chrisarnoldmsft
ms.date: 8/9/2022
audience: ITPro
ms.topic: troubleshooting
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.custom: 
  - CSSTroubleshoot
localization_priority: Normal
---

# Fix content ingestion errors when adding content providers

You can [add learning content providers](configure-other-content-sources.md) as content sources for Microsoft Viva Learning. This article lists errors that you may experience in the Microsoft 365 admin center during content ingestion, and steps you can follow to fix them. This list may contain more error codes in the future.

## Content ingestion errors

> [!NOTE]
> The maximum number of active learning items supported in a tenant is 500,000 records. The maximum number of total learning items supported in a tenant is 1 million records.

|Content provider |Error code |Error code description |
|:----------------|:----------|:----------------------|
|All providers |USR_ERROR_INVALID_RESOURCE_CREDENTIALS |The authentication credentials you provided are Invalid. Make sure you enter the correct credentials. You can contact Microsoft customer support for more details.|
|All providers |USR_ERROR_ACCESS_DENIED |Access denied by partner. Confirm that the credentials you entered are correct or contact the content provider's support team. |
|All providers |Changes not saved | Make sure that you've entered the correct configuration details.|

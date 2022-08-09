---
title: Fix content ingestion errors when adding LMS
description: Lists common content ingestion errors when adding LMSs for Viva Learning. Provides actions to be taken to fix these errors.
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

# Fix content ingestion errors when adding LMS

You can [add learning management systems](../configure-lms.md) as content sources for Microsoft Viva Learning. This article lists errors that you may experience in the Microsoft 365 admin center during content ingestion, and steps you can follow to fix them. This is an exhaustive list and may contain more error codes in the future.

## Content ingestion errors

> [!NOTE]
> The maximum number of active learning items supported in a tenant is 500,000 records. The maximum number of total learning items supported in a tenant is 1 million records.

|Learning management system |Error code |Error code description|
|:-------------------|:-------------|:--------|
|All LMSs | USR_ERROR_INVALID_RESOURCE_CREDENTIALS |The authentication credentials you provided are Invalid. Make sure you enter the correct credentials. You can contact Microsoft customer support for more details. |
|All LMSs |USR_ERROR_ACCESS_DENIED |Access denied by partner. Confirm that the credentials you entered are correct or contact the content provider's support team. |
|All LMSs |Changes not saved |Confirm that you've entered the correct configuration details. |
|SuccessFactors |USR_ERROR_SF_INITIAL_PACKAGE_NOT_FOUND |No new content ingested as the required package was not found in the SuccessFactors SFTP server. Make sure that the [SuccessFactors package](../configure-successfactors-content-source.md#configure-in-your-successfactors-portal) is available. It may take up to seven working days to generate this package the first time you sync. If you can't find the package, contact your SuccessFactors support team. |
|SuccessFactors |USR_ERROR_SF_DELTA_PACKAGE_NOT_FOUND |No new content was ingested as the required package was not found in the SuccessFactors SFTP server. Make sure that SF package is available in the configured folder path on your SF portal. If you can't find the package, contact your SuccessFactors support team. |
|SuccessFactors |USR_ERROR_SFTP_NO_FILES_FOUND |No new content ingested because there were no files present in the SuccessFactors SFTP server.  Make sure that you can find the files in the [SuccessFactors package](../configure-successfactors-content-source.md#configure-in-your-successfactors-portal). If you can't find the files, contact your SuccessFactors support team. |
|SuccessFactors |USR_ERROR_SF_COMPRESSED_PACKAGE_SIZE_EXCEEDED |No new content was ingested because the compressed package size exceeded 2 GB. [Contact Microsoft customer support](../help-support.md) for more details. |
|SuccessFactors |USR_ERROR_SF_UNCOMPRESSED_PACKAGE_SIZE_EXCEEDED |No new content was ingested because the uncompressed package size exceeded 25 GB. [Contact Microsoft customer support](../help-support.md) |
|Cornerstone OnDemand |USR_ERROR_INVALID_RESOURCE_CREDENTIALS |The authentication credentials you provided are Invalid. Make sure the credentials are being copied from Microsoft Viva Learning in Cornerstone OnDemand portal. |

Your changes won't be saved if you've entered any fields incorrectly. You can close and reopen the flyout to view and correct any invalid fields.

|Learning management system |Error message |
|:----------------|:----------------------|
|All LMSs |Your changes couldn’t be saved. Make sure you’ve entered the correct (field name). |

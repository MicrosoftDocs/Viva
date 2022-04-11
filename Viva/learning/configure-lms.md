---
title: Add learning management systems for Microsoft Viva Learning
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 11/01/2021
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: Learn how to configure learning management systems as a learning content source for Microsoft Viva Learning.
---

# Add learning management systems for Microsoft Viva Learning

A growing set of learning management systems are available through Viva Learning. This set may change at any time as more providers join or change their status with the program.

Learning management systems are not enabled by default. To enable these sources, you will need to [add them in the Microsoft 365 admin center](content-sources-365-admin-center.md#configure-settings-for-the-learning-content-sources) and follow the specific instructions shown in the following table.

>[!NOTE]
>You'll need a Viva Learning or Viva Suite license to access this feature. [Learn more about licensing](https://www.microsoft.com/microsoft-viva/learning).

>[!NOTE]
>It can take 24 to 48 hours for Viva Learning users to see content for the sources you enabled in the admin portal.

## Learning management systems

|Learning management system  |Configuration instructions  |
|---------|---------|
|Cornerstone OnDemand |[Configure Cornerstone OnDemand as a content source](configure-cornerstone-content-source.md)         |
|Saba    |[Configure Saba as a content source](configure-saba-content-source.md)         |
|SAP SuccessFactors   |[Configure SAP SuccessFactors as a content source](configure-successfactors-content-source.md)         |

>[!NOTE]
>Available learning management systems are subject to change. Depending on your organization, you may have access to different learning management systems than are listed here.

## Content ingestion errors

If you experience any errors in your Microsoft 365 admin center during content ingestion, refer to the table below for next steps. This is an exhaustive list and may contain more error codes in the future.

>[!NOTE]
>The maximum number of active learning items supported in a tenant is 500,000 records.
The maximum number of total learning items supported in a tenant is 1 million records.

|Learning management system |Error code |Error code description |
|:----------------|:----------|:----------------------|
|All LMSs |USR_ERROR_INVALID_RESOURCE_CREDENTIALS |The authentication credentials you provided are Invalid. Make sure you enter the correct credentials. You can contact Microsoft customer support for more details. |
|All LMSs |USR_ERROR_ACCESS_DENIED |Access denied by partner. Confirm that the credentials you entered are correct or contact the content provider's support team. |
|All LMSs |Changes not saved |Confirm that you've entered the correct configuration details. |
|SuccessFactors |USR_ERROR_SF_INITIAL_PACKAGE_NOT_FOUND |No new content ingested as the required package was not found in the SuccessFactors SFTP server. Make sure that the [SuccessFactors package](configure-successfactors-content-source.md#configure-in-your-successfactors-portal) is available. It may take up to 7 working days to generate this package the first time you sync. If you can't find the package, contact your SuccessFactors support team. |
|SuccessFactors |USR_ERROR_SF_DELTA_PACKAGE_NOT_FOUND |No new content was ingested as the required package was not found in the SuccessFactors SFTP server. Please ensure that SF package is available in the configured folder path on your SF portal. If you can't find the package, contact your SuccessFactors support team. |  
|SuccessFactors |USR_ERROR_SFTP_NO_FILES_FOUND |No new content ingested because there were no files present in the SuccessFactors SFTP server.  Make sure that you can find the files in the [SuccessFactors package](configure-successfactors-content-source.md#configure-in-your-successfactors-portal). If you can't find the files, contact your SuccessFactors support team.|
|SuccessFactors |USR_ERROR_SF_COMPRESSED_PACKAGE_SIZE_EXCEEDED |No new content was ingested because the compressed package size exceeded 2GB. [Contact Microsoft customer support](help-support.md) for more details. |
|SuccessFactors |USR_ERROR_SF_UNCOMPRESSED_PACKAGE_SIZE_EXCEEDED | No new content was ingested because the uncompressed package size exceeded 25GB. [Contact Microsoft customer support](help-support.md) |
|Cornerstone OnDemand |USR_ERROR_INVALID_RESOURCE_CREDENTIALS |The authentication credentials you provided are Invalid. Make sure the credentials are being copied from Microsoft Viva Learning in Cornerstone OnDemand portal. |

Your changes won't be saved if you've entered any fields incorrectly. You can close and reopen the flyout to view and correct any invalid fields.

|Learning management system |Error message |
|:----------------|:----------------------|
|All LMSs |Your changes couldn’t be saved. Make sure you’ve entered the correct (field name). |

## Content consumption for end users

Once you've added a learning management system as a content source from the Microsoft 365 admin center, content from the LMS will flow to the Viva Learning app and will be visible to end users.

Once a user chooses to play a course in Viva Learning, they will be directed to the LMS webpage and will need to enter the login credentials on the LMS sign in page. [Learn more about how to consume content with Viva Learning](https://support.microsoft.com/office/01bfed12-c327-41e0-a68f-7fa527dcc98a).

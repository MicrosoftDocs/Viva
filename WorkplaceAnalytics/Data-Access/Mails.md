---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Email metrics for Workplace Analytics Data export
description: One row for every email sent
author: madehmer
ms.author: v-midehm
ms.date: 02/27/2019
ms.topic: article
ms.prod: wpa
---

# Mails (.csv)

This file includes one row for every email sent with the following metrics.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MailId**|**string**|Unique identifier for each email; primary key|
|**ConversationId**|**string**|Unique thread identifier|
|**Subject**|**string**|Meeting subject (respects tenant privacy settings; see [Workplace Analytics Privacy settings](../use/settings.md#privacy-settings))|
|**SentTime**|**datetime**|When the email was sent, in the sender's local time|
|**SenderTimeSpentinMinutes**|**double**|How many minutes spent writing the email (heuristic estimated value)|
|**NumberOfRecipients**|**integer**|Number of email recipients, not including the sender|
  
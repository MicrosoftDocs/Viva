---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Mail metrics for Workplace Analytics Data Export
description: One row for every email sent
author: gbowerman
ms.author: madehmer
ms.date: 12/20/2018
ms.topic: language-reference
ms.prod: wpa
---

# Mails (.csv)

This file includes one row for every email sent with the following metrics.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MailId**|**string**|Unique identifier for each email. Primary key.|
|**ConversationId**|**string**|Unique thread identifier.|
|**Subject**|**string**|Meeting subject. Respects tenant privacy settings. See [Workplace Analytics settings](../use/settings.md#privacy-settings).|
|**SentTime**|**datetime**|When the email was sent, in the sender's local time.|
|**SenderTimeSpentinMinutes**|**double**|How many minutes spent writing the email (heuristic estimated value).|
|**NumberOfRecipients**|**integer**|Number of email recipients, not including the sender.|
  
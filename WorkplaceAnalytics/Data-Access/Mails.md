---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,FOLLOW
title: Mails table (WPA Data Access)
description: One row for every email sent
author: gbowerman
ms.author: guybo
ms.date: 05/11/2018
ms.topic: language-reference
ms.prod: wpa
---

# Mails table (CSV)

This table contains one row for every email sent.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MailId**|**string**|Unique identifier for each email. Primary key.|
|**ConversationId**|**string**|Unique thread identifier.|
|**Subject**|**string**|Meeting subject. Respects tenant privacy settings. See [Workplace Analytics settings](../setup/set-up-workplace-analytics#step-4-configure-workplace-analytics-settings).|
|**SentTime**|**datetime**|When the email was sent, in the sender's local time.|
|**SenderTimeSpentinMinutes**|**double**|How many minutes spent writing the email (heuristic estimated value).|
|**NumberOfRecipients**|**integer**|Number of email recipients, not including the sender.|
  
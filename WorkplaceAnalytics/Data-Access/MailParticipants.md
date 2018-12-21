---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Email participant metrics for Workplace Analytics Data Export
description: One row for every email sent, and every email received
author: gbowerman
ms.author: madehmer
ms.date: 12/20/2018
ms.topic: language-reference
ms.prod: wpa
---

# MailParticipants (.csv)

This file includes one row for every email sent, and every email received with the following metrics.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MailId**|**string**|Unique identifier for every email sent. Foreign key matching primary key of the [Mails table](./mails.md).|
|**PersonHistoricalId:**|**string**|Unique identifer for every person. Foreign key matching PersonHistorical table primary key.|  
|**IsSender**|**boolean**|True if this person sent the email.|
|**PersonTimeSpentInMinutes**|**double**|Time spent reading or writing the email (heuristic estimated value).|
|**LocalSentTime**|**datetime**|Local time when the email was sent.|

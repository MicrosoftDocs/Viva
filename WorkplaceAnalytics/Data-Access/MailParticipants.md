---
# Metadata Sample
# required metadata

title: MailParticipants table (WPA Data Access)
description: One row for every email sent, and every email received
author: gbowerman
ms.author: guybo
ms.date: 05/11/2018
ms.topic: language-reference
ms.prod: wpa
---

# MailParticipants table (CSV)


  Contains one row for every email sent, and every email received.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**MailId**|**string**|Unique identifier for every email sent. Foreign key matching Mails table primary key.|
|**PersonHistoricalId:**|**string**|Unique identifer for every person. Foreign key matching PersonHistorical table primary key.|  
|**IsSender**|**boolean**|True if this person sent the email.|
|**PersonTimeSpentInMinutes**|**double**|Time spent reading or writing the email (heuristic estimated value).|
|**LocalSentTime**|**datetime**|Local time when the email was sent.|


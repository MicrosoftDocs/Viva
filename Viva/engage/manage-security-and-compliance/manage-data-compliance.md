---
title: "Manage Viva Engage data compliance"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: dmillerdyson
ms.date: 08/08/2023
audience: Admin
ms.topic: article
ms.localizationpriority: medium
ms.service: viva
ms.custom: viva-engage
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 8c4651fa-12c2-4ced-b4ea-2200c0a630ed
description: "Monitor your Viva Engage data with these features: keyword monitoring, security settings, data export, data retention, and analytics."
---

# Manage Viva Engage data compliance

As a Viva Engage admin, you can keep your users' Viva Engage posts appropriate and meet security and compliance requirements. You can set up alerts for content that matches keywords, set data retention policies, and if needed, you can view private content. You can also [export data from Viva Engage](export-viva-engage-enterprise-data.md).

<a name="MonitorKeywords"> </a> 
## Monitor Keywords

Monitor sensitive content by specifying keywords such as banned words or employees' personal information. All messages in internal and external networks, including messages to and from external participants can be monitored.
  
 **Set person responsible for monitoring, editing, and deleting flagged posts**
  
1. In the Viva Engage admin center, go to **Content and security** > **Monitor Keywords**, and enter the person's email address in **Email Address**. This person should be a verified admin so they have permission to delete messages anywhere in Viva Engage.
    
2. When a post matches a keyword, the person listed in **Email Address** receives an email. They can then select a link in the email to review, edit, or delete the flagged post. 
    
 **Specify keywords and phrases to monitor**
  
1. In the Viva Engage admin center, go to **Content and Security** \> **Monitor Keywords**.
    
2. Enter the words and phrases you want to monitor, each on its own line.
    
    You can use regular expressions to match patterns. For information on using regular expressions, see [Regular Expression Language](/dotnet/standard/base-types/regular-expression-language-quick-reference).
    
    Here are some examples of regular expressions commonly used for monitoring.
    
|**Purpose**|**Pattern**|**Matches**|
|:-----|:-----|:-----|
|Word boundary  <br/> |\bword\b  <br/> |\btheme\b matches "theme" but not "themes" or "them"  <br/> |
|Credit cards  <br/> |\b(?:\d[ ‐]\*?){13,16}\b  <br/> |1234 5678 90123  <br/> 1234 5678 9012 3456  <br/> 1234‐5678‐9012‐3456  <br/> |
|Social Security numbers  <br/> |\b\d{3}[ -]\d{2}[ -]\d{4}\b  <br/> |123 45 6789  <br/> 123‐45‐6789  <br/> |
Monitor group create|has created|Matthew has created the Easter Region Sales group.
  
<a name="DataRetention"> </a>
## Data retention

You can control whether deleted messages and files stored in Viva Engage are retained and available in data exports. 
 
Networks in Archive Mode retain all content for the life of that network. This is true even if users delete content; the content is only removed from the front end. Networks in Delete mode remove content after 30 days after it's been deleted. At that point, the content is not recoverable.

 **Set whether to retain deleted messages and files stored in Viva Engage**
  
1. In the Viva Engage admin center, go to **Governance and Compliance** \> **Data Export**.
    
2. To prevent deleted data from being available in exported data, select **Delete**. Or, to enable deleted data to appear in exported data, select **Archive**.
    
    To permanently delete retained data in Viva Engage storage, you must use the Viva Engage Developer API. First, export the data to identify the data you need to delete permanently. Next, write a custom PowerShell script to loop through the specific items to delete. For information, see the REST API section of  [Develop apps for Viva Engage](https://go.microsoft.com/fwlink/?linkid=874797). 

 **Set whether to retain deleted files stored in SharePoint**

For Viva Engage files saved in SharePoint, Office 365 data retention settings apply. For more information, see [Overview of retention policies](/office365/securitycompliance/retention-policies).
    
<a name="ContentMode"> </a>
## Content mode

If as a verified Viva Engage admin, you have a legal reason to view private messages, you can select to see them. For more information, see [Monitor private content in Viva Engage](monitor-private-content.md).
  
## See also

[Overview of security and compliance in Viva Engage](security-and-compliance.md)

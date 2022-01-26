---
title: Frequently asked questions about Microsoft Viva Topics
ms.author: ruthhollands
author: ruthholls
manager: pamgreen
audience: admin
ms.reviewer: cjtan
ms.topic: article
ms.collection: m365initiative-viva-topics
ms.service: viva 
ms.subservice: viva-topics 
search.appverid:
    - MET150  
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Read commonly asked questions and answers about using Microsoft Viva Topics.

---

# Frequently asked questions about Microsoft Viva Topics 

## How does the Viva AI/ML model connect to Cloudspo’s data?
 
Viva AI builds an index similar to search and relies on the SPO search crawler to keep the index up to date. Search crawler detects changes in SPO, performs basic parsing of various document formats, and pushes the content and metadata streams into O365 Microsoft Substrate. Viva AI registers listeners in Office 365 Substrate for changes in these document streams. The main difference between Viva and Search is that Viva builds a knowledge graph, not a fulltext search index, so it’s possible to execute queries like: finding all topics by name, lookup metadata of a given topic such as alternative names, or, find all related topics of a given topic. For more information, see [Use Microsoft Search to find topics in Microsoft Viva Topics](search.md).
 


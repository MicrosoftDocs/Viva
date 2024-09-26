---
title: "Use eDiscovery for Viva Engage content"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/26/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:     
- MET150
- YAE150
ms.assetid: a9a25f87-e643-41ce-9630-b74d10e40b1a
description: Learn how to use eDiscovery with Engage.
ROBOTS: NOINDEX, NOFOLLOW 
---

# Use eDiscovery for Viva Engage content

You can use eDiscovery to surface Viva Engage content from within the Microsoft Purview compliance portal. However, to use this functionality, your Viva Engage network must be in Native Mode. Viva Engage networks provisioned after January 9, 2020 run in Native Mode by default. For more information, see [Overview of Native Mode](overview-native-mode.md).

### How to query Viva Engage content 

You can find complete instructions on how to run eDiscovery queries on your Microsoft content on the [Microsoft Purview compliance portal](/purview/). While the portal doesn’t explicitly discuss Viva Engage, this process does surface Viva Engage content. To narrow your eDiscovery search results to include _only_ Viva Engage content, follow these steps:  

1. In your eDiscovery query, add a **Type** filter. 
1. Depending on your version of eDiscovery, do one of the following:  
    - In eDiscovery (Standard), from the drop-down menu, select **Equals any of**, and then select the checkbox for **Yammer Messages**.
    
      :::image type="content" source="../media/engage/admin/query-type-ediscovery1.png" alt-text="Screenshot of how to filter an eDiscovery query to search on Engage content."lightbox="../media/engage/admin/query-zoom1.png":::


    - In eDiscovery (Premium), select **Equals any of**, select **choose value**, search on *Yammer* and select the checkbox next to **Yammer messages**.
    
      :::image type="content" source="../media/engage/admin/query-type-ediscovery2.png#lightbox" alt-text="Screenshot of how to filter an eDiscovery query to search on Engage content."lightbox="../media/engage/admin/query-zoom2.png":::

### Viva Engage data points

After you run your query, your search results will include (but aren't limited to) these key data points:  

- Message Body
- Author
- Recipients
- Links
- Attachments
- Mentions
- Timestamp
- Reactions

We continue to update the data points that are included in search results for Viva Engage.

## See also

[Overview of Microsoft Purview eDiscovery (Premium)](/purview/ediscovery-overview)
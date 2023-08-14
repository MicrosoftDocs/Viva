---
title: "eDiscovery in Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 08/14/2023
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:     
- MET150
- YAE150
ms.assetid: a9a25f87-e643-41ce-9630-b74d10e40b1a
description: Learn how to use eDiscovery with Engage.
ROBOTS: NOINDEX, NOFOLLOW 
---

# eDiscovery in Viva Engage

Viva Engage supports eDiscovery and eDiscovery (Premium) within the Microsoft Purview compliance portal. However, to use this functionality, your Viva Engage network must be in Native Mode.  

> [!NOTE] All Viva Engage networks provisioned after January 9, 2020 run in Native Mode by 
> default. For more information, see [Overview of Native Mode](../overview-native-mode.md).

### How to query Viva Engage content 

You can find complete instructions on how to run eDiscovery queries on your Microsoft content on the [Microsoft Purview compliance portal](/purview/). While the portal doesn’t explicitly discuss Viva Engage, this process can surface Viva Engage content. You can narrow your eDiscovery search results to include only Viva Engage content with the following step:  

1. In your eDiscovery query, add a **Type** filter.  
    -  In eDiscovery, from the drop-down menu, select **Equals any of**, and then select the checkbox for **Yammer Messages**.
    :::image type="content" source="../../media/engage/admin/query-type-ediscovery1.png" alt-text="Screenshot of how to filter an eDiscovery query to search on Engage content.":::

    - In eDiscovery (Premium), select **Equals any of**, select **choose value**, search on *Yammer* and select the check box next to **Yammer messages**. 
    :::image type="content" source="../../media/engage/admin/query-type-ediscovery2.png" alt-text="Screenshot of how to filter an eDiscovery query to search on Engage content.":::

### Viva Engage data points 
After you run your query, your search results will include (but aren't limited to) these key data points:  

- Message Body
- Author
- Recipients
- Links 
- Attachments
- Mentions 
- Timestamp

We continue to update which data points are included in search results for Viva Engage.

## See also
[eDiscovery in Office 365](/office365/securitycompliance/ediscovery)

[Overview of the eDiscovery (Premium) solution in Microsoft Purview](/office365/securitycompliance/office-365-advanced-ediscovery)
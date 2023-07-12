---
title: "Overview of eDiscovery in Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: dmillerdyson
ms.date: 06/28/2023
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
description: An overview about eDiscovery in Viva Engage.
---

# Overview of eDiscovery in Viva Engage networks

Viva Engage now supports both eDiscovery and eDiscovery (Premium) within the Microsoft Purview compliance portal.

To use this functionality, your Viva Engage network will need to be in Native Mode. If your network was provisioned after January 9, 2020, you are already in Native Mode. If your network was provisioned *before* January 9, 2020, you will need to follow the steps in the [Overview of Native Mode](../overview-native-mode.md).

 > [!NOTE]
> Native Mode is required to take advantage of eDiscovery and the Microsoft Purview compliance portal. This functionality is unavailable for networks in non-Native mode.

You can learn more about eDiscovery in the [Microsoft Purview compliance portal](/microsoft-365/compliance/).

The processes outlined in the above documentation explain how to run eDiscovery searches on all your Microsoft content. While Viva Engage isn’t discussed explicitly in those documents, the same processes mentioned apply to Viva Engage content. When writing a search query in either eDiscovery or eDiscovery (Premium), you can filter on Viva Engage content specifically by selecting **Viva Engage Messages** as the *Type* of content.

> [!NOTE]
> You do not need to select Viva Engage messages as the Type to ensure Viva Engage messages are included in your results. This option allows you to filter so that your results only include Viva Engage messages.

When viewing Viva Engage content in the eDiscovery tools, you can expect the following information to be available:

- Message Body
- Author
- Recipients
- Timestamp

We plan to continue updating the service to include more information not listed above.

## See also

[FAQ: eDiscovery](./faq-ediscovery.md)

[eDiscovery in Microsoft 365](/office365/securitycompliance/ediscovery)

[Overview of the eDiscovery (Premium) solution in Microsoft Purview](/office365/securitycompliance/office-365-advanced-ediscovery)

[Overview of Native Mode](../overview-native-mode.md)

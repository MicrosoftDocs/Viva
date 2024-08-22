---
ms.date: 08/20/2024
title: "Use eDiscovery for Viva Pulse Pulse content"
description: "View Viva Pulse content through Microsoft Purview eDiscovery content search."
ms.reviewer: 
ms.author: hasrivas
author: hasrivas
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH 
ms.topic: article
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection:  
search.appverid:
---

# Use eDiscovery for Viva Pulse content 

You can use eDiscovery to surface Viva Pulse content from within the Microsoft Purview compliance portal. Pulse requests and responses data is stored in Microsoft Forms. Hence, we rely on an eDiscovery search of Microsoft Forms data in Microsoft Purview. The following Pulse data is discoverable using Microosft Purview:
- Pulse requests: Pulse requests created and sent by users. 
- Pulse responses: Responses to Pulse requests by users.

## Pre-requisites

- Licensing: Because discovery of Forms content within this preview requires eDiscovery premium, you must have appropriate licensing. Please see this article for more information: 
[Microsoft Purview eDiscovery - Service Descriptions | Microsoft Learn](https://learn.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-purview-ediscovery#feature-availability)  If your tenant does not have appropriate licensing, see [Free trial of Microsoft Purview compliance solutions | Microsoft Learn](https://learn.microsoft.com/purview/compliance-easy-trials). 
- Permissions: You must have appropriate permissions to use eDiscovery. See the following article for more information: [Assign eDiscovery permissions in the Microsoft Purview compliance portal | Microsoft Learn](https://learn.microsoft.com/purview/ediscovery-assign-permissions).


## How to search for Pulse content via Microsoft Forms content

- Microsoft Pulse content is discoverable using the author's Exhange mailbox locations ([custodial, non-custodial, or additional](https://learn.microsoft.com/purview/ediscovery-managing-custodians)).

- To find both Pulse requests and responses, you can use the **Microsoft Forms** type when creating a collection using the query builder or use the KQL editor with **ItemClass=“IPM.File.Forms”** as the search term.

- You can identify specific Pulse requests by searching for the Pulse request title.

- Pulse requests and responses can be grouped within the review set by selecting **Group by conversations and related items**.

- Participants, recipients, sender can also be used to identify Pulse requests & responses.

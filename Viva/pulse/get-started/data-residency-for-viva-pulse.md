---
title: Data residency for Viva Pulse
description: "Data residency for Viva Pulse"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 07/12/2023
ms.topic: article
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection:
- m365initiative-viva-pulse 
- essentials-privacy
search.appverid: MET150
---

# Data residency for Viva Pulse

## Summary

Viva Pulse empowers leaders and managers to seek and act on feedback when it matters. Using research-backed templates, teams can quickly share their experience and suggestions, and reporting helps managers pinpoint what is working well and which areas to focus on over time.  

Learn more about [Microsoft Viva Pulse](../introduction-to-viva-pulse.md).

## Data residency for Viva Pulse

Viva Pulse data residency is limited to two regions, West US and EU, for data stored at rest which constitutes metadata for the Pulses authored and responded to, as well as reports generated for those Pulses. The Pulse instances and the responses are stored in Microsoft Forms, where the data residency for Microsoft Forms becomes applicable.

**West US data residency**

Required conditions:
1. _Tenant_ has a tenant hosting location country that is non-EU.
2. _Tenant_ has a valid Viva Pulse license.  
3. _Tenant_ has a valid Microsoft Forms license.

**EU data residency**

Required conditions:
1. _Tenant_ has a tenant hosting country included in European Union Data Boundary (EUDB). 
2. _Tenant_ has a valid Viva Pulse license.
3. _Tenant_ has a valid Microsoft Forms license.

## User experience

Viva Pulse data residency is seamless to the end user. The application will appropriately redirect the user to the correct region where their organizational data is hosted.

## How can I determine customer data location?

Viva Pulse research-backed templates and customized templates are stored in Azure Cosmos DB in West US or EU depending on the tenant’s hosting location. Pulse instances authored in Viva Pulse are stored in Microsoft Forms, along with all the responses to the Pulse. Data in Microsoft Forms is subject to [data residency capabilities offered by Microsoft Forms](https://support.microsoft.com/office/data-storage-for-microsoft-forms-97a34e2e-98e1-4dc2-b6b4-7a8444cb1dc3).

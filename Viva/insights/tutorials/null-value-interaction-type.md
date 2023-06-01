---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 03/29/2023
title: Null values after filtering Teams channel metrics
description: About using "reaction" as a value for "Interaction type" in Teams channel metrics
author: lilyolason
ms.author: v-lilyolason
ms.topic: reference
ms.localizationpriority: medium
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Null values after filtering the Teams channel metric


>[!Important]
>This article is for the legacy Workplace Analytics app and does not reflect functionality available on the updated Viva Insights platform. Access current documentation for Viva Insights advanced insights here: [advanced insights documentation](../advanced/introduction-to-advanced-insights.md).

In the **Teams channels** metric, you can filter by a property called "Interaction type." Workplace Analytics doesn't restrict which values for "Interaction type" you can pick, but certain values will only result in null values for all employees in the query:

* Channel messages sent where Interaction type = "Reaction" or "Channel visit"
* Channel message hours, After hours channel message hours, or Working hours channel message hours where Interaction type = "Reaction"

For more information about the **Teams channels** metric, refer to [Advanced insights metric filters](../use/metric-filters.md#teams-channel-metric-filters)
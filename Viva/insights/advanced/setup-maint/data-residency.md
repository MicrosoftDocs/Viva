---
ms.date: 09/24/2024
title: Viva Insights data residency for advanced insights, managers, and leaders
description: Provides information to customers about where data is stored at rest based on their geography and date of Viva Insights provisioning. 
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Viva Insights data residency for advanced insights, managers, and leaders

Viva Insights provides local data residency capabilities for advanced insights, managers, and leaders related to collaboration activities (for example, number of emails sent, or number of emails read) and metric computations data. The location where this data is stored at rest is determined by the default geography of the *tenant* (default mailbox region), not individual users.  

See the table below for supported local data residency scenarios:

| Viva Insights provisioned after: | With tenant default mailbox region: | Viva Insights advanced, manager, and leader data stored at rest provided in: |
|----|----|----|
| June 4, 2024 | Australia (AUS) | Australia |
| August 12, 2024 | Japan (JPN) | Japan |
| September 13, 2024 | Canada (CA) | Canada |
| September 13, 2024 | United Kingdom (GB) | United Kingdom |

All customers provisioned after the dates above do not need to take any action for local data residency.

Customers provisioned *before* the above dates will continue to be hosted in the same region as they did prior to having local residency capabilities available. See the table for [static data location information for select workloads](/microsoft-365/enterprise/m365-dr-workload-other#static-data-location-information-for-select-workloads).
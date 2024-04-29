---
ms.date: 06/16/2023
title: Upload organizational data during setup
description: Get a quick overview of how to upload organizational data as part of setup
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

# Upload organizational data

![insights admin](../images/applies-to-insights-admin.png) *Applies to: Insights Administrator*

:::image type="content" source="../images/setup-upload-1.png" alt-text="Image alt text." lightbox="../images/setup-upload-1.png":::

Now that you've set up the advanced insights app, you're ready to start bringing in data so analysts can run analyses and leaders can view organization insights.

By default, Viva Insights uses your organization’s Microsoft Entra data. When you leave Microsoft Entra ID as the default, you'll automatically bring in the following attributes to Viva Insights: **PersonId**, **ManagerId**, and **Organization**. You'll also bring in **Domain** and **TimeZone** from user settings and SMTP addresses, respectively.

If you want to keep using Microsoft Entra ID for now as your data source, you don’t need to do anything extra to set up organizational data in the advanced insights app.

If you want to add more attributes to your organizational data than what the default setting provides, you'll want to use a .csv file instead. To upload organizational data through a .csv file, follow the guidance in [Prepare organizational data](../admin/prepare-org-data.md) and [Upload organizational data (first upload)](../admin/upload-org-data-first.md). After you upload a file, here’s the basic process:

1. Data mapping – You map the uploaded data to the applicable field names. 
1. Data validation – Viva Insights validates the data. When validation completes successfully, you'll see a confirmation message. If validation wasn’t successful, you’re  advised what to do next. 
1. Data processing – Viva Insights processes the validated data. When the processing is done, you'll see a message that setup is complete.

---
title: "Migrate classic feeds in HTML apps with Embed feed for Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 08/02/2024
audience: Admin
ms.topic: article
ms.localizationpriority: medium
ms.service: viva-engage
ms.custom: Adm_Yammer
ms.collection: SPO_Content
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 4817d2fa-50f6-4f25-88a0-a312745768d4
description: "Replace JavaScript-based Embed feeds (Classic Yammer) to interface-based Embed feeds in your HTML-based applications."
---

# Replace classic feeds in HTML apps with Embed feeds for Engage 

**Embed Feed for Engage** lets you add Viva Engage feeds to your HTML-based applications with iFrame widgets you can copy and paste. This modern experience replaces classic Embed feeds, which required that you write JavaScript code.

>[!NOTE] 
>Starting January 31, 2025, Microsoft will retire and no longer support classic Embed feeds. To avoid a broken feed experience, we recommend that you replace your classic Embed feeds as soon as possible using the following instructions.

## Replace your classic Embed feed

Follow these instructions to update your Embed feed experience. This process doesn’t affect Viva Engage data in any way.

1. Open the HTML page where you've added the Embed feed.

1. In a new browser tab, go to the [iFrame widget configuration site](https://engage.cloud.microsoft/embed/widget?domainRedirect=false) in Viva Engage.

    :::image type="content" source="../../media/engage/admin/engage-embed-feed-ui.png" alt-text="Screenshot shows the Embed feed interface where you can use radio buttons to select the different types of feeds.":::

1. From the left pane, select the type of feed you want to replace. Note the following changes from the classic version:

    - **Home feed** replaces My feed.
    - **Community feed** replaces Group feed. For source, type the community name.
    - **Topic feed** requires a topic name for your feed.
    - **User feed** requires a user name associated with the feed.
    - **Web link feed** replaces Open Graph feed. Enter the source URL currently in use.

1. When you’re done, select **Get code**.

    The code for your iFrame widget appears on the main page.

1. Select **Copy**.

1. On the HTML page you opened in step 1, paste the iFrame code in the appropriate location to replace the JavaScript code for your previous classic Embed feed.

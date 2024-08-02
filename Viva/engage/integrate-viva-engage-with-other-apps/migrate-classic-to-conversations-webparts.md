---
title: "Migrate classic feeds in SharePoint to the Viva Engage Conversations web part"
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
description: "Migrate feeds that use the classic Highlights web part to Viva Engage Conversations web parts on your modern SharePoint pages."
---

# Migrate classic feeds on SharePoint to the Viva Engage Conversations web part

>[!NOTE]
>Starting January 31, 2025, Microsoft will retire and no longer support the classic Highlights web part for Viva Engage feeds in SharePoint. To avoid a broken feed experience, we recommend that you migrate to the Viva Engage Conversations web part as soon as possible using the instructions in this article.

Viva Engage Conversation web parts allow people to engage with each other in modern SharePoint without leaving the page. This functionality is available only for the online SharePoint experience available in Microsoft 365.

With Conversations web parts, you can:

- Add a feed from a community, user, or home page
- Start a conversation with a topic
- Interact with conversations (reply, react, mention, and so on)

Learn more about [Viva Engage web parts](https://support.microsoft.com/en-us/office/use-a-viva-engage-web-part-in-sharepoint-a53cfa0c-3d09-42c8-a286-1038a81c59da?ui=en-us&rs=en-us&ad=us).

## Migrate classic Highlights web parts to the Conversations web part

Use this procedure to migrate all instances of the classic Highlights web part in SharePoint pages that you own or have permissions to. The migration process doesn’t affect Viva Engage data in any way.

1. On the SharePoint modern page, select **Edit** at the top of the page.

1. Hover over your existing classic Highlights web part or under the title region, select the plus icon, and select the **Highlights** web part.

    :::image type="content" source="../../media/engage/admin/hover-for-web-part-menu.png" alt-text="Screenshot shows the title region and plus sign where you can access the web part menu on a modern SharePoint page.":::
    :::image type="content" source="../../media/engage/admin/web-part-menu-highlights.png" alt-text="Screenshot shows the Viva Engage web part menu.":::

1. Select **Use the classic version of Conversations source**.

    :::image type="content" source="../../media/engage/admin/web-part-menu-highlights-classic.png" alt-text="Screenshot shows the radio buttons that let you specify different types of conversation feeds available.":::
    You should see the code for your classic Highlights web part.

1. On the right, select **Use latest version**.

    :::image type="content" source="../../media/engage/admin/web-part-use-latest-version.png" alt-text="Screenshot shows the classic Highlights interface with an button to go to the newer Conversations interface.":::

1. Hover below the classic web part to open the web part menu to select **Conversations**.

    :::image type="content" source="../../media/engage/admin/hover-menu-conversations-web-part.png" alt-text="Screenshot shows the Conversations menu.":::

1. Set up the Conversations web part to include settings you want to retain from your Highlights web part, as well as new layout and background option from the **Section** panel on the right.

    :::image type="content" source="../../media/engage/admin/web-parts-old-and-new.png" alt-text="Screenshot shows the Conversations menu where you specify the feed type, source, and other options.":::

    - **Home Feed** displays the most recent conversations that appear on the **Home** page in Viva Engage. Select this if the Classic Highlights web part displayed the Viva Engage home feed. Turn off the publisher option if you don't want users in your organization to publish Engage posts from the web part.

    - **Community** displays the most recent conversations posted in the selected community. Select this option if the Classic Highlights web part displayed a **group feed**, and enter the community name. Choose the appropriate filter for the conversations you want to display in the web part. Turn off the publisher option if you don't want users in your organization to publish Engage posts from the web part.

    - **User** displays the most recent conversations in which the user participated. If the Classic Highlights web part displayed a specific person’s user feed, select this option and enter the user name.
 
    - **Topic** displays the most recent conversations tagged with this topic. Select this option if the Classic Highlights web part displays the feed for a topic, and enter the topic name.
 
1. In **Number of conversations to show**, select the number based on how much space the feed should use on the page.

    After you published the page, users can reply and follow the conversation from within your page.

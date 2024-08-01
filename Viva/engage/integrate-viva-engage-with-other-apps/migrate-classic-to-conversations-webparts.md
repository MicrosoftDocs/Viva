---
title: "Migrate Classic Highlights to Viva Engage Conversations web part in SharePoint"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 08/01/2024
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
description: "Migrate your Highlights web parts (for Classic Yammer) to Viva Engage Conversations web parts on all of your modern SharePoint pages."
---

# Migrate Classic Highlights to Viva Engage Conversations web part in SharePoint

>[!NOTE]
>Starting January 31, 2025, Microsoft will retire and no longer support the Classic Highlights web part. To avoid a broken feed experience, we recommend that you replace all Classic Highlights web parts with the Viva Engage Conversations web part.

The Viva Engage Conversations web part let you add a Viva Engage conversation feed to a modern SharePoint site. (*Modern* refers to the online SharePoint experience available in Microsoft 365.) With Conversations web parts, you can:

- Add the feed from a community, user, or the home page
- Start a conversation with a topic or any type of Engage post
- Interact with conversations (react, reply, mention, and so on)

  To learn more about this functionality, see [Use a Viva Engage web part in SharePoint](https://support.microsoft.com/en-us/office/use-a-viva-engage-web-part-in-sharepoint-a53cfa0c-3d09-42c8-a286-1038a81c59da?ui=en-us&rs=en-us&ad=us).

## Migrate Classic Highlights web parts to the Conversations web part

Use this procedure to migrate all instances of the Classic Highlights web part, regardless of the type of feed you display (group, person, topic, or home). The migration process doesn’t affect Viva Engage data in any way.

1. On the SharePoint modern page, select **Edit** at the top of the page.

1. Hover over an existing web part or under the title region, select the plus icon, and select the Viva Engage Conversations web part.
    :::image type="content" source="../../media/engage/admin/conversations-web-part-sharepoint.png" alt-text="Screenshot shows the Viva Engage Conversations web part interface.":::

1. Select the conversation source that you used with the Classic Highlight web part.

    :::image type="content" source="../../media/engage/admin/conversations-web-part-pane.png" alt-text="Screenshot shows the radio buttons that let you specify different types of conversation feeds on your SharePoint page.":::

    - **Home Feed** displays the most recent conversations that appear on the **Home** page in Viva Engage. Select this if the Classic Highlights web part displayed the Viva Engage home feed. Turn off the publisher option if you don't want users in your organization to publish Engage posts from the web part.

    - **Community** displays the most recent conversations posted in the selected community. Select this option if the Classic Highlights web part displayed a **group feed**, and enter the community name. Choose the appropriate filter for the conversations you want to display in the web part. Turn off the publisher option if you don't want users in your organization to publish Engage posts from the web part.

 
    - **User** displays the most recent conversations in which the user participated. If the Classic Highlights web part displayed a specific person’s user feed, select this option and enter the user name.
 
    - **Topic** displays the most recent conversations tagged with this topic. Select this option if the Classic Highlights web part displays the feed for a topic, and enter the topic name.
 
1. In **Number of conversations to show**, select the number based on how much space the feed should use on the page.

    After you published the page, users can reply and follow the conversation from within your page. 

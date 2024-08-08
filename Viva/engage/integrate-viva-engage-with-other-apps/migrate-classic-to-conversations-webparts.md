---
title: "Migrate classic feeds in SharePoint to the Viva Engage Conversations web part"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 08/07/2024
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

The Viva Engage Conversations web part allows people to engage with each other on modern SharePoint without leaving the page. 

The Conversations web part is available only for the online SharePoint experience available in Microsoft 365. Learn more about [Viva Engage web parts](https://support.microsoft.com/en-us/office/use-a-viva-engage-web-part-in-sharepoint-a53cfa0c-3d09-42c8-a286-1038a81c59da?ui=en-us&rs=en-us&ad=us).

## Which version are you using?
 
1. Go to the SharePoint page that contains your Viva Engage feed and select **Edit** at the top of the page. 
1. Select the Viva Engage web part and then select **Edit** to open the web part menu.

    - If the menu includes a note stating that you’re using the classic version of Viva Engage, proceed to the next section to migrate your feed.
    - If the menu doesn't include a note, no action is required.

## Migrate classic Highlights web parts to the Conversations web part

Use this procedure to migrate all instances of the classic Highlights web part in SharePoint pages that you own or have permissions to. The migration process doesn’t affect Viva Engage data in any way.

1. **Open the existing classic feed on SharePoint**

    1. In SharePoint, select **Edit** at the top of the page.
    1. Select the classic Highlights web part that you want to replace and record the type of feed it's delivering to users (for example, user feed, community feed).


2. **Create a new feed using the Conversations web part**

    1. Hover above the classic Highlights web part where you want to create a new feed, and select the plus (+) icon.

        :::image type="content" source="../../media/engage/admin/hover-for-web-part-menu.png" alt-text="Screenshot shows how to access the web part menu.":::

    1. In the web part menu, select **Conversations**.

        :::image type="content" source="../../media/engage/admin/hover-menu-conversations-web-part.png" alt-text="Screenshot shows the option for creating a Conversations web part.":::

    1. Set up the Conversations web part to include settings you want to retain from your previous Highlights web part. Add new layout and background options from the panel on the right. For **Number of conversations to show**, select the number based on the allotted space you have for the feed.

        :::image type="content" source="../../media/engage/admin/web-parts-old-and-new.png" alt-text="Screenshot shows the Conversations menu where you specify the feed type, source, and other options.":::

    >[!NOTE]
    >For **Home** and **Community** feeds, turn off the publisher option if you don't want users in your organization to publish new Engage posts from the web part.

    - **Home Feed** displays the most recent conversations that appear on the **Home** page in Viva Engage. Select this if the classic Highlights web part displays the Viva Engage home feed. 

    - **Community** displays the most recent conversations posted in the selected community. Select this option if the classic Highlights web part displayed a **group feed**, and enter the community name. Choose the appropriate filter for the conversations you want to display in the web part.

    - **User** displays the most recent conversations in which the user participated. If the classic Highlights web part displays a specific person’s user feed, select this option and enter the user name.
 
    - **Topic** displays the most recent conversations tagged with this topic. Select this option if the classic Highlights web part displays the feed for a topic. Enter the topic name.

3. **Delete the old feed and publish the new one**
    1. To delete your previous classic feed, use the trash can icon at the top left edge of the feed.

    1. Select **Republish** on the top right corner to publish your changes.

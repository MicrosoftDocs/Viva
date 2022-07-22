---
title: "Use audience targeting in Viva Connections to personalize the experience"
ms.reviewer: 
ms.author: hokavian
author: Holland-ODSP
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-connections
localization_priority: Priority
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-connections
search.appverid:
- SPO160
- MET150
description: "Learn how to use audience targeting in Viva Connections to personalize the experience"
---

# Use audience targeting in Viva Connections to personalize the experience

Learn more about the ways audience targeting can be used to make sure the right audiences see the right content in [Viva Connections](viva-connections-overview.md). Audience targeting can be applied to the three components that make up Viva Connections – the Dashboard, the Feed, and the Resources.

> [!NOTE]
>
> - Audience targeting filters content but is not meant to manage permissions, access, or secure confidential content.
> - [Azure Active Directory groups](/microsoft-365/community/all-about-groups) (including security groups, Microsoft 365 groups, and AAD dynamic groups) are supported.
> - While in edit-mode, the author will be able to view all content. In read-mode, the content will be filtered based on the audiences selected.  
> - Publish (or republish) to save changes made to existing page content, page metadata, and audience targeting settings for audience targeting features to take effect.  
> - If you've selected an audience group that you recently created or changed, it may take some time to see targeting applied for that group.

## How audience targeting works for each component?

:::image type="content" source="../media/connections/vc-pivots.png" alt-text="Image of audience targeting":::

|Dashboard   |Feed  |Resources   |
|---------|---------|---------|
|Audience targeting can be applied to cards on the Dashboard.       |  Audience targeting can be applied to SharePoint news posts that display in the Feed.         |   Audience targeting can be applied to links that display in Resources.      |

## Apply audience targeting to cards in the Dashboard

Create a personalized experience by targeting Dashboard cards to specific audiences to ensure only the most relevant cards are seen. Use audience targeting to create custom views for distinct roles and regions, generate as many different views as needed to create unique experiences, and to ensure the most important content is seen by the intended audience. [Follow these instructions if you are setting up the Viva Connections Dashboard for the first time.](create-dashboard.md)

> [!NOTE]
> You must be a site owner of the [SharePoint home site](/sharepoint/home-site) to edit the Viva Connections Dashboard.

1. From the select the **Settings** and then select **Manage Viva Connections**.
2. Select **View Dashboard** and then select **Edit**.
3. Select **Edit** on the card you want to apply audience targeting to.

    :::image type="content" source="../media/connections/edit-card.png" alt-text="Image of edit card":::

4. At the bottom of the edit pane, apply [groups](/microsoft-365/community/all-about-groups) to the **Audience to target** field. Exit the edit pane when you are done.
5. Preview the viewing experience for different audiences and devices by selecting **Preview** from the command bar and then Select **audiences to preview as**. Make sure you preview the experience for each audience and on both desktop and mobile devices. 
<br>

**While in preview-mode, make sure:** 

- There aren’t any physical gaps between cards that may appear while previewing different audiences and devices. If you see gaps, rearrange cards so that every audience and device will have a high-quality viewing experience. 
- Icons, graphics, and images are easy to identify and understand. 
- Buttons and links are active and go to their intended destinations. 
- Labels and description text are helpful, easy to read, and make sense for the intended audience. 


6. **Republish** the Dashboard when you are done for the audience targeting to take effect.

    :::image type="content" source="../media/connections/card-targeted-audience.png" alt-text="Image of card targeted audience":::

## Apply audience targeting to news posts that will display in the Feed  

Apply audience targeting to [SharePoint news posts](https://support.microsoft.com/en-us/office/create-and-share-news-on-your-sharepoint-sites-495f8f1a-3bef-4045-b33a-55e5abe7aed7) helps surface individual news posts within the Feed. Content that displays in the Viva Connections Feed is aggregated from a few sources – posts from official organizational news sites, [news that has been boosted,](https://support.microsoft.com/en-us/office/boost-sharepoint-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83#:~:text=%20%20%201%20On%20your%20organization%20news,the%20order%20in%20which%20they%20should...%20More%20) and video news posts. [Learn more about how content is sourced and ranked in the Viva Connections Feed.](faqs-viva-connections-feed.md)

1. Start from the site where the news is published. Select **Settings**, then **Site contents**.

2. Select the library where the news post is located. select **Settings** again and then select **Library settings**.

3. Under G**eneral settings**, select **Audience targeting settings**. Then select the checkmark box next to **Enable audience targeting** and then select **OK**.

4. Next, navigate to the news post in **Site contents**. Select the news post you want to apply audiences to and select **Page details** from the command bar.  

5. In the panel that opens, apply [groups](/microsoft-365/community/all-about-groups) to the **Audience** field. Select **Save** when you are done and **Republish** the news post for the audience targeting to take effect.

    :::image type="content" source="../media/connections/apply-groups.png" alt-text="Image of apply groups to target audience":::

## Apply audience targeting to links in Resources  

Resources are the navigation links that display in the Resources tab in the mobile app and are inherited from the SharePoint global navigation. You can apply audience targeting to individual links for specific audiences. Global navigation can only be edited from the home site. [Follow these instructions first if you are setting up global navigation for the first time.](sharepoint-app-bar.md)  

> [!NOTE]
>
> - You must be a site owner of the [SharePoint home site](/sharepoint/home-site) to edit global navigation.
> - When audience targeting is applied to a parent link, audience targeting also gets applied to the sub-links.  
> - While editing the navigation, all links and sub-links become visible to the editor, including those that are targeted. When saved, the navigation shows the targeted nodes.

1. Go to your organization’s home site, select **Settings**, and then select **Global navigation**.

2. In the panel, under **Navigation source**, select **Edit global navigation**.  

3. Turn the **Enable site navigation audience targeting** toggle at the bottom of the global navigation pane to **On**.

4. Select the ellipses **(…)** next to each navigational link and select **Edit** from the dropdown.  

5. Apply up to 10 security groups to the **Audiences to target** field. Select **OK** when you are done.  

    :::image type="content" source="../media/connections/security-groups-target-audiences.png" alt-text="Image of security groups target audiences":::

6. When you are finished targeting links, select **Save** and **Republish** the home site for audience targeting to take effect.

### More resources

[Overview: Viva Connections](viva-connections-overview.md)

[Create the Viva Connections Dashboard](create-dashboard.md)  

[Frequently asked questions about the Feed for Viva Connections](faqs-viva-connections-feed.md)

[Set up global navigation in the SharePoint app bar](sharepoint-app-bar.md)  

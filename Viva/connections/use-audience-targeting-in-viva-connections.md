---
ms.date: 06/19/2023
title: "Use audience targeting in Viva Connections to personalize the experience"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Learn how to use audience targeting in Viva Connections to personalize the experience"
---

# Use audience targeting in Viva Connections to personalize the experience

Learn more about the ways audience targeting can be used to make sure the right audiences see the right content in [Viva Connections](viva-connections-overview.md). Audience targeting can be applied to the three components that make up Viva Connections – the dashboard, the Feed, and the Resources.

You can make sure that your content is seen by the right people by using audience targeting within your Viva Connections experience, which is detailed in this article. You can also create separate Viva Connections experiences for different audiences. [Learn about the difference between audience targeting and different experiences](set-up-admin-center.md#when-to-use-a-separate-experience-vs-dashboard-card-level-targeting).

> [!NOTE]
>
> - Audience targeting filters content but is not meant to manage permissions, access, or secure confidential content.
> - [Microsoft Entra groups](/microsoft-365/community/all-about-groups) (including security groups, Microsoft 365 groups, and Microsoft Entra dynamic groups) are supported.
> - While in edit-mode, the author will be able to view all content. In read-mode, the content will be filtered based on the audiences selected.  
> - Publish (or republish) to save changes made to existing page content, page metadata, and audience targeting settings for audience targeting features to take effect.  
> - If you've selected an audience group that you recently created or changed, it may take some time to see targeting applied for that group.

## How audience targeting works for each component

:::image type="content" source="../media/connections/vc-pivots.png" alt-text="Image of audience targeting":::

|Dashboard   |Feed  |Resources   |
|---------|---------|---------|
|Audience targeting can be applied to cards on the dashboard.       |  Audience targeting can be applied to SharePoint news posts that display in the Feed.         |   Audience targeting can be applied to links that display in Resources.      |

## Apply audience targeting to cards in the dashboard

Create a personalized experience by targeting dashboard cards to specific audiences to ensure only the most relevant cards are seen. Use audience targeting to create custom views for distinct roles and regions, generate as many different views as needed to create unique experiences, and to ensure the most important content is seen by the intended audience. [Follow these instructions if you're setting up the Viva Connections dashboard for the first time.](create-dashboard.md)

> [!NOTE]
> You must be a site owner of the [SharePoint home site](/sharepoint/home-site) to edit the Viva Connections dashboard.

1. From the select the **Settings** and then select **Manage Viva Connections**.
2. Select **View dashboard** and then select **Edit**.
3. Select **Edit** on the card you want to apply audience targeting to.

    :::image type="content" source="../media/connections/edit-card.png" alt-text="Image of edit card":::

4. At the bottom of the edit pane, apply [groups](/microsoft-365/community/all-about-groups) to the **Audience to target** field. Exit the edit pane when you're done.
5. Preview the viewing experience for different audiences and devices by selecting **Preview** from the command bar and then Select **audiences to preview as**. Make sure you preview the experience for each audience and on both desktop and mobile devices.
<br>

   **While in preview-mode, make sure:**

   - There aren’t any physical gaps between cards that may appear while previewing different audiences and devices. If you see gaps, rearrange cards so that every audience and device will have a high-quality viewing experience.
   - Icons, graphics, and images are easy to identify and understand.
   - Buttons and links are active and go to their intended destinations.
   - Labels and description text are helpful, easy to read, and make sense for the intended audience.

6. **Republish** the dashboard when you're done for the audience targeting to take effect.

    :::image type="content" source="../media/connections/card-targeted-audience.png" alt-text="Image of card targeted audience":::

## Apply audience targeting to news posts that will display in the feed  

Apply audience targeting to [SharePoint news posts](https://support.microsoft.com/office/create-and-share-news-on-your-sharepoint-sites-495f8f1a-3bef-4045-b33a-55e5abe7aed7) helps surface individual news posts within the Feed. Content that displays in the Viva Connections Feed is aggregated from a few sources – posts from official organizational news sites, [news that has been boosted,](https://support.microsoft.com/office/boost-sharepoint-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83#:~:text=%20%20%201%20On%20your%20organization%20news,the%20order%20in%20which%20they%20should...%20More%20) and video news posts. [Learn more about how content is sourced and ranked in the Viva Connections Feed.](faqs-viva-connections-feed.md)

1. Start from the site where the news is published. Select **Settings**, then **Site contents**.

2. Select the library where the news post is located. select **Settings** again and then select **Library settings**.

3. Under **General settings**, select **Audience targeting settings**. Then select the checkmark box next to **Enable audience targeting** and then select **OK**.

4. Next, navigate to the news post in **Site contents**. Select the news post you want to apply audiences to and select **Page details** from the command bar.  

5. In the panel that opens, apply [groups](/microsoft-365/community/all-about-groups) to the **Audience** field. Select **Save** when you're done and **Republish** the news post for the audience targeting to take effect.

    :::image type="content" source="../media/connections/apply-groups.png" alt-text="Image of apply groups to target audience":::

## Apply audience targeting to links in resources  

Resources are the navigation links that display beneath the dashboard. You can provide another level of customization to your Resource links by applying audience targeting. Resource links that have audience targeting applied will only appear to users who are part of the selected audience.

For example, an organization could use audience targeting to provide a set of resource links for users working in Human Resources that would only be seen by these employees.

1. Start by selecting **Edit** in the Resources section of your Connections experience.

2. Hover over the resource link and select the **ellipsis**.

3. Select **Edit**.

:::image type="content" source="../media/connections/edit-viva-home/atr-edit-resource.png" alt-text="Screenshot of the resource link drop-down menu with the edit option highlighted."lightbox="../media/connections/edit-viva-home/atr-edit-resource.png":::

4. Under **Audiences to target**, enter the M365 group(s) that you want to see the resource link. Up to 10 audiences can be targeted.

5. Select **Save**.

:::image type="content" source="../media/connections/edit-viva-home/atr-add-at-to-existing-resources.png" alt-text="Screenshot of the resource link properties menu with the audiences to target field highlighted."lightbox="../media/connections/edit-viva-home/atr-add-at-to-existing-resources.png":::

6. Links that have been targeted to specific audiences will display an audience targeting icon in the upper left of the resource link.

:::image type="content" source="../media/connections/edit-viva-home/atr-audience-targeting-icon.png" alt-text="Screenshot of the audience targeting icon shown in the upper left of the resource link."lightbox="../media/connections/edit-viva-home/atr-audience-targeting-icon.png":::

See [customizing resources](edit-viva-home.md#customize-resources) for more information.

### More resources

[Overview: Viva Connections](viva-connections-overview.md)

[Create the Viva Connections dashboard](create-dashboard.md)  

[Frequently asked questions about the Feed for Viva Connections](faqs-viva-connections-feed.md)

[Set up global navigation in the SharePoint app bar](sharepoint-app-bar.md)  

---
ms.date: 08/14/2024
title: "Viva Connections Feed Web Part and Video News link Retirement - Support Guidance"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Feed for Viva Connections Web Part and Video News link Retirement - Support Guidance"
---

# Feed for Viva Connections Web Part and Video News link Retirement - Support Guidance

## Overview

Microsoft regularly reviews our offerings to determine their effectiveness in our commitment to providing the most efficient and enjoyable experiences for our users. This evaluation led us to identify an abundance of content web parts currently available. Microsoft has decided to phase out the feed for Viva Connections web part and the video news link to concentrate our resources and improve user experience on core content web parts.

Microsoft will begin retiring the Feed for Viva Connections web part and the video news link feature starting September 1, 2024, and will be fully retired on November 5, 2024.

This article provides an overview of the feature and the deprecation timeline, its effect on customers, alternative solutions, and frequently asked questions.

## Feed for Viva Connections web part depreciation

### Feature overview

The Feed for Viva Connections web part is a feature that brought personalized content into a user's feed, in a single experience. This content included news published in SharePoint, posts in Viva Engage communities, and Stream videos in SharePoint.

![Screenshot with the company feed highlighted.](../media/connections/use-feed-web-part/feedwebpart_highlighted.png)

### Depreciation timeline

|**Date** |**Action** |**Impact to customers** |
|:--------|:----------|:----------|
|**September 1, 2024** | Microsoft removes the Feed for Viva Connections web part from the toolbox. <br><br> All existing instances of the feed for Viva Connections web part will continue to function. | Site owners won't see the feed for Viva Connections web part in the toolbox. New feed for Viva Connections web parts can't be added to a SharePoint site or SharePoint page.|
|**November 5, 2024** | Support for the feed for Viva Connections web part ends. <br><br> Site editors  need to replace the Feed for Viva Connections web part with the provided [alternative solutions](#alternative-solutions). | Any feed for Viva Connections web parts that haven't been replaced won't display content and visitors to the page will see an error message in place of the web part.|

## Video news link depreciation

### Feature overview

The [video news link](/viva/connections/video-news-links) allowed for Stream videos to appear in the Viva Connections feed.

![Image of how to add a new video news link to a news site.](../media/connections/add-video-link.png)

|**Date** |**Action** |**Impact to customers** |
|:--------|:----------|:----------|
|**September 1, 2024** | Microsoft removes the video news link from the **+ New menu** in SharePoint organizational sites. | Site editors won't be able to add new videos to be published in the Viva Connection feed. <br><br> Any videos scheduled to publish before November 5,2024 will still appear in the Viva Connections feed.|
|**November 5, 2024** | Support for the video news link ends. Videos published using the video news link won't appear on the Viva Connections feed. <br><br> Site editors need to replace video news links with the provided [alternative solutions](#alternative-solutions).| Any videos scheduled to publish after this date won't display. An error message on the Viva Connections feed will display to users.|

## Effect on Users

Microsoft will begin removing the Feed for Viva Connection web part from the toolbox starting **September 1, 2024**. After September 1, 2024, site editors won’t be able to add the web part to a site or page. Additionally, the video news link will be removed from the **+ New** menu in the SharePoint organizational site. Site editors and SharePoint admins won't be able to embed new video links to Viva Connections feed.

On **November 5, 2024**, support for the feed for Viva Connections web part and video news links will end.

Any feed for Viva Connections web parts that haven't been replaced with the recommended [alternative solutions](#alternative-solutions) will result in a feed web part that is empty and no longer displays content, including any video news links that haven't been removed. Visitors to the site will instead see an error message regarding the November 5 depreciation. This could lead to an interruption of service for users who rely on the feed for information and updates on SharePoint sites.

## Alternative Solutions

To continue surfacing feed content on Viva Connections, the following web parts provide an alternative to the feed for Viva Connections web part and the video news link.

### Alternative solution to featuring news posts in SharePoint

- **News web part** - Allows you to display a collection of news posts from various SharePoint sources. For more information, see [Use the News web part on a SharePoint page](https://support.microsoft.com/office/c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_sitenews).

### Alternative solution for featuring Viva Engage in SharePoint

- **Viva Engage web parts** – Allow you to display the Viva Engage conversations and highlights to SharePoint. For more information, see [Use a Viva Engage web part in SharePoint](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da#highlights).

### Alternative solutions for featuring Stream videos in SharePoint and videos hosted on a SharePoint site

- **File and media web part** – Allows you to feature a single video on a SharePoint page. For more information, see [Featuring a video on a page](/stream/streamnew/portals-single-video).

- **Highlighted content web part** – Allows you to feature a list of videos on a page. For more information, see [Featuring a set of videos on a page](/stream/streamnew/portals-set-of-videos).

- **Video Pages** – Allows you to create video centric page content with a page template. For more information, see [Create video pages on SharePoint](https://support.microsoft.com/office/7823449f-e2cc-48d2-bda7-2ee82518958a).

## Action Items for Site owners and SharePoint admins

1. This change will automatically occur by the specified date.

2. Site editors and SharePoint admins should plan for the retirement and update and/or replace the affected SharePoint sites with the recommended alternatives.

3. Site editors and SharePoint admins should notify users about this change and update any relevant documentation.

## Frequently Asked Questions

**Will the Viva Connections Feed in Desktop or Mobile experience be impacted by this deprecation?**

The Viva Connections Feed in Desktop and Mobile experiences won't be impacted with this deprecation. This depreciation will only affect the Feed for Viva Connections web part.

**How do I find the sites that have the Feed for Viva Connections web part configured?**

- **Option 1**:
  1. Navigate to your organization’s SharePoint root site.

  2. Search for the web part ID `d0a64d22-555c-44e4-b120-aed62c263632` in the search bar (*Search results are limited to the current user's permission scope*).

- **Option 2**:

    Consider using the [script in this article](/stream/streamnew/webpart-transition#how-do-i-find-the-location-for-videos-embedded-in-stream-classic-web-part) that was shared by users who have successfully used it to find the location of videos embedded in Stream Classic. It serves as a template that can be customized to align with your unique requirements and context.


## Learn more

[Use the News web part on a SharePoint page](https://support.microsoft.com/office/c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_sitenews)

[Use a Viva Engage web part in SharePoint](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da#highlights)

[Featuring a video on a page](/stream/streamnew/portals-single-video)

[Featuring a set of videos on a page](/stream/streamnew/portals-set-of-videos)

[Create video pages on SharePoint](https://support.microsoft.com/office/7823449f-e2cc-48d2-bda7-2ee82518958a)

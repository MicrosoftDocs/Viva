---
ms.date: 09/22/2023
title: "Create a SharePoint home site for Viva Connections"
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
description: "Create a SharePoint home site for Viva Connections"
---

# Create a SharePoint home site for Viva Connections

Use this guided walkthrough if you're creating a SharePoint home site so your organization can use Viva Connections. Get guidance on how to create a cohesive experience between the desktop and mobile apps. Before you start, learn more about [planning SharePoint home site content](home-site-plan.md) and [how to launch a healthy portal](/sharepoint/portal-health).

Don’t have time to create a SharePoint home site from scratch? Consider using [the Landing site template from the SharePoint look book](https://adoption.microsoft.com/sharepoint-look-book/) and then add the [Dashboard web part](use-dashboard-web-part-on-home-site.md) and the [Feed web part](use-feed-web-part-for-viva-connections.md).

[Learn more about how Viva Connections and SharePoint home sites work together to create employee experiences.](viva-connections-overview.md#how-sharepoint-home-sites-and-viva-connections-work-together)

> [!NOTE]
>
> SharePoint home sites are created and managed in your Microsoft 365 admin center. You'll need to be a SharePoint admin to create a home site.
> A home site is not required to create a [Viva Connections experience](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/new-experiences-for-viva-connections-are-now-rolling-out/ba-p/3729071).
> [Learn more about the Viva Connections experience](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/more-options-coming-soon-for-the-viva-connections-desktop/ba-p/3644419), [how to customize it](edit-viva-home.md), how to choose the default landing experience, and [how to onboard new users](https://support.microsoft.com/office/see-what-you-can-do-in-the-viva-connections-desktop-experience-e1f53887-f3cc-4ec4-bdbd-2e2f673089b6).

## How to use this guide

The web parts used here pair well with SharePoint home sites, however web parts can be swapped or left out. Decide what is best for your organization and adjust the layout as needed.

The guidance here will help you design the SharePoint home site and customize web parts, but you'll need to provide your own content.

A SharePoint home site needs site navigation that is organized well, highlights popular resources and portals, and is relevant to the entire organization. This design guidance doesn't specifically talk about how to design site navigation. Get more guidance on [how to think about links in SharePoint home site navigation](/sharepoint/information-architecture-models-examples) and [in the global navigation](sharepoint-app-bar.md).

## Summary of web parts

> [!NOTE]
>
> Starting **September 1, 2024**, the feed for Viva Connection web part and the video news link will be removed and unavailable for SharePoint site editors to add to their sites. On **November 5, 2024**, support for the feed for Viva Connections web part and video news links will end and no longer display content.
>
> Site owners are encouraged to use the [News](https://support.microsoft.com/office/c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_sitenews), [Viva Engage](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da#highlights), [File and Media](/stream/streamnew/portals-single-video), and [Highlighted content](/stream/streamnew/portals-set-of-videos) web parts, and [Video pages](https://support.microsoft.com/office/7823449f-e2cc-48d2-bda7-2ee82518958a) as alternatives to using the feed for Viva Connections web part and the video news link. For more information, refer to the [Viva Connections Feed web part retirement support guidance documentation](feed-web-part-video-news-link-retirement.md).

|Image of the SharePoint home site  |Web parts key  |
|:---------|:---------|
|:::image type="content" source="../media/connections/vc-home-site-design-60.png" alt-text="SharePoint home site" lightbox="../media/connections/vc-home-site-design.png" border="false":::    |<ol><li>Hero web part</li><li>World clock web part</li><li>Weather web part</li><li>Feed for Viva Connections web part</li><li>Dashboard web part</li><li>Image web part</li><li>File viewer web part</li><li>Events web part</li><li>Quick Links web part</li><li>Quick Links web part</li><li>News web part</li><li>Quick Links web part</li><li>Call to action web part</li></ol>|

## Summary of the site structure

This SharePoint home site design uses a vertical section and a combination of one and two column sections. After [creating your communication site](https://support.microsoft.com/office/create-a-communication-site-in-sharepoint-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb), start by [laying out the sections](https://support.microsoft.com/office/add-sections-and-columns-on-a-sharepoint-modern-page-fc491eb4-f733-4825-8fe2-e1ed80bd0899) before adding web parts.  

:::image type="content" source="../media/connections/home-site-structure-2.png" alt-text="SharePoint home site design" border="false":::

## Build the site

Start with a [modern SharePoint communication site](https://support.microsoft.com/office/create-a-communication-site-in-sharepoint-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb). Next, [start adding sections](https://support.microsoft.com/office/add-sections-and-columns-on-a-sharepoint-modern-page-fc491eb4-f733-4825-8fe2-e1ed80bd0899) following the diagram in the site sections summary. Then, add and edit web parts. The guidance for customizing web parts can be applied when you are in edit mode for each web part.

:::image type="content" source="../media/connections/home-site-top.png" alt-text="Build SharePoint home site top section" border="false":::

|Number  |Web part  |Customization guidance  |
|---------|---------|---------|
|1    | [Hero web part](https://support.microsoft.com/office/use-the-hero-web-part-d57f449b-19a0-4b0d-8ce3-be5866430645)| Select **Tiles layout** and then **Four tiles**. |
|2    | [World clock web part](https://support.microsoft.com/office/use-the-world-clock-web-part-aa2ede87-e331-44f1-a116-a5b8fc67fd04)| Toggle the **Show days of the week** to **On**. |
|3     | [Weather web part](https://support.microsoft.com/office/show-the-weather-on-your-page-4a86540e-0846-4fc0-bad0-1a82fcd430fc)        |Decide which temperate measurement system makes the most sense for your audience between **Fahrenheit** and **Celsius**.|
|4  | [The Feed for Viva Connections](use-feed-web-part-for-viva-connections.md) | No settings needed. The [Feed content is personalized](faqs-viva-connections-feed.md) for each user and comes from SharePoint News and Viva Engage communities that they follow.  |
|5  | [The Dashboard web part](use-dashboard-web-part-on-home-site.md)| Set the **Maximum number of cards to show** to 9.|

:::image type="content" source="../media/connections/home-site-middle.png" alt-text="Build SharePoint home site middle section" border="false":::

| Number| Web part|Customization guidance|
|---|---|---|
| 6 | Image web part|Toggle **Add text over image** to **On**.|
| 7 | File viewer web part | No settings guidance. |
| 8 | Events web part | Select the **Filmstrip** layout and toggle **Show event images** to **On**. |

:::image type="content" source="../media/connections/home-site-bottom.png" alt-text="Build SharePoint home site bottom section" border="false":::

| Number |  Web part       |  Customization guidance |
|:---|:---|:---|
| 9  | Quick Links web part   | Select the **Compact** layout and then toggle **Show image in layout** to **Yes**.|
| 10 | Quick Links web part    | Select the **List** layout and toggle **Show descriptions** and **Show icons** to **Yes**.|
| 11 | News web part     | Select the **Side-by-side** layout, set the **Number of news posts to show** to 4. Then toggle **Show number of views**, **Show author**, and **Show publish date** to **On**. |
|  12 | Quick Links web part     |  Select the **Grid** layout.|
|  13 | Call to action web part     |  No settings guidance. |

## Customize site details

After the site is built, edit site details to create a customized design that aligns with your organization's brand and identity. These [site details can be managed](https://support.microsoft.com/office/customize-your-sharepoint-site-320b43e5-b047-4fda-8381-f61e8ac7f59b) from **Settings** > **Change the look**.

- **Theme** – Select a theme that is ideal for the entire organization. If you make your SharePoint home site [a hub site](/sharepoint/dev/features/hub-site/hub-site-overview), this theme will get passed down to sites that associate with the hub.
- **Header** – Use the Compact header layout to reproduce the same look as your SharePoint home site.
- **Logo** – Select a logo that is recognizable to the entire organization.
- **Footer** – Footer navigation is optional and can be used to highlight popular portals and resources.

## Extensibility

Use the [SharePoint Framework](/sharepoint/dev/spfx/sharepoint-framework-overview) (SPFx) to create [customized components like web parts](/sharepoint/dev/spfx/web-parts/overview-client-side-web-parts) and [Viva Connections Dashboard cards](/sharepoint/dev/spfx/viva/design/design-intro) that can be surfaced on a SharePoint home site and throughout the Viva Connections experience. The SPFx is the only extensibility and customization option for Viva Connections. [Learn more about Viva Connections extensibility](/sharepoint/dev/spfx/viva/overview-viva-connections).

## Best practices before launching your new SharePoint home site

- A SharePoint home site is used by the entire organization, so the site needs to be [inclusive and easily accessible on all devices](https://support.microsoft.com/office/get-ready-build-an-accessible-sharepoint-site-3a1df3ad-f093-450c-85a6-b3bf70fd6abb) and potentially [needs to be viewed in other languages](https://support.microsoft.com/office/create-multilingual-communication-sites-pages-and-news-2bb7d610-5453-41c6-a0e8-6f40b3ed750c).

- The SharePoint home site will be viewed by a high volume of users. Make sure you [manage site performance](/sharepoint/portal-health) through the planning and building phases.

- Before launching the SharePoint home site broadly, test the site with a handful of users to make sure key tasks and resources are readily accessible and fully functioning. 

- Consider using the [Portal launch scheduler](/microsoft-365/enterprise/portallaunchscheduler) to help you follow a phased roll-out approach by batching viewers in waves and managing the URL redirects for the new portal.

## Next: Enable and set up global navigation

Once you’ve set a communication site as a SharePoint home site, you'll be able to [enable and set up global navigation in the SharePoint app bar](sharepoint-app-bar.md). Global navigation can be set up while you're designing your SharePoint home site and is a requirement for Viva Connections. Resources highlighted in the global navigation [will appear in the “Resources” tab in the Viva Connections mobile app](viva-connections-overview.md).

## Learn more

[Plan, build, and launch a SharePoint home site for your organization](home-site-plan.md)

[Creating and launching a healthy SharePoint portal](/sharepoint/portal-health)

[Plan, build, and launch Microsoft Viva Connections for your organization](plan-viva-connections.md)

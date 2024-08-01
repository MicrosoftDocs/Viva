---
ms.date: 11/30/2023
title: "Plan, build, and launch a home site for your organization"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
recommendations: true
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
ms.localizationpriority: medium
ms.collection:
  - Strat_SP_admin
  - M365-collaboration
  - m365solution-scenario
  - m365solution-spintranet
  - m365initiative-viva-connections  F
  - Tier1
ms.custom:
- seo-marvel-apr2020
search.appverid:
- SPO160
- MET150
- BSA160
description: "Learn about how to plan, build, and launch the main landing site for your organization."
---

# Plan, build, and launch a SharePoint home site for your organization
  
A SharePoint home site provides a customized landing experience that reflects the organization’s brand, voice, and priorities. A SharePoint home site also serves as the gateway to other portals in your organization’s intranet. [Learn more about how Viva Connections and SharePoint home sites work together to create employee experiences.](viva-connections-overview.md#how-sharepoint-home-sites-and-viva-connections-work-together)

> [!NOTE]
>
> - A SharePoint home site is not required the Viva Connections desktop, mobile, or tablet experience. [Learn more about Viva Connections experience](set-up-admin-center.md), [how to customize it](edit-viva-home.md), how to choose the default landing experience, and [how to onboard new users](https://support.microsoft.com/office/access-and-use-the-viva-connections-app-in-microsoft-teams-8b4e7f76-f305-49a9-b6d2-09378476f95b).
> - The ability to set a home site has moved from the SharePoint Admin Center (SPAC) to the Viva Connections admin center.
> - You must have an Enterprise (E) or Frontline (F) license type to create a Viva Connections experience. Users with a basic Microsoft 365 subscription (E license) are limited to creating one experience. Users are required to have a Microsoft Viva suite or Viva Communications and Communities license in order to create two or more experiences (up to 50). See [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) for more info.
> - Viva Connections does not have any requirements to get started.
> - You must have SharePoint admin permissions to access the Microsoft 365 admin center.
If you’ve already created the communication site and are ready to specify it as your home site now, learn how to [set up Viva Connections in the Microsoft 365 admin center](set-up-admin-center.md).

**Use a SharePoint home site to:**

- Provide a gateway to other high-traffic portals.
- Connect people with an intranet-wide search experience.
- Showcase targeted news and content.
- Take advantage of the new people engagement tool, [Viva Connections](create-sharepoint-home-site-for-viva-connections.md).

|Example of a SharePoint home site:    |View in the SharePoint mobile app:   |
|---------|---------|
|:::image type="content" alt-text="Screenshot of a SharePoint home site as an example." source="../media/connections/home-site-example-3.png":::     | :::image type="content" alt-text="Screenshot of a SharePoint app viewing a SharePoint home site." source="../media/connections/home-site-fre-3.png":::        |

## What is a SharePoint home site?

Users are able to create multiple SharePoint home sites tied to multiple Viva Connection experiences that can take advantage of home site features. SharePoint home sites don't replace communication or team sites, but instead provide a landing place for your organization. Think of SharePoint home sites as an *add-on* to your intranet design. SharePoint home sites are communication sites that have special capabilities such as being marked as an official source of news in the organization. Consider making your tenant's root site the SharePoint home site. Next, review key differences between standard SharePoint communication sites and SharePoint home sites.

Creating a SharePoint home site so your organization can use Viva Connections? [Consider following this design guidance.](create-sharepoint-home-site-for-viva-connections.md)

**SharePoint home site features explained:**

SharePoint home sites are unlike any other site in SharePoint. When you set a SharePoint communication site as a home site, you’ll automatically apply special capabilities that make the SharePoint home site an ideal landing destination for your intelligent intranet.

### Use Viva Connections to integrate your intranet into Microsoft Teams

Viva Connections is designed to drive engagement, build community, and enable your organization to stay connected. You can create a Viva Connections experience as a standalone experience or take advantage of your intranet home site to provide a more holistic experience that uses existing content. Learn more about [Creating a new Viva Connections experience](/viva/connections/set-up-admin-center#create-a-new-viva-connections-experience).

### Search for content across the entire intranet

SharePoint home sites allow users to search for content (such as sites, news, and files) across the entire intranet rather than searching just the site like typical SharePoint sites. This becomes possible because the search scope for the SharePoint home site searches the entire intranet instead of just the site collection like a typical site.

### Official source of organizational news  

By default, a SharePoint home site is set as the organizational news source. News posts that are created from the SharePoint home site automatically become official organizational news and take priority on the [SharePoint start page](https://support.microsoft.com/office/discover-content-with-the-sharepoint-start-page-6b85097a-87e0-4611-a29a-dfd49b1a1220) and in the home section of the SharePoint mobile app. Administrators can [set sites as official organizations news sources in the admin center](/sharepoint/organization-news-site).

### Enable and customize global navigation in the SharePoint app bar

The SharePoint app bar features a global navigation option that displays intranet navigational nodes and resources no matter where users are in SharePoint. To take full advantage of this feature, you must have a SharePoint home site. Learn more about how to [enable and customize global navigation in the SharePoint app bar](/SharePoint/sharepoint-app-bar).

## Before getting started

Before you get started planning and building your SharePoint home site, review best practices and considerations.

### Best practices for creating SharePoint home sites

- Because a SharePoint home site is used by the entire organization, the site needs to be [inclusive and easily accessible on all devices](https://support.microsoft.com/topic/get-ready-build-an-accessible-sharepoint-site-3a1df3ad-f093-450c-85a6-b3bf70fd6abb).
- Because the site needs to be inclusive and easily accessible on all devices, [consider other languages that might be needed](https://support.microsoft.com/office/create-multilingual-communication-sites-pages-and-news-2bb7d610-5453-41c6-a0e8-6f40b3ed750c).
- The SharePoint home site will be viewed by a high volume of users. Make sure you [manage site performance](/sharepoint/portal-health) through the planning and building phases.
- Links in the SharePoint home site's navigation can direct users to content in addition to [global navigation](/sharepoint/sharepoint-app-bar), which can be used to lead users to universally used resources and portals.
- Make sure the SharePoint home site is discoverable by [adding an entry point to the Microsoft 365 app launcher](/microsoft-365/admin/manage/customize-the-app-launcher) and a [featured link on the SharePoint start page](/sharepoint/change-links-list-on-sharepoint-home-page).
- [News published from the SharePoint home site](https://support.microsoft.com/office/create-and-share-news-on-your-sharepoint-sites-495f8f1a-3bef-4045-b33a-55e5abe7aed7) should be relevant to the entire organization.

### Considerations

- Align the branding on the SharePoint home site to the overall intranet brand where possible.
- For organizations with many portals and resources, consider [making your SharePoint home site a hub site](/sharepoint/planning-hub-sites) to expand navigational options and easily sync permissions and branding across many sites.
- Use a SharePoint home site template from the SharePoint look book called [The Landing](https://adoption.microsoft.com/sharepoint-look-book/) to jump-start the design process.

## Summary of how to get a SharePoint home site for your organization

Since SharePoint home sites are the gateway to your intranet, you’ll want to prioritize content and resources that are relevant to most employees. Work with business owners and stakeholders to organize and align the flow of information and the navigational design. Then, use the [Page diagnostics for SharePoint tool](/microsoft-365/Enterprise/page-diagnostics-for-spo) to ensure to best viewing experience. Next, [set your SharePoint communication site as a home site](/SharePoint/home-site) in the SharePoint admin center. Finally, use the [Portal launch scheduler](/microsoft-365/enterprise/portallaunchscheduler) to plan the launch of your new site and make the site discoverable by adding links to key entry-points in the Microsoft 365 experience.

Before you get started planning your SharePoint home site, [hear from the Microsoft product team on how to think](https://techcommunity.microsoft.com/t5/video-hub/build-and-launch-a-sharepoint-home-site-tips-and-tricks-from-the/m-p/1696758) about and approach the design of your organization’s SharePoint home site.


| Plan                  | Build                | Launch and manage          |
| :------------------- | :------------------- |:----------------|
| - Align objectives with partners and business owners <br> - Organize priority content <br> - Design way finding for the SharePoint home site and global navigation <br> - Think about branding <br> - Use audience targeting on navigational links, news, and web parts| - Upload and organize site assets and content like files and logos (64x64px). <br> - Customize the site to align with the rest of the intranet <br> - Apply audience targeting <br> - Turn on a content approval flow <br> - Use PowerShell to turn the SharePoint comm site into a home site <br> - Swap the root site location with the SharePoint home site <br> - Measure site health and performance <br> - Test on all devices| - Share the site with your organization <br> - Use the Portal launch scheduler to release the new site in phases <br> - Make the SharePoint home site discoverable <br> - Announce the launch of the SharePoint home site using various communication channels <br> - Monitor site usage and analytics |

### Plan your SharePoint home site

A great SharePoint home site starts with a plan. Because your SharePoint home site is essentially the gateway to your intranet, you'll want to collaborate with other business owners such as human resources, leadership teams, and even your legal team to ensure the most important and universal resources are accessible for everyone in the organization.

|  Icon                 | Action        | Get started          |
| :------------------: | :------------------: |:----------------|
|  ![Screenshot of a sign](../media/connections/icon-plan-organize.png)   | **Get organized** | Start by aligning objectives with stakeholders and organizing priority content and resources. Consider details specific to your organization like if the SharePoint home page needs to be available in more than one language. Use modern SharePoint sites for the home site. Learn more about how [modern SharePoint sites](https://support.microsoft.com/office/sharepoint-classic-and-modern-experiences-5725c103-505d-4a6e-9350-300d3ec7d73f) and how to [create a multi-lingual site and pages](https://support.microsoft.com/office/create-multilingual-communication-sites-pages-and-news-2bb7d610-5453-41c6-a0e8-6f40b3ed750c). |
| ![Screenshot of a compass](../media/connections/icon-plan-nav.png)                 | **Plan navigation**                 | Then, organize the navigational structure for the SharePoint home site itself and global navigation. Consider making the SharePoint home site a hub site if you need to add an extra layer of navigation and make it easier to sync associated site permissions and branding. Learn more about [planning site navigation](/sharepoint/plan-implement-navigation-design) and how to [make your SharePoint home site a hub site](/sharepoint/planning-hub-sites). Then, review guidance on how to [set up global navigation on the SharePoint home site](/SharePoint/sharepoint-app-bar).|
| ![Screenshot of a user](../media/connections/icon-plan-gather.png)                | **Personalize content**                 | Next, think about the different audiences that your organization serves. Consider how elements on your SharePoint home site like navigational links and certain web parts could benefit from audience targeting to specific audiences. Learn more about [audience targeting](https://support.microsoft.com/office/change-the-look-of-your-sharepoint-site-06bbadc3-6b04-4a60-9d14-894f6a170818?ui=en-us&rs=en-us&ad=us). |
| ![Screenshot of a file](../media/connections/marketing-materials-icon.png)                   | **Gather branding assets**                   | Finally, start gathering assets needed to apply custom branding and other details to your SharePoint home site, like logo files (64x64px recommended), color themes, and any custom solutions. Learn more about how to [change the look of your site](https://support.microsoft.com/office/change-the-look-of-your-sharepoint-site-06bbadc3-6b04-4a60-9d14-894f6a170818?ui=en-us&rs=en-us&ad=us). |
| ![Screenshot of a chart](../media/connections/icon-plan-perf.png)                   | **Consider site performance**                   | Even before you build your site, understand the main elements that will make sure your SharePoint home site is healthy. A healthy SharePoint home site optimizes performance to ensure the best possible viewing experience. Use the Page diagnostics for SharePoint tool to make sure the SharePoint home page is healthy before sharing with end users. Learn more about [healthy portals](/sharepoint/portal-health) and using the [Page diagnostics tool for SharePoint](/microsoft-365/enterprise/page-diagnostics-for-spo). |

### Build your SharePoint home site

When you've prepared a plan, you're ready to start creating the home site in SharePoint. Start with a communication site, and after you have the general layout finalized, create a [Viva Connections experience from your existing SharePoint home site](/viva/connections/set-up-admin-center#build-from-an-existing-intranet-portal) in the Viva Connections admin center.

> [!NOTE]
>
> Starting **September 1, 2024**, the feed for Viva Connection web part and the video news link will be removed and unavailable for SharePoint site editors to add to their sites. On **November 5, 2024**, support for the feed for Viva Connections web part and video news links will end and no longer display content.
>
> Site owners are encouraged to use the [News](https://support.microsoft.com/office/c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_sitenews), [Viva Engage](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da#highlights), [File and Media](/stream/streamnew/portals-single-video), and [Highlighted content](/stream/streamnew/portals-set-of-videos) web parts, and [Video pages](https://support.microsoft.com/office/7823449f-e2cc-48d2-bda7-2ee82518958a) as alternatives to using the feed for Viva Connections web part and the video news link. For more information, refer to the [Viva Connections Feed web part retirement support guidance documentation](feed-web-part-video-news-link-retirement.md).

|  Icon                 | Action        | Get started           |
| :------------------: | :------------------: |:----------------|
|:::image type="content" source="../media/connections/icon-plan.png" alt-text="Screenshot of a clipboard ":::  | **Create a modern communication site** | Start by creating a SharePoint communication site and build out the site by using sections, web parts, and pages. Consider using a mega menu and footer to enhance way finding. Web parts that are useful for a SharePoint home site include: News web part, My feed web part, Viva Engage web parts, Quick link web part, and the Highlighted content web part. Learn how to [create a communication site](https://support.microsoft.com/office/create-a-communication-site-in-sharepoint-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb#:~:text=Steps%20to%20create%20a%20communication%20site%201%20Sign,news%2C%20events%2C%20and%20other%20content.%20...%20See%20More.), use [modern web parts](https://support.microsoft.com/office/using-web-parts-on-sharepoint-pages-336e8e92-3e2d-4298-ae01-d404bbe751e0), and [customize your site](https://support.microsoft.com/office/customize-your-sharepoint-site-320b43e5-b047-4fda-8381-f61e8ac7f59b#:~:text=Customize%20your%20SharePoint%20site.%201%20Change%20the%20logo.,navigation.%205%20Add%20a%20site%20footer.%20See%20More.). |
| ![Screenshot of an audience](../media/connections/icon-build-audience.png)   | **Apply audience targeting**| Next, turn on audience targeting on for the SharePoint home site. By enabling audience targeting, specific content will be prioritized to specific audiences in navigational links, news, and certain web parts. Learn more about [how audience targeting works](https://support.microsoft.com/office/target-content-to-a-specific-audience-on-a-sharepoint-site-68113d1b-be99-4d4c-a61c-73b087f48a81) and [how to apply it](https://support.microsoft.com/office/target-navigation-news-and-files-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293) to navigational links, news, and web parts.|
| ![Screenshot of a site](../media/connections/icon-build-flow.png)   | **Set up a page approval flow** | Then, make sure the SharePoint home site is set up for regular content updates. Turn on content approval to ensure only high-quality content is published on the SharePoint home site. Learn how to [turn on a page approval flow](https://support.microsoft.com/office/approval-flow-for-modern-pages-a8b2e689-d4a1-4639-8028-333c0ece30d9?ui=en-us&rs=en-us&ad=us).|
| ![Screenshot of a two sites getting switched](../media/connections/icon-build-swap.png)   | **Swap the root site location with the SharePoint home site**  | Before you set a communication site as the SharePoint home site, swap the communication site in place of the root site of your tenant as a best practice. The root site for your organization is one of the sites that's provisioned automatically when you purchase and set up a Microsoft 365 plan. If you set up a SharePoint home site first, and then swap locations with your root site, you may lose SharePoint home site settings and need to reapply them. Learn how to [swap the root site with the SharePoint home site](/sharepoint/modern-root-site#replace-your-root-site).|
| ![Screenshot of a house](../media/connections/icon-build-home.png)   | **Set the SharePoint home site** | Next, [build a Viva Connections experience from an existing intranet portal](/viva/connections/set-up-admin-center#build-from-an-existing-intranet-portal).|
| ![Screenshot of a map](../media/connections/icon-build-global.png)   | **Set up global navigation** | Then, enable global navigation to allow users to easily navigate to important intranet resources anywhere in SharePoint. Global navigation can only be customized from the SharePoint home site’s home page. Learn how to [enable and customize global navigation](/SharePoint/sharepoint-app-bar).|
| ![Screenshot of an approved site](../media/connections/icon-build-test.png)   | **Test site health and the viewing experience**  | Finally, review portal launch guidance and understand the main elements that will make sure your SharePoint home site is healthy. A healthy SharePoint home site optimizes performance to ensure the best possible viewing experience. Use the Page diagnostics for SharePoint tool to make sure the SharePoint home page is healthy before sharing with end users. Learn more about [healthy portals](/sharepoint/portal-health) and using the [Page diagnostics tool for SharePoint](/microsoft-365/enterprise/page-diagnostics-for-spo).|

### Launch your SharePoint home site

After you've set your SharePoint home site, it’s time to plan the launch and make sure the rest of the organization can find and use the SharePoint home site.

|  Icon                 | Action        | Get started          |
| :------------------: | :------------------: |:----------------|
|  ![Screenshot of a sharing a site with users](../media/connections/icon-launch-add.png)   | **Share the site and schedule the portal launch** | Start by ensuring your SharePoint home site is healthy, and then its time to share the site with the rest of the organization and schedule the launch. Use the Portal launch scheduler tool to gradually roll out the SharePoint home site to batches of end users. Using a phased approach is ideal to manage any performance issues that may arise and to ensure a positive viewing experience. Learn how about how to use the [Portal launch scheduler tool](/microsoft-365/enterprise/portallaunchscheduler). |
| ![Screenshot of a magnify glass](../media/connections/icon-launch-search.png)   | **Improve discoverability**| Next, make sure people in your organization can easily find the SharePoint home site through a few different entry points in the Microsoft 365 experience. Add a link to the SharePoint home site in the Microsoft app launcher (sometimes called the waffle) and on the SharePoint start page. Learn more about how to [add a custom tile to the app launcher](/microsoft-365/admin/manage/customize-the-app-launcher) and how to [add a featured link to the SharePoint start page](/sharepoint/change-links-list-on-sharepoint-home-page).|
| ![Screenshot of a mega phone](../media/connections/icon-launch-engage.png)   | **Engage your audience** | Then, let your organization know about the new SharePoint home site resource, and other new elements like global navigation. Consider multiple communication options like a SharePoint news post that can also be shared in email and in Microsoft Teams. Learn more about how to [create and post SharePoint news](https://support.microsoft.com/office/create-and-share-news-on-your-sharepoint-sites-495f8f1a-3bef-4045-b33a-55e5abe7aed7) and [share it in an email](https://support.microsoft.com/office/use-the-news-web-part-on-a-sharepoint-page-c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_send).|
| ![Screenshot of a usage report](../media/connections/icon-launch-manage.png)   | **Manage and maintain your SharePoint home site** | Finally, when the site is healthy, launched, and being used by the organization, monitor site usage and maintain the site. Site maintenance should include making sure site content is relevant, there aren’t any broken links, and that the site stays healthy and performant. Learn how to [view usage data and analytics](https://support.microsoft.com/office/view-usage-data-for-your-sharepoint-site-2fa8ddc2-c4b3-4268-8d26-a772dc55779e) for your site and how to [maintain your site over time](https://support.microsoft.com/office/manage-your-sharepoint-communication-site-21761aac-f7f7-4499-b0ca-cf283477c32f).|
| ![Screenshot of a globe and monitor](../media/connections/icon-launch-viva.png)   | **Integrate the SharePoint home site into Microsoft Teams using Viva Connections** | Expand the reach of the SharePoint home site and help meet users where they're already working by making it easy to access and share content all in one place. After you have a SharePoint home site and the global navigation enabled and customized in the SharePoint app bar, you’ve met the requirements to [integrate the SharePoint home site into Microsoft Teams](/viva/connections/add-viva-connections-app) using Viva Connections. Learn more about the [Viva Connections end-user experience](https://support.microsoft.com/office/your-intranet-is-now-in-microsoft-teams-8b4e7f76-f305-49a9-b6d2-09378476f95b).|

## SharePoint home site FAQs

**Q:** Are SharePoint home sites now set in the Microsoft admin center?
<br>
Starting in June 2023, use the Microsoft admin center to [set a SharePoint home site when you create a Viva Connections experience](set-up-admin-center.md).

**Q:** What’s the difference between a SharePoint home site and the SharePoint start page?
<br>
The content on the [SharePoint start page](https://support.microsoft.com/office/discover-content-with-the-sharepoint-start-page-6b85097a-87e0-4611-a29a-dfd49b1a1220) is driven and managed by [Microsoft Graph](/graph/overview#whats-in-microsoft-graph). Content is personalized to the individual users’ recent activity, followed sites, and content that is saved for later. The SharePoint home site is a landing experience for your entire organization. It displays universally relevant content and directs users to other important portals like Human Resources and company directories.

**Q:** Can I integrate the SharePoint start page with my SharePoint home site?
<br>
Integration between the SharePoint home site and [SharePoint start page](https://support.office.com/article/6b85097a-87e0-4611-a29a-dfd49b1a1220) (where the branding, theming, header, navigation, and footer elements from the SharePoint home site are applied to the start page and users can easily navigate between the pages) isn't available at this time. However you can [add a featured link to the SharePoint start page](/sharepoint/change-links-list-on-sharepoint-home-page) to increase SharePoint home site discovery.

Watch for updates in the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=SharePoint).

## Resources

**Watch:** [Build and launch a SharePoint Home Site: Tips and Tricks From The Product Team](https://techcommunity.microsoft.com/t5/video-hub/build-and-launch-a-sharepoint-home-site-tips-and-tricks-from-the/m-p/1696758)

[Planning your SharePoint hub sites](/sharepoint/planning-hub-sites)

[Creating and launching a healthy SharePoint portal](/sharepoint/portal-health)

Use and customize the [The Landing template](https://adoption.microsoft.com/sharepoint-look-book/) from the SharePoint look book

[Design a SharePoint home site for Viva Connections](create-sharepoint-home-site-for-viva-connections.md)

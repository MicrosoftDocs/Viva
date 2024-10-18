---
ms.date: 08/09/2024
title: "Frequently asked questions about the Feed for Viva Connections"
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
description: "Frequently asked questions about the Feed for Viva Connections"
---

# Get answers to common questions about the Viva Connections Feed

## What can I expect to see in the Feed?

The Feed gives content publishers a reliable means of distributing important news and information that their users need within their organizations. End-users will also see engaging content from sites they're a member of, sites they follow, and Viva Engage communities they follow. Get more information about the [content that displays in the Feed](#where-does-content-in-the-feed-come-from) and the [factors that impact the content's ranking in the Feed](#what-are-the-available-controls-to-influence-content-in-the-feed).

## Where does content in the Feed come from?

Content that is displayed in the Feed comes from three primary sources: organizational news published in SharePoint, posts in Viva Engage communities, and videos in Stream that are shared with the entire organization or targeted to user groups. Individual content items in the Feed will display for a 30-day period.

1. **News published on organizational news sites in SharePoint**

   SharePoint news that's published from [organizational news sites](/SharePoint/organization-news-site) will display in the Feed. Organizational news sites are communication sites that have been designated as a source of authoritative news in the SharePoint admin center. In addition to organizational news posts, the following news will also be displayed in the Feed:

   - SharePoint news from [sites you follow and sites you frequently visit](https://support.microsoft.com/office/find-and-follow-sites-news-and-content-4411e38f-9bc5-4ecc-bd33-3dbe939ac84c)
   - [Boosted news in SharePoint](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83) from organizational news sites
   - News that has [audience targeting applied](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293) from organizational news site or sites you follow
   - SharePoint news from sites that are relevant to your interests

2. **Posts in Viva Engage communities**

   Certain posts in various Viva Engage communities will appear in the Feed. These Viva Engage posts will come from Viva Engage communities that are authorized to post to "All Company" or the entire organization. Posts that are [All Company](https://techcommunity.microsoft.com/t5/yammer-blog/engage-your-entire-organization-with-new-all-company-features/ba-p/1441124) are intended to be viewed by everyone.

   In addition to All Company Viva Engage posts, you'll also see the following activity from Viva Engage in the Feed:

   - Viva Engage All Company Featured Posts
   - Viva Engage All Company Announcements
   - Viva Engage All Company Posts
   - Viva Engage Followed Community Featured Posts
   - Viva Engage Followed Community Announcements
   - Viva Engage Followed Community Posts
   - Viva Engage Followed Community Q&A posts
   - Viva Engage Followed Community Praise posts
   - Viva Engage Storyline posts

3. **Videos in SharePoint hosted by Stream**

   [Stream videos](/stream/streamnew/new-stream) built on SharePoint or OneDrive that are shared with your entire organization will appear in the Feed. Depending on how your organization stores and shares videos in Stream will impact the viewing experience for videos in the Feed.

   Not all of the three sources of content will be given equal weight in the ranking. [Learn more about how content is ranked](#how-is-the-feed-personalized-and-how-is-content-ranked).

## How often is Feed content refreshed?

For mobile, the Feed refreshes each time the application is selected. Users can also manually refresh the Feed through the pull-down action. On the web, the Feed automatically refreshes each time the web page is refreshed. Individual content items in the Feed will display for a 30-day period. SharePoint news posts that have been boosted will display prominently for up to four days. [Learn more about the news boost feature](https://support.microsoft.com/office/boost-sharepoint-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83).

## When can we expect to see a newly created post in the Feed?

Posts will typically take up to 1 hour to appear in a user’s Feed.  Content from a newly created [SharePoint home site](home-site-plan.md) is sometimes delayed for up to 24 hours after the site is initially created. After that initial 7-day period has passed, it will take up to 1 hour to appear.

## How is the Feed personalized and how is content ranked?

There are several factors such as the content’s age, whether it’s been "boosted" by the organization, the publishing source, and the author’s relationship to the reader to determine the content ranking. This is to users can discover new content each time they open the Feed so it never gets boring or predictable. However, engaging content in the Feed relies on how often content is created on the SharePoint sites and Viva Engage communities.

We’re experimenting and rapidly iterating on the logic used:

- **Chronology** - Content is sorted into 3 buckets.
- **Promotion** - Boost and Featured news is surfaced highly in each bucket.
- **Source Priority** - Messaging from organizational news sites is ranked slightly higher than organic content from people around you.
- **Engagement** - Ensure dynamic mix of content types within each bucket.

One of the primary goals of the Feed is to give content publishers a reliable means of distributing important news and information. To keep readers interested and coming back regularly we’re working to strike a balance between the engaging content they want (like from sites they're a member of, or communities they follow) and the information they need (like SharePoint organizational news site and Viva Engage All Company posts). To achieve this, we don’t rely on a pure chronological ranking.  

The content in the Feed is personalized for each user based on their memberships and permissions. We always restrict what content the user sees to content they have permissions to view.  In addition to any org-wide memberships, we’ll include content from SharePoint sites and Viva Engage communities the user is optionally a member of.  The goal of having a fresh, dynamic, and engaging Feed to keep them coming back.

## Why don’t I see any content in the Feed?

If you’re not seeing any content in your feed, it could be because of a few reasons:

1. There needs to be some content published to a SharePoint site or Viva Engage community that you’re a member of.  
2. Viva Engage Posts that aren't Featured or to **All Company** communities or **Announcements** may be removed and replaced in subsequent feed views to give users more dynamic content.

3. The SharePoint site you're publishing from (home site or organizational news site) is less than seven days old.  This issue will resolve itself and content will appear normally after the initial seven days after site creation.

## What are the available controls to influence content in the Feed?

There’s no configuration required to get the Feed working. For the current release, customers can impact content placement in the Feed by targeting content to audiences, or by promoting it.

- **Promote important ‘official’ communications** - Use [News boost](https://support.microsoft.com/office/boost-news-from-organization-news-sites-46ad8dc5-8f3b-4d81-853d-8bbbdd0f9c83) to raise the visibility of crucial news posts.
- **Highlight community discussions** - Feature posts in public Viva Engage communities that you’d like seen by the entire organization.
- **Publish from official news sources** - Like [organizational news sites](/sharepoint/organization-news-site) or [SharePoint home sites](/sharepoint/home-site). Where content is from, impacts the ranking.

For SharePoint news, more filtering is available through [audience targeting](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293), which allows publishers to designate content relevant to specific groups of people. Examples might be employees in a specific department, region, building, or title. This is done by enabling audience targeting on the site where content is being published, then using Microsoft Entra groups to define the target audience. However, if audience targeting isn't applied, users will still get the SharePoint News on their feed. Publishers also have the ability to promote critical messages in the Feed. News published from Org News sites has a Boost feature that explicitly tells the feed ‘this content is important’. As a result, that content is artificially pushed to the top of the feed. [Learn more about audience targeting in Viva Connections](/viva/connections/use-audience-targeting-in-viva-connections).

In Viva Engage, moderators of the All-Company community can Feature a post to indicate it’s significant and increase visibility within the organization. Featured posts from Viva Engage are treated as important by our ranking algorithm. For communities that you're a member of, communication managers can also [create Announcements within those communities](https://support.microsoft.com/office/create-polls-praise-announcements-and-questions-in-viva-engage-4b30c7e0-f915-4c69-9582-ccbbd09a516b), which will also be treated as important by our ranking algorithm.

For SharePoint news, more filtering is available through [audience targeting](https://support.microsoft.com/office/target-navigation-news-files-links-and-web-parts-to-specific-audiences-33d84cb6-14ed-4e53-a426-74c38ea32293), which allows publishers to designate content relevant to specific groups of people. Examples might be employees in a specific department, region, building, or title. This is done by enabling audience targeting on the site where content is being published, then using [Microsoft Entra](/entra/fundamentals/what-is-entra) groups to define the target audience. However, if audience targeting isn't applied, users will still get the SharePoint News on their feed. Publishers also have the ability to promote critical messages in the Feed. News published from Org News sites has a Boost feature that explicitly tells the feed ‘this content is important’. As a result, that content is artificially pushed to the top of the feed. [Learn more about audience targeting in Viva Connections](/viva/connections/use-audience-targeting-in-viva-connections).

## What actions can viewers take on the Feed?

For the current release, users on the Feed can do the following actions on posts:

1. Comment on a post
2. Reply to a comment on a post
3. Social Reactions – React to a post and comment
4. Share a post
5. Save a post for later

## What can I do to save content in the Feed after I have viewed it?  

Users can bookmark content that they would like to view later by selecting the **Save for Later**. Content can then be accessed through the save for later feature in the Viva Connections mobile app in Teams.

## Why isn’t boosted news displaying in the Feed for Viva Connections web part or in the Top News Card?  

> [!NOTE]
>
> Starting **September 1, 2024**, the feed for Viva Connection web part and the video news link will be removed and unavailable for SharePoint site editors to add to their sites. On **November 5, 2024**, support for the feed for Viva Connections web part and video news links will end and no longer display content.
>
> Site owners are encouraged to use the [News](https://support.microsoft.com/office/c2dcee50-f5d7-434b-8cb9-a7feefd9f165#bkmk_sitenews), [Viva Engage](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da#highlights), [File and Media](/stream/streamnew/portals-single-video), and [Highlighted content](/stream/streamnew/portals-set-of-videos) web parts, and [Video pages](https://support.microsoft.com/office/7823449f-e2cc-48d2-bda7-2ee82518958a) as alternatives to using the feed for Viva Connections web part and the video news link. For more information, refer to the [Viva Connections Feed web part retirement support guidance documentation](feed-web-part-video-news-link-retirement.md).

In the [Feed for Viva Connections web part](/viva/connections/use-feed-web-part-for-viva-connections), news posts from [organizational news sites](/sharepoint/organization-news-site) up to 24 hours from the post date will take precedence over older boosted news that has not yet reached the expiration. This can prevent boosted news from displaying prominently to end-users if the boosted news publishing date is older than the organizational news. Also, for [new organization news sites](/sharepoint/organization-news-site), it can take up to 24 hours for boosted news created from those sites to appear in the Top News card in Viva Connections dashboard.

## More resources:

[Overview of Viva Connections](viva-connections-overview.md)

[Set up and launch Viva Connections](set-up-admin-center.md)

[Use the Viva Connections Feed web part](https://support.microsoft.com/office/use-the-feed-web-part-for-viva-connections-001fbe90-3778-4801-9ea9-71308711d330)

[Create an organizational news site in SharePoint](/SharePoint/organization-news-site)

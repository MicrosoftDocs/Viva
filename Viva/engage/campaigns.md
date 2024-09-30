---
title: "Set up official campaigns in Viva Engage"
description: "Campaigns in Engage are an interactive way to drive engagement and build company culture."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/26/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Set up official campaigns in Viva Engage

Drive engagement across your organization through campaigns. Campaigns are an effective and interactive tool for building company culture, community, and belonging.

Viva Engage offers two types of campaigns: *Official* campaigns, which are available to the entire organization, and *community* campaigns, which are exclusive to the community’s membership. Learn more how community admins can [create, manage, and delete community campaigns here](https://support.microsoft.com/en-us/topic/community-campaigns-in-viva-engage-002003fe-8d8d-42c2-9b7c-6aa2e1d9fef8).

Licensed Engage admin or corporate communicators can create, manage, and delete official campaigns. Unlicensed admins can only access the campaign management dashboard to delete campaigns.

>[!NOTE]
>Campaigns are available in Viva Engage Premium. Learn more about licensing [here](manage-engage-licenses-microsoft-365.md).

## Open the campaign dashboard

Use the campaign dashboard to create, edit, and end campaigns. In the dashboard, you can also find analytics that show a campaign's overall performance and engagement.

1. Go to the [Viva Engage admin center](/viva/engage/eac-overview).

    [![Screenshot of the entrypoint into the Viva Engage admin center](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox).

2. On the **Feature management** tab, select **Campaigns** to access the campaign dashboard.

    [![Screenshot of the interface to manage campaigns in the Viva Engage admin center](/viva/media/engage/admin/campaigns-eac.png)](/viva/media/engage/admin/campaigns-eac.png#lightbox).

    The dashboard lists all active, ended, and draft campaigns created for the organization.

## Create an official campaign

1. From the campaign dashboard, select **Create campaign** in the upper-right corner of the campaign dashboard.
1. Fill in the fields according to your campaign goals.
    - **Campaign hashtag** is a required field. The campaign hashtag is the campaign name and appears on the campaign landing page.
    - **Default publisher** refers to the default post type (discussion, question, poll, or praise) when users post on the campaign page. For example, if you choose **Question**, the question format automatically appears when a user posts on the campaign page.
    - **Theme color** lets you customize the color of the campaign hashtag.  
    - **Add co-organizers** to help you manage the campaign. Learn more about the [coorganizer role and their permissions here.](https://support.microsoft.com/en-us/topic/add-co-organizers-to-viva-engage-campaigns-d799d73e-4292-42b0-a5a4-f1be0715cbaa)

1. Select **Confirm** to save your changes.<br>
The campaign is now in draft state. Until you publish the campaign, only Engage admins and corporate communicators can view the campaign.

1. To publish the organization, select the ellipses button on the campaign management dashboard, and from the menu select **Publish campaign**.

    [![Screenshot of the UI dropdown to publish and delete a campaign.](/viva/media/engage/admin/publish-campaign-button.png)](/viva/media/engage/admin/publish-campaign-button.png#lightbox)

The campaign landing page is visible to any Viva Engage licensed user who selects a post or comment that has the verified campaign hashtag.

## Create a multitenant campaign

If Viva Engage is set up as a hub-and-spoke multitenant organization, the hub tenant can host official campaigns that reach the entire organization. Hub leaders can harness the power of these campaigns to amplify their messages and reach to all subsidiaries on key causes and initiatives. Learn more about [multitenant organizations.](/Viva/engage/mto-setup)

You can create a multitenant campaign if you're a corporate communicator, Engage admin, network admin, or verified admin on the hub tenant.

1. Sign in as a hub admin or hub corporate communicator.

1. Follow the preceding instructions to create an official campaign.

1. In the **Create a new campaign** dialog, turn on the option **Visible to everyone in [*subsidiaries that comprise the MTO setup*]**. 

1. Complete setup and publish the campaign.

1. Assign coorganizers and executive sponsors as needed from persons in the hub tenant.

#### What’s different about a multitenant campaign?

Multitenant campaigns function much the same way as other official campaigns. Messaging from leaders appears in Leadership corner. All users (on the hub tenant and spoke tenants) can post to the campaign from most pages by adding the hashtag (#campaignname). All campaign content appears as verified.

Here are some key differences:

- Users in the hub tenant can only view and respond to posts from other users in the hub tenant.

- Users in the spoke tenants can view and respond to posts from hub users *and* users in their own spoke tenant. However, they can’t view or respond to posts from other spokes.

- Campaign analytics aggregates campaign activity for the multitenant organization (vs. showing analytics for individual tenants).

## Update the campaign cover photo

Corporate communicators can update the cover photo with a PNG or JPG image, 20 MB or smaller. Dimensions for this image are 984 pixels by 160 pixels.

- On the campaign homepage, select the options (...) menu under the existing image, and select **Upload cover photo**.

   :::image type="content" source="../media/engage/campaigns/upload-cover-photo.png" alt-text="Screenshot of the entry point into managing storyline settings.":::

## End or delete an official campaign

When an official campaign ends, the follow button and default publisher on the campaign landing page are disabled. Users can still post in communities and storylines using the verified campaign hashtag, and those posts appear on the campaign landing page.

1. In Viva Engage, select the ellipses (...) icon and then select **Admin**.  

1. From the Feature management tab, select **Campaigns**. 

1. Select the campaign, and in the **Actions** column select the ellipses icon, and select **End campaign** or **Delete**.
[![Screenshot of the analytics entrypoint at the top navigation of Engage.](/viva/media/engage/admin/analytics-navbar-icon.png)](/viva/media/engage/admin/analytics-navbar-icon.png#lightbox)

> [!NOTE]
> The three official campaigns that appear in the **Top campaigns** module on the right side of your home page are ordered based on number of followers. When you follow a campaign, it's removed from **Top campaigns** and replaced by a new campaign.  

## Build awareness for official campaigns

The verified campaign hashtag and campaigns discovery modules are the best means for discovering campaigns. To increase awareness and participation, use the verified campaign hashtag in posts and comments from the Home feed, storyline, communities, and from the official campaign landing page.

**Verified campaign hashtag**

- When users select a post or comment that contains the verified campaign hashtag, they're routed to the official campaign landing page, where they can follow the campaign.

   > [!NOTE]
   > To build campaign awareness and reach, campaign managers and leaders across the organization are encouraged to share as many posts as possible with the verified campaign hashtag to their storyline and communities. You can also share the campaign link through posts, emails, and Microsoft Teams chats for users to easily access the campaign landing page.

**Campaigns modules**
    
- **Top campaigns** module: On the right side of the Home feed, the *Top campaigns module* shows active official campaigns with the highest number of followers.

- **Followed campaigns** module: When a user follows an official campaign, they see a *Followed campaigns* module on the right side of their storyline.

## Manage official campaign analytics and engagement

Engage admin and corporate communicators have access to analytics that help monitor campaign engagement and improve future campaigns. They can access campaign analytics from the analytics icon on the top navigation menu of Engage, the campaign management dashboard, and the campaign landing page.

[![Screenshot of the analytics entrypoint at the top navigation of Engage.](/viva/media/engage/admin/analytics-navbar-icon.png)](/viva/media/engage/admin/analytics-navbar-icon.png#lightbox)

* From the campaign management dashboard, select the graph icon in the right column under **Actions** to navigate to campaign analytics.

    [![Screenshot of the entrypoint to campaign analytics from the campaign dashboard.](/viva/media/engage/admin/cmd-analytics.png)](/viva/media/engage/admin/cmd-analytics.png#lightbox)

* From the campaign landing page, select **View more analytics** from the **Summary analytics** module to navigate to campaign analytics.

    [![Screenshot of the campaigns analytics entrypoint from campaign landing page.](/viva/media/engage/admin/summary-campaigns-analytics.png)](/viva/media/engage/admin/summary-campaigns-analytics.png#lightbox)

   You're redirected to the campaign analytics dashboard, which contains key data to help monitor the success of your campaign.

   [![Screenshot of the campaign analytics page for admins in Engage.](/viva/media/engage/admin/campaign-analytics.png)](/viva/media/engage/admin/campaign-analytics.png#lightbox)

### Remove a post

If a post doesn't align with an official campaign's purpose, a corporate communicator or Engage admin can remove it. This action removes the post from the official campaign landing page without affecting the original post on either the storyline or community. If you remove a post in error, you can make it reappear on the campaign page by adding a comment with the campaign hashtag to the original post.

:::image type="content" alt-text="Screenshot of the post menu where you can find the Remove command." source="../media/engage/campaigns/remove-camp-post.png" lightbox="../media/engage/campaigns/remove-camp-post.png":::

### Export campaign data

Engage admins can use a network data export to get a record of all campaigns in the network. The campaigns.csv file stores attributes, such as community IDs and campaign IDs, for both official and community campaigns created on the network. For more details, see [Export network data](/viva/engage/eac-as-manage-data/#export-tenant-data-by-date-range).

### Corporate communicator privileges

Corporate communicators can perform the following functions to manage official campaigns:

- Publish official campaigns as **Active** and visible to all users in the network
- Set **Active** campaigns to **Ended** when a campaign is finished
- Republish **Ended** campaigns as **Active** for recurring campaigns
- Delete official campaigns that aren't relevant or were made by mistake
- Remove posts from the official campaign landing page if they aren't relevant
- Update certain assets on a campaign page such as:
    - Goal tracker
    - Cover photo
    - Pinned posts
    - Pinned resources and links
    - Theme color of the campaign hashtag
- View campaign analytics
- Assign campaign co-organizers
- Define leaders

>[!NOTE]
> The corporate communicator must manually update the goal tracker asset.

## Frequently asked questions

**Can I create a campaign for a hashtag that's already in use?**

Hashtags in use by other active or ended campaigns are unavailable for reuse. If the hashtag is in use by an unpublished campaign, it's available. However, any content created before the campaign is published won't be included in views or analytics.

**How often are campaign analytics refreshed?**

Analytics are refreshed daily. If you don’t see changes reflected immediately, check analytics the next day.

## See also

[Manage admin roles in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)

[View and manage analytics in Viva Engage](/viva/engage/analytics)

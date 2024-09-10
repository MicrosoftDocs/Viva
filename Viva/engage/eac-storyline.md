---
title: "Manage and set up storyline in Viva Engage"
description: "Storyline empowers everyone within your organization to connect and contribute, while enabling your leaders to reach and engage employees."
ms.reviewer: john.bacus
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 9/11/2024
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

# Manage and set up storyline in Viva Engage

Storyline empowers everyone in your organization to connect and contribute through the Web and mobile applications you use every day—-Outlook, Microsoft Teams, and Microsoft Viva. Through storyline, leaders can reach and engage their teams. Employees can share updates and experiences with followers and colleagues across the organization.

When storyline is enabled in your organization, you see the following changes in the Viva Engage app:

- Internal (nonguest) users who have access to Viva Engage see a new default Storyline tab on their user profile page.
- Users see a new Storylines page. Users can toggle between a personalized feed of posted content or a focused feed that includes only storyline content from the people that the user follows.

## Set up storyline

Engage administrators manage storyline for their organizations in the [Engage admin center](/viva/engage/eac-overview). 

1. To access storyline settings, select the ellipses on the right side of the top navigation menu, and then select **Admin**.

1. On the **Feature management** tab, select **Storyline** to customize settings.

    :::image type="content" source="../media/engage/admin/storyline-eac-updated.png" alt-text="Screenshot of the entry point into managing storyline settings." lightbox="../media/engage/admin/storyline-eac-updated.png#lightbox":::

## Enable storyline

The Storyline page in the Engage admin center controls the availability of storyline in the organization.

When you enable storyline, all internal users who have access to Viva Engage have the Storyline tab and a storyline feed on their profile page. They also have the ability to react and respond to others’ storyline posts. To restrict storyline, see [Restrict which users can post to their storyline](/viva/engage/eac-storyline?branch=pr-en-us-8285#restrict-which-users-can-post-to-their-storyline).

:::image type="content" source="../media/engage/admin/storyline-toggle.png" alt-text="Screenshot of the storyline settings toggles in Viva Engage." lightbox="../media/engage/admin/storyline-toggle.png#lightbox":::

>[!NOTE]
> Guests don't have their own storyline and can't see storyline content from internal users.

## Advanced settings

Admins can use these settings to control how they configure storyline for their organization. These settings establish the default behavior for storyline notifications and restrict who can post to storyline.  

### Set default notification channels for storyline posts

In its default configuration, storyline notifies users in Teams, email, and Viva Engage anytime a person they follow posts to their storyline page. Network and verified admins can override this configuration to control which default notifications are selected when a user follows someone. Users can also change the default notification setting for each person they follow.

System default selections for notifications include:

- Teams notifications, which appear in the Teams Activity feed.
- Email notifications. Email supports actionable messages, which lets users view and reply from Outlook Web Access.
- Viva Engage notifications, which appear as Viva Engage notification bells.

### Restrict which users can post to their storyline

By default, every internal user with access to Viva Engage has the option to post to their own storyline feed. Admins can override the default and restrict this option to specific users.  This setting controls who has a storyline feed on their user profile and who can create a new storyline post. It doesn’t restrict who can view, react, or reply to storyline posts made by others.

1. To restrict who can post to storyline, from the Engage admin center, go to **Manage storyline**.

1. Select **Advanced Settings**.

1. Switch **Eligible users with access to Viva Engage** to **Eligible users from selected group**.

1. Search for and select the group that includes users who should receive their own storyline page.

The supported group types include security groups, mail-enabled security groups, distribution lists, and Microsoft 365 groups. When a group is selected, Viva Engage checks the group membership on a daily basis to assign storyline privileges.

Your changes should take effect within minutes. Backend membership changes in the selected group can take up to 24 hours to be applied to storyline privileges.

To delete previous storyline conversations after you disable storyline, use the same processes that you use to delete other conversations in Viva Engage

#### What users experience when storyline is disabled

When you disable storyline for a user, the user is unable to create new storyline posts and the Storyline tab no longer appears on their user profile--regardless of whether they previously posted to their storyline. *If you disable storyline for all users in your network*, Storylines doesn't appear in the left navigation pane of Viva Engage for the web, or in the top navigation of the Viva Engage app for Teams and Outlook.

Even though the user no longer has a storyline tab on their profile, their storyline conversations are available through the All activity feed and through search.

All Storyline content is available through [network data export](eac-as-manage-data.md#export-tenant-data-by-date-range). Networks in Native Mode can also access this content [through eDiscovery](eDiscovery-engage.md).

> [!NOTE]
> If you need to address objectionable content or security concerns, an effective solution is to [delete the conversation](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md#DeleteMessagesFiles) or [block the offending user](./manage-viva-engage-users/add-block-or-remove-users.md).

### Configure a multitenant organization to use storyline

When Viva Engage is configured for a multitenant organization, the **Multi-tenant Organizations (MTO)** setting appears in the Advanced settings of the designated hub tenant. This setting enables users on all spoke tenants to engage with storyline posts from the hub tenant. However, these users can only participate if the multitenant organization configuration in Microsoft Entra ID has granted them access to storyline. Learn more about [configuring a multitenant organization in Viva Engage](/Viva/engage/mto-setup).

## Security and compliance

Storyline is built on the same content and conversation platform as community messages in Viva Engage. Therefore, you can use the same tools for storyline that you use for monitoring and governance.  

* Use [eDiscovery](ediscovery-engage.md) in the compliance portal for Native Mode networks.  
* Access storyline content through [network export](eac-as-manage-data.md).
* Files shared through storyline are stored on OneDrive. Shared files are subject to any governance you already have in place.
* Storyline supports the [Report a conversation](report-conversation-overview.md) feature that's available for community conversations.
* Microsoft Purview Communications Compliance (E5): Use AI to monitor conversations for bullying, harassment, or topics that are against usage policy.

In addition to the capabilities listed here, storyline features a feed that includes all storyline posts, sorted by the date the storyline conversation was started. To access this feed, go to the storyline landing page. In the feed, select the filter icon in the upper-right corner to switch the filter to **All**.

#### Security, compliance, and governance for files uploaded to storyline posts

Compliance for storyline posts is the same as the rest of Viva Engage. If you're in Native Mode, posts are ingested into the substrate and subjected to the same compliance and eDiscovery capabilities as posts in communities--including communications compliance and retention. Files are stored in OneDrive, where they inherit the same security and compliance policies configured for other files in OneDrive.

When user accounts are deleted (for example, when an individual leaves the company), the system follows the Microsoft 365 user deletion process. Learn more about [deleting a user account](./manage-viva-engage-users/manage-users-across-their-lifecycle.md#delete-a-user).

## File storage for storyline

Files attached to storyline posts are stored in a hidden library in the author’s OneDrive. There's no entry point to this location in the Microsoft 365 user experience, but you can access it through a URL resembling the following example: 

   `https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage/Attachments/Storyline`

To determine the precise URL for a user's storyline page, follow these steps:

1. Open the user's OneDrive in a browser.
2. Note the URL to the user's OneDrive.
3. Locate the **user identifier**, which is the part of the URL immediately that follows *my.sharepoint.com/personal/*.
4. Replace everything after the profile identifier and the backslash plus **VivaEngage**, without a space, case insensitive. The resulting URL resembles this example: 

   `https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage`
1. Press Enter. The library appears.  
1. Open the Attachments folder, and then open the storyline folder. The URL to the folder where storyline files are saved resembles this example:


   `https://<tenantname>-my.sharepoint.com/personal/<user identifier>/VivaEngage/Attachments/Storyline`

### Managing files uploaded to storyline posts

You can use the storyline interface to edit documents and rich media that was uploaded to posts. We strongly recommend that you don't add, replace, or delete documents and rich media directly in OneDrive, as those actions risk breaking the front-end experience of posts in your storyline.  

To delete files associated with a post from the **VivaEngage** library:

1. Remove the file from the associated post. From any post, the author or an admin can select the ellipsis (...) menu and choose **Edit**.  
2. Navigate to the author's **VivaEngage** library and delete the file.

## Frequently asked questions

### Why isn’t storyline available in our organization?

Storyline is only supported in Viva Engage networks that [enforce Microsoft 365 identity](/viva/engage/configure-your-viva-engage-network/enforce-office-365-identity). If your network doesn't enforce Microsoft 365 (formerly Office 365) identity, or if you have a Viva Engage Basic network, storyline isn't available to your organization.

### Who can see storyline content?

Storyline content is visible to any internal user who has access to Viva Engage. Guests can't see storyline content.  

### Does storyline work for guests?

Guests are excluded from storyline access. They don't have their own storyline and can't see any storyline content posted by other users.

### Can I control who sees storyline content?

You can't prevent any internal user from seeing storyline content if they have access to Viva Engage. Guests can't see any storyline content.

### How do I delete custom cover images that were uploaded to a person's storyline?

From the UI, Engage admins with premium Viva licenses can upload or delete cover photos for any user who has the premium Viva license and has storyline enabled. To do this, from the profile page of the user, hover over the profile header and select **Upload cover photo**. Then, delete or upload a new cover image, as needed.

If the admin or the user isn't premium licensed, or the user no longer has their own storyline, previously uploaded photos must be deleted with the API.

From the API, Engage admins or verified admins can delete cover images for any user in their network through an API call. The URL has this syntax:

`engage.cloud.microsoft/api/public/v1/user-profiles/user_id/cover-image`

For example, to delete the cover images of a user with id 1234567890, the URL would be:

`engage.cloud.microsoft/api/public/v1/user-profiles/1234567890/cover-image`


## See also

[Overview of the Viva Engage admin center](/Viva/engage/eac-overview)

[Set up the Viva Engage admin center](/Viva/engage/eac-get-started)

[Identify leaders and manage audiences in Viva Engage](/Viva/engage/leadership-identification)

---
title: "Manage and set up storyline in Viva Engage"
description: "Storyline empowers everyone within your organization to connect and contribute, while enabling your leaders to reach and engage employees."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
ms.date: 2/15/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Manage and set up storyline in Viva Engage

Storyline empowers everyonehin your organization to connect and contribute. It enables your leaders to reach and engage employees. Through storyline, people can share updates, experiences, and perspectives to reach followers and colleagues across the organization. Engage with storylines from the Web and the mobile applications you use every day: Outlook, Microsoft Teams, and Microsoft Viva.

When storyline is enabled in your organization, you see the following changes in the Viva Engage app:

- Internal (non-guest) users who have access to Viva Engage see a new default **Storyline** tab on their user profile page.
- Users see a new **Storylines** page. For this page, users can toggle between a personalized feed of posted content or a focused feed that includes only storyline content from the people that the user follows.

## Set up storyline

Microsoft 365 Global admin and Engage admin can manage storyline for their organizations in the [Engage admin center](/Viva/engage/eac-as-access-eac): Select the ellipses on the right of the top navigation menu, and then select **Admin**.

[![Screenshot of the entrypoint into the Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

On the **Feature management** tab in the Engage admin center, select **Storyline** to customize settings.

[![Screenshot of the entrypoint into managing storyline settings.](/viva/media/engage/admin/storyline-eac-updated.png)](/viva/media/engage/admin/storyline-eac-updated.png#lightbox)

## Enable storyline

In the interface for managing storyline, admins see toggles that control the availability of storyline in the organization. When storyline is enabled in your organization, it's available to all internal users who have access to Viva Engage. All internal users have their own storyline feed on their profile page and can see, react to, and respond to others’ storyline posts.  

[![Screenshot of the storyline settings toggles in Viva Engage.](/viva/media/engage/admin/storyline-toggle.png)](/viva/media/engage/admin/storyline-toggle.png#lightbox)

>[!NOTE]
> Guests don't have their own storyline and can't see storyline content from internal users.

When you disable storyline, the storylines landing page and the **Storylines** tab on user profile pages are removed. Users can't start new storyline conversations, but existing conversations aren't deleted. Previously posted storyline content can still be accessed through search and the Viva Engage Inbox by the people who participated in the storyline conversation. Users who didn't participate in the conversation previously don't have access after storyline is disabled. The storyline content continues to be available through network data export and is available through eDiscovery for networks that are in native mode.  

## Advanced settings

Storyline supports additional controls for admins to customize their configuration. Currently you can set default notification preferences for storyline, and we plan to add more controls.

### Set default notification channels for Storyline posts

In its default configuration, Storyline notifies followers via Teams, email, and Viva Engage when a person that they follow posts to their storyline. Network and Verified admins can override this set-up to control what default notifications are selected when a user follows someone. Users can also change from the default selections to their personal preferences for notifications for each person they follow.

The system default selections for notifications include:

- Microsoft Teams–notifications are delivered in the Teams Activity feed.
- Email–email delivered to your Inbox includes support for Actionable messages, so the conversation can be viewed and replied from Outlook Web Access.
- Viva Engage–notifications are delivered to the Viva Engage notification bells.

## Security and compliance

Storyline is built on the same content and conversation platform as community messages in Viva Engage. Therefore, you can use the same tools for storyline that you use for monitoring and governance.  

* Use eDiscovery through the compliance portal for native mode networks.  
* Storyline content is available via network export.
* Files shared through storyline are stored in OneDrive and are subject to any governance you already have in place.
* Storylines supports the same [Report a conversation](/yammer/manage-yammer-groups/configure-conversation-reporting) feature that's available for community conversations.
* Microsoft Purview Communications Compliance (E5): Use AI to monitor conversations for bullying, harassment, or topics that are against usage policy.

In addition to the capabilities listed here, storyline also features a feed that includes all storyline posts sorted by the date the storyline conversation was started. To access this feed, go to the storyline landing page. In the feed, select the filter icon in the upper-right corner to switch the filter to **All**.

#### Security, compliance, and governance for files uploaded to storyline posts

Storyline posts are backed by Yammer services. Compliance for posts is therefore the same as for the rest of Viva Engage. If you're in native mode, posts are ingested into the substrate and are subject to the same compliance and e-Discovery capabilities as posts in communities, including communications compliance and retention. Because files are stored in OneDrive, they inherit security and compliance policies configured for files in OneDrive.

When users are deleted—for example when an individual leaves the company—the system follows the Microsoft 365 user deletion process described in the **Delete a user** section of [Manage Yammer users across their lifecycle from Office 365](/yammer/manage-yammer-users/manage-users-across-their-lifecycle).

## File storage for storyline

All files attached to storyline posts are stored in a hidden library in the author’s OneDrive. There's no entry point to this location in the Microsoft 365 user experience, but you can access it with a URL resembling the following example: https://tenantname-my.sharepoint.com/personal/**useridentifier/VivaEngage/Attachments/Storyline**

To determine the precise URL for a user's storyline, follow these steps:

1. Open the user's OneDrive in the browser.
2. Note the URL to the user's OneDrive.
3. Locate the **user identifier**, which is the part of the URL immediately that follows *my.sharepoint.com/personal/*.
4. Replace everything after the profile identifier and the backslash **VivaEngage**, without a space, case insensitive. The resulting URL will resemble this example: 
   'https\://tenantname-my.sharepoint.com/personal/\<useridentifier>/VivaEngage'
1. Press ENTER. The library will appear.  
1. Open the Attachments folder, and then open the storyline folder. The resulting URL to the folder where storyline files are saved will resemble this example: 
   `https://tenantname-my.sharepoint.com/personal/<user identifier>/VivaEngage/Attachments/Storyline`

### Managing files uploaded to storyline posts

You can use the storyline interface to edit documents and rich media that was uploaded to posts. We strongly recommend that you don't add, replace, or delete documents and rich media directly in OneDrive, as those actions risk breaking the front-end experience of posts in your storyline.  

To delete files associated with a post from the **VivaEngage** library:

1. Remove the file from the associated post. From any post, the author or an admin can select the ellipsis (...) menu and choose **Edit**.  
2. Navigate to the author's **VivaEngage** library and delete the file.

## Frequently asked questions (FAQ)

### Why isn’t storyline available in our organization? 
Storyline is only supported in Yammer enterprise networks that [enforce Office 365 identity](/yammer/configure-your-yammer-network/enforce-office-365-identity). If your network doesn't enforce Office 365 identity or if you have a Yammer Basic network, storyline isn't available to your organization.

### Who can see storyline content? 
Storyline content is visible to any internal user who has access to Viva Engage. Guests can't see storyline content.  

### Does storyline work for guests? 
Guests are excluded from storyline access. They don't have their own storyline and can't see any storyline content posted by other users.

### Can I control who sees storyline content? 
You can't prevent any internal user from seeing storyline content if they have access to Viva Engage. Guests can't see any storyline content.

### Can I control which users get their own storyline?  
We plan to add the capability of to limit who gets their own storyline shortly after storyline reaches general availability. This functionality will allow you to use Azure AD groups to designate which users get a personal storyline feed their user profile page in Yammer. Users that don't get a storyline is able to reply and react to storyline posts from users who do have their own Storyline.

### How do I delete custom cover photos that were uploaded to a person’s storyline? 
When the preview features toggle is turned *on* the user or Network and Verified Admins can delete uploaded cover photos. To do this, go to the user profile page and select the delete option under **Update cover photo**.

To delete a previously uploaded cover photo when the preview toggle is turned *off*, you need to temporarily opt in to the preview so you can access the delete cover photo option.

## See also

[Access the Engage admin center](/Viva/engage/eac-as-access-eac)

[Set up the Engage admin center](/Viva/engage/eac-get-started)

[Identify leaders and manage audiences in Viva Engage](/Viva/engage/leadership-identification)
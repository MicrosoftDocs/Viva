---
title: "Access the Engage admin center"
description: "Describes settings in the Viva Engage admin center."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
ms.date: 02/15/2023
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

# Access the Engage admin center

Only users in the following admin roles can access the Viva Engage admin center: Global admin, Engage admin, Answers admin, and corporate communicator. End users (employees) in your organization can't access it.

In the Viva Engage Teams application, select the ellipses button from the top navigation menu to expose the admin option. Select **Admin** to go to the Engage admin center.

[![Screenshot of the entrypoint into the Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

## Manage corporate communicators  

As a Global admin, Engage admin, or corporate communicator, you can identify and remove users as corporate communicators. On the **Setup and configuration** tab, select **Manage corporate communicators** to open the configuration options.  

[![Screenshot of the interface for managing corporate communicators.](/viva/media/engage/admin/manage-corpcomms.png)](/viva/media/engage/admin/manage-corpcomms.png#lightbox)

### Assign a user as a corporate communicator

Select **Add user** to search for a user by their name or email ID. After the assignee is identified and selected as a corporate communicator, they're visible in the list of active corporate communicators in your organization.  

[![Screenshot of the interface for adding corporate communicators.](/viva/media/engage/admin/add-corp-comms.png)](/viva/media/engage/admin/add-corp-comms.png#lightbox)

>[!NOTE]
> While assigning a user to this role is a pre-licensed capability, the actions this user can perform depend on the nature of their license, core versus premium.  

Corporate communicators can do the following functions:

- **Create campaigns**
- **Manage campaigns**
    - Publish draft campaigns to be **Active** and viewable to all users in the network.
    - Set Active campaigns to **Ended** when a campaign is finished.
    - Republishing "Ended" campaigns as "Active" again for reoccurring campaigns.
    - Delete campaigns that aren't relevant or were created by mistake.
    - Update certain assets on a campaign page such as:
        - Goal tracker
        - Cover photo
        - Pinned posts
        - Pinned resources and links
        - Theme colors for the campaign hashtag
        - View campaign analytics

    - Identify leaders
        - Manage their audience

### Remove user as a corporate communicator

To remove a user from this role, select the delete icon on the right side of the corporate communicator list. They'll no longer be listed as an active corporate communicator in your network.

[![Screenshot of the interface for removing a corporate communicator in Viva Engage.](/viva/media/engage/admin/remove-corp-comm.png)](/viva/media/engage/admin/remove-corp-comm.png#lightbox)

## Configure your tenant

As a Global admin or Engage admin, you're encouraged to set up your Viva Engage enterprise experience for all employees before they start to use the application. This practice helps maintain a consistent experience. Engage admins can navigate to the **Setup and configuration** tab in the Engage admin center and select **Configure tenant**.  

[![Screenshot of the interface for configuring the tenant in Viva Engage.](/viva/media/engage/admin/config-tenant.png)](/viva/media/engage/admin/config-tenant.png#lightbox)

They're then routed to the Yammer admin center, where they can perform the following actions:  

- [Configure the network](/yammer/configure-your-yammer-network/configure-yammer)
    - Set the tenant network name
    - Require users to confirm email messages before posting
    - Restrict who can upload files, and limit file formats
    - Allow Tenor GIFs in messages
    - Control how links are displayed
    - Allow message translation
    - Set the default system message language and many more
- [Customize the look](/yammer/configure-your-yammer-network/customize-the-look-of-yammer)
- Manage domains in Office 365  
- [Migrate a network to Native Mode](/yammer/configure-your-yammer-network/native-mode-step-by-step-guide), if this isn't already done

>[!NOTE]
> Because Viva Engage is powered by Yammer technology, configuring the tenant through the Yammer admin center will publish changes to both Yammer and Viva Engage. We are working to bring these configuration options to the Engage admin center as part of our admin roadmap.

## See also

[Key admin roles and permissions in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[Manage data in the Engage admin center](/Viva/engage/eac-as-manage-data)

[Set up the Engage admin center](/Viva/engage/eac-get-started)

[View and manage campaigns in Viva Engage](/Viva/engage/campaigns)

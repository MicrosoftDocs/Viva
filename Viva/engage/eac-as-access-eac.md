---
title: "Access the Engage admin center"
description: "Viva Engage is a new employee experience that connects people across the company—wherever and whenever they work—so that everyone is included and engaged."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
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

The admin center can only be accessed by users with the following admin roles: Global admin, Engage admin, Answers admin and corporate communicators. It cannot be accessed by end users (employees) within your organization.

Within the Viva Engage Teams application, select the ellipses button on the top right corner to expose the admin option. Select **Admin** to navigate to the Engage admin center.

![Image of the entrypoint into the Engage admin center.](/Viva/media/engage/admin/admin-entrypoint.png)

## Manage corporate communicators  

As a Global admin, Engage admin, and corporate communicator, you can identify and remove users as corporate communicators. Under the **Setup and configuration** tab, select **Manage corporate communicators** to open configuration options.  

![Image of the interface for managing corporate communicators](/Viva/media/engage/admin/manage-corpcomms.png)

### Assigning user as a corporate communicator

Select **Add user** to search for a user by their name or email ID. Once the assignee is identified and selected as a corporate communicator, they will be visible in the list of active corporate communicators within your organization.  

![Image of the interface for adding corporate communicators](/Viva/media/engage/admin/add-corp-comms.png)

>[!NOTE]
> While assigning a user to this role is a pre-licensed capability, the actions this user can perform will depend on the nature of their license (seeded vs premium).  

Once assigned, the corporate communicator will be able to: 

- Create campaigns 
- Manage campaigns via: 
    - Publishing Draft campaigns to be **Active** and viewable to all users in the network 
    - Setting Active campaigns to **Ended** once a campaign is finished
    - Re-publishing Ended campaigns to be Active again for reoccurring campaigns 
    - Deleting campaigns that are not relevant or were made by mistake
    - Updating certain assets on a campaign page such as the: 
        - Goal tracker (to be available for GA) 
        - Executive sponsors 
        - Cover photo 
        - Pinning posts 
        - Pinning resources and links
        - Updating theme colors 
        - View campaign analytics 

    - Identify leaders 
        - Manage their audience 
        - Manage their delegates 

> [!NOTE]
> A corporate communicator with the seeded license can only identify leaders and their audiences. The user will need an Engage premium license to create and manage campaigns.  

### Remove user as a corporate communicator 

Selecting the delete icon on the right side of the corporate communicator list will remove the user from this role and they will no longer be visible as an active corporate communicator in your network.  

## Configure tenant

As a Global admin or Engage admin, you are encouraged to setup your Viva Engage enterprise experience for all employees before they start using the application. This will help maintain a consistent experience. An Engage admin can navigate to the **Setup and configuration** tab within the Engage admin center and select **Configure tenant**.  


![Image of the interface for configuring the tenant in Viva Engage.](/Viva/media/engage/admin/config-tenant.png)

They are then routed to the Yammer admin center to perform the following actions:  

- [Configure the network](https://learn.microsoft.com/yammer/configure-your-yammer-network/configure-yammer)
    - Set tenant network name 
    - Require users to confirm email messages before posting 
    - Restrict who can upload files and limit file formats 
    - Allow Tenor GIFs in messages 
    - Control how links are displayed 
    - Allow message translation 
    - Set default system message language and many more 
- [Customize the look](https://learn.microsoft.com/yammer/configure-your-yammer-network/customize-the-look-of-yammer)
- Manage domains in Office 365  
- [Migrate network to Native Mode](https://learn.microsoft.com/yammer/configure-your-yammer-network/native-mode-step-by-step-guide) (if not done already) 

>[!NOTE]
> Since Viva Engage is powered by Yammer’s technology, configuring the tenant through the Yammer admin center will publish changes to both Yammer and Viva Engage. We are working to actively bring these configuration options to the Engage admin center as part of our admin roadmap.

## See also 
[Answers in Viva Engage overview](https://support.microsoft.com/en-us/topic/getting-started-with-microsoft-viva-engage-729f9fce-3aa6-4478-888c-a1543918c284)

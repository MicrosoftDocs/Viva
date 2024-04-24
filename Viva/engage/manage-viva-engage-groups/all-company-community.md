---
title: "All Company now works like other Viva Engage communities"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 01/04/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 
description: "Learn how All Company now works like other communities in Viva Engage."
---

# All Company now works like other Viva Engage communities

All Company uses the Viva Engage community architecture in Native Mode and non-Native Mode tenants so that you can get all the new community experiences and features as they roll out. With this integration, All company now has community customization options, like cover photos and naming.

## What are the changes to All Company?

Now that All Company works like other communities, these features are available to network admins:

- You can edit the name, description, avatar, and cover photo for All Company.
  >[!IMPORTANT]
    > Previously the All Company name locale changed based on the user’s locale. Now that you can fully customize the name, the default All Company name is set in the network’s locale.  When the admin changes the name, the name persists for that network. The name doesn't adjust to the language of the user's locale if it differs from the network.
- Pinned resources actions (add, delete, reposition) are restricted to network admins.
- You can [restrict posts to All Company](https://support.office.com/article/3219d2ae-db15-4c9f-9dd2-28559ae39a97), if you want to control the types of conversations that take place in the All Company feed. When this setting is enabled, only admins can post in All Company. Employees can reply to a conversation starter or react to it.
- Previous All Company Resources are moved to Pinned resources.
- You can search for All Company communities by name (even if the community was renamed).
- Community insights are only for the All Company community. Previously, insights found under the All Company page applied to the entire network and weren't specific to the community.
  >[!NOTE]
  >If you need access to previous insights for All Company, access them through the following URL: https://engage.cloud.microsoft/domain-name/#/groups/company/insights. Substitute your organization’s domain name in the address.
- You can promote other users from the Viva Engage experience as admins of All Company to better manage the community. 
- All Company is sorted like all other communities. Users can favorite the All Company community to move it to the top of their communities list. 

These settings aren't available for network admins:

- Related communities
- Post to this community by email
- Deletion of All Company from the Viva Engage UI.  
- Changes to All Company privacy and data classification through Viva Engage settings

#### Is my All Company community Microsoft 365-connected, and what does being connected mean?

Today, networks can have communities that are all connected, all unconnected, or a mix of connected and unconnected.

A connected All Company indicates that a Microsoft 365 Group ("Group") was created. In Native Mode, All Company is always a connected community.

#### What is the benefit of All Company backed by a Group?

The key differences between an All Company that's connected to a Microsoft 365 Group and an unconnected All Company are:

- A connected All Company community creates a Group.
- A connected All Company can have Live Events.
- A connected All Company has [Microsoft 365 Resources](./viva-engage-and-office-365-groups.md).

The process for confirming that All Company is connected is the same as any other community. 

In the **Network Admins** settings, if **Enforce Office 365 Identity** is selected, your network has an All Company community that's connected to a Microsoft 365 Group. If  **Enforce Office 365 Identity** isn't selected, All Company isn't connected to a Group.

#### If the All Company community is connected, what should I be aware of?

- You can delete All Company in Microsoft Entra ID, which takes it through a soft-delete and then a hard-delete process.
- The Office 365 Expiration policy is enabled for All Company by default when connected.
- Privacy and Data Classification for All Company can be changed in Microsoft Entra ID. If privacy is set to private for All Company, users can't post or view the All Company group.

#### How do these changes to All Company affect my existing SharePoint web part and embed scenarios? 

If you use All Company in a SharePoint web part or embed scenario, your All Company feed will be empty. To  see your All Company feed, add the All Company community.  

For more information about the various SharePoint web parts and embed features, see Related articles.

## Related articles

[Viva Engage and Microsoft 365 Groups](viva-engage-and-office-365-groups.md)

[Use a Viva Engage web part in SharePoint Online](https://support.microsoft.com/office/a53cfa0c-3d09-42c8-a286-1038a81c59da)

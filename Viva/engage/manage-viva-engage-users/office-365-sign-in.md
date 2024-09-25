---
title: "Microsoft 365 sign-in for Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/24/2024
audience: Admin
ms.topic: overview
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: b1745e3c-d4d7-4e20-a155-ebf85106b998
description: "Choose the authentication method to use for Microsoft 365 and Viva Engage: directory sync, single sign-on (SSO), or Microsoft 365 sign-in. Add Viva Engage to the Office 365 navigation bar."
---

# Microsoft 365 sign-in for Viva Engage

Microsoft 365 sign-in lets users access Viva Engage with their Microsoft 365 identity. A single identity is preferable because:
  
- You can easily [Manage Viva Engage users across their life cycle in Microsoft 365](manage-users-across-their-lifecycle.md), in addition to managing Viva Engage administrators in Microsoft 365.
    
- Users can navigate between Viva Engage and Microsoft 365 without signing in under a separate username and password. From the Microsoft 365 app launcher, users can quickly switch back and forth between Viva Engage and Microsoft 365 services such as Outlook, SharePoint Online sites, and OneDrive for Business.
  
## How it works

**If a Microsoft 365 user visits Viva Engage for the first time from Microsoft 365** Viva Engage tries to connect their Microsoft 365 account to their existing Viva Engage account, if available. For the connection to be successful, the email addresses must match. When a user signs in with Microsoft 365, Viva Engage first tries to map the Microsoft 365 user's primary email, then proxy emails, and then the user principal name (UPN). If there are no matches, a new Viva Engage user is created.
  
**If a user visits Viva Engage through https://engage.cloud.microsoft**, Viva Engage checks whether the user has successfully signed in to Microsoft 365 at least once. This check ensures that the user has Microsoft 365 credentials and prevents the user from being locked out of an existing Viva Engage network if a Microsoft 365 deployment is underway. 

**If the user hasn't signed in to Microsoft 365**, they'll continue to use their legacy Viva Engage identity to access Viva Engage. A delay of a few hours often occurs between the time the user successfully signed in and the time Viva Engage can detect it.

*If you want to instantly use Microsoft 365 sign-in for Viva Engage, have users first sign in to Microsoft 365, and then access Viva Engage from the tile on the app launcher.*
  
>[!NOTE]
> Once a user connects and starts using Microsoft 365 sign-in for Viva Engage, they can no longer use their previous legacy Viva Engage identity to sign in. At this point, you'll need to manage the lifecycle of this user from Microsoft 365.
  
## How do I enable Microsoft 365 sign-in for Viva Engage?

Viva Engage detects when a Microsoft Entra account exists for a user and uses the Microsoft 365 sign-in for Viva Engage. We strongly recommend that admins [Enforce Microsoft 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md).
  
## Enforce Microsoft 365 sign-in for all users in the network

You can choose to enforce Microsoft 365 sign-in for Viva Engage for all users in the network, effectively disabling the legacy Viva Engage identity (where users sign in with email, password). After this is enforced, all users in the network must use Microsoft 365 accounts for sign-in. For more information, see [Enforce office 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md).
  
## Use Viva Engage with other Microsoft 365 services

Viva Engage integrates seamlessly with other services in Microsoft 365. For example, you can share [Stream or Microsoft 365 Video](https://techcommunity.microsoft.com/t5/microsoft-stream-blog/microsoft-stream-the-future-of-video-in-microsoft-365/ba-p/3969156) and [Group and share documents in Delve](https://support.microsoft.com/en-us/office/group-and-share-documents-in-delve-da0c5804-01ef-4edd-8b87-e576b19bef3e) with other users using Viva Engage. 
  
## Make Viva Engage the default enterprise social network in SharePoint

By default, when users select **Conversations** in SharePoint, they see their SharePoint newsfeed (Outlook groups), rather than Viva Engage conversations. You can make Viva Engage the default enterprise social network in SharePoint. With this, when users select **Conversations** in SharePoint, they see their Viva Engage conversations, rather than the SharePoint newsfeed (Outlook groups).
  
> [!NOTE]
> You must be an Microsoft 365 Global Administrator to make this change. For more information about permissions levels, see [About Microsoft 365 admin roles](/microsoft-365/admin/add-users/about-admin-roles). 
  
1. In Microsoft 365, go to **Admin** \> **SharePoint**.
    
2. Select **Settings**.

3. Choose **Classic settings page**.
    
4. Under **Enterprise Social Collaboration**, choose **Use Yammer.com service**.
  
5. Select **Save**.

  > [!NOTE]
  > This change can take up to 30 minutes to complete. 
  
## Frequently asked questions

**Q: Can I access Microsoft 365 and Viva Engage on my phone with just one sign-in account?**

A: Yes! Microsoft 365 identity can be used to access Viva Engage from any device or app. You can use it to access Viva Engage from the browser, from Viva Engage Embed, from third party Viva Engage apps and the Viva Engage apps for your phone/tablet. Use the same Microsoft 365 identity to access other Microsoft 365 services, such as OneDrive for Business or Outlook.

**Q: Do users have to do anything to make this work?**

A: Your network users should access Viva Engage once with their Microsoft 365 identity (this action connects the Microsoft 365 identity to Viva Engage). After this, users should sign in to Viva Engage again on all of their devices and apps.
    
**Q: I'm using Microsoft 365 SSO and the Microsoft 365 sign-in for Viva Engage, so what happens if Microsoft 365 is federated with an on-premises environment?**

A: The Microsoft 365 sign-in for Viva Engage automatically respects any Microsoft 365 federation setting.
    
**Q: Can I combine Viva Engage networks in order to take advantage of Microsoft 365 sign-in for Viva Engage?**

A: Yes, this is required as of October 16, 2018. For more information, see [Network migration: Consolidate multiple Viva Engage networks](../configure-your-viva-engage-network/consolidate-multiple-networks.md).

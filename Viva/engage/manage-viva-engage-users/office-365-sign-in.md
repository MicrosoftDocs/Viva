---
title: "Office 365 sign-in for Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 7/27/2023
audience: Admin
ms.topic: overview
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: b1745e3c-d4d7-4e20-a155-ebf85106b998
description: "Choose the authentication method to use for Office 365 and Viva Engage: directory sync, single sign-on (SSO), or Office 365 sign-in for Viva Engage. Add Viva Engage to the Office 365 navigation bar."
---

# Office 365 sign-in for Viva Engage

Office 365 sign-in for Viva Engage lets users access Viva Engage with their Office 365 identity. This is the preferred authentication model for Viva Engage because when you use the same identity: 
  
- You can easily manage the Viva Engage service in Office 365. For example, you can [Manage Viva Engage users across their life cycle from Office 365](manage-users-across-their-lifecycle.md), and you can manage Viva Engage administrators in Office 365.
    
- Users can seamlessly go to Viva Engage from Office 365 without having to sign in with a separate username and password. From the Office 365 app launcher, a user can quickly switch back and forth between Viva Engage and other Office 365 services including Outlook, SharePoint Online sites, and OneDrive for Business.
  
## How it works

When Office 365 users visit Viva Engage for the first time from Office 365, Viva Engage tries to connect their Office 365 account to their existing Viva Engage account, if available. The email address of the Office 365 user account must match the existing Viva Engage account email address for the connection to be successful. When a user signs in with Office 365, Viva Engage first tries to map the Office 365 user's primary email, then proxy emails, and then the user principal name (UPN). If there are no matches, a new Viva Engage user is created.
  
If the user visits Viva Engage through https://engage.cloud.microsoft, Viva Engage checks that the user has successfully signed in to Office 365 at least once. This check ensures that Office 365 credentials have been provided to the user. It also prevents users from being locked out of an existing Viva Engage network if the Office 365 deployment is underway. If the user hasn't signed in to Office 365, they'll continue to use their legacy Viva Engage identity to access Viva Engage. A delay of a few hours often occurs between the time the user successfully signed in and the time Viva Engage can detect it. If you want to instantly use Office 365 sign-in for Viva Engage, have users sign in to Office 365 first, and then access Viva Engage using the Viva Engage tile on the app launcher.
  
This is how it works:
  
After a user is connected and using Office 365 sign-in for Viva Engage, the user can no longer use their previous legacy Viva Engage identity to sign in. At this point, you'll need to manage the lifecycle of this user from Office 365.
  
## How do I enable Office 365 sign-in for Viva Engage?

Viva Engage detects when a Microsoft Entra account exists for a user and uses the Office 365 sign-in for Viva Engage. We strongly recommend that admins [Enforce Office 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md).
  
## Enforce Office 365 sign-in for all users in the network

You can choose to enforce Office 365 sign-in for Viva Engage for all users in the network, effectively disabling the legacy Viva Engage identity (where users sign in with email, password). After this is enforced, all users in the network will need to use Office 365 accounts for sign-in. For more information, see [Enforce office 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md).
  
## Use Viva Engage with other Office 365 services

Viva Engage integrates seamlessly with other services in Office 365. For example, you can share [Stream or Office 365 Video](/stream/streamnew/new-stream) and [Group and share documents in Office Delve](https://support.office.com/article/da0c5804-01ef-4edd-8b87-e576b19bef3e#BKMK_WorkTogetherByUsingViva Engage) with other users using Viva Engage. 
  
## Make Viva Engage the default enterprise social network in SharePoint

By default, when users select **Conversations** in SharePoint, they see their SharePoint newsfeed (Outlook groups), rather than Viva Engage conversations. You can make Viva Engage the default enterprise social network in SharePoint. With this, when users select **Conversations** in SharePoint, they see their Viva Engage conversations, rather than the SharePoint newsfeed (Outlook groups). 
  
> [!NOTE]
> You must be an Office 365 global administrator to make this change. For more information about permissions levels, see [About Office 365 admin roles](https://support.office.com/article/DA585EEA-F576-4F55-A1E0-87090B6AAA9D). 
  
1. In Office 365, go to **Admin** \> **SharePoint**.
    
2. Select **Settings**.

3. Choose **Classic settings page**.
    
4. Under **Enterprise Social Collaboration**, choose **Use Yammer.com service**.
  
5. Select **Save**.
    
    > [!NOTE]
    > This change can take up to 30 minutes to complete. 
  
## Frequently asked questions

**Q: Can I access Office 365 and Viva Engage on my phone with just one sign-in account?**
    
A: Yes! Office 365 identity can be used to access Viva Engage from any device or app. You can use it to access Viva Engage from the browser, from Viva Engage Embed, from third party Viva Engage apps and the Viva Engage apps for your phone/tablet. And you'll use the same Office 365 identity to access other Office 365 services such as OneDrive for Business or Outlook.
    
**Q: Do users have to do anything to make this work?**

A: Your network users should access Viva Engage once with their Office 365 identity (this action connects the Office 365 identity to Viva Engage). After this, users should sign in to Viva Engage again on all of their devices and apps.
    
**Q: I'm using Office 365 SSO and the Office 365 sign-in for Viva Engage, so what happens if Office 365 is federated with an on-premises environment?**

A: The Office 365 sign-in for Viva Engage automatically respects any Office 365 federation setting.
    
**Q: Can I combine Viva Engage networks in order to take advantage of Office 365 sign-in for Viva Engage?**

A: Yes, this is required as of October 16, 2018. For more information, see [Network migration: Consolidate multiple Viva Engage networks](../configure-your-viva-engage-network/consolidate-multiple-networks.md).

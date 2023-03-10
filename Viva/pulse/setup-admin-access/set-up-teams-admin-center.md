---
title: Set up Viva Pulse in the Teams admin center
description: "Set up Viva Pulse in the Teams admin center"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 03/08/2023
ms.topic: article
ms.service: viva
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
ROBOTS: NOINDEX, NOFOLLOW
---

# Set up Viva Pulse in the Teams admin center

> [!NOTE]
> This article applies to a preview version of Microsoft Viva Pulse. You must be in the Private Preview program to access it. Features are subject to change.

## Prerequisites

You will need to have Microsoft Teams deployed for your organization to use Viva Pulse in Microsoft Teams. Viva Pulse will also be available as a Web experience for which users will not need a Microsoft Teams license.

## Admin roles and permissions

To set up Viva Pulse, you’ll need the following permissions:

To set up Viva Pulse and manage individual licensing, you'll need these permissions:
* [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles)
* Viva Pulse Admin
* [Microsoft Teams admin](/microsoftteams/using-admin-roles)

The Microsoft 365 Global Admin has global access to most management features and data across Microsoft online services. For Viva Pulse, the Global Admin can install and pin the Viva Pulse app in Microsoft Teams, assign a user to the Viva Pulse Admin role, and manage in-app Viva Pulse settings as well.

The Viva Pulse Admin is an Azure Active Directory (Azure AD) role that can be assigned to any user in the organization by the Microsoft 365 Global Admin. As a Viva Pulse Admin, you can configure the app for tenant wide usage, including setting up the minimum default confidentiality threshold, customization capabilities to personalize the Pulse requests, and deletion of user data. For more information, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference#knowledge-administrator).

The Microsoft Teams Admin can pin and install the Viva Pulse Admin in Teams for a customer tenant.

## Set up Viva Pulse in Microsoft Teams

The following settings are optional and are not required to be completed before users in the organization can start using Viva Pulse.

Viva Pulse is enabled by default for all Microsoft Teams users in your organization. You can turn Viva Pulse off or on at the tenant level    on the Manage apps page in the Microsoft Teams admin center. For more information, see [Manage your apps in the Microsoft Teams admin center](/microsoftteams/manage-apps).

To allow or block specific users in your organization from using Viva Pulse, make sure Viva Pulse is turned on for your organization on the Manage apps page in the Microsoft Teams admin center and create a custom app permission policy and assign it to those users. For more information, see [Manage app permission policies in Teams](/microsoftteams/teams-app-permission-policies).

## Deploy Viva Pulse to your users

Viva Pulse is available to users from the Microsoft Teams app store. For more information, see [Learn how to add apps to Teams](https://support.microsoft.com/en-us/office/add-an-app-to-microsoft-teams-b2217706-f7ed-4e64-8e96-c413afd02f77).
---
title: Set up Microsoft Viva Learning in the Teams admin center
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 10/27/2021
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
ms.custom: admindeeplinkTEAMS
ms.localizationpriority: medium
description: Learn how to get Microsoft Viva Learning and manage it in the Teams admin center.
---

# Set up Microsoft Viva Learning in the Teams admin center

## Prerequisites

You'll need to have Microsoft Teams deployed for your organization in order to use Viva Learning.

## Licensing

Your Microsoft 365 or Office 365 Enterprise subscription includes Viva Learning with basic features. However, you'll need a Viva Learning or Viva Suite license to access premium features. [Learn more about licensing](https://www.microsoft.com/microsoft-viva/learning?rtc=1).

## Admin roles and permissions

To set up learning content sources in Viva Learning and manage individual licensing, you'll need these permissions:

- [Microsoft Teams admin](/microsoftteams/using-admin-roles)
- [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles) or [SharePoint admin](/sharepoint/sharepoint-admin-role)
- [Knowledge admin](/azure/active-directory/roles/permissions-reference#knowledge-administrator)

The knowledge admin is an Azure Active Directory (Azure AD) role in the Microsoft 365 admin center that can be assigned to anyone in the organization. This role manages the organization's learning content sources through the Microsoft 365 admin center. For more information, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference#knowledge-administrator) and [Overview of Microsoft Learning](overview-viva-learning.md).

## Set up Viva Learning

Viva Learning is enabled by default for all Microsoft Teams users in your organization. You can turn off or turn on Viva Learning at the organization level on the **Manage apps** page in the Microsoft Teams admin center. For more information, see [Manage your apps in the Microsoft Teams admin center](/microsoftteams/manage-apps).

To allow or block specific users in your organization from using Viva Learning, make sure Viva Learning is turned on for your organization on the **Manage apps** page in the Microsoft Teams admin center. Then create a custom app permission policy and assign it to those users. For more information, see [Manage app permission policies in Teams](/microsoftteams/teams-app-permission-policies).

## Deploy Viva Learning to your users

Viva Learning is available to users from the Microsoft Teams app store. [Learn how to add apps to Teams](https://support.microsoft.com/office/add-an-app-to-microsoft-teams-b2217706-f7ed-4e64-8e96-c413afd02f77).

## Next steps

[Manage content sources for Viva Learning in the Microsoft 365 admin center](content-sources-365-admin-center.md)

[Configure how content shows up in Viva Learning](use-tabs.md)

---
title: Access Viva Glint with Azure Active Directory
description: To access the Microsoft Viva Glint application, a Global administrator must first register Viva Glint in an Azure Active Directory (Azure AD) tenant.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: Access, authentication, login, AAD, Azure Active Directory, Azure AD, sign in 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 06/20/2023
---

# Access Viva Glint with Azure Active Directory

To access the Microsoft Viva Glint application, a Global administrator must register Viva Glint in an Azure Active Directory (Azure AD) tenant. A service administrator must also import users to Viva Glint. Users must exist in both Azure AD and Viva Glint with the same email address to successfully access the application.

>[!NOTE]
> To add a Support or Partner user to Viva Glint, follow this guidance: [Add an external user to Viva Glint.](https://go.microsoft.com/fwlink/?linkid=2240483)

## Set up and manage a Viva Glint Azure Active Directory tenant

For information on tenant creation, user and group creation, bulk user maintenance, authentication options, and how to enable single sign-on with Azure AD, see the following articles:

- [Set up a Microsoft Viva Glint tenant](https://go.microsoft.com/fwlink/?linkid=2230741)
- [Create users and groups in Azure Active Directory](/training/modules/create-users-and-groups-in-azure-active-directory/)
- [Perform bulk user maintenance in Azure Active Directory](/training/modules/manage-user-accounts-licenses-microsoft-365/7-perform-bulk-user-maintenance-azure-active-directory)
- [What authentication and verification methods are available in Azure Active Directory?](/azure/active-directory/authentication/concept-authentication-methods)
- [Enable single sign-on for an enterprise application](/azure/active-directory/manage-apps/add-application-portal-setup-sso)

>[!TIP]
> Add all users in Azure AD to minimize friction for ongoing role and data access changes for Viva Glint users. Control Viva Glint User Role membership and permissions in the Viva Glint application.

## Import users to Viva Glint

The Global administrator adds service administrators to Azure AD and Viva Glint for initial access. As the service administrator, see information below to add other users (HR, leadership, managers, individual contributors) to Viva Glint.

> [!NOTE]
> Email addresses for users in Viva Glint must match email addresses tied to users in Azure AD. Coordinate with the Global administrator for your Viva Glint Azure AD tenant to ensure that these email addresses match.

### Understand prerequisites for importing users

To import users to Viva Glint, first follow critical data preparation steps:

- [Finalize file layout](https://go.microsoft.com/fwlink/?linkid=2230914)
- [Set up attributes in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742)

### Import users

After employee data preparation and attribute setup:

- [Upload employee data to Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742)
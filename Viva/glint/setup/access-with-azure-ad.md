---
title: Access Viva Glint with Microsoft Entra ID
description: To access the Microsoft Viva Glint application, a Global administrator must first register Viva Glint in a Microsoft Entra tenant.
ms.author: SarahBerg
author: SarahAnneBerg
manager: elizapo
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

# Access Viva Glint with Microsoft Entra ID

To access the Microsoft Viva Glint application, a Global administrator must register Viva Glint in a Microsoft Entra tenant. A service administrator must also import users to Viva Glint. Users must exist in both Microsoft Entra ID and Viva Glint with the same email address to successfully access the application.

>[!NOTE]
> To add a Support or Partner user to Viva Glint, follow this guidance: [Add an external user to Viva Glint.](https://go.microsoft.com/fwlink/?linkid=2240483)

<a name='set-up-and-manage-a-viva-glint-azure-active-directory-tenant'></a>

## Set up and manage a Viva Glint Microsoft Entra tenant

For information on tenant creation, user and group creation, bulk user maintenance, authentication options, how to enable single sign-on, and federation, see the following articles:

- [Set up a Microsoft Viva Glint tenant](https://go.microsoft.com/fwlink/?linkid=2230741)
- [Create users and groups in Microsoft Entra ID](/training/modules/create-users-and-groups-in-azure-active-directory/)
- [Perform bulk user maintenance in Microsoft Entra ID](/training/modules/manage-user-accounts-licenses-microsoft-365/7-perform-bulk-user-maintenance-azure-active-directory)
- [What authentication and verification methods are available in Microsoft Entra ID?](/azure/active-directory/authentication/concept-authentication-methods)
- [Enable single sign-on for an enterprise application](/azure/active-directory/manage-apps/add-application-portal-setup-sso)
- [What is federation with Microsoft Entra ID?](/entra/identity/hybrid/connect/whatis-fed)
- [Microsoft Entra Connect and federation](/entra/identity/hybrid/connect/how-to-connect-fed-whatis)
- [Microsoft Entra federation compatibility list](/entra/identity/hybrid/connect/how-to-connect-fed-compatibility)

>[!TIP]
> Add all users in Microsoft Entra ID to minimize friction for ongoing role and data access changes for Viva Glint users. Control Viva Glint User Role membership and permissions in the Viva Glint application.

## Import users to Viva Glint

The Global administrator adds service administrators to Microsoft Entra ID and Viva Glint for initial access. As the service administrator, see information below to add other users (HR, leadership, managers, individual contributors) to Viva Glint.

> [!NOTE]
> Email addresses for users in Viva Glint must match email addresses tied to users in Microsoft Entra ID. Coordinate with the Global administrator for your Viva Glint Microsoft Entra tenant to ensure that these email addresses match.

### Understand prerequisites for importing users

To import users to Viva Glint, first follow critical data preparation steps:

- [Finalize file layout](https://go.microsoft.com/fwlink/?linkid=2230914)
- [Set up attributes in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742)

### Import users

After employee data preparation and attribute setup:

- [Upload employee data to Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742)

---
ms.date: 05/17/2024
title: "Set up Viva Engage"
description: "Guidance for setting up licensing and installation of Viva Engage for an organization."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.collection:  
- M365initiative-viva
- highpri
- essentials-get-started
search.appverid:
- MET150
---
# Set up Viva Engage

To set up Microsoft Viva Engage, you must have Microsoft 365 Global administrator or Engage administrator permissions.

## Set up licensing for Viva Engage

**Core experience**

As a foundational component of Microsoft Viva Engage, the Core Service Plan provides essential features and capabilities to enhance engagement and collaboration within your organization.

- **If you *don't* enforce Viva Engage licensing**, users can access the Viva Engage Core experience.<br>
- **If you *do* enforce Viva Engage licensing**, users can still access the Viva Engage Core experience. However, each user must be assigned:<br>

    - a Microsoft 365 license, *and*
    - a Viva Engage Core Service Plan (or Yammer Enterprise Service Plan)

**Premium experience**

 Your organization can enjoy premium Viva Engage experiences if your tenant owns either of these plans:

- Microsoft Viva Suite
- Microsoft Viva Employee Communications and Communities

>[!NOTE]
>Administrators do not need a premium Viva Engage license to configure premium Viva Engage and Answers experiences. Learn more about [managing licenses in Microsoft 365](/Viva/engage/manage-engage-licenses-microsoft-365).

|Service plan |Enables |Comes with this product |
|-------------------|---------|-------|
|**Viva Engage Core**|Engage core experiences and the Answers in Viva core experiences <br> *Example:* Communities, storyline |Microsoft 365|
|**Viva Employee Communities and Communications**|Engage premium experiences <br> *Example:* Leadership corner, AMAs (Ask Me Anything), storyline announcements, delegation, analytics, campaigns |Microsoft Viva Suite|
|**Viva Engage Knowledge**|[Answers in Viva premium experience](/viva/engage/eac-answers-overview-set-up#licensing) |Microsoft Viva Suite|

## Configure and review privacy and security settings

The Engage administrator (Yammer administrator) can manage Viva Engage content and security settings.
For details, see [Overview of security & compliance for Viva Engage](/viva/engage/manage-security-and-compliance/security-and-compliance).

## Set up Viva Engage

Where you set up Viva Engage is a matter of preference. Global and Engage admins (Yammer administrators in Microsoft Entra ID) can use the Microsoft 365 admin center for initial setup. The Engage admin center provides most Viva Engage settings and customization options. To control some Viva features, such as Copilot in Viva Engage, you must use [Microsoft 365 feature access management](/viva/feature-access-management).

From the Microsoft 365 admin center, you can:

- Assign [Engage and Answers admins](eac-key-admin-roles-permissions.md)
- Pin Viva Engage in Teams
- Manage other settings in Viva Engage


## Configure privacy and security settings

The Engage admin (Yammer administrator) can manage data, privacy, and security settings in Viva Engage. Learn how to protect Viva Engage data and comply with evolving legal and regulatory standarts in this [overview of security & compliance](/viva/engage/manage-security-and-compliance/security-and-compliance).


## Install Viva Engage

### Install Viva Engage in Teams

The Microsoft Teams admin can to deploy and pin the app for all users, or for particular departments, through a [Teams app setup policy](/microsoftteams/teams-app-setup-policies). Setup policies allows users to easily set up Viva Engage themselves, using the following steps:

1. Open Teams on the web or in a desktop client.
2. From the left side of Teams, select **Apps**.
3. Search for Viva Engage.
4. Select the Viva Engage app, and then select **Add**. The app is added to all your Teams clients, including mobile.

### Install or access Viva Engage on other surfaces

You can direct users to other installation options, such as:

- [Install the Viva Engage desktop app](https://prod.support.services.microsoft.com/en-au/office/install-the-viva-engage-desktop-app-66ccb412-ca1d-4e43-872c-9705abf11b1b)
- [Install Viva Engage on your iOS or Android phone](https://support.microsoft.com/en-us/office/set-up-viva-engage-on-your-mobile-phone-e52e65ad-14fa-4db9-b8f7-80fe3f6e25a7)
- [Access Viva Engage on the web](https://engage.cloud.microsoft.com/)

## Customize the appearance for Viva Engage in the Teams store

You can customize the appearance for the following properties of the Viva Engage app in the Teams app store:

- app name
- app description
- app icons
- accent color

Customizing the Viva Engage app is ideal for companies that tailor their network branding to fit their corporate identity.

> [!NOTE]
> Currently, customizations don't affect the Viva Engage app branding that appears _within_ the Viva Engage Experience. Learn more about [customizing details of an app](/MicrosoftTeams/customize-apps#customize-details-of-an-app).
 
## Support adoption of Viva Engage
 
Review the contents of the [Viva Engage Adoption page](https://adoption.microsoft.com/en-us/viva/engage/) to help you get started, train and engage your organization, build champions, and secure your environment. If you’re setting up the premium Viva Engage experience, you’ll need to assign admin roles specific to Viva Engage to ensure usage and successful adoption of its many premium features

### See also
[Admin roles and permissions in Viva Engage](eac-key-admin-roles-permissions.md)

---
title: Set up Microsoft Viva Amplify
ms.reviewer: smathurin
ms.date: 08/10/2023
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-amplify
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-amplify
  - Tier1
ms.localizationpriority: medium
description: Learn how to set up Viva Amplify for your organization.
---
# Set up Microsoft Viva Amplify
  
Viva Amplify centralizes campaign management, publishing, and reporting so corporate communicators can reach and engage all employees meaningfully. Using multi-channel publishing, communicators can reach employees across Outlook, Teams, and SharePoint. Users can create and manage organization-wide campaigns to help inform organizations, create alignment, and inspire action – all from one place. Employees will continue to see relevant messages in their existing preferred channels.

Viva Amplify is a web experience and is automatically enabled for users with the required licensing.

## Licensing for Viva Amplify

The **Viva Amplify** and **Viva Amplify - Organizational data** service plans are enabled for licensed users of the following products:

- Microsoft Viva [Learn more about setting up Microsoft Viva](/viva/setup-microsoft-viva)
- Microsoft Viva Employee Communities & Communications
- Microsoft Viva for Faculty
- Microsoft Viva with Glint add-on
- Microsoft Viva with Glint add-on for Faculty

## Product limitations

- **Vanity URLs**: At launch, Viva Amplify may have limitations when used with vanity URLs. If your company has a vanity URL, please reach out to your support contact to discuss the best approach for rolling out our product within your organization.
- **Localization** At launch, Viva Amplify is available exclusively in English. More languages are planned for future releases.

### Assign admin roles

>[!IMPORTANT]
>Users need both SharePoint admin and Groups admin roles to be able to manage settings in Viva Amplify.

First, familiarize yourself with [roles in Viva Amplify.](viva-amplify-roles.md)

1. Sign into your Microsoft 365 admin center and navigate to **Viva Amplify**.
1. Choose **Assign SharePoint Administrator Role settings**.
1. Search for a user by entering their name or email.
1. Select the user(s) for whom you want to assign the **SharePoint Administrator** role.
1. Choose **Assign Groups Administrator Role settings**.
1. Search for a user by entering their name or email.
1. Select the user(s) for whom you want to assign the **Groups Administrator** role.
1. Select **Add**.

You can also assign roles from your Microsoft 365 admin center by navigating to **Roles** > **Role assignment**.

## Manage organizational data

## Manage campaign settings

## Manage campaign creation

Viva Amplify is designed so that users with a wide range of roles, such as project managers who do regular status reports for stakeholders, can benefit from using campaigns. You can use the admin controls in Amplify to restrict who can create campaigns:

- The default setting enables everyone in the organization to create campaigns with Amplify.
- You can choose to only allow specific people or security groups to create campaigns.

>[!IMPORTANT]
>Users who you want to be able to create campaigns need to have **Site creation** and **Group creation** permissions in SharePoint. [Learn how to assign these permissions in the SharePoint admin center.](/sharepoint/manage-site-creation)

## Manage campaigns in the SharePoint admin center

As with SharePoint sites, Viva Amplify campaigns can be managed in the **Active sites** page of your SharePoint admin center. Here, you can view campaigns in your organization. [Learn more about managing sites and campaigns.](/sharepoint/manage-sites-in-new-admin-center)

## Delete campaigns

As a Global admin or SharePoint admin, you can delete a Viva Amplify campaign using the same method you would to delete a SharePoint site. Deleted campaigns are stored for a set amount of time based on your organization's retention policies. [Learn more about how to delete a campaign](/sharepoint/delete-site-collection).

>[!IMPORTANT]
>Make sure to notify the campaign owner and any subsite owners before you delete a campaign so they can move their data to another location if needed.

Deleting a campaign deletes everything within it, including:

- Campaign publications
- Document libraries and files
- Lists and list data
- Campaign settings and history
- Any subsites and their contents

## Restore a previously deleted campaign

>[!NOTE]
>You need SharePoint administrator permissions to restore a deleted campaign.

Just like with SharePoint sites, you can restore deleted Viva Amplify campaigns. [Learn more about how to restore a deleted campaign](/sharepoint/restore-deleted-site-collection).

## Manage sensitivity labels for campaigns

Viva Amplify campaigns adhere to the same sensitivity label classifications that govern SharePoint sites. This means that if sensitivity labels were enabled for your organization for your Microsoft Team sites, Microsoft 365 groups, and SharePoint sites, it can also be applied to Viva Amplify campaigns. [Learn more about sensitivity labels](/purview/sensitivity-labels-teams-groups-sites).

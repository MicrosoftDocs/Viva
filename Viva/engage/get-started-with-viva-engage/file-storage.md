---
title: "Viva Engage file storage overview"
description: "Where files are stored in Viva Engage depends on whether the network uses Microsoft 365 connected groups."
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 01/04/2024
audience: Admin
ms.topic: article
ms.service: viva
ms-subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
---

# Viva Engage file storage overview

Files uploaded to Viva Engage in Microsoft 365 connected Viva Engage groups are stored in the group's default SharePoint document library. These files can be accessed from within Viva Engage.

For information about using Viva Engage files stored in SharePoint, see the following articles:

- [Where are my Viva Engage files stored?](https://support.microsoft.com/en-us/office/how-do-i-tell-where-my-viva-engage-files-are-being-stored-fadfdefa-e00d-40b6-94cb-a9ddb171a443)

- [Edit a previously uploaded file when your Viva Engage connected group now stores files in SharePoint](https://support.microsoft.com/en-us/office/edit-a-previously-uploaded-file-when-your-viva-engage-connected-group-now-stores-files-in-sharepoint-4b2cfde2-871e-4f0d-9936-db5a57ef5f87?ui=en-us&rs=en-us&ad=us)

## Benefits

For network and tenant administrators:

- SharePoint has a rich set of security and compliance features that apply to files uploaded in Viva Engage for Microsoft 365 connected Viva Engage groups, including eDiscovery, data loss protection, and in-geo residence for files at rest.  

For end users:
  
- A familiar user interface for file navigation and management in SharePoint.

- Greater discoverability and easier access through Microsoft search.

    Users with appropriate permissions can find and access the files through Viva Engage, SharePoint, and other Microsoft 365 resources by using browse or search in SharePoint and Delve.  

- Offline access to files by syncing a SharePoint folders to a folder on their computer.  

## What determines where a file is stored

Files are stored in SharePoint when they're uploaded to a Microsoft 365 connected Viva Engage group. This includes:  
  
- Files that are attached to a message in a Microsoft 365 connected Viva Engage group.  

- Files that are uploaded to a group from the **Files** page of a Microsoft 365 connected Viva Engage group.

- Files that are attached to an email that is sent to a Microsoft 365 connected Viva Engage group.

 > [!NOTE]
 > Any policies configured on the SharePoint document library take precedent over the Viva Engage upload admin configuration when a user tries to upload a file in a connected Viva Engage community.
  
Files continue to be stored in Viva Engage cloud storage in the following instances:

- If the Viva Engage network doesn't use Microsoft 365 connected groups. This includes:

  - Microsoft 365 tenants that have more than one Viva Engage network  
  
  - Viva Engage networks that don't enforce Office 365 identity  

  - Yammer Basic networks  

- When the location the file is being uploaded to isn't a Microsoft 365 connected Viva Engage group:

    - Groups that aren't Microsoft 365 connected groups, including All Company, external groups, and secret groups
  
    - Viva Engage private messages

        >[!NOTE]
        > Existing files stored in Viva Engage legacy storage will not be moved to SharePoint.  

- If your organization is using a third-party app that uses Yammer Files APIs:

  - If we detect that you're currently using the Yammer Files APIs, even if you're using connected groups, files for your tenant will be stored in legacy storage until your app is updated to be an Azure Marketplace app that calls Yammer APIs. We’ll share details on how to create an Azure Marketplace Yammer app soon. If you're a developer and have questions about this change, email api@yammer-inc.com.

    >[!IMPORTANT]
    > If you create a third-party app that uses Files APIs after your organization has received the Viva Engage files in SharePoint feature, file calls will fail. Users will see an HTTP 401 error (unauthorized client error) because the Yammer OAuth token doesn't include claims from Microsoft Entra ID, which is required for accessing files stored in SharePoint.

 > [!NOTE]
 > Moving a conversation to a Microsoft 365 connected Viva Engage group won't change where the file is stored.
  
## Where files are stored in SharePoint

Files that users upload in Microsoft 365 connected groups are saved in the **Apps > Viva Engage** subfolder of the SharePoint document library for the Microsoft 365 connected group. The SharePoint document library can be accessed from Viva Engage under **Microsoft 365 Resources** or **Office 365 Resources** on the right side of a Microsoft 365 connected Viva Engage group, as well as through SharePoint itself.

 > [!NOTE]
 > We recommend that you do not delete, move, or rename files in the **Apps > Viva Engage** subfolder.
  
## Guest access to files

The following table shows how each type of guest can access files uploaded in Viva Engage and stored in SharePoint.

| Type of user | Access to group files in Viva Engage | Access to group files in SharePoint |
|----------|----------|----------|
|**Conversation-level guest that is in your network**|**Private group**: Can view files that have been shared in the conversation, but can't upload files.<br/>**Public group**: Can view, edit, and upload files.|Conversation level guests can't access any files saved in SharePoint nor upload any files. If you want to enable access to specific files in the conversation, add them as an Azure B2B guest on the Office 365 tenant. File upload isn't permitted.|
|**Network-level guest that is also an Azure B2B guest, and also a member of the group in Microsoft 365**|Can view, edit, and upload files.|These Azure B2B guests can view, upload, or edit files from the SharePoint Document library only. File access from Viva Engage isn't permitted.|
|**Azure B2B guest, but not a member of the group<br/>Network-level guest<br/>Conversation-level guest that isn't in your network**|Automatic file access isn't allowed. These users can request access to specific files.<br/>Can't upload files.|Automatic file access isn't permitted. Guests can request access to specific files. File upload isn't permitted.|
|**Network-level guest, but not Azure B2B guest**|Automatic file access isn't allowed. A guest must become an Azure B2B guest and a member of the group in Microsoft 365. Alternatively, other group members can grant access to specific files or the entire document library through one of many SharePoint external sharing methods.|No automatic access for network level guests to Viva Engage files saved in SharePoint. If you want to enable access to specific files, add them as an Azure B2B guest on the Office 365 tenant. For more information, see [Microsoft Entra B2B documentation](/azure/active-directory/b2b/). If guests need to upload files to a specific group from SharePoint or have automatic access to files uploaded to SharePoint, add them as a group member in SharePoint.|

> [!NOTE]
> Membership in the group for guests in Microsoft Entra ID and Viva Engage are completely separate. Deleting a network-level guest from a Microsoft 365 connected Viva Engage group or from the tenant in Microsoft Entra ID doesn't remove the user in Viva Engage, and deleting a user from Viva Engage doesn't delete the user from a Microsoft 365 group or Microsoft Entra ID.

For more information about Microsoft Entra B2B guests, see [Guest access in a Microsoft Entra B2B](/azure/active-directory/b2b/what-is-b2b).

## Requirements

- Viva Engage version requirements

    Ensure your users are using the most recent Viva Engage versions. At a minimum, users should be using the following or newer versions:

    - Viva Engage on iOS - 7.33.0  

    - Viva Engage on Android - 5.5.84

    - Viva Engage desktop on Windows or Mac - 3.4.2

- Cookie and browser requirements

    To store Viva Engage files in SharePoint, we use the ADAL library and use Microsoft Entra ID tokens for authentication. If browsers don’t have third-party cookies enabled or if the security zone settings are incorrect in Internet Explorer 11 or Edge, the ADAL library used to refresh Microsoft Entra tokens can't send information needed to Microsoft Entra ID.

    > [!NOTE]
    > Microsoft 365 apps and services doesn't support Internet Explorer 11 as of August 17, 2021. (Microsoft Teams doesn't support Internet Explorer 11 earlier, as of November 30, 2020.) [Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666). Note that Internet Explorer 11 remains a supported browser. Internet Explorer 11 is a component of the Windows operating system and [follows the lifecycle policy](/lifecycle/faq/internet-explorer-microsoft-edge) for the product on which it is installed.

    When a token refresh call fails, users will see:

    - On the Viva Engage page for a connected group, Microsoft 365 Resources are dimmed

    - File operations fail

    - Viva Engage live events can't be created.

     For more information, see [A silent sign-in request was sent but no user is signed in](https://github.com/AzureAD/azure-activedirectory-library-for-js/wiki/FAQs#q6-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in).

    To avoid problems:

    - Ensure that no extensions (such as Ghostery) block or prevent reading of cookies.

    - In Internet Explorer 11 or Microsoft Edge, ensure protected mode is disabled for the trusted zone.

        Include **engage.cloud.microsoft** and related URLs as a part of trusted zone. For more information, see [Microsoft 365 URLs and IP address ranges](/microsoft-365/enterprise/urls-and-ip-address-ranges)

    - In complex environments, especially those using wildcard configurations such as *.fabrikam.com, additional effort may be required to find the right configuration. URLs may need to be moved between zones, or replaced with the absolute versions in some cases.

    - Users shouldn’t access Viva Engage using incognito or InPrivate mode or equivalent modes in other browsers.

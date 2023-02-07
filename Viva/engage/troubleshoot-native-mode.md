---
title: "Troubleshoot your Viva Engage network for Native Mode for Microsoft 365"
f1.keywords:
- NOCSH
ms.author: pamgreen
author: v-jebizie
manager: pamgreen
ms.date: 01/21/2020
audience: Admin
ms.topic: article
ms.service: yammer
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
description: "Troubleshoot issues with your Viva Engage network in Native Mode for Microsoft 365."
---

# Troubleshoot problems with Native Mode for Microsoft 365

## What is Native Mode?

### What benefits are new to Native Mode?

Viva Engage premium functionality is only available to networks in Native Mode. Networks in Native Mode can also [perform eDiscovery](overview-native-mode.md) on their home network through the Security & Compliance Portal, just like they do for other Microsoft 365 products. In addition, administrators and users both benefit by having an experience that is more consistent within Viva Engage and within the Microsoft 365 ecosystem.

 > [!NOTE]
> Native Mode is strongly recommended for reasons of security, compliance, and Microsoft 365 integration.

### What is required for me to be in Native Mode for Microsoft 365 in Viva Engage?

While all networks provisioned after January 2020 are in Native Mode by default, existing networks will need to use our Alignment Tool ("Tool") to have their network enter Native Mode. To use the Tool, your network must enforce Microsoft 365 Identity. There must also only be one (primary) home network on the Microsoft 365 tenant. Once a network satisfies those two criteria, the Alignment Tool can be used to address any incompatibilities of your network with a Native Mode network.

#### Are there more licensing requirements when moving to native mode?

Native Mode doesn't have any other licensing requirements beyond those required for [Microsoft 365 and Microsoft 365 plans that include Groups](/yammer/configure-your-yammer-network/yammer-and-office-365.md).

### What features aren't supported in Native Mode and why aren't they supported?

- *Native Mode doesn't support private unlisted groups*: AAD and Microsoft 365 Groups don't support this feature, so it isn't possible for us to offer it in Native Mode networks. The downloadable Alignment Tool report will provide you with information on the quantity and usage of private unlisted groups in your network.

- *Native Mode doesn't support external communities*: Hybrid and non-native mode external collaboration capabilities, including external communities, aren't compatible with [Azure B2B](/azure/active-directory/external-identities/). Native Mode networks can host B2B guests in M365 Groups-backed communities. Users from Native Mode networks can, if allowed by your Viva Engage Security Settings, collaborate in external communities in other Viva Engage networks that aren't in Native Mode. In addition, External Networks will continue to be supported for Native Mode Viva Engage networks in the US Geo.

Azure Active Directory (Azure AD) business-to-business (B2B) collaboration lets you securely share your company's applications and services with guests from any other organization, while maintaining control over your own corporate data.

The downloadable Alignment Report will provide you with information on the quantity and usage of external groups in your network.

- *Native Mode doesn't support network-level guests*: For greater network security, guests cannot be given access to an entire Viva Engage network. The downloadable Alignment Report will provide you with information on the quantity and activity of guests in your network.

- *External participants*: Viva Engage currently allows users to add external participants to individual threads. This feature isn't available for Viva Engage Enterprise networks that are in Native Mode or the [EU Geo](/yammer/manage-security-and-compliance/manage-data-compliance.md). This feature isn't compatible with the Azure B2B guest model, and so won't be supported in Native Mode networks.

- *File uploads in Viva Engage Private messages*: In order to be in Native Mode, all files uploaded in Viva Engage must be stored in SharePoint. Since Viva Engage private messages don't store files in SharePoint or OneDrive for Business, the Alignment Tool must delete any previously uploaded private message files. Users will no longer be able to upload files in private messages. The downloadable Alignment Report will provide you with information on the quantity of files previously uploaded in private messages.

### What is the main difference between Native Mode and eDiscovery?

- *Native Mode* - A state where all the users, groups, and content from your network are compatible with (and mapped to) their counterparts in AAD/Microsoft 365 and Microsoft 365.

- *eDiscovery* - A Yammer feature Microsoft now provides to customers through the [Microsoft Purview compliance portal](https://go.microsoft.com/fwlink/?linkid=2132455).  

Viva Engage can offer eDiscovery to customers once all their Users, Groups, and Content can be discoverable through the Security and Compliance Center. To facilitate this process, Viva Engage must ensure that all Groups are Microsoft 365 connected because eDiscoverable content must be saved in the group mailbox. Similarly, users must have an AAD account.

### What can you include in communications to your users?

Below is some content you can use as-is or modify to meet your needs when you're ready to communicate upcoming changes to your organization. For example, this is how you might draft an email to your users:

----------------EXAMPLE----------------

*Hello NAME OF EMPLOYEE,*

*We are getting our Viva Engage network ready to support required compliance and security policies for our organization.*

*Here are some changes you will see rolling out over the next few weeks:*

*- All unlisted private groups will become private listed groups on DATE. Non-members will be able to see the group in search results and other areas, but only members can access the content. If you don't want your group to be visible to non members, you must delete it before that date. You can also change the name of the group if the concern is that people will identify the purpose of the group based on the name.*

*- All network, group, and conversation-level guests from our Viva Engage network will be removed on DATE. If you're working with people outside of our Viva Engage network, you should figure out an alternate way to communicate with them.*

*- All Viva Engage group files will be stored in SharePoint beginning on DATE. This means previously uploaded group files will be migrated to SharePoint and all new group file uploads will be saved to SharePoint.*

*- All files that were previously uploaded on Viva Engage private messages will be deleted on DATE. No new files can be uploaded in Viva Engage private messages.*

*- Beginning DATE users will need to have Microsoft 365 Group creation rights in order to create a group in Viva Engage. If you don't currently have Microsoft 365 Group creation rights, you will no longer be able to create groups in Viva Engage. Reach out to your manager if you don't have Microsoft 365 Group creation rights, but feel you need to do so to perform your job.*

*Your IT team*

## Migration

### What can end users expect during migration?

The majority of end users can expect no change in their Viva Engage experience while the Tool runs. If end users are accustomed to creating communities in Viva Engage, they will need M365 group creation rights to continue doing so during migration. We recommend that you communicate the expected process changes to your end users early in the migration planning process.

### How do I check the status of my network's migration to Native Mode?

Any Global Admin from your tenant can check the status of your network's alignment to Native Mode by accessing the Engage admin center. On the **Setup & configuration** tab, they can access **Configure tenant**, which will then route them to the Yammer admin center. In the Yammer admin center, they can click on **native mode** to see their progress.

## Networks

### Should I align my network to be in Native Mode?

Yes. Hybrid and non-native networks will be migrated to Native Mode automatically throughout 2023 and it is strongly recommended that you initiate the process on your own when you are prepared. In addition, all Viva Engage premium functionality requires that your network be in Native mode. 

### Is it possible for a network that is in Native Mode to get out of Native Mode?

No. Once a network is in Native Mode, it isn't possible for it to get out of Native Mode. We recommend administrators carefully review the documentation we provide on Native Mode before beginning the process because *it is unstoppable and irreversible*.  

### How does a network enter Native Mode for Microsoft 365?

**New Networks**
All new networks provisioned after January 2020 are in Native Mode by default.

**Existing Networks**
Existing networks will be able to upgrade to Native Mode by using the Microsoft 365 Alignment Tool.

## Files

### How does Viva Engage in Native Mode handle file migration?

Once a Viva Engage group is connected, the Alignment Tool migrates all files previously uploaded to Viva Engage to SharePoint. When files are moved to the SharePoint document library, only the latest version is moved over, and the version history isn't copied.

### Why does the Alignment Tool delete messages and files from deleted groups and deleted users?

Deleted groups and deleted users don't typically have a mailbox, which means content associated with that group or user wouldn't be available for eDiscovery. Therefore, we need to remove that content from Native Mode networks in order to offer an eDiscovery solution in the Compliance Center that includes all conversations and files in your Native Mode network.

### How does Viva Engage in Native Mode handle file name conflicts?

It is possible that files previously uploaded to Viva Engage won't comply with SharePoint filename restrictions. When migration completes, the IT admin gets a report of any file name conflicts. Update the file names and make sure there are no file names with the following invalid characters before running the Tool again:

- "
- \*
- :
- < >
- ?
- /
- \
- |

You won't be able to take your network to Native Mode for Microsoft 365 until you resolve any files left behind.

## Error Codes

If you receive errors in the report generated by the alignment tool, follow the steps in the table below to troubleshoot them. If you encounter an error code that isn't listed below, [contact the Microsoft support team](/microsoft-365/admin/contact-support-for-business-products?tabs=online).

|**Code** |**Description** | **Migration** |
|:--------|:-------------- |:------------- |
|CannotOpenFile--2147024816 |Can't open a file |Remove file |
|FilealreadyExists--2130575257 |File is in SharePoint already |Rename/remove |
|FileNameCharactersNotPermitted—2130575245 |[Characters not permitted in SharePoint exist in file name](https://support.office.com/article/invalid-file-names-and-file-types-in-onedrive-onedrive-for-business-and-sharepoint-64883a5d-228e-48f5-b3d2-eb39e07630fa)|Rename/remove 
|InvalidCharactersInPath--2147024809|[Characters not permitted in SharePoint exist in file name](https://support.office.com/article/invalid-file-names-and-file-types-in-onedrive-onedrive-for-business-and-sharepoint-64883a5d-228e-48f5-b3d2-eb39e07630fa)|Rename/remove|
|PathTooLong---2147024690---2130575338|[Filepath is too long](https://support.office.com/article/invalid-file-names-and-file-types-in-onedrive-onedrive-for-business-and-sharepoint-64883a5d-228e-48f5-b3d2-eb39e07630fa)|Rename/remove|
|SpFileDeleted---2130575338|File deleted in SharePoint|Upload again to SharePoint/ delete file|
|Unknown||Remove file/ [contact  support](/microsoft-365/admin/contact-support-for-business-products?tabs=online)|
| 

> [!NOTE]
> If you have a large number of files with disallowed characters, you can [contact Microsoft support](/microsoft-365/admin/contact-support-for-business-products?tabs=online) to obtain a script that renames files in a bulk process.

### What happens to the conversations and files from deleted Microsoft 365 Groups that are within their 30-day recovery window?

When the Alignment Tool is run, it'll remove the conversations and Viva Engage-hosted files for all deleted groups, whether the group is in a hard- or soft-deleted state. This means that if there are Viva Engage Microsoft 365 connected groups that were in the soft delete period when the Alignment Tool was run, those groups, if restored, would be restored without conversations and without any files that had been uploaded to Viva Engage. Group metadata and files that were uploaded to SharePoint would continue to be restored as they are in non Native Mode scenarios.

## Users and guests

### Network guests

- *Why aren't network guests supported in Native Mode?*

  Network guests in Viva Engage aren't currently Azure B2B guests, and so their userIDs aren't associated with an account in Azure Active Directory for your Microsoft 365 tenant. Since eDiscovery requires all users to be in AAD, the network-level guest feature can't be supported in Native Mode. B2B guests can be invited to collaborate at the community level in Native Mode networks.

- *What should I do about my existing network guests?*

  Most networks have never had any network guests. If your network has had network guests in the past, it's likely most of those guests no longer have access due to your network enforcing Microsoft 365 Identity.

  The downloadable Alignment Report provides information about the network guests in your network and their activity within the network. We recommend you use the information in the report to help you decide whether these users should continue to have access to the network. If you do want these users to have access to the network when your network is in Native Mode, you'll need to provide them with new credentials associated with an AAD account.

### What happens to users who don’t have Microsoft 365 Group creation rights?

If your network enforces Microsoft 365 Group creation rights, users without those rights will no longer be able to create communities in Viva Engage. We recommend that all users be able to create Viva Engage communities so that your entire organization can enjoy the benefits of an open, collaborative network.

### What about users who aren't in Azure Active Directory ("AAD")?

- *Why would I have users not in AAD in my network if I enforce Microsoft 365 Identity?*
  Enforcing Microsoft 365 Identity doesn't remove users from your network who left your organization prior to your organization enforcing Microsoft 365 identity. Most customers who do have users in their Viva Engage network that aren't in AAD; will find that these users haven't been active in the network since Microsoft 365 Identity was enforced for the network or, earlier.

- *Why would some of these users have recent activity?*
  At the time a network chooses to enforce Microsoft 365 Identity, the administrator can choose whether or not to log out all logged in users to the network. If your network didn't force all users to log out, it's possible that some of these users have remained active enough that they've remained logged in.

- *What should I do about users who aren't in AAD?*
  The downloadable Alignment Report provides information about which users in your Viva Engage network aren't in (or mapped to an account in) Azure Active Directory. We recommend you use the information in the report to help you decide whether these users should continue to have access to the network. You'll need to create a new AAD account for a user or invite them as a B2B guest if you want to provide continued Viva Engage access to users who don't currently have an AAD account. In some cases, these accounts may be service accounts or bots, rather than specific end users.

- *Why would a user not be in AAD?*
  There are multiple reasons why:

  - In some cases, the user was invited to the network, but has never logged into Viva Engage. These users are "pending" users.

  - The user hasn't needed to log in to Viva Engage since the network started enforcing Microsoft 365 identity. That is, they are using Viva Engage regularly enough, and with the same client, that they have remained logged in since the network began enforcing identity.

  - The user could be a network-level guest in the network. Network level guests aren't supported in AAD.

- *What does the Tool do for pending users?*
  The Tool will first try to associate the pending user with an account in AAD for your Microsoft 365 tenant. If that association is successful, the user will remain in the network. If we aren't able to associate the pending user with an AAD account on your tenant, then we'll delete the user from Viva Engage.  

### Why aren't external participants in individual conversations supported in Native Mode?

 This feature isn't currently compatible with the Azure B2B guest model. This feature isn't available for Viva Engage Enterprise networks that are in Native Mode or the [EU Geo](../manage-security-and-compliance/manage-data-compliance.md).

## Groups

### What do I need to do to prepare my All Company community to be Microsoft 365 connected?

There's no preparation required to make your All Company community Microsoft 365-connected. The Tool will connect the community and make the Verified Admins for the network community owners of the All Company community in AAD. As community owners, they'll be able to post announcements in the All Company community as they were able to do before All Company was Microsoft 365-connected.

- *How is All Company different than other Microsoft 365-connected groups?*
  The All Company community is different than other Viva Engage communities in that all users in the network are treated as members of the group without them needing to actually be a member of the group. Once All Company is connected, it is possible to add members to the group from AAD. However, we don't recommend that users be added as members because it won't change the behavior of the community within Viva Engage for those users.

- *Can I delete All Company once it is connected?*
  We don't recommend that you delete All Company, as it is an important way for your users to communicate broadly across your organization. Once All Company is Microsoft 365-connected, it is possible to delete the Microsoft 365 Group from the Microsoft 365 admin center or the Azure Active Directory admin center. If that's done, Viva Engage will honor the deletion and not show All Company in your network.

- *Can I make All Company private once it is connected?*
  A private All Company is an unsupported state in Viva Engage. In addition, we don't recommend that you make All Company private, as it is an important way for your users to communicate broadly across your organization. Once All Company is Microsoft 365-connected, it's possible to make it private from the Microsoft 365 admin center or the Azure Active Directory admin center. If that's done, Viva Engage won't show All Company in your network to anyone regardless of group membership.

### Why aren't external groups supported in Native Mode?

Because Viva Engage external groups aren't compatible with Azure B2B, guests in external groups in Viva Engage aren't associated with an account in Azure Active Directory for your Microsoft 365 tenant.

- *What should I do about my external groups?*
  The downloadable Alignment Report provides information about the use of external groups within your enterprise network so that you can determine the best path forward for your organization. Many organizations already block the ability to create external groups in their network—those companies won't be affected by this change.

  If your network does have external groups, we recommend you use the downloadable Alignment Report to see whether there are any external guests in the group, whether those guests have had any recent activity, as well as whether the group itself has had any recent activity. You can assess what actions to take on the group. On one hand, if the group has no external members, but has had recent activity by internal members, then you may opt to let the Tool make that group an internal only group. On the other hand, if you find the group has external members, but the group itself hasn't had any activity at all for some time, you may decide to delete the group before running the Tool.

  Whatever path you choose, we recommend you communicate clearly to the owners of these groups what changes are coming so that they can alert you. In some cases, these groups may be owned by senior leaders within your organization so, be sure to choose the appropriate communication channel when reaching out to group owners.

### How do unlisted private groups work?

- *Why can't I have unlisted private groups in Native Mode?*
  Azure Active Directory and Microsoft 365 Groups don't currently support having unlisted private groups. If Viva Engage continued to support this feature in a Native Mode network, groups would be unlisted in Viva Engage. However, these groups would be exposed through other Microsoft 365 products. The downloadable Alignment Report will provide you with information on the quantity and usage of private unlisted groups in your network.

- *What should I do about my unlisted private groups?*
  The downloadable Alignment Report provides information about the usage of private unlisted groups within your enterprise network so that you can determine the best path forward for your organization.

  If your network does have private unlisted groups, we recommend you use the downloadable Alignment Report to see whether there are any users or guests in the group, and whether those users or guests have had any recent activity in the group. You can assess what actions to take on the group. On one hand, if the group has had recent activity, but the group name doesn't contain any confidential or sensitive information, you may opt to let the Tool make that group an internal only group. On the other hand, if you find the group hasn't had any activity for some time, you may decide to delete the group before running the Tool.

  Whatever path you choose, we recommend you communicate clearly to the owners of these groups what changes are coming so that they can alert you. In some cases, these groups may be owned by senior leaders within your organization, so be sure to choose the appropriate communication channel when reaching out to group owners.  

### What happens to Groups without owners who have Microsoft 365 group creation rights?

- *Why do you need to add the global admin running the Alignment Tool as a group owner in groups that have no owner with Microsoft 365 group creation rights?*

  This change is done for either (1) groups without any owners, or (2) groups with owners, but none have Microsoft 365 Group creation rights. To make a Yammer community or group a Microsoft 365-connected group, it's necessary to have at least one group owner with Microsoft 365 Group creation rights. Because global admins have Microsoft 365 Group creation rights, adding the global admin as a group owner helps ensure that the group can become Microsoft 365-connected.

- *What should I do about my groups without owners with Microsoft 365 group creation rights?*

  The downloadable Alignment Report provides information about the groups within your enterprise network that don't have any group owners with group creation rights so that you can determine the best path forward for your organization. These groups include:

  - groups that have no owners
  - groups whose owners don't have Microsoft 365 group creation rights.

  If your network has many of these groups, you have a few options available to you.
  You can allow the Tool to add the global admin running the Tool to each group as an owner so that the group can become Microsoft 365-connected. Once a group is connected, you can, at your discretion, remove the global admin from having ownership of the group.
  
  You can also review the impacted groups from the downloadable Alignment Report and see if they have any recent activity or active group members. If they don't, you may elect to delete those groups before running the Tool. After those groups have been deleted, you can run the Tool. By deleting inactive groups before running the Tool, you'll reduce the number of groups to which you, as a global admin, need to be added to in order to achieve Native Mode.  

  You can grant Microsoft 365 Group creation rights to all users within your organization, or at least to the users that are owners of unconnected groups in Viva Engage, so that those groups can be connected without the global admin needing to be added as an owner. Once those groups are connected, you can choose whether to revoke group creation rights from some of those users who were granted access.

Whatever path you choose, we recommend you communicate clearly to the users in your network of the changes that are coming so that they can alert you of any concerns or potential issues.

## Related articles

[Overview of Native Mode](./overview-native-mode.md)

[Microsoft 365 Security & Compliance Portal](https://go.microsoft.com/fwlink/?linkid=2111321)

[Manage Yammer data compliance](../../../OfficeDocs-O365ITPro-pr/yammer/manage-security-and-compliance/manage-data-compliance.md)


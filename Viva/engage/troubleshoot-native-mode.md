---
ms.date: 12/14/2022
title: "Troubleshoot your Viva Engage network for Native Mode for Microsoft 365"
description: "Troubleshoot issues with your Viva Engage network in Native Mode for Microsoft 365."
ms.reviewer: ethli
ms.author: v-whitfieldd
author: dwhitfield233
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Troubleshoot problems with Native Mode for Microsoft 365

## What is Native Mode?

### What benefits are new to Native Mode?

Viva Engage premium functionality is only available to networks in Native Mode. Networks in Native Mode can also [perform eDiscovery](./overview-native-mode.md) on their home network through the Security & Compliance Portal, just like they do for other Microsoft 365 products. In addition, administrators and users both benefit by having an experience that's more consistent within Viva Engage and within the Microsoft 365 ecosystem.

 > [!NOTE]
> Native Mode is strongly recommended for reasons of security, compliance, and Microsoft 365 integration.

### What's required for me to be in Native Mode for Microsoft 365 in Viva Engage?

While all networks provisioned after January 2020 are in Native Mode by default, existing networks will need to use our Alignment Tool ("Tool") to have their network enter Native Mode. To use the Tool, your network must enforce Microsoft 365 Identity. There must also only be one (primary) home network on the Microsoft 365 tenant. If a network satisfies those two criteria, the Alignment Tool can be used to address any incompatibilities between the network and a Native Mode network.

#### Are there more licensing requirements when moving to native mode?

Native Mode doesn't have any licensing requirements beyond the requirements for [Microsoft 365 and Microsoft 365 plans that include Groups](/yammer/configure-your-yammer-network/yammer-and-office-365).

### What features aren't supported in Native Mode, and why aren't they supported?

- *Native Mode doesn't support private unlisted groups*: Azure Active Directory (Azure AD) and Microsoft 365 Groups don't support this feature, so we can't offer it in Native Mode networks. The downloadable Alignment Tool report can provide information about the quantity and usage of private unlisted groups in your network.

- *Native Mode doesn't support external communities*: Hybrid and non-native mode external collaboration capabilities, including external communities, aren't compatible with [Azure B2B](/azure/active-directory/external-identities/). Native Mode networks can host B2B guests in Microsoft 365 Groups-backed communities. Users from Native Mode networks can  collaborate in external communities in other Viva Engage networks that aren't in Native Mode your Viva Engage Security Settings allow this functionality. In addition, external networks are supported for Native Mode Viva Engage networks in the US geo.

Azure AD business-to-business (B2B) collaboration lets you securely share your company's applications and services with guests from any other organization while maintaining control over your own corporate data.

The downloadable Alignment Report provides information about the quantity and usage of external groups in your network.

- *Native Mode doesn't support network-level guests*: For greater network security, guests can't be given access to an entire Viva Engage network. The downloadable Alignment Report provides information about the quantity and activity of guests in your network.

- *External participants*: Viva Engage currently allows users to add external participants to individual threads. This feature isn't available for Viva Engage Enterprise networks that are in Native Mode or the [EU geo](/yammer/manage-security-and-compliance/manage-data-compliance). This feature isn't compatible with the Azure B2B guest model, so it's not and so won't be supported in Native Mode networks.

- *File uploads in Viva Engage Private messages*: To be in Native Mode, all files uploaded in Viva Engage must be stored in SharePoint. Because Viva Engage private messages don't store files in SharePoint or OneDrive for Business, the Alignment Tool deletes any previously uploaded private message files. Users will no longer be able to upload files in private messages. The downloadable Alignment Report provides information about the quantity of files previously uploaded in private messages.

### What is the main difference between Native Mode and eDiscovery?

- *Native Mode* - A state where all the users, groups, and content from your network are compatible with (and mapped to) their counterparts in Azure AD/Microsoft 365 and Microsoft 365.

- *eDiscovery* - A Yammer feature Microsoft now provides to customers through the [Microsoft Purview compliance portal](https://sip.compliance.microsoft.com/homepage).  

Viva Engage can offer eDiscovery to customers when all their users, groups, and content are discoverable through the Security and Microsoft Purview compliance portal. To facilitate this process, Viva Engage must ensure that all Groups are Microsoft 365-connected because eDiscoverable content must be saved in the group mailbox. Similarly, users must have an Azure AD account.

### What can you include in communications to your users?

Following is a sample email to users that you can use as is or modify to meet your needs when you're ready to communicate upcoming changes to your organization.

------------------------------

*Hello NAME OF EMPLOYEE,*

*We're getting our Viva Engage network ready to support required compliance and security policies for our organization.*

*Here are some changes you'll see rolling out over the next few weeks:*

*- All unlisted private groups will become private listed groups on DATE. Non-members will be able to see the group in search results and other areas, but only members can access the content. If you don't want your group to be visible to non-members, you must delete it before that date. You can also change the name of the group if the concern is that people will identify the purpose of the group based on the name.*

*- All network, group, and conversation-level guests from our Viva Engage network will be removed on DATE. If you work with people outside of our Viva Engage network, you should figure out an alternate way to communicate with them.*

*- All Viva Engage group files will be stored in SharePoint beginning on DATE. This means that previously uploaded group files will be migrated to SharePoint, and all new group file uploads will be saved to SharePoint.*

*- All files that were previously uploaded on Viva Engage private messages will be deleted on DATE. No new files can be uploaded in Viva Engage private messages.*

*- Beginning DATE, users need to have Microsoft 365 Group creation rights in order to create a group in Viva Engage. If you don't currently have Microsoft 365 Group creation rights, you'll no longer be able to create groups in Viva Engage. Contact your manager if you don't have Microsoft 365 Group creation rights but feel you need them to perform your job.*

*Your IT team*

## Migration

### What can end users expect during migration?

Most end users can expect no change in their Viva Engage experience while the Tool runs. If end users create communities in Viva Engage, they'll need Microsoft 365 group creation rights to continue doing this during migration. We recommend that you communicate the expected process changes to your end users early in the migration planning process.

### How do I check the status of my network's migration to Native Mode?

Any Global Admin from your tenant can check the status of your network's alignment to Native Mode through the Engage admin center: On the **Setup & configuration** tab, access **Configure tenant**, which will direct you to the Yammer admin center. In the Yammer admin center, select **native mode** to see =progress.

## Networks

### Should I align my network to be in Native Mode?

Yes. Hybrid and non-native networks will be migrated to Native Mode automatically throughout 2023. We strongly recommend that you initiate the process on your own when you're ready. In addition, all Viva Engage premium functionality requires that your network be in Native mode. 

### Can a network that's in Native Mode to get out of Native Mode?

No. Once a network is in Native Mode, it can't get out of Native Mode. We recommend that administrators carefully review the documentation we provide about Native Mode before beginning the process because *it's unstoppable and irreversible*.  

### How does a network enter Native Mode for Microsoft 365?

**New Networks**
All new networks provisioned after January 2020 are in Native Mode by default.

**Existing Networks**
Existing networks will can upgrade to Native Mode by using the Microsoft 365 Alignment Tool.

## Files

### How does Viva Engage in Native Mode handle file migration?

After a Viva Engage group is connected, the Alignment Tool migrates all files previously uploaded to Viva Engage to SharePoint. When files are moved to the SharePoint document library, only the latest version is moved over, and the version history isn't copied.

### Why does the Alignment Tool delete messages and files from deleted groups and deleted users?

Deleted groups and deleted users don't typically have a mailbox, which means content associated with that group or user wouldn't be available for eDiscovery. Therefore, we need to remove that content from Native Mode networks to offer an eDiscovery solution in the compliance portal that includes all conversations and files in your Native Mode network.

### How does Viva Engage in Native Mode handle file name conflicts?

Files previously uploaded to Viva Engage may not comply with SharePoint filename restrictions. When migration completes, the IT admin gets a report of file name conflicts. Update the file names and make sure there are no file names that contain the following invalid characters before you run the Tool again:

- "
- \*
- :
- < >
- ?
- /
- \
- |

You won't be able to take your network to Native Mode for Microsoft 365 until you resolve name issue for any files left behind.

## Error codes

If you receive errors in the report generated by the Alignment Tool, follow the steps in this table to troubleshoot. If you encounter an error code that isn't listed here, [contact the Microsoft support team](/microsoft-365/admin/contact-support-for-business-products?tabs=online).

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
> If you have many files with disallowed characters, you can [contact Microsoft support](/microsoft-365/admin/contact-support-for-business-products?tabs=online) to obtain a script that renames files in a bulk process.

### What happens to the conversations and files from deleted Microsoft 365 Groups that are within their 30-day recovery window?

When the Alignment Tool is run, it removes the conversations and Viva Engage-hosted files for all deleted groups, whether the group is in a hard-deleted or soft-deleted state. This means that if there are Viva Engage Microsoft 365-connected groups that were in the soft delete period when the Alignment Tool was run, those groups, if restored, would be restored without conversations and without any files that had been uploaded to Viva Engage. Group metadata and files that were uploaded to SharePoint would continue to be restored as they are in non-Native Mode scenarios.

## Users and guests

### Network guests

- *Why aren't network guests supported in Native Mode?*

  Network guests in Viva Engage aren't currently Azure B2B guests, and so their userIDs aren't associated with an account in Azure Active Directory for your Microsoft 365 tenant. Because eDiscovery requires all users to be in Azure AD, the network-level guest feature can't be supported in Native Mode. B2B guests can be invited to collaborate at the community level in Native Mode networks.

- *What should I do about my existing network guests?*

  Most networks have never had any network guests. If your network has had network guests in the past, it's likely most of those guests no longer have access due to your network enforcing Microsoft 365 Identity.

  The downloadable Alignment Report provides information about the network guests in your network and their activity within the network. We recommend you use the information in the report to help decide whether these users should continue to have access to the network. If you do want these users to have access to the network when your network is in Native Mode, you'll need to provide them with new credentials associated with an Azure AD account.

### What happens to users who don’t have Microsoft 365 Group creation rights?

If your network enforces Microsoft 365 Group creation rights, users who lack those rights will no longer be able to create communities in Viva Engage. We recommend that all users be able to create Viva Engage communities so that your entire organization can enjoy the benefits of an open, collaborative network.

### What about users who aren't in Azure Active Directory?

- *Why would I have users not in Azure AD in my network if I enforce Microsoft 365 Identity?*
  Enforcing Microsoft 365 Identity doesn't remove users from your network who left your organization prior to your organization enforcing Microsoft 365 identity. Most customers who do have users in their Viva Engage network that aren't in Azure AD determine that these users haven't been active in the network since Microsoft 365 Identity was enforced for the network or earlier.

- *Why would some of these users have recent activity?*
  At the time a network chooses to enforce Microsoft 365 Identity, the administrator can choose whether or not to log out all logged-in users of the network. If your network didn't force all users to log out, it's possible that some of these users have stayed active enough that they've remained logged in.

- *What should I do about users who aren't in Azure AD?*
  The downloadable Alignment Report provides information about which users in your Viva Engage network aren't in (or mapped to an account in) Azure AD. We recommend that you use the information in the report to help you decide whether these users should continue to have access to the network. If you want to provide continued Viva Engage access to users who don't currently have an Azure AD account, you need to create a new Azure AD account for them or invite them as a B2B guest. In some cases, these accounts may be service accounts or bots, rather than specific end users.

- *Why would a user not be in Azure AD?*
  There are multiple possible reasons:

  - In some cases, the user was invited to the network but has never logged into Viva Engage. These users are "pending" users.

  - The user hasn't needed to log in to Viva Engage since the network started enforcing Microsoft 365 identity. That is, they're using Viva Engage regularly enough, and with the same client, that they have remained logged in since the network began enforcing identity.

  - The user could be a network-level guest in the network. Network-level guests aren't supported in Azure AD.

- *What does the Tool do for pending users?*
  The Tool first tries to associate the pending user with an account in Azure AD for your Microsoft 365 tenant. If that association is successful, the user will remain in the network. If the tool is unable to associate the pending user with an Azure AD account on your tenant, the user is deleted from Viva Engage.  

### Why aren't external participants in individual conversations supported in Native Mode?

 This feature isn't currently compatible with the Azure B2B guest model. This feature isn't available for Viva Engage Enterprise networks that are in Native Mode or the [EU geo](/yammer/manage-security-and-compliance/manage-data-compliance).

## Groups

### What do I need to do to prepare my All Company community to be Microsoft 365 connected?

There's no preparation required to make your All Company community Microsoft 365 connected. The Tool connects the community and assigns the Verified Admins for the network community as owners of the All Company community in Azure AD. As community owners, they'll be able to post announcements in the All Company community, as they were able to do before All Company was Microsoft 365 connected.

- *How is All Company different than other Microsoft 365-connected Groups?*
  The All Company community is different than other Viva Engage communities in that all users in the network are treated as members of the group without them needing to actually be a member of the group. Once All Company is connected, it is possible to add members to the group from Azure AD. However, we don't recommend that users be added as members because it won't change the behavior of the community in Viva Engage for those users.

- *Can I delete All Company once it's connected?*
  We don't recommend that you delete All Company, as it's an important way for your users to communicate broadly across your organization. Once All Company is Microsoft 365 connected, it's possible to delete the Microsoft 365 Group from the Microsoft 365 admin center or the Azure Active Directory admin center. If that's done, Viva Engage will honor the deletion and not show All Company in your network.

- *Can I make All Company private once it's connected?*
  A private All Company is an unsupported state in Viva Engage. In addition, we don't recommend that you make All Company private, as it's an important way for your users to communicate broadly across your organization. Once All Company is Microsoft 365 connected, it's possible to make it private from the Microsoft 365 admin center or the Azure Active Directory admin center. If that's done, Viva Engage won't show All Company in your network to anyone regardless of group membership.

### Why aren't external groups supported in Native Mode?

Because Viva Engage external groups aren't compatible with Azure B2B, guests in external groups in Viva Engage aren't associated with an account in Azure AD for your Microsoft 365 tenant.

- *What should I do about my external groups?*
  The downloadable Alignment Report provides information about the use of external groups in your enterprise network so you can determine the best path forward for your organization. Many organizations already block the ability to create external groups in their network. Those companies won't be affected by this change.

  If your network does have external groups, we recommend that you use the downloadable Alignment Report to see whether there are any external guests in the group, whether those guests have had any recent activity, and whether the group itself has had any recent activity. You can assess what actions to take on the group. On one hand, if the group has no external members, but has had recent activity by internal members, you might opt to let the Tool make that group an internal only group. On the other hand, if the group has external members, but the group itself hasn't had any activity at all for some time, you might decide to delete the group before you run the Tool.

  Whatever path you choose, we recommend that you communicate clearly to the owners of these groups what changes are coming so that they can alert you. In some cases, these groups may be owned by senior leaders within your organization so, be sure to choose the appropriate communication channel when reaching out to group owners.

### How do unlisted private groups work?

- *Why can't I have unlisted private groups in Native Mode?*
  Azure Active Directory and Microsoft 365 Groups don't currently support unlisted private groups. If Viva Engage continued to support this feature in a Native Mode network, groups would be unlisted in Viva Engage. However, these groups would be exposed through other Microsoft 365 products. The downloadable Alignment Report provides information about the quantity and usage of private unlisted groups in your network.

- *What should I do about my unlisted private groups?*
  The downloadable Alignment Report provides information about the use of private unlisted groups in your enterprise network so you can determine the best path forward for your organization.

  If your network has private unlisted groups, we recommend that you use the Alignment Report to see whether there are any users or guests in the group and whether those users or guests have had any recent activity in the group. You can assess what actions to take on the group. On one hand, if the group has had recent activity but the group name doesn't contain any confidential or sensitive information, you might opt to let the Tool make that group an internal-only group. On the other hand, if the group hasn't had any activity for some time, you might decide to delete the group before you run the Tool.

  Whichever path you choose, we recommend that you communicate clearly to the owners of these groups what changes are coming so that they can alert you. In some cases, these groups may be owned by senior leaders within your organization, so be sure to choose the appropriate communication channel when reaching out to group owners.  

### What happens to groups without owners who have Microsoft 365 group creation rights?

- *Why do you need to add the global admin who runs the Alignment Tool as a group owner in groups that have no owner with Microsoft 365 group creation rights?*

  This change is done for either groups without any owners or groups with owners, but none have Microsoft 365 Group creation rights. To make a Yammer community or group a Microsoft 365-connected group, at least one group owner must have Microsoft 365 Group creation rights. Because global admins have Microsoft 365 Group creation rights, adding the global admin as a group owner helps ensure that the group can become Microsoft 365 connected.

- *What do I do about my groups without owners who have Microsoft 365 group creation rights?*

  The downloadable Alignment Report identifies groups in your enterprise network that don't have group owners with group creation rights so that you can determine the best path forward for your organization. These groups include:

  - Groups that have no owners.
  - Groups whose owners don't have Microsoft 365 group creation rights.

  If your network has many of these groups, you have a few options available to you.

  - You can allow the Tool to add the global admin who runs the Tool to each group as an owner so that the group can become Microsoft 365-connected. After a group is connected, you have the option to remove the global admin from having ownership of the group.
  
  - You can also review the impacted groups from the downloadable Alignment Report and see if they have any recent activity or active group members. If they don't, you might elect to delete those groups before you run the Tool. After those groups have been deleted, you can run the Tool. If you delete inactive groups before you run the Tool, you reduce the number of groups to which you, as a global admin, need to be added to in order to achieve Native Mode.  

  - You can grant Microsoft 365 Group creation rights to all users in your organization or at least to the users that are owners of unconnected groups in Viva Engage, so that those groups can be connected without adding the global admin as an owner. After those groups are connected, you can choose whether to revoke group creation rights from those users who you granted access.

Whichever option you choose, we recommend that you communicate clearly to the users in your network of the changes that are coming so that they can alert you of any concerns or potential issues.

## Related articles

[Overview of Native Mode](./overview-native-mode.md)

[Microsoft 365 Security & Compliance Portal](https://go.microsoft.com/fwlink/?linkid=2111321)

[Manage Yammer data compliance](/yammer/manage-security-and-compliance/manage-data-compliance)

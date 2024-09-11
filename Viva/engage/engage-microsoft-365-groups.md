---
ms.date: 09/10/2024
title: "Viva Engage and Microsoft 365 Groups"
description: "Viva Engage communities can access Microsoft 365 services, including a SharePoint team site and document library, OneNote notebook, plan in Planner, and Power BI workspace."
ms.reviewer: auhosford
ms.author: v-bvrana
author: Starshine89
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Viva Engage and Microsoft 365 Groups

If your Viva Engage network is eligible, you can use communities connected to Microsoft 365 Groups in Viva Engage.

You can tell that a community in Viva Engage is connected to Microsoft 365 Groups if you see the **Microsoft 365 Resources** section in the right navigation pane of the Viva Engage community:

:::image type="content" alt-text="Screenshot showing Microsoft 365 resources." source="../media/195dd76c-6007-469e-9242-7889a3b217a9.png":::


## Advantages of using communities connected to Microsoft 365 Groups

Communities that are connected to Microsoft 365 have many advantages over communities that aren't connected:

- Access Microsoft 365 services (SharePoint site and document library, OneNote notebook, and plan in Planner) from Engage. Microsoft 365 Groups also includes integration with services like Power BI.

- Create and host [live events](organize-live-event.md)
-  [Add apps to Viva Engage](https://support.office.com/article/Add-apps-to-viva-engage-bbb77f10-8779-4f3d-8096-db256f8653b8) with Microsoft 365 connectors
- Manage who can [create Microsoft 365 Groups](https://support.office.com/article/manage-who-can-create-office-365-groups-4c46c8cb-17d0-44b5-9776-005fced8e618)
- [Use dynamic groups](/viva/engage/manage-viva-engage-groups/create-a-dynamic-group) to update group membership automatically from Microsoft Entra ID
- Edit group membership from other Microsoft 365 apps.
- View the group in the Global Address List in Outlook
- Monitor usage through the [Microsoft 365 Groups activity report](https://support.office.com/article/Office-365-Reports-in-the-admin-center-Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40)
- Create optional [Microsoft 365 Groups naming policies](/azure/active-directory/enterprise-users/groups-naming-policy)
- Use the optional [Microsoft 365 Group Expiration Policy](/microsoft-365/admin/create-groups/office-365-groups-expiration-policy) to clean up unused groups.
- Use planned features only available with connected groups. This functionality includes getting local data center residency for newly uploaded files that are stored in SharePoint. See the [Microsoft 365 Roadmap](https://go.microsoft.com/fwlink/?LinkId=509914).
  
## Viva Engage configuration to use communities connected to Microsoft 365 Groups

To use communities connected to Microsoft 365 Groups in Viva Engage, make sure your Viva Engage network meets the following requirements:

- You must [enforce Microsoft 365 identity](/viva/engage/configure-your-viva-engage-network/enforce-office-365-identity) for Viva Engage users. When you first enforce Microsoft 365 identity, there's a seven-day trial period, after which the **Status** of your  **Microsoft 365 Identity Enforcement** changes to **Committed**.

- Since October 16, 2018, all Viva Engage networks must be in a 1:1 network configuration. This means that you have one Viva Engage network associated with one Microsoft 365 tenant. For more information, see [Consolidating multiple Viva Engage networks](/viva/engage/configure-your-viva-engage-network/consolidate-multiple-networks).

>[!NOTE]
> If you want to ensure that all of your communities are connected, align your network to Native Mode. To learn more, see [Overview of Native Mode](overview-native-mode.md).

Here's how the process works after your network becomes eligible for connected groups:

- About 24 hours after the **Status** in **Microsoft 365 Identity Enforcement** changes to **Committed**:
    - In the **Microsoft 365 (previously known as Office 365) Connected Viva Engage Groups** section, the **Status** for your network changes to **Enabled**.

    - Any new communities created in Viva Engage that are eligible are automatically connected to Microsoft 365 Groups.  

- After about one week, existing eligible communities are converted to communities connected to Microsoft 365 Groups.

 For a community to be eligible, the following criteria apply:

- The community owner must have Microsoft 365 Group creation privileges. By default, all Microsoft 365 users have this privilege.

- The community must be a public or private internal community. Unlisted private groups and external groups can't be connected to Microsoft 365 Groups.

- The community must have an owner, and it must have members.

## What happens when you create a new Viva Engage community connected to Microsoft 365 Groups

When you create a Viva Engage community connected to Microsoft 365 Groups, the new Microsoft 365 group is created, and a new SharePoint site and document library, OneNote notebook, and Planner are created. These resources are in addition to your regular Viva Engage community features. You can access these resources from the Viva Engage community page in Viva Engage.

>[!IMPORTANT]
> If you create a Microsoft 365 group from any other app, such as Outlook, it won't include Viva Engage. For the connected group to include Viva Engage, you must create the group in Viva Engage.

## Viva Engage networks in Native Mode

When your Viva Engage community is a Microsoft 365-connected group, you can manage many aspects of your group through the Microsoft 365 admin center, in addition to Viva Engage. You can manage all groups from Viva Engage networks that are in Native Mode through both admin centers. From the Microsoft 365 admin center, you can manage thes following:

- Add or remove group members
- Manage group ownership
- Delete a group
- Restore a deleted group
- Rename the group
- Update the group description
- Change the group's privacy setting

## Email and Microsoft 365 connected groups

In a connected group setup from Viva Engage, you can have group conversations in Viva Engage or in Outlook. If you send an email to a group in Viva Engage, it appears in the group's Viva Engage messages. Or, use the group's name from the Outlook global address list to send a group email directly to Outlook.

Your company can continue to use groups in Viva Engage and groups in Outlook based on which group type better fits the scenario for a team.
  
Email notifications for Viva Engage messages can be sent to users depending on the preferences that they've set in their Viva Engage notification settings. This setting applies both to connected and nonconnected groups.

## FAQ - Network eligibility

### I'm an admin. How do I know if my Viva Engage network is configured correctly and eligible for Viva Engage communities connected to Microsoft 365 Groups?
  
In the Viva Engage admin center, go to **Network Admin** > **Security Settings**. In the **Microsoft 365 (previously known as Office 365) Connected Viva Engage Groups** section, the status for your network shows as ***Enabled***.
  
### Can I disable Viva Engage connected to Microsoft 365 Groups?
  
No, but you can [manage who can create Microsoft 365 Groups](/office365/admin/create-groups/manage-creation-of-groups). 

### If I restrict users from creating Microsoft 365 groups for my tenant, are groups that are created by those restricted users Microsoft 365 connected?
  
No. Groups created by people who are restricted from creating Microsoft 365 groups won't be Microsoft 365 connected.
  
### If I have multiple Viva Engage networks mapped to Microsoft 365, will the Microsoft 365-connected Viva Engage groups work?
  
No. The Microsoft 365-connected Viva Engage groups experience works only for a Microsoft 365 tenant that's associated with a single Viva Engage network. See [Network migration: Consolidate multiple Viva Engage networks](./configure-your-viva-engage-network/consolidate-multiple-networks.md). This setup is required for all Viva Engage networks as of October 16, 2018.
  
### I don't want my existing groups to get connected to Microsoft 365. Can I turn this off?
  
No, but you can [manage who can create groups](/office365/admin/create-groups/manage-creation-of-groups), which also applies to conversion of existing groups. Only groups that have at least one admin who has group creation privileges can be connected to Microsoft 365.

If you apply new a creation policy, that policy won't retroactively change groups that are already connected to Microsoft 365. It only affects new groups.

### I have an unconnected group. How can I get it to be connected?

When your network first becomes eligible for connected groups, all groups that meet the criteria are converted to connected groups. After that, groups *are not* automatically connected if they become eligible. For example, say your network has Microsoft group creation policies applied, and you add a group admin with group creation permission. To have a group connected, you can submit a support request to have all eligible groups in your network connected.

## FAQ - General

### What type of Viva Engage communities can be connected to Microsoft 365 Groups?
  
Currently, only private and public internal communities can be connected to Microsoft 365 Groups.
  
### Can I make my Microsoft 365-connected Viva Engage community private and not list it in the Group Directory (secret)?
  
No. That setting isn't available for Microsoft 365-connected Viva Engage communities.

### Can I use an existing group or SharePoint site for a Microsoft 365-connected Viva Engage group?

No, a new group and resources specific to that new group are created when you create a Microsoft 365-connected community in Viva Engage. You can't connect a new Viva Engage community to an existing Microsoft 365 group, an existing SharePoint site or SharePoint document library, or an existing OneNote notebook.
  
### Can I hide a Microsoft 365-connected group from the Global Address Book?

Yes. Use the following cmdlet in PowerShell:

```Set-UnifiedGroup -Identity [group_name] -HiddenFromAddressListsEnabled $true```

For more information, see [Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup).

### Where can I create Viva Engage communities that are connected to Microsoft 365 Groups?
  
Viva Engage communities that are connected to Microsoft 365 Groups can only be created in Viva Engage. Microsoft 365 groups created in other locations don't include a Viva Engage community.
  
### Can I create a Viva Engage community connected to Microsoft 365 Groups from the Microsoft 365 admin center?
  
No, this functionality will be added in later waves. However, for Viva Engage communities connected to Microsoft 365 Groups, you can manage members and delete groups from the Microsoft 365 admin center. Metadata updates can also be applied to groups from the admin center.
  
### Can I add guests to Viva Engage communities connected to Microsoft 365 Groups?
  
No. This causes a sync failure because guests aren't managed by Microsoft Entra ID.
  
### How many members can my group have?
  
Because the upper limit of membership depends on how members interact with the associated resources provisioned with the Microsoft 365 group, there isn't a documented upper limit. However, we have seen customers who have Viva Engage communities with memberships ranging from 1,000 to more than 100,000 members. 
  
### What happens if I delete a Viva Engage community connected to Microsoft 365 Groups?
  
All the Microsoft 365 content associated with the community is deleted. This content includes the document library, OneNote notebook, and Planner plans. These resources are "soft-deleted," and can be restored by your administrator for up to 30 days.

### Does the Microsoft 365 group expiration policy apply to Viva Engage communities connected to Microsoft 365 Groups?

Yes. When a Microsoft 365 group is deleted because it expired, the Viva Engage community is deleted.

### Can I have a Viva Engage community connected to Microsoft 365 Groups that uses dynamic membership?

Yes. Any Microsoft 365-connected Viva Engage community can be converted to dynamic membership. See [Create a dynamic group](./manage-viva-engage-groups/create-a-dynamic-group.md) for requirements and limitations.
  
### In a connected group, are Viva Engage files and the SharePoint library the same thing?
  
No, these things are separate file storage locations. Members of the group have access to both locations. Files that are attached to Viva Engage messages or uploaded in a **Files** page are stored in Viva Engage cloud storage. Files that are uploaded directly to the group's SharePoint document library are stored in SharePoint.

We recommend that you store content that needs the structure and management capabilities of SharePoint in the group document library. For easy sharing of images and documents or to stream videos in Viva Engage, we recommend that you continue to use the default Viva Engage cloud storage.

>[!NOTE]
> As of December 2018, we are in process of rolling out Viva Engage files stored in SharePoint. When your network gets this new feature, new files uploaded to Viva Engage are stored in the group's SharePoint document library in the Apps/Viva Engage folder. Any files that were uploaded before your network gets this new feature remain in Viva Engage cloud storage. To find out where Viva Engage files are stored for your network, see [How do I tell where my Viva Engage files are stored?](https://support.office.com/article/7a647cb4-6005-4350-a258-68f00a5f7b29)
  
### Do my Viva Engage communities connected to Microsoft 365 Groups follow my Microsoft 365 Groups naming policy?
  
Yes. Any new community created in Viva Engage gets the added prefix and suffix from the group naming policy. Blocked words aren't allowed in the group name. For more information, see [Microsoft 365 Groups naming policy](https://support.office.com/article/6ceca4d3-cad1-4532-9f0f-d469dfbbb552).

>[!NOTE]
> Only Microsoft 365 groups created during migration to Native Mode to back existing communities don't follow the group-naming policy.

Viva Engage community names can't contain the following characters: @, #, [, ], <, or >. If the naming policy includes any of these characters, regular Viva Engage users can't create communities in Viva Engage.

<a name='q-can-i-use-my-viva-engage-communities-connected-to-microsoft-365-groups-with-group-based-licensing-in-azure-ad'></a>

### Can I use my Viva Engage communities connected to Microsoft 365 Groups with group-based licensing in Microsoft Entra ID?

By default, Viva Engage communities connected to Microsoft 365 Groups aren't compatible with Microsoft Entra group Based Licensing because the groups aren't security enabled.

## FAQ - Troubleshooting

### Only some of my communities were converted to Microsoft 365 groups. How do I get the rest of them converted?

When the automated conversion happened, it didn't convert communities that didn't meet the eligibility criteria. You can make the needed changes to make those communities eligible, and then [create a support ticket](/office365/admin/contact-support-for-business-products) to get them converted.

Before you open the support ticket:

- Make sure all groups have an owner, and the owners all have Microsoft 365 Group creation privileges.

- Make sure all groups have members.

- If you have unlisted (secret) groups, change them to private or public groups.

To find this information, do a data export and look in the groups.csv file. You must cross-reference the owner list with the list of people who have Microsoft 365 Group creation privileges.

### How long before changes to a Viva Engage community connected to Microsoft 365 Groups take effect in Viva Engage?

Changes to connected communities can take up to 24 hours to take effect throughout your network. Such changes include changes to group membership, permissions, name, and other settings.

## Related articles

[Manage who can create Microsoft 365 Groups](/office365/admin/create-groups/manage-creation-of-groups)

[Export data from Viva Engage](eac-as-manage-data.md)

---
title: "Network migration - Consolidate multiple Viva Engage networks"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 10/27/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MET150
- YAE150
ms.assetid: a22c1b20-9231-4ce2-a916-392b1056d002
description: Migrate one or more secondary networks into a primary Viva Engage Enterprise network (previously called 'Network merge').
---

# Network migration - Consolidate multiple Viva Engage networks

If you have multiple email domains in your Microsoft 365 tenant and those email domains are spread across two or more Viva Engage networks, we require that you consolidate into one Viva Engage network.
  
This article is only necessary if you have multiple Viva Engage networks, for example if your company has multiple business units or subsidiaries, each with its own Viva Engage network, that is on the same Microsoft 365 tenant.
  
Consolidation to one primary network helps get all your employees closely collaborating with each other, and simplifies management of your Viva Engage network.
  
Here are the basic steps:
  

|Step <br/> |Description <br/> |
|:-----|:-----|
|[Step 1: Plan](consolidate-multiple-networks.md#Plan) <br/> |Identify the Viva Engage networks to consolidate, identify data to export and upload, plan any needed changes to group structure and membership in the primary network, and plan communication with your users.  <br/> |
|[Step 2: Export content from primary networks](consolidate-multiple-networks.md#Export) <br/> |IMPORTANT: Migration only migrates users, not content. <br/>Export all content from secondary Viva Engage networks in order to access the content later. No one can access the secondary network after the migration begins. |
|[Step 3: Communicate with all users before the migration](consolidate-multiple-networks.md#Precommunicate) <br/> |Use the sample communication provided here to inform everyone on the secondary networks of the change, timing, what information is preserved, and the group structure in the primary network. Recommend that users save information they want to keep before the migration start date, such as files and data in conversations. Let primary network users know that more people are joining.  <br/> |
|[Step 4: Perform the network migration](consolidate-multiple-networks.md#self-service) <br/> |Run the network migration tool once for each secondary network. The tool migrates all users from the secondary Viva Engage network into the primary Viva Engage network, and turns off the secondary network. It doesn't migrate any conversations or files.  <br/> |
|[Step 5: Make primary network changes](consolidate-multiple-networks.md#parentchanges) <br/> |Adjust the structure of your primary Viva Engage network so it meets the needs of users who will be joining it. Create groups, invite members to the groups, and upload files that you exported.  <br/> |
|[Step 6: Communicate with all users after the migration](consolidate-multiple-networks.md#aftercommunicate) <br/> |Let everyone know the consolidated Viva Engage network is ready to use.  <br/> |

### Important things to know as you get started
  
- During the migration, only active and pending users, including the users' information, such as name and profile picture, are migrated.

  - If a user exists in a primary and secondary network, the user's account in the primary network will remain and if needed, will be promoted from a guest account to a regular account. The account in the secondary network will be deleted.

- Groups, conversations, and files aren't migrated. If you want any of this content from your secondary network, you must export it and upload it.

- After a migration completes, no-one can access the secondary Viva Engage network.

- Only users with the global admin role in Microsoft 365 can perform network consolidation.

- The primary and secondary Viva Engage networks must be on verified domains in one Microsoft 365 tenant. Consolidating Viva Engage networks across Microsoft 365 tenants isn't supported.

- Network migration can't be reversed.

- Multiple network migrations can be started back-to-back, without waiting for the previous ones to finish.

## Step 1: Plan

<a name="Plan"> </a>

Here are the main questions to ask during the planning step:
  
- Which Viva Engage networks need to be consolidated?

- Which network should be the primary network, and which are the secondaries?

- What role should users have in planning the consolidation? Consider using a Viva Engage group on each secondary network to help plan the changes.

- What's the timing? Do we need down-time? If so, what's the best time to schedule the consolidation?

- What's the best way to communicate with the users before and after the consolidation?

- What groups are necessary in the primary network for the users who are coming in from the secondary networks? Who should be in these groups? Who should be the admins for each group?

- For each secondary network, what content needs to be exported and loaded onto the primary network?

- Who will do each task: export the data from the secondary network, set up the group structure in the primary network, decide what data needs to be uploaded, upload that data, and communicate with users? Do you have the resources in-house to do this, or do you need a third-party to help?

    When you export data from a secondary network, you'll end up with CSV files containing group, user, admin, file, and conversation information, plus a folder that includes all the files from the network.

    If you plan to use this exported information to upload data or set up groups in your primary network, do the following:
    1. Identify who can help you upload data. Someone from your secondary network must identify content that is important going forward and map it to where it needs to go in the parent network.  
    2. After you determine what content is important, identify the skill set required to bring the content into your primary network. If there's a small amount of data, it can be done manually. But if you have extensive content in the secondary network, find someone comfortable using Windows PowerShell and the Yammer API. You may need to find a third-party to help you.
        - If you need to create new groups with specific people from the secondary network, or adding users from your secondary network to existing groups in your primary network, for each group, create CSV files with the group members to invite.
            - If you have just a few groups to add or modify, you can create these lists before migration (see Create a CSV file with emails for a group), and then for each group, invite members from your primary network after migration.
            - If you have many groups, find someone who can use PowerShell and the Yammer API. Ask them to generate the group membership changes from your secondary network before migration and to set up the groups in your parent network.
        - If you want to load files or messages from the secondary network, find someone who can use Windows PowerShell and the Yammer API to write scripts to load the data.

## Step 2: Export content from primary networks

<a name="Export"> </a>

For information about how to export all Viva Engage data for a secondary network, see [Export data from Viva Engage](../eac-as-manage-data.md).
  
- Exported files can be uploaded to the primary network. You must create a mapping between the file name and the location for the file in your primary network.

- Group names and group memberships aren't migrated. You can use the exported lists of groups and users to help you create appropriate groups in the primary network.

- Conversations aren't migrated, so secondary network users must save any needed data from conversations.

## Step 3: Communicate with all users before the migration

<a name="Precommunicate"> </a>

Use the sample communication below to let everyone on the secondary networks know the purpose of the change, the timing, what information will be kept, and the group structure in the primary network. Recommend that users save information they want to keep before the migration start date, such as files and data in conversations. Let primary network users know that more people are joining.

To communicate with all users on a network, you can use the Viva Engage **All Company** group. If you contact people by email, export the Viva Engage users list. For instructions, see [Export data from Viva Engage](../eac-as-manage-data.md). You can also get the email addresses for a specific group by [exporting Viva Engage group members to a CSV file](https://support.microsoft.com/topic/ecab40f5-c792-46a7-9450-9af572420d11).
  
**Sample pre-migration communication to people currently using secondary Viva Engage networks**

*We're consolidating all of our Viva Engage networks so that we can communicate more easily with each other. This migration starts on [date]. After the migration is complete, when you access Viva Engage using your regular work email address, you'll go directly to the new consolidated Viva Engage network.*<br/> 

*Important tasks to do before [date]: <br/> The consolidation doesn't move your Viva Engage content from [Contoso_sub1.com] to the [Contoso.com] Viva Engage network. You must save any files and conversations you want to keep.* <br/> 

*Save files: <br/> In Viva Engage, select the Settings icon, and then select **Files**.<br/> Use the **My Files** section to find your files.<br/>Next to each file you want to save, select the down arrow, and then select **Download**. <br/>Choose a location, and then select **Save**.* 

*Save data from private conversations: <br/>  In Viva Engage, select your Inbox, and then select **Private Messages**.<br/> Select a message and review the content of the conversation.<br/> Copy and paste any needed information into a file.*  

*Down time: <br/>  Please don't use the [Contoso.com] Viva Engage network from [date] to [date]. We'll be adding groups and group files from the [Contoso.sub] network. You'll get another email from us when everything is ready to use.*<br/>

### Sample message for people currently using the primary Viva Engage network

We're excited to announce that all of [Contoso] users from [Contoso_sub1] and [Contsoso_sub2] will now be joining us on the [Contoso.com] Viva Engage network.  <br/> Starting [date], you'll notice some changes to our group structure and some new groups, as well as more people. [list the changes]  <br/> Questions or concerns or just want to welcome [Contoso_sub1] and [Contoso_sub2] staff? Join the new "One company - one Viva Engage network" group. We want your input to make our new consolidated network help everyone's voice be heard.  <br/>

## Step 4: Perform the network migration

<a name="self-service"> </a>

> [!IMPORTANT]
> Before you start, be sure you have exported data from the secondary networks and communicated with users!
  
The network migration has three steps that you'll be guided through. Multiple network migrations can be started back-to-back, without waiting for the previous ones to finish. Start from the primary network (the network into which you want to migrate the other networks).
  
### Run the Network Migration tool

1. In the primary Viva Engage network, go to **Settings** \> **Network Admin**.

2. Choose **Network Migration**.

   :::image type="content" source="../../media/f9ae9328-9cb2-46f7-9bce-26bcdc29b3fa.png" alt-text="Screenshot of the Network Migration menu item for Admins.":::

  
    You start on the page with the title **Step 1 of 3 - Check/Add Verified Domains**. This page lists the verified domains that have already been added to the Microsoft 365 tenant for this Viva Engage network. If you don't see the network you want, follow the link to Microsoft 365 to [add additional verified domains](https://support.office.com/article/6383f56d-3d09-4dcb-9b41-b5f5a5efd611), and then return to this page.

    :::image type="content" source="../../media/cac649d6-9245-4645-8f59-fb27dffd87e8.png" alt-text="Screenshot of Step 1 of 3: Check/Add Verified Domains before migrating a Viva Engage network.":::
  
3. When you have added all of the verified domains you want, choose **Next**.

    You're now on the **Step 2 of 3 - Choose a Viva Engage Network to Migrate** page. This page lists all the networks that are eligible for migration. Remember, all of the domains of a Viva Engage network that you want to migrate must be added as verified domains on Microsoft 365. Only the verified domains for Viva Engage networks are listed on the page. If you don't see the network you're looking for, choose the **Previous** button and add the verified domains.

   :::image type="content" source="../../media/3a975838-6d80-4dd1-9b3e-14f157820773.png" alt-text="Screenshot of Step 2 of 3: Choose a Viva Engage Network to Migrate.":::
  
4. On the **Step 2 of 3 - Choose a Viva Engage Network to Migrate** page, select the secondary Viva Engage network that you want to migrate into this network, and then choose **Next**.

5. You reach the page with title **Step 3 of 3 - Export Data &amp; Start Migration**. This page gives you information about the network you're about to migrate, such as network name and number of messages, so that you can confirm if it is the right network. Note that only  *active*  and  *pending users*  will be migrated. All other content is permanently deleted.

    :::image type="content" source="../../media/8de9e6e7-d172-44bc-808c-ec72f34f09e2.png" alt-text="Screen shot of Step 3 of 3 - Export Data &amp; Start Migration.":::


6. When you have exported the data you want, and you're ready to begin the migration, choose **Start Migration**.

    A confirmation dialog box appears.

    :::image type="content" source="../../media/4b93a2e6-9dc4-409c-99cb-2ab7dc225679.png" alt-text="Screenshot of dialog box to Confirm that you want to migrate a Viva Engage network.":::
  
7. In the **Are you absolutely sure you want to migrate the network?** box, under **I confirm the network migration of** _Network Name_, enter the name of the network you want to migrate to confirm it, and then choose **Migrate**.

   > [!CAUTION]
   > You cannot stop or reverse the migration. So be very sure that you have exported all of the data that you want and that you have chosen the correct network to migrate before you choose **Migrate**. If you're unsure, choose **Cancel** and go back to export your data or check the network name.
   >
   > Once you migrate a network, all content and data in the secondary network will be lost. Make sure to export any files or documents you wish to keep before initiating the migration.
  
8. On the **Status of network migrations** page, you can view the status for the migration. It lists the domains associated with the networks being migrated, the person who initiated the migration, the start and completed dates and times for the migration, and the status of the migration. You can see details about the network, such as the number of active users, the number of messages, and the external networks.

    :::image type="content" source="../../media/05c6da77-091b-48fc-8d08-4455454d4c87.png" alt-text="Screenshot showing the Status of network migrations; Viva Engage network migration is running.":::
  
9. Multiple network migrations can be started back-to-back, without waiting for the previous ones to finish. So, you can start the next migration immediately by going through the wizard again.

### View status of network migration

The network migration process works as shown in the following illustration.
  
:::image type="content" source="../../media/00d177ba-3be3-45eb-9341-a00abf7b295c.png" alt-text="Flowchart showing that first you migrate the domains from the secondary Viva Engage network and decommission the network, and then migrate users and external networks in parallel.":::
  
In step 1, the domains from the secondary network are migrated and the secondary network is decommissioned. Then in step 2, the active and pending users and external networks are migrated in parallel. Even if a subset of users or external networks isn't migrated, the migration itself will continue and finish, and more details/errors can be found on the status page.
  
The migration status page can show the following error messages.
  
| Error message | What it means |
|:-----|:-----|
|Failed to migrate  _source network name_ <br/> |The migration of the secondary network did not succeed.  <br/> |
|Failed to migrate  _user email_ <br/> |If one or more users failed to migrate, there will be one or more error messages to that effect. At this point, you can decide to add the user manually to the primary network. Note that the secondary network has been migrated at this point.  <br/> |
|Failed to migrate  _external network name_ <br/> |If one or more external networks failed to migrate, there will be one or more error messages to that effect. Note that the secondary network has been migrated at this point.  <br/> |

To troubleshoot further, contact [Viva Engage support](https://support.office.com/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).
  
## Step 5: Make primary network change

<a name="parentchanges"> </a>

### Create groups

Use the data from groups.csv and users.csv to identify groups that might be needed in the primary network, and to invite the new users to those groups. You can do this manually or by creating a Windows PowerShell script.
  
### Upload files

In data exports, files are named with their Viva Engage ID, rather than their file name. Their file name and location is listed in the Files.csv file, so you'll need to create a Windows PowerShell script to rename the exported files and load them into the appropriate location in the primary network.
  
## Step 6: Communicate with all users after the migration

<a name="aftercommunicate"> </a>

Use this communication to reinforce how you want people to use Viva Engage.
  
**Sample post-migration communication**

*We're ready to start collaborating more efficiently! Sign in to Viva Engage today, using your [Contoso.com] email and regular password for that account. If you need your password reset for that account, contact [IT department]. We restructured the groups so that the content works for everyone, so take some time to browse the groups and join the ones that make sense for you.  <br/> Questions or concerns? Join the new "One company - one Viva Engage network" group. We want your input to make our new consolidated network help your voice be heard.*  <br/>

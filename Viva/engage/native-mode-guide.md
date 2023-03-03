---
ms.date: 12/14/2022
title: "Viva Engage Native Mode: Step-by-step guide"
description: "Learn more about the process of migrating to Native Mode with this in-depth step-by-step guide."
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
# Viva Engage Native Mode: Step-by-step guide

Organizations that want to take advantage of the new compliance features in Viva Engage need to make sure their network is aligned to Native Mode. Native Mode also provides other benefits, such as the ability to host live events in every Viva Engage community, simplify file administration through SharePoint, and apply Microsoft 365 Group management policies.

Any network that was created after January 16, 2020, is already in Native Mode and can make use of these features right out of the box! Organization that 's networks created prior to that date need to use the Native Mode Alignment Tool to ensure that the network is fully backed by Microsoft 365 before they can access these new features.

 > [!NOTE]
> Native Mode is strongly recommended for reasons of security, compliance, and M365 integration.

The following steps show you what you need to do before and during a transition to Native Mode. For more information about what Native Mode means for your Viva Engage Network, see [Overview of Native Mode](./overview-native-mode.md).

## 1. Initial Steps to access the Native Mode Alignment Tool

To align your network to Native Mode, you need to make sure that your Microsoft tenant has only one Viva Engage Network associated with it.  If you've more than one Yammer Network on your Microsoft tenant, you first need to complete the steps in [Consolidate multiple Viva Engage networks](/yammer/configure-your-yammer-network/consolidate-multiple-yammer-networks)

After you ensure that there's just one Viva Engage Network in your Microsoft tenant, you need to ensure that that network enforces Microsoft 365 Identity. For more information, see [Enforce Microsoft 365 Identity](/yammer/configure-your-yammer-network/enforce-office-365-identity)

## 2. Access the Native Mode Alignment Tool

Only Microsoft 365 global Admins can access the Native Mode Alignment Tool. It’s important to know that during times of high network traffic it can take up to a few hours for Global Admin privileges to be reflected in Viva Engage. If your account is only granted these privileges on a temporary basis, it may not be visible immediately after your account is elevated. To access the Native Mode Alignment Tool after Viva Engage recognizes that your account has Global Admin capabilities: Log in to Viva Engage, go to the Network Admin section, and select the Native Mode for Microsoft 365 menu item.

> [!IMPORTANT] 
> The Alignment Tool can take a long time for processing. Most customers are able to complete the tool in one to two weeks, but it can take up to 90 days in extreme circumstances. The account used to initiate the alignment tool must maintain global admin privileges for the duration of the alignment process.

## 3. Prepare to run the Native Mode Alignment Tool
Before you run the Native Mode Alignment Tool, you should generate and review the Alignment Report for your network. To run the report from within the tool, select the **Generate Report** button in the middle of the screen. This step won't make any changes to your network and won't the alignment process. It outputs a list of all users and communities in your Viva Engage Network.

This report comes in .yml format. If you prefer to review the file as a .csv file, we provide a tool available via GitHub that converts the file.

Use the report to identify the following information:

- **Which users are currently unmapped**
The Alignment Tool tries to map all unmapped users to an existing Azure AD account. Any users who don't have an Azure AD account are deleted from the network.

- **How many files each user has stored in Private Messages**

  The Alignment Tool hard-deletes all files that are attached to private messages. These files are unrecoverable after the alignment completes.

- **Which communities in your network are Private and Unlisted**

   Unlisted communities become standard private communities through the Azure B2B Guest framework alignment. The Native Mode Alignment Tool converts all your external groups to internal groups. If you have enabled Azure B2B guests in your Viva Engage network, you can reinvite them as Azure B2B guests as part of the migration.

- **Which communities in your network allow external guests**

  External groups aren't permitted in Native Mode. Guest access in Native Mode is only available through the Azure B2B Guest framework. The Native Mode Alignment Tool converts all your external groups to internal groups. If you have enabled Azure B2B Guests in your Viva Engage network, you can reinvite your guests as Azure B2B guests as part of the migration.

- **Which communities in your network don't have any owners or have owners who lack Microsoft 365 Group Creation Rights**

  The Native Mode Alignment Tool creates a new Microsoft 365 Group, which is authorized by using the credentials of the existing owners of the Viva Engage community. If the Viva Engage community doesn't have any owners or if none of the owners are authorized to create Microsoft 365 Groups, the tool creates the group by using the credentials of the Global Admin who initiated the Alignment Tool. So, it's important that your Global Admin maintains their privileges during the alignment process.

  We recommend that you send advanced communications to all users who have files stored in private messages, owners of any groups that are marked as unlisted, and owners of any groups that are currently external.

## 4. Export the content in your Viva Engage network

  Immediately before running the Alignment Tool, you should export any content from your Viva Engage Network that isn't already backed up. The best practice is to export this content regularly. We encourage you to set up automated backups every month or so. Once these regular backups are in place, it is easier to export any other data as needed for processes like this one. 

  If you don't make regular backups of your data, you need to export all the data in your home network that you want to retain a copy of. External networks can be ignored, as they aren't affected by the Native Mode Alignment Tool. You can export data going as far back as the beginning of your network, but you may decide you only need to back up data going back a certain amount of time. Keep in mind that the Native Mode Alignment Tool deletes certain data, such as the files attached to private messages and any messages posted in previously deleted groups from your network. So any data that's not backed up may be  nonrecoverable after the tool runs.

  This is the multi-step process to export a large volume of content from your network:

  1.	**Export message data** 
          - We suggest that you export message data by using the [Network Data Export feature](/yammer/manage-security-and-compliance/export-yammer-enterprise-data#ExportNetworkData) in the Viva Engage Admin panel.
          - We suggest that you limit your export to a maximum date range of two months at a time and exclude attachments. If you include attachments, you may need to limit your date range significantly further, such as to one week at a time, to prevent the system from encountering time-out errors.

  2. **Export files**
        - We suggest that you export files separately from messages by using the [Viva Engage file export API](/yammer/manage-security-and-compliance/export-yammer-enterprise-data#export-yammer-files-via-api).
        - You can use this API to export all the files from a specified date range. It API supports up to six concurrent requests, and each request should be limited to a two-month period. This functionality enables you to simultaneously export a full year of files in a single API call.

## 5. Run the Alignment Tool for the first time

After you’ve reviewed the Alignment Report, communicated upcoming changes to the users in your network, exported your data, and are aware of what changes the tool will make in your network, you should be ready to run the tool for the first time. The tool runs in the background of your network and has no noticeable affect on end users. As soon as the tool starts to run, it makes some changes to your network to prevent new unmapped users, unconnected groups, and so on.

It's important to note that in most cases, you need to run the tool more than once. To run the tool, scroll to the bottom of the page and select the **Continue** button. You'll be prompted to confirm that you've read and understand the documentation and information about the changes the tool will make to your network. Read through the form and this guide carefully and make sure you fully understand the implications of running the tool.

> [!IMPORTANT]
> Running the Native Mode Alignment Tool will make permanent and irreversible changes in your network. Data that's deleted through this process can't be recovered.

When you're ready, complete the authorization form and initiate the Alignment Tool. You'll need to keep the window open for one-five minutes while the initial phase of the tool processes, after which you can navigate away from the page without consequence. If you try to navigate away from the page during the initial setup phase, you'll receive a warning that prevents you from accidentally navigating away too early.

## 6.	Track Alignment Tool progress

The Alignment Tool runs in the background and shouldn't affect end users. The account that runs the Alignment Tool must maintain global admin status during the alignment process. Small networks may be able to complete the process in one to two weeks. For large networks, it can take up to 90 days to run the first time. If your network needs to run the tool multiple times, each run will take less time than the previous run, as the tool only needs to process content that wasn't processed in previous runs.

To check on the progress of the Alignment Tool, just go back to the page where you started the tool. At the top of the page, you'll see a banner that reports current status of the tool, the next steps, and whether the tool is ready for you to take next steps.

You can also see a more-detailed status update near the bottom of the screen. That report updates every 30 minutes to tell you the number of users, groups, files, and so on, that have been migrated.

## 7. Resolve the error report

Once the tool has finished running, the banner at the top of the page will report one of two things. If the banner says that your network is successfully aligned to Native Mode, you're finished, and no further actions are required. If the banner says that the alignment has failed and an error report was generated, you need to download that error report. Most errors are easy to resolve and just require you to rename a file that has characters that aren't allowed in SharePoint files.

> [!NOTE]
> The error report can be found at the very bottom of the page. This is a separate report from the Alignment Report that you reviewed earlier. 

The error report is in .csv format by default and will remain available until the next time the Alignment Tool is run. When the tool is run again, a new error report is generated.
The report contains a list of files that failed to migrate from Azure to SharePoint, plus error codes. For a list of common error codes and the steps to remediate, see the [error codes section of the troubleshoot native mode article](/yammer/troubleshoot-problems/troubleshoot-native-mode#error-codes). You also can enlist our Premier Support Team to help resolve the error reports. If you have a high volume of errors, the Support Team can provide scripts that enable you to bulk-update the files in your network for faster remediation.

It's possible that your error report may contain errors that aren't covered in the documentation cited earlier or that don't appear to be actionable. Often these errors are generated as duplicates of other errors that are actionable. We suggest that you work through all the errors that you can and then rerun the Alignment Tool. Often most of these errors will get resolved when the tool is rerun after the actionable errors are fixed.

> [!IMPORTANT]
> Once a network is successfully aligned to Native Mode, the system will automatically prevent any action that would break this alignment. Once this process has run successfully, you don't have to go through it again. 

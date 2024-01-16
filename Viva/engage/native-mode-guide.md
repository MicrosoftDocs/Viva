---
ms.date: 10/06/2023
title: "Viva Engage Native Mode: Step-by-step guide"
description: "Learn about the process of migrating to Native Mode with this in-depth step-by-step guide."
ms.reviewer: auhosford
ms.author: v-bvrana
author: Starshine89
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---
# Viva Engage Native Mode: Step-by-step guide

Organizations that want to take advantage of the new compliance features in Viva Engage need to make sure their network is aligned to Native Mode. Native Mode also provides other benefits, such as the ability to:
- Host a live event in every Viva Engage community.
- Simplify file administration through SharePoint.
- Apply Microsoft 365 Group management policies.

Any network that was created after January 16, 2020, is already in Native Mode and can make use of these features immediately. You can use the Native Mode Alignment Tool to ensure that the network is backed by Microsoft 365 before accessing these new features.

 > [!NOTE]
> Automatic migration to Native Mode was announced 2022 for reasons of security, compliance, and Microsoft 365 integration. For more information, see [Automatic Native Mode migration and network consolidation](automatic-migration-native-mode.md).

The following steps tell you how to transition to Native Mode. For more information about what Native Mode means for your Viva Engage Network, see [Overview of Native Mode](overview-native-mode.md).

## 1. Initial steps to access the Native Mode Alignment Tool

To align your network to Native Mode, make sure that your Microsoft tenant has only one Viva Engage Network associated with it. If you have more than one Viva Engage Network on your Microsoft tenant, you must first complete the steps in [Consolidate multiple Viva Engage networks](./configure-your-viva-engage-network/consolidate-multiple-networks.md).

Next, make sure that network enforces Microsoft 365 identity. For more information, see [Enforce Microsoft 365 Identity](./configure-your-viva-engage-network/enforce-office-365-identity.md).

## 2. Access the Native Mode Alignment Tool

Only Engage admins and Microsoft 365 Global administrators can use the Native Mode Alignment Tool. If your account is granted these privileges on a temporary basis, it can take a few hours for your admin privileges to be reflected in Viva Engage. Once granted, temporary privileges are only required to initiate the alignment process; they don't need to be maintained the entire time the tool is running. Additionally, Privileged Identity Management (PIM) has no effect on the alignment process.

To access the Native Mode Alignment Tool after Viva Engage recognizes your admin capabilities: Sign in to Viva Engage, go to the Network Admin section, and select the **Native Mode for Microsoft 365** menu item.

> [!IMPORTANT] 
> The Alignment Tool can take a long time for processing. Most customers are able to run the tool in one to two weeks, but it can take up to 90 days in extreme circumstances.

## 3. Prepare to run the Native Mode Alignment Tool
Before you run the Native Mode Alignment Tool, you should generate and review the Alignment Report for your network. To run the report from within the tool, select the **Generate Report** button in the middle of the screen. This step doesn't make any changes to your network and doesn't start the alignment process. It just outputs a list of all users and communities in your Viva Engage Network.

This report comes in YML format. If you prefer to review the report as a CSV file, we provide a tool available in GitHub that converts the file.

Use the report to identify the following information:

- **Which users are currently unmapped**

   The Alignment Tool tries to map all unmapped users to an existing Microsoft Entra account. Any users who don't have a Microsoft Entra account are deleted from the network.

- **How many files each user has stored in Private Messages**

     The Alignment Tool hard-deletes all files that are attached to private messages. These files are unrecoverable after the alignment is completed.

- **Which communities in your network are Private and Unlisted**

   Unlisted communities become standard private communities through the Microsoft Entra B2B Guest framework alignment. The Native Mode Alignment Tool converts all your external groups to internal groups. If you have Microsoft Entra B2B guests in your Viva Engage network, you can reinvite them as Microsoft Entra B2B guests as part of the migration.

- **Which communities in your network allow external guests**

  External groups aren't permitted in Native Mode. Guest access in Native Mode is only available through the Microsoft Entra B2B Guest framework. The Native Mode Alignment Tool converts all your external groups to internal groups. If you have Microsoft Entra B2B Guests in your Viva Engage network, you can reinvite your guests as Microsoft Entra B2B guests as part of the migration.

- **Which communities in your network don't have any owners or have owners who lack Microsoft 365 Group Creation Rights**

  The Native Mode Alignment Tool creates a new Microsoft 365 Group, which is authorized by using the credentials of the existing owners of the Viva Engage community. If the Viva Engage community has no owner--or if no owners are authorized to create Microsoft 365 Groups--the tool creates the group using the credentials of the admin who initiated the Alignment Tool.

  Before you run the tool, we recommend that you notify all users who have files stored in private messages, owners of any groups that are marked as unlisted, and owners of any groups that are currently external.

## 4. Export the content in your Viva Engage network

  Immediately before running the Alignment Tool, you should export any content from your Viva Engage Network that isn't already backed up. The best practice is to export this content regularly. We encourage you to set up automated backups about once a month. When regular backups are in place, it's easier to export any other data as needed.

  If you don't make regular backups of your data, export all the data in the home network that you want to retain. External networks can be ignored, as the Native Mode Alignment Tool won't affect them. You can export data from the beginning of your network, but you may decide you only need to back up data going back a certain period of time. Keep in mind that the Native Mode Alignment Tool deletes certain data, such as the files attached to private messages and any messages posted in previously deleted groups from your network. Any data that's not backed up may be nonrecoverable after the tool runs.

  It's a two-step process to export a large volume of content from your network:

  1.	**Export message data** 
          - We suggest that you export message data by using the [Network Data Export feature](eac-as-manage-data.md#export-tenant-data-by-date-range) in the Viva Engage admin panel.
          - We suggest that you limit your export to a maximum date range of two months at a time and exclude attachments. If you include attachments, you may need to limit your date range significantly, such as to one week at a time, to prevent the system from encountering time-out errors.

  2. **Export files**
        - We suggest that you export files separately from messages by using the [Viva Engage file export API](/rest/api/yammer/yammer-files-export-api).
        - You can use this API to export all files from a specified date range. The API supports up to six concurrent requests, and each request should be limited to a two-month period. This method enables you to simultaneously export a full year of files in a single API call.

## 5. Run the Alignment Tool for the first time

After you review the Alignment Report, communicate upcoming changes to the users in your network, export your data, and are aware of what changes the tool makes in your network, you should be ready to run the tool for the first time.

The tool runs in the background of your network and has no noticeable effect on end users. As soon as the tool starts to run, it makes changes to your network to prevent new unmapped users, unconnected groups, and so on.

It's important to note that in most cases, you need to run the tool more than once.

To run the tool, scroll to the bottom of the page and select the **Continue** button. You're prompted to confirm that you've read and understand the changes that the tool will make to your network. Read through the form and this guide carefully and make sure you fully understand the implications of running the tool.

> [!IMPORTANT]
> The Native Mode Alignment Tool makes permanent and irreversible changes in your network. Data that's deleted through this process can't be recovered.

When you're ready, complete the authorization form and initiate the Alignment Tool. You need to keep the window open for up to five minutes while the initial phase of the tool finishes. If you try to navigate away from the page during the setup phase, the tool sends a warning to prevent you from accidentally leaving too soon.

## 6.	Track Alignment Tool progress

The Alignment Tool runs in the background and shouldn't affect end users. Small networks may be able to complete the process in one to two weeks. For large networks, it can take up to 90 days to run the first time. If your network needs to run the tool multiple times, each run takes less time than the previous run, as the tool only needs to process content that wasn't processed in previous runs.

To check on the progress of the Alignment Tool, go back to the page where you started the tool. At the top of the page, a banner reports the current status of the tool, next steps, and whether the tool is ready for you to take next steps.

Near the bottom of the screen, details about the status update every 30 minutes. Details include the number of users, groups, files, and so on, that have been migrated.

## 7. Resolve the error report

When the tool finishes, the banner at the top of the page reports one of two things. If the banner says that your network is successfully aligned to Native Mode, the alignment process is complete and no further action is required. If the banner says that the alignment failed and an error report was generated, you must download the error report and fix the errors. Most errors are easy to resolve and just require that you rename a file that has characters that aren't allowed in SharePoint files.

> [!NOTE]
> The error report appears at the very bottom of the page. This is a different report from the Alignment Report that you reviewed earlier.

This CSV error report remains available until the next time the Alignment Tool is run. When the tool is run again, a new error report is generated.

The report contains a list of files that failed to migrate from Microsoft Entra ID to SharePoint, plus error codes. For a list of common error codes and the steps to remediate, see the [error codes section of this article](troubleshoot-native-mode.md#error-codes). You also can enlist our Premier Support Team to help resolve errors. If you have a high volume of errors, the Support Team can provide scripts to bulk-update the files in your network for faster remediation.

It's possible that your error report contains errors that aren't covered in the documentation cited earlier or that don't appear to be actionable. Often these errors are duplicates of other errors that are actionable. We suggest that you work through all the errors you can and then rerun the Alignment Tool. Most of these errors get resolved the next time you run the tool after actionable errors are fixed.

> [!IMPORTANT]
> After a network is successfully aligned to Native Mode, the system automatically prevents any action that would break this alignment. Once this process runs successfully, you don't have to go through it again.

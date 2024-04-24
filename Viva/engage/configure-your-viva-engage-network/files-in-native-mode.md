---
title: "Files in Native Mode"
description: "How to prepare your Viva Engage network for Native Mode for Microsoft 365."
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 10/28/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
---

# Viva Engage files in Native Mode for Microsoft 365

In Native Mode for Microsoft 365, all Viva Engage files must be stored in SharePoint. It's easier for users and admins to access files when you have a single location for file storage.

## What happens to files in private messages when you run the Native Mode Alignment tool?

- Users won't be able to upload files to Private messages. Link sharing is still available.

- All files in Private messages are deleted.

## What happens to Group files when you run the Native Mode Alignment tool?

- Group files in Microsoft Azure are copied to SharePoint Document Library (SDL) for the group.
- After group files are successfully copied to SharePoint, we delete the non SharePoint version of the files.
- Previously deleted files for groups are deleted.
- New files are uploaded to SharePoint.
- Non-SharePoint group files are deleted *within 30 days* after the migration is completed.
- For groups that have multiple files with the same name, duplicates are appended with _X, where X is an increasing number for each duplicate file (for example, file_1, file_2, file_3, and so on).
- Viva Engage files that don't align with SharePoint naming standards are renamed to meet requirements.

## File renaming rules

- Characters not supported in SharePoint are replaced with an underscore ( _ ).
- Duplicate files or files with names that already exist in SharePoint are renamed using the following format: filename_yammerFileID_extension.
- Filenames with a blank space as the first or last character, or that end with a period, are edited to remove those characters.
- Unnamed files are named according to the following format: "Viva Engage File", "Viva Engage File (2)", "Viva Engage File (3)", and so on.
- Files with names starting with \~$ are renamed to remove the leading tilde, for example: "~$Viva Engage File" is renamed to "$Viva Engage File".
- Filenames containing _vti_ anywhere in the name are replaced with - vti-, for example: "Viva_Engage_vti_File" is renamed to "Viva-Engage-vti-File".
- Files named. lock, CON, PRN, AUX, NUL, COM0 - COM9, LPTO - LPT9, or desktop.ini are renamed to append "__file" to the name, for example: "COM0" are renamed to "COM0_file". 

## Before running the tools

Because migration deletes files and the process is irreversible, we suggest you:

- Export the files before running the Tool and save them in case anyone asks for them.

- Update to the latest versions of Viva Engage Android, Viva Engage iOS, and Viva Engage Desktop apps, as older versions have issues uploading files to SharePoint.

- If third-party APIs are used to upload files, use the [latest version of Upload files into Viva Engage groups](/rest/api/yammer/upload-files-into-yammer-groups). The previous versions are blocked and file uploads don’t work.

- Notify users in advance of the migration. Specifically, inform them that files in Viva Engage private messages will be deleted and no longer accessible. Only the latest version of the file is migrated to SharePoint, and the previous versions aren't copied. The follower count isn't copied. Users can no longer mark files as official.

## Admin step-by-step experience

1. Export all files. Learn more about how to [Export Viva Engage data](../manage-security-and-compliance/export-viva-engage-enterprise-data.md#find-and-delete-specific-messages-or-files).

2. Start the **Microsoft 365 Alignment tool**.

3. Download the **Alignment Report**, which provides details on the files that each user and group has.

   - Each user has a count for the total number of private message files. These files will be deleted after running the Tool.
   - Each group has a count of Viva Engage and SharePoint files. We plan to migrate all the Viva Engage files to SharePoint. Existing SharePoint files won't be affected.

4. Authorize and run the Tool.

   - SLA - up to 30 days for networks with < 100-K files
   - SLA - up to 45 days for networks with > 100-K files

5. After the Microsoft 365 Alignment tool has completed, review the Error Report and determine if other steps are necessary before your network can be in Native Mode for Microsoft 365.

### End user experience

This table explains the expected end user experience for files while the Tool is running:

|Tasks|Microsoft 365 Viva Engage Groups|Unconnected Viva Engage Groups|Private Messages|
|-----|------------------------|-------------------------|----------------|
|Delete files|User can delete files|File isn't migrated to SharePoint.|Files are deleted and users have no access.|
|Edit file|Edited files are stored in SharePoint|Only the latest file is migrated to SharePoint. If a user edits a file during migration, they risk losing data. Old versions are no longer accessible in SharePoint.|N/A|
|New file|New files are stored in SharePoint|File is in Microsoft Azure, but migrated to SharePoint by the time the Tool has completed its work.|N/A|
||||

If a group is deleted, all the files from that group are deleted (not migrated over).

## After successfully entering Native Mode

- All group files are [stored in SharePoint](https://go.microsoft.com/fwlink/?linkid=2111253), providing a consistent file management experience.

- File search can happen from SharePoint and Viva Engage. Viva Engage searches the first 5000 characters of files in Microsoft Azure cloud storage and the title and author, but only searches the title and author of files stored in SharePoint.

> [!NOTE]
> If you receive an error code during the alignment process for Native Mode, refer to the [Error Codes section in the Troubleshooting Native Mode topic](../troubleshoot-problems/troubleshoot-native-mode.md#error-codes) for more information.

## Related articles

[Overview of Native Mode](../overview-native-mode.md)

[Troubleshoot problems with Native Mode for Microsoft 365](../troubleshoot-problems/troubleshoot-native-mode.md)

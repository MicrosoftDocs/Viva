---
ms.date: 06/04/2024
title: Import OKRs and initiatives into Viva Goals with Excel
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce     
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- highpri  
search.appverid:
- MET150
description: "Learn how to import OKRs and initiatives into Viva goals through a standard Excel template."
---

# Import OKRs and initiatives into Viva Goals with Excel

Viva Goals allows bulk importing of objectives, key results, and initiatives using a standard Excel template. Bulk import allows you to take pre-existing lists of OKRs and Initiatives and quickly add them to Viva Goals.

## Prerequisites for importing OKRs

**Max OKRs and initiatives:** Only 1,000 records can be imported at once. Split the files if there are more than 1000 OKRs to be imported.

**File format:** Files should be saved only as .xlsx (Template will be provided in .xlsx).

**File name:** Don't rename the sheets as it is critical to autodetect by the system during import process. Also don't rename/remove column headers from the template.

**Roles and permissions:** Only organization owners and team owners have this option enabled.

- **Org owner** – Allowed to import OKRs and Initiatives into any team and to the organization.

- **Team owner** – Allowed to only import OKRs and Initiatives to teams in which the user is a team owner.

## How to import OKRs and Initiatives

1. Go to the Team or the Organization where you want to import OKRs and Initiatives and select  the drop-down next to the **Add Objective** button and select **Import OKRs.**
:::image type="content" source="../media/goals/import-okrs-projects/import-okr-option.png" alt-text="Screenshot showing how to import OKRs." lightbox="../media/goals/import-okrs-projects/import-okr-option.png":::

1. This will open the page from which you can download the import template.
:::image type="content" source="../media/goals/import-okrs-projects/template-download-page.png" alt-text="Screenshot showing the template download page." lightbox="../media/goals/import-okrs-projects/template-download-page.png":::

1. Read the instructions for using the template and select the link to download the Excel template.
    - The Excel template also includes all necessary instructions in the **Read Me** sheet.  
    - Refer to **Basic Fields and Advanced Fields** sheet in Excel to learn more about each field in detail.

1. Fill in the OKRs and Initiative details in the OKRs and Initiative tab and save the file with the .xlsx extension.

1. Drag and drop the filled-in Excel workbook in the file upload section (to the right) or select on the hyperlink to select the file from your local storage.

1. You'll see a preview of a few records from the file to ensure you have selected the right one.

1. If the file is correct, select **Import**.

> [!IMPORTANT]
> The system may take some time to import the records from the file.

### View import status

To view the details of import status and details for imports initiated in the past 28 days, select **View Status** from the banner that appears on top, or choose **Account Settings** > **Perferences** > **My Imports** from the left pane.

Once the import completes, you can download the import status report from the My Import summary page to view which OKRs and Initiatives were imported successfully and which were not.

For records that haven't been imported, refer to the "reason" column in the Import status report. Rectify the errors and reupload in the same file. Note that the system doesn't create duplicate records if the attributes of the OKRs and Initiatives such as Owner, Title, Time period, and Team/Organization to which it belongs are unchanged.

## Frequently asked questions

### What file formats are supported?

Only .xlsx files.

### Are there any limitations users need to be aware of?

- The number of rows in Excel shouldn't be greater than 1,000.
- The file size limit is 5 MB.
- The file shouldn't be protected.
- Avoid changing the name of the sheet (for quick detection), renaming column headers, and removing columns.

### Where can users learn what columns are needed, what should be filled in, and other details?

The Instructions tab in the Excel template explains what's needed in detail.

### Does this feature only add new OKRs and Initiatives?

The feature also modifies existing OKRs and/or Initiatives if an exact match is found in the Viva Goals system. Matches are identified based on the Title, Owner of the OKR or Initiative, Type (Organization, Team name, Individual), and Time period, which avoids creating duplicate OKRs and Initiatives.

### How can users align a child OKR to a parent OKR?

1. The parent and the child OKR should exist in the Excel sheet.  
1. Copy the OKR Reference value of the parent to the Parent OKR field of the Child.

### How can users find the status of their import progress?

Once the import is complete, an email will be sent to the user with a summary. A link to the import summary page will be included where users can download the import status Excel file. This file provides status information for each OKR in the uploaded Excel file.

### How long should it take to complete the import once the user submits the file?

Depending on the file size and number of rows, it can take up to 30 minutes.

### Which users are allowed to import OKRs from an Excel file?

The user needs to have one of these roles to be eligible to see the option of OKR import:

- Team owner
- Org owner

> [!NOTE]
> Note that team owners can only import OKRs to teams where they are the team owner and not to the Org level.

### How can users know if OKRs didn’t import successfully, and how they can reupload?

The import status Excel sheet has a dedicated column that details the issue for each OKR that failed in the import operation. Users can read the details, do the necessary changes on the same sheet and/or on the Viva Goals system, and restart the import process using the same sheet.

### If the OKR owners are not part of the Viva Goals organization, can a user get import permissions?

No. The users must exist in the Viva Goals Organization during the time of import.

### Should OKR owners, time periods, and teams exist before importing OKRs?

Yes: OKR owners, time periods, and teams can't be created or invited as part of the OKR import process. Attempting to add these via import will result in an error.

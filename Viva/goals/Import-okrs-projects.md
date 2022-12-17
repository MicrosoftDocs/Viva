---
title: Import OKRs and Initiatives/Projects into Viva Goals with Excel
ms.reviewer: 
ms.author: rasanders
author: rasanders
manager: Liz.Pierce     
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- highpri  
search.appverid:
- MET150
description: "Learn how to import OKRs and initiative/projects into Viva goals through a standard Excel Template"
---

# Overview 

Viva Goals allows bulk importing of Objectives, Key Results and Projects using a standard Excel template. Bulk import allows you to take pre-existing lists of OKRs and Projects and quickly add them to Viva Goals. 

## Pre=requisites and things to note 

**Max OKRs and initiatives/projects:** Only 1000 records can be imported at once. Split the files if there are more than 1000 OKRs to be imported.

**File format:** Files should be saved only as .xlsx (Template will be provided in .xlsx)

**File name:** Please do not rename the sheets as it is critical to auto-detect by the system during import process. Also do not rename/remove column headers from the template.

**Role and Permission:**

- Only organization administrators, organization owners, team owner and team administrators have this option enabled.
    - **Org administrator, Org Owner** – Allowed to import OKRs and Projects into any team and to the organization.
    - **Team Owner, Team Admin** - Allowed to only import OKRs and Projects to teams in which the user is a team administrator or team owner. 

## How to Import OKRs and Initiatives/Projects

1. Go to the Team or the Organization where you want to import OKRs and Projects and click  the drop down next to the **Add Objective** button and select **Import OKRs.**
1. Read the instructions for using the template and click on the link to Download the excel template.
    1. The Excel template also includes all necessary instructions in the **Read Me** sheet.  
    1. Refer to **Basic Fields and Advanced Fields** sheet in the excel to learn more about each field in detail.  
1. Fill in the OKRs and Project details in the OKRs and Project tab and save the file with .xlsx 
1. Drag and drop the filled-in excel in the file upload section (on to the right) or click on the hyperlink to select the file from your local storage 
1. You will see a preview of few records from the file to ensure you have selected the right one 
1. If the file is correct, click **Import** 

> [!IMPORTANT]
> The system may take some time to import the records from the file 

To view the details of import status and details for imports initiated in the past 28 days, select **View Status** from the banner that appears on top or click on your Profile photo and choose **Account Settings > My Import summary**

Once the import completes, you can download the import status report from the My Import summary page to view what OKRs and Projects were imported successfully and what did not.

For records that have not been imported, please refer to the "reason" column in the Import status report. Rectify the errors and re-upload in the same file. NOTE: The system does not create duplicate records if the attributes of the OKRs and Projects such as Owner, Title, Time period and Team/Organization to which it belongs are unchanged.

 ## FAQ (Frequently Asked Questions)

1. What are the File Formats supported? 
    1. Only .xlsx

1. Any limitations that users need to be aware of? 
    1. No. of rows in the excel should not be greater than 1000. 
    1. File size limit of 5MB. 
    1. File should not be protected. 
    1. Avoid changing the name of the sheet (for quick detection), renaming column headers, removing columns. 

1. Where can users learn what columns are needed, what should be filled in, and other details? 
    1. The  Instructions tab  in the excel template explains what’s needed in detail.

1. Does this feature only add new OKRs and Projects? 
    1. The feature also modifies existing OKRs, Projects if an exact match is found in Viva Goals system. Matches are identified based on the Title, Owner of the OKR or Project, Type (Organization, Team name, Individual), and Time period. This avoids creating duplicate OKRs and Projects.

1. How can users align a child OKR to a parent OKR? 
    1. The parent and the child OKR should exist in the excel sheet.  
    1. Copy the OKR Reference value of the parent to the Parent OKR field of the Child.

1. How can users get to know the status of their import progress? 
    1. Once the import is complete, an email  will be sent to the import initiated user with a summary as well as a link to  the import summary page where users can download the import status excel file which provides status information for each OKRs in the uploaded excel file. 

1. How long should it take to complete the import once the user submits the file? 
    1. Depending on the file size and number of rows, it can take up to 30 minutes. 

1. Which users are allowed to import OKRs from an excel file? 
    1. The user needs to have one of these roles to be eligible to see the option of OKR import: 
        1. Org administrator 
        1. Team administrator 
        1. Team owner 
        1. Org owner 
        1. Team owners and admins can only import OKRs to teams where they are the team admin/owner and not to the Org level. 

1. How can users know about OKRs that didn’t import successfully and how can they re-upload? 
    1. The import status excel sheet has a dedicated column that details the issue for each OKR that failed in the import operation. 
    1. Users can read the details, do the necessary changes on the same sheet and/or on the Viva Goals system and restart the import process using the same sheet. 

1. If the OKR owners are not part of the Viva Goals organization, can auser get import permissions? 
    1. No. The users must exist in the Viva Goals Organization during the time of import. 

1. Should OKR owners, time periods, and teams exist before importing OKRs? 
    1. Yes, OKR owners, time periods, and teams cannot be created or invited as part of the OKR import process. Attempting to add these via import will result in an error.
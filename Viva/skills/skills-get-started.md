---
title: Set up Skills in Viva 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 04/16/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: medium
description: An introduction to setting up Skills in Viva, 
---

# Set up skills in Viva 

Start setting up Skills in Viva by building your skills library with skills from the default skills library in Viva and/or importing your own custom skills. 

## Get started

1. In the Microsoft 365 admin center, select **Settings** and then select Viva.  

2. Select **Manage skills library**.  

3. Select **Get started** to begin building your library.  

4. Read the setup overview, then select **Next** to walk through each setup step.

## Use the default skills library 

Choose the skills you’d like to use from the default skills library in Viva. The more skills you include from the default library, the more specific suggestions users see in their skills profiles. 

1. **Use all skills (recommended)**:  this option is highly recommended and includes all 9,500+ skills in the skills library.  

2. **Select specific skills**: this option allows you to choose specific domains and/or skills within domains to include; however choosing a subset of skills may limit the number of skill options and suggestions available to your users. (Note: a minimum of 500 skills is recommended.)  

## Import your custom skills library  

Choose whether you’d like to import your own custom skills library. This step is optional if you selected skills from the default skills library in Viva.  

1. Select **Download library template** and **Download mapping template**. 

2. Populate the templates with your skills data.  

   1. Library template:  
      - Required fields: Skill ID (externalCode), Skill Name (Name.en_US) 
      - Recommended fields: Skill Description (Description.en_US)  
      
   1. Mapping template:  
      - Required fields: Job Title (JobTitle), Skill Name (SkillName)  

3. Save as .csv file and upload to a SharePoint site.  

    1. Open the SharePoint Site library  

    1. Select Upload at the top of the documents library and select files.  

    1. In the ‘Open’ dialog, navigate to the location where the .csv file is saved. Select the file and select open.  

    1. File should be uploaded to the SharePoint site.  

    1. Alternatively, you could use the drag and drop feature to upload files to your SharePoint site.  

4. Get the file path of the .csv files 

    1. Select the file and select the **ellipsis** (…) button 

    1. Choose ‘Details’ to open the pane.  

    1. Scroll down the pane to find the ‘Path’ listed.  

    1. Select the button to copy the selected file’s path to the Clipboard. The file path should be formatted like this: `https://contoso.sharepoint.com/TeamAdmin/Shared%20Documents/Folder%20Name/Skills%20Library.csv`

5. Paste the file paths for both files into the Skills custom import step  

6. Select **Next** to begin file validation. If there's a problem with the file, you see an error message at this step.  

> [!NOTE]
> - The admin completing custom import must have permissions to view and edit the uploaded .csv files in SharePoint. 
> - A minimum of 20 skills are required to import custom skills. Each file must be under 100mb. 
> - The following characters cannot be used as a prefix in any imported field '+', '-', '@', '=', '\t', '\r' 
> - Name.en_US must map to SkillName filed in mapping file  
> - JobTitle should match user profile job titles in Microsoft Entra ID (formerly AAD) or Organizational Data in Microsoft 365. If your organization does not have fresh and complete data in this field for users, please update the system with the latest, either through Microsoft Entra ID or Organizational Data in Microsoft 365.  The more accurately a title reflects a person's job, the more accurate skill suggestions will be.  
> - When saving CSV files for custom imports, ensure you use the comma `,` as the delimiter (CSV comma delimited). Your system may default do a different separator. In European countries, for example, it's often set to a semicolon `;`.
> - Delete any "%20" strings that are present in your pasted filepaths. 

## Review your organization's skills library

Review your organization’s skills library details and select Next. The data includes:  

  - The number of skills from the default skills library in Viva  

  - The number of skills and number of roles/job titles from your custom import  

  - The number of duplicate skills identified in your selection.  In the case of duplicates, your organization’s custom data is prioritized and used over data from the default skills library in Viva.

## Manage settings 

Settings for Skills in Viva allow you to manage the availability of skills in your organization. 

  > [!NOTE]
  > While turning on the skills library for users is recommended at this step, it’s not required to complete Skills in Viva setup. You have the option to complete setup and create your skills library without making it available to users right away.  

1. Select **Turn on skills library** to make skills available in supported Microsoft 365 and Viva experiences.  

    1. If you turn on the skills library, once the setup process is complete and you have confirmed your selections, your skills library is created and users are able to being searching for and adding skills to their profiles within a matter of minutes.  

    1. If you don't turn on the skills library, your organization’s skills library are still created upon completion of the wizard, but it won't be available to users in your organization until you choose to publish it from **Settings.**

2. For skills to appear in Viva Learning, you must also select to **Allow skills in Viva Learning**.  

   - This is a one-time consent to replace “interests” in Viva Learning with skills. Any existing “interests” data is deleted, and users see this replaced with “skills.”

   > [!NOTE]
   > This action can't be reversed. It can take up to three business days for this change to reflect In Viva Learning.  

3. Users receive **skill suggestions** relevant to their role on default.  

    1. When skill suggestions are on for users, users have the option to turn it off for themselves in their skill settings. When skill suggestions are turned off, the user won't see any suggested skills and can only manually confirm skills from a list. 

    1. Skill suggestions are on for users by default.  If you need to disable skill suggestions for specific users, groups, or your entire tenant, you can update this setting using PowerShell. For more information, see [control access to features in Viva](../feature-access-management.md).
    
    - Install Exchange Online PowerShell Version 3.2.0 or later:
    `Install-Module -Name ExchangeOnlineManagement`  
    - Connect to Exchange Online with admin credentials: 
    `Connect-ExchangeOnline`
    - Create a policy to disable skill suggestions for users or groups.  
    `Add-VivaModuleFeaturePolicy -ModuleId VivaSkills -FeatureId UserOptOutPreference -Name UsersAndGroups -IsFeatureEnabled $false -GroupIds group1@contoso.com,group2@contoso.com -UserIds user1@contoso.com,user2@contoso`

    This example adds a policy that disables skills suggestions for the specified users and group members. If you want to disable skills suggestions for all users, use the `-Everyone` parameter instead. 

4. Select **Next**. 

#### Final review and confirmation 

1. Review your skills library and settings information. If there are any changes you want to make, go back to those steps and edit.  

2. When you're ready to complete the setup process, select **Confirm**.  

3. Your skills library is created and your settings are saved.  You can now manage your library and settings on an ongoing basis.


### Next Steps

[Manage your skills library](manage-skills-library.md)

---
title: Set up Skills in Viva 
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 11/15/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: medium
description: An introduction to setting up Skills in Viva, 
---

# Set up Skills in Viva 


1. In the Microsoft 365 admin center, select **Settings** and then select Viva.  

2. Select **Manage skills library**.  

3. Select **Get started** to begin building your library.  

4. Read the setup overview, then select **Next** to walk through each setup step.

## Use the default skills library 

Choose the skills you’d like to use from the default skills library in Viva. The more skills you include from the default library, the more specific suggestions users see in their skills profiles. 

1. **Use all skills (recommended)**:  this option is highly recommended and includes all 9,500+ skills in the skills library.  

2. **Select specific skills**: this option allows you to choose specific domains and/or skills within domains to include; however choosing a subset of skills may limit the number of skill options and suggestions available to your users. (Note: a minimum of 500 skills is recommended.)  

## Import your custom skills library  

Choose whether you’d like to import your own custom skills library. This step is optional, if you’ve selected skills from the default skills library in Viva.  

1. Select **Download library template** and **Download mapping template**. 

2. Populate the templates with your skills data.  

    a. Library template:  
      - Required fields: Skill ID (externalCode), Skill Name (Name.en_US) 
      - Recommended fields: Skill Description (Description.en_US)  
      
    b. Mapping template:  
      - Required fields: Job Title (JobTitle), Skill Name (SkillName)  

3. Save as .csv file and upload to a SharePoint site.  

    a. Open the SharePoint Site library  

    b. Select Upload at the top of the documents library and select files.  

    c. In the ‘Open’ dialog, navigate to the location where the .csv file is saved. Select the file and select open.  

    d. File should be uploaded to the SharePoint site.  

    e. Alternatively, you could use the drag and drop feature to upload files to your SharePoint site.  

4. Get the file path of the .csv files 

    a. Select the file and select the **ellipsis** (…) button 

    b. Choose ‘Details’ to open the pane.  

    c. Scroll down the pane to find the ‘Path’ listed.  

    d. Select the button to copy the selected file’s path to the Clipboard. The file path should be formatted like this: `https://contoso.sharepoint.com/TeamAdmin/Shared%20Documents/Folder%20Name/Skills%20Library.csv`

5. Paste the file path into Skills custom import step  

    a. Enter the file path details. Note “%20” replaced with spaces and remove “/” from end of each row:  
      - SharePoint site URL: `https://contoso.sharepoint.com/TeamAdmin`
      - Document library name: `Shared Documents/Folder Name`
      - Skills library file path: [Skills Library.csv] 

6. Select **Next** to begin file validation. If there's a problem with the file, you'll see an error message at this step.  

> [!NOTE]:  
> - Minimum of 20 skills required to upload  
> - Name.en_US must map to SkillName filed in mapping file  
> - JobTitle should match user profile job titles in AAD or Microsoft 365 Organizational Data Upload (see more information). The mMore accurately a title reflects a person's job, the more accurate skill suggestions will be 
> - Character limitations 
> - Maximum file size  
> - Admin must have permissions to view and edit the uploaded templates in SharePoint 
> - Make sure to delete / and spaces from file path fields

### Review your organization's skills library

Review your organization’s skills library details and select Next. The data includes:  

  - The number of skills from the default skills library in Viva  

  - The number of skills and number of roles/job titles from your custom import  

  - The number of duplicate skills identified in your selection.  In the case of duplicates, your organization’s custom data is prioritized and used over data from the default skills library in Viva.

### Manage settings 

Settings for Skills in Viva allow you to manage the availability of skills in your organization. 

> [!NOTE]:
> While it's recommended to turn on the skills library for users at this step, this step is optional and it’s not required to complete set up Skills in Viva. You can still complete the setup process and create your skills library without making it available to users.  

1. Select **Turn on skills library** to make skills available in supported Microsoft 365 and Viva experiences.  

    a. If you turn on the skills library, once the setup process is complete and you have confirmed your selections, your skills library is created and users are able to begin identifying their skills profile immediately.  

    b. If you don't turn on the skills library, your organization’s skills library will still be created upon completion of the wizard, but it will not be available to users in your organization until you choose to publish it from **Settings.**

2. For skills to appear in Viva Learning, you must also select to **Allow skills in Viva Learning**.  

    a. This is a one-time consent to replace “interests” in Viva Learning with skills. Any existing “interests” data is deleted, and users see this replaced with “skills.”

> [!NOTE]: 
> This action can't be reversed.  It can take up to seven days for changes to reflect in Viva Learning.  

3. Users receive **skill suggestions** relevant to their role on default.  

    a. When skill suggestions are on for users, users have the option to turn it off for themselves in their skill settings. When skill suggestions are turned off, the user won't see any suggested skills and will only be able to manually confirm skills from a list. 

    b. Skill suggestions are on for users by default.  If you need to disable skill suggestions for specific users, groups, or your entire tenant, you can update this setting using PowerShell. For more information, see [control access to features in Viva](https://learn.microsoft.com/en-us/viva/feature-access-management).
    
    - Install Exchange Online PowerShell Version 3.2.0 or later:
    (insert cmdlet snippet)  
    - Connect to Exchange Online with admin credentials: 
    (insert cmdlet snippet)  
    - Create a policy to disable skill suggestions for users or groups.  
    `Add-VivaModuleFeaturePolicy -ModuleId VivaSkills -FeatureId UserOptOutPreference -Name UsersAndGroups -IsFeatureEnabled $false -GroupIds group1@contoso.com,group2@contoso.com -UserIds user1@contoso.com,user2@contoso`

This example adds a policy that disables skills suggestions for the specified users and group members. If you want to disable skills suggestions for all users, use the `-Everyone` parameter instead. 

4. Select **Next**. 

#### Final review and confirmation 

1. Review your skills library and settings information. If there are any changes you want to make, go back to those steps and edit.  

2. When you're ready to complete the setup process, select **Confirm**.  

3. Your skills library is created and your settings are saved.  You can now manage your library and settings on an ongoing basis.


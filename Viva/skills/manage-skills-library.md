---
title: Manage Skills Library
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
description: An introduction to managing your organization's skills library. 
---

# Manage skills library

You can manage your skills library in the following ways: 

- View, add and, delete skills from the default skills library in Viva. 
- View, import, export, and delete skills from your custom skills library. 


## Manage settings  

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Settings** tab.  

4. Select **Skills library** in the Settings tab to view and manage availability of skills in your organization.  

   1. Turn on skills library
        
      - Check Turn on skills library to make skills available to your organization’s supported applications and services across Microsoft 365 and Viva. Users have access to skills in supported experiences. 
      
      - Uncheck Turn on skills library to turn off skills in your organization. Users won't have access to skills.
    
   1. Allow skills in Viva Learning
      - Check the box to replace “interests” in Viva Learning with skills. Any existing “interests” data is deleted, and users see this replaced with “skills.” 
    
   > [!NOTE]
   > This action can't be reversed.  It can take up to three business days for changes to reflect in Viva Learning.  

5. Select **Skill suggestions** to see details about the settings. Users receive **skill suggestions** relevant to their role on default.  

    1. When skill suggestions are on for users, users have the option to turn it off for themselves in their skill settings. When skill suggestions are turned off, the user won't see any suggested skills and will only be able to manually confirm skills from a list. 

    1. Skill suggestions are on for users by default.  If you need to disable skill suggestions for specific users, groups, or your entire tenant, you can update this setting using PowerShell. For more information, see [control access to features in Viva](../feature-access-management.md).
    
       - Install Exchange Online PowerShell Version 3.2.0 or later:<br/>`Install-Module -Name ExchangeOnlineManagement`

       - Connect to Exchange Online with admin credentials:<br/>`Connect-ExchangeOnline`

       - Create a policy to disable skill suggestions for users or groups.<br/> `Add-VivaModuleFeaturePolicy -ModuleId VivaSkills -FeatureId UserOptOutPreference -Name UsersAndGroups -IsFeatureEnabled $false -GroupIds group1@contoso.com,group2@contoso.com -UserIds user1@contoso.com,user2@contoso`

       This example adds a policy that disables skills suggestions for the specified users and group members. If you want to disable skills suggestions for all users, use the `-Everyone` parameter instead. 

## Manage your organization’s skills library 

Your skills library is managed in two parts. You can add and delete skills you’ve selected from the default skills library in Viva, and you can reimport custom skills.  

## Manage default skills library in Viva  

View and manage the skills you selected from the default skills library in Viva. The more skills you include from the default library, the more specific suggestions users see in their skills profiles. Our recommendation is to use all 9,500+ skills, with a minimum of 500 skills.

## View your current skill selection  

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Skills library** in Viva.  

5. Review list. You can filter by domain and search by skill name.

## Add skills from the default skills library 

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Skills library** in Viva.  

5. Select **+ Add Skills**.  

6. Select the skills you want to add by checking them. You can filter by domain and search by skill name.  

7. Select **Add** to immediately add the skills to your library.  

   > [!NOTE]
   > If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in Viva Learning.  

8. Select **Done** to close the flyout.

## Delete skills from the default skills library   

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Skills library** in Viva.  

5. Select the skills you want to delete. You can filter by domain and search by skill name.  

6. Select **Delete skills**. 

7. Select **Delete** to confirm you want to delete the selected skills. 

   > [!NOTE]
   > Deleting skills will immediately remove the skills and associated skills data from your organization and from your users’ experience.

> [!NOTE]
> If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in Viva Learning.


## Manage custom skills import 

Manage your custom skills library and role-to-skills mapping import. If you didn't import custom skills as a part of your initial setup, you can add it later. This step is optional if you’ve selected skills from the default skills library in Viva.  

#### View custom import details 


1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Custom skills**. You can filter by role and search by skill name.  

5. Select **View details** to see an overview of your imported files, who completed the import, and the import date.  

### Import custom skills library  

Follow these steps to either import your custom skills library for the first time or to reimport with changes to your initial custom import.

> [!NOTE]
> Reimporting custom skills library will override existing data.  New skills will be added to your library. Deleted skills and any data associated with those skills will be immediately removed for your organization. Any changes to skill name or skill description will be treated as a deletion of the old skill and the addition of a new skill.

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **New import**.  

5. Select **Download library template** and **Download mapping template.** 

6. Populate the templates with your skills data.  

   1. Library template:  

      - Required fields: Skill ID (externalCode), Skill Name (Name.en_US) 
      - Recommended fields: Skill Description (Description.en_US)  

   1. Mapping template:  
      - Required fields: Job Title (JobTitle), Skill Name (SkillName)  

7. Save as .csv file and upload to a SharePoint site. 
    1. Open the SharePoint Site library  
    1. Select Upload at the top of the documents library and select files.  
    1. In the ‘Open’ dialog, navigate to the location where the .csv file is saved. Select the file and select open.  
    1. File should be uploaded to the SharePoint site.  
    1. Alternatively, you could use the drag and drop feature to upload files to your SharePoint site.  

8. Get the file path of the .csv files 
    
    1. Select the file and select the ellipsis (…) button 
    1. Choose ‘Details’ to open the pane.  
    1. Scroll down the pane to find the ‘Path’ listed.  
    1. Select the copy button to copy the selected file’s path to the Clipboard. The File Path looks like: `https://contoso.sharepoint.com/TeamAdmin/Shared%20Documents/Folder%20Name/Skills%20Library.csv`
  
9. Paste the file path for both files into the Skills custom import step.

10. Select **Next** to begin file validation. If there's a problem with the file, you see an error message at this step.  

11. Review your custom skills data.  

12. Check the box to acknowledge that importing custom skills will immediately impact your users’ experience if skills is turned on. Any new skills are added, and any deleted or missing skills in the import file are removed from your users’ experience, and all data associated with these skills are also be removed.  

13. Select **Confirm** to import.  

> [!NOTE]
> If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in Viva Learning.

> [!NOTE]
> - The admin completing custom import must have permissions to view and edit the uploaded .csv files in SharePoint. 
> - A minimum of 20 skills are required to import custom skills. Each file must be under 100mb. 
> - The following characters cannot be used as a prefix in any imported field '+', '-', '@', '=', '\t', '\r' 
> - Name.en_US must map to SkillName filed in mapping file  
> - JobTitle should match user profile job titles in Microsoft Entra ID (formerly AAD) or Organizational Data in Microsoft 365. If your organization does not have fresh and complete data in this field for users, please update the system with the latest, either through Microsoft Entra ID or Organizational Data in Microsoft 365.  The more accurately a title reflects a person's job, the more accurate skill suggestions will be. 
> - When saving CSV files for custom imports, ensure you use the comma `,` as the delimiter (CSV comma delimited). Your system may default do a different separator. In European countries, for example, it's often set to a semicolon `;`.
> - Delete any "%20" strings that are present in your pasted filepaths. 


### Export custom import  

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Custom skills**. You can filter by role and search by skill name.  

5. Select **Export custom skills** to export your custom skills import files.  


### Delete custom skills 

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Custom skills**. You can filter by role and search by skill name.  

5. Select **Delete custom skills**.  

6. Select **Delete** to confirm that you want to delete your custom skills. 

    Deleting custom skills immediately removes all of these skills from your users’ experiences deletes all data associated with those skills. 
    
> [!NOTE]
> If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in Viva Learning.

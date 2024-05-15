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
ms.localizationpriority: medium
description: An introduction to managing your organization's skills library. 
---

# Manage skills library

You can manage your skills library by adding and deleting skills from the default skills library. You can also import, export, and delete skills from your custom skill library. 


## Manage settings  

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Settings** tab.  

4. Select **Skills library** in the Settings tab to view and manage availability of skills in your organization.  

   - **Turn on skills library**
        
      - Select **Turn on skills library** to make the skills library available in your users' profiles.
      
      - Clear **Turn on skills library** to turn off skills in your organization. Users won't be able to search for and add new skills or receive skills suggestions. They'll still have access to their confirmed and dismissed skills.
    
   - **Allow skills in Viva Learning**
      - Select this option to replace "interests" in Viva Learning with skills. Any existing "interests" data is deleted, and users see this replaced with "skills." 

      > [!NOTE]
      > This action can't be reversed. It can take up to three business days for changes to reflect in Viva Learning.  
   - **Turn on skills in Viva Insights**. Learn more about the skills landscape report in Viva Insights. Select this option to enable sending skills data to Viva Insights.
   - 
5. Select **Skill suggestions** to see details about the settings. Users receive **skill suggestions** relevant to their role by default.  

    When skill suggestions are enabled, users have the option to turn it off for themselves in their skill settings. When skill suggestions are turned off, the user won't see any suggested skills and will only be able to manually confirm skills from a list. 

    If you need to disable skill suggestions for specific users, groups, or your entire tenant, create an access control policy. For more information, see [control access to features in Viva](../feature-access-management.md).

## Manage your organization’s skills library 

Your skills library is managed in two parts. You can add and delete skills you’ve selected from the default skills library in Viva, and you can reimport custom skills.  

## Manage default skills library in Viva  

View and manage the skills you selected from the default skills library in Viva. The more skills you include from the default library, the more specific suggestions users see in their skills profiles. Our recommendation is to use all 7,000+ skills, with a minimum of 500 skills.

## View your current skill selection  

1. In the Microsoft 365 admin center, go to **Settings** > **Viva** > **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Skills library** in Viva.  

5. Review the list. You can filter by domain and search by skill name.

## Add skills from the default skills library 

1. In the Microsoft 365 admin center, go to **Settings** > **Viva** > **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Skills library** in Viva.  

5. Select **+ Add Skills**.  

6. Select the skills you want to add. You can filter by domain and search by skill name.  

7. Select **Add** to immediately add the skills to your library.  

   > [!NOTE]
   > If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to be reflected in suggested skills for users and in Viva Learning.  

8. Select **Done**.

## Delete skills from the default skills library   

1. In the Microsoft 365 admin center, go to **Settings** > **Viva** > **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Skills library** in Viva.  

5. Select the skills you want to delete. You can filter by domain and search by skill name.  

6. Select **Delete skills**. 

7. Select **Delete** to confirm you want to delete the selected skills. 

> [!NOTE]
> - Deleting skills will immediately remove the skills and associated skills data from your organization and from your users' experience.
> - If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in Viva Learning.


## Manage custom skills import 

Manage your custom skills library and role-to-skills mapping import. If you didn't import custom skills as a part of your initial setup, you can add it later. This step is optional if you’ve selected skills from the default skills library in Viva.  

#### View custom import details 


1. In the Microsoft 365 admin center, go to **Settings** > **Viva** > **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **Custom skills**. You can filter by role and search by skill name.  

5. Select **View details** to see an overview of your imported files, who completed the import, and the import date.  

### Import custom skills library  

Follow these steps to either import your custom skills library for the first time or to reimport with changes to your initial custom import.

> [!NOTE]
> - Reimporting custom skills library will override existing data.  New skills will be added to your library. Deleted skills and any data associated with those skills will be immediately removed for your organization. Any changes to skill name or skill description will be treated as a deletion of the old skill and the addition of a new skill.
> - The admin completing custom import must have permissions to view and edit the uploaded .csv files in SharePoint. 

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.  

2. Select **Manage skills library**.  

3. Select the **Skills library** tab.  

4. Select **New import**.  

5. Select **Download library template** and **Download mapping template.** 

6. Populate the templates with your skills data.  

   - Library template:  

      - Required fields: Skill ID (externalCode), Skill Name (Name.en_US) 
      - Recommended fields: Skill Description (Description.en_US)  

   - Mapping template:  
      - Required fields: Job Title (JobTitle), Skill ID (SkillExternalCode)
      - Optional, for reference only: Skill Name (SkillName.en_US))  

3. Save as a .csv (comma separated) file and upload to a SharePoint site.  
    1. Open the SharePoint Site library.
    1. Select **Upload** at the top of the documents library, and then select **Files**.  
    1. Navigate to the location where you saved the .csv file. Select the file, and then select **Open**.    

    Alternatively, you could use the drag and drop feature to upload files to your SharePoint site.  

4. Get the file paths for your .csv files. 
    1. Select the file, and then select the **ellipsis** (…).
    2. Select **Details**.  
    3. Scroll to find the **Path**.  
    4. Select the option to copy the selected file's path to the Clipboard. The file path should be formatted like this: `https://contoso.sharepoint.com/TeamAdmin/Shared%20Documents/Folder%20Name/Skills%20Library.csv`
  
9. Paste the file path for both files into the Skills custom import step. Delete any "%20" strings in the file path.

10. Select **Next** to begin file validation. If there's a problem with the file, you see an error message at this step.  

11. Review your custom skills data.  

12. Select the option to acknowledge that importing custom skills will immediately impact your users’ experience if skills is turned on. Any new skills are added, and any deleted or missing skills in the import file are removed from your users’ experience, and all data associated with these skills are also be removed.  

13. Select **Confirm** to import.  

If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in suggested skills for users and in Viva Learning.

> [!NOTE]

> - A minimum of 20 skills are required to import custom skills. Each file must be under 100mb. 
> - The following characters cannot be used as a prefix in any imported field '+', '-', '@', '=', '\t', '\r' 
> - Skill ID (externalCode) in the library file must map to Skill ID (SkillExternalCode) in the role to skill mapping file.  
> - JobTitle should match user profile job titles in Microsoft Entra ID  or Organizational Data in Microsoft 365. If your organization does not have fresh and complete data in this field for users, please update the system with the latest, either through Microsoft Entra ID or Organizational Data in Microsoft 365. The more accurately a title reflects a person's job, the more accurate skill suggestions will be. 
> - When saving CSV files for custom imports, ensure you use the comma `,` as the delimiter (CSV comma delimited). Your system may default do a different separator. In European countries, for example, it's often set to a semicolon `;`.
> - Delete any "%20" strings that are present in your pasted file paths. 


### Export custom import  

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.

1. Select the **Skills library** tab.  

4. Select **Custom skills**. You can filter by role and search by skill name.  

5. Select **Export custom skills** to export your custom skills import files.  


### Delete custom skills 

1. In the Microsoft 365 admin center, select **Settings** and then select **Viva**.
1. Select the **Skills library** tab.  
4. Select **Custom skills**. You can filter by role and search by skill name.  
5. Select **Delete custom skills**.  
6. Select **Delete** to confirm that you want to delete your custom skills. 

    Deleting custom skills immediately removes all of these skills from your users’ experiences deletes all data associated with those skills. 
    
> [!NOTE]
> If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to be reflected in suggested skills for users and in Viva Learning.

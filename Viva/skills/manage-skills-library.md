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

You can manage your skills library by adding and deleting skills from the default skills library. You can import, export, and delete skills from your custom skill library. You can also control whether skills are available for users.


## Manage where skills are available and skills suggestions

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home#/featureexplorer), select **Settings**, and then select **Viva**.  
2. Select **Manage skills library**, and then select **Settings**. 
3. Select **Skills library** in the Settings tab to view and manage availability of skills in your organization.  

   1. Select **Turn on skills library** to make the skills library available in your users' profiles.
   
   Clear **Turn on skills library** to turn off skills. Users won't be able to search for and add new skills or receive skills suggestions. They'll still have access to their confirmed and dismissed skills.
    
   2. Select **Allow skills in Viva Learning** to replace "interests" in Viva Learning with skills information. Any existing "interests" data is deleted, and users see this replaced with "skills." 

      > [!NOTE]
      > This action can't be reversed. It can take up to three business days for changes to reflect in Viva Learning.  
   3. Select **Turn on skills in Viva Insights** (if available in your tenant) to send skills data to Viva Insights. Learn more about the [skills landscape report in Viva Insights](/viva/insights/advanced/introduction-to-advanced-insights).
   - 
5. Select **Skill suggestions** to see details about the settings. Users receive **skill suggestions** relevant to their role by default.  

    When skill suggestions are enabled, users have the option to turn it off for themselves in their skill settings. When skill suggestions are turned off, users don't see any suggested skills and can only manually confirm skills from a list. 

    If you need to disable skill suggestions for specific users, groups, or your entire tenant, create an access control policy. For more information, see [control access to features in Viva](../feature-access-management.md).

## Manage your organization’s skills library 

Your skills library is managed in two parts. You can add and delete skills you’ve selected from the default skills library in Viva, and you can reimport custom skills.  

### Manage default skills library in Viva  

View and manage the skills you selected from the default skills library in Viva. The more skills you include from the default library, the more specific suggestions users see in their skills profiles. Our recommendation is to use all 7,000+ skills, with a minimum of 500 skills.


1. In the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home#/featureexplorer), select **Settings**, and then select **Viva**.  
2. Select **Manage skills library**. Select the **Skills library** tab, and then select **Skills library in Viva**. 
3. Review the list. You can filter by domain and search by skill name.
4. To add skills, select **+ Add Skills**. Select the skills you want to add. You can filter by domain and search by skill name. Select **Add**.  

   > [!NOTE]
   > If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to be reflected in suggested skills for users and in Viva Learning.  
5. To delete skills, select the skills you want to delete. You can filter by domain and search by skill name. Select **Delete skills**. Select **Delete** again to confirm you want to delete the selected skills. 

  > [!NOTE]
  > - Deleting skills immediately removes the skills and associated skills data from your organization and from your users' experience.
  > - If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in Viva Learning.

8. Select **Done**.

### Manage custom skills import 

Manage your custom skills library and role-to-skills mapping import. If you didn't import custom skills as a part of your initial setup, you can add it later. This step is optional if you’ve selected skills from the default skills library in Viva.  

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home#/featureexplorer), select **Settings**, and then select **Viva**.  
2. Select **Manage skills library**. Select the **Skills library** tab, and then select **Custom skills**. You can filter by role and search by skill name.  

5. Select **View details** to see an overview of your imported files, who completed the import, and the import date.  

### Import custom skills library  

Follow these steps to either import your custom skills library for the first time or to reimport with changes to your initial custom import.

> [!NOTE]
> - Reimporting custom skills library overwrites existing data.  New skills will be added to your library. Deleted skills and any data associated with those skills will be immediately removed for your organization. Any changes to skill name or skill description are treated as a deletion of the old skill and the addition of a new skill.
> - The admin completing custom import must have permissions to view and edit the uploaded .csv files in SharePoint. 

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home#/featureexplorer), select **Settings**, and then select **Viva**.  
2. Select **Manage skills library**. Select the **Skills library** tab, and then select **New import**.  

3. Select **Download library template** and **Download mapping template.** 
4. Open the template files you downloaded.
5. Add the skills for your custom skills library into the library template.   
   - Required fields: Skill ID (externalCode), Skill Name (Name.en_US) 
   - Recommended fields: Skill Description (Description.en_US)  
6. Add the mapping information for jobs and their corresponding skills into the mapping template.      
   - Required fields: Job Title (JobTitle), Skill ID (SkillExternalCode) 
   - Optional, for reference only: Skill Name (SkillName.en_US) 
  
7. Save the templates as .csv (comma separated) files to a secure SharePoint location.
   
   Make sure you use commas as the delimiter. Your system might default to a different separator. In European countries, for example, it's often set to a semicolon `;`.

8. Get the file paths for your .csv files. 
   1. Select the file, and then select the ellipsis (**...**).
   2. Select **Details**, and then scroll to find the **Path**.  
   3. Select the option to copy the selected file's path to the Clipboard. The file path should be formatted like this: `https://contoso.sharepoint.com/TeamAdmin/Shared%20Documents/Folder%20Name/Skills%20Library.csv`
9. Paste the file paths for both files into the **Skills library file path** and **Skill mapping file path** fields. 
10. Select **Next** to begin file validation. If there's a problem with the file, you see an error message at this step.  

   > [!NOTE]
   > - The admin importing your custom skills information must have permissions to view and edit the uploaded .csv files in SharePoint.
   > - If you see a "file not found" error, try deleting "%20" strings from your pasted file paths. 

11. Review your custom skills data.  

12. Acknowledge that importing custom skills will immediately impact your users’ experience if skills is turned on.  

13. Select **Confirm** to import.  

If your library is published for users, the changes are reflected within 24 hours in their experience. It may take up to 72 hours for changes to your skills library to reflect in suggested skills for users and in Viva Learning.

> [!NOTE]

> - A minimum of 20 skills are required to import custom skills. Each file must be under 100mb. 
> - The following characters cannot be used as a prefix in any imported field '+', '-', '@', '=', '\t', '\r' 
> - Skill ID (externalCode) in the library file must map to Skill ID (SkillExternalCode) in the role to skill mapping file.  
> - JobTitle should match user profile job titles in Microsoft Entra ID  or Organizational Data in Microsoft 365. If your organization does not have fresh and complete data in this field for users, please update the system with the latest, either through Microsoft Entra ID or Organizational Data in Microsoft 365. The more accurately a title reflects a person's job, the more accurate skill suggestions will be. 


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

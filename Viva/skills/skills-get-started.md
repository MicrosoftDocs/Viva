---
title: Set up Skills in Viva 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 05/17/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.localizationpriority: medium
description: An introduction to setting up Skills in Viva, 
---

# Set up skills in Viva 

Start setting up Skills in Viva by building your skills library with skills from the default skills library in Viva or importing your own custom skills. 

## Create your skills library

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home#/featureexplorer), select **Settings**, and then select **Viva**.  
2. Select **Manage skills library**, and then select **Get started**.  
3. Read the overview, then select **Next**.
4. Choose the skills you want to use from the default skills library. The more skills you include from the default library, the more specific suggestions users see in their skills profiles. Choose one of the following, and then select **Next**.

   - **Use all skills (recommended)**: This option is highly recommended and includes all 7,000+ skills in the skills library.  
   - **Select specific skills**: This option lets you choose specific domains and skills within domains to include; however, choosing a subset of skills may limit the number of skill options and suggestions available to your users. (Note: A minimum of 500 skills is recommended.)  

5. Import your custom skills library. Choose whether you’d like to import your own custom skills library. This step is optional if you selected skills from the default skills library in Viva.  

   1. Select **Download library template** and **Download mapping template**. 
   2. Populate the templates with your skills data.  
      - Library template:  
         - Required fields: Skill ID (externalCode), Skill Name (Name.en_US) 
         - Recommended fields: Skill Description (Description.en_US)  
      - Mapping template:  
         - Required fields: Job Title (JobTitle), Skill ID (SkillExternalCode) 
         - Optional, for reference only: Skill Name (SkillName.en_US) 
        > [!NOTE]
  > - You need a minimum of 20 skills to import custom skills. Each file must be under 100mb. 
   > - The following characters can't be used as a prefix in any imported field '+', '-', '@', '=', '\t', '\r' 
   > - **Skill ID (externalCode)** must map to **Skill ID (SkillExternalCode)** in the role to skill mapping file.  
   > - **JobTitle** should match user profile job titles in Microsoft Entra ID or Organizational Data in Microsoft 365. If you don't have fresh and complete data in this field, update the system with the latest, either through Microsoft Entra ID or Organizational Data in Microsoft 365. The more accurately a title reflects a person's job, the more accurate skill suggestions will be.  
   > - When saving .csv files for custom imports, ensure you use the comma `,` as the delimiter (CSV comma delimited). Your system may default do a different separator. In European countries, for example, it's often set to a semicolon `;`.
   3. Save the templates as .csv (comma separated) files and upload them to a SharePoint site.  
   4. Get the file paths for your .csv files. 
       1. Select the file, and then select the ellipsis (**...**).
       2. Select **Details**, and then scroll to find the **Path**.  
       3. Select the option to copy the selected file's path to the Clipboard. The file path should be formatted like this: `https://contoso.sharepoint.com/TeamAdmin/Shared%20Documents/Folder%20Name/Skills%20Library.csv`
   5. In the Microsoft 365 admin center, paste the file paths for both files into the paths fields. Delete any "%20" strings in the file paths.
   6. Select **Next** to begin file validation. If there's a problem with the file, you see an error message at this step.  

   > [!NOTE]
   > The admin importing your custom skills information must have permissions to view and edit the uploaded .csv files in SharePoint. 

6. Review your organization’s skills library details and select **Next**. The data includes:  

     - The number of skills from the default skills library  
     - The number of skills and number of roles/job titles from your custom import  
     - The number of duplicate skills identified in your selection. If you have duplicates, your organization's custom data is prioritized over data from the default skills library in Viva.
7. Select **Turn on the skills library** to let your users can see and access skills in supported Microsoft 365 experiences. This is an optional step - if you don't turn on skills now, your skills library is still created, but it's not visible to users. You can make skills available to your users later by publishing the skills library from **Settings**.
8. Specify where else you want skills information to appear, and then select **Next**.
   - Select **Allow skills in Viva Learning** to make skills information visible in Viva Learning. [Learn more about skills-based learning inViva Learning](/viva/learning/skills-in-learning).

      This is a one-time consent to replace “interests” in Viva Learning with skills. Any existing "interests" data is deleted, and users see this replaced with "skills." This action can't be reversed. 

      It can take up to three business days for this change to reflect In Viva Learning.  
   - Select **Turn on skills in Viva Insights**, if it's available for your tenant. Learn more about the [skills landscape report in Viva Insights](/viva/insights/advanced/introduction-to-advanced-insights).

      > [!NOTE]
   >This is a premium Viva Insights scenario. Review the [licensing requirements](https://www.microsoft.com/en-us/microsoft-viva/pricing) Users receive **skill suggestions** relevant to their role by default. Users can control whether they see these suggestions in their skill settings. When skill suggestions are turned *off*, the user won't see any suggested skills and can only manually confirm skills from a list. 
   >
   - You can disable skill suggestions for specific users, groups, or your entire tenant by using an access control policy. For more information, see [control access to features in Viva](../feature-access-management.md).
    

10. Review your skills library and settings information. If there are any changes you want to make, go back to those steps and edit.  

    When you're ready, select **Confirm**.  

Your skills library is created, and your settings are saved. You can now manage your library and settings on an ongoing basis.


### Next Steps

[Manage your skills library](manage-skills-library.md)

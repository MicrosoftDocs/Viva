---
# Metadata Sample
# required metadata

title: Workplace Analytics setup
description: How to set up and configure Workplace Analytics
author: paul9955
ms.author: v-pascha
ms.date: 10/26/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: Workplace Analytics
---

# Set up Workplace Analytics

This article describes the steps that are required for setting up and configuring Workplace Analytics. While the Office 365 admin and the Workplace Analytics admin perform most of these steps, others in your organization help make decisions that relate to setup. For more information, see [Determine key personas and roles for implementation](Determine-key-personas.md). 

## Setup steps 

* **Owner** - The following persons or entities perform these steps:
  * **Workplace Analytics admin**. The Workplace Analytics admin does most of this work. In these steps, that person is referred to as "you."
  * **Office 365 admin**. In one step, you verify that the Office 365 administrator has assigned licenses and roles.  
  * **Workplace Analytics**. In a few steps, Workplace Analytics processes and validates data. 
* **Task** - Complete steps to set up and configure Workplace Analytics  
* **Outcome** - In your organization, people have been assigned licenses and roles. Those roles grant access to data that the people can use to analyze work habits and implement change in how employees spend their time.  

**To set up Workplace Analytics**

1.	**Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page**. If prompted, enter your organization's credentials. This page begins a sequence that guides you through setup. Under **Required to start**, the page describes the next task, verifying the assignment of licenses and roles:
   
      ![The Home page guides you through setup](../images/wpa/setup/01-home-start.png)
  
2.	**Licenses and roles**. Verify that your Office 365 admin has assigned licenses and roles to people in the organization, and then select **Next**. For more information, see [Assign licenses](assign-licenses-to-population.md) and [Assign roles](assign-roles-to-wpa-admins.md).

3.	**System settings**. Set the time zone, week days, weekend days, and working hours. For more information, see [Workplace Analytics system settings](configure-wpa-settings.md#system-settings). 

4.	**Privacy settings**. Set minimum group size and choose whether to hide subject lines, domains, email addresses, and terms in subject lines. For more information, see [Workplace Analytics privacy settings](configure-wpa-settings.md#privacy-settings). After you've finished making both the system settings and the privacy settings, select **Next**. 

5.	**Collaboration data**. Workplace Analytics extracts collaboration data (data about email usage, meetings, chats, and calls) from Office 365, and then processes it. This processing can last as long as a week. After it finishes, Workplace Analytics displays a "completed processing" status on the **Setup** page. 

      ![Workplace Analytics processes collaboration data](../images/wpa/setup/03-process-collab-data.png)

6.	**Prepare organizational data**. Export organizational data from your HR system into a UTF-8 encoded .csv file. For information about what data to export and how to structure it, see [Prepare organizational data](Prepare-organizational-data.md). 

7.	**Upload organizational data**. Upload the .csv file into Workplace Analytics. For more information, see [Upload organizational data](upload-organizational-data-1st.md). 

    The next three steps are part of the **Upload organizational data** task: 

    a.	**Map data**. Map the uploaded data to Workplace Analytics field names. For more information, see [Field mapping](upload-organizational-data-1st.md#field-mapping). 

    b.	**Data validation**. Workplace Analytics validates the upload and then notifies you whether your uploaded data validated. If it did not, you are advised what further action you can take. For more information, see [Data validation](Upload-organizational-data.md#data-validation). 

    c.	**Data processing**. Workplace Analytics processes the validated data. 

    ![Processing organizational data](../images/wpa/setup/07-process-org-data.png)

    When this processing finishes, your setup of Workplace Analytics is complete, as the status bar indicates: 

    ![Setup is complete](../images/wpa/setup/08-setup-complete.png) 

8.	**Set up meeting exclusion rules.** Some meetings (such as personal meetings or work-related social activities) reflect activities that would skew analysis of work-related collaboration if they were included in your data. You can remove meetings from analysis. For more information, see [Meeting exclusion rules in Workplace Analytics](../tutorials/meeting-exclusions-intro). 


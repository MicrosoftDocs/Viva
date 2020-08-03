---

title: Workplace Analytics setup
description: How to set up and configure Workplace Analytics
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Set up Workplace Analytics

This article describes the steps that are required to set up and configure Workplace Analytics. Although the Office 365 admin and the Workplace Analytics admin perform most of these steps, others in your organization help make decisions that relate to setup. For more information, see [Determine key personas and roles for implementation](Determine-key-personas.md). 

**Prerequisites:** See [Environment requirements](environment-requirements.md) to learn about Office 365 tenant requirements, Workplace Analytics licenses, and supported browsers. 

## Setup steps 

* **Owner:** The following persons or entities do the setup steps:
  * **Workplace Analytics admin** does most of the work and is the person referred to in the steps as "you."
  * **Office 365 admin** assigns licenses and roles in Step 2.  
  * **Workplace Analytics** processes and validates data in a few of the steps.
* **Task:** Complete steps to set up and configure Workplace Analytics.  
* **Outcome:** In your organization, people have been assigned licenses and roles. Those roles grant access to data that the people can use to analyze work habits and implement change in how employees spend their time. Also, you've set system defaults and privacy settings and an admin has uploaded organizational data.  

<!-- IN THIS VIDEO, MUST FIX A) EARLY SCREENSHOT THAT SHOWS EXPLORE PAGE AND B) END SEQUENCE THAT NO LONGER MATCHES CURRENT FRE. -->

### Video: Overview for admins

<iframe width="640" height="564" src="https://player.vimeo.com/video/282873274" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

**To set up Workplace Analytics**

1. **Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page**. If prompted, sign in with your work account. This page begins a sequence that guides you through setup. Under **Required to start**, the page describes the next task, and verifies the assignment of licenses and roles:

      ![The Home page guides you through setup](../images/wpa/setup/onboarding-intro.png)
  
2. **Licenses and roles** - Verify that your Office 365 admin has assigned licenses and roles to people in the organization, and then select **Next**. For more information, see [Assign licenses](assign-licenses-to-population.md) and [Assign roles](assign-roles-to-wpa-admins.md). 

   > [!Important]
   > On the **Home** page, under **Required to start**, Workplace Analytics admins can see the current number of assigned roles and licenses. They can proceed with setup only if the number of assigned licenses is greater than zero. Licenses can take from 24 up to 72 hours to activate after you purchase licenses. Until licenses are provisioned, unlicensed users will  get a [500 error](../tutorials/wpa-tool-500-error) when opening Workplace Analytics.

3. **System defaults** - Set the time zone, week days, weekend days, and working hours. For more information, see [Workplace Analytics system defaults](../Use/settings.md#system-defaults).

4. **Privacy settings** - Set minimum group size and choose whether to hide subject lines, domains, email addresses, and terms in subject lines. For more information, see [Workplace Analytics privacy settings](../Use/settings.md#privacy-settings). After you've finished making both the system defaults and the privacy settings, select **Next**.

   > [!Important] 
   > At this point, Workplace Analytics automatically extracts collaboration data (data about email usage, meetings, chats, and calls) in the background and keeps it ready for analysis. <u>Exception:</u> If your organization purchased Workplace Analytics before June 12, 2019, this extraction is not performed in the background. Before you can move on to step 5, you must wait for the extraction to complete. You will know that it has finished when Workplace Analytics displays a "completed processing" status on the **Setup** page.

<!-- REMOVED PER PRAMOD 31 MAY 2019: 
5. **Collaboration data** - Workplace Analytics extracts collaboration data (data about email usage, meetings, chats, and calls) from Office 365, and then processes it. This processing can last as long as a week. After it finishes, Workplace Analytics displays a "completed processing" status on the **Setup** page.

      ![Workplace Analytics processes collaboration data](../images/wpa/setup/03-process-collab-data.png)
-->

5. **Prepare organizational data** - Export organizational data from your HR system into a UTF-8 encoded .csv file. For information about what data to export and how to structure it, see [Prepare organizational data](Prepare-organizational-data.md).

6. **Upload organizational data** - Upload the .csv file into Workplace Analytics. For more information, see [Upload organizational data](upload-organizational-data-1st.md).

    The following steps are part of the **Upload organizational data** task:

    a. **Map data** - Map the uploaded data to Workplace Analytics field names. For more information, see [Field mapping](upload-organizational-data-1st.md#field-mapping). 

    b. **Data validation** - Workplace Analytics validates the upload and then notifies you whether your uploaded data validated. If it did not, you are advised what further action you can take. For more information, see [Data validation](upload-organizational-data-1st.md#data-validation). 

    c. **Data processing** - Workplace Analytics processes the validated data. 

    ![Processing organizational data](../images/wpa/setup/onboarding-validation-success.png)

    When this processing finishes, your setup of Workplace Analytics is complete, as the status bar indicates: 

    ![Setup is complete](../images/wpa/setup/onboarding-setup-complete.png) 

## Product availability

After organizational data has been uploaded and validated, no further action by the admin is necessary. After this point, it takes about one day before Workplace Analytics is ready for use. (For organizations with many licensed employees, it might take slightly longer.)

For example, analysts can begin to conduct analyses (by using the [Explore](../use/explore-intro.md) and [Queries](../tutorials/query-basics.md) pages) after privacy settings have been made, collaboration data has been extracted, and organizational data has been uploaded. As soon as Workplace Analytics is ready for use, an email notification to that effect is sent to users who've been assigned the [analyst role](../use/user-roles.md#role-descriptions-and-access-levels).    

## Related topics

[Environment requirements for Workplace Analytics](environment-requirements.md)

---
title: Use Advanced Configuration Data Apps
description: For highly trained users, Microsoft Viva Glint Advanced Configuration Data Apps offer the ability to perform complex data updates and export recipients for closed surveys. 
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: advanced configuration, data app, retroactive update, export users
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high pri
ms.date: 04/16/2024
---

# Use Advanced Configuration Data Apps

For highly trained users, Microsoft Viva Glint Advanced Configuration Data Apps allow you to perform complex data updates and export recipients for closed surveys. Use the following guidance to understand when and how to use Data Apps.

## EXPORT_USERS_FROM_SURVEY_CYCLE

For one or multiple survey cycles, export a snapshot of employee data as they were when a survey launched. 

### Use this information to:

- Confirm manager reporting lines at a fixed point in the past.
- Confirm attribute values for employees when a survey launched.
- Prepare a file for a retroactive update.

### To export users:

1. Select parameters:
   1. **surveyName:** Select **Load Values** and choose an option form the dropdown list.
   1. **cycleName:** Select **Load Values** and choose an option form the dropdown list.
   1. **includeAttributes:** Select **yes** to include all attributes. Select **no** to include required attributes only.
   1. **includeAllCycles:** Select **yes** to include all cycles. Select **no** to include the selected cycle only.
   1. **includePersonalEmail:** Select **yes** to include the personal email attribute (if applicable). Select **no** to exclude. 
1. Select **Save as ZIP** to download.

> [!NOTE]
> To preserve special characters and formatting, always open files by [importing data from .csv](https://go.microsoft.com/fwlink/?linkid=2247414) in Microsoft Excel.

## RETROACTIVE_PULSE_UPDATE

When a survey has closed, Manager Hierarchy information that displays in reporting isn't updated by regular employee data uploads. To update data in reporting, use the Retroactive Pulse Update Data App to apply new values.

If your update doesn't involve Manager Hierarchy, use the [Retroactive Upload](https://go.microsoft.com/fwlink/?linkid=2247341) feature instead.

> [!CAUTION]
> Do not perform a retroactive update while a Viva Glint survey is live.

### To perform a retroactive update to Manager Hierarchy:

Use these steps when manager reporting lines need to be corrected for a closed survey.

1. Export current employee data from the Glint People page to preserve employees and Manager IDs in their current state. When the retroactive update is complete, you'll reload this data to reset users to their current information.
1. Export survey cycle data with the EXPORT_USERS_FROM_SURVEY_CYCLE Data App for the survey(s) that will be updated.
1. Prepare an update file with the EXPORT_USERS_FROM_SURVEY_CYCLE file from Step 2.

   > [!IMPORTANT]
   > Retain all users from the survey cycle in your update file. Even users who are not directly impacted by a Manager ID change can have a reporting line impact.

   1. To preserve special characters and formatting, always open files by [importing data from .csv](https://go.microsoft.com/fwlink/?linkid=2247414) in Microsoft Excel.
   1. Delete data in all columns except for First Name, Last Name, Email, Employee ID, Status, and the Manager ID attribute.
   2. Delete columns that Viva Glint derives (like Age Group or Tenure). To confirm which attributes are derived go to **Configuration** and choose **People**. In the **Actions** menu select **Manager User Attributes** and go to the **Derived Attributes** section.
   1. Correct values for users that should have their Manager ID updated.
   1. Save your edited file with corrected values as a .csv or .xlsx file.
1. Go to **Configuration** and select **People** and choose the **Import** option.
   1. Leave the **Checking this box will update ALL employee records** setting **unselected**.
   1. Drag your update file to this window or select the **browse to choose a file** option to select it.
   1. Select **Import File** and select **Close** on the file processing message that appears.
   2. Refresh the **People** page to update the file processing status at the top of the page.
   3. When the upload completes, select **Review Upload**.
   4. Download and review any [errors](/viva/troubleshoot/glint/data-file-upload/file-upload-errors-warnings?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json).
   1. Select **Confirm Import**.

      > [!IMPORTANT]
      > If uploads aren't confirmed within 60 minutes, they expire and don't process.
      
1. After uploading your corrected data on the **People** page, go to **Advanced Configuration** and select **Data Apps**.
1. In **Data Apps**, select **RETROACTIVE_PULSE_UPDATE**.
1. Select parameters to update Manager ID:
   1. **surveyName:** Select **Load Values** and choose an option from the dropdown list.
   1. **cycleName:** Select **Load Values** and choose an option from the dropdown list.
   1. **roleOrDistributionList:**  Select **Load Values** and choose **(all)**.
   1. **attributeName:**  Select **Load Values** and choose your Manager ID attribute. 
   1. **reloadAnalytics:** Switch toggle to **Off**.
   1. Select **Execute, and show first 500 log records**.
1. Select parameters to update the overall Manager Hierarchy:
   1. **surveyName:** Select **Load Values** and choose an option from the dropdown list.
   1. **cycleName:** Select **Load Values** and choose an option from the dropdown list.
   1. **roleOrDistributionList:**  Select **Load Values** and choose **(all)**.
   1. **attributeName:**  Select **Load Values** and choose **(hierarchy) Manager**.
   1. **reloadAnalytics:** Switch toggle to **On**.
   1. Select **Execute, and show first 500 log records**.    
1. Confirm Manager Hierarchy changes in your **Dashboard** and **Reports**.
1. If the user data updates made by the correction file loaded for this update should be reset to current attribute values, load the data exported in Step 1 to the Glint People page.

   For example, if Manager corrections apply to survey data in the past, but have since changed for employees, be sure to load data exported in Step 1 to restore current information.

> [!NOTE]
> Depending on the number of Manager ID updates and users involved, it may take up to an hour to see changes reflected in reporting.

---
title: Use Advanced Configuration Uploads
description: For highly trained users, Microsoft Viva Glint the Advanced Configuration Uploads option allows you to perform custom data access uploads for users in bulk and complex data updates.
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: advanced configuration, uploads, retroactive update, bulk custom access
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/17/2024
---

# Use Advanced Configuration Uploads

For highly trained users, Microsoft Viva Glint the Advanced Configuration Uploads option allows you to view file upload details, perform custom data access uploads for users in bulk, and complete complex data updates.

## Review upload types

- **MANAGERS_UPLOAD:** To upload custom results data access for dashboard users in bulk.
- **Retroactive User Updates:** To perform an upload to user data in closed surveys.
- **ROLE_UPLOAD:** To upload users to a Viva Glint User Role, follow the guidance in this article: [Import and export Viva Glint User Roles](export-user-roles.md).

> [!NOTE]
> To upload employee data, follow the guidance in this article: [Upload your employee attributes to Viva Glint](upload-employee-attributes.md).

> [!CAUTION]
> Uploads performed in Advanced Configuration do not calculate derived fields or transform date formats to yyyy/mm/dd. If data should be derived, like Tenure from Hire Date, load data through the Viva Glint People page or SFTP.

## Perform a MANAGERS_UPLOAD

When several users need customized data access to their Viva Glint Dashboards, use the MANAGERS_UPLOAD to update their access in bulk. To grant 1 or a few users access to custom segments of data, grant custom access from their user profile: [Learn more](custom-user-role.md).

### To upload custom access for multiple users:

1. Prepare a file using the [custom data access export in User Roles](custom-access.md).
1. Save your file in .csv format with a comma separator and UTF-8 encoding.
1. In the **Advanced Configuration** menu, select **Uploads**.
1. In the **Choose job type** dropdown list, select **MANAGERS_UPLOAD**.
1. **Incremental:**
   1. Switch on this toggle to append access to users in your file.
   1. Switch off this toggle to overwrite all access for users in your file. Users not included in the file aren't impacted.
1. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section.
1. In the **Upload Job Details** page that appears, confirm that the **Uploaded Lines Summary** matches the changes in your uploaded file.
1. Select **Apply Upload to Database** to upload new values to and kick off a process to refresh reporting data.
1. In the **Load import file into database?** dialog, select **Yes**.
1. Go to some users' profiles to confirm that customized access appears as expected.

For example, the custom data access for this user:

|manager reference  |population   |add or remove|survey uuid |Cost Center |Manager Level 1 |Region |Country |City |
|----------|-----------|------------|------------|------------|------------|------------|------------|------------|
|ana.bowman@contoso.com|0 |ADD|aa1aa1aa-a1a1-1a1a-1a1a-111111111a11|37651 | | | | |
|ana.bowman@contoso.com|0 |ADD|aa1aa1aa-a1a1-1a1a-1a1a-111111111a11 |17123 | | | | |
|ana.bowman@contoso.com|1 |ADD|aa1aa1aa-a1a1-1a1a-1a1a-111111111a11 | |7890 | | | |
|ana.bowman@contoso.com|2 |ADD|aa1aa1aa-a1a1-1a1a-1a1a-111111111a11 | | |EMEA |Ireland |Dublin |

Displays on Ana's profile like this:

:::image type="content" source="../../media/glint/setup/glint-custom-access.png" alt-text="Screenshot of a user's custom Cost Center, Manager Team, and Location access.":::

## Perform Retroactive User Updates

When a survey closes, employee attributes that display in reporting aren't updated by regular employee data uploads. To update data in reporting in a closed survey, use the Retroactive User Updates option to apply new values. This option applies new data to past versions of user data and doesn't touch current employee information.

> [!NOTE]
> To retroactively update a Manager Hierarhcy, always use the RETROACTIVE_PULSE_UPDATE Data App and not the Retroactive User Updates option. [Learn more](/viva/glint/setup/glint-data-apps.md#retroactive-pulse-update).

> [!IMPORTANT]
> If your organization can't save files in .csv format, Retroactive User Updates isn't an opton. Instead:
> 1. Import an .xlsx file to the [People page](upload-employee-attributes.md).
> 2. [Create a User Role](set-up-user-roles.md) and add these users to the role.
> 3. Use the [RETROACTIVE_PULSE_UPDATE Data App](glint-data-apps.md) and select your User Role in **roleOrDistributionList.** 

### To perform a Retroactive User Updates upload:

> [!CAUTION]
> Do not perform a retroactive update while a Viva Glint survey is live.

1. Export survey cycle data with the EXPORT_USERS_FROM_SURVEY_CYCLE Data App for the surveys that need to be updated. [Learn more](/viva/glint/setup/glint-data-apps.md#export-users-from-survey-cycle).
1. Prepare an update file with the EXPORT_USERS_FROM_SURVEY_CYCLE file from Step 1.
   1. To preserve special characters and formatting, always open files by [importing data from .csv](https://go.microsoft.com/fwlink/?linkid=2247414) in Microsoft Excel.
   1. Delete all columns except for First Name, Last Name, Email, Employee ID, Status, and the attributes that need to be retroactively updated (for example, Department).
   1. Delete all user rows for employees whose data remains the same.
   1. Correct values for users and attributes that need to be updated.
      1. For example: To correct Department = ‘Sales’, ‘SALES’, ‘sales’, which create three values where there should be one in reporting, update all users to Department = ‘Sales’.
   1. Save your edited file with corrected values in.csv format.
1. In the **Advanced Configuration** menu, select **Uploads**.
1. In the **Choose job type** dropdown list, select **Retroactive User Updates**.
1. In the **Survey** dropdown list, select your survey.
1. In the **Survey Cycle** dropdown list, select your survey cycle.
1. Switch on the **Incremental** toggle.
1. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section.
1. Confirm the **File to be Uploaded** and select **Upload**.
1. In the **Upload Job Details** page that appears, confirm that the **Attribute(s)** and **Updated users** count match the attributes and count of users in your uploaded file.
1. Select **Apply Upload to Database** to upload new values and kick off a process to refresh reporting data.
1. In the **Load import file into database?** dialog, select **Yes**.
1. Confirm changes to attributes in your **Dashboard** and **Reports**.

> [!NOTE]
> Depending on the number of attributes and users involved, it may take up to an hour to see changes reflected in reporting.    


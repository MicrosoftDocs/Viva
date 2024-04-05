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
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 02/27/2024
---

# Use Advanced Configuration Uploads

For highly trained users, Microsoft Viva Glint the Advanced Configuration Uploads option allows you to view file upload details, perform custom data access uploads for users in bulk, and complete complex data updates.

## Review upload types

- **MANAGERS_UPLOAD:** To upload custom results data access for dashboard users in bulk.
- **USERS_UPLOAD:** 
   - To upload employee data, follow the guidance in this article: [Upload your employee attributes to Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742).
   - Use the guidance in this article to perform a Retroactive USERS_UPLOAD.
- **ROLE_UPLOAD:** To upload users to a Viva Glint User Role, follow the guidance in this article: [Import and export Viva Glint User Roles](https://go.microsoft.com/fwlink/?linkid=2230866).

> [!CAUTION]
> Uploads performed in Advanced Configuration do not calculate derived fields or transform date formats to yyyy/mm/dd. If data should be derived, like Tenure from Hire Date, load data through the Viva Glint People page or SFTP.

## Perform a MANAGERS_UPLOAD

When several users need customized data access to their Viva Glint Dashboards, use the MANAGERS_UPLOAD to update their access in bulk. To grant 1 or a few users access to custom segments of data, grant custom access from their user profile: [Learn more](https://go.microsoft.com/fwlink/?linkid=2266497).

### To upload custom access for multiple users:

1. Prepare a file with the following columns, in the order listed:
      1. **manager reference:** Populate with the email address of the user or users.
      1. **population:** Enter 0 for the first population. Each additional population increases in number for each user.
      1. **add or remove:** Enter ADD or REMOVE, in all caps.
      1. **survey uuid:** The survey ID of the program that the user should have customized access for.
         1. To find this ID, go to **Configure** and then choose **Survey Programs**. 
         1. Select the **Program** that a user will have custom access to. 
         1. From the **Program Summary** page, the link in your web browser contains the 36-character survey ID after the last forward slash.
         > [!NOTE]
         > To apply custom Focus Area access, enter: GOAL in this column. To apply custom Admin access, for users with advanced permissions, enter: ADMIN.
      1. **Attribute(s) from your employee data:** Match the label and case exactly from the Viva Glint attribute setup and populate with values that indicate data that the user should have access to.
         1. To grant custom access to: 
            1. Another manager's team, include an attribute column labeled: Manager Level 1 and list the Employee ID of the manager that another user should have access to.
            1. A level in a non-Manager hierarchy, include all levels above the level the user should have access to. Example: To grant access to Location Hiearchy Level 3 = Dublin, include columns for Region, Country, and City.
1. Save your file in .csv format.
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
|ana.bowman@contoso.com|0 |ADD|ab1cd2ef-g3h4-5i6j-7kl8-901234567m89 |37651 | | | | |
|ana.bowman@contoso.com|0 |ADD|ab1cd2ef-g3h4-5i6j-7kl8-901234567m89 |17123 | | | | |
|ana.bowman@contoso.com|1 |ADD|ab1cd2ef-g3h4-5i6j-7kl8-901234567m89 | |7890 | | | |
|ana.bowman@contoso.com|2 |ADD|ab1cd2ef-g3h4-5i6j-7kl8-901234567m89 | | |EMEA |Ireland |Dublin |

Displays on her profile like this:

:::image type="content" source="../../media/glint/setup/glint-custom-access.png" alt-text="Screenshot of a user's custom Cost Center, Manager Team, and Location access.":::

## Perform a Retroactive USERS_UPLOAD

When a survey has closed, employee attributes that display in reporting aren't updated by regular employee data uploads. To update data in reporting in a closed survey, use the Retroactive Upload to apply new values. This option applies new data to past versions of user data and does not touch current employee information.

> [!IMPORTANT]
> To retroactively update a Manager Hierarhcy, always use the RETROACTIVE_PULSE_UPDATE Data App and not the Retroactive USERS_UPLOAD option. [Learn more](https://go.microsoft.com/fwlink/?linkid=2245700).

### To perform a Retroactive upload:

Use these steps to perform a Retroactive Upload:

> [!CAUTION]
> Do not perform a retroactive update while a Viva Glint survey is live.

1. Export survey cycle data with the EXPORT_USERS_FROM_SURVEY_CYCLE Data App for the survey(s) that will be updated. [Learn more](https://go.microsoft.com/fwlink/?linkid=2245700).
1. Prepare an update file with the EXPORT_USERS_FROM_SURVEY_CYCLE file from Step 1.
   1. To preserve special characters and formatting, always open files by [importing data from .csv](https://go.microsoft.com/fwlink/?linkid=2247414) in Microsoft Excel.
   1. Delete all columns except for First Name, Last Name, Email, Employee ID, Status, and the attribute(s) that need to be retroactively updated (for example, Department).
   1. Delete all user rows for employees whose data remains the same.
   1. Correct values for users and attributes that need to be updated.
      1. For example: To correct Department = ‘Sales’, ‘SALES’, ‘sales’, which create 3 values where there should be one in reporting, update all users to Department = ‘Sales’.
   1. Save your edited file with corrected values in.csv format.
1. In the **Advanced Configuration** menu, select **Uploads**.
1. In the **Choose job type** dropdown list, select **USERS_UPLOAD**.
1. Switch on the **Retroactive** toggle.
1. Switch on the **Incremental** toggle.
1. In the **Survey** dropdown list, select your survey.
1. In the **Survey Cycle** dropdown list, select your survey cycle.
1. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section.
1. Confirm the **File to be Uploaded** and select **Upload**.
1. In the **Upload Job Details** page that appears, confirm that the **Attribute(s)** and **Updated users** count match the attributes and count of users in your uploaded file.
1. Select **Apply Upload to Database** to upload new values and kick off a process to refresh reporting data.
1. In the **Load import file into database?** dialog, select **Yes**.
1. Confirm changes to attributes in your **Dashboard** and **Reports**.

> [!NOTE]
> Depending on the number of attributes and users involved, it may take up to an hour to see changes reflected in reporting.    


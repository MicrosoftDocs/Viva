---
title: Upload your employee attributes in Viva Glint
description: Learn how Viva Glint provides the most relevant results reporting when employee attributes are uploaded on a regular cadence.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: SFTP, file requirements, upload attributes, manual upload, update attributes, Employee Attribute File
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 03/23/2023
---

# Upload your employee attributes

User file imports help admins to keep users current with their organization's HRIS system. During the Platform Setup, you determine which upload method to use when uploading your employee attributes, such as manually or using a Secure File Transfer Protocol (SFTP).

>[!WARNING]
> For security reasons, use only the two options provided; never email your employee attributes file.

## Import attributes using SFTP

Before you begin SFTP attributes transfer, ensure that Microsoft Viva Glint has already added your public SSH Key and IP addresses for all users that connect to your account and complete the Allowed List steps.

### File requirements

The files exported by your HRIS system should be either comma-separated values (CSV) or Microsoft Excel (TM) files (.csv or .xlsx extensions). CSV is the preferred format with UTF-8 encoding. The following section provides additional information on the file format and structure.

- File format – The Viva Glint system can accept employee attributes in either 'CSV – UTF 8' or 'XLSX' format. Files need to remain in that format once we set the expected format, or a failure message is generated.
- File names - There are no specific restrictions. If your organization doesn’t have specific requirements for naming the files, the following naming convention is preferred:
  - Full File: $clientuuid$_user_full_yyyymmdd.csv
  - Incremental file: $clientuuid$_user_delta_yyyymmdd.csv
  - The `$clientuuid$` part of the file name is your unique ID within Viva Glint.
- Dates – Choose one format you use for dates and adhere to it. Our preferred format is “yyyy/mm/dd". If dates are sent in another format, we can configure the system to reformat the dates as the file is uploaded initially. However, the system shows errors if date formats don't match once we set the expected format.
    > [!NOTE]
    > The date format must include “/” instead of a hyphen between year, month, and day, and all dates must be in the same format.
- Attribute names - Once attributes are determined, the attribute names (column headers) must remain the same. For example, “Employee ID” can't be changed to “EMP ID.”

### Upload your attributes on the SFTP Server

Once you access your SFTP account, you'll see options for multiple folders. Employee files need to be dropped in either the **/files/user_full** or **/files/user_delta** folder. 

- The **user_full** folder is for full employee files, which means the file overwrites previous user attributes in the system. All others that aren't in this upload will be moved to INACTIVE status.
- The **user_delta** folder is for incremental employee files, which means that the system only updates the employees in the file; it won't update or inactivate anyone, not in that file.

   > [!NOTE]
   > Your SFTP account and folders may vary based on your application.

   > [!IMPORTANT]
   > Ensure your file is placed in the correct file location on the SFTP server. If you have an incremental file and place it in the user_full file, all employees in the file will be updated, but employees who are not in the incremental file will be changed to INACTIVE. It is essential to understand where to place your files.

Our system gathers files from the user_full and user_delta folders. Once a file is placed in one of the folders, it can take up to 30 minutes to process. After the file uploads, the system will send you either a success or failure message. To have employees within your organization receive email notifications (including warnings and errors) for automated file uploads, share a list of email addresses when setting up attributes' automation. An email is sent for each file uploaded, regardless of success or failure.

## Import attributes manually

The import function allows you to quickly modify employee records in bulk and add new users. You can also import employee attributes manually: 

- To achieve a *one-off* upload of employee attributes outside of an SFTP upload 
- As a division or company upload for the user to maintain confidentiality around errors or attributes for that specific upload
- For a custom file upload (different from the regularly scheduled file upload)
- When there's no SFTP access or for initial testing
- For a quick upload of user attributes

> [!TIP]
> Update your employee file on a regular basis. Ensure that your latest employee attributes have been sent and uploaded prior to a survey launch as your attributes can't be changed at the point of survey launch.

### Process for manual import of employee attributes

The following steps guide you through the process of importing the attributes manually: 

1. Select the **Configure** symbol. 
2. In the **Employees** section, select **People**.
3. Select **Import**.
4. Select the checkbox when updating all employee records, both in the file and in the system. 
5. Drag and drop your file or browse to select it. 

    Select **Import File**. A message appears, informing you that an email is sent once the upload is ready for review and then confirm your changes.
6. Then, select **Close**.

> [!NOTE]
> Only the user performing the upload will receive an email, even when other file notification emails go to multiple email addresses.

## Update your Employee Attribute File

Your company can send Employee Attribute File updates whenever necessary and based on whatever cadence works best for you. Some companies send daily, weekly, or monthly updates, while others don’t forward updates until they're ready to launch a survey. 

> [!TIP]
> Update your Employee Attribute File weekly, or at least at a regular cadence. 
>
> If you have fewer than 10,000 employees in your attributes base, a daily feed of the full file should be sufficient, and you won’t have to send an incremental file. If you have a large employee data set with several attributes (50+), sending full files 1-2 times per month with daily incremental files may make more sense for your company’s needs.

## Related topics

- [Create Employee Attribute Template](create-employee-attribute-template.md)

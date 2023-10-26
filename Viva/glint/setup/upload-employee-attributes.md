---
title: Upload your employee attributes in Viva Glint
description: Learn how Viva Glint provides the most relevant results reporting when employee attributes are uploaded on a regular cadence.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: file requirements, upload attributes, manual upload, update attributes, Employee Attribute File
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 03/23/2023
---

# Upload your employee attributes to Viva Glint

User file imports help admins to keep users current with their organization's HRIS system. During the Platform Setup, learn how to upload employee data in the Microsoft Viva Glint application.

>[!WARNING]
> For security reasons, never email your employee attributes file.

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

## Import employee data

The import function allows you to quickly modify employee records in bulk and add new users.

> [!CAUTION]
> Employee data can't be deleted. This option performs a full employee upload, which applies any changes in the file and marks anyone not in the file as an inactive employee.
     
> [!TIP]
> Update your employee file on a regular basis. Ensure that your latest employee attributes have been sent and uploaded prior to a survey launch as your attributes can't be changed at the point of survey launch.

### Process for import of employee attributes

The following steps guide you through the process of importing the attributes manually: 

1. Select the **Configure** symbol. 
2. In the **Employees** section, select **People**.
3. Select **Import**.
4. Select the checkbox when updating all employee records, both in the file and in the system. 
5. Drag and drop your file or browse to select it. 

    Select **Import File**. A message appears, informing you that an email is sent once the upload is ready for review and then confirm your changes.
6. Then, select **Close**.

> [!NOTE]
> Only the user performing the upload will receive an email when the file has processed.

## Update your employee data regularly

Your company can send employee data updates whenever necessary and based on whatever cadence works best for you. Some companies send daily, weekly, or monthly updates, while others don’t forward updates until they're ready to launch a survey. 

> [!TIP]
> Update your employee data weekly, or at least at a regular cadence. 
>
> If you have fewer than 10,000 employees, a daily feed of the full file should be sufficient, and you won’t have to send an incremental file. If you have a large employee base with several attributes (50+), sending full files 1-2 times per month with daily incremental files may make more sense for your company’s needs.

## Related topics

- [Create Employee Attribute Template](create-employee-attribute-template.md)

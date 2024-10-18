---
title: Understand Viva Glint SFTP and data automation
description: Use Microsoft Viva Glint Secure File Transfer Protocol (SFTP) to establish regular imports of employee data.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: sftp, data transfer, data automation
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/07/2024
---

# Understand Viva Glint SFTP and data automation

Use Microsoft Viva Glint Secure File Transfer Protocol (SFTP) to establish regular imports of employee data. An automated data feed enables you to keep your HR Information System (HRIS) data in sync with Viva Glint and allows your organization to:

- Send surveys and results to the right participants at any time.
- Automatically trigger surveys for employees at specific points in the employee lifecycle.
- Always have the most up-to-date employee information.

## Prepare data for import

Before transferring data to Viva Glint with SFTP, ensure that you review information on Viva Glint attribute fundamentals and complete your attribute setup. [Learn more](https://go.microsoft.com/fwlink/?linkid=2240826).

> [!CAUTION]
> Ensure that all Company Admin users are included in your first file upload, with Employee IDs that match the IDs in Viva Glint. If not, Company Admin users will be deactivated and lose access to the platform.

## Manage SFTP settings

In Viva Glint general settings, manage Public SSH keys, add public IP addresses, specify notification users, manage encryption settings, and view SFTP credentials. [Learn more](https://go.microsoft.com/fwlink/?linkid=2247430).

## Understand automated data import

Viva Glint SFTP: 

- Allows for full and partial data files.
- Regularly checks for and automatically imports new files.
- Derives attributes to create calculated fields during import.
- Works best with recommended file formats.

## SFTP directories

In your SFTP account, there are two (2) directories that Viva Glint monitors for files to automatically import:

- **/files/user_full:** Use for FULL file uploads - existing employee records in the platform that aren't included in your file become INACTIVE.
- **/files/user_delta:** Use for PARTIAL file uploads - only the employee records in the file are updated in the platform; all others are unchanged.

> [!NOTE]
> - Files are automatically deleted from SFTP after 48 hours.
> - Files that cause warnings and errors can be downloaded from the **Activity Audit Log** in **General Settings** for 28 days after import.

> [!TIP]
> For some versions of SAP Success Factors and Workday, "/files" may be auto-appended to the file path for SFTP transmissions. Remove "/files" from the file path ("/user_full" or "/user_delta") to prevent upload errors if your HRIS version auto-appends "/files".

## Transfer methods

Depending on how frequently your organization imports data to Viva Glint, consider which SFTP data transfer method best meets your needs.

- **Automated HRIS data feed:** Work with your employee data team to establish an automated export that is transmitted from your HRIS to SFTP directly.
- **Manual SFTP file transfer:** Connect with an FTP application to manually place a full or incremental file on SFTP.

## Derived attributes

While your employee data uploads to Viva Glint, derived attributes and values are calculated for Manager Hierarchy, Tenure, and Age Groups based on selections made during your attribute setup. [Learn more](send-employee-attributes.md).

> [!NOTE]
> Don’t include derived attributes in your employee data file, Viva Glint creates these fields.

## File best practices

Select a file transfer frequency, format, layout, and naming convention based on your company's needs and HRIS capabilities.

### Frequency:

Update your employee data at least weekly or at a regular cadence that aligns with your company's survey schedule.  

If you have fewer than 10,000 employees, a daily feed of the full file should be a good frequency, and incremental files can be uploaded for one-off updates. If you have a large employee base with several attributes (50+), sending full files 1-2 times per month with daily incremental files may make more sense for your company’s needs. Discuss with your HRIS team to find out data file transfer possibilities.

### Format and layout:

Consistent file format and layout over time ensure successful file imports. Maintain the same attribute labels in your file’s header row and select one file format from Viva Glint’s options:

- **.csv** with a comma separator and UTF-8 encoding. When values contain commas, enclose in double quotation marks.
- **.xlsx** with a single tab and no password or formulas.

### Naming convention:

Viva Glint recommends the following file naming conventions, where "companyid" is your unique ID within Viva Glint, but this file name method isn't required. Ensure that whichever file name you select is 64 characters or fewer, including the file extension.

- Companyid_user_full_yyyymmdd.csv
- Companyid_user_delta_yyyymmdd.csv

For example: contoso_user_delta_20230101.csv

> [!IMPORTANT]
> File extensions must reflect PGP encryption, if used. For example, an encrypted .csv file extension would appear as: contoso_user_full_20230101.**csv.pgp**

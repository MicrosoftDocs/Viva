---
title: Review employee data with Viva Glint checklists
description: Confirm that your employee data file, attributes, and attribute values align with Microsoft Viva Glint requirements with these checklists.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: data file, quality check, data checklist, checklist, quality assurance
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/20/2024
---

# Review employee data with Viva Glint checklists

Confirm that your employee data file, attributes, and attribute values align with Microsoft Viva Glint requirements with these checklists.

## Review file level items

|Item   |Check that...   |
|:----------|:-----------|
|File name    |There aren't special characters (like @ or %) in the name.       |
|File format    |The file is .xlsx (one sheet with no password or formulas) or .csv (comma delimited and UTF-8 encoded).       |
|File encryption    |If you opt for PGP encryption, the file extension reflects the encryption (for example: filename.csv.pgp).       |

## Review attribute level items

|Item   |Check that...   |
|:----------|:-----------|
|Required attributes | There are columns for Viva Glint required attributes: First name, Last name, Email address, Employee ID, and Status. |
|Truncation   | Attribute labels in the header row don't exceed 64 characters.      |
|Naming convention   | Attribute labels in the header row are free of typos and in a user friendly format. These become report filters.      |
|Hidden columns and rows  | There aren't any hidden columns or rows (remove).    |
|Blank columns and rows  | There aren't any columns or rows with data removed that still show in the file (remove).     |
|Manager hierarchy fields  | There's a Manager ID field (along with Employee ID) to create a manager hierarchy.     |
|Hierarchy fields  | There are attributes for each reporting hierarchy (for example: Region, Country, and City).     |
|Derived attributes | Attributes that Viva Glint derives (Age Group and Tenure) aren't included in the file. [Learn more](https://go.microsoft.com/fwlink/?linkid=2272183).    |
|Time zone  | Time zone is included as a column in the file. [Learn more](https://go.microsoft.com/fwlink/?linkid=2272525).    |
|Language codes |  Survey and/or dashboard language columns are included as columns in the file. [Learn more](https://go.microsoft.com/fwlink/?linkid=2272182).    |

## Review attribute value level items

|Item   |Check that...   |
|:----------|:-----------|
|Truncation   | Attribute values in the file don't exceed 64 characters.      |
|Required field: First name  | All records are populated with a value.      |
|Required field: Last name   | All records are populated with a value. If no last name information is available, populate with a period (.) or a dash (-).      |
|Required field: Email address   | All records are populated with a unique value. For users with no email address, populate with Employee ID + '@example.com.'      |
|Required field: Employee ID  | All records are populated with a unique value.      |
|Required field: Status | All records are populated with ACTIVE or INACTIVE, in all caps.      |
|Date format  | All date attributes follow the same format and don't contain a dash (-). Viva Glint preferred format: yyyy/mm/dd.      |
|Inactive employees  | Inactive users are only included if they're 1) termed, 2) on leave, or 3) are needed to complete a manager hierarchy.      |
|Manager ID  | All users **except the CEO** have a Manager ID value populated.      |
|Time zone  | Time zone values are populated correctly for all users. See the [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533) for correct time zone values.     |
|Language codes | Survey and/or dashboard language values are populated correctly for all users. See the [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533) for correct language values.      |
|Consistency | Values have a consistent spelling and naming convention. For example, department value of 'Sales,' 'SALES,' and 'sales' all appear as different values in reporting.      |

## Next step
After confirming that your data follows Viva Glint requirements and best practices with checklists, set up attributes in Viva Glint to create a mapping of your employee attributes.

> [!div class="nextstepaction"]
> [Setup attributes in Viva Glint](send-employee-attributes.md)

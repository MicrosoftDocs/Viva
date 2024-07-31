---
title: Viva Glint employee attribute fundamentals
description: Learn how Viva Glint uses data about the people in your organization to convert survey feedback into insightful and action-oriented information to improve employee engagement.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: standard attributes, custom attributes, functional attributes, time zones, languages
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 07/31/2024
---

# Viva Glint employee attribute fundamentals

## Understand attribute types

Attributes are data about the people in your organization. Attributes are used to convert feedback into insightful and action-oriented intelligence to improve employee engagement and achieve business goals.

Attribute column headers (labels) are unique to your organization. For example, your HR information system (HRIS) may include "Employee ID," while another company has "Work ID." The labels in Viva Glint guidance are for example purposes only. Choose name labels that match your organization's HRIS.

## Standard attribute types

- **Required attributes**: These are required fields for each user in your Employee Data File.
- **Recommended attributes**: Custom data for your organization that can include fields that are converted into derived values (or buckets), like Tenure.

>[!NOTE]
> Attributes that are used to derive other fields are required for all future uploads. For example, Viva Glint uses Hire Date to create Tenure groups, Hire Date is required in all uploads.

### Attributes by item and survey type

| **Attribute** | **Description/Notes** | **Required for Engagement surveys** | **Required for Employee Lifecycle surveys** |
|---|---|---|---|
| **Status** | Must always be fully capitalized ACTIVE or INACTIVE.<br>An employee on temporary leave should have their status updated to INACTIVE and then returned to ACTIVE upon return. | Yes | Yes |
| **First name** | Appears in email invites and reminders (can be the legal first name, preferred first name, or whichever is in your HRIS). | Yes | Yes |
| **Last name** | Employee’s legal last name field from your HRIS. | Yes | Yes |
| **Employee ID** | Each employee has a unique ID. Don't use blanks or spaces. | Yes | Yes |
| **Email address** | Each employee should have a unique email address. Don't include extra spaces.<br>If an employee doesn't have an email address, copy the employee’s unique ID into the email field. | Yes | Yes |
| **Personal email address** | Opt to include personal email address to contact exiting employees. | No | Recommended |
| **Time zone** | See [Time zones](#time-zones) | No | No |
| **Language** | See [Language](#languages) | No | No |
| **Manager ID** | Providing the employee ID of the manager for each employee allows automatic build-out of a manager hierarchy. | Highly recommended | Highly recommended |
| **Hire date** | Used to derive tenure buckets.<br>Viva Glint standard values: <1 Year, 1-2 Years, 2-4 Years, 4-6 Years, 6-10 Years, 10-15 Years, 15-20 Years, 20+ Years.* | No | Yes, to trigger Employee Lifecycle Onboarding surveys |
| **Birth year** | Used to derive age group buckets.<br>Viva Glint standard values: <25, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, and 70+ | No | No |
| **End date** | Employee’s termination date. | No | Yes, for triggering Employee Lifecycle Exit surveys |

*Tenure values for new Viva Glint customers after January 13, 2024. Prior to this date: 0-1 Year, 1-2 Years, 2-3 Years, 3-4 Years, 4-5 Years, 5-7 Years, 7+ Years.

## Custom attributes

Use custom attributes to see which groups of employees are more engaged than others and use this information to develop action plans to improve engagement. Your organization can include up to 100 custom attributes; required and hierarchy attributes don't contribute to the 100 custom attribute limit. Include attributes in your employee data file header row with labels that match your HRIS.

**Best practices**:

- The more attributes you provide, the more ways data can be sliced and diced to provide richer insights and alerts. 
- Attributes that are too specific don't meet the minimum confidentiality threshold of five to appear in reporting, so avoid them.

### General Data protection Regulation (GDPR) compliance for attributes

Confidentiality around employee data is of the highest priority for Microsoft Viva Glint. Using [EU General Data Protection Regulation (GDPR) guidelines](https://www.microsoft.com/professionalservices/gdpr), we apply these privacy protection standards globally to ensure that every person’s data is handled with the utmost confidentiality and integrity.

## Optional system attributes

Optional system attributes are values that indicate how and when communications are sent to an employee, such as time zone and language.

|Optional System Attribute  |Description  |
|----------|-----------|
|Survey Language     |The language in which employees receive surveys and emails.      |
|Dashboard Language|The language in which users view dashboards.  |
|User Timezone|The time zone in which survey communications are sent.  |
|Personal Email|Users' personal email addresses that can be used to survey exiting employees. Select Company and Personal Email in the Communications section of your survey program.  |

>[!NOTE]
> Time zone and language values are case sensitive and must be sent exactly as they appear. Employee records with blank or invalid time zone or language values receive communications in your organization’s default time zone and language.  

### Time zones

Global companies often include a time zone attribute column in their Employee Attribute Template to trigger emails in employees’ time zones. Use the Time Zone tab of the [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533) to find valid time zone values. Before a survey launches, ensure that all employees have a valid value attached to their records.

### Languages

Use the Language Codes tab on the [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533) to find language values that trigger survey emails in an employee’s preferred language. Ensure that you include a Language column in your Employee Attribute File. Before a survey launches, ensure that all employees have a valid value attached to their records.

If you also supply language values to indicate users’ dashboard languages (for users who view reports), include a separate column (example: Dashboard Language).

>[!NOTE]
> Dashboards do not support languages that are read from right to left.

## Next step
Learn about Viva Glint organizational hierarchy fundamentals, including a Glint calculated Manager Hierarchy and other hierarchy groups.

> [!div class="nextstepaction"]
> [Viva Glint organizational hierarchy fundamentals](hierarchy-fundamentals.md)

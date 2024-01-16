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
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 01/16/2024
---

# Viva Glint employee attribute fundamentals

## Understand and set up attribute types

Attributes are data about the people in your organization. Attributes are used to convert feedback into insightful and action-oriented intelligence to improve employee engagement and achieve business goals.

Attribute column headers (name labels) may be customized. For example, you might choose "Employee ID," while another company chooses "Work ID." For this reason, know that the labels in our guidance are for purposes of example only. Choose name labels that make sense to your organization as these labels appear on your reports.

## Standard attribute types

- **Required attributes**: When building your Employee Attribute Template, this is the data that is required to be part of your Employee Data File.
- **Recommended attributes**: Data that can be converted into derivative groups (or buckets). Derivative groups keep attributes from being used to specifically identify an employee.

>[!NOTE]
> Recommended attributes are not required, but if sent initially in your Employee Attribute Template, then they are required for all future uploads.

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
| **Manager ID** | Providing the employee ID of the manager for each employee allows automatic build-out of a managerial hierarchy. | Highly recommended | Highly recommended |
| **Hire date** | Used to derive tenure buckets.<br>Viva Glint standard values: 0-1 year, 1-2 years, 2-3 years, 3-4 years, 4-5 years, 5-7 years, 7+ years. | No | Yes, for Employee Lifecycle *Onboarding* surveys |
| **Birth year** | Used to derive age group buckets.<br>Viva Glint standard values: <25, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, and 70+ | No | No |
| **End date** | Employee’s termination date, off-boarding date, last day, and so on. | No | Yes, for Employee Lifecycle Exit surveys |

## Custom attributes

By selecting more than required attributes only, you can see what groups of employees are more engaged than others and use this information to develop action plans to improve engagement. 

Your template may include up to 100 custom, flat attributes. *A flat attribute is a descriptor that can't be further broken down, such as gender, work location, or department.*

Add custom attributes to the header row on your template, named the way that seems most sensible to you. Choose attributes that can boost the way you do business.

**Best practices**:

- The more attributes you provide, the more ways data can be sliced and diced to provide richer insights and alerts. 
- Attributes that are too specific won't meet the minimum confidentiality threshold of five to appear in reporting, so avoid them.

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
> Time zone and language values are case sensitive and must be sent exactly as they appear. Employee records with blank or invalid time zone or language values will receive communications in the organization’s default time zone and language.  

### Time zones

Global companies often include a time zone attribute column in their Employee Attribute Template to trigger survey emails in employees’ time zones. Use the Time Zone tab of the Employee Attribute Template to find valid time zone values. Before a survey launches, ensure that all employees have a valid value attached to their records.
> [!TIP]
> For global companies, consider adding time zones and languages meaning to reach employees in their appropriate timezones and their preferred language.

### Languages

Use the Language Codes tab of the Employee Attribute Template to find language values that trigger survey emails in an employee’s preferred language. Ensure that you include a Language column in your Employee Attribute File. Before a survey launches, ensure that all employees have a valid value attached to their records.

If you also supply language values to indicate users’ dashboard languages (for those who view reports), include a separate column (example: Dashboard Language).

> [!TIP]
> For global companies, consider adding time zones and languages meaning to reach employees in their appropriate timezones and their preferred language.

>[!NOTE]
> Dashboards do not support languages that are read from right to left.

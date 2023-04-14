---
title: Viva Glint Attribute fundamentals
description: Learn how Viva Glint uses data about the people in your organization to convert survey feedback into insightful and action-oriented information to improve employee engagement.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: viva glint, employee data, attribute types, glint attributes, glint data
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/04/2023
---

# Attribute fundamentals

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
| **Status – ACTIVE or INACTIVE** | Must always be fully capitalized.<br>An employee on temporary leave should have their status updated to INACTIVE and then returned to ACTIVE upon return. | Yes | Yes |
| **First name** | Appears in email invites and reminders (can be the legal first name, preferred first name, or whichever is in your HRIS). | Yes | Yes |
| **Last name** | Employee’s legal last name field from your HRIS. | Yes | Yes |
| **Employee ID** | Each employee has a unique ID. Don't use blanks or spaces. | Yes | Yes |
| **Email address** | Each employee should have a unique email address. Don't include extra spaces.<br>If an employee doesn't have an email address, copy the employee’s unique ID into the email field. | Yes | Yes |
| **Time zone** | See [Time zones](#time-zones) | Yes | Yes |
| **Language** | See [Language](#languages) | Yes | Yes |
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

Confidentiality around employee data is of the highest priority for Microsoft Viva Glint. Using [EU General Data Protection Regulation (GDPR) guidelines](https://microsoft.sharepoint.com/:w:/r/teams/PSTeam/_layouts/15/Doc.aspx?sourcedoc=%7BDA8D8CB5-F3CB-4433-9798-EC1D052A205D%7D&file=Confidentiality%20in%20Viva%20Glint%20programs.docx&action=default&mobileredirect=true&share=IQG1jI3ay_MzRJeY7B0FKiBdAXkwdmWiW1Pu4SDT7ZUHgAg&cid=ec5d3ef1-8c67-430b-9de2-5d5507db4843), we apply these privacy protection standards globally to ensure that every person’s data is handled with the utmost confidentiality and integrity.

## Functional attributes

Functional attributes are values that indicate how and when communications are sent to an employee, such as time zone and language.

>[!NOTE]
> Time zone and language values are case sensitive and must be sent exactly as they appear. Employee records with blank or invalid time zone or language values will receive communications in the organization’s default time zone and language.  

### Time zones

Global companies often include a time zone attribute column in their Employee Attribute Template to trigger survey emails in employees’ time zones. Use the Time Zone tab of the Employee Attribute Template to find valid time zone values. Before a survey launches, ensure that all employees have a valid value attached to their records.

### Languages

Use the Language Codes tab of the Employee Attribute Template to find language values that trigger survey emails in an employee’s preferred language. Ensure that you include a Language column in your Employee Attribute File. Before a survey launches, ensure that all employees have a valid value attached to their records.

If you also supply language values to indicate users’ dashboard languages (for those who view reports), include a separate column (example: Dashboard Language).

>[!NOTE]
> Dashboards do not support languages that are read from right to left.
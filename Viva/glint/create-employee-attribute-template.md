---
title: Create your Employee Attribute Template in Viva Glint
description: Learn how Viva Glint uses the attributes and hierarchies you provide about the people in your organization to surface meaningful and actionable insights. The template is the row of column headers; all the data you will provide.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: HRIS planning tool, upload data, data file, header row, required attributes, custom attributes
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 03/24/2023
---

# Create your Employee Attribute Template in Viva Glint

The Employee Attribute Template is a guide and planning tool used to document your organization’s file format and attribute selections, before uploading your employee data to the Microsoft Viva Glint system. This essential step helps our team to know which attributes to expect so your data can be structured and surfaced correctly in reporting and role reporting.

Use our template as guidance to ensure that data is uploaded in the correct format, incorporating our recommendations and requirements.

Ensure that attribute labels that you set up initially stay consistent over time in the Employee Data Files transferred to Viva Glint. For example, if an attribute is set up as “*Employee ID*,” it can't later be recognized as the same column renamed as “Employee Number.”

## Why is creating an employee data template important? 

Every report, recommendation, and action plan that is built for your organization relies on the foundation of employee data that you provide. The collection of detailed information about the people in your organization is essential, so we can use cuts of that data to highlight meaningful insights from survey results. In doing that, Viva Glint helps you to determine what you are doing right and where your opportunities lie.

A successful process means that you first need to: 

- Understand the definitions and why we ask for attributes and hierarchies
- Use the Employee Attribute Template to format and create your data file
- Understand how to set up and upload your data to Viva Glint

### Use your IT department for support

Many companies rely on their IT department to stage and maintain the backend processes that power Viva Glint programs. Your IT department may be the best internal expert when it comes to certain data preparation tasks.

## Create the template

[Download the Employee Attribute Template here](https://community.glintinc.com/glint-guided-experience-documentation-43/employee-data-attribute-template-1446). The following extensions are supported for files exported by your HRIS system:

- .csv for files with a comma delimiter and UTF-8 encoding
- .xlsx for files in Microsoft Excel format with a single tab of data

The first page of the template contains instructions for building your own template. Follow the guidance on the instruction page, the following tabs, and in the following table  to set up your template.

>[!TIP]
>Your template is only the column headers. No employee data is needed at this point.

### Definitions for Employee Attribute Template

| **Term** | **Definition** |
|---|---|
| **Employee Attribute Template** | XLSX guidance for creating your organization’s file format and data selections, before setting up attributes in our platform. |
| **Attribute** | Demographic details about employees. They're also referred to as filters in the platform. |
| **Attribute Header Row** | The blueprint of the Employee Attribute Template. It dictates the columns of information and the name labels for the columns. |
| **Required Attribute** | Information about each employee in your organization that Viva Glint requires to be part of your Employee Attribute Template status, such as:<li>Status: ACTIVE or INACTIVE <li>First name <li>Last name <li>Email address <li>Employee ID |
| **Custom Attribute** | Any employee information collected in addition to the required attributes. <br>Up to 100 custom attributes can be collected. Examples: birth year, hire date, gender, work location, department. <br><p>Viva Glint is GDPR compliant and prohibits the processing of any employee information classified as sensitive. No attributes classified as sensitive can be incorporated into an Employee Attribute Template. |
| **Flat Attribute** | A category that can't be broken down further, such as age group or gender. |
| **Functional Attribute** | A value that indicates how and when communications are sent to an employee, such as language and time zone. |
| **Hierarchy** | Filtering down of an employee attribute into levels from highest to lowest, largest to smallest, etc. to provide more precise insights into engagement.  <br>Example: Region > Country > State > City |
| **Derivation** | Other fields configured based on employee attributes. <p>Examples: Age groups can be derived from birth year or tenure can be derived from hire date. |
| **Schema** | The framework in our platform’s backend, which stores a mapping of your organization’s attributes. |

### Instructions to upload your Employee Attribute Template

You'll receive an email confirming that Viva Glint is ready to receive your data in the template that has been prepared for you in our backend.

Once your header row (Employee Data Template) is complete, move on to Create your Employee Attribute File.

## Related topics

- [Upload your employee attributes](upload-employee-attributes.md)
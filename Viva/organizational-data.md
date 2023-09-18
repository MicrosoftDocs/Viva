---
title: "Microsoft Viva - Organizational data"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: pamgreen
ms.date: 09/18/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.custom:
ROBOTS: NOINDEX, NOFOLLOW
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Import Organizational Data in Microsoft Viva and Microsoft 365"
---
# Import and use Organizational Data in Microsoft 365
> *This feature is currently in private preview. This information relates to a feature that may be substantially modified before it's released. Microsoft makes no warranties, expressed or implied, with respect to the information provided here.*

*Organizational Data* refers to employee data that your admin uploads by using the Organizational Data in Microsoft 365 feature. Organizational Data in Microsoft 365 combines this uploaded data with existing Microsoft 365 data to power certain capabilities in Microsoft 365 applications. This feature also helps improve your [Microsoft 365 User Profile](/graph/api/resources/profile?view=graph-rest-beta) data by ingesting Organizational Data that currently resides in your organization's external systems (such as human capital management systems). This helps fill in any gaps related to missing or stale user profile data and enables richer experiences in Microsoft 365 and Microsoft Viva.

*Microsoft 365 User Profile Data* refers to the information associated with a user's account and is stored in the [Microsoft 365 User Profile](). This information includes email address, phone number, job title, and other descriptive information.

Microsoft 365 User Profile Data comes from two main sources: either Microsoft Entra ID (formerly Azure Active Directory), which is the default setting, or from Organization Data in Microsoft 365 through a .csv file that you upload. The properties in the Microsoft Entra schema and in the Microsoft 365 User Profile match the column names in the .csv file and are referred to as *attributes* in Organizational Data in Microsoft 365. 

## Data attributes

When you upload a .csv file, you need to include at least one required attribute, **Microsoft_PersonEmail**, for each employee. To learn how to set up and structure an Organizational Data .csv file, see [Prepare Organizational Data](#prepare-and-import-your-organizational-data).

You can also include the following optional attributes. (The value in parentheses is the corresponding property name in the [Microsoft 365 User Profile](/graph/api/resources/profile?view=graph-rest-beta#relationships) schema.).

For information on how the Organizational Data attributes map to Microsoft 365 User Profile data, see [Attribute reference](#attribute-reference) for more details about the specific attributes, and [Attribute to property mapping](#attribute-to-property-mapping) .

- Names
   - First Name (first)
   - Last Name (last)
   - Display Name (displayName)
- Positions
   - Job Title (jobTitle) 
   - Role (role)
   - Level (level)
   - Layer (layer)
   - Company
      - Display Name (displayName)
      - Department (department)
      - Office Location (officeLocation)
      - Address
         - Post Office Box (postOfficeBox)
         - Street Address (street)
         - City (city)
         - State (state)
         - Country or Region (countryOrRegion)
         - Postal Code (postalCode)


> [!IMPORTANT]
> 1. In the Microsoft 365 User Profile, Organizational Data takes precedence over data from other sources. When a service queries a Microsoft 365 User Profile, if there is both Organizational Data and Microsoft Entra ID data for a single attribute, the Organizational Data value is used.
> 2. Three name related attributes (Microsoft_FirstName, Microsoft_LastName, and Microsoft_DisplayName) are treated as a group in the Microsoft 365 User Profile, so if any one of them has a value in the input .csv file, the other two also need to have values. Otherwise, the specified value isn't stored in the Microsoft 365 User Profile.

 
## Prepare and import your Organizational Data 

Before you upload Organizational Data, you need to do the following:

1. [Download a .csv template](#step-1---download-a-csv-template)
1. [Structure the Organizational Data](#step-2---structure-the-organizational-data)
1. [Upload your Organizational Data](#step-3---import-the-organizational-data-for-the-first-time)
1. [Update your Organizational Data](#step-4---update-or-make-other-changes-to-your-organizational-data)

### Step 1 - Download a .csv template

1. Sign into to the Microsoft 365 admin center as a user with Global Admin permissions.
1. On the **Organizational Data in Microsoft 365** page (under **Setup > Migration and imports**), select **Get started**.
2. Select **Download CSV template**.

> [!NOTE]
> You can also use Organizational Data exported from another system, such as your HR software, as your starting point, as described in [Get an export of organizational data](/viva/insights/advanced/admin/prepare-org-data#step-3---get-an-export-of-organizational-data).

### Step 2 - Structure the Organizational Data
Now that you have your .csv file starting point, add the Organizational Data that you want to use in Microsoft 365. Save the file to SharePoint.

There are three types of attributes you can add in your Organizational Data file: required, reserved optional, and custom. Attributes can be in any order in the file. However, you can't use the names of required and reserved attributes as the names of any new custom attributes.

- **Required** - The only attribute required by default is email address.
- **Reserved** - Attributes are reserved column headers for attributes that are currently used to calculate, filter, and group data.
- **Custom** - Custom attributes are any additional attributes you want to define to use in filtering and grouping data. When you upload these attributes, analysts can use them when building queries. To learn how to upload custom attributes, refer to Upload Organizational Data (first upload).

All dates should be in the MM/DD/YYYY format. All numerical fields need to be in the "number" format and can't contain commas or a dollar sign.

> [!NOTE]
> The maximum number of total attributes allowed in the system is 105, which includes required attributes.

#### Sample Organizational Data file
Here's an example snippet of a valid .csv file:

```
PersonId,EffectiveDate,HireDate,ManagerId,LevelDesignation,Organization,Layer,Area 
Emp1@contoso.com,12/1/2020,1/3/2014,Mgr1@contoso.com,Junior IC,Sales,8,Southeast 
Emp2@contoso.com,11/1/2020,1/3/2014,Mgr1@contoso.com,Junior IC,Sales,8,Southeast 
Emp3@contoso.com,12/1/2020,1/3/2014,Mgr2@contoso.com,Manager,Sales,7,Northeast 
Emp4@contoso.com,10/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest 
Emp5@contoso.com,11/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest 
Emp6@contoso.com,12/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest
```

For more information about attributes, refer to the Attribute reference section.

### Step 3 - Import the Organizational Data for the first time 
After you create a .csv file with your Organizational Data, you're ready to import it. 

1. On the **Import data from SharePoint** page, browse to the SharePoint location where you saved your .csv file.
2. Select the checkbox to confirm that you understand that the data you upload here may be processed by Viva and Microsoft 365, as well as non-Microsoft services that you've granted access to the data through Microsoft Graph. Select **Next**.
3. Review the details for your upload, and then select **Begin validation**.

Your Organizational Data is validated against the requirements for use with Viva and Microsoft 365 services. This can take up to 24 hours. You can check the validation status on the **Organizational data** page in the admin center. When the validation is complete, you'll see a message that your data is in use and managed by Viva and Microsoft 365. 

Each end user's Organizational Data is stored in that end user's mailbox and respects the data residency rules for Exchange Online (as described in [Data Residency for Exchange Online](/microsoft-365/enterprise/m365-dr-workload-exo?view=o365-worldwide)).

### Step 4 - Update or make other changes to your Organizational Data

Only the global admin can update or delete Organizational Data stored in the Microsoft 365 User Profile.

To update an end user's Organizational Data, upload a new .csv file that contains updated attributes. In that file include *only* the users whose Organizational Data you want to update, and be sure to include all the attributes that you want to be part of their Microsoft 365 User Profile. If you include an attribute in the file but leave the value empty for an end user, the current value in the Microsoft 365 User Profile for that attribute will be deleted.

To delete values for end users' Organizational Data attributes, upload a new .csv file for the specific users. In the .csv file, provide the email for each end user whose data you want to delete in the Microsoft_PersonalEmail column, and set the rest of the columns to empty. (For strings, use ", for integers, use -1.) Leave all other attributes unchanged.

When the new Organizational Data is uploaded, the previous data for each affected end user is deleted with seven days.

## Data usage, retention, and management information for Organizational Data
Review the following information to understand how Organizational Data is used, stored, and deleted.

### Data usage
The Organizational Data you upload may be used by Viva, Microsoft 365 services, and non-Microsoft services that have been given access through the Microsoft Graph API. *This data is treated as **publicly available** within the organization, meaning it may be displayed to any end user in the organization. This data might also be used in [cross-tenant collaboration scenarios](https://support.microsoft.com/office/what-is-a-shared-channel-in-microsoft-teams-e70a8c22-fee4-4d6e-986f-9e0781d7d11d), in Microsoft 365 Copilot, and machine learning model training.*

In the Microsoft 365 User Profile, Organizational Data is given precedence over Microsoft Entra ID data. When a service queries a Microsoft 365 User Profile, if there's both Organizational Data *and* Microsoft Entra ID data for a single attribute, the Organizational Data value is returned. For example, a given end user has "Software Engineer" as the jobTitle property in Microsoft Entra ID. The global admin for your organization uses the Organizational Data in Microsoft 365 feature to upload a value of "Senior Software Engineer" for the **Microsoft_JobTitle** attribute for that same end user. After the upload, both values are stored in the end user's Microsoft 365 User Profile. when an experience like [Profile cards in Microsoft 365](https://support.microsoft.com/office/profile-cards-in-microsoft-365-e80f931f-5fc4-4a59-ba6e-c1e35a85b501) queries the Microsoft 365 User Profile to get the **jobTitle** property for that end user, "Senior Software Engineer" is returned (instead of "Software Engineer").

If you prefer to use the value for a Microsoft Entra ID property instead of the Organizational Data, *do not* upload Organization Data for that attribute.

Ensure that the data you upload matches attribute names and descriptions listed in the [Attribute reference](#attribute-reference). Also avoid uploading [sensitive personal data](https://commission.europa.eu/law/law-topic/data-protection/reform/rules-business-and-organisations/legal-grounds-processing-data/sensitive-data/what-personal-data-considered-sensitive_en).

### Data deletion
The standard process for end users to submit deletion requests is described in the Organizational Data in Microsoft 365 section of [Office 365 Data Subject Requests under the GDPR and CCPA](/compliance/regulatory/gdpr-dsr-Office365). Data deletion is completed within 30 days of receipt of the request. 

When a Microsoft 365 license is removed from a tenant or when consent is removed from the Microsoft 365 admin center, all data artifacts are purged within 30 days.

### Data retention
Organizational Data is stored as long as the end user is active and has a valid license and no deletion request has been made by the end user or the global admin.

### Data residency
When you upload Organizational Data, your .csv file is stored in your SharePoint Online site as described in [Data Residency for SharePoint Online](/microsoft-365/enterprise/m365-dr-workload-spo?view=o365-worldwide). However, each end user’s Organizational Data attributes are added to their Microsoft 365 User Profile and stored in the user’s Exchange Online mailbox as described in [Data Residency for Exchange Online](/microsoft-365/enterprise/m365-dr-workload-exo?view=o365-worldwide). 

### Manage data subject requests
A *Data Subject Request* or DSR is a formal request by a data subject (an end user) to a controller to take an action on their personal data. To understand what data subject rights end users have, see [Office 365 Data Subject Requests Under the GDPR and CCPA](/compliance/regulatory/gdpr-dsr-office365). 

Use the following information to fulfill DSRs from end users:

- Access and Export – An end user can access and export Organizational Data uploaded by a global admin and stored in the Microsoft 365 User Profile by using the data export function in the profile card. See [Export data from your profile card](https://support.microsoft.com/office/export-data-from-your-profile-card-d809f83f-c077-4a95-9b6c-4f093305163d). 
- Edit – see [Update or make changes to Organizational Data](#step-4---update-or-make-other-changes-to-your-organizational-data). 
- Delete – see [Update or make changes to Organizational Data](#step-4---update-or-make-other-changes-to-your-organizational-data) and [Data deletion](#data-deletion). 


## Attribute reference   	

|#|Attribute|Description|Data type|Example|
|-|-|-|-|-|
|1|Microsoft_PersonEmail|Unique identifier for the employee record - an employee's email address.|Email|person.name@xyz.com|
|2|Microsoft_ManagerEmail|Unique identifier for an employee’s manager - the employee's manager’s email address.|Email|manager.name@xyz.com|
|3|Microsoft_Organization|The internal organization or department name that an employee belongs to.|String|Financial Planning and Analysis|
|4|Microsoft_LevelDesignation|Level that represents an employee's experience, management level, or seniority within the organization. This is whatever public level designation your company uses.|String|Director|
|5|Microsoft_JobDiscipline|The discipline that an employee belongs to. For more actionable insights, avoid using too few or too many unique Job disciplines. This is the public job discipline.|String|Finance management|
|6|Microsoft_Layer|An employee's position within the organizational hierarchy, expressed as their distance from the top leader of the organization. For example, the CEO is at Layer 0. Avoid using too few or too many unique layers. This is the layer that is publicly available in your company.|Integer|2|
|7|Microsoft_FirstName|First name of the end user.|String|Alexa|
|8|Microsoft_LastName|Last name of the end user.|String|Smith|
|9|Microsoft_DisplayName|Preferred name of employee to display. This is the public display name an employee chooses to list.|String|Alexa Smith|  
|10|Microsoft_JobTitle|The public facing job title of the employee.|String|Software engineer|
|11|Microsoft_CompanyOfficeLocation|An employee’s company office location. This is a location code, like a building number, floor, or room. This shouldn't be an employee's home office or personal address.|String|2N|
|12|Microsoft_CompanyPostOfficeBox|The post office box number. This is the publicly available company office box number.|String|PO Box 12|
|13|Microsoft_CompanyOfficeStreet|The street. This is the publicly available company office street address.|String|NE 12th Street|
|14|Microsoft_CompanyOfficeCity|The city of the company office the user is associated with. This is the publicly available office address city.|String|Redmond|
|15|Microsoft_CompanyOfficeState|The state. This is the publicly available company office state.|String|Washington|
|16|Microsoft_CompanyOfficeCountryOrRegion|The country or region. It's a free-format string value, for example, "United States". This is the publicly available company office country or region.|String|United States|
|17|Microsoft_CompanyOfficePostalCode|The postal code. This is the publicly available company office postal code.|String|98004|
|18|Microsoft_Company|Company name.|String|Contoso|

## Attribute to property mapping
The following table shows how Organizational Data attributes map to properties in the Microsoft 365 User Profile schema.


|#|Attribute (column heading) in .csv file|Property in Microsoft 365 User Profile schema |
|-|-|-|
|1|Microsoft_PersonEmail |N/A <br><br>The email is converted to the Microsoft Entra ID objectId of the end user and is used for internal processing.|
|2|Microsoft_ManagerEmail|positions -> manager -> userId<br><br>The email is converted to the Microsoft Entra ID objectId for the manager and is stored in the Microsoft 365 User Profile.|
|3|Microsoft_Organization|positions -> positionDetail -> companyDetail -> department|
|4|Microsoft_LevelDesignation |positions -> positionDetail -> level |
|5|Microsoft_JobDiscipline |positions -> positionDetail -> role |
|6|Microsoft_Layer|positions -> positionDetail -> layer|
|7|Microsoft_FirstName|names -> first|
|8|Microsoft_LastName|names -> last|
|9|Microsoft_DisplayName|names -> displayName|
|10|Microsoft_JobTitle|positions -> positionDetail -> jobTitle|
|11|Microsoft_CompanyOfficeLocation|positions -> positionDetail -> companyDetail -> officeLocation|
|12|Microsoft_CompanyPostOfficeBox|positions -> positionDetail -> companyDetail -> physicalAddress -> postOfficeBox|
|13|Microsoft_CompanyOfficeStreet|positions -> positionDetail -> companyDetail -> physicalAddress -> street| 
|14|Microsoft_CompanyOfficeCity|positions -> positionDetail -> companyDetail -> physicalAddress -> city|
|15|Microsoft_CompanyOfficeState|positions -> positionDetail -> companyDetail -> physicalAddress -> state|
|16|Microsoft_CompanyOfficeCountryOrRegion|positions -> positionDetail -> companyDetail -> physicalAddress -> countryOrRegion|
|17|Microsoft_CompanyOfficePostalCode|positions -> positionDetail -> companyDetail -> physicalAddress -> postalCode|
|18|Microsoft_Company|positions -> positionDetail -> companyDetail -> displayName|
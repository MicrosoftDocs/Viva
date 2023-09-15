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
description: "Import organizational data in Microsoft Viva and Microsoft 365"
---

# Import and use organizational data in Microsoft 365

*Organizational data* is descriptive information about employees - for example, their names, positions, and company location. The Organizational data in Microsoft 365 feature lets you combine the organizational data that resides in your organization's external systems (such as HCM systems) with existing Microsoft 365 data (such as profile data) to power certain capabilities in applications (like advanced insights in Viva Insights) and to fill in the gaps for any missing or stale information.

Microsoft 365 uses organizational data from two sources: either Microsoft Entra ID (formerly Azure Active Directory), which is the default setting, or from a .csv file that you upload. The properties in the Microsoft Entra schema and the column names in the .csv file are referred to as *attributes* - these make up the descriptive information. 

## Data attributes

When you upload a .csv file, you need to include at least one required attribute, **PersonEmail**, for each employee. To learn how to set up and structure an organizational data .csv file, see [Prepare organizational data](#prepare-and-import-your-organizational-data).

You can also include the following optional attributes. (The value in parenthesis is the corresponding property name in the Microsoft 365 User Profile schema).

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
- ManagerEmail (manager/userId - note that the Microsoft Entra objectId of the manager is stored in the Microsoft 365 User Profile)

Ensure that the data you upload matches the attributes’ names and descriptions listed above. Also avoid uploading sensitive personal data.

> [!IMPORTANT]
> 1. If you choose to include some or all of the optional attributes in your .csv file, the values of the included attributes will take precedence over the values of the same attributes from existing sources (such as Microsoft Entra). 
> 2. Three name related attributes (First Name/Last Name/Display Name) are treated as a group in the Microsoft 365 User Profile, so if any one of them has a value in the input .csv file, the other two also need to have values. Otherwise, the specified value isn't uploaded.

## Data usage
The data you upload is used by Viva, Microsoft 365 services, and non-Microsoft services as approved by your organization’s administrator. This data is treated as **publicly available** within the organization and can be used in [cross-tenant collaboration scenarios](https://support.microsoft.com/office/what-is-a-shared-channel-in-microsoft-teams-e70a8c22-fee4-4d6e-986f-9e0781d7d11d). This data also might be used by Copilot scenarios and machine learning training.  

The uploaded data is sent to and stored in the Microsoft 365 User Profile, which Viva and Microsoft 365 services can query. Non-Microsoft services approved by your organization’s administrator can query the [Microsoft Graph](/viva/insights/personal/overview/privacy-guide-admins#microsoft-graph) API to access the data. Learn how to [manage permissions in Microsoft Graph](/azure/active-directory/manage-apps/manage-application-permissions?pivots=portal).

Organizational data that is manually uploaded by using a .csv file takes precedence over existing data. When Viva, Microsoft 365 services, and approved non-Microsoft services query the Microsoft 365 User Profile, a response generation process determines the value for each property. For the attributes listed, if you manually upload an attribute *and* the attribute has a different value in an existing source (such as Microsoft Entra ID), the value from the .csv file takes precedence -  that's the value that is used in Viva, Microsoft 365 services, and approved non-Microsoft services.

Because of this, if you prefer to use the values in existing sources, do **NOT** upload values for those attributes. 

## Prepare and import your organizational data 

Before you upload organizational data, you need to do the following: 

1. Know what data to include
2.	Download a .csv template
3.	Structure the organizational data
4. Upload your organizational data

### Step 1 - Know what data to include
By default the only required attribute is an email address, but different apps might require different attributes for full functionality. Check the documentation for the specific service to make sure you have the required attributes.

#### Employees to include
At a minimum, include the organizational data for all employees who have Viva licenses. It's even better to include every person in your company, even if you plan to gather data for only a subgroup — that is, a specific target population within the company. 

For example, if the people in Marketing communicate frequently with the people in Product Development, but the app has HR data only about the Marketing organization, you won't be able to create reports to show how much time Marketing is spending with Product Development.

If you can't include every person in your organization, the minimum to include is all people for whom data is being gathered. 

#### Including all licensed employees
It's the admin's responsibility to maintain up-to-date and complete organizational data. In this task, *complete* means two things: data that includes both the right people and the right attributes for those people.

The reason for including all licensed employees in the organization is that, if their organizational data is missing, analysts can't filter by that data when they build a query on the Analysis page. So, employees whose data is missing is excluded from the analyses that analysts perform.

> [!IMPORTANT]
> Make sure the Microsoft 365 admin has assigned licenses to all employees you want to include in reports. Even if you include an employee in your organizational data file, they'll need a license to show up in reports. 

### Step 2 - Download a .csv template
When you're ready to create your organizational data upload, you can download a template to use as a starting point. 

1. On the **Organizational data in Microsoft 365** page (under **Setup > Migration and imports**), select **Get started**.
2. Select **Download CSV template**.

> [!NOTE]
> You can also use organizational data exported from another system, such as your HR software, as your starting point, as described in [Get an export of organizational data](/viva/insights/advanced/admin/prepare-org-data#step-3---get-an-export-of-organizational-data).

### Step 3 - Structure the organizational data
Now that you have your CSV file starting point, add the organizational data that you want to use in Microsoft 365. 

There are three types of attributes you can add in your organizational data file: required, reserved optional, and custom. Attributes can be in any order in the file. However, you can't use the names of required and reserved attributes as the names of any new custom attributes.


- **Required** - The only attribute required by default is email address.
- **Reserved** - Attributes are reserved column headers for attributes that are currently used to calculate, filter, and group data.
- **Custom** - Custom attributes are any additional attributes you want to define to use in filtering and grouping data. When you upload these attributes, analysts can use them when building queries. To learn how to upload custom attributes, refer to Upload organizational data (first upload).

All dates should be in the MM/DD/YYYY format. All numerical fields need to be in the "number" format and can't contain commas or a dollar sign.

> [!NOTE]
> The maximum number of total attributes allowed in the system is 105, which includes required attributes.


#### Sample organizational data file
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

### Step 4 - Import the organizational data 
After you create a .csv file with your organizational data, you're ready to import it. 

1. On the **Import data from SharePoint** page, browse to the location where you saved your CSV file.
2. Select the checkbox to confirm that you understand that the data you upload here may be processed by Viva and Microsoft 365, as well as non-Microsoft services that you've granted access to the data through Microsoft Graph. Select **Next**.
3. Review the details for your upload, and then select **Begin validation**.

   Your organizational data is validated against the requirements for use with Viva and Microsoft 365 services. This can take up to 72 hours. You can check the validation status on the **Organizational data** page in the admin center. When the validation is complete, you'll see a message that your data is in use and managed by Viva and Microsoft 365. 

### Step 5 - Periodically refresh your organizational data

We recommend that you upload employee data at least once a month to keep data fresh and analysis relevant.

To refresh data, import a new CSV file using the same steps. Be aware that new uploads *overwrite existing data*. 

## Attribute reference   	

|Attribute (column Header)|Description|Data type|Example|
|-|-|-|-|
|Microsoft_PersonEmail|Unique identifier for the employee record - an employee's email address.|Email|person.name@xyz.com|
|Microsoft_ManagerEmail|Unique identifier for an employee’s manager - the employee's manager’s email address.|Email|manager.name@xyz.com|
|Microsoft_Organization|The internal organization/department name that an employee belongs to.|String|Financial Planning and Analysis|
|Microsoft_LevelDesignation|Level that represents an employee's experience, management level, or seniority within the organization. This is whatever public level designation your company uses.|String|Director|
|Microsoft_JobDiscipline|The discipline that an employee belongs to. For more actionable insights, avoid using too few or too many unique Job disciplines. This is the public job discipline.|String|Finance management|
|Microsoft_Layer|An employee's position within the organizational hierarchy, expressed as their distance from the top leader of the organization. For example, the CEO is at Layer 0. Avoid using too few or too many unique layers. This is the layer that is publicly available in your company.|Integer|2|
|Microsoft_FirstName|First name of the user.|String|Alexa|
|Microsoft_LastName|Last name of the user.|String|Smith|
|Microsoft_DisplayName|Preferred name of employee to display. This is the public display name an employee chooses to list.|String|Alexa Smith|  
|Microsoft_JobTitle|The public facing job title of the employee.|String|Software engineer|
|Microsoft_CompanyOfficeLocation|An employee’s company office location. This is a location code, like a building number, floor, room etc. This shouldn't be an employee's home office or personal address.|String|2N|
|Microsoft_CompanyPostOfficeBox|The post office box number. This is the publicly available company office box number.|String|PO Box 12|
|Microsoft_CompanyOfficeStreet|The street. This is the publicly available company office street address.|String|NE 12th Street|
|Microsoft_CompanyOfficeCity|The city of the company office the user is associated with. This is the publicly available office address city.|String|Redmond|
|Microsoft_CompanyOfficeState|The state. This is the publicly available company office state.|String|Washington|
|Microsoft_CompanyOfficeCountryOrRegion|The country or region. It's a free-format string value, for example, "United States". This is the publicly available company office country or region.|String|United States|
|Microsoft_CompanyOfficePostalCode|The postal code. This is the publicly available company office postal code.|String|98004|
|Microsoft_Company|Company name.|String|Contoso|

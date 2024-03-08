---
title: "Organizational Data in Microsoft 365"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: elizapo
ms.date: 11/30/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-suite
ms.localizationpriority: medium
ms.custom:
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

*Organizational data* refers to employee data that your admin uploads by using the Organizational Data in Microsoft 365 feature. Organizational Data in Microsoft 365 combines this uploaded data with existing Microsoft 365 data to power certain capabilities in Microsoft 365 applications. This feature also helps improve your [Microsoft 365 User Profile](/graph/api/resources/profile?view=graph-rest-beta&preserve-view=true) data by ingesting organizational data that currently resides in your organization's external systems (such as human capital management systems). This helps fill in any gaps related to missing or stale user profile data and enables richer experiences in Microsoft 365 and Microsoft Viva.

*Microsoft 365 User Profile Data* refers to the information associated with a user's account and is stored in the Microsoft 365 User Profile. This information includes email address, phone number, job title, and other descriptive information.

Microsoft 365 User Profile Data comes from two main sources: either Microsoft Entra ID (formerly Azure Active Directory), which is the default setting, or from Organization Data in Microsoft 365 through a .csv file that you upload. The properties in the Microsoft Entra schema and in the Microsoft 365 User Profile match the column names in the .csv file and are referred to as *attributes* in Organizational Data in Microsoft 365. 

## Data attributes

When you upload a .csv file, you need to include at least one required attribute, **Microsoft_PersonEmail**, for each employee. To learn how to set up and structure an organizational data .csv file, see [Prepare and import your organizational data](#prepare-and-import-your-organizational-data).

You can also include the following optional attributes. (The value in parentheses is the corresponding property name in the [Microsoft 365 User Profile](/graph/api/resources/profile?view=graph-rest-beta&preserve-view=true#relationships) schema.).

See [Attribute reference](#attribute-reference) for more details about the specific attributes, and [Attribute to property mapping](#attribute-to-property-mapping) for information on how the Organizational Data in Microsoft 365 attributes map to Microsoft 365 User Profile data.

- Names 
   - **Microsoft_FirstName** (first) 
   - **Microsoft_LastName** (last) 
   - **Microsoft_DisplayName** (displayName) 
- Positions  
   - Detail 
      - **Microsoft_JobTitle** (jobTitle) 
      - **Microsoft_JobDiscipline** (role) 
      - **Microsoft_LevelDesignation** (level) 
      - **Microsoft_Layer** (layer) 
         - Company 
            - **Microsoft_Company** (displayName) 
            - **Microsoft_Organization** (department) 
            - **Microsoft_CompanyOfficeLocation** (officeLocation) 
               - Address 
                  - **Microsoft_CompanyPostOfficeBox** (postOfficeBox) 
                  - **Microsoft_CompanyOfficeStreet** (street) 
                  - **Microsoft_CompanyOfficeCity** (city) 
                  - **Microsoft_CompanyOfficeState** (state) 
                  - **Microsoft_CompanyOfficeCountryOrRegion** (countryOrRegion) 
                  - **Microsoft_CompanyOfficePostalCode** (postalCode) 
- Manager 
   - **Microsoft_ManagerEmail** (userId) 

> [!IMPORTANT]
> 1. In the Microsoft 365 User Profile, Microsoft Entra data takes precedence over Organizational Data in Microsoft 365. When a service queries a Microsoft 365 User Profile, if there is both organizational data and Microsoft Entra data for a single attribute, the Microsoft Entra value is used.
> 2. Three name related attributes (**Microsoft_FirstName**, **Microsoft_LastName**, and **Microsoft_DisplayName**) are treated as a group in the Microsoft 365 User Profile, so if any one of them has a value in the input .csv file, the other two also need to have values. Otherwise, the specified value isn't stored in the Microsoft 365 User Profile.

 
## Prepare and import your organizational data 

Before you upload organizational data, you need to do the following:

1. [Download a .csv template](#step-1---download-a-csv-template)
1. [Structure the organizational data](#step-2---structure-the-organizational-data)
1. [Import your organizational data for the first time](#step-3---import-your-organizational-data-for-the-first-time)
1. [Update or make other changes to your data](#step-4---update-or-make-other-changes-to-your-data)

### Step 1 - Download a .csv template

1. Sign into to the Microsoft 365 admin center as a user with Global Admin permissions.
1. On the **Organizational Data in Microsoft 365** page (under **Setup > Migration and imports**), select **Get started**.
2. Select **Download CSV template**.

> [!NOTE]
> You can also use organizational data exported from another system, such as your HR software, as your starting point, as described in [Get an export of organizational data](/viva/insights/advanced/admin/prepare-org-data#step-3---get-an-export-of-organizational-data).

### Step 2 - Structure the organizational data
Now that you have your .csv file starting point, add the organizational data that you want to use in Microsoft 365. Save the file to SharePoint.

There are three types of attributes you can add in your organizational data file: required, reserved optional, and custom. Attributes can be in any order in the file. However, you can't use the names of required and reserved attributes as the names of any new custom attributes.

- **Required** - The only attribute required by default is email address.
- **Reserved** - Attributes are reserved column headers for attributes that are currently used to calculate, filter, and group data.
- **Custom** - Custom attributes are any other attributes you want to define to use in filtering and grouping data. When you upload these attributes, analysts can use them when building queries. To learn how to upload custom attributes, see [Upload Organizational Data (first upload)](./insights/advanced/admin/upload-org-data-first.md).

Use the MM/DD/YYYY format for all dates. All numerical fields need to be in the "number" format and can't contain commas or a dollar sign.

> [!NOTE]
> The maximum number of total attributes allowed in the system is 105, which includes required attributes.

#### Sample data file
Here's an example snippet of a valid .csv file:

```
Microsoft_PersonEmail,Microsoft_ManagerEmail,Microsoft_LevelDesignation,Microsoft_Organization,Microsoft_Layer,Microsoft_CompanyOfficeCity
Emp1@contoso.com,Mgr1@contoso.com,Junior IC,Sales,8,Seattle
Emp2@contoso.com,Mgr1@contoso.com,Junior IC,Sales,8,Seattle
Emp3@contoso.com,Mgr2@contoso.com,Manager,Sales,7,Seattle
Emp4@contoso.com,Mgr3@contoso.com,Support,Sales,9,New York
Emp5@contoso.com,Mgr3@contoso.com,Support,Sales,9,New York
Emp6@contoso.com,Mgr3@contoso.com,Support,Sales,9,New York

```

For more information about attributes, see the [Attribute reference](#attribute-reference).

### Step 3 - Import your organizational data for the first time 
After you create a .csv file with your data, the next steps are to save the data to SharePoint and then import it into Viva.

#### Upload the .csv file to SharePoint
Use the following steps to upload your data to SharePoint. Make sure that your SharePoint site has the right permissions and that only those that should be able to access the data can access the site.

1. Open the SharePoint site library.
2. Select **Upload**, and then select **Files**.
   :::image type="content" source="media/sharepoint-library.png" alt-text="A screenshot shows the Upload menu in SharePoint.":::
3. Navigate to the location where you saved the .csv file, and then select **Open**.

You can also use drag and drop to upload the file.

Before you import the data into Viva, you need the path to the file on SharePoint, in this format: https://*domain*.sharepoint.com/sites/*sitename*/Documents/*foldername*/*filename*.csv. Use the following steps to get the path to your file.

1. Select the ellipses (...) next to the file and then select **Details**.
   :::image type="content" source="media/sharepoint-path-ellipses.png" alt-text="A screenshot shows the ellipses option next to a file in a SharePoint library. "::: 
1. Find the **Path** value, and then select the copy icon. 
   :::image type="content" source="media/sharepoint-path-icon.svg" alt-text="A screenshot shows the Path information for a file in SharePoint.":::
   
   
> [!NOTE]
> Be sure to follow these steps to get the path to the file. This is a different path than what's visible in the URL field of a browser when you view the .csv file in SharePoint.

#### Import the data into Microsoft 365
Now you're ready to import the data. 

1. Sign into to the Microsoft 365 admin center as a user with Global Admin permissions.
1. On the **Organizational Data in Microsoft 365** page (under **Setup > Migration and imports**), select **Get started**.
3. On the **Import data from SharePoint** page, enter the SharePoint location where you saved your .csv file. (If you copied the location at the end of the upload step, paste it here.) 
1. Confirm that you understand that the data you upload here may be processed by Viva and Microsoft 365, as well as non-Microsoft services that you've granted access to the data through Microsoft Graph. Select **Next**.
1. Review the details for your upload, and then select **Begin validation**.

Your organizational data is validated against the requirements for use with Viva and Microsoft 365 services. This can take up to 24 hours. You can check the validation status on the **Organizational data** page in the admin center. When the validation is complete, you'll see a message that your data is in use and managed by Viva and Microsoft 365. 

Each end user's organizational data is stored in that end user's mailbox and respects the data residency rules for Exchange Online (as described in [Data Residency for Exchange Online](/microsoft-365/enterprise/m365-dr-workload-exo?view=o365-worldwide&preserve-view=true)).

### Step 4 - Update or make other changes to your data

Only the global admin can update or delete organizational data stored in the Microsoft 365 User Profile.

To update or delete an end user's organizational data, create and upload a new .csv file containing only the users whose data you want to update or delete. 

- To update a value, include all of the attributes that you want to update. Provide a different value for any attribute that you want to change. If you include an attribute but don't provide a value (but do **not** set it to an empty string), the current value in the Microsoft 365 User Profile is used (it isn't updated).
- To delete a value, set the value for the attribute to an empty string by using two single quotes (''). (Set the **Microsoft_Layer** attribute "-1".) To delete all of the data for a user, enter the empty string or integer value for all of their attributes.


> [!NOTE]
> If you use Excel to edit the .csv file, use three single quotes (''') instead of two ('')- Excel sees a single quote (') as the escape character.

After the new organizational data is uploaded, the previous data for each affected end user is deleted with 30 days.

## Data usage, retention, and management information for Organizational Data in Microsoft 365
Review the following information to understand how organizational data is used, stored, and deleted.

### Data uploaded from Viva Insights
If your global admin consents to sharing data from Viva Insights with the Organizational Data in Microsoft 365 feature, the following data is shared:

- PersonId
- ManagerId
- Organization
- LevelDesignation
- FunctionType
- Layer
- Location
- RoleStart Data

The following data is uploaded from the Organizational Data feature but isn't available for use in Insights:
- Microsoft_FirstName
- Microsoft_LastName
- Microsoft_DisplayName
- Microsoft_JobTitle
- Microsoft_RoleEndDate
- Microsoft_City
- Microsoft_CountryOrRegion
- Microsoft_PostalCode
- Microsoft_PostOfficeBox

### Data usage
The organizational data you upload may be used by Viva, Microsoft 365 services, and non-Microsoft services that have been given access through the Microsoft Graph API. *This data is treated as **publicly available** within the organization, meaning it may be displayed to any end user in the organization. This data might also be used in [cross-tenant collaboration scenarios](https://support.microsoft.com/office/what-is-a-shared-channel-in-microsoft-teams-e70a8c22-fee4-4d6e-986f-9e0781d7d11d), in Microsoft 365 Copilot, and machine learning model training.*

In the Microsoft 365 User Profile, Microsoft Entra data is given precedence over Organizational Data in Microsoft 365 by default. When a service queries a Microsoft 365 User Profile, if there's both organizational data *and* Microsoft Entra data for a single attribute, the Microsoft Entra value is returned. For example, a given end user has "Software Engineer" as the jobTitle property in Microsoft Entra ID. The global admin for your organization uses the Organizational Data in Microsoft 365 feature to upload a value of "Senior Software Engineer" for the **Microsoft_JobTitle** attribute for that same end user. After the upload, both values are stored in the end user's Microsoft 365 User Profile. When an experience like [Profile cards in Microsoft 365](https://support.microsoft.com/office/profile-cards-in-microsoft-365-e80f931f-5fc4-4a59-ba6e-c1e35a85b501) queries the Microsoft 365 User Profile to get the **jobTitle** property for that end user, "Software Engineer" is returned (instead of "Senior Software Engineer").

If you prefer to use the value from your organizational data in the Microsoft 365 User Profile, contact Microsoft by sending a request to orgdatainm365support@microsoft.com. Include the subject line, "Request to give organizational data precedence over Microsoft Entra data in Microsoft 365 User Profile for Tenant [Name] [Tenant ID]." It can take up to four days for this change to take effect. 

If you later want to switch back to the default behavior (where Microsoft Entra data is given precedence), contact Microsoft again, using a subject line of, "Request to give Microsoft Entra data precedence over Organizational Data in Microsoft 365 User Profile for Tenant [Name] [Tenant ID]." This change also takes up to four days.

To ensure that the data in the Microsoft 365 User Profile remains up to date and accurate, we recommend that you upload refreshed organizational data regularly (for example, weekly). This prevents the data in the user profile from becoming stale when compared to the data in your organization's human capital management systems.

Ensure that the data you upload matches attribute names and descriptions listed in the [Attribute reference](#attribute-reference). Also avoid uploading [sensitive personal data](https://commission.europa.eu/law/law-topic/data-protection/reform/rules-business-and-organisations/legal-grounds-processing-data/sensitive-data/what-personal-data-considered-sensitive_en).

### Data deletion
See [Update or make other changes to organizational data](#step-4---update-or-make-other-changes-to-your-data) for information about deleting user data. After the update is processed, the associated user data is deleted within 30 days.

When a Microsoft 365 license is removed from a tenant or when consent is removed from the Microsoft 365 admin center, all data artifacts are purged within 30 days.

### Data retention
Organizational data is stored as long as the end user is active and has a valid license and no deletion request has been made by the end user or the global admin.

### Data residency
When you upload organizational data, your .csv file is stored in your SharePoint Online site, and each end user's organizational data attributes are coped to their Microsoft 365 User Profile and stored in the user's Exchange Online mailbox. For data residency information for SharePoint Online and Exchange Online, see [Data Residency for SharePoint Online](/microsoft-365/enterprise/m365-dr-workload-spo?view=o365-worldwide&preserve-view=true) and [Data Residency for Exchange Online](/microsoft-365/enterprise/m365-dr-workload-exo?view=o365-worldwide&preserve-view=true). 

### Manage data subject requests
A *Data Subject Request* or DSR is a formal request by a data subject (an end user) to a controller to take an action on their personal data. To understand what data subject rights end users have, see [Office 365 Data Subject Requests Under the GDPR and CCPA](/compliance/regulatory/gdpr-dsr-office365). 

Use the following information to fulfill DSRs from end users:

- Access and Export – An end user can access and export organizational data uploaded by a global admin and stored in the Microsoft 365 User Profile by using the data export function in the profile card. See [Export data from your profile card](https://support.microsoft.com/office/export-data-from-your-profile-card-d809f83f-c077-4a95-9b6c-4f093305163d). 
- Edit – see [Update or make other changes to organizational data](#step-4---update-or-make-other-changes-to-your-data). 
- Delete – see [Update or make other changes to organizational data](#step-4---update-or-make-other-changes-to-your-data) and [Data deletion](#data-deletion). 


## Attribute reference   	
The following table provides more details about the Organizational Data in Microsoft 365 attributes.

>[!NOTE]
> Be aware that *Microsoft_LevelDesignation* and *Microsoft_Layer* attributes don't have corresponding properties in Microsoft Entra. Because of this, the only way to add these values to a Microsoft 365 User Profile is by using the Organizational Data in Microsoft 365 feature.

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
The following table shows how Organizational Data in Microsoft 365 attributes map to properties in the Microsoft 365 User Profile schema.


|#|Attribute (column heading) in .csv file|Property in Microsoft 365 User Profile schema |
|-|-|-|
|1|Microsoft_PersonEmail |N/A <br><br>The email is converted to the Microsoft Entra objectId of the end user and is used for internal processing.|
|2|Microsoft_ManagerEmail|positions -> manager -> userId<br><br>The email is converted to the Microsoft Entra objectId for the manager and is stored in the Microsoft 365 User Profile.|
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

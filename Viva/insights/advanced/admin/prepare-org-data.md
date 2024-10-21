---
ms.date: 09/09/2024
title: Prepare organizational data in Viva Insights
description: Learn how to prepare and structure your data for upload into the Viva Insights advanced insights app. 
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Prepare an organizational data file upload

The advanced insights app can get organizational data in one of two ways: through Microsoft Entra ID, which is the default setting, or through an organizational data file that you as an admin upload. In this article, we discuss the second option, the organizational data file. Read on to find out what you as an admin need to do to identify, gather, and structure data before uploading organizational data.

To learn about organizational data in general, find out which data Microsoft Entra ID automatically syncs with Viva Insights, and to get an overview of the **Organizational data** page in the advanced insights admin experience, refer to [Organizational data in Viva Insights](org-data-overview.md).

>[!Important]
> After you upload a .csv file with organizational data, you won't be able to switch back to using Microsoft Entra ID. You'll need to regularly upload .csv files to keep your organizational data current.

## Prepare organizational data

When you’re ready to start working with an organizational data file, the following sections guide you through the data-preparation process:

1. [Identify trends that you want to analyze](#step-1---identify-trends-that-you-want-to-analyze) – Decide which trends you need to learn about to improve efficiency at work. After identifying these trends, you can better choose what organizational data to use.
1. [Know what data to include](#step-2---know-what-data-to-include) – A few data attributes are required, and many are optional. Among the optional ones, choose attributes that best serve your analytical purposes.
1. [Get an export of organizational data](#step-3---get-an-export-of-organizational-data) – Have an admin export the HR data from your organization’s HR system. Optionally, include line-of-business data, if your analysis requires it.
1. [Structure the organizational data](#step-4---structure-the-organizational-data) – For your data to validate successfully, you need to first structure it correctly in the .csv file that you upload.
1. [Upload the organizational data file](#step-5---upload-the-organizational-data-file) – After your .csv file is ready, you upload it to the advanced insights app where, after validation and processing, it becomes available for analysis.

### Step 1 - Identify trends that you want to analyze

To know what organizational data to extract, you first need to decide what workplace trends you want to learn about. For example, in an upcoming analysis, you may want to examine collaboration across different employee segments, or groups. You need to first define these groups, which you can do in various ways:

* By organizational data
* By organizational hierarchy levels
* By performance, engagement, or other line-of-business data

Defined groups can be used in the following examples of analyses:

#### Collaboration between groups

A common analysis scenario is to find patterns of collaboration between different groups of employees. For example, you might want to know how much your product marketing team is talking to your sales team.

Attributes for segmenting populations can be helpful to consider in defining patterns of collaboration, such as:

* Job family or role attributes, like profession, function, discipline, and job code
* Organization, line of business, or cost center, like HR, Finance, Sales, and Marketing
* Location attributes, like city, state, country, and regions, as defined by your organization
* Attributes that describe their work, like remote, full-time employee, or vendor

Most of these attributes are available within HR information systems.

#### Hierarchical collaboration

It’s also common to seek patterns of collaboration behavior in reference to the hierarchy of your organization. You might also quantify collaboration between managers and individual contributors, and between higher and lower levels in the organization.

The following concepts are helpful in this kind of analysis:

* **IC or manager** – Whether an employee is an individual contributor or a manager.
* **Organizational hierarchy** – For example, the names of all managers above the employee in that employee's reporting structure; each manager can be stored as a separate attribute.
* **Layer** – For example, the position of the employee in the organizational hierarchy where layer 0 = the top leader in the company.
* **Span** – For example, the number of direct reports assigned to an employee.
* **Level** – For example, senior manager, VP, director, CVP.

Most of these attributes are also found in HR information systems.

#### Collaboration, engagement, and outcome data

Finally, you might want to consider tying collaboration behavior patterns to employee engagement scores or other performance outcome data. This data might include sales-quota attainment or performance ratings. This data is often found outside of traditional HR information systems, either in separate HR data repositories or in line-of-business systems.

### Step 2 - Know what data to include

To get full functionality from the advanced insights app, you need to supply several required attributes, as described in [Attribute reference](#attribute-reference). Additionally, you can supply up to 100 optional attributes to group and filter data in interesting and custom ways.

Examples of organizational data include job family, job role, organization, and line of business. This data is supplied to the advanced insights app at the individual level, which means that these attributes provide context to each person in the dataset.

#### Employees to include

At a minimum, include the organizational data for all employees who have Viva Insights licenses. It's even better to include every person in your company as part of your data upload, even if you plan to gather collaboration data for only a subgroup—that is, a specific target population within the company.

For example, if the people in Marketing communicate frequently with the people in Product Development, but the app has HR data only about the Marketing organization, you can't create reports to show how much time Marketing is spending with Product Development.

If you can't include every person in your organization, the minimum to include is all people for whom collaboration data is being gathered. This minimum enables you to analyze collaboration patterns between groups within this population, but not between groups outside this population.

##### Including all licensed employees

It's the admin's responsibility to maintain up-to-date and complete organizational data. In this task, "complete" means two things: data that includes the right people and includes the right attributes for those people.

The reason for including all licensed employees in the organization is that, if their organizational data is missing, analysts can't filter by that data when they build a query on the **Analysis** page. So, employees whose data is missing is excluded from the analyses that analysts perform.

>[!Important]
>Make sure the Microsoft 365 admin has assigned licenses to all employees you want to include in reports. Even if you include an employee in your organizational data file, they'll need a license to show up in reports. For more information about licensing and reports, see [When users show up in query results](../setup-maint/assign-licenses.md#when-users-show-up-in-query-results).


##### Notification of missing data

If the app detects that data is missing for one or more licensed employees, it alerts admins through a pop-up notification in the top-right corner of the **Data connections** tab.

###### Upload missing organizational data

To upload this missing data, the admin can follow these steps:

1. On the pop-up notification, select **Download** to download a .csv file that contains the names of licensed employees whose organizational data is missing. 
1. Open the .csv file.
1. Append the missing data for these employees. This means adding attributes (columns) that describe the employees in a way consistent with previous uploads.
1. Upload the file. Refer to [Upload organizational data (subsequent upload)](./upload-org-data-subsequent.md) for more information.

In addition to including all licensed employees in the upload of organizational data, we recommend that you also include unlicensed employees, as we explained [earlier](#including-all-licensed-employees).

### Step 3 - Get an export of organizational data

Before you format and upload organizational data, you need to get it from one or more sources. Your primary source is the team that manages your organization's HR information systems. This team needs to provide you with a data export of HR attributes for individual employees.

In addition, your analysts might need data about business outcomes. If so, you need to contact line-of-business owners who have access to data stores that contain this information. For example, this data might include:

* Performance-review data for specific work groups.
* Employee engagement scores captured by HR outside of HR information systems.
* Sales or other quota-attainment data that provide more views into performance.
* Employee survey data.

After you get this data, you'll need to structure it for successful processing after uploading it to the app.

### Step 4 - Structure the organizational data

After you get your exported data, structure it into the correct format.

#### Add required, reserved optional, and custom attributes

There are three types of attributes you can add in your organizational data file: required, reserved optional, and custom.

##### Required

Supply the following attributes as column headers, exactly as written below, in the .csv upload.

* **EffectiveDate**
    * Make sure the **EffectiveDate** column has values in all rows. If you don’t provide an **EffectiveDate** column in your upload, the date you uploaded the data becomes the default **EffectiveDate**.
* **PersonId**
* **ManagerId**
* **Organization** (case sensitive)

##### Reserved optional

The following attributes are reserved column headers for attributes that are currently used to calculate, filter, and group data. Different attributes from the list below may be needed depending on the particular Power BI template.

* **LevelDesignation**
* **FunctionType**
* **HireDate**
* **HourlyRate**
* **Layer**
* **SupervisorIndicator**
* **WeeklyBadgeOnsiteDays**
* **Location**

>[!Note]
>Attributes can be in any order in the file. However, the names of these required and reserved attributes can't be used as the names of any new custom attributes.

#### Custom attributes

Custom attributes are any other attributes you want to define to use in filtering and grouping data. When you upload these attributes, analysts can use them when building queries. To learn how to upload custom attributes, refer to [Upload organizational data (first upload)](upload-org-data-first.md). 

> [!Note] 
>
> * The maximum number of total attributes allowed in the system is 105, which includes the five required attributes. 
> * All numerical fields (such as the required attribute "HourlyRate") need to be in the "number" format and cannot contain commas or a dollar sign.

>[!Tip]
>Go to our [File rules and validation errors](rules-validation-errors.md) article for more information about formatting your file.

#### Example .csv export file

Here's an example snippet of a valid .csv export file:

``PersonId,EffectiveDate,HireDate,ManagerId,LevelDesignation,Organization,Layer,Area Emp1@contoso.com,12/1/2020,1/3/2014,Mgr1@contoso.com,Junior IC,Sales,8,Southeast Emp2@contoso.com,11/1/2020,1/3/2014,Mgr1@contoso.com,Junior IC,Sales,8,Southeast Emp3@contoso.com,12/1/2020,1/3/2014,Mgr2@contoso.com,Manager,Sales,7,Northeast Emp4@contoso.com,10/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest Emp5@contoso.com,11/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest Emp6@contoso.com,12/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest``

For more information about attributes, see [Attribute reference](#attribute-reference) section.

### Step 5 - Upload the organizational data file

After you create a source .csv file, you can upload it to the advanced insights app through the **Organizational data page > Data hub** or **Data connections** tab.

If this is the first time you upload organizational data, refer to [Upload organizational data (first upload)](upload-org-data-first.md). If this isn't the first time, refer to [Upload organizational data (subsequent uploads)](./upload-org-data-subsequent.md). 

After your data successfully uploads, the app performs more validation and processing to complete provisioning.

#### How often to upload an organizational data .csv file

It's recommended that you upload employee data at least once a month to keep data fresh and analysis relevant. Soon after an employee data upload has succeeded, the updated data becomes available for users to see as insights in the app.

##### Supplying data over a time period


By default, Viva Insights includes meeting and email data for measured employees for one year. Organizational data is provided to Viva Insights with an effective date associated with each row in the upload file.

If you do a point-in-time export of organizational data from your HR information system as of the current date, you get a picture of your employee population for that single point in time. For the greatest data fidelity during provisioning, you should provide organizational data exports for each of the last 13 months. This data can be supplied in a single file or in a sequence of files. 

Here's how that would look in practice. For each measured employee, you'd have 13 separate rows. Each of those rows would contain an effective date for each month that data was pulled for. If an effective date for each month isn't possible, then you can provide one single point in time. In that case, set the effective date to the first day of the current month, one year back. For example, if provisioning occurred in October 2020, the effective date for all rows should be set to 10/1/2019.

Employee collaboration activity is mapped to the most recent organizational data snapshot (based on **EffectiveDate**) that precedes the date of the collaboration activity. 

## Advanced configuration - Configure email address to find corresponding EntraID for processing

Viva Insights uses email addresses to find the corresponding EntraID for processing. With this advanced configuration, you can choose the date that Viva Insights should use to get the EntraID for each email address.

### Option 1: EffectiveDate

*Applies if: Your data source tracks email address changes by EffectiveDate*

EffectiveDate is the date that a given attribute value applies for an employee. The attribute applies until another record for the same attribute with a different EffectiveDate is specified. If no EffectiveDate is uploaded, the date of upload is used as the default.

#### Scenario

1.	Your data source tracks email address changes by EffectiveDate.
2.	The email address changed from BoSmith@contoso.com to BoJames@contoso.com for EntraID “A”.  This change is recorded in the HCM system using EffectiveDate.

**Example:**

1.	04/14/2024: The email address changed from BoSmith@contoso.com to BoJames@contoso.com for EntraID “A”. This change is recorded in the HCM source system with a new row for BoJames@contoso.com with the EffectiveDate 04/14/2024.
2.	This is snapshot exported from the HCM source system on 04/15/2024:

    | PersonId | EffectiveDate | Organization |
    |----|----|----|
    | BoSmith@contoso.com | 04/01/2024 | ABC |
    | BoJames@contoso.com | 04/14/2024 | ABC |

3. 04/16/2024: The file exported on the snapshot date is uploaded in Viva Insights
    * Select EffectiveDate under **Advanced configuration**
    * This ensures that the email address changes are tracked by the corresponding EffectiveDate provided in the uploaded file.
        * From 04/01/2024 to 04/14/2024, BoSmith@contoso.com is used to fetch EntraID “A”
        * From 04/14/2024, BoJames@contoso.com is used to fetch EntraID “A”

         [Learn more about how to use EffectiveDate to supply data over a time period](#supplying-data-over-a-time-period).

### Option 2: Select date

*Applies if: Your data source doesn’t track email address changes. The email address on the selected date is used for all past dates.*

1.	Select today’s date if you exported data from it recently.
2.	Otherwise, select an older date.

#### Scenario 1

1.	Your data source doesn’t track email address changes and you exported data from it recently.
2.	The email address changed for EntraID "A" and you want the new email address to match to "A" for the entire historical data.

**Example:**

1.	04/14/2024: The email address changed from BoSmith@contoso.com to BoJames@contoso.com for EntraID "A".
2.	The snapshot exported from the HCM source system on 04/15/2024:

    | PersonId | EffectiveDate | Organization |
    |---|---|---|
    | BoJames@contoso.com | 04/01/2024 | ABC | 

3. 04/16/2024: The file exported on the snapshot date is uploaded in Viva Insights.

4. Select **04/16/2024** from the dropdown
    * This ensures that the email address on 04/16/2024 (for example, BoJames@contoso.com) is used to fetch EntraID "A" for all past dates.

#### Scenario 2

1.	Your data source doesn’t track email address changes and you didn't recently export any data.
2.	The email address changed for EntraID "A" and you want the old email address to match to "A" for the entire historical data.

**Example:**

1. The snapshot exported from the HCM source system on 04/20/2024:

    | PersonId | EffectiveDate | Organization |
    |----|----|----|
    | BoSmith@contoso.com | 04/01/2024 | ABC |

2.	04/25/2024: The email address changed from BoSmith@contoso.com to BoJames@contoso.com  for EntraID "A".

3.	05/10/2024: The file exported on the snapshot date is uploaded in Viva Insights.
    * Select **04/20/2024** from the dropdown and not **04/25/2024** or **05/10/2024**. 
    * This ensures that the email address on 04/20/2024 (for example, BoSmith@constoso.com) is used to fetch EntraID "A" for all past dates.


## Attribute reference

This section contains information about the attributes that you use in the organizational data files uploaded to the advanced insights app.

>[!Note]
>If you share data from Viva Insights with the Organizational Data in Microsoft 365 feature, some of the attributes listed below are shared. Any attribute, however, that contains **Microsoft_** will not be available in Viva Insights. [Learn more about Organizational Data in Microsoft 365](/viva/organizational-data#data-uploaded-from-viva-insights).

>[!Note]
>The “OnsiteDays” field is now “WeeklyBadgeOnsiteDays.” See the table below to learn more.

| Viva Insights mapped field | Description | Data type | Example value| Required or reserved
|--------------------------|----------|---|--------------------|----|
|**PersonId**| Unique identifier for an employee record. It can be the employee's primary SMTP address or email alias.  | Email | `joe@contoso.com`| Required<sup>1</sup>
|**ManagerId** | Unique identifier for an employee’s manager. It can be the manager’s primary SMTP address or email alias. For CEOs, this can be left blank. | Email| `sally@contoso.com`| Required |
|**Organization**| The internal organization that an employee belongs to. For more actionable insights, avoid using too few or too many unique Organizations.| String| `Financial Planning and Analysis` |Required|
|**EffectiveDate**| <li>Date that a given attribute value applies for an employee. The attribute applies until another record for the same attribute with a different EffectiveDate is specified. If no EffectiveDate is uploaded, the date of upload is used as default.<li>Admin can select DataType as either DateTime_MM/DD/YYYY or DateTime_DD/MM/YYYY.<li>If selected Datatype is DateTime_MM/DD/YYYY, it supports MM/DD/YYYY, MM/DD/YYYY followed by more text such as "time," MM-DD-YYYY, MM-DD-YY, or YYYY-MM-DD.<li>If selected Datatype is DateTime_DD/MM/YYYY, it supports DD/MM/YYYY, DD/MM/YYYY followed by more text such as "time," D/MM/YYYY, D/MM/YY, DD-MM-YYYY, DD-MM-YY, or YYYY-DD-MM.<li>If selected Datatype is DateTime_MM/DD/YYYY or DateTime_DD/MM/YYYY, it supports Wednesday, March 14, 2012; March 14, 2012; 14-Mar-2012; or 14-Mar-12. | DateTime| `12/31/2021`|Required<sup>2</sup>|
|**LevelDesignation** | Level that represents an employee’s experience, management level, or seniority within the organization. For more actionable insights, avoid using too few or too many unique LevelDesignation values.| String | `Director` |Reserved<sup>3</sup>
|**FunctionType**| The job function that an employee performs. For more actionable insights, avoid using too few or too many unique FunctionTypes| String | `Finance Management` | Reserved|
|**HireDate**| <li>The date an employee began employment. If an employee has multiple hire dates, it’s best to use the most recent hire date.<li>Admin can select DataType as either DateTime_MM/DD/YYYY or DateTime_DD/MM/YYYY.<li>If selected Datatype is DateTime_MM/DD/YYYY, it supports MM/DD/YYYY, MM/DD/YYYY followed by more text such as "time," MM-DD-YYYY, MM-DD-YY, or YYYY-MM-DD.<li>If selected Datatype is DateTime_DD/MM/YYYY, it supports DD/MM/YYYY, DD/MM/YYYY followed by more text such as "time," D/MM/YYYY, D/MM/YY, DD-MM-YYYY, DD-MM-YY, or YYYY-DD-MM.<li>If selected Datatype is DateTime_MM/DD/YYYY or DateTime_DD/MM/YYYY, it supports Wednesday, March 14, 2012; March 14, 2012; 14-Mar-2012; or 14-Mar-12.| DateTime| `12/31/2021`| Reserved|
|**HourlyRate**| An employee’s salary represented as an hourly rate in US dollars. | Double | `25.25` | Reserved|
|**Layer**| An employee’s position within the organizational hierarchy, expressed as their distance from the top leader of the organization. For example, the CEO is at Layer 0. For more actionable insights, avoid using too few or too many unique Layers. | Integer | `2` |Reserved
|**SupervisorIndicator**| The manager status of an employee as **IC** (individual contributor), **Mngr** (manager), or **Mngr+** (manager of managers).| String |`IC`| Reserved|
|**WeeklyBadgeOnsiteDays**| The average number of days per week an employee works from the company’s main worksite. Must be a number between 0 and 7. WeeklyBadgeOnsiteDays can be based on badge data or on other sources—for example, tags in the HR system showing the number of days an employee plans to work onsite.| Double | `4` |Reserved|
|**Location** | An employee’s office location.| String | `Burbank` | Reserved|
| **CountryOrRegion** |  The country or region in which the employee works. | String | `Japan` | Reserved |
| **My_Custom_attribute**<br> (example: **Campus**)| An attribute you create | String | `West` | N/A (custom)<sup>4</sup>

<sup> 1. You need to include required fields. Each required field needs non-blank values for each row.  </sup>

<sup> 2. If you don’t include an **EffectiveDate** column with your upload, the upload date becomes the default **EffectiveDate**. </sup>

<sup> 3. You don’t have to include any of these reserved fields. However, if you do use them, retain these column names.</sup>

<sup> 4. You’re not required to include custom attributes. If you do add them, however, they can’t have the same name as any of the required or reserved attributes. </sup>

### Attribute notes and recommendations

#### Some attributes exist only for a subset of the population

When choosing attributes to include, some attribute values might be populated for one organization but not others. For example, if the upload includes sales quota-attainment data that only applies to your sales organization, you can't use this data for filtering and grouping employees outside of sales.

#### Too many unique values

Sometimes an attribute has too many unique values to use for grouping and filtering. For example, if a job function or code is too narrowly defined, it might not give you a useful view of the overall group. If an attribute has hundreds of unique values that result in a small population group per value, the attribute might not be useful.

#### Too few unique values

Conversely, sometimes an attribute is too broadly defined for useful filtering. For example, if your organization resides entirely in the United States and your HR records per employee contain a country code that always equals US, that attribute wouldn't be useful.

#### Redundant attributes

Some attributes might represent the same data and provide unnecessary redundant data for analysis. For example, HR data could contain both a cost center ID and a cost center name for an employee. Because both represent the same information in a slightly different format, include only the one with the more "user friendly" name.

#### Line-of-business data

Unlike HR data, for line-of-business data, you might not need to include every person in your company as part of your data upload. Knowing the scenarios you want to analyze will help you to decide.
For example, suppose you want to compare collaboration patterns between employees in the Sales organization who have high engagement as compared to those who have low engagement. Although you want HR data for all employees so you can characterize broader collaboration patterns, you only need engagement score data for employees in the Sales organization, because you're using the score values to group and filter specific report outputs.

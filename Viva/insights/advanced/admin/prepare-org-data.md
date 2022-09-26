---
title: Prepare organizational data in Viva Insights
description: Learn how to prepare and structure your data for upload into the Viva Insights advanced insights app. 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Prepare organizational data

This article describes the value of organizational data for analysts and the steps of identifying, gathering, and structuring the data before uploading it.

To learn more about the nature and use of organizational data, see [Use organizational data for more effective analysis](#use-organizational-data-for-more-effective-analysis). When you’re ready to start working with organizational data, the following sections describe how:

* [Identify trends that you want to analyze](#identify-trends-that-you-want-to-analyze) – Decide what trends you need to learn about to improve efficiency at work. From this, you can better choose what organizational data to use.
* [Know what data to include](#know-what-data-to-include) – A few data attributes are required, and many are optional. Among the optional ones, choose those that best serve your analytical purposes.
* [Get an export of organizational data](#get-an-export-of-organizational-data) – Have an admin export the HR data from your organization’s HR system. Optionally, include line-of-business data, if your analysis requires it.
* [Structure the organizational data](#structure-the-organizational-data) – For your data to validate successfully, you need to first structure it correctly in the.csv file that you upload.
* [Upload the data](#upload-the-data) – After your .csv file is ready, you upload it to the advanced insights app where, after validation and processing, it becomes available for analysis.

## Use organizational data for more effective analysis

Organizational data is descriptive information about employees. After an admin uploads organizational data, the advanced insights app combines it with Microsoft 365 data to provide detailed, actionable insights into the company's communication and collaboration trends. An analyst can uncover these trends and use them to make more effective business decisions.

Here are examples of what analysts can do with advanced insights after the organizational data is uploaded:

* Know how people communicate across job functions, department groups, and management hierarchies by enabling the grouping and filtering of descriptive attributes.
* Customize metrics to quantify group relationships, such as collaboration time between the marketing and sales groups.

Advanced insights automatically collects collaboration data from Microsoft 365. Analyzing just this data would create an incomplete picture; it’s the organizational data that you upload that provides analysis context.

## Identify trends that you want to analyze

To know what organizational data to extract, you first need to decide what workplace trends you want to learn about. For example, in an upcoming analysis, you may want to examine collaboration across different employee segments, or groups. You need to first define these groups, which you can do in various ways:

* Groups as defined by organizational data
* Groups made up of organizational hierarchy levels
* Groups made up of performance, engagement, or other line-of-business data

Defined groups can be used in the following examples of analyses:

### Collaboration between groups

A common analysis scenario is to find patterns of collaboration between different groups of employees. For example, you might want to know how much your product marketing team is talking to your sales team.

Attributes for segmenting populations can be helpful to consider in defining patterns of collaboration, such as:

* Job family or role attributes, such as profession, function, discipline, and job code
* Organization, line of business, or cost center, such as HR, Finance, Sales, and Marketing
* Location attributes, such as city, state, country, and regions, as defined by your organization
* Attributes that describe their work, such as remote, full-time employee or vendor, part-time or full-time, their tenure within the organization, or the tenure of their current role.

Most of these attributes are available within HR information systems.

### Hierarchical collaboration

It’s also common to seek patterns of collaboration behavior in reference to the hierarchy of your organization, as well as to quantify collaboration between managers and individual contributors, and between higher and lower levels and layers in the organization.

The following concepts are helpful in this kind of analysis:

* **IC or manager** – Whether an employee is an individual contributor or a manager.
* **Organizational hierarchy** – For example, the names of all managers above the employee in that employee's reporting structure; each manager can be stored as a separate attribute.
* **Layer** – For example, the position of the employee in the organizational hierarchy where layer 0 = the top leader in the company.
* **Span** – For example, the number of direct reports assigned to an employee.
* **Level** – For example, senior manager, VP, director, CVP, and so on.

Most of these attributes are also found in HR information systems.

### Collaboration, engagement, and outcome data

Finally, you might want to consider tying collaboration behavior patterns to employee engagement scores or other performance outcome data, such as sales-quota attainment or high/low performance ratings. This data is often found outside of traditional HR information systems, either in separate HR data repositories or in line-of-business systems.

## Know what data to include

To get full functionality from the advanced insights app, you need to supply several required attributes, as described in [Attribute reference](#attribute-reference). Additionally, you can supply up to 100 optional attributes to group and filter data in interesting and custom ways.

Examples of organizational data include: job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, and manager. This data is supplied to the advanced insights app at the individual level, which means that these attributes provide context to each person in the dataset.

### Employees to include

At a minimum, include the organizational data for all employees who have Viva Insights licenses. It's even better to include every person in your company as part of your data upload, even if you plan to gather collaboration data for only a subgroup, a specific target population within the company.

For example, if the people in Marketing communicate frequently with the people in Product Development, but the app has HR data only about the Marketing organization, you won't be able to create reports to show how much time Marketing is spending with Product Development.

If you can't include every person in your organization, the minimum to include is all people for whom collaboration data is being gathered. This minimum enables you to analyze collaboration patterns between groups within this population, but not between groups outside this population.

### Including all licensed employees

It's the admin's responsibility to maintain up-to-date and complete organizational data. In this task, "complete" means two things: data that includes the right people and includes the right attributes for those people.

The reason for including all licensed employees in the organization is that, if their organizational data is missing, analysts can't filter by that data when they build a query on the **Analysis** page. So, employees whose data is missing will be excluded from the analyses that analysts perform.

#### Notification of missing data

If the app detects that data is missing for one or more licensed employees, it alerts admins through a pop-up notification in the top-right corner of the **Data connections** tab.

##### Upload missing organizational data

To upload this missing data, the admin can follow these steps:

1. On the pop-up notification, select **Download** to download a .csv file that contains the names of licensed employees whose organizational data is missing. 
1. Open the .csv file.
1. Append the missing data for these employees. This means adding attributes (columns) that describe the employees in a way consistent with previous uploads.
1. Upload the file. Refer to [Upload organizational data (subsequent upload)](./upload-org-data-subsequent.md)] for more information.

In addition to including all licensed employees in the upload of organizational data, we recommend that you also include unlicensed employees, as we explained [earlier](#including-all-licensed-employees).

### Get an export of organizational data

Before you format and upload organizational data, you need to get it from one or more sources. Your primary source is the team that manages your organization's HR information systems. This team will need to provide you with a data export of HR attributes for individual employees.

In addition, your analysts might need data about business outcomes. If so, you'll need to contact line-of-business owners who have access to data stores that contain this information. For example, this data might include:

* Performance-review data for specific work groups
* Employee engagement scores captured by HR outside of HR information systems
* Sales or other quota-attainment data that provide additional views into performance
* Employee survey data

After you get this data, you'll need to structure it for successful processing after uploading it to the app.

## Structure the organizational data

After you’ve identified what data to provide, you need to export it into the correct format for uploading it. To start with, the data must be in a UTF-8 encoded .csv file and contain at least the set of required attributes for the population, which can be in any order in the file. For more information about saving a file in UTF-8 format, see Solution.

The file name needs contain only alphanumeric characters (letters and numbers), with no spaces or special characters. For example, FileName2.csv.

### Required attributes

Supply the following attributes as column headers, exactly as written below, need be supplied exactly as written as column headers in the .csv upload.<!--, of which **PersonId** and **ManagerId** are not case sensitive, but **Organization** is.-->

* **EffectiveDate**
    * Make sure the **EffectiveDate** column has values in all rows. If you don’t provide an **EffectiveDate** column in your upload, the date you uploaded the data becomes the default **EffectiveDate**.
* **PersonId**
* **ManagerId**
* **Organization** (case sensitive)

### Reserved optional attributes

The following attributes are reserved column headers for attributes that are currently used to calculate, filter, and group data. <!--As indicated, FunctionType, and SupervisorIndicator are case sensitive.-->

* **LevelDesignation**
* **FunctionType**
* **HireDate**
* **HourlyRate**
* **Layer**
* **SupervisorIndicator**
* **OnsiteDays**
* **Location**

>[!Note]
>Attributes can be in any order in the file. However, the names of these required and reserved attributes can't be used as the names of any new custom attributes.

### Custom attributes

Custom attributes are any additional attributes you want to define to use in filtering and grouping data. When you upload these attributes, analysts can use them when building queries. To learn how to upload custom attributes, refer to [Upload organizational data (first upload)](upload-org-data-first.md). 

> [!Note] 
>
> * The maximum number of total attributes allowed in the system is 105, which includes the five required attributes. 
> * All dates should be in the MM/DD/YYYY format.
> * All numerical fields (such as the required attribute "HourlyRate") must be in the "number" format and cannot contain commas or a dollar sign.

For more information, see Attribute descriptions and data-coverage requirements.

### Example .csv export file

Here's an example snippet of a valid .csv export file:

PersonId,EffectiveDate,HireDate,ManagerIdLevelDesignation,Organization,Layer,Area
Emp1@contoso.com,12/1/2020,1/3/2014,Mgr1@contoso.com,5,Sales,8,Southeast Emp2@contoso.com,11/1/2020,1/3/2014,Mgr1@contoso.com,5,Sales,8,Southeast Emp3@contoso.com,12/1/2020,1/3/2014,Mgr2@contoso.com,4,Sales,7,Northeast Emp4@contoso.com,10/1/2020,8/15/2015,Mgr3@contoso.com,6,Sales,9,Midwest Emp5@contoso.com,11/1/2020,8/15/2015,Mgr3@contoso.com,6,Sales,9,Midwest Emp6@contoso.com,12/1/2020,8/15/2015,Mgr3@contoso.com,6,Sales,9,Midwest

For more information about attributes, refer to the [Attribute reference](#attribute-reference) section.

## Upload the data

After you create a source .csv file, you can upload it to the advanced insights app through the **Organizational data page > Data hub** or **Data connections** tab.

If this is the first time that you'll upload organizational data, refer to [Upload organizational data (first upload)](upload-org-data-first.md). If this isn't the first time, refer to [Upload organizational data (subsequent uploads)](./upload-org-data-subsequent.md). 

After your data has been successfully uploaded, the app performs additional validation and processing to complete provisioning.

## How often to upload organizational data

It's recommended that you upload employee data at least once a month to keep data fresh and analysis relevant. Soon after an employee data upload has succeeded, the updated data becomes available for users to see as insights in the app.

### Supplying data over a time period

<!--pending confirmation-->

By default, Viva Insights includes meeting and email data for measured employees for one year. Organizational data is provided to Viva Insights with an effective date associated with each row in the upload file.

If you do a point-in-time export of organizational data from your HR information system as of the current date, you'll get a picture of your employee population for that single point in time. For the greatest data fidelity during provisioning, you should provide organizational data exports for each of the last 13 months. This data can be supplied in a single file or in a sequence of files. 

Here's how that would look in practice. For each measured employee, you'd have 13 separate rows. Each of those rows would contain an effective date for each month that data was pulled for. If an effective date for each month isn't possible, then you can provide one single point in time. In that case, set the effective date to the first day of the current month, one year back. For example, if provisioning occurred in October 2020, the effective date for all rows should be set to 10/1/2019.

Employee collaboration activity will be mapped to the most recent organizational data snapshot (based on **EffectiveDate**) that precedes the date of the collaboration activity. 

## Attribute reference

This section contains information about the attributes that you use in the organizational data files uploaded to the advanced insights app.

|Attribute (column header) | Description | Data type | Example value| Required or reserved
|--------------------------|----------|---|--------------------|----|
|**PersonId**| Unique identifier for an employee record. It can be the employee's primary SMTP address or email alias.  | Email | `joe@contoso.com`| Required<sup>1</sup>
|**ManagerId** | Unique identifier for an employee’s manager. It can be the manager’s primary SMTP address or email alias.| Email| `sally@contoso.com`| Required |
|**Organization**| The internal organization that an employee belongs to. For more actionable insights, avoid using too few or too many unique Organizations.| String| `Financial Planning and Analysis` |Required|
|**EffectiveDate**| Date that a given attribute value applies for an employee. The attribute applies until another record for the same attribute with a different EffectiveDate is specified. If no EffectiveDate is uploaded, the date of upload is used as default.| DateTime| `12/31/2021`|Required<sup>2</sup>|
|**LevelDesignation** | Level that represents an employee’s experience, management level, or seniority within the organization. For more actionable insights, avoid using too few or too many unique LevelDesignation values.| String | `Director` |Reserved<sup>3</sup>
|**FunctionType**| The job function that an employee performs. For more actionable insights, avoid using too few or too many unique FunctionTypes| String | `Finance Management` | Reserved|
|**HireDate**| The date an employee began employment. If an employee has multiple hire dates, it’s best to use the most recent hire date.| DateTime| `12/31/2021`| Reserved|
|**HourlyRate**| An employee’s salary represented as an hourly rate in US dollars. | Double | `25.25` | Reserved|
|**Layer**| An employee’s position within the organizational hierarchy, expressed as their distance from the top leader of the organization. For example, the CEO is at Layer 0. For more actionable insights, avoid using too few or too many unique Layers. | Integer | `2` |Reserved
|**SupervisorIndicator**| The manager status of an employee as **IC** (individual contributor), **Mngr** (manager), or **Mngr+** (manager of managers).| String |`IC`| Reserved|
|**OnsiteDays**| The average number of days per week an employee works from the company’s main worksite. OnsiteDays can be based on badge data or on other sources—for example, tags in the HR system showing the number of days an employee plans to work onsite.| String | `4` |Reserved|
|**Location** | An employee’s office location.| String | `Burbank` | Reserved|
| **My_Custom_attribute**<br> (example: **Parking_space**)| An attribute you create | String | `15D` | N/A (custom)<sup>4</sup>

<sup> 1. You need to include required fields. Each required field needs non-blank values for each row.  </sup>

<sup> 2. If you don’t include an **EffectiveDate** column with your upload, the upload date becomes the default **EffectiveDate**. </sup>

<sup> 3. You don’t have to include any of these reserved fields. However, if you do use them, retain these column names. If you provide values for reserved fields, they’ll replace previously uploaded values.</sup>

<sup> 4. You’re not required to include custom attributes. If you do add them, however, they can’t have the same name as any of the required or reserved attributes. </sup>

## Attribute notes and recommendations

### Some attributes exist only for a subset of the population

When choosing attributes to include, some attribute values might be populated for one organization but not others. For example, if the upload includes sales quota-attainment data that only applies to your sales organization, you can't use this data for filtering and grouping employees outside of sales.

### Too many unique values

Sometimes an attribute has too many unique values to use for grouping and filtering. For example, if a job function or code is too narrowly defined, it might not give you a useful view of the overall group. If an attribute has hundreds of unique values that result in a small population group per value, the attribute might not be useful.

### Too few unique values

Conversely, sometimes an attribute is too broadly defined for useful filtering. For example, if your organization resides entirely in the United States and your HR records per employee contain a country code that always equals US, that attribute wouldn't be useful.

### Redundant attributes

Some attributes might represent the same data and provide unnecessary redundant data for analysis. For example, HR data could contain both a cost center ID and a cost center name for an employee. Because both represent the same information in a slightly different format, you’ll want to include only the one with the more "user friendly" name.

### Line-of-business data

Unlike HR data, for line-of-business data, you might not need to include every person in your company as part of your data upload. Knowing the scenarios you want to analyze will help you to decide.
For example, suppose you want to compare collaboration patterns between employees in the Sales organization who have high engagement as compared to those who have low engagement. Although you'll want HR data for all employees so you can characterize broader collaboration patterns, you only need engagement score data for employees in the Sales organization, because you're using the score values to group and filter specific report outputs.

## Valid values and formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid).

### Rules for field headers

All field header or column names need to: 

* Begin with a letter (not a number).
* Only contain alphanumeric characters (letters and numbers, for example, **Date1**).
* Have no leading or trailing blank spaces or special characters (non-alphanumeric, such as @, #, %, &).

### Rules for field values

The field values in data rows need to comply with the following formatting rules:

* The required EffectiveDate and HireDate field values must be in the MM/DD/YYYY format
* The required PersonId and ManagerId field values must be a valid email address (for example, `gc@contoso.com`)
* The required Layer field values must contain numbers only
* The required HourlyRate field values must contain numbers only, which the app assumes is in US dollars for calculations and data analysis

## Rules for characters in field values

The following field rules apply to characters in field values:

* Double-byte characters, such as Japanese characters, *are* permitted in the field values.
* The maximum character length of field values in rows is 128 KB, which is about 1024 x 128 characters.
* “New line" (\n) characters are *not* permitted in field values.
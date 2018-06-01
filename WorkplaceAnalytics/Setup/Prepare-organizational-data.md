---
# Metadata Sample
# required metadata

title: Prepare organizational data in Workplace Analytics
description: How to prepare data from your organization to be uploaded to Workplace Analytics. 
author: LeisaLaDell
ms.author: v-leash
ms.date: 02/14/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Prepare organizational data

This article describes what organizational data is and gives the steps to help your prepare it for uploading to Workplace Analytics.

## About organizational data
Organizational data is the information about employees that your company provides to use in Workplace Analytics. Workplace Analytics combines your organizational data with Office 365 to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

This topic introduces key concepts about compiling and uploading organizational data in Workplace Analytics. After reading this topic you will know what kind of organizational data you can provide, how to determine the data you want to provide, what that data can help you discover, and how to upload the data.

### With organizational data you can:

* Know how people communicate across job functions, management hierarchy, etc. by enabling grouping and filtering on organizational data attributes.
* Enable metrics customization that allow you to quantify group relationships (like collaboration time between marketing and sales).
* Enable specific metrics calculations such as insularity and redundancy.

### Organizational data for employees in your organization can come from the following sources:
* Human resources (HR) information systems.
* Other line of business (LOB) data stores encompassing business outcome data, such as:
  * Performance review data from specific work groups.
  * Employee engagement scores captured by HR outside of HR information systems.
  * Sales, or other quota attainment data that provide additional views into performance.
  * Employee survey data.

Examples of organizational data include: job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports and manager. This data is supplied to Workplace Analytics at the individual level, meaning these attributes are used to give context to each person that makes up the dataset.

### To supply Workplace Analytics with organizational data, you will need to work with the following internal teams:
* Team that manages your organization’s HR information system to provide a data export of HR attributes for individual employees.
* Line of business owners who have data that is of interest to analysts for inclusion.

## How often to upload
You can update organizational data as frequently as you like, but it will be refreshed upon the latest update of email and calendar data. Since email and calendar data is updated once a month, it may make sense to provide a updates for this data on a similar cadence.
## Who to include in the data

### HR data
We recommend that you include every person in your company as part of your data upload, even if you only plan to gather collaboration data for a sub-group within your company. This will enable you to see who everyone is collaborating with, even if they are outside your target population.

For example, if the people in Marketing communicate frequently with the people in Product Development, but Workplace Analytics only has HR data about the Marketing organization, you won't be able to create reports to show how much time Marketing is spending with Product Development.

If you can't include every person in your organization, the minimum is to include all people for whom collaboration data is being gathered, which will allow you to analyze collaboration patterns between groups within this population, but not between groups outside this population.

### Line-of-business data
Unlike HR data, for line-of-business data you may not need to include every person in your company as part of your data upload. Knowing the scenario you want to analyze will help you to decide. 

For example, suppose you want to compare collaboration patterns between employees in the Sales organization who have high engagement versus those who have low engagement. Although you will want HR data for all employees so you can characterize broader collaboration patterns, you only need engagement score data for employees in the sales organization, as you will be using the score values to group and filter specific report outputs.

## What to include in the upload
To get full functionality from Workplace Analytics, there are several required attributes that you will need to supply (these are described in the Export data section below). Additionally, you can supply up to 65 total attributes that you can use to group and filter data in interesting custom ways.

The specific requirements for which organizational data attributes you want to provide will depend on the specific business scenarios that data analysts want to explore.

You can use the following steps to help you think through all the relevant factors in determining what data to provide.

## Step one – Identify the kind of collaboration and communication trends you want to analyze
In your analysis, you will look at collaboration across different employee segments. These employee segments can be groups as defined by organizational data, groups made up of organizational hierarchy levels, or groups made up of performance, engagement, or other line of business data. We discuss a few common analyses here.

### Collaboration between groups
A common analysis scenario is to find patterns of collaboration between different groups of employees.  For example, you might want to know how much your product marketing team is talking to your sales team.

Concepts that are helpful in segmenting populations to define patterns of collaboration are:
* Job family or role attributes, such as profession, function, discipline, job code.
* Organization, line of business, or cost center, such as HR, Finance, Marketing.
* Location attributes, such as city, state, country, regional areas as defined by your organization.
* Attributes describing the type of worker, such as remote worker, exempt/non-exempt, FTE/vendor, part time/full time, tenure in organization, tenure in current role.

Most of these attributes are available within HR information systems.

### Hierarchical collaboration
It is also common to want to define patterns of collaboration behavior in reference to the hierarchy in your organization, as well as to quantify collaboration between managers and individual contributors, and between higher and lower levels and layers in the organization.

Concepts that are helpful in this analysis are:
* Whether an employee is an individual contributor or a manager.
* Organizational hierarchy. For example, the names of all managers above the employees in his or her reporting structure; each manager can be stored as a separate attribute.
* Layer. For example, the position of the employee in the organizational hierarchy where layer 0 = the top leader in the company.
* Span. For example, the number of direct reports assigned to an employee.
* Level. For example, senior manager, VP, director, CVP, and so on.

Most of these attributes are also found in HR information systems.

### Collaboration, engagement, and outcome data
Finally, you many want to consider tying collaboration behavior patterns to employee engagement scores or other performance outcome data such as sales quota attainment or high/low performance ratings. These data are often found outside of traditional HR information systems, either in separate HR data repositories or in line of business systems.

## Step two – Avoid common pitfalls
Strive to avoid the following pitfalls when choosing the organizational data you want to provide.

### Too many unique values 
Sometimes an attribute will have too many unique values to be used in grouping and filtering.

For example, if a job function or code is very narrowly defined, it might not give a useful view of the overall group. If it is likely that an attribute could have hundreds of unique values resulting in a small population group per value, the attribute may not be useful.

### Too few unique values
Conversely, sometimes an attribute is too broadly defined to allow for useful filtering.

For example, if your organization resides entirely in the United States and your HR records per employee contain a country code that always equals US, that attribute would not be useful to include.

### Redundant attributes
Some attributes may represent the same data and provide redundant data that is not necessary for analysis.

For example, HR data could contain both a cost center id and a cost center name for an employee. Since both represent the same information in a slightly different format, you may want to include only the one with the more “user friendly” name.

### Attributes that only exist for a population subset
When choosing attributes to include, be aware of cases where some attribute values might be populated for one organization but not others.

For example, if you bring in sales quota attainment data that only applies to your sales organization you must be mindful that this data cannot be used for filtering and grouping employees outside of sales.

### Dirty data
In addition to some attributes only being applicable for certain employees in the population, you may find that data from HR and other line of business systems can often be dirty or inconsistent. As noted later in this topic, there are key organizational data attributes that must be supplied in order for Workplace Analytics to accept the data. If your systems have gaps in these special attributes, you will have to perform data cleansing to provide accurate values for the missing entries or suitable defaults.

## Step three – Export data
Once you have identified the data to provide, you will need to export it into a format that can then be uploaded to Workplace Analytics. This section explains how to properly format the data into a comma separated value (.csv) file that will successfully upload into Workplace Analytics.

### Required attributes and file format
The data must be supplied in a UTF-8 encoded .csv file and contain a set of required attributes for the population. The following table provides details on the required attributes and the data coverage requirements.

**Required attributes**. These attributes must be supplied with these exact column headers (case sensitive) in the .csv upload:
* PersonId
* HireDate
* EffectiveDate
* ManagerId
* TimeZone
* LevelDesignation
* Organization

**Reserved optional attributes**. These reserved column headers are for attributes that are currently used only to filter and group data. In the future, they will be used for additional metric calculations.  While these attributes are not required, if included, they must meet the coverage requirements (see table below).
* FunctionType
* Layer
* HourlyRate

**Custom attributes**. You may also define any additional attributes to use in filtering and grouping data.  

> [!Note] 
> The maximum number of total attributes allowed in the system is 65 (including the attributes mentioned above). 

Attribute description and data coverage requirements

> [!Note] 
> All dates should be in the MM/DD/YYYY format. 


Attribute (column header) | Description of data / data validity | Data coverage requirements
---------|----------|---------
PersonId |Unique identifier for the employee record. This identifier can be the employee's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example: <li><u>Allowed:</u> person.name@xyz.com </li><li><u>Not allowed:</u> <Name, Person> (person.name@xyz.com) </li> | Each row must contain a valid PersonId. Each upload file can have only ONE record with the same PersonID / EffectiveDate pair.
 HireDate| Date the employee began employment. This date determines the beginning date for calculating metrics of a measured employee. If an employee has multiple hire dates (for example: first hire date, most recent hire date), we recommend using the most recent hire date. | Each row should ideally contain a valid HireDate. If not included, metrics will be calculated from the start date of the data collection period.
EffectiveDate |Date for which the given attribute value applies for the employee. The attribute will apply until another record for the same attribute with a different effective date is specified. | Each row must contain a valid EffectiveDate. Each upload file can have only one record with the same PersonID / EffectiveDate pair.
ManagerId | Unique identifier for the employee’s manager. This data is needed to correctly calculate metrics for time spent with managers and their direct reports.<br>This identifier can be the manager's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example: <li><u>Allowed:</u> person.name@xyz.com </li><li><u>Not allowed:</u> <Name, Person> (person.name@xyz.com) </li> | Each row must contain a valid ManagerId.
 TimeZone |Time zone in which the employee performs work. This must be one of the time zones in Time zones in Workplace Analytics. If you do not have a time zone available for each employee, the system will use the default, which is Pacific Standard Time. | This attribute column is not required. If not included, the default will be used.
LevelDesignation | The employee’s level, represented as a string. The level will be specific to your organization and can represent an employee’s experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity. | Each row must contain a LevelDesignation value.
Organization| The internal organization the employee belongs to. An employee’s organization will be specific to your individual needs and could be identified by the leader of the organization, or other naming convention. This data is needed to correctly calculate metrics for redundancy and insularity. | Each row must contain an organization value.
FunctionType | The job function the employee performs. This is specific to your organization. This data is used to filter and group reports, and for grouping of data in Explore the metrics features. | This attribute column is not required. If it is included, then each row must contain a function value.
 Layer | The place within the organizational hierarchy where the employee belongs. The layer is represented as an integer and expressed as distance from the top leader of the organization. For example, the CEO, is at layer 0. This data is used to filter and group reports, and for grouping of data in Explore the metrics features. | This attribute column is not required. If it is included, then each row must contain an integer value.
HourlyRate | The salary of the employee, represented as an hourly rate (if you have annual rate, divide each record by 2080). Note: The value can be formatted as a whole number, or include two decimal places, and cannot include any special characters such as a dollar sign. The value can represent pay only, or include the full value of benefits, as long as that choice is consistently applied for all employees. This is not yet used in calculations but can be used to filter and group employees. Note that the Explore the metrics feature uses a fixed default HourlyRate of $75. | This attribute column is not required. If it is included, then each row must contain a floating point or integer value with no special characters (such as a dollar sign).
Any user-defined columns | Additional columns can represent any data that you want to use in queries to group and filter employee records. | No coverage requirements.

### Supplying data over a time period
By default, Workplace Analytics includes meeting and email data for measured employees for one year. 

Organizational data is provided to Workplace Analytics with an effective date associated with each row in the upload file, as mentioned above.

If you do a point in time export of organizational data from your HR information system as of the current date, you will get a picture of your employee population for that single point in time; therefore, for greatest data fidelity, during provisioning you should provide organizational data exports for each of the 12 months in the past year. This can be supplied in a single file or in a sequence of files.

This means that for each measured employee you would have 12 separate rows for each employee, with an effective date for each month that data was pulled. If this is not possible, then you can provide one single point in time. In this case, the effective date should be set to the first day of the current month, one year back. For example, if provisioning occurred in June 2017 the effective date for all rows should be set to 6/1/2016.

### Example .csv export file
This is an example snippet of a valid CSV export file:

PersonId,EffectiveDate,HireDate,ManagerId,TimeZone,LevelDesignation,Organization,Layer,Area
Emp1@contoso.com,6/1/2016,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast
Emp1@contoso.com,7/1/2016,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast
Emp1@contoso.com,8/1/2016,1/3/2014,Mgr2@contoso.com,Pacific Standard Time,4,Sales,7,Northeast
Emp2@contoso.com,6/1/2016,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest
Emp2@contoso.com,7/1/2016,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest
Emp2@contoso.com,8/1/2016,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest

### Allowed time zones
The default time zone for Workplace Analytics is Pacific Standard Time. Visit [Timezones for Workplace Analytics](../Use/Timezones-for-workplace-analytics.md) for a complete list of the times zones that you can use.

## Step four - Upload data
After you have created your source .csv file, you can upload it to the Workplace Analytics service. See [Upload organizational data](Upload-organizational-data.md). 

<!-- OLD CONTENT: 

### To upload your organizational data to Workplace Analytics 
1. On the **Settings** page, click **Organizational data**.
2. Browse to, and then upload your file.

The upload process will verify that the file contains the required column headers. 

If your upload succeeds, you see an Upload successful message. If the file does not contain the required column headers, you will receive an error message. -->

After your data has been successfully uploaded, Workplace Analytics will perform additional validation and processing to complete provisioning. The Workplace Analytics team will contact your Workplace Analytics administrator if any problems arise.

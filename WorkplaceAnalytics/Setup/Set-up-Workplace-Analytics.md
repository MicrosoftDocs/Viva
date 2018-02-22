---
# Metadata Sample
# required metadata

title: Workplace Analytics Getting Started Checklist
description: This is a Checklist to introduce what is required to implement Workplace Analytics for your Organization
author: v-leash
ms.author: v-leash
ms.date: 2/16/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Workplace Analytics Getting Started Checklist
To successfully set up and implement Workplace Analytics, you will need to coordinate and obtain information and buy-in from a wide variety of stakeholders.

Use this checklist to help assemble the people and obtain the data and configuration information that you will need to set up and provision Workplace Analytics.

> [!TIP]
> This checklist outlines recommended steps and a high-level list of items to consider and is not intended to be exhaustive. You may want to copy this checklist into a spreadsheet and then customize it for your organization.

# Checklist

| Task | Owners | Outcome |
|------|--------|---------|
|  [1 - Determine key personas and assign roles for implementation](#step-one-determine-key-personas-and-roles-for-implementation)    |Workplace Analytics sponsor (the initial point-person for the engagement)       |   A list of people in your organization with key roles identified      |
| [2 - Assign licenses to population in scope for analysis](#step-two-assign-licenses-to-population-in-scope-for-analysis)     |   Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator     | Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator       |
|   [3 - Assign roles to WpA Admin and Analysts](#step-three-assign-roles-to-wpa-admin-and-analysts)   |    Office 365 global administrator   |     Administrator can use Workplace Analytics to set system defaults, privacy settings, upload and verify organizational data; data analysts can log into and use Workplace Analytics once data is provisioned    |
|  [4 - Configure Workplace Analytics settings](#step-four-configure-workplace-analytics-settings)    |    Workplace Analytics sponsor, Workplace Analytics administrator   |  Privacy settings are defined in Workplace Analytics and you have confirmed that you are ready to provision the service using these rules. Default time zone values are defined in Workplace Analytics.        |
|  [5 - Prepare and upload organizational data](#Step-five-Prepare-organizational-data-for-upload)    |   Workplace Analytics administrator, HR information system administrator, LOB system administrators, or data analyst     |      placeholder   |
|  [6 - Validate and verify data](#step-seven-validate-and-verify-data)    |  Workplace Analytics administrator, data analysts with full access     |    Workplace Analytics administrators are comfortable that data has been provisioned successfully, data analysts are comfortable with the data and ready to use Workplace Analytics for their analysis.     |
|    [7 - Set up meeting exclusions](#Step-eight-Set-up-meeting-exclusions)  |   Workplace Analytics administrator, data analysts with full access     |     Workplace Analytics administrators and analysts are satisfied that meeting query results are focused on the data relevant for analysis.


When you have finished all the steps, you are ready to [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md).

## Step one: Determine key personas and roles for implementation

 * **Owner** - Workplace Analytics sponsor (the initial point-person for the engagement)
 * **Task** - Identify people in the organization to fill key roles in setting up Workplace Analytics
 * **Outcome** - A list of people in your organization with key roles identified

Use these personas to help  identify the people you will need to help gather data, make decisions, and perform tasks needed to set up Workplace Analytics.

### Personas

* Workplace Analytics sponsor - The initial point-person for the engagement
* Workplace Analytics administrator - This role has access to Admin and Data Sources features, and will set system defaults, privacy settings, and upload and verify organizational data.
* Office 365 Global administrator
* Exchange administrator
* Human resources (HR) information system administrator
* Line of business (LOB) system administrators, or data analyst

## Step two: Assign licenses to population in scope for analysis

* **Owner** -	Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator
* **Task** - Determine population in scope for analysis and assign licenses via Office 365
* **Outcome** -	Office 365 licenses are assigned for the population that will be analyzed

The Workplace Analytics sponsor will work with the Workplace Analytics administrator and Office 365 Global administrator to identify the population (the people in your company) whose Office 365 collaboration activity you will analyze. These people are referred to as _measured employees_ within Workplace Analytics. Employees in your organization that are not licensed for analysis but may have meeting and email collaboration with measured employees are called _other internal collaborators_.

Some organizations will analyze the entire population, while others will use sub-populations for specific analysis scenarios and sections of the organization.

Once you have identified the population in scope, the Office 365 Global administrator will assign Workplace Analytics licenses to users in this population.  

You can use Office 365 PowerShell to do a bulk assignment of Workplace Analytics licenses to users.

**Related topics**

[How to assign Office 365 licenses](https://support.office.com/en-us/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc?ui=en-US&rs=en-US&ad=US)

[How to assign bulk licenses](office365/enterprise/powershell/assign-licenses-to-user-accounts-with-office-365-powershell)


### Mailboxes not fully migrated to Office 365 Exchange Online
If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with the following options.
### Options for mailboxes hosted using Exchange on-premises
* Migrate these mailboxes to Office 365 Exchange Online
* Contact the FastTrack team to understand the process for analyzing these mailboxes (this requires additional work streams within your organization).


## Step three: Assign roles to WpA Admin and Analysts

* **Owner** - Office 365 global administrator
* **Task** - Assign users for administrators and data analysts to Workplace Analytics service
* **Outcome** - Administrator can use Workplace Analytics to set system defaults, privacy settings, upload and verify organizational data; data analysts can log into and use Workplace Analytics once data is provisioned

To allow administrators to set system defaults, privacy settings, upload and verify organizational data, and to allow data analysts to be able to use Workplace Analytics, you must assign users to the Workplace Analytics service.

### Workplace Analytics roles and the level of access
* **Analyst role** - Full access to all service features, except Admin. This role is used for the analyst who requires the most complete access to the data.
* **Analyst (Limited Access) role** - Access to Home page, Explore metrics features. This role is used for the analyst who only needs access to insights generated from our curated set of Explore the metrics dashboards
* **Administrator role** - Access to Admin and Data Sources features. This role is used for the Workplace Analytics administrator to set system defaults, privacy settings, upload, and verify organizational data.

### To assign users to Workplace Analytics
* Follow the instructions in this [support article](/active-directory/active-directory-coreapps-assign-user-azure-portal).

> [!NOTE]
> Workplace Analytics does not support assigning licenses to groups.


## Step four: Configure Workplace Analytics Settings

### Time zone
* **Owner** - Workplace Analytics administrator
* **Task** - Provide default time zone values the system will use in metric calculations if the data is not available for a measured employee or other internal collaborator
* **Outcome** - Default time zone values are defined in Workplace Analytics

The default time zone is used to compute after-hours metrics when a time zone is not provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone.

The default time zone for Workplace Analytics is Pacific Standard Time.

For a complete list of valid times zones, visit [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md)  

### Privacy Settings
* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator
* **Task** - Use company-specific legal and privacy guidelines to define settings to use in Workplace Analytics
* **Outcome** - Privacy settings are defined in Workplace Analytics and you have confirmed that you are ready to provision the service using these rules

Being aware of employees’ rights is a key component to ensuring a successful program using Workplace Analytics.  It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Workplace Analytics.

> [!IMPORTANT]
> Please consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

Once you have examined your privacy needs, you will use the Settings area in Workplace Analytics to define the privacy settings for your data.

### Detail Display:
- **Minimum Aggregation Size**: Set the minimum group size required to display data in Explore Metrics. By default, the minimum group size is set to five. 
- Decide to show or hide subject lines in meeting reports

### User Data Exclusion:
- Exclude emails/meetings to, or from, specific users, or all users from a domain using “;” as the delimiter
- Exclude emails/meetings with specific terms in the subject line using “;” as the delimiter.   Terms can be any combination of letters, numbers and special characters, e.g. client attorney privilege; D&I

> [!NOTE]
> If you exclude email addresses, you should not assign licenses to them.  You also should consider all aliases for an individual.

### Related topic
[Settings in Workplace Analytics](../Use/Settings.md)

## Step five: Prepare and upload organizational data

* **Owner** - Workplace Analytics administrator, HR information system administrator, LOB system administrators, or data analyst
* **Task** - Obtain organizational data needed for analysis from other information systems
* **Outcome** - CSV file of organizational data is generated and uploaded to Workplace Analytics for final provisioning

Organizational data is the information about employees that your company provides to use in Workplace Analytics. Workplace Analytics combines your organizational data with Office 365 to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

### What is Organizational data?
- Individual-level metadata that provides descriptive information of a company’s employees
- Sourced from multiple sources
    - Human Resources Information Systems (HRIS) Ex: Workday, PeopleSoft
    - Payroll Systems
    - Employee Surveys (Engagement, Manager Feedback, Culture)
    - Performance Management Systems or Quota Attainment Systems
    - CRM Systems
- Workplace Analytics Org Data is structured as a flat file with each row representing one person with columns representing attribute fields

### How is it used?
- Provides context for the mailboxes that enables Workplace Analytics to calculate metrics based on the relationship of the Org Data attributes
- Enables the user to filter and group data in meaningful ways and generate custom metrics

### How often should it be refreshed?
To account for organization changes, it is recommended to refresh the data monthly
When loading your data the first time, Workplace Analytics loads 13 months of data.  Ideally, you would load 13 dated rows of organizational data for each employee.

#### Who should be included in the Org Data file?
- HR Data:
    - It is recommended HR data is collected for all employees in your company, even if they are not part of the measured population
    - At a minimum, you must have data for all employees in your measured population
- Line of Business Data:
    - Scenario-Dependent: You should have line of business data for all employees of interest in the scenario you are analyzing
> [!NOTE]
>  You can include up to 65 data attributes in your Org data file

>[!Important]
>To help ensure privacy, we recommend not including employee names as any additional attribute.

### What are common pitfalls to avoid?
- Too many or too few unique values
- Redundant values
- Attributes that only exist for a subset of your employees
- Dirty data

### Org Data Required Fields
Must be included in upload file

|Attribute<br>(Names must match, case sensitive)|Description|Data Coverage Requirements|Format Examples|
|-----------------------------------------------|-----------|--------------------------|---------------|
|PersonId|Unique identifier for the employee record. Recommend the primary SMTP is used. Can be email address, alias, or UPN for the employee, must be in simplified format (such as: person.name@xyz.com, not <Name, Person> (person.name@xyz.com)).<br>NOTE: This is hidden in the query output row level data|Each row must contain a valid PersonId.<br>Each load file can have only ONE record with the same PersonID / EffectiveDate pair.|person.name@xyz.com|
|EffectiveDate|Date for which the given attribute value applies for the employee, of the form MM/DD/YYYY. The attribute will apply until another record for the same attribute with a different effective date is specified.  The first effective date must be more than 13 months prior to the processing date.|Each row must contain a valid EffectiveDate.<br>Each load file can have only ONE record with the same PersonID / EffectiveDate pair.|MM/DD/YYYY|
|HireDate|Date the employee began employment. This date determines the beginning date for calculating metrics of a measured employee. If an employee has multiple hire dates (for example: first hire date, most recent hire date), we recommend using the most recent hire date.|Each row should ideally contain a valid HireDate.<br>If not included, metrics will be calculated from the start date of the data collection period.|MM/DD/YYYY|
|ManagerId|Unique identifier for the employee’s manager. Can be email address, alias, or UPN and must be in simplified format. This data is needed to correctly calculate metrics for time spent with managers and their direct reports. NOTE: This is hidden in the query output row level data|Each row must contain a value.  If no manager, can use something like “nomanager@xyz.com”|manager.name@xyz.com|
|TimeZone|Time zone the employee does work in. This must be one of the Windows nomenclature time zones. If you do not have time zone available for each employee, the system will use the default provided.|Each row should contain a value. If not present, the default will be used.|Pacific Standard Time|
|LevelDesignation|The employee’s level, represented as a string. The level can represent an employee’s experience or management level, or seniority within the organization, and will be specific to your organization. This data is needed to correctly calculate metrics for redundancy and insularity.|Each row must contain a value.  If no value exists for an employee, can use a dummy term such as “not applicable”|CEO, Vice President, Director, Manager, IC|
|Organization|The internal organization the employee belongs to. An employee’s organization will be specific to your individual needs and could be identified by the leader of the organization, or other naming convention. This data is needed to correctly calculate metrics for redundancy and insularity.  Important to choose the right level based on how you want to group, filter, or compare your data.|Each row must contain a value.  If no value exists for an employee, can use a dummy term such as “not applicable”|Marketing, Finance, Johnson, Jones, Roberts…|

### Org Data Reserved Fields
If included, must meet the specific criteria and naming conventions outlined below

|Attribute<br>(Names must match, case sensitive)|Description|Data Coverage Requirements|Format Example|
|-----------------------------------------------|-----------|--------------------------|--------------|
|FunctionType|The job function the employee performs. This is also specific to your organization. This data is used to filter and group reports, and for grouping of data in Explore metrics features.|This column header is not required to be present; if it is present, then all rows must contain a value.  If there is no value for an employee, use a dummy value such as “not applicable”.|Software Engineering, Program Management, Finance Management|
|Layer|The place in the organizational hierarchy that the employee belongs, represented as an integer and expressed as distance from the CEO, who is at layer 0. This data is used to filter and group reports, and for grouping of data in Explore metrics features.|This column header is not required to be present; if it is present, then all rows must contain a value.  If there is no value for an employee, use a dummy value such as “not applicable”.|0,1,2,3,…|
|HourlyRate|The salary of the employee, represented as an hourly rate (if you have annual rate, divide each record by 2080). The value can be expressed as pay only, or loaded including full value of benefits; only requirement is that it is consistently specified across all employees. This is not yet used in calculations but can be used to filter and group employees. Note that the Explore metrics feature uses a default HourlyRate of $75 that currently cannot be changed.|This attribute column header is not required to be present; if it is present, then all rows must contain a floating point or integer value.  **DO NOT INCLUDE A “$” SIGN**|75|

### Org Data Common Additional Fields
Note: Avoid special characters

|Attribute|Description|Format Example|Potential Specific Use Cases|
|---------|-----------|--------------|----------------------------|
|Location|Location of the employee.  Often this is broken up into multiple fields to represent different levels of detail (Country, Region, State, City).  For workspace planning cases, you may go to the site or building level.|United States<br>West Region<br>Washington<br>Seattle|All<br>More specific attributes for Workspace Planning|
|Organization2|Drill down of Organization to get to a more specific group of employees. An employee’s organization will be specific to your individual needs and could be identified by the leader of the organization, or other naming convention.|HR Talent Management|All|
|Organization3|(see description above for Organization2)|Learning and Development|All|
|Cost Center|Cost center groupings of employees|Center A, Center B…|All|
|RoleType|An indicator of whether the role is an Individual Contributor, Manager, or Manager of Managers|IC, Mgr, Mgr+|All|
|EmployeeType|An indicator of whether the employee is a contractor, vendor, exempt, non-exempt, or other employee type designations|Vendor, Regular, etc|All|
|Tenure|Length of tenure at the company|6|All|
|Title|Standard Job Title|Sr Software Engineer|All|
|Performance Rating|Employee performance rating category.  This can be useful in looking at work patterns of high performing people.|Exceeds, Meets, Does not Meet|All|
|EngagementScore|Employee engagement score rating category.  This can be useful in looking at work patterns associated with engaged employees.|High, Medium, Low|Employee Engagement<br>Manager Effectiveness|
|QuotaAttainment|Employee quota attainment category.  This can be useful in looking at work patterns associated with high performing sales roles.|Exceeds, Meets, Does not Meet|Sales Productivity|
|ManagerScore|Manager feedback survey score rating categories.  This can be useful in looking at manager effectiveness initiatives.|High, Medium, Low|Employee Engagement<br>Manager Effectiveness|


### To prepare your organizational data for upload to Workplace Analytics
* Follow the instructions in the topic [[Prepare and upload organizational data - link]].

Once the .csv file has been created, the Workplace Analytics administrator can upload it into the service.

### To upload your organizational data to Workplace Analytics
1.	On the **Settings** page, click **Organizational data**.
2.	Browse to, and then upload your file.

### After upload
The upload process will check that you have the correct headers in the file for the data that Workplace Analytics requires.
* If your upload succeeds, you see an Upload successful message.
* If you do not have the required attribute headers in your file, you will receive an error message.

Once your upload has been submitted successfully, there is additional validation and processing of your data to complete provisioning. If any problems arise, the Workplace Analytics team will contact your Workplace Analytics administrator.

### After provisioning
Once data is completely provisioned, Workplace Analytics users will be able to access full product features.
Office 365 meeting and email data is refreshed monthly. This is a good time for the Workplace Analytics administrator to also generate and upload updated organizational data.

### Related topic
[Data sources in Workplace Analytics](../Use/Data-sources.md)

## Step six: Validate and verify data

* **Owner** - Workplace Analytics administrator, data analysts with full access
* **Task** - Ensure Office 365 data is available and ready for analysis, ensure the correct organizational data has been uploaded and is ready for analysis.
* **Outcome** - Workplace Analytics administrators are comfortable that data has been provisioned successfully, data analysts are comfortable with the data and ready to use Workplace Analytics for their analysis.

Once final provisioning is complete, Workplace Analytics administrators and data analysts can use the Data sources section to verify that Office 365 and organizational data is loaded and ready for use.

Using Data sources metrics, Workplace Analytics administrators and data analysts can:
* Verify that Office 365 data is available for analysis for the expected number of measured employees.
* Work with the internal suppliers of organizational data (HR information system administrators, LOB system administrators, or data analysts) to verify that the necessary data has been loaded as expected.

Data sources metrics help Workplace Analytics data analysts:
* Get a high-level picture of the data that is available for analysis.
* Verify that the organizational data they need for their specific analysis are available.
* Feel comfortable that the data is applicable to the business problem being analyzed.

### To view the Data sources metrics
* On the navigation bar, click **Sources**.

## Step seven: Set up meeting exclusions
* **Owner** - Workplace Analytics administrator, data analysts with full access
* **Task** - Set meeting exclusion rules to reflect your company's meeting norms and exclude meetings that are not relevant for analysis.  
* **Outcome** - Workplace Analytics administrators and analysts are satisfied that meeting query results are focused on the data relevant for analysis.

### Related topics

[Understand meeting exclusions](../Use/Understand-meeting-exclusions.md)

[Create custom meeting exclusions](../Use/Create-custom-meeting-exclusions-rules.md)

---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup Checklist
description: This is a Checklist to introduce what is required to implement Workplace Analytics for your Organization
author: v-leash
ms.author: v-leash
ms.date: 2/16/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Workplace Analytics Setup Checklist
To successfully set up and implement Workplace Analytics, you will need to coordinate and obtain information and buy-in from a wide variety of stakeholders.

Use this checklist to help assemble the people and obtain the data and configuration information that you will need to set up and provision Workplace Analytics.

> [!TIP]
> This checklist outlines recommended steps and a high-level list of items to consider and is not intended to be exhaustive. You may want to copy this checklist into a spreadsheet and then customize it for your organization.

## Checklist

| Task | Owners | Outcome |
|------|--------|---------|
|  [1 - Determine key personas and assign roles for implementation](#step-one-determine-key-personas-and-roles-for-implementation)    |Workplace Analytics sponsor (the initial point-person for the engagement)       |   A list of people in your organization with key roles identified      |
| [2 - Assign licenses to population in scope for analysis](#step-two-assign-licenses-to-population-in-scope-for-analysis)     |   Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator     | Office 365 licenses are assigned for the population that will be analyzed     |
|   [3 - Assign roles to WpA Admin and Analysts](#step-three-assign-roles-to-Workplace-Analytics-Admins-and-Analysts)   |    Office 365 global administrator   |     Workplace Analytics roles are assigned so that administrators can use Workplace Analytics to set system defaults, privacy settings, and upload and verify organizational data. And,  data analysts can log into and use Workplace Analytics once data is provisioned.   |
|  [4 - Configure Workplace Analytics settings](#step-four-configure-workplace-analytics-settings)    |    Workplace Analytics sponsor, Workplace Analytics administrator   |  Privacy settings are defined in Workplace Analytics and you have confirmed that you are ready to provision the service using these rules. Default time zone values are defined in Workplace Analytics.        |
|  [5 - Prepare and upload organizational data](#Step-five-Prepare-and-upload-organizational-data)    |   Workplace Analytics administrator, HR information system administrator, LOB system administrators, or data analyst     |     [[CONTENT PLACEHOLDER]]    |
|  [6 - Validate and verify data](#step-six-validate-and-verify-data)    |  Workplace Analytics administrator, data analysts with full access     |    Workplace Analytics administrators are comfortable that data has been provisioned successfully, data analysts are comfortable with the data and ready to use Workplace Analytics for their analysis.     |
|    [7 - Set up meeting exclusions](#Step-seven-Set-up-meeting-exclusions)  |   Workplace Analytics administrator, data analysts with full access     |     Workplace Analytics administrators and analysts are satisfied that meeting query results are focused on the data relevant for analysis.


When you have finished all these steps, you are ready to [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md).

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

#### Related topics

[How to assign Office 365 licenses](https://support.office.com/en-us/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc?ui=en-US&rs=en-US&ad=US)

[How to assign bulk licenses](https://docs.microsoft.com/en-us/office365/enterprise/powershell/assign-licenses-to-user-accounts-with-office-365-powershell)


### Mailboxes not fully migrated to Office 365 Exchange Online
If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with the following options.
### Options for mailboxes hosted using Exchange on-premises
* Migrate these mailboxes to Office 365 Exchange Online
* Contact the FastTrack team to understand the process for analyzing these mailboxes (this requires additional work streams within your organization).


## Step three: Assign roles to Workplace Analytics Admins and Analysts

* **Owner** - Office 365 global administrator
* **Task** - Assign users for administrators and data analysts to Workplace Analytics service
* **Outcome** - Workplace Analytics roles are assigned so that administrators can use Workplace Analytics to set system defaults, privacy settings, and upload and verify organizational data. And,  data analysts can log into and use Workplace Analytics once data is provisioned.

To allow administrators to set system defaults, privacy settings, upload and verify organizational data, and to allow data analysts to be able to use Workplace Analytics, you must assign users to the Workplace Analytics service.

### Workplace Analytics roles and the level of access
* **Analyst role** - Full access to all service features, except Admin. This role is used for the analyst who requires the most complete access to the data.
* **Analyst (Limited Access) role** - Access to Home page, Explore metrics features. This role is used for the analyst who only needs access to insights generated from our curated set of Explore the metrics dashboards
* **Administrator role** - Access to Admin and Data Sources features. This role is used for the Workplace Analytics administrator to set system defaults, privacy settings, upload, and verify organizational data.

### To assign users to Workplace Analytics
* Follow the instructions in this [support article](/active-directory/active-directory-coreapps-assign-user-azure-portal).

### Related topics
[Group-based licenses in Workplace Analytics](../Use/Group-Based-Licensing.md)

[Use PowerShell to assign roles in Workplace Analytics](../Use/Using-PowerShell-to-Assign-Roles.md)



## Step four: Configure Workplace Analytics Settings

### Time zone
* **Owner** - Workplace Analytics administrator
* **Task** - Provide default time zone values the system will use in metric calculations if the data is not available for a measured employee or other internal collaborator
* **Outcome** - Default time zone values are defined in Workplace Analytics

The default time zone is used to compute after-hours metrics when a time zone is not provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone.

The default time zone for Workplace Analytics is Pacific Standard Time. 

For a complete list of valid times zones, visit [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md)  

### To change the default time zone 
1. On the **Settings** page, click **Settings**.
2. Under **System defaults**, select the time zone you want from the **Default time zone** list.
3. Click **Save**.

> [!IMPORTANT]
> This setting takes effect the next time organizational data is received and processed for the following month. A change in this setting does not affect any historical data.

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

### To set your privacy settings 
1. On the **Settings** page, click **Settings**.
2. Under **Privacy settings**, configure the settings to meet your company's needs.
> [!NOTE]
> You may click **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you click the **I confirm that all privacy settings are complete** checkbox. When you click the checkbox, it begins the processing of Office 365 data.
3. Click **Save**.
> [!IMPORTANT]
>  Carefully validate that your privacy settings are correct, before you click the I confirm that all privacy settings are complete checkbox, You can change the settings at any time, but the settings changes will not take effect until the data is processed again for the following month.
4. To begin the processing of Office 365 data, click **I confirm that all privacy settings are complete**, and then click **Save**.

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

### Related topics
[Data sources in Workplace Analytics](../Use/Data-sources.md)

[Prepare and upload organizational data](../Use/Prepare-and-upload-organizational-data.md) 

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

Workplace Analytics uses activities stored in a person’s Office 365 email and calendar to reveal internal and external collaboration trends. However, a person’s calendar and email can contain a diverse set of activities (such as personal meetings, work-related social activities, all-day training meetings, and so forth) that are not relevant to work-related collaboration, and if included in the metrics, can skew query results.

Analysts can use the Meeting exclusions feature to create custom meeting exclusions that help ensure query results accurately represent relevant meeting norms within their company. Or, analysts may choose to use the default meeting exclusions that exclude a set of meetings that would commonly fall outside relevant collaboration for analysis.


### Related topics

[Understand meeting exclusions](../Use/Understand-meeting-exclusions.md)

[Create custom meeting exclusions](../Use/Create-custom-meeting-exclusions-rules.md)



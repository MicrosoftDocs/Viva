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
To successfully set up and implement Workplace Analytics, you will need to coordinate and obtain information and buy-in from a wide variety of stakeholders.

Use this checklist to help assemble the people and obtain the data and configuration information that you will need to set up and provision Workplace Analytics. 


> [!TIP]
> This checklist outlines recommended steps and a high-level list of items to consider and is not intended to be exhaustive. You may want to copy this checklist into a spreadsheet and then customize it for your organization.

# Checklist 
[[placeholder -  In this article, internal links]]

# Step one: Determine key personas and assign roles for set up

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

# Step two: Determine the population to analyze

* **Owner** -	Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator
* **Task** - Determine population in scope for analysis and assign licenses via Office 365
* **Outcome** -	Office 365 licenses are assigned for the population that will be analyzed

The Workplace Analytics sponsor will work with the Workplace Analytics administrator and Office 365 Global administrator to identify the population (the people in your company) whose Office 365 collaboration activity you will analyze. These people are referred to as _measured employees_ within Workplace Analytics. Employees in your organization that are not licensed for analysis but may have meeting and email collaboration with measured employees are called _other internal collaborators_.

Some organizations will analyze the entire population, while others will use sub-populations for specific analysis scenarios and sections of the organization.

Once you have identified the population in scope, the Office 365 Global administrator will assign Workplace Analytics licenses to all cloud users in this population. Learn more about [[how to assign Office 365 licenses - link]].

You can use Office 365 PowerShell to do a bulk assignment of Workplace Analytics licenses to users. Learn more about [[how to assign bulk licenses - link]].

## Mailboxes not fully migrated to Office 365 Exchange Online 
If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with the following options.
## Options for mailboxes hosted using Exchange on-premises
* Migrate these mailboxes to Office 365 Exchange Online
* Contact the FastTrack team to understand the process for analyzing these mailboxes (this requires additional work streams within your organization).


# Step three: Assign users and population 

* **Owner** - Office 365 global administrator
* **Task** - Assign users for administrators and data analysts to Workplace Analytics service
* **Outcome** - Administrator can use Workplace Analytics to set system defaults, privacy settings, upload and verify organizational data; data analysts can log into and use Workplace Analytics once data is provisioned

To allow administrators to set system defaults, privacy settings, upload and verify organizational data, and to allow data analysts to be able to use Workplace Analytics, you must assign users to the Workplace Analytics service.

### Workplace Analytics roles and the level of access
* **Analyst role**: Full access to all service features, except Admin. This role is used for the analyst who requires the most complete access to the data.
* **Analyst (Limited Access) role**: Access to Home page, Explore metrics features. This role is used for the analyst who only needs access to insights generated from our curated set of Explore the metrics dashboards
* **Administrator role**: Access to Admin and Data Sources features. This role is used for the Workplace Analytics administrator to set system defaults, privacy settings, upload, and verify organizational data. 

### To assign users to Workplace Analytics 
* Follow the instructions in this support article. [[get document from teams - link]]
[[NOTES - Need to mention that we don’t support Group based license assignment .  
Inlcude a link to the document that FT currently uses]].


# Step four: Configure privacy and time zone options

## Privacy
* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator
* **Task** - Use company-specific legal and privacy guidelines to define privacy settings to use
* **Outcome** - Privacy settings are defined in Workplace Analytics and you have confirmed that you are ready to provision the service using these rules


Being aware of employees’ rights is a key component to ensuring a successful program using Workplace Analytics.  It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics. 

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Workplace Analytics.

> [!IMPORTANT]
> Please consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

Once you have examined your privacy needs, you will use the Settings area in Workplace Analytics to define the privacy settings for your data.

[[explain privacy settings considerations and implications - -fast track docs and robert’s doc. - link]]

### To configure your privacy settings
1.	On the **Settings** page, click **Settings**.
2.	Under **Privacy settings**, configure the settings to meet your company's needs.
> [!NOTE]
> You may click **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you click the **I confirm that all privacy settings are complete** checkbox. When you click the checkbox, it begins the processing of Office 365 data.
3.	Click **Save**.
> [!NOTE]
> Carefully validate that your privacy settings are correct, before you click the **I confirm that all privacy settings are complete** checkbox, You can change the settings at any time, but the settings changes will not take effect until the data is processed again for the following month.
4.	To begin the processing of Office 365 data, click the **I confirm that all privacy settings are complete checkbox**, and then click **Save**.

## Time zone
* **Owner** - Workplace Analytics administrator
* **Task** - Provide default time zone values the system will use in metric calculations if the data is not available for a measured employee or other internal collaborator
* **Outcome** - Default time zone values are defined in Workplace Analytics 



This is the default time zone used to compute after-hours metrics when a time zone is not provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone. 
The default time zone for Workplace Analytics is Pacific Standard Time. Visit Time zones in Workplace Analytics for a complete list of times zones you can use.

### To change the default time zone
1.	On the **Settings** page, click **Settings**.
2.	Under **System defaults**, select the time zone you want from the **Default time zone** menu.
3.	Click **Save**.

This setting takes effect the next time organizational data is received and processed for the following month. A change in this setting does not affect any historical data.

### Related topic
[[Settings in Workplace Analytics - link]]

# Step five: Prepare organizational data for upload

* **Owner** - Workplace Analytics administrator, HR information system administrator, LOB system administrators, or data analyst
* **Task** - Obtain organizational data needed for analysis from other information systems
* **Outcome** - CSV file of organizational data is generated and uploaded to Workplace Analytics for final provisioning

Organizational data is the information about employees that your company provides to use in Workplace Analytics. Workplace Analytics combines your organizational data with Office 365 to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

### To prepare your organizational data for upload to Workplace Analytics
* Follow the instructions in the topic [[Prepare and upload organizational data - link]].

Once the .csv file has been created, the Workplace Analytics administrator can upload it into the service. 

# Step six: Upload your organizational data

### To upload your organizational data to Workplace Analytics
1.	On the **Settings** page, click **Organizational data**.
2.	Browse to, and then upload your file.

## After upload
The upload process will check that you have the correct headers in the file for the data that Workplace Analytics requires.
* If your upload succeeds, you see an Upload successful message.
* If you do not have the required attribute headers in your file, you will receive an error message.

Once your upload has been submitted successfully, there is additional validation and processing of your data to complete provisioning. If any problems arise, the Workplace Analytics team will contact your Workplace Analytics administrator.

## After provisioning
Once data is completely provisioned, Workplace Analytics users will be able to access full product features.
Office 365 meeting and email data is refreshed monthly. This is a good time for the Workplace Analytics administrator to also generate and upload updated organizational data.

### Related topic
[[Data sources in Workplace Analytics - link]] 

# Step seven: Validate and verify data

* **Owner** - Workplace Analytics administrator, data analysts with full access
* **Task** - Ensure Office 365 data is available and ready for analysis, ensure the correct organizational data has been uploaded and is ready for analysis.
* **Results** - Workplace Analytics administrators are comfortable that data has been provisioned successfully, data analysts are comfortable with the data and ready to use Workplace Analytics for their analysis.

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

# Step seven: Set up meeting exclusions 
* **Owner** - Workplace Analytics administrator, data analysts with full access
* **Task** - Set meeting exclusion rules to reflect your company's meeting norms and exclude meetings that are not relevant for analysis.  
* **Results** - Workplace Analytics administrators and analysts are satisfied that meeting query results are focused on the data relevant for analysis.

[[Link to current topic]]

# Step eight: Analyze data 
[[Link to Explore data]]





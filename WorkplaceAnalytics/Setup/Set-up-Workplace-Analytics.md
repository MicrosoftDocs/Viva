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


 [[Placeholder]]  || 
---------|----------|---------
 Owner | Workplace Analytics sponsor (the initial point-person for the engagement)1 |
 Task | Identify people in the organization to fill key roles in setting up Workplace Analytics |
 Outcome | A list of people in your organization with key roles identified | 

		

Use these personas to help  identify the people you will need to help gather data, make decisions, and perform tasks needed to set up Workplace Analytics. 

### Personas

* Workplace Analytics sponsor (the initial point-person for the engagement)
* Workplace Analytics administrator - This role has access to Admin and Data Sources features, and will set system defaults, privacy settings, and upload and verify organizational data.
* Office 365 Global administrator
* Exchange administrator
* Human resources (HR) information system administrator
* Line of business (LOB) system administrators, or data analyst

# Step two: Determine the population to analyze

Owner	Workplace Analytics sponsor, Workplace Analytics administrator, Office 365 Global administrator, Exchange administrator
Task	Determine population in scope for analysis and assign licenses via Office 365
Outcome	Office 365 licenses are assigned for the population that will be analyzed



Column A | Column B | Column C
---------|----------|---------
 A1 | B1 | C1
 A2 | B2 | C2
 A3 | B3 | C3

The Workplace Analytics sponsor will work with the Workplace Analytics administrator and Office 365 Global administrator to identify the population within your company that is within the scope of analysis, meaning, the people whose Office 365 collaboration activity you will analyze.

In Workplace Analytics, these people are referred to as _measured employees_. Employees in your organization that are not licensed for analysis but may have meeting and email collaboration with measured employees are called _other internal collaborators_.

Some organizations will analyze the entire population, while others will use sub-populations for specific analysis scenarios and sections of the organization.

Once you have identified the population in scope, the Office 365 Global administrator will assign Workplace Analytics licenses to all cloud users in this population. Learn more about how to assign Office 365 licenses.

You can use Office 365 PowerShell to do a bulk assignment of Workplace Analytics licenses to users. Learn more about how to assign bulk licenses.

## Mailboxes not fully migrated to Office 365 Exchange Online 
If your organization has not fully migrated to Office 365 Exchange Online, you may encounter mailboxes that are hosted using Exchange on-premises. Your Office 365 Global administrator or Exchange administrator can help to determine if you will encounter this scenario, and assist you with the following options.
## Options for mailboxes hosted using Exchange on-premises
* Migrate these mailboxes to Office 365 Exchange Online
* Contact the FastTrack team to understand the process for analyzing these mailboxes (this requires additional work streams within your organization).


# Step three: Assign users and population 

Owner	Office 365 global administrator
Task	Assign users for administrators and data analysts to Workplace Analytics service
Outcome	Administrator can use Workplace Analytics to set system defaults, privacy settings, upload and verify organizational data; data analysts can log into and use Workplace Analytics once data is provisioned


Column A | Column B | Column C
---------|----------|---------
 A1 | B1 | C1
 A2 | B2 | C2
 A3 | B3 | C3

To allow administrators to set system defaults, privacy settings, upload and verify organizational data, and to allow data analysts to be able to use Workplace Analytics, you must assign users to the Workplace Analytics service.

Choose from these three roles and their corresponding level of access:
* **Analyst role**: Full access to all service features, except Admin. This role is used for the analyst who requires the most complete access to the data.
* **Analyst (Limited Access) role**: Access to Home page, Explore metrics features. This role is used for the analyst who only needs access to insights generated from our curated set of Explore the metrics dashboards
* **Administrator role**: Access to Admin and Data Sources features. This role is used for the Workplace Analytics administrator to set system defaults, privacy settings, upload, and verify organizational data. 
### To assign users to Workplace Analytics 
* Follow the instructions in this support article. [[get document from teams]]
[[NOTES - Need to mention that we don’t support Group based license assignment .  
Inlcude a link to the document that FT currently uses]].


# Step four: Configure privacy and time zone options

# Step five: Upload your organizational data

# Step six: Validate and verify data

# Step seven: Set up meeting exclusions 

# Step eight: Analyze data 






---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup -- Prepare and upload organizational data
description: Eighth setup step -- Prepare and upload organizational data
author: paul9955
ms.author: v-leash
ms.date: 04/19/2018
ms.topic: get-started-article
ms.prod: wpa
---

* **Owner** - Workplace Analytics administrator, HR information system administrator, LOB system administrators, or data analyst
* **Task** - Obtain organizational data needed for analysis from other information systems
* **Outcome** - CSV file of organizational data is generated and uploaded to Workplace Analytics for final provisioning

Organizational data is the information about employees that your company provides to use in Workplace Analytics. Workplace Analytics combines your organizational data with Office 365 to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

### What is organizational data?
- Individual-level metadata that provides descriptive information of a company’s employees
- Sourced from multiple sources
    - Human Resources Information Systems (HRIS) Ex: Workday, PeopleSoft
    - Payroll Systems
    - Employee Surveys (Engagement, Manager Feedback, Culture)
    - Performance Management Systems or Quota Attainment Systems
    - CRM Systems
- Workplace Analytics org dData is structured as a flat file with each row representing one person with columns representing attribute fields.

### How is it used?

 * Provides context for the mailboxes that enables Workplace Analytics to calculate metrics based on the relationship of the Org Data attributes.
 * Enables the user to filter and group data in meaningful ways and generate custom metrics.

### How often should it be refreshed?
To account for organization changes, it is recommended to refresh the data monthly.
When loading your data the first time, Workplace Analytics loads 13 months of data.  Ideally, you would load 13 dated rows of organizational data for each employee.

#### Who should be included in the org data file?
- HR Data:
    - It is recommended HR data is collected for all employees in your company, even if they are not part of the measured population.
    - At a minimum, you must have data for all employees in your measured population.
- Line of Business Data:
    - Scenario-Dependent: You should have line-of-business data for all employees of interest in the scenario you are analyzing.

> [!Note]
> You can include up to 65 data attributes in your Org data file.

> [!Important]
> To help ensure privacy, we recommend not including employee names as any additional attribute. 

### What are common pitfalls to avoid? 
 * Too many or too few unique values
 * Redundant values
 * Attributes that only exist for a subset of your employees
 * Dirty data

### To prepare your organizational data for upload to Workplace Analytics

<!-- 
After you have created your source .csv file, you can upload it to the Workplace Analytics service. After your data has been successfully uploaded, Workplace Analytics will perform additional validation and processing to complete provisioning. The Workplace Analytics team will contact your Workplace Analytics administrator if any problems arise.
-->

* Follow the instructions in the topic [Prepare organizational data](../Setup/Prepare-organizational-data.md).

Once the .csv file has been created, the Workplace Analytics administrator can upload it into the service. For more information, see [Upload organizational data](../Setup/Upload-organizational-data.md).

Once your upload has been submitted successfully, there is additional validation and processing of your data to complete provisioning. If any problems arise, the Workplace Analytics team will contact your Workplace Analytics administrator.

### After provisioning
Once data is completely provisioned, Workplace Analytics users will be able to access full product features.
Office 365 meeting and email data is refreshed monthly. This is a good time for the Workplace Analytics administrator to also generate and upload updated organizational data.

### Related topics
[Data sources in Workplace Analytics](../Use/Data-sources.md)

[Prepare organizational data](../Setup/Prepare-organizational-data.md) 

[Upload organizational data](../Setup/Upload-organizational-data.md)
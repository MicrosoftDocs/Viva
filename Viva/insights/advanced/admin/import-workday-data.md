---
ROBOTS: NOINDEX,NOFOLLOW
title: Import organizational data from Workday
description: Learn how to set up a connection and import your data from Workday to the Viva Insights advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data from Workday

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of four ways: 

* Through Microsoft Entra ID, which is the default source
* Through a .csv file that you as an Insights Administrator upload
* Through a data import that you, your source system admin, and your Microsoft 365 IT admin set up
* Through a connection between Workday and Viva Insights

This article talks about the fourth option: importing data through a Workday connection.

## Prerequisites

Before you can set up a connection between Workday and Viva Insights, you'll need the following information about your Workday environment from your Workday admin:

* Tenant name
* Username
* Password

## For the first import

If this isn’t the first time you’re importing data from Workday, jump to [For all imports](#for-all-imports).

### Set up your Workday connection

*Applies to: Insights Administrator*

1. In the advanced insights app's admin experience, go to either the **Data hub** or the **Organizational data** page.
    1. On the **Data hub** page, select **Start** under **Data source > Workday**.
    2. On the **Organizational data** page's **Data connection** tab, select **Manage data sources**. Then, select **Start** under **Workday**. 
1. Enter a name for your connection.
1. Under **Set up Workday connection**:
    1. Enter the Workday tenant name, username, and password.
    1. Select how frequently you want Workday to send data to Viva Insights: weekly or monthly.
1. Select the box under **Authorization status** to allow Workday to start sending data to Viva Insights.
1. Read the acknowledgement note and select **Accept**.

## For subsequent imports

If you’ve already set up your connection and imported a first set of data to Workday, follow these steps to update or replace your existing data:

1.	In the advanced insights app's admin experience, go to either the **Data hub** or the **Organizational data** page.
    1. On the **Data hub** page, select **Start** under **Data source > Workday**.
    2. On the **Organizational data** page's **Data connection** tab, select **Manage data** sources. Then, select **Manage** under **Workday**.
2.	Select one option:
    * **Edit authorization or update refresh schedule**. With this option, you can:
        * Allow or stop allowing Workday to send data to Viva Insights.
        * Change the data refresh schedule.
    * **Replace data**. With this option, you can:
        * Overwrite all your existing organizational data with new data from Workday.
        * Remove certain fields by importing data from Workday with fewer fields.
        >[!Caution] 
        >**Replace data** permanently overwrites your existing data.
3.	Select **Next**.

### Edit authorization or update refresh schedule

If you chose **Edit authorization or update refresh schedule**, you’ll arrive at the **Edit Workday connector** page.

1.	Enter your workday credentials: tenant name, username, and password.
2.	If you want to turn on or off Workday’s ability to send data to Viva Insights, select or deselect the checkbox.
3.	If you want to update how often Workday data goes to Viva Insights, use the dropdown menu beneath **Update refresh schedule**.
4.	Read the acknowledgement note and select **Accept**.

### Replace data

If you chose **Replace data**, a popup warning will appear: “Replacing data overwrites all previously ingested data. If your new import is missing any data fields, auto-refresh queries that use those missing fields will be disabled.” If you want to proceed, select **Confirm**.

After you select **Confirm**, a new full refresh of your Workday data will start.

## For all imports

### How Workday sends data to Viva Insights

When you connect Workday to Viva Insights, Workday sends over a set of predefined source columns. These columns are mapped to Viva Insights data fields. You can't change these predefined fields right now, but you'll be able to in the future.

#### Field mapping

The following table shows how Workday fields correspond to Viva Insights fields. For specific details about each Viva Insights field, including data type and formatting requirements, refer to the [Attribute reference in Prepare organizational data](/viva/insights/advanced/admin/prepare-org-data).

|Workday field|Viva Insights field|
|----|----|
|`responseData.worker.workerData.personalData.contactData.emailAddressData`|PersonId
|`responseData.worker.workerData.employmentData.workerJobData.positionData.managerAsOfLastDetectedManagerChangeReference.ID` and `responseData.worker.workerData.workerID`|	ManagerId
|`responseData.worker.workerData.organizationData.workerOrganizationData.organizationData.organizationName`| Organization
|`responseData.worker.workerData.employmentData.workerJobData.positionData.effectiveDate`|EffectiveDate
|`responseData.worker.workerData.employmentData.workerJobData.positionData.jobProfileSummaryData.managementLevelReference.ID`| LevelDesignation
|`responseData.worker.workerData.employmentData.workerJobData.positionData.jobProfileSummaryData.jobFamilyReference.ID`|FunctionType
|`responseData.worker.workerData.employmentData.workerJobData.positionData.jobProfileSummaryData.managementLevelReference.ID`|Layer
|[No mapping from Workday]	| HourlyRate
`responseData.worker.workerData.employmentData.workerStatusData.hireDate`|	HireDate
|[No mapping from Workday]	|SupervisorIndicator
|[No mapping from Workday]	| OnsiteDays
|`responseData.worker.workerData.employmentData.workerJobData.positionData.businessSiteSummaryData.locationReference`|Location


## Validation

After you connect Workday to Viva Insights, the advanced insights app starts validating your Workday data.

After this phase completes, validation has either succeeded or failed. Depending on the outcome, you'll either receive a success status or a failure status in the Import history table on the **Data connections** screen.

For information about what happens next, go to the appropriate section:

- [Validation succeeds](#validation-succeeds)

- [Validation fails](#validation-fails)

### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Processing” status on the **Import history** table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you’ll either find a “Success” or “Validation failed” status in the **Import history** table.

#### Processing succeeds

When you find the “Success” status in the **Import history** table, the import process is complete.

After you receive the “Success” status, you can:

* Select the view (eye) icon to see a summary of the validation results.
* Select the mapping icon to see the mapping settings for the workflow.

#### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. You can try to import your data again.

>[!Note]
>Processing failures are generally due to backend errors. If you’re seeing persistent processing failures and you’ve corrected the data in your import file, log a [support ticket](/microsoft-365/admin/get-help-support) with us.


### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the Workday admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the Workday admin so they know what to correct before sending the data again. 

The data source admin might find the following section helpful to fix data errors in their export file.

#### Guidelines for correcting errors in data

*Applies to: Workday admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until the data source admin fixes the source data. Refer to [File rules and validation errors](rules-validation-errors.md) for specific formatting rules that might help resolve errors you encounter.

Unless you’re updating data for existing employees, keep in mind that **PersonId**, **ManagerId**, **Organization**, and **EffectiveDate** are required for all rows. If you’re *just* updating data for existing employees, **PersonId** and **EffectiveDate** are required for all rows.

>[!Note]
>If you don't enter a value for **EffectiveDate**, Viva Insights will assign the date of upload.

## Related topic

[Prepare organizational data](prepare-org-data.md)

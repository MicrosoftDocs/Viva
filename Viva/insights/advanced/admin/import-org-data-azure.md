---
ROBOTS: NOINDEX, NOFOLLOW
title: Import organizational data with Azure blob import
description: Learn how to import organizational data into Viva Insights through an Azure blob import.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data with Azure blob import  

>[!IMPORTANT]
> This feature is for private preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of five ways: through Microsoft Entra ID, which is the default source; through individual .csv files that you as an Insights Administrator upload directly to Viva Insights; through an API-based import; through Workday; or through an Azure blob import that you, your source system admin, and your Azure contributor set up.

This article covers the fifth option, Azure blob import.

With an Azure blob import, your Azure contributor creates a blob container on the Azure portal, and your source system admin configures a periodic export of a zip file to the blob container’s location. You can then set up Viva Insights to automatically pull organization data from the zip file within this location.

### Workflow

1. Setup:

    1. The Azure contributor creates a SAS URL for a secure blob container on the Azure portal. The blob store location should be secure for sensitive organizational data, and it needs to be set up in the customer’s Azure subscription.

    2. The Azure contributor provides the SAS URL to the Insights admin and source system admin by sharing it in a secure way.

    3. The source system admin prepares the data in a zip file, and configures a periodic export of the file from the HR source system to the blob container.

    4. The Insights admin enters the SAS URL in the Viva Insights app to turn on the import from the Azure blob store location.  

2. Validation: Viva Insights validates the data. (If validation isn’t successful, you can choose from a few options described in [Validation fails](#validation-fails).)

3. Processing: Viva Insights processes the data. (If processing isn’t successful, you can choose from a few options described in [Processing fails](#processing-fails).)

After the data successfully validates and processes, the overall data-import task is complete.

## Setup

### 1. Create blob SAS URL

*Applies to: Azure contributor*

1. Open a browser and sign in to your organization’s Azure portal. 

2. Under **Azure services**, select **Storage accounts**.

3. Under **Storage accounts** at the top left, select **Create** to create a new storage account.

4. Under **Project details**, use the default settings.

5. Under **Instance details**, enter a storage account name and select your region. For Performance and Redundancy, you can use the default settings unless you need to make changes.

6. At the bottom, select **Next: Advanced**.

7. On the Advanced page, make sure that “Require secure transfer for REST API operations” and “Enable storage account key access” are both selected. For “Minimum TLS version,” select at least **Version 1.2**.

8. For all other Advanced settings, you can use the default settings unless you need to make changes.

9. At the bottom, select **Next: Networking**.

10. Under **Network connectivity**, select **Enable public access from all networks**.

11. Under **Network routing**, select your routing preference.

12. At the bottom, select **Next: Data protection**.  

13. On the Data protection page, you can use the default settings unless you need to make changes.

14. At the bottom, select **Next: Encryption**.

15. On the Encryption page, you can use the default settings unless you need to make changes.

16. At the bottom, select **Next: Tags**.

17. Optional: Add tags to the account.  

18. At the bottom, select **Next: Review**.

19. Review your selections. Then, at the bottom left, select **Create**.

20. On the next page, a message will appear that says, “Deployment is in progress.” Once deployment is complete, your storage account and its settings will appear.

21. On the left, under **Data storage**, select **Containers**.

22. To create a new container, at the top, select **Container**. Then, on the right, enter a name for the container, like “hrupload.” At the bottom, select **Create**.

23. When the new storage container you created appears, select it. Then, on the left under **Settings**, select **Shared access tokens**.

24. Under **Signing key** and **Stored access policy**, you can use the default settings. Under **Permissions**, select **Read** and **List**.

25. Under **Expiry**, set a token expiration date of one year from now.  

26. For **Allowed IP addresses** and **Allowed protocols**, you can use the default settings.  

27. Select **Generate SAS token and URL**.

28. Copy and securely share the blob SAS URL with the Insights admin and the source system admin.

### 2. Prepare org data zip file and send to blob store

*Applies to: Source system admin*

**Task 1 - Prepare your data**

Before you start exporting and importing your data, make sure you prepare your file according to steps 1 through 4 in [Prepare an organizational data file upload](./prepare-org-data.md). You can also use this document to learn about required and reserved optional attributes.

Tips for preparing your data

* For new data, include full historical data for all employees.

* Import organizational data for all employees in the company, including licensed and non-licensed employees.

* Refer to the [sample .csv template](https://download.microsoft.com/download/7/a/1/7a17695f-d401-4abd-aeef-e72158084160/OrganizationalDataFileTemplateDataImport.xlsx) for data structure and guidelines to avoid common issues like too many or too few unique values, redundant fields, invalid data formats, and more. [Learn more about file rules and validation errors](./rules-validation-errors.md).

**Task 2 - Export data from your source system and store the zipped folder**

*Required resource: [zipped folder template](https://go.microsoft.com/fwlink/?linkid=2243005) (contains .csv and .json files with required formatting)*

At the frequency you decide (once a month, once a week, etc.) programmatically export organizational data from your source system as a zipped folder. Base this zipped folder on the [one here](https://go.microsoft.com/fwlink/?linkid=2243005). Your zipped folder needs to contain a data.csv file, which contains all the data fields you want to import, and a metadata.json file, which maps how data fields in your source system correspond to the ones in Viva Insights.

Here are a few more details about these files and what they need to contain:

**data.csv**

Add all fields you want to import in this file. Make sure you format it according to our guidelines in [Prepare organizational data](./prepare-org-data.md).

**metadata.json**

Indicate the type of refresh you’re performing and how Viva Insights should map your fields:

* ``` “DatasetType”: “HR” ``` (line 2). Leave this as-is. 

* ``` “IsBootstrap”: ``` (line 3). Use “true” to indicate a full refresh and “false” to indicate an incremental refresh.  

* “Mapping”: If you use names other than what Viva Insights uses, change each column header name to match what you use in your source system.

>[!IMPORTANT]
> Remove any fields that aren’t present in your .csv file.

**Mapping example**

The following example represents one field you’ll find in the metadata.json file:

```
"PersonId": { 
    "name": "PersonId", 
    "type": "EmailType"
```

* ``` "PersonId": { ``` corresponds to the source column name. 

* ``` “name” : “PersonId” ```, corresponds to the Viva Insights field name. 

* ``` "type": "EmailType" ``` corresponds to the field’s data type.

Let’s say that instead of PersonId, your source system uses Employee for this field header. To make sure your fields are mapped correctly, you’ll want to edit the first line below, so it looks like this:

```
"Employee": {
    "name": "PersonId",
    "type": "EmailType"
```
When you upload your data, your Employee field will become PersonId in Viva Insights.

Then, use the steps below to send the organizational data zip file to the blob location created by the Azure contributor in step 1.

1. Open a browser and enter the blob SAS url provided to you by the Azure contributor.  

2. At the top, select **Upload**. Then, on the right, upload the zip folder you created using the instructions above.

### 3. Set up Viva Insights to import data from the blob location

*Applies to: Insights admin*

1. Start the import from one of two places: the **Data hub** page, or the **Organizational data** page under **Data connections**.

    1. From **Data hub**:
        1. In the **Data source** section, under **Azure blob import**, select **Start**.

    2. From **Data connections**:
        1. Next to **Current source**, select **Manage data sources**.
        1. An Azure blob import window appears. Select **Start**.

2. Under **Connection name**, enter a unique name for the import.

3. Under **Blob SAS URL**, enter the URL for the import provided to you by the Azure contributor in Step 1.

### 4. Validation

*Applies to: Insights admin*

After the source system admin exports the data and you set up the import, the app starts validating. In most cases, file validation should complete quickly.

After this phase completes, validation has either succeeded or failed. Depending on the outcome, you’ll either receive a success status or a failure status in Import history table in **Organizational data > Data connections**.

For information about what happens next, go to the appropriate section:

* [Validation succeeds](#validation-succeeds)
* [Validation fails](#validation-fails)

#### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Processing” status on the **Import history** table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you’ll either find a “Success” or “Failed” status in the **Import history** table.

##### Processing succeeds

When you find the “Success” status in the **Import history** table, the upload process is complete.

After you receive the “Success” status, you can:

* Select the view (eye) icon to see a summary of the validation results.
* Select the mapping icon to see the mapping settings for the workflow.

>[!Note]
> Each tenant can have only one import in progress at a time. You need to complete the workflow of one data file, which means you either guide it to a successful validation and processing or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the **Data connections** tab.

##### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. For processing to succeed, the source system admin needs to correct errors and push the data to Viva Insights again.

>[!Note]
> Processing failures are generally due to backend errors. If you’re seeing persistent processing failures and you’ve corrected the data in your imported file, [log a support ticket with us](/microsoft-365/admin/get-help-support).

#### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the source system admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the source system admin so they know what to correct before sending the data again.

The source system admin might find the following section helpful to fix data errors in their export file.

#### About errors in data
*Applies to: Source system admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until the data source admin fixes the source data.

Refer to [Prepare organizational data](./prepare-org-data.md) for specific formatting rules that might help resolve errors you encounter.

Here are a few import-specific errors you might encounter if your files aren't formatted correctly:

* There is a problem with the files in the .zip file. Make sure the .zip file contains only one .json file and one .csv file and upload it again.

* The .csv file in your .zip file is empty. Add a non-empty .csv file and upload the .zip file again.

* The .json file in your .zip file is empty. Add a non-empty .json file and upload the .zip file again.

* The content in the .json file isn't mapped to a supported data type. Map the content to a supported data type and upload the .zip file again.

* The .json file is invalid. Please use a valid .json file and upload the .zip file again.

* The header names in the .csv file don’t match the fields you mapped in the .json file. Make sure the .json file contains the same fields as the .csv file, and upload the .zip file again.

* The number of headers in the .csv file doesn't match the fields you mapped in the .json file. Make sure the .json file contains the same fields as the .csv file, and upload the .zip file again.

* Your .csv file is mapped to a null or empty field in your .json file. Map it to a non-empty field and upload the .zip file again.

[Learn about other file rules and validation errors](./rules-validation-errors.md).

### Manage data source and make changes
*Applies to: Insights admin*

After you've set up your data import, use the steps below to make changes like setting a new blob store URL, or turning off automated imports.

1. On the **Organizational data** page under **Data connections**, select **Manage data sources**.
2. Under **Azure blob import**, select **Manage**.

On the next page, you can edit the connection name, or the blob SAS URL. If you update the SAS URL, the new location will be used for future data refreshes.

You can also turn automated imports on or off. When you’re done, select **Save**.

To replace or edit the organizational data using the existing blob SAS URL, contact your source system admin. When you import data to Viva Insights, you’ll either perform a full or an incremental refresh. If you want to delete fields, you can use a full refresh to do so.

#### How to indicate a full or incremental refresh

1. In metadata.json, go to line 3.
1. Update the ``` “IsBootstrap”: ``` property to one of the following:
    1. For a full refresh, use ``` “IsBootstrap” : “true” ```.
    1. For an incremental refresh, use ``` “IsBootstrap” : “false”```.

When your import/export option runs, Viva Insights will start to process your data either as a full or incremental refresh, depending on what you specified here in metadata.json.

>[!IMPORTANT]
> Make sure you delete any fields from metadata.json that you're not including in your data.csv file. If you have more fields in your metadata.json file than in your data.csv file—or vice versa—processing for your import will fail. Refer to [Prepare, export, and import organizational data](./prepare-org-data.md) to learn more about metadata.json and how to use it to map fields.

#### Refresh types

**Full**

When you perform a full refresh, you’re replacing all your organization’s data in Viva Insights—that is, you overwrite what you’ve already imported. When you perform a full refresh, make sure to provide data for all licensed and unlicensed employees (meaning those who have a Viva Insights subscription and those who don’t). We describe what fields to provide later in this article.

You can use a full refresh to delete fields, because fields you leave out won’t show up in your data. We talk about deleting data in the next section.

**Deleting fields with full refreshes**

To delete fields with a full refresh, export your data as a .csv that contains all fields except the fields you want to delete. Because a full refresh replaces existing data, you’ll end up with every field except the ones you left out during the import.

**Incremental**

Perform an incremental refresh when you only want to add some new information to organizational data you’ve already uploaded to Viva Insights. Here’s what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes 

Here are a couple of examples of when you might perform an incremental refresh:

**Example – adding new hires**

Say you want to add five new hires to your organizational data. During the import, you’d include:

* Five rows that contain new employee data.
* Required attributes: PersonId,  ManagerId, Organization, and EffectiveDate.
* All reserved optional fields (for example, HireDate) that you’ve already imported to Viva Insights. 

After the import finishes, the only change you’d notice is five new rows and their values.

**Example – adding a new attribute**

Maybe you want to add an optional reserved attribute that wasn’t in your data before—let’s say **Location**—for all existing employees. When you go to import your data, you’d only include the **Location**, **PersonId**, and **EffectiveDate**, with current and historical values for each employee, in your .csv file. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, **Location**.

#### Fields to include in data.csv for full and incremental refreshes

For the refresh types listed below, include the fields in the following table within your data.csv file. Make sure you:

* Format these fields according to our guidelines in [Prepare organizational data](./prepare-org-data.md).
* Remove any fields you're not including from your metadata.json file.
* Keep both the data.csv and metadata.json files in your one zipped folder.

| For this kind of refresh | Include these fields in data.csv | With these values | For these employees |
|----|----|----|----|
| **Full** | PersonId | Current </br> <br> All historical | All | 
|   | ManagerId | Current </br> <br> All historical | All |
|   | Organization | Current </br> <br> All historical | All |
|   | EffectiveDate | Current </br> <br> All historical | All |
|   | All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights | Current </br> <br> All historical | All |
| **Full** (for deleting reserved optional fields) | PersonId | Current </br> <br> All historical | All | 
|   | ManagerId | Current </br> <br> All historical | All |
|  | Organization | Current </br> <br> All historical | All |
|   | EffectiveDate | Current </br> <br> All historical | All |
|   | All reserved optional fields (for example, **HireDate**) you’ve already imported to Viva Insights, except the reserved optional fields you want to delete | Current (except for to-be-deleted fields) </br> <br> All historical (except for to-be-deleted fields) | All |
| **Incremental** (for adding new fields or editing existing fields, but *not* adding new employees) | PersonId | Current </br> <br> All since the last upload (refer to note below) | All |
|   | EffectiveDate | Current </br> <br> All since the last upload (refer to note below) | All |
|   | Any reserved optional fields (for example, **HireDate**) you want to add | Current </br> <br> All since the last upload (refer to note below) | All |
| **Incremental** (for adding new employees) | PersonId | Current </br> <br> All since the last upload (refer to note below) | New employees only |
|   | ManagerId | Current </br> <br> All since the last upload | New employees only |
|  | Organization | Current </br> <br> All since the last upload | New employees only |
|   | EffectiveDate | Current </br> <br> All since the last upload | New employees only |
|   | All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights | Current </br> <br> All since the last upload | New employees only |

>[!Note]
> "All historical": Values for previous time periods. For example, if you include monthly data, then you'd include values for every month leading up to this one. When you’re first starting to use Viva Insights, 13 months’ worth of data is recommended. After that, it’s recommended to update data regularly so it builds into 27 months’ worth of data. </br> <br>
> "All values since the last upload": Values for the period between uploads. For example, if the last upload was in March and now it’s July, include values for April, May, and June.

## Related topics

[Prepare organizational data](prepare-org-data.md)
---
ROBOTS: NOINDEX,NOFOLLOW
title: Import organizational data from Workday
description: Learn how to set up a connection and import your data from Workday to the Viva Insights advanced insights app
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

# Import organizational data from Workday

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of four ways: 

* Through Azure Active Directory, which is the default source
* Through a .csv file that you as an Insights Administrator upload
* Through a data import that you, your source system admin, and your Microsoft 365 IT admin set up
* Through a connection between Workday and Viva Insights

This article talks about the fourth option: importing data through a Workday connection.

## Prerequisites

Before you can set up a connection between Workday and Viva Insights, you'll need the following information about your Workday environment from your Workday admin:

* Tenant name
* Username
* Password

## Set up your Workday connection

*Applies to: Insights Administrator*

1. In the advanced insights app's admin experience, go to either the **Data hub** or the **Organizational data** page.
    * On the **Data hub** page, select **Start** under **Data source > Workday connector**.
    * On the **Organizational data** page's **Data connection** tab, select **Manage data sources**. Then, select **Start** under **Workday connector**. 
1. Enter a name for your connection.
1. Under **Set up Workday connection**:
    1. Enter the Workday tenant name, username, and password.
    1. Select how frequently you want Workday to send data to Viva Insights: weekly or monthly.
1. Select the box under **Authorization status** to allow Workday to start sending data to Viva Insights.
1. Select **Save**.

### How Workday sends data to Viva Insights

When you connect Workday to Viva Insights, Workday sends over a set of predefined source columns. These columns are mapped to Viva Insights data fields. You can't change these predefined fields right now, but you'll be able to in the future.

## Validation

After you connect Workday to Viva Insights, the advanced insights app starts validating your Workday data.

In most cases, file validation should complete quickly. If your organizational data file is large, validation could take up to one or two minutes. After this phase completes, validation has either succeeded or failed. Depending on the outcome, you’ll either receive a success notification or a failure notification in the top-right corner of the **Data connections** screen.

For information about what happens next, go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Processing” status on the **Import history** table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you’ll either find a “Success” or “Validation failed” status in the **Import history** table.

#### Processing succeeds

When you find the “Success” status in the **Import history** table, the import process is complete.

After you receive the “Success” status, you can:

* Select the view (eye) icon to see a summary of the validation results.
* Select the mapping icon to see the mapping settings for the workflow.

#### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. For processing to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. If you’ve corrected all errors and are still getting a “Processing failed” status, file a support ticket with us.

### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the Workday admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the Workday admin so they know what to correct before sending the data again. 

The data source admin might find the following section helpful to fix data errors in their export file.

#### Guidelines for correcting errors in data

*Applies to: Workday admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until the data source admin fixes the source data. In this section, we go over some rules about the source file that might help resolve errors. For more information about preparing data, refer to [Prepare organizational data](prepare-org-data.md).

##### Rules for the file

The data file needs to be in the .csv format, and it can't be empty.

##### Rules for field headers

All field header or column names need to:

* Contain a value.
* Be unique—that is, two column names can’t be the same.
* Begin with a letter (not a number).
* Only contain alphanumeric characters (letters and numbers, for example, **Date1**). 
* Have no leading or trailing blank spaces or special characters (those that are non-alphanumeric, like *@*, *#*, *%*, *&*). You’ll get an error if your column name contains a formula.

##### Rules for field values

All rows need to contain the following fields:

* **PersonId**
* **ManagerId** (unless the import is an update for existing employees only) 
* **Organization** (unless the import is an update for existing employees only)
* **EffectiveDate** 

    >[!Note]
    >If you don’t enter a value here, Viva Insights will assign the date of upload as the **EffectiveDate**.

Some field values need to follow specific formatting, as described in this table:

|Field | Format |Example
|------|--------|------|
|**EffectiveDate** | MM/DD/YYYY | `01/15/2023`
|**HireDate** | MM/DD/YYYY | `01/15/2023`
|**PersonId** | Valid email address| `gc@contoso.com`
|**ManagerId** | Valid email address |`gc@contoso.com`
|**Layer** | Numbers only | `5`
| **HourlyRate** (refer to note below) | <ul><li>Numbers only <li>Double| `23.75`

>[!Note]
>The app doesn't currently perform currency conversions for **HourlyRate** data. All calculations and data analysis assumes the data to be in US dollars.


##### Rules for characters in field values

The following field rules apply to characters in field values:

* Double-byte characters, such as Japanese characters, are permitted in the field values.
* The maximum character length of field values in rows is 128 KB, which is about 1024 x 128 characters.
* “New line” (\n) characters are not permitted in field values. 

## Related topic

[Prepare organizational data](prepare-org-data.md)

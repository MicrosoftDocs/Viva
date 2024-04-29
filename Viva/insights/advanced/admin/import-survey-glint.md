---
ROBOTS: NOINDEX, NOFOLLOW
title: Import survey results from Glint
description: Learn how to set up a connection between Glint and Viva Insights and import your data to the advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import survey results from Glint

In this article, we discuss how to import survey results from Glint to Viva Insights, like:

* Employee-level survey data
* Survey responses, question texts
* Question labels
* Categories
* Survey names
* Rating scales
* Survey closed date

>[!Important]
>If this isn't the first time you're importing survey data, jump to [For all imports](#for-all-imports).

## For the first import

The first time you as the Insights Administrator import survey results into Viva Insights, you'll need to coordinate a few tasks to get a Glint app set up in your tenant. Then, you can start your import.

### Workflow

1.	The *Microsoft 365 admin* [installs the Glint](#install-the-app) app on the Azure portal.
2.	You as the *Insights admin* [set up the import](#set-up-a-new-import-in-viva-insights) in the advanced insights app.
3.	The *Glint admin* [sends survey data](#send-data-from-glint) to Viva Insights.
4. Viva Insights validates and processes the data.

### Install the app

*Applies to: Microsoft 365 admin*

1.	Provide consent to the import application:
    1. Access the admin consent portal at this link: Admin consent.
    1. Enter your admin username and password, and then select Accept.
2.	Find and share the Glint-Viva Insights import app:
    1. In **Enterprise Applications**, search for **spi-glint-vi-ingress-prod**. The application ID is **519483bc-2c8f-451b-89d5-b19a221a4fa9**.
    1. Share the application ID with the Insights admin, so they can enter it in the advanced insights app.

### Set up a new import in Viva Insights

*Applies to: Insights admin*

1.	Set up a new import in one of two places: through the **Data hub** page or through the **Survey data** page.
    1. Through **Data hub**:
        1. Under the **Data sources** pane on the right, go to **Survey data import** in the **Survey sources section**.
        1. Select **Start**.
    1. Through **Survey data**:
        1. Next to **Select source: Glint**, select **Manage data sources**.
2.	If your Glint tenant uses the default app ID, you'll notice the app ID prefilled in the App ID field. If your Glint tenant doesn't use the default app ID, enter the app ID from the app registration process.

    >[!Note]
    >If you don't have this ID, contact your Microsoft 365 admin or Privileged Role Administrator.
3.	Select **Save**. Your import is now set up and ready to get data from Glint. Reach out to the Glint admin so they can start their export.

## For all imports

### Send data from Glint

*Applies to: Glint admin*

After the app is set up and the connection is ready in the advanced insights app, the Glint admin can push survey data to Viva Insights.

1.	Sign in to the Glint admin portal. 
2.	Select **Get Started** under **Send data to Viva Insights**. 
3.	Allow Glint to send data to Viva Insights by selecting **Authorize**. 
4.	Select which survey programs to send. 

>[!Note]
>For this private preview, you can only send ad-hoc and recurring surveys.  

After Glint sends the data, a success message appears. 

### Validate and process

After the Glint admin sends data, the advanced insights app starts validating the import.

After this phase completes, validation has either succeeded or failed. Depending on the outcome, the **Import history** table on the **Data connections** tab will either show “Validated, processing” or "Validation failed."

For information about what happens next, go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

#### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Processing” status on the Import history table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you’ll either find a “Validated, processing” or “Validation failed” status in the Import history table.

##### Processing succeeds

When you find the “Success” status in the **Import history** table, the upload process is complete.

After you receive the "Success" status, you can select the view (eye) icon to see a summary of the validation results.

##### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. If you want to try running the import again, have the Glint admin resend their survey data. If you’re still getting a “Processing failed” status, file a support ticket with us.

#### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the Glint admin so they know what to correct before sending the data again.

The Glint admin might find the following section helpful to fix data errors in their export file.

##### About errors in data

*Applies to: Glint admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until you fix the source data. After you fix the source data, you'll need to push the survey again to Viva Insights.

###### Survey error reference

You might get an error if the file:

* Is empty.
* Isn't in .csv format.
* Contains duplicate question labels.
* Is missing a question label.
* Has a question label with invalid characters.
* Has a question label that begins with a number.
* Has a response value that exceeds 128KB.
* Has a response value with a “new line” (/n) character.

You might also get an error if there's an issue with connection setup.

## Viewing information in the Data quality tab

The **Data quality** tab shows you the following information for each imported survey:

* **Question labels** – All the attributes provided by your organization in the organizational data upload file. When analysts run the Viva Insights with Glint Power BI query, they can filter and group employees in the organization by these question labels, so being familiar with them will give you insight into the types of queries to use for analysis.
* **Quality score** – The percentage of measured employees who have a non-blank value for the specified question label. This score is intended as guidance, not to be an absolute measure of quality. A quality score of more than 95% leads to better-quality insights. If quality scores are low, it's difficult to determine how people collaborate across different characteristics. 
* **Last updated** – When the survey was sent to Viva Insights.
* **Employees with this field** – The number of measured employees and internal collaborators with a non-blank value for the question label.
* **Unique values** – The count of the unique attribute values included in the data. For example, if a Work-life balance question label contains response values from 1 to 5, its unique values count is five.

---
title: Import survey results from Viva Glint into Viva Insights
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

# Import survey results from Viva Glint into Viva Insights (preview)

>[!IMPORTANT]
> This feature is in public preview. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

*Applies to: Viva Insights admin, Viva Glint admin*

This article discusses how to import survey results – employee-level survey responses, question texts, question labels, categories, survey names, rating scales, and survey closed date – from Viva Glint into Viva Insights.

Through this process, your company can get a more complete picture around the employee experience, by combining data around how employees feel (Viva Glint) with how employees work (Viva Insights).

**Workflow**

1. The **Viva Insights admin** sets up a new import in the advanced insights app.

2. The **Viva Insights admin** contacts the **Viva Glint admin** to share Viva Glint survey data, and the **Viva Glint admin** selects specific survey programs and sends the data to Viva Insights.

3. **Viva Insights** validates and processes the data so it’s ready for use.

### 1. Set up a new import in the advanced insights app

*Applies to: Viva Insights admin*

1. You can set up a new import in one of two places: through the **Data hub** page or through the **Survey data** page.

    1. Through **Data hub**:
        1. Under the **Data sources** pane on the right, go to **Viva Glint** in the **Survey data sources** section.
        1. Select **Manage**.
    2. Through **Survey data**:
        1. Select **Source: Viva Glint**. 

2. You’ll be prompted to contact the Viva Glint admin, who needs to select specific survey programs and share it with Insights.

### 2. Send data from Viva Glint 

*Applies to: Viva Glint admin*

Contact your Viva Glint admin, who will use [these steps](/viva/glint/setup/insights-integration) to share Viva Glint survey data with Viva Insights.

### 3. Data validation and processing 

*Applies to: Viva Insights admin, Viva Glint admin*

#### Validation

After the Viva Glint admin sends data, the advanced insights app starts validating the import.

After this phase completes, validation either succeeds or fails. Depending on the outcome, you’ll see “Validated, processing” or “Validation failed” on the **Import history** table on the **Data connections** tab.

For information about what happens next, go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

##### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Validated, processing” status on the **Import history** table.

After processing completes, depending on the outcome, you’ll see “Success” or “Validation failed” status in the **Import history**.

##### Processing succeeds 

When you see the “Success” status in the **Import history** table, the upload process is complete.

After you receive the “Success” status, you can select the view (eye) symbol to see a summary of the validation results.

:::image type="content" source="../images/glint-survey-data-processing.png" alt-text="Screenshot that shows processing succeeds for survey import.":::

##### Processing fails 

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. If you want to try running the import again, have the Viva Glint admin resend their survey data. If you’re still getting a “Processing failed” status, [file a support ticket with us](/microsoft-365/admin/get-help-support).

##### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. Under **Actions**, select the download symbol to download an error log.

For validation to succeed, the Viva Glint admin needs to correct the errors and push the data to Viva Insights again.  Send the error log to the Viva Glint admin so they know what to correct before sending the data again.

The Viva Glint admin can use this section to fix data errors in their export file.

#### About errors in data 

*Applies to: Viva Glint admin*

When any data row or column has an invalid value for any attribute, the entire import  fails until the source data is fixed. After fixing the source data, push the survey again to Viva Insights.

##### Survey error reference

You might get an error if the file: 

* Is empty.
* Isn't in .csv format.
* Contains duplicate question labels.
* Is missing a question label.
* Has a question label with invalid characters.
* Has a question label that begins with a number.
* Has a response value that exceeds 128KB.
* Has a response value with a “new line” (/n) character. 

You might also get an error if there's an issue with the connection setup.

### View survey information in the Data quality tab

*Applies to: Viva Insights admin*

The **Data quality** tab shows you the following information for each imported survey:

* **Data fields** – The question labels for your survey.
* **Quality score** – The percentage of measured employees who have a non-blank value for the specified question label. This score is intended as guidance, not to be an absolute measure of quality. A quality score of more than 95 percent leads to better-quality insights. If quality scores are low, it's difficult to determine how people collaborate across different characteristics.
* **Last updated** – When the survey was sent to Viva Insights.
* **Employees with this field** – The number of measured employees and internal collaborators with a non-blank value for the question label
* **Unique values** – The count of the unique attribute values included in the data. For example, if a **Work-life balance question label** contains response values from 1 to 5, its unique values count is five.

:::image type="content" source="../images/glint-survey-data-quality.png" alt-text="Screenshot that shows the survey data quality tab.":::

### Delete Glint survey data 

*Applies to: Viva Glint admin*

Follow [these steps](https://go.microsoft.com/fwlink/?linkid=2271365) to delete any Viva Glint survey data that was imported into Viva Insights.

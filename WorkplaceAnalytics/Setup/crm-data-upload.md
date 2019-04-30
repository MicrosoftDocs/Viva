---
# Metadata Sample
# required metadata

title: Prepare and upload CRM data in Workplace Analytics
description: How to prepare and upload CRM data in Workplace Analytics 
author: madehmer
ms.author: v-midehm
ms.date: 04/29/2019
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# CRM data in Workplace Analytics

You can now upload your company's Customer Relationship Management (CRM) data into Workplace Analytics. Data from Salesforce or Dynamics CRM typically includes customer account information, sales records, purchasing history, service history, and product inquiries.

Workplace Analytics can combine your CRM data with other organizational (HR) and Office 365 data for more advanced collaboration and productivity analysis in Workplace Analytics queries. For more complete analysis, Workplace Analytics requires the following CRM data:

* Customer accounts
* Customer contacts
* Sales opportunities
* Sales assignments

When exporting and uploading the data into Workplace Analytics, you can choose what data gets uploaded in what way, such as hashed versions of any sensitive or private information or even excluding it.

## Import tasks

- [CRM data in Workplace Analytics](#crm-data-in-workplace-analytics)
  - [Import tasks](#import-tasks)
    - [Decide what data you need](#decide-what-data-you-need)
    - [Prepare the CRM source data](#prepare-the-crm-source-data)
      - [Required and optional attributes](#required-and-optional-attributes)
    - [CRM data rules](#crm-data-rules)
  - [Upload, validate, and process the CRM data](#upload-validate-and-process-the-crm-data)
  - [Related topics](#related-topics)

The first time you open the CRM data page, it’ll prompt you to start a new upload.

   ![First CRM data upload](../images/wpa/setup/crm-first-upload.png)

After your first upload  of CRM accounts and contacts data, the CRM data page  will show a list of “Data uploads,” as follows.

   ![Subsequent CRM data uploads](../images/wpa/setup/crm-upload.png)

### Decide what data you need

Similar to other organizational data, it’s important to know what CRM data you need to upload for more complete analysis in Workplace Analytics. The more data you share with Workplace Analytics, the more in-depth, advanced analysis you’ll be able to get.

### Prepare the CRM source data

To help prepare the CRM data, you can download and use the template provided on the **Upload Start** page in Workplace Analytics. You must save your CRM data files as **CSV UTF-8** files in Excel before you can upload them into Workplace Analytics.

   ![CRM data template](../images/wpa/setup/crm-tips.png)

The validity thresholds are predetermined by Workplace Analytics for the attribute values in the uploaded CRM data. These are the percentage of rows in the upload file that must have a valid, non-null value for the attribute. The source file might still be valid even if some rows have invalid or missing values for some columns.

#### Required and optional attributes

To get full functionality from Workplace Analytics, you’ll need to include the following *required attributes* in a CRM Accounts and Contacts upload for data analysis in Workplace Analytics. You can also include optional attributes that might help filter and group data for more in-depth analysis in Workplace Analytics.

The following **Required attributes** must match the exact column headers (case sensitive) in the .csv upload:

|Source column in CSV |Required attribute |Data type |
|------|-----------|----------|
|Account ID |AccountId |String |
|Account Name |AccountName |String |
|Account Owner Email |AccountOwnerEmail |Email |
|Effective Date |AccountsStartDate |DateTime |
|Contact   ID  |ContactId |String |
|Contact Name |ContactName |String |
|Contact Email |ContactEmail |Email |
|Contact Date |ContactStartDate |DateTime |

The following is a sample list of **Optional attributes** for customer accounts and contacts that you can include in the upload.

|Source column in CSV |Optional attribute |Data type |
|------|-----------|----------|
|Parent Account |AccountName |String |
|Parent Account ID |AccountId |String |
|Type |AccountType |String |
|Industry |AccountIndustry |String |
|Annual Revenue |AccountAnnualRevenue |Double |
|Website |AccountWebsite |String |
|Account Created Date |AccountCreatedDate |DateTime |
|Account Last Modified Date |AccountLastModifiedDate |DateTime |
|Revenue |AccountRevenue |Double |

> [!Note] 
> * All DateTime values must be in the MM/DD/YYYY 12:12PM format.
> * Numerical fields (such as "HourlyRate") must be in the "number" format and cannot contain commas or a dollar sign.

### CRM data rules

Confirm the CRM data file follows the same rules you applied when creating the Organizational data upload file. For more details, see Organizational data rules  and Attribute notes and recommendations.

## Upload, validate, and process the CRM data

1. In **Settings** > **Upload** > **CRM data**, select **New upload**.
2. Download and use the template provided in the **Tips** section.
3. In the **Data source** section, select the applicable source for the upload, such as **Salesforce** or **Dynamics CRM**.
4. In the **Data type** section, select the type of CRM data you want to upload. You can upload only one of the following types of data files at a time. However, you can wait until you’ve uploaded all the files you need, before submitting the data for validation.
   * Accounts
   * Contacts
   * Opportunities
   * Seller assignments
5. In the **Select file** section, select the source (.csv) file that corresponds with the data type selected in the previous step. You can select **Download a .csv template** to help with file requirements.
6. Select More options to change the default Append selection to the Delete and add new option:

   * To preserve previously uploaded data and incrementally append it with new data, keep the default selection of **Append new records**.
   * To remove and replace existing data with this new data, select **Delete all old records and add new records**.

7. In the Create an upload name section, type a name and a description for your upload, and then select **Next**.
8. In the **System fields** section, confirm or change the following:

   * In **Source** column  in CSV, select the applicable field name that corresponds with the name in the Workplace Analytics attribute column for each of the fields in the uploaded .csv files.
   * In **Data type**, confirm the data in the file matches the specified data type. For example, the Account Owner Email value must be a valid email in each row for this column in the upload file. These fields are read-only on this page. 
   * In **Report options**, you can change this setting to one of the following only for optional or custom attributes. This setting is read-only for the required attributes.
     * **Include in report** includes the data in reports generated by queries.
     * **Exclude from report** excludes data from reports that are generated by queries.
     * **Hash in report** includes de-identified or a hashed version of the data in reports generated by queries.
   * In First row from uploaded file, you can confirm the field mapping is correct with this read-only column, which shows the value of the first row of data in the file.
9. In the **Custom fields (optional)** section, you can add any additional custom fields that Workplace Analytics was not able to map for you in the **System fields** section, and then map the applicable columns and other options accordingly.
10. Select **Next**.
11. On the summary page, confirm the file details, and then select **Submit**.
12. The new upload will be listed in the Data Uploads section with a status of Validating, which might take a few minutes.
13. When the status changes to Validated, Ready to process: 
    * If you have more CRM files to upload, select Upload and go back to Step 2 and repeat these steps until you’ve uploaded all the applicable CRM files.
    * After all applicable CRM files are validated, select Turn on processing to save the data and get it processed in Workplace Analytics. 
14. Other possible statuses and options:
    * **Processed** - this status means the data was successfully saved.
    * **Validation failed** - this status means the data couldn’t be validated because something went wrong with the upload.
    * **Processing failed** - this status means the data could not be saved or processed due to an error.
    * **Abandoned** - this status means you tried to upload a file of the same data type (such as accounts) two or more times before the processing completed on the first upload. When this occurs, Workplace Analytics will abandon the previous uploads and will try to validate the last upload of the same data type.
    * **Download log** - select to see a detailed list of issues that caused the failure.
    * **Mapping** – select to see the field mappings . If they’re not set correctly, you’ll need to correct them in the .csv file and repeat the upload steps with the new file.
    * **Records created** – after a file’s status changes to Processed, you can select this to see the number of new records that were created with the upload.


## Related topics

* [Prepare organizational data](Prepare-organizational-data.md)
* [First organizational upload](upload-organizational-data-1st.md)
* [Subsequent organizational uploads](upload-organizational-data.md)
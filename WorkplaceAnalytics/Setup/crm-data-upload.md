---

title: Prepare and upload CRM data in Workplace Analytics
description: How to prepare and upload CRM data in Workplace Analytics
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
--- 

# CRM data in Workplace Analytics

You can now upload your company's Customer Relationship Management (CRM) data into Workplace Analytics. Data from Salesforce or Dynamics CRM typically includes customer account information, sales records, purchasing history, service history, customer requests, and product inquiries.

Workplace Analytics can combine your CRM data with your organizational (HR) and Microsoft 365 data for more advanced collaboration and productivity analysis in Workplace Analytics queries. For the most complete analysis, Workplace Analytics requires the following CRM data:

* Customer accounts
* Customer contacts
* Seller assignments

You can use this data to help analyze customer history to maintain and improve business relationships with existing customers and drive sales growth with new customers.

**Import tasks**

  - [Decide what data you need](#decide-what-data-you-need)
  - [Prepare the CRM source data](#prepare-the-crm-source-data)
    - [Required and reserved attributes](#required-and-reserved-attributes)
    - [CRM data rules](#crm-data-rules)
  - [Upload, validate, and process the CRM data](#upload-validate-and-process-the-crm-data)

The first time you open the CRM data page, it’ll prompt you to start a new upload.

   ![First CRM data upload](../images/wpa/setup/crm-first-upload.png)

After your first upload of CRM accounts and contacts data, the CRM data page will show a list of “Data uploads,” as follows.

   ![CRM data uploads](../images/wpa/setup/crm-upload-c.png)

## Decide what data you need

Similar to other organizational data, it’s important to know what CRM data you need to upload for more complete analysis in Workplace Analytics. The more data you share with Workplace Analytics, the more in-depth, advanced analysis you’ll be able to get.

When exporting and uploading the data into Workplace Analytics, you can choose what data gets uploaded in what way, such as hashed versions of any sensitive or private information or by excluding it, if necessary.

Examples of CRM data include: customer account history, contact information, and seller assignments. Workplace Analytics requires this data at the individual level, which means that these attributes provide context to each account or contact in the dataset.

You can use this data to analyze sales collaboration between your internal sales organization and the sales accounts and contacts that they manage and other performance outcome data.

It's best to include all accounts and contacts as part of your data upload, even if you plan to gather data for only a subgroup or specific target population within the data.

For example, if you want to create reports to show the seller assignments or contacts for your salespeople in Workplace Analytics, you'll need to upload files for accounts, contacts, and assignments.

## Prepare the CRM source data

After you’ve identified what CRM data you want to upload, you need to export it into the correct format required by Workplace Analytics. To help prepare the source data, download and use the template provided on the **Upload Start** page in Workplace Analytics, which includes instructions, the required and reserved attribute headings, and example data. You must save your CRM data files as **CSV UTF-8** files in Excel before you can upload them into Workplace Analytics.

   ![CRM data template](../images/wpa/setup/crm-upload.png)

The validity thresholds are predetermined by Workplace Analytics for the attribute values in the uploaded CRM data. These are the percentage of rows in the upload file that must have non-null values (no blanks) for the attribute. The source file might still be valid even if some rows have missing values for some columns. The required attributes are set at 100%, which means every row must have non-null values for these columns in the file. This setting is not intended to check or allow for invalid values. A single invalid value, such as an incorrect data type, email address, or TimeZone string will cause the file upload to fail.

### Required and reserved attributes

To get full functionality from Workplace Analytics, you’ll need to include the following *Required attributes* in each CRM upload (first and subsequent). Optionally, you can also include *Reserved* and *Custom* attributes that can help filter and group data for more in-depth analysis in Workplace Analytics.

The following **Required attributes** must match the exact column headings (case sensitive) in the .csv upload:

|Source column in CSV |Required attribute |Data type |
|------|-----------|----------|
|**Accounts data**     |
|Account ID or Number|AccountId |String |
|Account Name |AccountName |String |
|Effective Date |AccountsStartDate |Date |
|**Contacts data**           |
|Account ID or Number |ContactsAccountId |String |
|Contact ID or Number |ContactId |String |
|Email |ContactEmail |Email |
|Effective Date |ContactsStartDate|Date |
|**Seller assignments data**           |
|Account Number |SellerAssignmentAccountId |String |
|Effective Date |SellerAssignmentStartDate |Date |
|Account Owner |SellerEmail |Email |

The following is a sample list of **Reserved attributes** that you can optionally include in the upload.

|Source column in CSV |Optional attribute |Data type |
|------|-----------|----------|
|**Accounts data** |
|Account Owner Email |AccountOwnerEmail |Email |
|Parent Account |ParentAccountName |String |
|Parent Account ID |ParentAccountId |String |
|Relationship Type |AccountType |String |
|Industry |AccountIndustry |String |
|Annual Revenue |AccountAnnualRevenue |Double |
|Website |AccountWebsite |String |
|Account Created Date or Created On |AccountCreatedDate |Date |
|Account Last Modified Date or Modified On |AccountLastModifiedDate |Date |
|Revenue |AccountRevenue |Double |
|**Contacts data** |
|First Name |ContactFirstName |String |
|Last Name |ContactLastName |String |
|Business Phone |ContactPhone |Number|
|Job Title |ContactTitle |String |
|**Seller assignments data** |
|Role |SellerStandardTitle |String |
|Region |SellerRegion |String |

> [!Note]
> * Field values cannot contain commas or other special characters.
> * All Date values must be in the MM/DD/YYYY format.
> * Numerical fields (such as "Revenue") must be in the "number" format and cannot contain commas or a dollar sign. For more details, see [Use only valid values and formats](prepare-organizational-data.md#attribute-reference).

The **AccountsStartDate** is required to help capture a historical snapshot of your CRM data. These  help ensure accuracy of analyses that span the time frames in which changes can occur in your CRM system. For example, in your CRM system, consider an Account with AccountName “Contoso” and AccountID “123” which is created on 01-Jan-2019 and the name is changed to “Contoso Corp” in the system on 01-April-2019. This change will show as a new record with the new AccountsStartDate and AccountName. For example:

|AccountID |AccountName |AccountsStartDate |AccountIndustry |
|------|-----------|----------|----------|
|123 |Contoso |01/01/2020 |Software tech|
|123 |Contoso Corp |04/01/2019 |Software tech|

Let’s say an external collaborator is matched as a contact for this account. Any analysis involving that contact which is performed on a time frame prior to 01-Apr-2019 would use the first record and set of attribute values (where AccountsStartDate = “01-Jan-2019”). Any analysis for a time frame that is after 01-Apr-2019, which would use the second record and set of attribute values, where AccountsStartDate = “01-Apr-2019”.

> [!Note]
> If only one **AccountsStartDate** is provided, all associated attribute values (such as AccountID, AccountName, and AccountIndustry values for the following example) are used for analysis performed over any time frame.

|AccountID |AccountName |AccountsStartDate |AccountIndustry |
|------|-----------|----------|----------|
|123 |Contoso |01/01/2020 |Software tech|

### Custom attributes

Custom attributes in the CRM upload are not mapped by default to any Required or Reserved attributes. You can include these optional attributes in the CRM upload with custom attribute names and data types in Workplace Analytics.

If any of the Custom fields can be mapped to Workplace Analytics system attributes (Required or Reserved), you can modify the mapping for those in this section.

  ![CRM data custom attributes](../images/wpa/setup/crm-custom-attributes.png)

### CRM data rules

Confirm the CRM column names and field values in the files follow the same rules you applied when creating the Organizational (HR) data upload file, such as no spaces, commas, dollar signs, or other special characters in the column names.

For a complete list of rules, see [Attribute notes and recommendations](Prepare-organizational-data.md#attribute-notes-and-recommendations) and [Use only valid values and formats](Prepare-organizational-data.md#use-only-valid-values-and-formats).

#### Tips for common upload issues

* The upload must have *100 percent coverage* for all required attributes, which means every row must have valid values for these attributes or the validation will fail. To ensure this:

  * Only export rows to the .csv file that have non-null values for the required attribute columns, such as AccountID.
  * For Date fields, use functions in the .csv file to set all rows that have empty or null values to "Today's date."

* The ContactID must be unique, which is usually a GUID and must be different from the ContactEmail.
* AccountID and AccountName are typically managed at a domain level, however the upload needs the lowest possible Account level for analysis. You can always add Parent fields to group these fields in the .csv file. For example, AccountContinent to group accounts by continent.
* Confirm all email fields have a valid email address, not an alias (such as abc@contoso.com, not just "abc"). Use functions in the file to check and remove special characters and spaces from the email fields.
* Custom or reserved string fields (for example, "Redmond, WA") can have commas, which in a .csv file equals a new column. To prevent commas from being mistaken as field separators, set these text strings to wrap in the .csv file.
* Confirm that instances of double quotes or single quotes are always pairs in the .csv file. If not, will lead to the system misinterpreting the data as missing columns.
* Before starting the upload process, confirm the upload file is saved as a UTF-8 encoded .csv file and is closed (not open in another app).
* See [Common Format and MIME Type for Comma-Separated Values (CSV)](https://tools.ietf.org/html/rfc4180) for a complete list of format requirements as defined by the industry.

## Upload, validate, and process the CRM data

1. In **Settings** > **Upload** > **CRM data**, select **New upload**.
2. Download and use the template provided in the **Tips** section.
3. In the **Data source** section, select the applicable source for the upload, such as **Salesforce** or **Dynamics CRM**.
4. In the **Data type** section, select the type of CRM data you want to upload. You can only upload one of the following types of data files at a time. However, you can wait until you’ve uploaded all the files you need, before submitting the data for validation, which is more time efficient.
   * Accounts
   * Contacts
   * Seller assignments

   > [!Tip]
   > For the first upload, limit it to Accounts and Contacts only. Seller assignments adds a higher level of complexity for validation.

5. In the **Select file** section, select the source (.csv) file that corresponds with the data type selected in the previous step. You can select **Download a .csv template** to help with file requirements.
6. Select **More options** to change the default append option to the delete and add new option:

   * To preserve previously uploaded data and incrementally append it with new data, keep the default selection of **Append new records**.
   * To remove and replace existing data with this new data, select **Delete all old records and add new records**.

7. In the **Create an upload name** section, type a name and a description for your upload, and then select **Next**.
8. In the **System fields** section, confirm or change the following:

   * In **Source column of CSV**, select the applicable field name that corresponds with the name in the Workplace Analytics attribute column for each of the fields in the uploaded .csv files.
   * In **Data type**, confirm the data in the file matches the specified data type. For example, the Account Owner Email value must be a valid email in each row for this column in the upload file. These fields are read-only on this page.
   * In **Report options**, you can change this setting to one of the following only for optional or custom attributes. This setting is read-only for the required attributes.
     * **Include in report** includes the data in reports generated by queries.
     * **Exclude from report** excludes data from reports that are generated by queries.
     * **Hash in report** includes de-identified or a hashed version of the data in reports generated by queries.
   * In **First row from uploaded file**, you can confirm the field mapping is correct with this read-only column, which shows example values of the first row of data in the file for both Salesforce and Dynamics CRM.
9. In the **Custom fields (optional)** section, you can add any additional custom fields that Workplace Analytics was not able to map for you in the **System fields** section, and then map the applicable columns and other options accordingly.
10. Select **Next**.
11. On the summary page, confirm the file details, and then select **Submit**.
12. The new upload will be listed in the **Data Uploads** section with a status of **Validating**, which might take a few minutes.
13. When the status changes to **Validated, Ready to process**:
    * If you have more CRM files to upload, select **Upload** and go back to Step 2 and repeat these steps until you’ve uploaded all applicable CRM files.
    * After all applicable CRM files are validated, select **Turn on processing** to save the data and get it processed in Workplace Analytics.

     ![Process CRM data](../images/wpa/setup/crm-process-data.png)

14. Other possible statuses and options you might see on the CRM data page:
    * **Processed** - this status means the data was successfully saved.
    * **Validation failed** - this status means the uploaded file does not meet the validation requirements of Workplace Analytics. Validation will fail for the following reasons:

      * Incorrect encoding of the uploaded file. The upload must use UTF-8 encoding.
      * Coverage requirement not being met, such as a mandatory field (such as AccountId) in the upload file has one or more records with empty or null values. Mandatory fields cannot have empty or null values.
      * Incorrect email format where an email address field has one or more records with an invalid email format (a valid email is username@coname.com).

    * **Processing failed** - this status means the data could not be saved or processed due to an error.
    * **Abandoned** - this status means you tried to upload a file of the same data type (such as accounts) two or more times before the processing completed on the first upload. When this occurs, Workplace Analytics will abandon the previous uploads and will try to validate the last upload of the same data type.
    * **Download log** - select to see a detailed list of issues that caused the failure.
    * **Mapping** – select to see the field mappings . If they’re not set correctly, you’ll need to correct them in the .csv file and repeat the upload steps with the new file.
    * **Records created** – after a file’s status changes to Processed, you can select this to see the number of new records that were created with the upload.

## Related topics

* [Queries with CRM data](../tutorials/crm-queries.md)
* [Prepare organizational data](Prepare-organizational-data.md)
* [First organizational upload](upload-organizational-data-1st.md)
* [CRM data sources](../Use/crm-data.md)
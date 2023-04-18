---
ROBOTS: NOINDEX, NOFOLLOW
title: Import organizational data (first import)
description: Learn how to set up a connection and import your data to the Viva Insights advanced insights app
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

# Import organizational data (first import)

*Applies to: private preview customers*

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of three ways: through Azure Active Directory, which is the default source; through individual .csv files that you as an Insights Administrator upload directly to Viva Insights; or through an automated data import that you, your source system admin, and your Microsoft 365 IT admin set up.
This article talks about the third option, importing data. 

With an import, you create your own app to automatically export your source data and metadata to a zipped folder. Then, your custom app runs a console app we created, called DescriptiveDataUploadApp. Through DescriptiveDataUploadApp, Viva Insights pulls your data into the advanced insights app. 

However, before you can run your app and start transferring data to Viva Insights, you'll need to coordinate a few tasks between your Microsoft 365 admin and Insights Administrator (Insights admin). Refer to [Workflow](#workflow) for an overview of required steps.

>[!Important]
>Only use the following steps if this is the first time you’re importing organizational data. If this isn’t your first import, refer to [Import organizational data (subsequent imports)](import-org-data-subsequent.md) to refresh previously imported data.


## Workflow


1. Setup:
    1. The data source admin [generates a security certificate](#generate-the-security-certificate) and provides it to the Microsoft 365 admin.
    1. Using the security certificate, the Microsoft 365 admin [registers a new app in Azure](#register-a-new-app-in-azure).
    1. Using IDs from the app registration, the Insights admin [sets up the import](#set-up-the-import-in-viva-insights).
    1. The data source admin [prepares their data and exports it](#prepare-export-and-import-organizational-data) using a custom app (for example, a PowerShell script). Their custom app saves data to a zipped folder and automatically runs the [DescriptiveDataUploadApp](#run-the-descriptivedatauploadapp-in-the-console) on the console.
    1. The DescriptiveDataUploadApp pulls data from the data source admin’s local file to Viva Insights.

1. Validation: Viva Insights validates your data. (If validation isn’t successful, you can choose from a few options described in [Validation fails](#validation-fails).)
1. Processing: Viva Insights processes your data. (If processing isn’t successful, you can choose from a few options described in [Processing fails](#processing-fails).)

After the data successfully validates and processes, the overall data-import task is complete.

:::image type="content" source="../images/admin-data-import-flow.png" alt-text="Flow diagram that shows the Workflow steps above, starting with actions by the Data source admin and ending with actions by the Advanced insights app." lightbox="../images/admin-data-import-flow-expanded.png":::

## Setup

### Generate the security certificate

*Applies to: data source admin*

To start getting data from your source file into Viva Insights, the Microsoft 365 admin needs to create and register an app in Azure. As the data source admin, you’ll need to help the Microsoft 365 admin register their app by giving them a security certificate.

Here’s what to do:

1.	Create a certificate by following the instructions in this article: [Create a self-signed public certificate to authenticate your application](/azure/active-directory/develop/howto-create-self-signed-certificate)
2.	Send the generated certificate to the Microsoft 365 admin.

That’s it for now. If you want to get a head start on your next steps, follow the steps in [Export and import your data on a set frequency](#export-and-import-your-data-on-a-set-frequency).  

### Register a new app in Azure

*Applies to: Microsoft 365 admin*

>[!Note]
>For more information about registering an app in Azure, refer to [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app#register-an-application).


1. From the Microsoft admin center's left rail, select **All admin centers**. This option appears as the last one on the list.

    :::image type="content" source="../images/admin-di-all-admin-centers.png" alt-text="Screenshot that shows selecting All admin centers from the left rail.":::

1. Select **Azure Active Directory**.

1. Create a new app registration:
    1. In the top toolbar, select **Add > App registration**.

        :::image type="content" source="../images/admin-di-add-new-registration-1.png" alt-text="Screenshot that shows the Azure portal add menu expanded with App registration highlighted.":::

    2. On the resulting screen:
        1. Give your app a name. 
        1. Under **Supported account types**, leave the first option, **Accounts in this organizational directory only ([Your organization] only - Single tenant)**, selected. 
        1. Select the **Register** button at the bottom of the screen.

        :::image type="content" source="../images/admin-di-registration-3.png" alt-text="Screenshot that shows Register an application screen with i, ii, and iii that correspond to the steps listed above."lightbox="../images/admin-di-registration-3.png":::

    1. When you arrive back at the **Overview** screen, copy down the **Application (client) ID** and **Directory (tenant) ID**.
    
         :::image type="content" source="../images/admin-di-app-id.png" alt-text="Screenshot that shows the ID and certificate/secret pane in Azure.":::


    >[!Important]
    >Keep these IDs handy. You'll need to provide them later.
1. Add a certificate:
    1.  Select **Add a certificate or secret**.

        :::image type="content" source="../images/admin-di-secret.png" alt-text="Application (client) ID":::

    2. Select **Upload certificate**.
    
        :::image type="content" source="../images/admin-di-upload-cert.png" alt-text="ID and certificate/secret pane":::


    3. Upload the certificate that the data source admin gave you and add a **Description**. Select the **Add** button.

        :::image type="content" source="../images/admin-di-upload-cert-pane3.png" alt-text="Screenshot that shows the Upload certificate dialog box in Azure.":::

5. Remove API permissions:
    1. Select **API permissions** from the left rail.
    2. For each listed **API / Permissions** name, select the ellipses (**...**) to the right of the API—for example, **Microsoft Graph**.
    3. Select **Remove permission**.

        :::image type="content" source="../images/admin-di-upload-remove-perms-1.png" alt-text="Screenshot that shows selecting Remove permissions in Azure. "lightbox="../images/admin-di-upload-remove-perms-1.png":::
    1. Confirm removal.

    When you remove permissions for these items, you’re making sure app only has permissions for what it needs.

1. Share the IDs you noted down in step 3c:
    1. Give the Insights admin the app ID.
    1. Give the data source admin the app ID *and* the tenant ID.

### Set up the import in Viva Insights

*Applies to: Insights admin*

1. Go to the **Organizational data** tab in the Viva Insights admin portal.

1. Start the import from one of two places: the **Data hub** tab or the **Data connections** tab. 

    1. From **Data hub**:
    
        1. In the **Data source** section, find the **Automated import** option. Select the **Start** button.

    1. From **Data connections**:
    
        1. Next to **Current source**, select the **data sources** button.

        1. A **Switch to: Automated import** window appears. Select **Start**.

1. On the **Automated organizational data import** page:
    1. Give your connection a name.
    
    1. Enter the app ID that your Microsoft 365 admin gave you.
    
    1. Save.
1. Select the connection you named in step 3a as the new data source. 
1. Contact the data source admin and request that they send org data to Viva Insights.

### Prepare, export, and import organizational data

#### Tips for preparing your data

* For new data, include full historical data for all employees. 
* Import organizational data for all employees in the company, including licensed and non-licensed employees. 
* Refer to the [sample .csv template](https://go.microsoft.com/fwlink/?linkid=2224590) for data structure and guidelines to avoid common issues like too many or too few unique values, redundant fields, invalid data formats, and more.

#### Export and import your data on a set frequency

To export data from your source system and import it into Viva Insights on a set frequency, you’ll need to create a custom app. Your app can take any form—for example, a PowerShell script—but it needs to do two things: 

1. Export your source data as a zipped folder at the frequency you pick, and store that folder in your local files.
1. Automatically run the DescriptiveDataUploadApp we created on the console. The DescriptiveDataUploadApp then brings your locally stored data into Viva Insights.

:::image type="complex" source="../images/admin-custom-app-flow.png" alt-text="Screenshot that shows a diagram of the flow of information from source system to Viva Insights."lightbox="../images/admin-custom-app-flow-expanded1.png":::
   Flow diagram of the data-import process. The first step shows a data icon labeled, "Source system" with a downward arrow leading to a PowerShell/command icon labeled, "Your custom app." Next to the arrow, there's a clock indicating automated refresh based on frequency. A downward arrow leads from the "Your custom app" icon to a folder icon labeled, "Local folder." A horizontal arrow leads to the right from the folder icon to an app icon in the center of the diagram labeled, "DescriptiveDataUploadApp." From the app icon, a horizontal arrow leads to the right to the Viva Insights icon, labeled, "Viva Insights."
:::image-end:::

##### Export and store the zipped folder

At the frequency you decide (once a month, once a week, etc.) have your custom app export organizational data from your source system as a zipped folder and store it in your files. Base this zipped folder on the zipped folder we provide. (Select [this link](https://go.microsoft.com/fwlink/?linkid=2224590) to download the folder.) Your zipped folder needs to contain a data.csv file and a metadata.json file.


Here are a few more details about these files and what they need to contain:

###### data.csv

Add all fields you want to import in this file. Make sure you format it according to our guidelines in [Prepare organizational data](prepare-org-data.md#structure-the-organizational-data).

###### metadata.json

Indicate the type of refresh you’re performing and how Viva Insights should map your fields:

* `“DatasetType”: “HR”` (line 2). Leave this as-is.
* `“IsBootstrap”:` (line 3). Use `“true”` to indicate a full refresh and `“false”` to indicate an incremental refresh. If this is your first import, use `“true”`.
* `“Mapping”:`. If you use names other than what Viva Insights uses, change each column header name to match what you use in your source system.

>[!Important]
>Remove any fields that aren’t present in your .csv file.

**Mapping example**

The following example represents one field you’ll find in the metadata.json file:

```json
"PersonId": {
    "name": "PersonId",
    "type": "EmailType"
```


* `"PersonId": {` corresponds to the source column name.
* `“name” : “PersonId”,`  corresponds to the Viva Insights field name.
* `"type": "EmailType"`  corresponds to the field’s data type.

Let’s say that instead of `PersonId`, your source system uses `Employee` for this field header. To make sure your fields are mapped correctly, you’ll want to edit the first line below, so it looks like this:

```json
      "Employee": {
        "name": "PersonId",
        "type": "EmailType"
```

When you upload your data, your `Employee` field will become `PersonId` in Viva Insights.

 
##### Run the DescriptiveDataUploadApp in the console

Whenever it exports the zipped folder from your source system, have your custom export app automatically run the DescriptiveDataUploadApp. We created the DescriptiveDataUploadApp [on GitHub](https://github.com/microsoft/vivainsights_ingressupload) to transfer your data into Viva Insights. Clone this app to your machine by running the following command: `git clone https://github.com/microsoft/vivainsights_ingressupload.git.` 

1.	For each export, have your custom export app run the DescriptiveDataUploadApp.
2.	A console pops up requesting values. Add the following values:
    1. AppID/ClientID. This ID is in the registered app information on the Azure portal under Application (client) ID.
    1. Absolute path to the zipped folder. Format the path like this: `C:\\Users\\JaneDoe\\OneDrive - Microsoft\\Desktop\\info.zip`.
    1. Azure Active Directory tenant ID. This ID is also on the app's overview page under Directory (tenant) ID.
    1. Certificate name. This name is configured in your registered application. If you haven’t created a certificate yet, refer to [How to create a self-signed certificate](/azure/active-directory/develop/howto-create-self-signed-certificate). After you upload the certificate, the certificate name shows up under **Description** in the Azure Portal.

## Validation

After the data source admin sends data, the app starts validating.

After this phase completes, validation has either succeeded or failed. Depending on the outcome, you’ll either receive a success notification or a failure notification in the top-right corner of the **Data connections** screen.

For information about what happens next, go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Processing” status on the **Import history** table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you’ll either find a “Success” or “Failed” status in the **Import history** table.

#### Processing succeeds

When you find the “Success” status in the **Import history** table, the upload process is complete.

After you receive the “Success” status, you can:

* Select the view (eye) icon to see a summary of the validation results.
* Select the mapping icon to see the mapping settings for the workflow.

>[!Note]
>Each tenant can have only one upload in progress at a time. You need to complete the workflow of one data file, which means you either guide it to a successful validation and processing or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the **Data connections** tab.

#### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. For processing to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. If you’ve corrected all errors and are still getting a “Processing failed” status, file a support ticket with us.

### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the data source admin so they know what to correct before sending the data again. 

The data source admin might find the following section helpful to fix data errors in their export file.

#### About errors in data

*Applies to: data source admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until the data source admin fixes the source data.

Refer to [Prepare organizational data](prepare-org-data.md) for specific formatting rules that might help resolve errors you encounter.

## Related topics

[Prepare organizational data](prepare-org-data.md)

[Import organizational data (subsequent import)](import-org-data-subsequent.md)

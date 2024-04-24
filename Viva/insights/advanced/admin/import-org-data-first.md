---
ROBOTS: NOINDEX, NOFOLLOW
title: Import organizational data (first import)
description: Learn how to set up a connection and import your data to the Viva Insights advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data (first import)

*Applies to: private preview customers*

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of three ways: through Microsoft Entra ID, which is the default source; through individual .csv files that you as an Insights Administrator upload directly to Viva Insights; or through an automated data import that you, your source system admin, and your Microsoft 365 IT admin set up.

This article talks about the third option, importing data. 

With an import, you bring data from your source system to the Viva Insights HR data ingress API through a zip file. You can either:

* Create a custom app to export data from the source system to a zip file. Then, using the same app, import that data using the API information below. 
* Create a custom app to export data from the source system to a zip file. Then, run a C# console app we created to import data to Viva Insights.
* Create a custom app to export data from the source system to a zip file. Then, run a PowerShell script we created to import data to Viva Insights. 


However, before you can run your app and start transferring data to Viva Insights, you'll need to coordinate a few tasks between your Microsoft 365 admin and Insights Administrator (Insights admin). Refer to [Workflow](#workflow) for an overview of required steps.

>[!Important]
>Only use the following steps if this is the first time you’re importing organizational data. If this isn’t your first import, refer to [Import organizational data (subsequent imports)](import-org-data-subsequent.md) to refresh previously imported data.


## Workflow


1. Setup:
    1. The data source admin [generates a security certificate](#generate-the-security-certificate) and provides it to the Microsoft 365 admin.
    1. Using the security certificate, the Microsoft 365 admin [registers a new app in Azure](#register-a-new-app-in-azure).
    1. Using IDs from the app registration, the Insights admin [sets up the import](#set-up-the-import-in-viva-insights).
    1. The data source admin prepares their data and either:
        1.	Exports it from their source system using a custom app based on our API, then, using the same app, imports the data to Viva Insights.
        2.	Exports it from their source system using a custom app based on our API, then, using our C# solution or PowerShell script, imports the data to Viva Insights.

    :::image type="content" source="../images/admin-data-import-flow.png" alt-text=" Diagram of the workflow above."lightbox="../images/admin-data-import-flow-expanded.png":::

1. Validation: Viva Insights validates your data. (If validation isn’t successful, you can choose from a few options described in [Validation fails](#validation-fails).)
1. Processing: Viva Insights processes your data. (If processing isn’t successful, you can choose from a few options described in [Processing fails](#processing-fails).)

After the data successfully validates and processes, the overall data-import task is complete.

## Setup

### Generate the security certificate

*Applies to: data source admin*

To start getting data from your source file into Viva Insights, the Microsoft 365 admin needs to create and register an app in Azure. As the data source admin, you’ll need to help the Microsoft 365 admin register their app by giving them a security certificate.

Here’s what to do:

1.	Create a certificate by following the instructions in this article: [Create a self-signed public certificate to authenticate your application](/azure/active-directory/develop/howto-create-self-signed-certificate)
2.	Send the generated certificate to the Microsoft 365 admin.

That’s it for now. If you want to get a head start on your next steps, follow the steps in [Export your data on a set frequency](#export-your-data-on-a-set-frequency).  

### Register a new app in Azure

*Applies to: Microsoft 365 admin*

>[!Note]
>For more information about registering an app in Azure, refer to [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app#register-an-application).


1. From the Microsoft admin center's left rail, select **All admin centers**. This option appears as the last one on the list.

    :::image type="content" source="../images/admin-di-all-admin-centers.png" alt-text="Screenshot that shows selecting All admin centers from the left rail.":::

1. Select **Microsoft Entra ID**.

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

1. Start the import from one of two places: the **Data hub** page or the **Organizational data** page, under **Data connections**. 

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

#### Export your data on a set frequency

At the frequency you decide (once a month, once a week, etc.) have your custom app export organizational data from your source system as a zip folder and store it in your files. Base this zip folder on the one [here](https://go.microsoft.com/fwlink/?linkid=2230444). Your zip folder needs to contain a data.csv file and a metadata.json file. 

Here are a few more details about these files and what they need to contain:

###### data.csv

Add all fields you want to import in this file. Make sure you format it according to our guidelines in [Prepare organizational data](prepare-org-data.md#step-4---structure-the-organizational-data).

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

#### Import your data

To import your data to Viva Insights, you can pick from three options:

* Use our API to build a custom app that exports and imports your data at the frequency you choose.
* Run our C# solution on your console, which is based on our API.
* Run our PowerShell script, which is also based on our API. 

>[!Note]
>Our C# and PowerShell solutions only import data to Viva Insights. They don’t export data from your source system.

Before working with any of the options below, make sure you have this information:

* App (client) ID. Find this ID in the registered app information on the Azure portal under Application (client) ID. 
* Client secret: This is a secret string that the application uses to prove its identity when requesting a token. It’s also referred to as application password. This secret is only shown for the first time when the client secret is created. To create a new client secret, refer to [Create a Microsoft Entra app and service principal in the portal](/azure/active-directory/develop/howto-create-service-principal-portal#option-3-create-a-new-application-secret).
* Certificate name. This name is configured in your registered application. After you upload the certificate, the certificate name shows up under **Description** in the Azure Portal. You can use the certificate name as an alternative to the client secret.
* The zip file and the path to the zip file.  Don’t change the file names data.csv and metadata.json. 
* Microsoft Entra tenant ID. Also find this ID on the app's overview page under **Directory (tenant) ID**.
* Scale unit: The scale unit provided to you for your tenant, for example, `novaprdwus2-01`.

##### About the Viva Insights HR data ingress API 

View the following commands: 

[Request headers]

These two request headers are required for all the APIs mentioned below  
 

`x-nova-scale unit: <ScaleUnit obtained from your VI contact>`

`Authentication: Bearer <Oauth token from AAD>` 
 
>[!Note]
>Generate Active Directory OAuth token for registered app (daemon app auth flow) using:  
>`Authority: https://login.microsoftonline.com` 
>
> `Tenant: <target AAD tenant ID> `
>
>`Audience: https://api.orginsights.viva.office.com`
>
>For more information about generating tokens, refer to: [Acquire and cache tokens with Microsoft Authentication Library (MSAL)](/azure/active-directory/develop/msal-acquire-cache-tokens)

##### Get connector/ping to check if connector is set for a tenant
 
`[GET] https://api.orginsights.viva.office.com/v1.0/scopes/<tenantId>/ingress/connectors/ status?connectorType=Hr`

[ResponseBody]  

If connector is set and caller application (id) is granted authorization:  
 
 
```
200:  

{ 
       “ConnectorId”: “Connector-id-guid” 

}
```
                       

If Insights Administrator has removed the connector or, connector has not been set by Insights Administrator yet: 

 
`403: Forbidden.`

##### Push data

1P/3P survey app to call Viva Insights API to push content 


`[POST] https://api.orginsights.viva.office.com/v1.0/scopes/<tenantId>/ingress/connectors/HR/ingestions/fileIngestion` 

[Body] file content as multipart/form-data 


Type: [Zip archive](/dotnet/api/system.io.compression.ziparchive) 

 

Content to be archived: 

Metadata.json 

Data.csv  

 
 
[Request Body] 

```
Body: 

{ 

   "$content-type": "multipart/form-data", 

   "$multipart":  

    [ 

        { 

            "headers":  

                { 

                    "Content-Disposition": "form-data; name=\"file\"; filename=info" 

                   }, 

            "body": @{body('Get_blob_content_(V2)')} 

         } 

    ] 

} 
``` 

[Response Body] 

```
200:  
{ 

  "FriendlyName": "Data ingress", 

  "Id": "<ingestion Id>", 

  "ConnectorId": "<connector Id>", 

  "Submitter": "System", 

  "StartDate": "2023-05-08T19:07:07.4994043Z", 

  "Status": "NotStarted", 

  "ErrorDetail": null, 

  "EndDate": null, 

  "Type": "FileIngestion" 

} 
``` 

In case connector is not set:

`403: Forbidden`

If connector is set but previous ingestion is not complete yet:

`400: Bad request: Previous ingestion is not complete.`

##### Poll status

API to poll status for the ingestion, as the ingestion of data is long-running operation. 
 
`[GET] 
 https://api.orginsights.viva.office.com/v1.0/scopes/<tenantId>/ingress/connectors/Hr/ingestions/{ingestionId}`

[Response] 

```
200: 
{ 

            "FriendlyName": "Data ingress", 

            "Id": "<ingestion Id>", 

            "ConnectorId": "<connector Id>", 

            "Submitter": "System", 

            "StartDate": "2023-05-08T19:05:44.2171692Z", 

            		  "Status": "NotStarted/ExtractionComplete/ValidationFailed 

/Completed/", 

            "ErrorDetail": null, 

            "EndDate": "2023-05-08T20:09:18.7301504Z", 

            "Type": "FileIngestion" 

}, 
```

##### Download error stream in case of validation failed (issue in data) 

`[GET] 
https://api.orginsights.viva.office.com/v1.0/scopes/<tenantId>//Hr/ingestions/{ingestionId}/errors`

 

[Response] 

`200: File stream with errors, if any.`

##### Option 1: Use the Viva Insights HR data ingress API to build a custom import/export app 

You can use the Viva Insights HR data ingress API to build a custom app that automatically exports data from your source system, and then imports it to Viva Insights.  

Your app can take any form—for example, a PowerShell script—but it needs to export your source data as a zip folder at the frequency you pick, store the folder in your files, and import that folder into Viva Insights. 

##### Option 2: Import data through our C# solution after exporting data through your custom app 

After you’ve exported your source data as a zip folder at the frequency you pick, and stored that folder in your files, you can run the DescriptiveDataUploadApp C# solution on the console. The DescriptiveDataUploadApp C# solution then brings your locally stored data into Viva Insights. 

To run the solution: 

1. Clone this app to your machine by running the following command on the command line:
 
    `git clone https://github.com/microsoft/vivainsights_ingressupload.git.`  

1. Include the following console values. Refer to [Prepare, export, and import organizational data for descriptions](#prepare-export-and-import-organizational-data). 
    * AppID/ClientID 
    * Absolute path to the zipped file. Format the path like this: `C:\\Users\\JaneDoe\\OneDrive - Microsoft\\Desktop\\info.zip` 
    * Microsoft Entra tenant ID 
    * Certificate name

##### Option 3: Run the DescriptiveDataUpload PowerShell solution after exporting data through your custom app 

Similar to option 2, after you’ve exported your source data as a zip folder at the frequency you pick, and stored that folder in your files, you can run the DescriptiveDataUpload PowerShell solution on the console. The DescriptiveDataUpload PowerShell solution then brings your locally stored data into Viva Insights. 

1. Clone the source code to your machine by running this command on the command line: 

    `git clone https://github.com/microsoft/vivainsights_ingressupload.git` 

1. Open a new PowerShell window as an administrator. 

1. In your PowerShell window, run the following command: 

    `Install-Module -Name MSAL.PS`

    Or, go to this [PowerShell gallery link](https://www.powershellgallery.com/packages/MSAL.PS) for instructions on installation. 

1. Set parameters. Refer to [Prepare, export, and import organizational data](#prepare-export-and-import-organizational-data) for descriptions. 

    * `ClientID` 
    * `pathToZippedFile` 
    * `TenantId` 
    * `novaScaleUnit`
    * `ingressDataType: HR`  
    * `ClientSecret` or `certificateName` 
 

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
>Each tenant can have only one import in progress at a time. You need to complete the workflow of one data file, which means you either guide it to a successful validation and processing or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the **Data connections** tab.

#### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. For processing to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. 

>[!Note]
>Processing failures are generally due to backend errors. If you’re seeing persistent processing failures and you’ve corrected the data in your imported file, [log a support ticket with us](/microsoft-365/admin/get-help-support).

### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the data source admin so they know what to correct before sending the data again. 

The data source admin might find the following section helpful to fix data errors in their export file.

#### About errors in data

*Applies to: data source admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until the data source admin fixes the source data.

Refer to [Prepare organizational data](prepare-org-data.md) for specific formatting rules that might help resolve errors you encounter.

Here are a few import-specific errors you might encounter if your files aren't formatted correctly:

* There is a problem with the files in the .zip file. Make sure the .zip file contains only one .json file and one .csv file and upload it again.
* The .csv file in your .zip file is empty. Add a non-empty .csv file and upload the .zip file again.
* The .json file in your .zip file is empty. Add a non-empty .json file and upload the .zip file again.
* The content in the .json file isn't mapped to a supported data type. Map the content to a supported data type and upload the .zip file again.
* The .json file is invalid. Please use a valid .json file and upload the .zip file again.
* The header names in the .csv file don’t match the fields you mapped in the .json file. Make sure the .json file contains the same fields as the .csv file, and upload the .zip file again.
* The number of headers in the .csv file doesn't match the fields you mapped in the .json file. Make sure the .json file contains the same fields as the .csv file, and upload the .zip file again.
* Your .csv file is mapped to a null or empty field in your .json file. Map it to a non-empty field and upload the .zip file again.


## Related topics

[Prepare organizational data](prepare-org-data.md)

[Import organizational data (subsequent import)](import-org-data-subsequent.md)

---
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

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of three ways: through Azure Active Directory, which is the default source; through individual .csv files that you as an Insights Administrator upload directly to Viva Insights; or through an automated data import that you, your source system admin, and your Microsoft 365 IT admin set up.

This article talks about the third option: importing data. When you set up an import, you’ll drop your exported source data into a zip file, along with some metadata for Viva Insights. Viva Insights then pulls that data in to the advanced insights app. To start importing data, you'll need to coordinate a few tasks between your Microsoft 365 IT admin and your data source admin, including registering a new app and getting a security certificate. Refer to the next section, [Workflow](#workflow), for an overview of required steps.

>[!Important]
>Only use the following steps if this is the first time you’re importing organizational data. If this isn’t your first import, refer to [Import organizational data (subsequent imports)](import-org-data-subsequent.md) to refresh previously imported data.

## Workflow


1. Setup:
    1. The data source admin [prepares their data export](#prepare-the-data-export).
    1. The data source admin [generates a security certificate](#generate-the-security-certificate) and provides it to the Microsoft 365 IT admin.
    1. The Microsoft 365 IT admin [registers a new app in Azure](#register-a-new-app-in-azure).
    1. The Insights Administrator [sets up the automated import](#set-up-the-import-in-viva-insights).
    1. The data source admin pushes data to Viva Insights.
1. Validation: Viva Insights validates your data. (If validation isn’t successful, you can choose from a few options described in [Validation fails](#validation-fails).)
1. Processing: Viva Insights processes your data. (If processing isn’t successful, you can choose from a few options described in [Processing fails](#processing-fails).)

After the data successfully validates and processes, the overall data-import task is complete.

:::image type="content" source="../images/admin-import-diagram-small.png" alt-text="org data import flowchart" lightbox="../images/admin-import-diagram.png":::

## Setup

### Prepare the data export

*Applies to: data source admin*

To make the data-transfer process go smoothly, you’ll need to export and save your source data in the right format.

1. Export organizational data from your source system as a .csv.
1. Download the zip folder we’ve prepared for you here: 
1.	Open OrganizationalDataFile.xlsx within the zip folder and save the Template tab as a .csv.
1.	Enter your data in the **Template** tab and format your data according to our guidelines in [Prepare organizational data](prepare-org-data.md).

>[!Note]
>Viva Insights doesn’t support custom fields for data import, so make sure you’re using required and reserved optional fields only. Our [Prepare organizational data](prepare-org-data.md#attribute-reference) article includes an attribute reference.

You’ll enter the path for the zip folder when you set up the connection to Viva Insights.

### Tips for preparing your data

* For new data, include full historical data for all employees. 
* Import organizational data for all employees in the company, including licensed and non-licensed employees. 
* Refer to the sample .csv template [LINK PENDING] for data structure and guidelines to avoid common issues like too many or too few unique values, redundant fields, invalid data formats, and more.


### Generate the security certificate

*Applies to: data source admin*

To start getting data from your source file into Viva Insights, the Microsoft 365 admin needs to create and register an app in Azure. As the data source admin, you’ll need to help the Microsoft 365 admin register their app by giving them a security certificate.

Here’s what to do:

1.	Create a certificate by following the instructions in this article: [Create a self-signed public certificate to authenticate your application](/azure/active-directory/develop/howto-create-self-signed-certificate)
2.	Send the generated certificate to the Microsoft 365 admin.

That’s it for now. If you want to get a head start on your next steps, follow steps 1-3 in [Set up the connection to Viva Insights](#set-up-the-connection-to-viva-insights).  



### Register a new app in Azure

*Applies to: Microsoft 365 admin*

>[!Note]
>For more information about registering an app in Azure, refer to [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app#register-an-application).


1. From the Microsoft admin center's left rail, select **All admin centers**. This option appears as the last one on the list.

    :::image type="content" source="../images/admin-di-all-admin-centers.png" alt-text="all admin centers":::

1. Select **Azure Active Directory**.

1. Create a new app registration:
    1. In the top toolbar, select **Add > App registration**.

        :::image type="content" source="../images/admin-di-add-new-registration1.png" alt-text="add new app registration":::

    2. On the resulting screen:
        1. Give your app a name. 
        1. Under **Supported account types**, leave the first option, **Accounts in this organizational directory only ([Your organization] only - Single tenant)**, selected. 
        1. Select the **Register** button at the bottom of the screen.

        :::image type="content" source="../images/admin-di-registration3.png" alt-text="name app":::

    1. When you arrive back at the **Overview** screen, copy down the **Application (client) ID** and **Directory (tenant) ID**.
    
         :::image type="content" source="../images/admin-di-app-id.png" alt-text="ID and certificate/secret pane":::


    >[!Important]
    >Keep these IDs handy. You'll need to provide them later.
1. Add a certificate:
    1.  Select **Add a certificate or secret**.

        :::image type="content" source="../images/admin-di-secret.png" alt-text="Application (client) ID":::

    2. Select **Upload certificate**.
    
        :::image type="content" source="../images/admin-di-upload-cert.png" alt-text="ID and certificate/secret pane":::


    3. Upload the certificate that the data source admin gave you and add a **Description**. Select the **Add** button.

        :::image type="content" source="../images/admin-di-upload-cert-pane3.png" alt-text="ID and certificate/secret pane":::

5. Remove API permissions:
    1. Select **API permissions** from the left rail.
    2. For each listed **API / Permissions** name, select the ellipses (**...**) to the right of the API—for example, **Microsoft Graph**.
    3. Select **Remove permission**.

        ![ID and certificate/secret pane](../images/admin-di-upload-remove-perms1.png)

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

### Set up the connection to Viva Insights

*Applies to: data source admin*

To send data to Viva Insights, you’ll need set up the connection between your source data and Viva Insights. To create this connection, we made [an app in GitHub](https://github.com/microsoft/vivainsights_ingressupload/tree/main/DescriptiveDataUploadApp), which you can clone and use.
 
Here’s how to get the app set up:

>[!Note]
>We wrote these directions specifically for Visual Studio, but you can set up your application through any code editor.

#### Set up the application

1. Clone the app. Open a command prompt and enter the following command: `git clone https://github.com/microsoft/vivainsights_ingressupload.git`.
1. If Visual Studio was open, close it. Open or re-open Visual Studio as an administrator.
1. On the right, select **Open a local folder**. Choose the cloned folder (**vivainsights_ingressupload**). 
    >[!Note]
    >The cloned folder will live in whichever directory you ran the git clone command from.
1. On the right, in the **Solution Explorer** tab, double-click **DescriptiveDataUploadApp.sln**.
    :::image type="content" source="../images/admin-upload-app-sln1.png" alt-text="Screenshot of DescriptiveDataUploadApp.sln in Visual Studio's Solution Explorer.":::
1. At the top of Visual Studio, you’ll need to select a start-up project. Select **DescriptiveDataUploadApp.csproj**.
1. Select the play button to run the app or press Ctrl + F5 on your keyboard.
    :::image type="content" source="../images/admin-upload-app-play1.png" alt-text="Screenshot of the play button for DescriptiveDataUpload app in Visual Studio.":::

#### Enter values in the console

>[!Note]
>None of the values require quotation marks ("") around them.

After you set up the app, a console pops up asking you for the following inputs:

1. App (client) ID. Find this ID in the registered app information on the Azure portal under **Application (client) ID**. If you haven’t created and registered your app yet, follow the instructions in [Register a new app in Azure](#register-a-new-app-in-azure).
1. Path to the zipped file you downloaded in Prepare organizational data. Format the path like this: `C:\\Users\\JaneDoe\\OneDrive - Microsoft\\Desktop\\info.zip`.
1. Azure Active Directory tenant ID. Also find this ID on the app's overview page under **Directory (tenant) ID**.
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

![Screenshot that shows successful processing.](../images/admin-status-success.png)

After you receive the “Success” status, you can:

* Select the view (eye) icon to see a summary of the validation results.
![Screenshot that shows validation results.](../images/admin-upload-results.png)
* Select the mapping icon to see the mapping settings for the workflow.
![Screenshot that shows mapping settings.](../images/admin-map-results.png)

>[!Note]
>Each tenant can have only one upload in progress at a time. You need to complete the workflow of one data file, which means you either guide it to a successful validation and processing or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the **Data connections** tab.

#### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. For processing to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. If you’ve corrected all errors and are still getting a “Processing failed” status, file a support ticket with us.

![Screenshot that shows Processing failed.](../images/admin-status-process-failed.png)

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
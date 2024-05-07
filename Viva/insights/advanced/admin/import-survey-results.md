---
ROBOTS: NOINDEX, NOFOLLOW
title: Import survey results
description: Learn how to import survey results to the advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import survey results

In this article, we discuss how to import survey results from a survey data source to Viva Insights.

>[!Important]
>If this isn't the first time you're importing survey data, jump to [For all imports](#for-all-imports).

## For the first import

The first time you (the Insights Administrator) import survey results into Viva Insights, you'll need to coordinate a few tasks to get a survey import app set up in your tenant. Then, you can start your import.

### Workflow

1. The *survey source admin* [registers a multi-tenant application](#register-a-new-single-tenant-app-in-azure) on the Microsoft Entra admin center.
1. The *Microsoft 365 admin* [installs the Glint app](#install-the-app) on the Azure portal. 
1. You as the *Insights Administrator* ("Insights admin") [set up the import](#set-up-a-new-import-in-viva-insights) in the advanced insights app.

### Generate the security certificate 

*Applies to: survey source admin*

To get data into Viva Insights, the Microsoft 365 admin needs to create and register an app in Azure. As the data source admin, you’ll need to help the Microsoft 365 admin register their app by giving them a security certificate.

Here’s what to do: 

1.	Create a certificate by following the instructions in this article: [Create a self-signed public certificate to authenticate your application](/azure/active-directory/develop/howto-create-self-signed-certificate).
2.	Send the generated certificate to the Microsoft 365 admin. 



### Register a new single-tenant app in Azure

*Applies to: survey source admin*

>[!Note]
>For more information about registering an app in Azure, refer to [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app#register-an-application).

1. From the Microsoft admin center's left rail, select **All admin centers**. This option appears as the last one on the list.

    :::image type="content" source="../images/admin-di-all-admin-centers.png" alt-text="Screenshot that shows selecting All admin centers from the left rail.":::

1. Select **Microsoft Entra ID**.

1. Create a new app registration:
    1. In the top toolbar, select **Add > App registration**.
    2. On the resulting screen:
        1. Give your app a name. 
        1. Under **Supported account types**, select the second option, **Accounts in any organizational directory (Any Microsoft Entra directory - Multitenant)**. 
        1. Select the **Register** button at the bottom of the screen.

        :::image type="content" source="../images/admin-import-survey.png" alt-text="Screenshot that shows Register an application screen with i, ii, and iii that correspond to the steps listed above."lightbox="../images/admin-import-survey.png":::
1. Add a certificate:    
    1. Select **Add a certificate or secret**.

        :::image type="content" source="../images/admin-di-secret.png" alt-text="Screenshot of the Application (client) ID.":::

    2. Select **Upload certificate**.
    
        :::image type="content" source="../images/admin-di-upload-cert.png" alt-text="Screenshot of the ID and certificate/secret pane.":::


    3. Upload the certificate that the data source admin gave you and add a **Description**. Select the **Add** button.

        :::image type="content" source="../images/admin-di-upload-cert-pane3.png" alt-text="Screenshot that shows the Upload certificate dialog box in Azure.":::
### Install the app

*Applies to: Microsoft 365 admin*

In the Azure portal, install the app the survey source admin created. For directions, refer to this Azure article: [Add an enterprise application](/azure/active-directory/manage-apps/add-application-portal#add-an-enterprise-application).


### Set up a new import in Viva Insights

*Applies to: Insights Administrator*

1. Set up a new import in one of two places: through the **Data hub** page or through the **Survey data** page. 
    1. Through **Data hub**:
        1. Under the **Data sources** pane on the right, go to **Survey data import** in the **Survey sources** section.
        1. Select **Start**.
    1. Through **Survey data**: 
        1. Next to **Select Survey data source**, select **Custom survey data import**.
1. Enter the app ID from the app registration process.

    >[!Note]
    >If you don't have this ID, contact your Microsoft 365 admin.

1. Select **Save**. Your import is now set up and ready to get data from the survey source.

## For all imports

### Send data from the survey source

*Applies to: survey source admin*

After the app is set up and the connection is ready in the advanced insights app, the survey source admin can push survey data to Viva Insights.

1.	In the survey app, set up an export to send survey data to Viva Insights after a specific survey closes.
2.	Select the specific survey and add date ranges to share with Viva Insights.


## Validation

After the Glint admin sends data, the app starts validating.

After this phase completes, validation has either succeeded or failed. Depending on the outcome, you’ll either receive a success notification or a failure notification in the top-right corner of the **Data connections** screen.

For information about what happens next, go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

### Validation succeeds

After successful validation, Viva Insights starts processing your new data. Processing can take between a few hours and a day or so. During processing, you’ll see a “Validated, processing” status on the **Import history** table.

After processing completes, it's either succeeded or failed. Depending on the outcome, you’ll either find a “Success” or “Validation failed” status in the **Import history** table.

#### Processing succeeds

When you find the “Success” status in the **Import history** table, the upload process is complete.

After you receive the “Success” status, you can select the view (eye) icon to see a summary of the validation results.


#### Processing fails

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. If you want to try running the import again, have the survey source admin resend their survey data. If you’re still getting a “Processing failed” status, [file a support ticket with us](/microsoft-365/admin/get-help-support#online-support).

### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the data source admin so they know what to correct before sending the data again. 

The data source admin might find the following section helpful to fix data errors in their export file.

#### About errors in data

*Applies to: survey source admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until you fix the source data. After you fix the source data, you'll need to push the data again to Viva Insights.

##### Survey error reference

You might get an error if the file:
* Is empty
* Isn't in .csv format
* Contains duplicate column headers (question labels)
* Is missing a column header (question label)
* Has a column header (question label) with invalid characters
* Has a field value that exceeds 128KB
* Has a field value that doesn't match the right data type (for example, integer instead of date)

You might also get an error if there's an issue with connection setup.

### Viewing information in the Data quality tab

The **Data quality** tab shows you the following information for each imported survey:

* **Data fields** – The question labels for your survey. When you create queries, you can filter and group employees in the organization by these data fields, so being familiar with them will give you insight into the types of queries to use for analysis.
* **Quality score** – The percentage of measured employees who have a non-blank value for the specified question label. This score is intended as guidance, not to be an absolute measure of quality. A quality score of more than 95% leads to better-quality insights. If quality scores are low, it's difficult to determine how people collaborate across different characteristics. Additionally, low quality scores on required data fields may give skewed (under-reported) metric calculations for metrics that rely on those attributes.
* **Last updated** – When the survey was sent to Viva Insights.
* **Employees with this field** – The number of measured employees and internal collaborators with a non-blank value for the question label.

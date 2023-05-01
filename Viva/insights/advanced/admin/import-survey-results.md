---
ROBOTS: NOINDEX, NOFOLLOW
title: Import survey results
description: Learn how to import survey results to the advanced insights app
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

# Import survey results from Glint 

In this article, we discuss how to import survey results from Glint to Viva Insights.

>[!Important]
>If this isn't the first time you're importing survey data, jump to [For all imports](#for-all-imports).

## For the first import

The first time you (the Insights Administrator) import survey results into Viva Insights, you'll need to coordinate a few tasks to get a Glint app set up in your tenant. Then, you can start your import.

### Workflow

1. The *Glint admin* [registers a multi-tenant application](#register-a-new-multitenant-app-in-azure) on the Azure Active Directory admin center.
1. The *Microsoft 365 admin* [installs the Glint app](#install-the-app) on the Azure portal. 
1. You as the *Insights Administrator* ("Insights admin") [set up the import](#set-up-a-new-import-in-viva-insights) in the advanced insights app.

### Register a new multitenant app in Azure

*Applies to: Glint admin*

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
        1. Under **Supported account types**, select the third option, **Accounts in any organizational directory (Any Azure AD directory - Multitenant)**. 
        1. Select the **Register** button at the bottom of the screen.

        :::image type="content" source="../images/admin-di-registration-3.png" alt-text="Screenshot that shows Register an application screen with i, ii, and iii that correspond to the steps listed above."lightbox="../images/admin-di-registration-3.png":::

### Install the app

*Applies to: Microsoft 365 admin*

In the Azure portal, install the app the Glint admin created. For directions, refer to this Azure article: [Add an enterprise application](/azure/active-directory/manage-apps/add-application-portal.md#add-an-enterprise-application).


### Set up a new import in Viva Insights

*Applies to: Insights admin*

1. Set up a new import in one of two places: through the **Data hub** page or through the **Survey data** page. 
    1. Through **Data hub**:
        1. Under the **Data sources** pane on the right, go to **Survey data import** in the **Survey sources** section.
        1. Select **Start**.
    1. Through **Survey data**: 
        1. Next to **Current source: Glint**, select **Start**.
1. If your Glint tenant uses the default app ID, you'll notice the app ID prefilled in the **App ID** field. If your Glint tenant *doesn't* use the default app ID, enter the app ID from the app registration process. 

    >[!Note]
    >If you don't have this ID, contact your Microsoft 365 admin.

1. Select **Save**. Your import is now set up and ready to get data from Glint.

## For all imports

### Send data from Glint

*Applies to: Glint admin*

After the app is set up and the connection is ready in the advanced insights app, you as the Glint admin can push survey data to Viva Insights.

1. In Glint, set up an export to send survey data to Viva Insights after a specific survey closes.
1. Set up a connection to Viva Insights, name it, select the specific survey, and add date ranges to share with Viva Insights.
1. Select **Submit**.


## Validation

After the Glint admin sends data, the app starts validating.

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

If processing fails, you’ll find a “Processing failed” status in the **Import history** table. For processing to succeed, the Glint admin needs to correct errors and push the data to Viva Insights again. If they've corrected all errors and are still getting a “Processing failed” status, file a support ticket with us.

### Validation fails

If data validation fails, you'll see a "Validation failed" status in the **Import history** table. For validation to succeed, the data source admin needs to correct errors and push the data to Viva Insights again. Under **Actions**, select the download icon to download an error log. Send this log to the data source admin so they know what to correct before sending the data again. 

The data source admin might find the following section helpful to fix data errors in their export file.

#### About errors in data

*Applies to: Glint admin*

When any data row or column has an invalid value for any attribute, the entire import will fail until you fix the source data. After you fix the source data, you'll need to push the data again to Viva Insights.

In this release, only Standard Survey categories are ingested with mapping from Glint. Custom categories will result in an error.

##### Survey error reference

You might get an error if the file:

* Is empty
* Is over 1GB
* Isn't in .csv format
* Contains duplicate column headers
* Is missing a column header
* Has a column header with invalid characters
* Has a field value that exceeds 128KB
* Has a field value that doesn't match the right data type (for example, integer instead of date)

You might also get an error if there's an issue with connection setup.

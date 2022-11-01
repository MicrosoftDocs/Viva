---
title: "BigQuery Integration"
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to integrate your Viva Goals OKRs with BigQuery Data"
---

# BigQuery integration

Viva Goals can integrate with Google BigQuery to automatically update your OKRs.
  
Consider this example: You have data in your BigQuery warehouse that tracks the number of converted leads. Your goal is to increase the value of converted leads to a certain amount. If you implement BigQuery integration, you can save yourself from repeatedly going back and forth between BigQuery and Viva Goals to update your progress. Viva Goals will sync the values for you and chart your progress toward goals, saving time and keeping your OKRs current.

## Step 1: Set up the service account in the Google Cloud admin console

Viva Goals uses a service account with OAuth 2.0 to call into the Google BigQuery APIs. For  BigQuery integration, you need to add the Viva Goals service account, *ally-bigquery@ally-346417.iam.gserviceaccount.com*, to your BigQuery project and provide the required access and permissions. Read on for step by step instructions.

### Create an IAM role for BigQuery
  
Follow these steps in your Google Cloud platform console to create a role:

1. Log in to your google cloud platform developers console, https://console.developers.google.com/.

2. Go to the "hamburger" menu in the upper-left corner of the screen and choose **IAM & Admin** -> **Roles**.

    :::image type="content" source="../media/goals/goals-create-IAM-role-for-bigQuery.png" alt-text="Screenshot shows where you create an IAM role for BigQuery." lightbox="../media/goals/goals-create-IAM-role-for-bigQuery.png":::

3. At the top of the roles screen, select **+ Create Role**.

    :::image type="content" source="../media/goals/goals-create-role.png" alt-text="Screenshot shows the create role option." lightbox="../media/goals/goals-create-role.png":::

4. Enter the details in the form. Then select **Add Permissions** and add the following permissions:

    bigquery.datasets.get

    bigquery.jobs.create

    bigquery.tables.get

    bigquery.tables.getData

5. Select **Create** to complete role creation.

### Provide access to the Viva Goals service account

Now it's time to assign the new role to the Viva Goals service account so Viva Goals has permissions to read information from BigQuery and connect it to your OKRs.

1. Go to the "hamburger" menu in the upper-left corner of the screen and choose **IAM & Admin** -> **IAM**.
  
    :::image type="content" source="../media/goals/8/bigquery-iam-tab.png" alt-text="Screenshot shows where you choose IAM under IAM & Admin." lightbox="../media/goals/8/bigquery-iam-tab.png":::

2. Select the **+ Add** button at the top of the page.
  
    :::image type="content" source="../media/goals/8/bigquery-add-button.png" alt-text="Screenshot shows where you select the Add button." lightbox="../media/goals/8/bigquery-add-button.png":::

3. For **Add screen**, add the Viva Goals service account email, as noted below, in the **New Principals** field:

    ally-bigquery@ally-346417.iam.gserviceaccount.com
  
    :::image type="content" source="../media/goals/8/bigquery-details.png" alt-text="Screenshot shows where you add the service email account in the New Principals field." lightbox="../media/goals/8/bigquery-details.png":::

4. Select **Save** to complete setup.

## Step 2: Set up BigQuery integration in Viva Goals

The admin can follow these steps to set up BigQuery integration in Viva Goals:

1. Go to the Viva Goals integrations page through **Admin** > **Integrations**.
  
    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Screenshot shows the Viva Goals integrations page." lightbox="../media/goals/8/viva-goals-integrations-page.png":::
    
2. Scroll through the integration options until you find BigQuery. Select **enable** if this is the first time or **manage** if an integration was previously established.
  
    :::image type="content" source="../media/goals/8/bigquery-enable-button.png" alt-text="Screenshot shows where you enable BigQuery in Viva Goals." lightbox="../media/goals/8/bigquery-enable-button.png":::
  
3. Select **New Connection**. In the dialog that opens, enter the connection name and the BigQuery Project ID that holds the data you want to connect to your OKRs.
  
    :::image type="content" source="../media/goals/8/bigquery-new-connection-button.png" alt-text="Screenshot highlights the New Connection option." lightbox="../media/goals/8/bigquery-new-connection-button.png":::
  
4. Viva Goals uses a service account with OAuth 2.0 to call into the Google BigQuery APIs. Add the Viva Goals service account to your BigQuery project and provide the required access and permissions.
  
    :::image type="content" source="../media/goals/8/bigquery-configure-new-connection.png" alt-text="Screenshot shows where you configure a new BigQuery connection in Viva Goals." lightbox="../media/goals/8/bigquery-configure-new-connection.png":::
  
5. Select **Next** to finish setup.

Viva Goals lets you connect with multiple BigQuery projects. Select **New connection** to add another connection. You differentiate connections by name. Those names are displayed to members when they link their OKRs to BigQuery data.

## Step 3: Use BigQuery integration

After setup is complete, users in your organization can link the success of their OKRs directly to data in BigQuery cloud datasets.

1. When you create or edit an objective or key result, select **Connect data source to auto-update progress**.
2. From the list of integrations, select **BigQuery.**
  
    :::image type="content" source="../media/goals/8/bigquery-datasource.png" alt-text="Screenshot shows where you select BigQuery from the list of data sources in Viva goals." lightbox="../media/goals/8/bigquery-datasource.png":::
  
3. If you already created a BigQuery connection, or an administrator in your organization shared a BigQuery connection with you, that connection will be automatically selected. If no connections were already created or shared, Viva Goals will prompt you to add a new connection.
4. Add the BigQuery SQL query that will return a single-valued numeric value. This value will be connected to the OKR's progress or KPI depending on how the OKR is measured.
  
    :::image type="content" source="../media/goals/8/bigquery-connection-details.png" alt-text="Screenshot shows where you add a new BigQuery connection to OKRs in Viva goals." lightbox="../media/goals/8/bigquery-connection-details.png":::
  
5. Select **Next** to finish and save your OKR. You should now see a BigQuery icon next to the OKR. The OKR will sync automatically every hour, but you can also select **refresh**  to refresh it manually.

---
title: "BigQuery Integration"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to integrate your Viva Goals OKRs with BigQuery Data"
---

# BigQuery integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals can integrate with Google BigQuery to automatically update your OKRs. 
  
Take this example: you have data inside your BigQuery warehouse to track the number of converted leads. The goal is to increase the value of converted leads to a certain amount. By implementing a BigQuery integration, you can save yourself the hassle of repeatedly going back and forth between BigQuery and Viva Goals to update your progress. Viva Goals will sync the values for you and chart your progress toward goals, saving time and keeping OKRs current.

## Step 1: Set up the service account in the Google Cloud admin console 

Viva Goals uses a service account with OAuth 2.0 to call into the Google BigQuery APIs. For the BigQuery integration to work, you need to add the Viva Goals service account (ally-bigquery@ally-346417.iam.gserviceaccount.com) to your BigQuery project and provide the required access & permissions. Read on for step by step instructions.

### Create an IAM role for BigQuery
  
Follow the steps below in your Google Cloud platform console to Create a role.

1. Log in to your google cloud platform developers console - https://console.developers.google.com/

2. Navigate to the hamburger menu on the top left corner of the screen and choose IAM & Admin -> Roles.

    :::image type="content" source="../media/goals/goals-create-IAM-role-for-bigQuery.png" alt-text="Image of create a IAM Role for BigQuery " lightbox="../media/goals/goals-create-IAM-role-for-bigQuery.png":::

3. From the roles screen, select the + Create Role on the top of the page.

    :::image type="content" source="../media/goals/goals-create-role.png" alt-text="Image of create role" lightbox="../media/goals/goals-create-role.png":::

4. Fill in the details in the form and proceed to "Add Permissions" and add the following permissions

bigquery.datasets.get

bigquery.jobs.create

bigquery.tables.get

bigquery.tables.getData

5. Select Create to complete the role creation.

### Provide access to the Viva Goals service account

Now it's time to assign this role to Viva Goals' service account so that Viva Goals has permissions to read information from BigQuery and connect them to the OKRs.

1. Navigate to the hamburger menu on the top left corner of the screen and choose IAM & Admin -> IAM.
  
    :::image type="content" source="../media/goals/8/bigquery-iam-tab.png" alt-text="Choose IAM under IAM & Admin." lightbox="../media/goals/8/bigquery-iam-tab.png":::

2. Select the + Add button on top of the page.
  
    :::image type="content" source="../media/goals/8/bigquery-add-button.png" alt-text="Select the Add button on top of the page." lightbox="../media/goals/8/bigquery-add-button.png":::

3. In the Add screen add the Viva Goals' service account email (mentioned below) into the **New Principals** field.

ally-bigquery@ally-346417.iam.gserviceaccount.com
  
    :::image type="content" source="../media/goals/8/bigquery-details.png" alt-text="Add the service email account in the New Principals field." lightbox="../media/goals/8/bigquery-details.png":::

4. Select Save to complete setup.

## Step 2: Set up the BigQuery integration in Viva Goals

The admin can take the following steps to set up the BigQuery integration in Viva Goals: 

1. Navigate to the Viva Goals integrations page through **Admin > Integrations**.
  
    :::image type="content" source="../media/goals/8/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/8/viva-goals-integrations-page.png":::
    
2. Scroll through the integration options until you locate BigQuery, then select **enable** if this is the first time, or **manage** if an integration has already been established.
  
    :::image type="content" source="../media/goals/8/bigquery-enable-button.png" alt-text="Enabling BigQuery in Viva Goals." lightbox="../media/goals/8/bigquery-enable-button.png":::
  
3. Click on **New Connection**. In the popup that follows, enter the connection name and the BigQuery Project ID that holds the data you would like to connect to OKRs.
  
    :::image type="content" source="../media/goals/8/bigquery-new-connection-button.png" alt-text="Adding BigQuery connection in Viva Goals." lightbox="../media/goals/8/bigquery-new-connection-button.png":::
  
4. Viva Goals uses a service account with OAuth 2.0 to call into the Google BigQuery APIs. For the BigQuery integration to work, you need to add Viva Goals' service account to your BigQuery project and provide the required access & permissions.
  
    :::image type="content" source="../media/goals/8/bigquery-configure-new-connection.png" alt-text="Configuring new BigQuery connection in Viva Goals." lightbox="../media/goals/8/bigquery-configure-new-connection.png":::
  
5. Click **Next** to finish the setup.

Viva Goals allows you to connect with multiple BigQuery projects. Click **New connection** to add another and differentiate them using names. These names are displayed to members when they link their OKRs to BigQuery data.

## Step 3: Use the BigQuery integration

Once the setup is complete, users in your organization can link the success of their OKRs directly to data inside BigQuery cloud datasets.

1. While creating (or editing) an Objective or Key Result, click on **Connect data source to auto-update progress**.
2. From the list of integrations, pick BigQuery.
  
    :::image type="content" source="../media/goals/8/bigquery-datasource.png" alt-text="Selecting BigQuery from the list of data sources in Viva goals." lightbox="../media/goals/8/bigquery-datasource.png":::
  
3. If you already created a BigQuery connection, or an administrator in your organization shared a BigQuery connection with you, that will be automatically selected for you. If there are no connections created or shared already, Viva Goals will prompt you to add a new connection.
4. Add the BigQuery SQL query that will return a single-valued numeric value. This value will be connected to the OKR's progress or KPI depending on how the OKR is measured.
  
    :::image type="content" source="../media/goals/8/bigquery-connection-details.png" alt-text="Adding new BigQuery connection to OKRs in Viva goals." lightbox="../media/goals/8/bigquery-connection-details.png":::
  
5. Hit **next** to finish and save your OKR. You should now see a BigQuery icon next to the OKR. The OKR will sync automatically every hour, but you can refresh it manually by clicking on **refresh**.

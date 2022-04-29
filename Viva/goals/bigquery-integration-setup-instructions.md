---
title: BigQuery integration - setup instructions
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

description: "This article describes the setup that is required to be completed by the BigQuery administrator of the organization."
---

# BigQuery integration - setup instructions

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals can integrate with Google BigQuery to automatically update your OKRs. For example, you have the data inside your BigQuery warehouse to track the number of converted leads. The goal is to increase the value of converted leads to a certain amount. By implementing a BigQuery integration, you can save yourself the hassle of repeatedly going back and forth between BigQuery and Viva Goals to update your progress: Viva Goals will sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## Setting up BigQuery integration

Viva Goals uses a [service account with OAuth 2.0](https://developers.google.com/identity/protocols/oauth2/service-account) to call into the Google BigQuery APIs. For the BigQuery integration to work, you need to add Viva Goals' service account (ally-bigquery@ally-346417.iam.gserviceaccount.com) to your BigQuery project and provide the required access & permissions. Read on for step by step instructions.

## Create a IAM role for BigQuery 

Follow the steps below in your google cloud platform console to Create a role.

1. Log in to your google cloud platform developers console - https://console.developers.google.com/

2. Navigate to the hamburger menu on the top left corner of the screen and choose **IAM & Admin -> Roles**.

    :::image type="content" source="../media/goals/goals-create-IAM-role-for-bigQuery.png" alt-text="Image of create a IAM Role for BigQuery ":::

3. From the roles screen, select the **+ Create Role** on the top of the page. 

    :::image type="content" source="../media/goals/goals-create-role.png" alt-text="Image of create role":::

4. Fill in the details in the form and proceed to "Add Permissions" and add the following permissions

    - `bigquery.datasets.get`
    
    - `bigquery.jobs.create`
    
    - `bigquery.tables.get` 
    
    - `bigquery.tables.getData`
    
:::image type="content" source="../media/goals/goals-add-permissions.png" alt-text="Image of add permissions":::

5. Select **Create** to complete the role creation.

## Provide access to Viva Goals' service account

Now it's time to assign this role to Viva Goals' service account so that Viva Goals has permissions to read information from BigQuery and connect them to the OKRs.

1. Navigate to the hamburger menu on the top left corner of the screen and choose **IAM & Admin -> IAM**. 

2. Select the **+ Add** button on top of the page. 

    :::image type="content" source="../media/goals/goals-access-to-viva-goals-service-account.png" alt-text="Image of access to Viva Goals' service account":::

3. In the Add screen add the Viva Goals' service account email (mentioned below) into the members field.

    -  ally-bigquery@ally-346417.iam.gserviceaccount.com

4. Select **Save** to complete setup.

    :::image type="content" source="../media/goals/goals-complete-setup.png" alt-text="Image of complete setup":::

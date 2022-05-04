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

## How to set up the BigQuery integration

An admin can set up the BigQuery integration in Viva Goals. Take the following steps: 

1. Navigate to Ally’s integrations page through **Admin > Integrations**.
1. Scroll through the integration options until you locate BigQueary, then select **enable** if this is the first time, or **manage** if an integration has already been established.
1. Click on **New Connection**. In the popup that follows, enter the connection name and the BigQuery Project ID that holds the data you would like to connect to OKRs.
1. Viva Goals uses a service account with OAuth 2.0 to call into the Google BigQuery APIs. For the BigQuery integration to work, you need to add Viva Goals' service account to your BigQuery project and provide the required access & permissions. [Please click here for step by step instructions to complete setup](https://help.ally.io/en/articles/4089956-bigquery-integration-setup-instructions).
1. Click **Next** to finish the setup.

Viva Goals allows you to connect with multiple BigQuery projects. Click **New connection** to add another and differentiate them using names. These names are displayed to members when they link their OKRs to BigQuery data.

## How to use the BigQuery integration

Once the setup is complete, users in your organization can link the success of their OKRs directly to data inside BigQuery cloud datasets.

1. While creating (or editing) an Objective or Key Result, click on **Connect data source to auto-update progress**.
1. From the list of integrations, pick BigQuery.
1. If you already created a BigQuery connection, or an administrator in your organization shared a BigQuery connection with you, that will be automatically selected for you. If there are no connections created or shared already, Ally will prompt you to add a new connection.
1. Add the BigQuery SQL query that will return a single-valued numeric value. This value will be connected to the OKR's progress or KPI depending on how the OKR is measured.
1. Hit **next** to finish and save your OKR. You should now see a BigQuery icon next to the OKR. The OKR will sync automatically every hour, but you can refresh it manually by clicking on **refresh**.

The colors of the progress bars indicate the status of the objective.

- If the progress is 0-25% less than expected progress at any point in time, the status is Behind (orange)
- If the progress is over 25% less than expected progress at any point in time, the status is At-Risk (red)

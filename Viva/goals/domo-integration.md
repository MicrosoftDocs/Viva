---
ms.date: 04/17/2022
title: "Domo integration"
ms.reviewer: 
ms.author: rasanders
author: rasanders
manager: Liz.Pierce
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

description: "Learn how to integrate your Domo datasets directly with Viva Goals to automate OKR success measurement."
---

# Domo integration

ThViva Goals Domo integration enables automated real-time tracking of OKR progress. 
  
Let's consider this example: You use Domo cards to visualize your sales team's close rate: quarter-to-date (QTD) versus goal. When you configure a Domo integration and set up a data link in Viva Goals, you can connect to other source sales systems, if all data integrations, aggregations, and key performance indicator (KPI) visualizations are already implemented in Domo. Viva Goals will automatically update OKR progress, which saves you time and brings all your data and progress in one place. 
  
## How to enable Domo integration

A Viva Goals admin can follow these steps to enable Domo Integration: 

1. Go to Viva Goals integrations page: **Admin > Integrations**.
  
    :::image type="content" source="../media/goals/7/viva-goals-integrations-page.png" alt-text="Screenshot shows the integrations page in Viva Goals." lightbox="../media/goals/7/viva-goals-integrations-page.png":::

2. Enable the Domo integration in the **Data Integrations** category.
  
    :::image type="content" source="../media/goals/7/domo-enable-button.png" alt-text="Screenshot shows where you enable Domo in Viva Goals." lightbox="../media/goals/7/domo-enable-button.png":::

   The integration can also be disabled at any time from the same section.
  
    :::image type="content" source="../media/goals/7/domo-disable-button.png" alt-text="Screenshot show where you disable Domo." lightbox="../media/goals/7/domo-disable-button.png":::

## How to configure Domo connection

In the **Connections** section, select **New Connection.** In the popup that appears, follow the prompts to configure the Domo connection by using a Domo client ID and secret. The connection can be shared with all users or made private. You can also edit a saved Domo connection from the same section.
  
  :::image type="content" source="../media/goals/7/domo-creating-new-connection.png" alt-text="Screenshot shows the dialog box where you enter new Domo connection details." lightbox="../media/goals/7/domo-creating-new-connection.png":::

To create a Domo client ID and secret, visit [https://developer.domo.com/new-client](https://developer.domo.com/new-client) and sign in with your Domo domain and credentials. Enter **Name** and **Description** details, and then select **Data** as **Application scope**.

## How to set up the Domo data link

After the connection is configurated, users can **Edit** their Viva Goals OKRs to set up a Data Link to directly track progress from their Domo datasets.  

> [!NOTE]
> Domo integration is available only for the **KPI (success metric)** method of measuring OKR success, not for the **% completion** method.

1. When you create/edit an objective or key result, select **Add an integration**. Select **Domo** from the list of integrations.
  
   :::image type="content" source="../media/goals/7/domo-from-the-list-of-datasources.png" alt-text="Screenshot shows where you select Domo from the list of data sources in Viva goals." lightbox="../media/goals/7/domo-from-the-list-of-datasources.png":::

2. If a Domo connection isn't already configured, Viva Goals lets the user configure a connection. If one is already configured, Viva Goals lets users select a connection and set up a data link.

3. In the dialog that appears, follow the prompts to set up the Domo data link.  
  
4. Select **Connection**, enter the **DataSet-ID**,and your **KPI** from the list of measures/dimensions available in the selected dataset.
  
   :::image type="content" source="../media/goals/7/domo-new-connection-details.png" alt-text="Screenshot shows where you specify the KPI measurement type." lightbox="../media/goals/7/domo-new-connection-details.png":::

   > [!NOTE]
   > To obtain the DataSet-ID: Log in to your Domo instance and select the Dataset name mentioned under the card.

5. Copy the 36-character DataSet-ID from the URL of the DataSet page.

6. If there are multiple values for the KPI and you have the *close rate* for all your sales team members as part of the Domo dataset, you can apply a function (sum/average/count) on the set of values. For example, average of close rate for the entire sales team.

    Or, apply any available dataset fields as **Filters**. For example, filter a particular AE name.

    Viva Goals displays the final KPI value for your reference before saving the data link setup.


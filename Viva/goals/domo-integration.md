---
title: "Domo Integration"
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

description: "Learn how to integrate your Domo datasets directly with Viva Goals to automate OKR success measurement."
---

# Domo Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals' Domo integration allows automated real-time tracking of Objectives and Key Results (OKR) progress. For example, you use Domo cards to visualize the Sales teams' close rate - Quarter-to-date (QTD) vs Goal. By configuring a Domo integration and setting up a data-link within Viva Goals, you can save the hassle of reinventing the wheel by connecting to other source sales systems (as all data integrations, aggregations and key performance indicator (KPI) visualizations have already been implemented within Domo). Viva Goals will automatically update OKR progress, thus saving time.

## Enable the Domo Integration

A Viva Goals admin can enable the Domo Integration on Viva Goals. To do so:

1. Navigate to Viva Goals’ Integrations page through **Admin > Integrations**.

2. Enable the Domo Integration under the **Data Integrations** category.

3. The Integration can also be disabled at any time from the same section.

    :::image type="content" source="../media/goals/viva-goals-domo-integration-1.png" alt-text="Domo Integration 1":::

## Configuring the Domo Connection

In the **Connections** section, select **New Connection** and in the popup that appears, follow the prompt to configure the Domo connection using a Domo Client ID & Secret. A connection can be shared with all users or made private based on the user's preference. Editing a saved Domo connection is also allowed from the same section at any time.

:::image type="content" source="../media/goals/viva-goals-domo-integration-2.png" alt-text="Domo Integration 2":::

To create a Domo Client ID & Secret, visit [https://developer.domo.com/new-client](https://developer.domo.com/new-client), sign in with your Domo domain & credentials. Enter **Name** and **Description** details and select **Data** as **Application scope**.

:::image type="content" source="../media/goals/viva-goals-domo-integration-3.png" alt-text="Domo Integration 3":::

## Setting up the Domo Data Link

Once the connection configuration is done, users can **Edit** their Viva Goals OKRs to set up a Data Link to directly track progress from their Domo datasets.  

> [!NOTE]
> Domo Integration is available only for **KPI (success metric)** method of measuring OKR success and not for **% completion** method.

1. While creating/editing an Objective or Key Result, select **Add an integration**. Select **Domo** from the list of integrations.

2. If a Domo Connection isn't configured, Viva Goals also allows the user to configure a connection right there. If already configured, Viva Goals allows the users to proceed with setting up the data link by selecting an available connection.

    :::image type="content" source="../media/goals/viva-goals-domo-integration-4.png" alt-text="Domo Integration 4":::

In the popup that appears, follow the prompts to set up the Domo data link.  
Select **Connection**, key in **DataSet-ID**, your actual **KPI** from the list of measures/dimensions available on the selected dataset.

> [!NOTE]
> To obtain the DataSet-ID:</br>
> Login to your Domo instance and select the Dataset name mentioned under the card.

:::image type="content" source="../media/goals/viva-goals-domo-integration-5.png" alt-text="Domo Integration 5":::

Grab the 36 character DataSet-ID from the URL of the DataSet page.

:::image type="content" source="../media/goals/viva-goals-domo-integration-6.png" alt-text="Domo Integration 6":::

If there are multiple values for the KPI, and you have the Close Rate for all your sales team members as part of the Domo dataset, you can apply a function (sum/average/count) on the set of values. For example, average of Close Rate for the entire sales team.</br>
or</br>
Apply any available dataset fields as **Filters**. For example, filter a particular AE Name - Adam's Close Rate.

Viva Goals displays the final KPI value for your reference before saving the data link set-up.

:::image type="content" source="../media/goals/viva-goals-domo-integration-7.png" alt-text="Domo Integration 7":::

It’s as easy as that! Now you know how to work smarter by integrating Viva Goals with Domo.

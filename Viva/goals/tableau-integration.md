---
title: "Tableau Integration"
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

description: "Learn how to integrate your Tableau dashboard KPIs directly with Viva Goals to automate OKR success measurement."
---

# Tableau integration

The Viva Goals Tableau integration enables automated real-time tracking of objectives and key result (OKR) progress. 
  
Let's consider this example: You have Tableau workbooks with dashboard views that are used to visualize the sales team's close rate, quarter-to-date (QTD) versus goal. You configure Tableau integration and set up a data link in Viva Goals to save the hassle of connecting to any other source sales systems. If you've already implemented all the key performance indicator (KPI) visualizations in Tableau, Viva Goals will sync the values for you, saving you time while keeping your OKR progress up to date.

## How to enable Tableau integration

Admins follow these steps to enable Tableau integration in Viva Goals: 

1. Go to the Viva Goals integrations page: **Admin** > **Integrations**.
  
    :::image type="content" source="../media/goals/7/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/7/viva-goals-integrations-page.png":::

2. Enable Tableau integration under the **Data Integrations** category.
  
    :::image type="content" source="../media/goals/7/tableau-enable-button.png" alt-text="Screenshot shows where you enable Tableau in Viva Goals." lightbox="../media/goals/7/tableau-enable-button.png":::

   You can also disable integration at any time from the same section.
  
    :::image type="content" source="../media/goals/7/tableau-disable-button.png" alt-text="Screenshot shows where to disable Tableau in Viva Goals." lightbox="../media/goals/7/tableau-disable-button.png":::

## How to configure the Tableau connection

In the **Connections** section, select **New Connection**. In the dialog that appears, use a personal access token or the user name and password method to configure the Tableau connection.
  
  :::image type="content" source="../media/goals/7/tableau-creating-new-connection.png" alt-text="Screenshot shows where you enter a name for your new connection and the Tableau URL." lightbox="../media/goals/7/tableau-creating-new-connection.png":::

> [!NOTE]
> Personal access token should be available from the Tableau 2019.4 release.

Select the  information icon (**i**) to learn more about each field in the dialog. Help article link are also provided.

Connections can be shared or made *private*.  

You can edit a saved Tableau connection from the same section at any time.  
  
> [!NOTE]
> If your organization uses an on-premises Tableau Server, such as  `https://tableau.\<org-name\>.com`), restrictions apply to external connections that can access the server. In this scenarios, contact your Viva Goals customer success manager (CSM), to learn which IPs must be permitted to establish the connection.

## How to set up the Tableau data link

After the connection is configured, users can **Edit** their OKRs to set up a data link integration to track progress in Viva Goals from their Tableau workbooks.

> [!NOTE]
> Tableau Integration is available only for the **KPI (success metric)** method of measuring OKR success. It's not available for **% completion** method.

1. When you create or edit an objective or key result, select **Add an integration**, and then select **Tableau** from the list of integrations.
  
    :::image type="content" source="../media/goals/7/tableau-from-the-list-of-datasources.png" alt-text="Screenshot shows where you select Tableau as the data source for the new connection." lightbox="../media/goals/7/tableau-from-the-list-of-datasources.png":::

1. If a Tableau connection isn't already configured, Viva Goals prompts the user to configure a connection. If a connection is already configured, Viva Goals prompts the user to set up the data link.

1. In the dialog that appears, follow the steps to set up the Tableau data link integration. Select **Workbook**, **View** (Dashboards or Standalone Worksheets), and your **KPI** from the list of measures/dimensions available on the selected **View**.  
  
   :::image type="content" source="../media/goals/7/tableau-connection-details.png" alt-text="Screenshot shows where you specify the table workbook, view, and measure for your new Tableau connection." lightbox="../media/goals/7/tableau-connection-details.png":::

   If there are multiple instances for the KPI value, for example, you have the sales goal for all your sales team members as part of the Tableau View, you can choose to apply a sum/average/count on the set of values (or) filter out by a particular person or any available filter field.  

   Viva Goals displays the selected value for your reference before you save the data link set up.

> [!NOTE]
> Based on Tableau REST API limitations, Viva Goals currently has visibility only into published workbooks and views. If any worksheets already part of a workbook are hidden, they will not be displayed. Unhide all worksheets from which your team would like to integrate KPIs before you publish the Tableau dashboards.
  
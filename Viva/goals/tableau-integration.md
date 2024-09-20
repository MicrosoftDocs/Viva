---
ms.date: 05/06/2024
title: Tableau integration
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150
description: "Learn how to integrate your Tableau dashboard KPIs directly with Viva Goals to automate OKR success measurement."
---

# Tableau integration

The Viva Goals Tableau integration enables automated real-time tracking of OKR progress. For example, if you have Tableau workbooks with dashboard views that are used to visualize the sales team's close rate (quarter-to-date versus goal), you can integrate Tableau to set up a data link in Viva Goals and avoid the hassle of connecting to other source sales systems. If you've already implemented all the key performance indicator (KPI) visualizations in Tableau, Viva Goals will sync the values for you, saving you time while keeping your OKR progress up to date.

> [!NOTE]
> At present, integrations are only supported for Tableau in the cloud; they are not available for Tableau on premises.

## Enable Tableau integration

Admins can follow these steps to enable Tableau integration in Viva Goals:

1. Go to the Viva Goals integrations page: **Admin** > **Integrations**.

1. Enable Tableau integration under the **Data Integrations** category.

   You can also disable the integration at any time from the same section.

## Configure a Tableau connection

1. Go to **Admin** > **Integrations**.

1. Select **Manage** next to Tableau under **Data Integrations**.

1. In the **Connections** section, select **New Connection**.

1. In the dialog that appears, use a personal access token or the user name and password method to configure the Tableau connection. Select the  information icon (**i**) to learn more about each field in the dialog. Help article links are also provided.

> [!NOTE]
> Personal access tokens should be available per the Tableau 2019.4 release.

Connections can be shared or made *private*.  

You can edit a saved Tableau connection from the same section at any time.

## Set up a Tableau data link

After the connection is configured, users can **Edit** their OKRs to set up a data link integration to track progress in Viva Goals from their Tableau workbooks.

> [!NOTE]
> Tableau integration is only available for the **KPI (success metric)** method of measuring OKR success. It's not available for the **% completion** method.

1. When you create or edit a key result, open the **Progress and Status** dropdown. In the section with the text "Connect to a data source for automatic progress updates", find and select the icon for Tableau.

1. If a Tableau connection hasn't already been configured, Viva Goals will prompt you to configure a connection. If a connection has already been configured, Viva Goals will prompt you to set up the data link.

1. In the dialog that appears, follow the steps to set up the Tableau data link integration. Select a **Workbook**, **View** (Dashboards or Standalone Worksheets), and your **KPI** from the list of measures/dimensions available on the selected **View**.  

   If there are multiple instances for the KPI value (for example, you have the sales goal for all your sales team members as part of the Tableau view), you can choose to apply a sum/average/count on the set of values or filter out by a particular person/filter field.  

   Viva Goals displays the selected value for your reference before you save the data link setup.

> [!NOTE]
> Based on Tableau REST API limitations, Viva Goals currently has visibility only into published workbooks and views. If any worksheets already part of a workbook are hidden, they will not be displayed. Unhide all worksheets from which your team would like to integrate KPIs before you publish the Tableau dashboards.

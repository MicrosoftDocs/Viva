---
title: "Tableau Integration"
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

description: "Learn how to integrate your Tableau dashboard KPIs directly with Viva Goals to automate OKR success measurement."
---

# Tableau Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals' Tableau integration allows automated real-time tracking of Objectives and Key Results (OKR) progress. For example, you have Tableau workbooks with dashboard views used to visualize the Sales teams' close rate - Quarter-to-date (QTD) vs Goal. By configuring a Tableau integration and setting up a data-link within Viva Goals, you can save the hassle of connecting to any other source sales systems and reinventing the wheel (as you've already implemented all the key performance indicator (KPI) visualizations within Tableau). Viva Goals will sync the values for you, thus saving time while keeping your OKRs progress up-to-date.

## Enable the Tableau Integration

A Viva Goals admin can enable the Tableau Integration on Viva Goals. To do so:

1. Navigate to Viva Goals’ integrations page through **Admin > Integrations**.

2. Enable the Tableau Integration under the **Data Integrations** category.

3. The Integration can also be disabled at any time from the same section.

## Configure the Tableau Connection

In the **Connections** section, select **New Connection** and in the popup that appears, follow the prompt to configure the Tableau connection either using a Personal Access Token (or) the Username & Password method.

> [!NOTE]
> Personal Access Token should be available from the Tableau 2019.4 release.

Select the (**i**) information icon to know more about each field in the popup. Links to help articles are provided as required.

A connection can be Shared or made Private based on the user's preference.  
Editing a saved Tableau connection is also allowed from the same section at any time.  
  
> [!NOTE]
> In case your organization uses an on-premise Tableau Server (For example, `https://tableau.\<org-name\>.com`) and it has restrictions on what external connections can access the server, let your Viva Goals Customer Success Manager (CSM) know, so we can share the IPs that need to be permitted for establishing the connection successfully.

## Setting up the Tableau Data Link

Once the connection configuration is done, users can **Edit** their OKRs to set up a Data Link integration to directly track progress in Viva Goals from their Tableau workbooks.

> [!NOTE]
> Tableau Integration is available only for **KPI (success metric)** method of measuring OKR success and not available for **% completion** method.

1. While creating/editing an Objective or Key Result, select **Add an integration**, then select **Tableau** from the list of integrations.

2. If a Tableau Connection isn't configured, Viva Goals allows the user to configure a connection first. If already configured, Viva Goals allows the users to proceed with setting up the data link.

In the popup that appears, follow the prompts to set up the Tableau data link integration.
Select **Workbook**, **View** (Dashboards or Standalone Worksheets), your actual **KPI** from the list of measures/dimensions available on the selected **View**.  

If there are multiple instances for the KPI value, for example, you have the Sales Goal for all your sales team members as part of the Tableau View, you can choose to apply a sum/average/count on the set of values (or) filter out by a particular person or any available filter field.  

Viva Goals displays the selected value for your reference before you save the data link set up.

It’s as easy as that! Now you know how to work smarter by integrating Viva Goals and Tableau.

We're building more awesome use cases that will help you achieve amazing results.  

> [!NOTE]
> Based on the Tableau REST API limitations, Viva Goals currently has visibility of only the published Workbooks & Views. If any worksheets already part of a workbook are hidden, then they will not show up on the Views. Ensure to un-hide all the worksheets from where your team would like to integrate KPIs before publishing the Tableau dashboards.
  

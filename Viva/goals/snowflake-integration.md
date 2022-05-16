---
title: Snowflake integration
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
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
description: "Learn how to integrate your Viva Goals OKRs with Data in Snowflake."
---

# Snowflake integration

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals can integrate with Snowflake to automatically update your OKRs. 

Let's take this example: You have data inside your Snowflake warehouse to track leads generated across multiple channels and your goal is to generate 4000 qualified leads from SEO By implementing a Snowflake integration, you can save yourself the hassle of repeatedly going back and forth between Snowflake and Viva Goals to update your progress. Viva Goals will sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## How to set up the Snowflake integration 

An admin can set up the Snowflake integration in Viva Goals. Take the following steps: 

1. Navigate to Viva Goals’ integrations page through **Admin > Integrations**.

2. Scroll through the integration options until you locate Snowflake, then select **enable** if this is the first time, or "manage" if an integration has already been established.

3. Click on **New Connection**. In the popup that follows, enter the connection name, Account URL, Username, Password and the warehouse. The warehouses should populate automatically to choose from if the credentials entered are correct. 

4. Click **Next** to finish the setup.

Viva Goals allows you to connect with multiple Snowflake warehouses. Click **New connection** to add another and differentiate them using names. These names are displayed to members when they link their OKRs to Snowflake data.

## How to use the Snowflake integration

Once the setup is complete, users in your organization can link the success of their OKRs directly to the data inside a Snowflake warehouse.

1. While creating (or editing) an Objective or Key Result, click on **Connect data source to auto-update progress**.
1. From the list of integrations, pick Snowflake.

1. If you already created a Snowflake connection, or an administrator in your organization shared a Snowflake connection with you, that will be automatically selected for you. If there are no connections created or shared already, Viva Goals will prompt you to add a new connection.
1. Add the Snowflake SQL query that will return a single-valued numeric value. This value will be connected to the OKR's progress or KPI depending on how the OKR is measured.

1. Hit **next** to finish and save your OKR. You should now see a Snowflake icon next to the OKR. The OKR will sync automatically every hour, but you can refresh it manually by clicking on **refresh**.

The colors of the progress bars indicate the status of the objective.

 - If the progress is 0-25% less than expected progress at any point in time, the status is Behind (orange).
 - If the progress is over 25% less than expected progress at any point in time, the status is At-Risk (red).

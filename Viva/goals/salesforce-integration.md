---
title: "Salesforce Integration"
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

description: "Learn how to integrate your Viva Goals OKRs with Salesforce reports."
---

# Salesforce Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals has the ability to integrate with Salesforce, allowing you to automatically update your Objectives and Key Results (OKRs). For example, if you have a Salesforce report that tracks converted leads, with a goal in mind to increase the value of converted leads to a certain amount, implementing a Salesforce integration will save you the hassle of repeatedly updating your progress in Viva Goals.

## Set up

An admin can set up the Salesforce integration in Viva Goals. To do so:

1. Navigate to Viva Goals’ integrations page through **Admin -> Integrations**.

2. Scroll through the list until you reach Salesforce. Select **Enable** (Or **Manage** if a connection has been made previously).

3. Select **"New Connection"** and follow the prompts to sign into your Salesforce account.

4. Select **"Next"** to finish the setup.

Viva Goals allows you to connect with multiple Salesforce accounts. Select **New connection** to add another account and differentiate them using names. These names are displayed to members when they link their OKRs to Salesforce reports.

## How to use the Salesforce Integration?

Once the setup is complete, users in your organization can link the success of their OKRs directly to fields in Salesforce reports.

1. While creating (or editing) an Objective or Key Result, navigate to the **Progress** section and select **Connect to a Data Source**.

2. From the list of integrations, select **Salesforce**.

3. Search for the name of the report you would like to connect. If you have multiple Salesforce connections, select the connection that your report is associated with before searching for the report.

4. **Select a field**: Select the field you would like to designate as the measure of success. The available fields will vary based on the configuration of the report selected.

5. Select **Next** followed by **Save** to complete the update for your OKR.

    You should now see a Salesforce icon next to the OKR. The OKR will sync automatically every hour, but to refresh it manually, go to the cloud icon and select **Sync**.

    The colors of the progress bars indicate the status of the Objective.

      - If the progress is 0-25% less than expected progress at any point in time, the status is Behind (orange).

      - If the progress is over 25% less than expected progress at any point in time, the status is At-Risk (red).


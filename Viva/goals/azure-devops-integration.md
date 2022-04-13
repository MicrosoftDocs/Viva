---
title: Azure DevOps integration
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
description: "Learn how to integrate your work items with OKRs in Viva Goals"
---

# Azure DevOps integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to Azure DevOps integration

Viva Goals’ Azure DevOps integration allows you to update your OKR progress automatically depending on the progress of work items in your Azure DevOps projects. Let’s say you use Azure DevOps to track the status of issues, and you've an objective in Viva Goals for resolving 30 issues every quarter. When you link this objective to the corresponding project in Azure DevOps, the status of your OKR will be updated as the work items under the associated project get resolved. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

### Enabling the Azure DevOps integration

Admins can enable this integration, and here’s how it can be done: 

- From the sidebar, click on **Admin** and select the **Integrations** tab. 
- Against Azure DevOps, you'll have an option to **enable** the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration. 
- This integration can also be **disabled** from the same section by clicking on **Change**, and choosing**Disable integration** from the dropdown.

### Configuring the Azure DevOps connection 

- After enabling the integration, the first step is to configure an Azure DevOps connection. 
- Select **New Connection**, and sign into your Azure DevOps account. 
- Provide a name for the connection, and furnish the **Account Name** and the **Project Name**. 
- It's optional to share this connection with other users in the organization. Click on Next to get up and running with this integration. You can edit the saved connection at any time.

Viva Goals allows you to connect with multiple projects. Select New Connection to fetch data from another project. You can differentiate these connections using names, and the names will be displayed to other users when they link their OKRs with Azure DevOps data.

### Connecting the Azure DevOps connection to an OKR

Once you've configured the connection, the next step is to start linking OKRs to the Azure DevOps projects.

- For the **Objectives and key results can be used interchangeably** OKR Model: While **creating or editing an OKR**, click on **Connect data source to auto-update progress**. From the drop down menu, select **Azure DevOps**. 

  > [!NOTE]
  > The option to connect to a data source will appear only for Key Results and not for Objectives if the **Objectives are always aspirational, key results are always measurable** OKR Model is being used.

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared. 
- Choose the method using which you want to measure the progress — percent complete or KPI (success metric). If you are choosing KPI, provide a metric, starting value, and target value. 
- Select a connection, and choose the **Query**. As soon as you choose a query, the **count of matching work items** will be displayed. 
- The progress will be calculated based on the count of tickets completed under the chosen query (if you've chosen KPI metric to track progress), or will be calculated based on the percentage of tickets closed (if you've chosen percent complete to track progress). 
- Click **Next > Save**.

:::image type="content" source="../media/goals/connection-to-an-okr.gif" alt-text="Connection to an OKR":::

You've successfully linked your objective to a query in Azure DevOps to track the progress of your work items, and update the status of the corresponding OKR automatically.


The colors of the progress bar indicated the status of the objective.

- If the progress is 0-25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange.
- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red.

To learn more about Viva Goals’ other integrations, see our [Integrations page](https://help.ally.io/en/collections/30526-integrations).
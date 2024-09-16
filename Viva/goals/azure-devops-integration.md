---
ms.date: 10/05/2023
title: Azure DevOps integration
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn how to integrate your Azure DevOps work items with OKRs in Viva Goals"
---

# Azure DevOps integration

## Introduction to Azure DevOps integration

Viva Goals integrates with Microsoft Azure DevOps to automatically update key results and projects in Viva Goals. Key Result and Project progress is updated automatically based on the connected Azure DevOps work items. You can use the Azure DevOps integration to

- Automatically track progress for a key result  
- Automatically track progress for an initiative KPI 
- Automatically track progress and tasks for an initiative.  
    - This approach updates initiative progress, syncs Azure DevOps work item details with Viva Goals initiative “tasks,” and, when used with the Viva Goals Azure DevOps extension, Viva Goals OKR alignment details are surfaced directly in Azure DevOps linked work items.

See below for more details on how the Azure DevOps integration works when connecting to key results, initiatives metrics, and initiative tasks. 

## Outcomes (OKRs) vs Outputs (Initiatives) 

One of the fundamental tenets of OKRs is distinguishing between outcomes versus outputs. OKRs, and key results, are focused on driving impact (i.e., outcomes), while Viva Goals [initiatives](/viva/goals/projects) are focused on outputs – the work that is planned to achieve the key results. Both are important metrics to track, but they measure different things.

While you can integrate both Viva Goals key results and initiatives with your Azure DevOps work items, it's important to understand the difference. Azure DevOps primarily focuses on tracking work, so it's more common to integrate Viva Goals initiatives with Azure DevOps. There are certain examples where it may make sense to track key result progress based on Azure DevOps work items.

## When to use the Azure DevOps Integration 

There are three ways to use the Azure DevOps integration with Viva Goals workflows. Details on each of these capabilities are described below:

1. **Track progress for an initiative with tasks:** In addition to tracking initiative progress based on Azure DevOps work items, this approach enables a cross-platform user experience. The Azure DevOps work item details are synced to the Viva Goals initiative views and the alignment of Azure DevOps work to Viva Goals OKRs can be viewed directly within the linked Azure DevOps work items via the Azure DevOps Extension (coming soon)
1. **Track progress for an initiative with KPIs:** This approach enables you to track initiative progress based on the Azure DevOps work items status. A single numeric value is synced with Viva Goals. 
1. **Track progress for a Key Result:** This approach enables you to track KR progress based on the Azure DevOps work items status. A single numeric value is synced with Viva Goals.

## How to set up Azure DevOps Integration  

The Azure DevOps integration needs to be enabled by a Viva Goals Tenant and Organization admin. Viva Goals admins must first enable the Azure DevOps integration for their tenant ([Enable Integrations in Viva Goals | Microsoft Learn](vg-integrations-administration-overview.md)). Once enabled at the tenant level, a Viva Goals Organization admin must then enable it for their org ([Viva Goals Integrations Administration Overview](vg-integrations-administration-overview.md).)

> [!NOTE]
> Once enabled, any user in the organization who has permissions to create/edit an OKR and/or initiative can set up integration between Viva Goals and Azure DevOps! 

## How to enable Azure DevOps integration with initiatives

This method is the recommended approach for aligning work in Azure DevOps to OKRsin Viva Goals. In addition to tracking initiative progress based on Azure DevOps work items, this approach enables a cross-platform user experience. The Azure DevOps work item details are synced to the Viva Goals initiative views and, when used with the Viva Goals Azure DevOps extension, the alignment of Azure DevOps work to Viva Goals OKRs is surfaced directly within the linked Azure DevOps work items.

1. Select **Add Initiative** in Viva Goals or edit an existing initiative. 
1. Select **Outcome**. 
1. Select **Add tasks**. 
1. Select **Automatically from a data source**. 
1. Select **Azure DevOps** from the list of available integrations.
1. Select the appropriate Azure DevOps connection. If you need to create a new Azure DevOps connection, you'll need to sign into Azure DevOps to create a data connection. A new connection is needed for each Azure DevOps project. After signing in:

    - Provide a connection name: We recommend including the Azure DevOps Organization and Project in the name for future reference.
    - Select the **Azure DevOps Organization**  
    - Select the **Azure DevOps Project** 
    - Select **Next** 
    
1. Select the connection method: 
    - **Shared Query:** enables you to connect to an existing query saved within Azure DevOps. 
    - **Work items:** enables you to connect to one or more work items of a specific work item type.  This approach allows you to connect directly to the “parent” work items that contain the supporting work;  the child work items are automatically included.

**If using the connect to ‘Shared Query’ method:** 

1. Select the **shared query** method. 
1. Search for and select the shared query that contains the Azure DevOps work items. 
1. Select the work item type you want to use for calculating progress of your initiative. You can choose from any work item type in the query or all work items in the shared query. 
1. Select the Azure DevOps field you want to use for tracking initiative progress. Viva Goals initiative progress is calculated as the % complete of the chosen work item type.
1. Select **Next.** 
1. Select **Save.** 

You should now see the Azure DevOps icon next to your initiative. You should also see the Azure DevOps work item details in your Viva Goals initiative views. Viva Goals will now automatically sync the work item details and update the initiative progress once per hour based on the ADO field for the work item types selected within your shared query.

**If using the Connect to Work Items method:**

1. Select **work items** method. 
1. Select the work item type to connect to – we recommend choosing the “parent” work item type in your Azure DevOps hierarchy that contains the work being done. The integration will automatically include the child work items. For example, connect to a feature that is the parent to the tasks versus connecting to each individual task. 
1. Search for and select the specific work item(s) of the chosen type.
1. Select the work item type you want to use for calculating progress of your initiative. You can choose to measure progress by a specific work item type (i.e., the type you directly connect to or any of its children types) or all work items (i.e., connected and children).  
1. Select the ADO field you want to use for tracking initiative progress. 
1. Select **Next**. 
1. Select **Save**. 

You should now see the Azure DevOps icon next to your initiative. You should also see the Azure DevOps work item details in your Viva Goals initiative views.  Viva Goals will now automatically sync the work item details and update this initiative progress once per hour based on the Azure DevOps field for the work item types selected.

After completion of the above steps, not only will the Viva Goals initiative progress be automatically updated regularly, but the following capabilities will be enabled:
 
- The Azure DevOps work item details are shown in the Viva Goals initiative views, along with hyperlinks to the Azure DevOps work item details 
- If you've enabled the Viva Goals Azure DevOps extension, the full alignment between OKRs and the Azure DevOps work items are accessible from a Viva Goals tab within the linked Azure DevOps work items. 

## How to use Azure DevOps Integration with initiative KPIs

Use this method when you want to update the Viva Goals initiative progress with a single numeric value. This approach won't surface the Azure DevOps work items within Viva Goals initiative views; nor does this method have the capability to embed Viva Goals within the Azure DevOps work items.

1. Select **Add Initiative** in Viva Goals or edit an existing initiative. 
1. Select **Outcome**. 
1. Select **Add Metric** and fill in on the necessary details (i.e., name, type, units, starting, target values)

    - For percentage-based metrics, the initiative progress is calculated based on the % of selected ADO field value for completed work items vs total work items. 
    - For non-percentage-based metrics (numeric, currency), the initiative progress is a count of the selected ADO field value for completed or, optionally, total work items. 
    
1. Select **Progress.** 
1. Select **Automatically from a data source.**
1. Select **Azure DevOps** from the list of available integrations.
1. Select the appropriate Azure DevOps connection.  If you need to create a new Azure DevOps connection, you need to sign into Azure DevOps to create a data connection. A new connection is needed for each Azure DevOps project. After signing in:

    - Provide a Connection Name: recommend including the Azure DevOps Organization and initiatives in the name for easy future reference. 
    - Select the **Azure DevOps Organization** 
    - Select the **Azure DevOps Project**
    - Select **Next** 
    
1. Select the connection method: 

    - **Shared Query:** enables you to connect to an existing query stored within Azure DevOps
    - **Work items:** enables you to connect to one or more work items of a specific work item type. This approach allows you to connect directly to the “parent” work items that contain the supporting work;  the child work items are automatically considered.

**If using the connect to ‘Shared Query’ method:** 

1. Select the **shared query** method. 
1. Search for and select the shared query that contains the Azure DevOps work items. 
1. Select the work item type you want to use for calculating progress of your initiative. You can choose from any work item type in the query or all work items in the query. 
1. Select the Azure DevOps field you want to use for tracking initiative progress.  
1. Select **Next.** 
1. Select **Save.** 

You should now see the Azure DevOps icon next to your initiative. Viva Goals will now automatically update the progress once per hour. 

**If using the Connect to Work Items method:**

1. Select **work items** method. 
1. Select the ‘work item type’ to connect to – we recommend choosing the “parent” work item type in your Azure DevOps hierarchy that contains the work being done. The integration will automatically include the child work items. For example, connect to a feature that is the parent to the tasks versus connecting to each individual task. 
1. Search for and select the specific work item(s) of the chosen type.
1. Select the work item type you want to use for calculating progress of your initiative. You can choose to measure progress by a specific work item type (i.e., the type you directly connect to or any of its children types) or all work items (i.e., connected and children).
1. Select the ADO field you want to use for tracking initiative progress. 
1. Select **Next**. 
1. Select **Save**. 

You should now see the Azure DevOps icon next to your initiative. Viva Goals will now automatically update this initiative once per hour.

## How to use Azure DevOps Integration with a Key Result

Use this method when you want to update the Viva Goals Key Result progress with a single numeric value. This approach won't surface the Azure DevOps work items within Viva Goals; nor does this method have the capability to embed Viva Goals within the Azure DevOps work items.

1. Select **Add Key Result** in Viva Goals or edit an existing Key Result 
1. Select **Add Metric** and fill in on the necessary details (i.e., name, type, units, starting, target values)

    - For percentage-based metrics, the key result progress is calculated based on the % of selected ADO field value for completed work items vs total work items. 
    - For non-percentage-based metrics (numeric, currency), the key result progress is a count of the selected ADO field value for completed or, optionally, total work items. 
    
1. Select **Progress.** 
1. Select **Automatically from a data source.**
1. Select **Azure DevOps** from the list of available integrations.
1. Select the appropriate Azure DevOps connection. If you need to create a new Azure DevOps connection, you need to sign into Azure DevOps to create a data connection. A new connection is needed for each Azure DevOps project. After signing in:

    - Provide a Connection Name: recommend including the Azure DevOps Organization and initiative in the name for easy future reference.
    - Select the **Azure DevOps Organization.**  
    - Select the **Azure DevOps Project.**
    - Select **Next.**
    
1. Select the connection method: 

    - **Shared Query:** enables you to connect to an existing query stored within Azure DevOps
    - **Work items:** enables you to connect to one or more work items of a specific work item type. This approach allows you to connect directly to the “parent” work items that contain the supporting work; the child work items are automatically considered.

**If using the connect to ‘Shared Query’ method:** 

1. Select the **shared query** method. 
1. Search for and select the shared query that contains the Azure DevOps work items. 
1. Select the work item type you want to use for calculating progress of your key result. You can choose from any work item type in the query or all work items in the shared query. 
1. Select the ADO field you want to use for tracking key result progress.  
1. Select **Next.** 
1. Select **Save.** 

You should now see the Azure DevOps icon next to your key result. Viva Goals will now automatically update the progress once per hour.

**If using the Connect to Work Items method:**

1. Select **work items** method. 
1. Select the ‘work item type’ to connect to – we recommend choosing the “parent” work item type in your Azure DevOps hierarchy that contains the work being done. The integration will automatically include the child work items. For example, connect to a feature that is the parent to the tasks versus connecting to each individual task.  
1. Search for and select the specific work item(s) of the chosen type.
1. Select the work item type you want to use for calculating progress of your key result. You can choose to measure progress by a specific work item type (i.e., the type you directly connect to or any of its children types) or all work items (i.e., connected and children). 
1. Select the ADO field you want to use for tracking key result progress.    
1. Select **Next**. 
1. Select **Save**. 

You should now see the Azure DevOps icon next to your Key Result. Viva Goals will now automatically update this initiative once per hour based on the ADO field for the work item types selected.

## Progress Calculation for ADO fields in Viva Goals: 


|Track Progress By    |Percentage metric   |Number metric   |
|---------|---------|---------|
|Count of Work Items      |Percent of completed work items out of the total work items for the given query or work item type.         |Number of work items for the given query or work item type.         |
|Story Points      |Percent of story points for the completed work items out of the total story points for the work items for given query or work item type.         |Sum of story points for the work items for given query or work item type.         |
|Effort     |Percent of effort for the completed work items out of the total effort for the work items for given query or work item type.         |Sum of effort for the work items for given query or work item type.         |
|Original Estimate      |Percent of total original estimate hours for the completed work items out of the total original estimate hours for all the work items for given query or work item type.         |Sum of original estimate hours for the work items for given query or work item type.         |
|Remaining Work      |N/A         |Total remaining work hours for the work items for given query or work item type.         |
|Completed Work      |Percent of total completed work hours for the completed work items out of the total completed work hours for all work items for the given query or work item type.         |Total completed work hours for the work items for given query or work item type.        |
|Custom Fields      |Percent complete of the associated numeric custom field in ADO for the given query or work item type.         |Total sum of associated numeric custom field in ADO for the given query or work item type.         |
 

## Troubleshooting connection issues

To integrate with Azure DevOps, the Viva Goals Service needs to be able to access the work items in the Azure DevOps Organization and initiative that you configure when creating the connection in Viva Goals. Depending on how your organization manages their Microsoft Entra Conditional Access policies and Azure DevOps permissions, Viva Goals could be unable to access information. 

### Forbidden Errors 

If you encounter forbidden error messages when creating an Azure DevOps connection, it's likely that IP address constraints or other Conditional Access Policies are to blame. In this case you need to verify if the Enable Microsoft Entra ID CAP validation policy is enabled on the Azure DevOps Organization, for more details please reference [Azure DevOps documentation.](/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops&preserve-view=true) 

### Solutions

You have two options, you can either turn off the Enable Microsoft Entra ID CAP validation policy on the Azure DevOps organization. Which would require and Azure DevOps Administrator, or you need to add the Viva Goals Service Outbound IP addresses to the Conditional Access Policies for your tenants Microsoft Entra ID. 

## FAQ (Frequently Asked Questions)

1. **When connecting my Viva Goals initiative tasks with Azure DevOps, why don’t I see all of the work items in my shared query and/or all of the child work items when using the “connect to work item” method?**
    1. Whether connecting your Viva Goals initiative to Azure DevOps, Viva Goals doesn't expose all of the work items.   What Viva Goals shows depends on how you choose to calculate the overall Viva Goals initiative progress during the setup process. If you choose to calculate initiative progress by any work item, Viva Goals will indeed expose all of the shared query work items or all of the child items, if you connected directly to work items. <br> <br> However, we believe choosing “any” work item type is the exception, as this approach would expose an excessive amount of work item detail not necessary within Viva Goals UX.  We assume most users choose to calculate progress by a specific work item type within the shared query or a child of the connected work items.   Viva Goals will use that decision to limit what we expose in the Viva Goals UX.  <br> <br> For example, assume you Azure DevOps work is tracking Features, User Stories and Tasks. Further assume, you choose to track Viva Goals initiative progress based on User Story completion.  Viva Goals will only show the Features and User Stories within the Viva Goals initiative views. Users can quickly “double-click” into Azure DevOps for more details as needed.

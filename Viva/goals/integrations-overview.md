---
title: Integrations overview
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
- highpri
search.appverid:
- MET150
description: "Learn how to enable and manage your connections and even request an integration"
---

# Viva Goals integrations overview

Viva Goals support integration with industry-leading tools and platforms you use every day, so your OKR implementation process is as simple, effective, and seamless as possible. Don't switch away from the tools you love, and don't waste time switching back and forth. Use integrations to automatically update OKRs when your work gets done and foster ongoing feedback on your goals.

## How to enable integrations 

To activate a specific integration, go to **Admin** > **Integrations** and select **Enable**.

> [!IMPORTANT]
> Integrations must first be enabled by your global administrators before they can be managed by org administrators. Contact your tenant administrator to enable supported integrations you do not see in the integrations dashboard.  
> 
> Instructions for global admins to enable integrations are located here: **[Enable Integrations in Viva Goals](vg-integrations-administration-overview.md)**.

## How to view integrations 

At the integrations page, there are two views you can use to see the available integrations: 

- The list view is a clean, compact view of all integrations with a call-to-action button to enable or manage the integration. 

- The detail-driven grid view provides links to the corresponding help article and to contact support. 

You'll see the grid view by default. To toggle between the two views, select the icons in the upper-right corner of the page.

## How to create connections

To set up a connection, select **Enable** on the integration you want to set up a connection for, and then follow the setup steps. 

*Remember that only admins can edit connections.* 

To make connections public (usable by everyone in the organization) or private, toggle the **Share connection** checkbox. Users will be able to see their private connections, followed by their public connections (if any).

## Data update frequency for integrations 

Viva Goals checks for new data about once per hour. You can also trigger a sync manually.

   >[!Note]
   >When you trigger a sync manually, make sure the OKR or project is already integrated with one of the integration tools.

1. Select the integration icon next to the progress bar of an OKR or project.

2. Select the refresh symbol.


## How to edit an integration

There are three ways to edit an integration:

- Against a specific key result, go to **More Actions icon** > **Edit**. You'll find an option to **Edit** the integration on the **Connect data source to auto-update progress** dropdown. 

- For a simpler way to edit the integration, select the **Integrations icon** next to the progress bar and then select **Edit integration** from the pop-over window. 

- From the quick-view window, select the **Integrations icon**  and then select **Edit integration**.

## Integrations supported in Viva Goals

The following is a list of all the integrations currently available in Viva Goals:

:::row:::
   :::column span="4":::
      **Supported Integrations**
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
      [Azure Data Explorer ](azure-data-explorer-integration.md)
    :::column-end:::
    :::column:::
      [Azure DevOps (ADO)](azure-devops-integration.md)
    :::column-end:::  
    :::column:::    
      [Amazon RedShift](amazon-redshift-integration.md)
    :::column-end:::
    :::column:::
      [Asana](asana-integration.md)         
    :::column-end:::
:::row-end:::   

:::row:::
    :::column:::
      [BigQuery](bigquery-integration.md)         
    :::column-end:::  
    :::column:::    
      [Box](box-integration.md)      
    :::column-end:::    
    :::column:::
      [Domo](domo-integration.md)   
    :::column-end:::
    :::column:::
      [Dynamics 365](dynamics-365-integration.md)
    :::column-end:::  
:::row-end:::   

:::row:::   
    :::column:::    
      [Excel Online](excel-online-integration.md)
    :::column-end:::    
   :::column:::
      [Favro](favro-generating-an-api-token.md)  
    :::column-end:::
    :::column:::
      [GitHub](github-integration.md)
    :::column-end:::  
    :::column:::    
      [GitLab](gitlab-integration.md)
    :::column-end:::
:::row-end:::

:::row:::   
    :::column:::
      [Google Sheets](gsheets-integration.md)  
    :::column-end:::
    :::column:::
      [Hubspot](hubspot-integration.md)
    :::column-end:::  
    :::column:::    
      [Jira](jira-integration.md)
    :::column-end:::    
    :::column:::
      [Looker](looker-integration.md)  
    :::column-end:::
:::row-end:::
 
:::row:::   
    :::column:::
      [Microsoft Planner](microsoft-planner-integration.md)
    :::column-end:::  
    :::column:::    
      [Mode](mode-integration.md)
    :::column-end:::  
    :::column:::
      [monday.com](monday.com-integration.md)
    :::column-end:::
    :::column:::
      [MS SQL Server](ms-sql-server-integration.md)
    :::column-end:::  
:::row-end:::
 
:::row:::   
    :::column:::    
      [MySQL](mysql-integration.md)
    :::column-end:::    
    :::column:::
      [Planview Projectplace](planview-projectplace-integration.md)  
    :::column-end:::
    :::column:::
      [PostgreSQL](postgresql-integration.md)
    :::column-end:::  
    :::column:::    
      [Power BI](power-bi-integration.md)
    :::column-end:::        
:::row-end:::
 
:::row:::   
    :::column:::
      [Salesforce](salesforce-integration.md)
    :::column-end:::
    :::column:::
      [Slack](slack-collaborate-with-viva-goals.md)
    :::column-end:::  
    :::column:::    
      [Smartsheet](smartsheet-integration.md) 
    :::column-end:::    
    :::column:::
      [Snowflake](snowflake-integration.md)
    :::column-end:::
:::row-end:::

:::row:::   
    :::column:::
      [Tableau](tableau-integration.md)
    :::column-end:::  
    :::column:::    
      [Trello](trello-integration.md)
    :::column-end:::    
    :::column:::
      [Zendesk](zendesk-integration.md) 
    :::column-end:::
    :::column:::
      
    :::column-end:::
:::row-end:::
 
 
## How to disable an integration

To disable an integration, select **Manage**, and then select **Disable integration** from the **Change** dropdown. 

> [!NOTE]
> OKRs that currently use the disabled connection will no longer be able to sync.

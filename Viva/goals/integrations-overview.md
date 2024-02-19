---
ms.date: 02/18/2024
title: Viva Goals integrations overview
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
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
- vg-integration
search.appverid:
- MET150
description: "Learn how to enable, view, and manage integrations in Viva Goals, as well as how to create and manage connections for those integrations."
---

# Viva Goals integrations overview

Viva Goals can integrate with the industry-leading tools and platforms you use every day, making your OKR implementation process as straightforward as possible. Using integrations allows your goals to automatically update as you do your work and fosters ongoing feedback on those goals.

## Enable an integration

To activate a specific integration:

1. Go to **Admin** > **Integrations**. You will see a list of all the integrations you have access to.

1. Find the integration you want to add.

1. If you haven't enabled the integration already, it will show an icon that says either **Add to \<INTEGRATION>** (for example, **Add to Teams** or **Add to Slack**) or **Get started**. Select this icon. <!--Editor's Note: Learn whether there is a difference between Add to and Get started.-->

1. Follow the setup process.

> [!IMPORTANT]
> An integration must be enabled by a Microsoft Global Administrator before a Viva Goals Org Admin can use the steps below to enable them for their specific org. Learn how to contact your Global Administrator to enable new integrations by following the steps [here](vg-integrations-administration-overview.md).

## View available integrations

The Integrations page offers two ways to view your available integrations:

- The **List** view is a clean, compact view of all available integrations and features a call-to-action button that lets you enable or manage the integration.

- The detail-driven **Grid** view is similar to the list view but provides a link to each integration's help article.

You'll see the grid view by default <!--Editor's Note: Is this true?-->. To toggle between the two views, use the icons in the upper-right corner of the Integrations page.

## Create a connection

To create a connection for an existing integration:

1. Go to **Admin** > **Integrations**.

1. Select **Manage** next to the relevant integration.

1. Select **New Connection** and follow the setup process.

Only admins can edit connections.

## Make a connection public or private

To make a connection public (that is, usable by everyone in the organization) or private:

1. Go to **Admin** > **Integrations**.

1. Select **Manage** next to the relevant integration.

1. Select **Edit** next to the relevant connection.

1. Toggle the **Share connection with all users** checkbox. If the checkbox is full, the connection is public. Otherwise, the connection is private.

 Users will be able to see their private connections, followed by their public connections (if any).

## Have Viva Goals check an integration for updated data

Viva Goals checks integrations for new data about once per hour. You can also trigger a sync manually.

> [!NOTE]
> Before you trigger a sync manually, make sure the OKR or initiative is already integrated with one of the integration tools.

To trigger a sync manually:

1. Go to the goal whose data you want to sync.

1. Select the integration's icon in the **Last updated** column, which is to the right of the progress bar.

1. Select **Sync**.

## Edit an integration

There are three ways to edit an integration:

- On a specific goal, select **More options** (the three dots) > **Edit**. Under the **Progress and Status** dropdown, open the **Connected data source** dropdown and choose **Edit integration**.

- For a simpler way to edit the integration, select the integration's icon in the goal's **Last updated** column, which is to the right of the progress bar. From there, select **Details** > **Edit Integration**.

- Select a goal's name in the **Title** column. In the quick-view window on the right, select the integration's icon. Open the "Progress updated" dropdown, then select **Edit integration**.

## Disable an integration

To disable an active integration:

1. Go to **Admin** > **Integrations**.

1. Select **Manage** next to the relevant integration.

1. Select **Disable Integration** from the **Change** dropdown.

> [!NOTE]
> OKRs currently using the disabled integration will not be able to sync going forward.

## Integrations supported in Viva Goals

The following is a list of all the integrations currently available in Viva Goals:

:::row:::
   :::column span="4":::
      **Supported Integrations**
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
      [Azure Data Explorer](azure-data-explorer-integration.md)
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

---
ms.date: 11/14/2022
title: Enable Integrations in Viva Goals
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
search.appverid:
- MET150
description: "Learn about integration administration with Viva Goals."
---

# Enable integrations in Viva Goals 

Viva Goals supports integrations with Microsoft and third-party apps and platforms so that the OKR implementation process is as simple, effective, and seamless as possible.

As a Global admin, you can control which integrations are available for all Viva Goals organizations in the tenant.  

- Read more about the types of integrations in Viva Goals: [Integrations overview](#integrations-overview)
- Read more about Roles and Permissions in Viva Goals: [Roles and permissions in Viva Goals](roles-permissions-in-viva-goals.md)

There are three options for global admins to control which integrations are available in your tenant.  

- All available 
- None available 
- Select integrations are available 

**All available**
When you select this option, all integrations will be available to all Viva Goals organizations in your tenant. Integrations that are available in the tenant can be further managed by org owners and org administrators. 

**None available**
When you select this option, no integrations will be available in your tenant. 

> [!IMPORTANT]
> Existing connections will not continue to work when this option is selected.

**Select integrations are available**
Selecting this option enables global admins to select which integrations are available in the tenant. By default, O365 core service integrations, such as Excel and Planner are available.

To modify which integrations are available in your organization, select the enable status for each integration you want to manage.  

> [!IMPORTANT]
>  If you deselect an enabled integration, existing connections supported by that integrations will not continue to work.

## How to manage integrations

Only Global admins have permission to manage which integrations are available for the tenant. 

1. Log in to your Viva Goals account. 
1. Select the organization drop down from the navigation panel on the left.
    :::image type="content" source="../media/goals/admin-controls/navigation-pane.png" alt-text="Screenshot showing the navigation side bar and how to select the organization drop down."::: 
1. Select Create or Join organization 
    :::image type="content" source="../media/goals/admin-controls/select-create-join-org.png" alt-text="Screenshot showing how to select Create or join organization from the dropdown.":::  
1. From the Create or Join organizations page, select Settings in the top right corner 
    :::image type="content" source="../media/goals/admin-controls/select-setting.png" alt-text="Screenshot showing where to select the settings option from the organization page.":::
1. Select the integrations settings for your tenant and select save. If you choose the option for Selected integrations are available, select the integrations you want to manage and select save.  
    :::image type="content" source="../media/goals/admin-controls/integrations-selections.png" alt-text="Screenshot showing the list of integration available for your tenant.":::

> [!NOTE]
> Selecting None available or deselecting integrations that were previously available will disable any existing connections in your tenant.

## Integrations Overview

Viva Goals supports two types of integrations, which are discussed in further detail below: data integrations and collaboration integrations. Additionally, integrations can be grouped into three different categories: 

1. In-Boundary Microsoft 365 Integrations: In-boundary Microsoft 365 integrations, such as Microsoft Teams, process all data within the Microsoft 365 service boundary.  

1. Cross-Boundary Integrations: Cross-boundary integrations, such as Azure Data Explorer, process data between different Microsoft service boundaries utilizing Microsoft APIs.   

1. Third-Party Integrations: Third-party integrations utilize third party APIs to process data. Third-party APIs are not controlled or owned by Microsoft and are not governed by the Microsoft Product Terms, your organization’s volume licensing agreement, or any other Microsoft terms or agreements. Your organization’s use of third-party integrations is subject to that third-party’s terms and privacy statement. Before enabling, or allowing users within your organization to enable, an integration, you should review the third party’s terms and relevant documentation. 

The table below shows which type of integrations are supported, their category, and contains links to applicable third-party terms.

|Integration  |Category  |Type  |Terms of Use |
|---------|---------|---------|---------|
|Amazon Redshift|Third-party|Data|https://aws.amazon.com/legal/?nc1=f_cc|
|Asana|Third-party|Data|https://asana.com/terms|
|Azure DevOps|Cross-boundary Microsoft|Data |https://www.microsoft.com/licensing/terms|
|Azure Data Explorer|Cross-boundary Microsoft|Data|https://www.microsoft.com/licensing/terms|
|BigQuery|Third-party |Data |https://cloud.google.com/product-terms/  |
|Box      |Third-party |Data |https://www.box.com/legal/  |
|Domo       |Third-party |Data |https://www.domo.com/company/service-terms |
|Dynamics      |Cross-boundary Microsoft |Data |https://www.microsoft.com/licensing/terms |
|Excel Online       |In-boundary Microsoft 365 |Data |https://www.microsoft.com/licensing/terms |
|Favro      |Third-party |Data |https://help.favro.com/en/collections/362206-pricing-privacy-and-terms |
|GitHub      |Third-party |Data |https://docs.github.com/en/site-policy |
|GitLab      |Third-party |Data |https://about.gitlab.com/terms/ |
|Google Sheets       |Third-party |Data |https://cloud.google.com/product-terms/ |
|HubSpot      |Third-party |Data |https://legal.hubspot.com/terms-of-service |
|Jira Cloud, Jira Server and Data Center       |Third-party |Data |https://www.atlassian.com/legal/cloud-terms-of-service |
|Looker      |Third-party |Data |https://cloud.google.com/product-terms/ |
|Mode      |Third-party |Data |https://mode.com/tos/ |
|Monday.com      |Third-party |Data |https://monday.com/l/ |
|MS SQL     |Cross-boundary Microsoft |Data |https://www.microsoft.com/licensing/terms |
|MySQL      |Third-party|Data |https://www.mysql.com/about/legal/ |
|Planner      |In-boundary Microsoft 365 |Data |https://www.microsoft.com/licensing/terms |
|PostgreSQL      |Third-party |Data |https://www.postgresql.org/about/policies/ |
|Power BI      |Cross-boundary Microsoft |Data |https://www.microsoft.com/licensing/terms |
|Project for the Web |Cross-boundary Microsoft |Data | https://www.microsoft.com/licensing/terms|
|ProjectPlace      |Third-party |Data |https://www.planview.com/legal/legal-terms/ |
|Salesforce      |Third-party |Data |https://www.salesforce.com/company/legal/ |
|Smartsheet      |Third-party |Data |https://www.smartsheet.com/legal |
|Slack      |Third-party |Collaboration|https://slack.com/legal |
|Snowflake      |Third-party |Data |https://www.snowflake.com/legal |
|Tableau      |Third-party |Data |https://www.tableau.com/legal |
|Teams|In-boundary Microsoft 365 |Collaboration|https://www.microsoft.com/licensing/terms |
|Trello|Third-party|Data  |https://www.atlassian.com/legal/cloud-terms-of-service |
|Zendesk|Third-party|Data  |https://www.zendesk.com/company/agreements-and-terms  |
|Zapier|Third-party|Data  |https://zapier.com/legal |


## How Data Integrations Work  

Data integrations in Viva Goals enable you to create connections with data sources that will automatically update key results and initiatives, enabling you to have a single source of truth for progress. For example, if you connect an initiative to Azure Dev Ops, Viva Goals will be automatically updated according to progress in Azure Dev Ops. 

When you connect to a data source in Viva Goals, your authentication tokens are used to establish a secure connection between Viva Goals and the selected application. Once every hour, Viva Goals utilizes that connection to retrieve updates from the connected data source and reflect those updates in Viva Goals. 

> [!NOTE]
> When you connect to a data source via an integration, data from that integration will flow into Viva Goals from outside of your tenant. Viva Goals utilizes public APIs to retrieve data from third-party integrations. Viva Goals does not share data from your tenant with third parties to support data integrations by default.  

## How Collaboration Integrations Work  

Collaboration integrations enable users to complete their work in Viva Goals from collaboration platforms like Microsoft Teams. This enables users to take quick actions for their goals in the flow of work in these tools. 

Control over whether Viva Goals is allowed to be installed in the collaboration platform is exercised at the tenant level via administrative tools provided by the platform. For example, the Viva Goals app can be blocked at the tenant level in the Teams Admin Center. 

If enabled by the tenant administrator and organizational administrator, users can install Viva Goals as an application from app stores in these collaboration applications, such as the Microsoft Teams store. Once installed, in addition to viewing Viva Goals within the collaboration application, Viva Goals uses the chat, notification and meeting capabilities of the collaboration platform to have conversations about goals.  

For example, in a Teams chat or channel, a user can search for a goal and ask a question about it. Other users can then respond and react, and Viva Goals can synchronize this comment thread back to the OKR’s activity feed in Viva Goals. This means that data from Viva Goals can be shared to Teams and other collaboration integrations. 

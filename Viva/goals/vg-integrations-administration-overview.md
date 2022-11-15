---
title: Viva Goals Integrations Administration Overview
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
description: "Learn about integration administration with Viva Goals."
---

# Viva Goals Integrations Administration Overview 

Viva Goals supports integrations with Microsoft and third-party apps and platforms so that the OKR implementation process is as simple, effective, and seamless as possible.   

**Organization owners and organization administrators in Viva Goals can enable and configure integrations for their organization. As a Global Admin, you can control who has permission to create and manage organizations in Viva Goals and thereby control who can enable Viva Goals integrations.** 

- Read more about organization creation permissions: [Restrict organization creation permissions | Microsoft Learn ](restrict-organization-creation-permissions.md)
- Read more about Roles and Permissions in Viva Goals: [Roles and permissions in Viva Goals | Microsoft Learn](roles-permissions-in-viva-goals.md) 

Viva Goals supports two types of integrations, which are discussed in further detail below: data integrations and collaboration integrations. Additionally, integrations can be grouped into three different categories: 

1. In-Boundary M365 Integrations: In-boundary M365 integrations, such as Microsoft Teams, process all data within the M365 service boundary.  

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
|Excel Online       |In-boundary M365 |Data |https://www.microsoft.com/licensing/terms |
|Favro      |Third-party |Data |https://help.favro.com/en/collections/362206-pricing-privacy-and-terms |
|Github      |Third-party |Data |https://docs.github.com/en/site-policy |
|GitLab      |Third-party |Data |https://about.gitlab.com/terms/ |
|Google Sheets       |Third-party |Data |https://cloud.google.com/product-terms/ |
|HubSpot      |Third-party |Data |https://legal.hubspot.com/terms-of-service |
|Jira Cloud       |Third-party |Data |https://www.atlassian.com/legal/cloud-terms-of-service |
|Looker      |Third-party |Data |https://cloud.google.com/product-terms/ |
|Mode      |Third-party |Data |https://mode.com/tos/ |
|Monday.com      |Third-party |Data |https://monday.com/l/ |
|MS SQL     |Cross-boundary Microsoft |Data |https://www.microsoft.com/licensing/terms |
|MySQL      |Third-party|Data |https://www.mysql.com/about/legal/ |
|Planner      |In-boundary M365 |Data |https://www.microsoft.com/licensing/terms |
|PostgresSQL      |Third-party |Data |https://www.postgresql.org/about/policies/ |
|PowerBI      |Cross-boundary Microsoft |Data |https://www.microsoft.com/licensing/terms |
|ProjectPlace      |Third-party |Data |https://www.planview.com/legal/legal-terms/ |
|Salesforce      |Third-party |Data |https://www.salesforce.com/company/legal/ |
|Smartsheet      |Third-party |Data |https://www.smartsheet.com/legal |
|Slack      |Third-party |Collaboration|https://slack.com/legal |
|Snowflake      |Third-party |Data |https://www.snowflake.com/legal |
|Tableau      |Third-party |Data |https://www.tableau.com/legal |
|Teams|In-boundary M365 |Collaboration|https://www.microsoft.com/licensing/terms |
|Trello|Third-party|Data  |https://www.atlassian.com/legal/cloud-terms-of-service |
|Zendesk|Third-party|Data  |https://www.zendesk.com/company/agreements-and-terms  |
|Zapier|Third-party|Data  |https://zapier.com/legal |


## How Data Integrations Work  

Data integrations in Viva Goals enable you to create connections with data sources that will automatically update key results and projects, enabling you to have a single source of truth for progress. For example, if you connect a Project to Azure Dev Ops, Viva Goals will be automatically updated according to progress in Azure Dev Ops. 

When you connect to a data source in Viva Goals, your authentication tokens are used to establish a secure connection between Viva Goals and the selected application. Once every hour, Viva Goals utilizes that connection to retrieve updates from the connected data source and reflect those updates in Viva Goals. 

> [!NOTE]
> When you connect to a data source via an integration, data from that integration will flow into Viva Goals from outside of your tenant. Viva Goals utilizes public APIs to retrieve data from third-party integrations. Viva Goals does not share data from your tenant with third parties to support data integrations by default.  

## How Collaboration Integrations Work  

Collaboration integrations enable users to complete their work in Viva Goals from collaboration platforms like Microsoft Teams. This enables users to take quick actions for their goals in the flow of work in these tools. 

Control over whether Viva Goals is allowed to be installed in the collaboration platform is exercised at the tenant level via administrative tools provided by the platform. For example, the Viva Goals app can be blocked at the tenant level in the Teams Admin Center. 

If enabled by the tenant administrator and organizational administrator, users can install Viva Goals as an application from app stores in these collaboration applications, such as the Microsoft Teams store. Once installed, in addition to viewing Viva Goals within the collaboration application, Viva Goals leverages the chat, notification and meeting capabilities of the collaboration platform to have conversations about goals.  

For example, in a Teams chat or channel, a user can search for a goal and ask a question about it. Other users can then respond and react, and Viva Goals can synchronize this comment thread back to the OKR’s activity feed in Viva Goals. This means that data from Viva Goals can be shared to Teams and other collaboration integrations. 
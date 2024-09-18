---
ms.date: 04/29/2024
title: Enable integrations as a Viva goals admin in Viva Goals
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
- highpri
- vg-integration
search.appverid:
- MET150
description: "Learn about integration administration with Viva Goals."
---

# Enable integrations as a Viva goals admin in Viva Goals

Viva Goals supports integrations with Microsoft and third-party apps and platforms so that the OKR implementation process is as simple, effective, and seamless as possible.

As a Viva goals admin, you can control which integrations are available for all Viva Goals organizations in your tenant.

Information about the types of integrations in Viva Goals can be found in [Integrations overview](#integrations-overview), while information about roles and permissions in Viva Goals can be found in [Roles and permissions in Viva Goals](roles-permissions-in-viva-goals.md).

## Manage integrations

Viva goals admins have permission to manage which integrations are available for their tenants.

1. Log in to your Viva Goals account.

1. Select the **Viva Goals Admin Center** icon in the top right corner to visit the admin portal.

1. Once you're in the admin portal, select the **Integrations** tab on the left side of the screen.

1. Configure the integrations settings for your tenant and select **Save**. If you choose the **Selected integrations are available** option, toggle the **Status** slider for the integrations you want to enable (or disable) and then select **Save**.

> [!NOTE]
> Selecting **All integrations disabled** or disabling integrations that were previously enabled will disable any existing connections associated with the integration in your tenant.

## Choosing which integrations are available for your tenant

Viva Goals admins have three options to choose from when deciding which integrations should be available to organizations in their tenants:

- All integrations available
- All integrations disabled
- Selected integrations are available

### All integrations available

If you select this option, all integrations will be available to all Viva Goals organizations in your tenant. Org owners and org administrators can exercise further management over the integrations in their particular organizations.

### All integrations disabled

If you select this option, no integrations will be available in your tenant.

> [!IMPORTANT]
> Existing connections will stop functioning if this option is selected.

### Selected integrations are available

Selecting this option allows Viva goals admins to choose specific integrations to be available in their tenants. O365 core service integrations, such as Excel and Planner, are available by default.

To modify which integrations are available in your organization, toggle the **Status** slider for each integration you want to enable (or disable).

> [!IMPORTANT]
> If you disable a previously enabled integration, existing connections supported by that integration will stop working.

## Integrations overview

Viva Goals supports two types of integrations: [data integrations](#how-data-integrations-work) and [collaboration integrations](#how-collaboration-integrations-work). Integrations can be further grouped into three different categories:

- **In-boundary Microsoft 365 integrations:** In-boundary Microsoft 365 integrations, such as Microsoft Teams, process all their data within their own Microsoft 365 service boundaries.  

- **Cross-boundary integrations:** Cross-boundary integrations, such as Azure Data Explorer, process data between different Microsoft service boundaries by utilizing Microsoft APIs.

- **Third-party integrations:** Third-party integrations utilize third-party APIs to process data. Third-party APIs are not controlled or owned by Microsoft and are not governed by the Microsoft Product Terms, your organization's volume licensing agreement, or any other Microsoft terms or agreements. Your organization's use of third-party integrations is subject to that third party's terms and privacy statement. Before enabling (or allowing users within your organization to enable) a third-party integration, you should review the third party's terms and relevant documentation.

The table below features a list of supported integrations, as well as their categories, types, and links to any applicable terms.

|Integration  |Category  |Type  |Terms of use |
|---------|---------|---------|---------|
|Amazon Redshift|Third-party|Data| https://aws.amazon.com/legal/?nc1=f_cc|
|Asana|Third-party|Data| https://asana.com/terms|
|Azure DevOps|Cross-boundary Microsoft|Data | https://www.microsoft.com/licensing/terms |
|Azure Data Explorer|Cross-boundary Microsoft|Data| https://www.microsoft.com/licensing/terms |
|BigQuery|Third-party |Data | https://cloud.google.com/product-terms/  |
|Box      |Third-party |Data | https://www.box.com/legal/  |
|Domo       |Third-party |Data | https://www.domo.com/company/service-terms |
|Dynamics      |Cross-boundary Microsoft |Data | https://www.microsoft.com/licensing/terms |
|Excel Online       |In-boundary Microsoft 365 |Data | https://www.microsoft.com/licensing/terms |
|Favro      |Third-party |Data | https://help.favro.com/en/collections/362206-pricing-privacy-and-terms |
|GitHub      |Third-party |Data | https://docs.github.com/en/site-policy |
|GitLab      |Third-party |Data | https://about.gitlab.com/terms/ |
|Google Sheets       |Third-party |Data | https://cloud.google.com/product-terms/ |
|HubSpot      |Third-party |Data | https://legal.hubspot.com/terms-of-service |
|Jira Cloud, Jira Server and Data Center       |Third-party |Data | https://www.atlassian.com/legal/cloud-terms-of-service |
|Looker      |Third-party |Data | https://cloud.google.com/product-terms/ |
|Mode      |Third-party |Data | https://mode.com/tos/ |
|Monday.com      |Third-party |Data | https://monday.com/l/ |
|MS SQL     |Cross-boundary Microsoft |Data | https://www.microsoft.com/licensing/terms |
|MySQL      |Third-party|Data | https://www.mysql.com/about/legal/ |
|Planner      |In-boundary Microsoft 365 |Data | https://www.microsoft.com/licensing/terms |
|PostgreSQL      |Third-party |Data | https://www.postgresql.org/about/policies/ |
|Power BI      |Cross-boundary Microsoft |Data | https://www.microsoft.com/licensing/terms |
|Project for the Web |Cross-boundary Microsoft |Data | https://www.microsoft.com/licensing/terms |
|ProjectPlace      |Third-party |Data | https://www.planview.com/legal/legal-terms/ |
|Salesforce      |Third-party |Data | https://www.salesforce.com/company/legal/ |
|Smartsheet      |Third-party |Data | https://www.smartsheet.com/legal |
|Slack      |Third-party |Collaboration| https://slack.com/legal |
|Snowflake      |Third-party |Data | https://www.snowflake.com/legal |
|Tableau      |Third-party |Data | https://www.tableau.com/legal |
|Teams|In-boundary Microsoft 365 | Collaboration|https://www.microsoft.com/licensing/terms |
|Trello|Third-party|Data  | https://www.atlassian.com/legal/cloud-terms-of-service |
|Zendesk|Third-party|Data  | https://www.zendesk.com/company/agreements-and-terms  |

## How data integrations work

Data integrations in Viva Goals enable you to create connections with data sources that will automatically update key results and initiatives, enabling you to have a single source of truth for progress. For example, if you connect an initiative to Azure DevOps, Viva Goals will automatically update that initiative when relevant progress is made in Azure DevOps.

When you connect to a data source in Viva Goals, your authentication tokens are used to establish a secure connection between Viva Goals and the selected application. Once every hour, Viva Goals utilizes that connection to retrieve updates from the connected data source and reflect those updates in Viva Goals.

> [!NOTE]
> When you connect to a data source via an integration, data from that integration will flow into Viva Goals from outside of your tenant. Viva Goals utilizes public APIs to retrieve data from third-party integrations. Viva Goals does not share data from your tenant with third parties to support data integrations by default.

## How collaboration integrations work  

Collaboration integrations enable users to complete their work in Viva Goals from collaboration platforms like Microsoft Teams. This enables users to take quick actions for their goals in the flow of work in these tools.

Control over whether Viva Goals is allowed to be installed in the collaboration platform is exercised at the tenant level via administrative tools provided by the platform. For example, the Viva Goals app can be blocked at the tenant level in the Teams Admin Center.

If enabled by the tenant administrator and organizational administrator, users can install Viva Goals as an app within these collaboration applications from an appropriate app store (like the Microsoft Teams store). Once installed, in addition to viewing Viva Goals within the collaboration application, users can filter the collaboration platform's chat, notification, and meeting capabilities back to Viva Goals.

For example, in a Teams chat or channel, a user can search for a goal and ask a question about it. Other users can then respond and react, and Viva Goals can synchronize this comment thread back to the OKR's activity feed in Viva Goals. This means that data from Viva Goals can be shared to Teams and other collaboration integrations.

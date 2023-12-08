---
ms.date: 09/22/2023
title: Viva Connections analytics
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - intro-overview
  - highpri
  - Tier1
search.appverid:
- SPO160
- MET150f
ms.custom: intro-overview
description: "View usage data for Viva Connections to learn more about usage trends."
---

# View usage data for Viva Connections

Understand how and when users engage with components of the Viva Connections experience by using Viva Connections analytics. Review the number of people who have viewed and engaged with your organization's Viva Connections experiences, the content types users engage with, and the platforms used to access Viva Connections.

> [!NOTE]
>
> - Site member permissions (or higher) to your organization’s SharePoint [home site](/sharepoint/home-site) or Viva Connections app are required to view usage analytics for Viva Connections.
> - Currently, up to 30 days of usage data (if available) can be viewed in the analytics report or downloaded in an Excel (.xlxs) format.
> - Usage reports are only supported for Worldwide Production Environments and for some Special Cloud deployments of Microsoft 365. Refer to the [usage report](#whats-in-the-usage-report) section for details.
> - For tenants that are setup for more than one region, the option to access analytics will have to be disabled for each region using the PowerShell command.
> - Usage analytics data is aggregated and cannot be tracked to an individual user.
> - The analytics feature and centralized Viva Connections administration in the Microsoft 365 Admin center are unavailable in GCC, GCC High, and DoD environments. Please refer to the [list of service availability](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#service-availability-for-each-plan) for more information.

## How to access the report

People with site member (or higher) permissions to your organization’s [SharePoint home site](/sharepoint/home-site) or Viva Connections app in Teams can view usage data.

### To view usage data for Viva Connections from a SharePoint home site

1. Navigate to your organization’s SharePoint home site.
2. Select the **Settings** :::image type="icon" source="../media/connections/viva-connections-analytics/sharepoint-setting-icon.png"::: icon.
3. Then, select **Manage Viva Connections**.
4. Next, go to the **Analytics** section and select **View report**.

    :::image type="content" source="../media/connections/viva-connections-analytics/access-analytics-from-sharepoint.png" alt-text="Screenshot showing the analytics section with view report highlighted.":::

### To view usage data for Viva Connections from Teams

1. Navigate to your organization’s Viva Connections app in Teams.
2. Select the **ellipsis** in the top-right corner.
3. Then, select **View Analytics**

    :::image type="content" source="../media/connections/viva-connections-analytics/access-analytics-from-connections.png" alt-text="Screenshot showing options with view analytics highlighted.":::

## What’s in the usage report

The Analytics page contains charts and graphs providing information on overall traffic, usage, and engagement.

### Overall traffic

This section provides usage data for unique users, engaged users, total visits, and returning users. It also includes activity for desktop, web, and mobile usage; regardless of the platform.

- **Unique users:** Total number of individual viewers across all Viva Connections apps and devices.
- **Engaged users:** Total number of individual viewers who interact with Viva Connections components.
- **Total visits:** Total number of all visits, aggregated across Viva Connections apps, devices, and components.

    :::image type="content" source="../media/connections/viva-connections-analytics/analytics-usage-report.png" alt-text="Screenshot showing data covering overall traffic." lightbox="../media/connections/viva-connections-analytics/analytics-usage-report.png":::

### Usage details

This section breaks down usage data across apps and devices, and includes activity for the [Dashboard](/viva/connections/use-dashboard-web-part-on-home-site), [Feed](/viva/connections/use-feed-web-part-for-viva-connections), and Resources web parts.

- **Total views by apps and devices**: Includes views for desktop, web, and mobile usage.
- **Engaged users by component**: Includes number of engaged users for the Dashboard, Feed, and Resources web parts.
  - **Dashboard**: Includes usage from the [Dashboard web part](/viva/connections/use-dashboard-web-part-on-home-site)
  - **Feed**: Includes usage from the [Feed web part](/viva/connections/use-feed-web-part-for-viva-connections)
  - **Resources**: Includes usage from the tab in the mobile app and the desktop app (The global navigation bar in SharePoint isn't included).

    :::image type="content" source="../media/connections/viva-connections-analytics/analytics-usage-details.png" alt-text="Screenshot showing data covering usage details." lightbox="../media/connections/viva-connections-analytics/analytics-usage-details.png":::

### Engagement details

- **Engaged users by dashboard card**: Includes usage data for each dashboard card on your dashboard, indicating how often each user engages with a card.

    :::image type="content" source="../media/connections/viva-connections-analytics/analytics-engagement-details.png" alt-text="Screenshot showing data covering engagement details." lightbox="../media/connections/viva-connections-analytics/analytics-engagement-details.png":::

## Filter and download reports

Reports can be filtered on the last seven days or the last 30 days. Select a range of days next to a graph to filter the data.

:::image type="content" source="../media/connections/viva-connections-analytics/analytics-filter.png" alt-text="Screenshot showing data filtered by the last 30 days." lightbox="../media/connections/viva-connections-analytics/analytics-filter.png":::

Select **Download report** at the top of the analytics page to download an Excel spreadsheet that contains all the information on the analytics page across three separate tabs and sheets of data.

:::image type="content" source="../media/connections/viva-connections-analytics/vc-analytics-spreadsheet.png" alt-text="Screenshot showing downloaded analytics report in a spreadsheet." lightbox="../media/connections/viva-connections-analytics/vc-analytics-spreadsheet.png":::

## How to to disable analytics features

Your organization might not want to see analytics data due to local data and compliance regulations or other reasons. The following steps can be followed to disable the Viva Connections analytics feature using PowerShell:

1. [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).

   >[!NOTE]
   >
   > - If you installed a previous version of SharePoint Online Management Shell, go to Add, or Remove programs and uninstall "SharePoint Online Management Shell".
   > - For tenants that are setup for more than one region, the option to access analytics will have to be disabled for each region using the PowerShell command.

2. Connect to SharePoint as a [Global Administrator or SharePoint Administrator](/sharepoint/sharepoint-admin-role) in Microsoft 365. To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).

3. Connect to the tenant's SharePoint service by running the following command:

    Run `Connect-SPOService -Url <sharepoint admin URL> -Credential <credentials>`

4. Enter the password in the password prompt.
5. Run `Get-SPOTenant` to view the tenant admin Settings.
6. Locate the "DisableVivaConnectionsAnalytics" setting.
7. Enable or disable the setting by running the following command:

    Run `Set-SPOTenant -DisableVivaConnectionsAnalytics $True`
8. Run `Get-SPOTenant` to confirm the setting is updated.

## Explanations for common report errors

You may see an error in the Analytics section. Review common errors to learn more about how to resolve them so you can download reports to view usage data for Viva Connections.

### Not enough data to generate a report

This message displays if there isn't enough usage data to generate a report. Finish setting up Viva Connections and try to access the report again. [Learn more about how to set up Viva Connections](/viva/connections/guide-to-setting-up-viva-connections).

:::image type="content" source="../media/connections/viva-connections-analytics/lack-of-data-error.png" alt-text="Screenshot showing error when there isn't enough usage data.":::

### General error

Sometimes due to connectivity issues or other technical problems, the analytics report may not be available. Check your network connection, refresh the page, and try loading the report again.

:::image type="content" source="../media/connections/viva-connections-analytics/general-error.png" alt-text="Screenshot showing a general error when there's a problem generating a report.":::

### Errors within the downloaded report

Within the downloaded Excel report, you may notice that certain sections aren't available due to insufficient usage data. Learn more about how to [amplify your organization’s instance of Viva Connections](/viva/connections/launch-viva-connections) and the available [Microsoft Viva adoption resources](https://adoption.microsoft.com/viva/).

### The report has been disabled

You may get the following message: "Viva Connections usage data has been disabled for your organization by your administrator." This message means you won't be able to access usage reports unless your admin enables the feature for your organization.

:::image type="content" source="../media/connections/viva-connections-analytics/data-disabled-error.png" alt-text="Screenshot showing error received when reports have been disabled.":::

## Learn more

[Overview: Viva Connections](/viva/connections/viva-connections-overview)

[Getting started with Microsoft Viva](/viva/getting-started-with-microsoft-viva)

---
ms.date: 06/12/2024
title: Viva Connections analytics
ms.reviewer: evanatkin
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
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

Understand how and when users engage with components of the Connections experience by using analytics. Review data on overall traffic, usage, and engagement across each of your organization's Connections experiences. Data can be further filtered to view a specified range or downloaded as an analytics report in Excel.

> [!NOTE]
>
> - Member level permissions (or higher) are required to view usage analytics for Connections.
> - Usage analytics data is aggregated and cannot be tracked to an individual user.
> - Users with a basic Microsoft 365 subscription (E license) are limited to creating one experience. Users are required to have a Microsoft Viva suite or Viva Communications and Communities license to create two or more experiences (up to 50). For more information, see [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing).
> - For tenants that are setup for more than one region, the option to access analytics will have to be disabled for each region using PowerShell commands. For more information, see [how to disable analytics features](#how-to-to-disable-analytics-features).
> - The analytics feature is unavailable in GCC, GCC High, and DoD environments. For more information, see the [list of platform features](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#platform-features).

## How to access the report

Users need member level permissions (or higher) in their Connections experience to access and view the analytics data for that experience. For organizations that have more than one Connections experience, you can view the analytics report for each experience by going to that experience and opening the report.

Analytics data for Connections can be accessed from your SharePoint home site or the Connections app in Microsoft Teams.

### Access analytics data from a SharePoint home site

1. Navigate to your organization’s SharePoint home site.
2. Select the **Settings** :::image type="icon" source="../media/connections/viva-connections-analytics/sharepoint-setting-icon.png"::: icon.
3. Select **Manage Viva Connections**.
4. Go to the **Analytics** section and select **View report**.

    :::image type="content" source="../media/connections/viva-connections-analytics/access-analytics-from-sharepoint.png" alt-text="Screenshot showing the analytics section with view report highlighted.":::

### Access analytics data from Microsoft Teams

1. Navigate to your organization’s Connections app in Teams.
2. Select the **ellipsis** in the top-right corner.
3. Select **View Analytics**

    :::image type="content" source="../media/connections/viva-connections-analytics/access-analytics-from-connections.png" alt-text="Screenshot showing options with view analytics highlighted.":::

## What’s in the usage report

The Analytics page contains charts and graphs providing data on overall traffic, usage, and engagement for your accessed Connections experience. Data can be filtered down to the last 7, 30, or 90 days. Overall traffic data can be filtered to the last 12 months.

> [!NOTE]
>
> - A Microsoft Viva suite or Viva Communications and Communities license is required to view data beyond 30 days. For more information, see [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing).
> - Data filtered to the previous 90 days and 12 months will be available in mid-June 2024. Historical data for these new filters will not be available.

### Overall traffic

This section provides usage data on unique users, engaged users, total views, and returning users. Activity for desktop, web, and mobile usage is combined in this section, regardless of the platform.

- **Unique users**: Total number of individual users regardless of how many times they visited across all Connections platforms and devices.
- **Engaged users**: Total number of individual viewers who interact with Connections content types.
- **Total views**: Total number of views across all Connections platforms and devices.
- **Returning users**: Can view by the percentage or number of users who engaged with Connections content since the last month over a 12-month view. Select the dropdown to switch viewing data on returning users by percentage and individual user.

> [!NOTE]
>
> A Microsoft Viva suite or Viva Communications and Communities license is required to view data on returning users. For more information, see [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing).

:::image type="content" source="../media/connections/viva-connections-analytics/analytics-usage-report.png" alt-text="Screenshot showing data covering overall traffic." lightbox="../media/connections/viva-connections-analytics/analytics-usage-report.png":::

### Usage details

This section breaks down usage data across the types of devices and apps used to access the Connections experience, including activity from the [Dashboard, Feed, and Resources](/viva/connections/viva-connections-overview#components-to-viva-connections).

- **Total views by apps and devices**: Includes views for desktop, web, and mobile usage.
- **Engaged users by component**: Includes number of engaged users for the Dashboard, Feed, and Resources web parts.
  - **Dashboard**: Includes usage from the Dashboard.
  - **Feed**: Includes usage from the Feed.
  - **Resources**: Includes usage from the tab in the mobile app and the desktop app (The global navigation bar in SharePoint isn't included).

    :::image type="content" source="../media/connections/viva-connections-analytics/analytics-usage-details.png" alt-text="Screenshot showing data covering usage details." lightbox="../media/connections/viva-connections-analytics/analytics-usage-details.png":::

### Engagement details

- **Engaged users by dashboard card**: Includes usage data for each dashboard card on your dashboard, indicating how often each user engages with a card.

    :::image type="content" source="../media/connections/viva-connections-analytics/analytics-engagement-details.png" alt-text="Screenshot showing data covering engagement details." lightbox="../media/connections/viva-connections-analytics/analytics-engagement-details.png":::

## Filter and download reports

Reports can be filtered on the last 7, 30, or 90 days, or the last 12 months. To filter the data, select a range of days next to a graph.

> [!NOTE]
>
> A Microsoft Viva suite or Viva Communications and Communities license is required to view or download report data beyond 30 days. For more information, see [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing).

:::image type="content" source="../media/connections/viva-connections-analytics/analytics-filter.png" alt-text="Screenshot showing data filtered by the last 30 days." lightbox="../media/connections/viva-connections-analytics/analytics-filter.png":::

Select **Download report** at the top of the analytics page to download an Excel spreadsheet that contains all the information on the analytics page across three separate tabs and sheets of data. The spreadsheet contains all data available that the account has access to (based on license).

:::image type="content" source="../media/connections/viva-connections-analytics/vc-analytics-spreadsheet.png" alt-text="Screenshot showing downloaded analytics report in a spreadsheet." lightbox="../media/connections/viva-connections-analytics/vc-analytics-spreadsheet.png":::

## How to to disable analytics features

Your organization might not want to see analytics data due to local data and compliance regulations or other reasons. Use the following steps to disable the Connections analytics feature using PowerShell. For tenants that are set up for more than one region, the option to access analytics needs to be disabled for each region using the PowerShell command.

1. Make sure any previous versions of SharePoint Online Management Shell are uninstalled on your device (Settings > Apps > Installed apps > uninstall "SharePoint Online Management Shell").

2. [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).

3. Connect to SharePoint as a [SharePoint Administrator](/sharepoint/sharepoint-admin-role) in Microsoft 365. To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).

4. Connect to the tenant's SharePoint service by running the following command:

    Run `Connect-SPOService -Url <sharepoint admin URL> -Credential <credentials>`

5. Enter the password in the password field.

6. Run `Get-SPOTenant` to view the tenant admin Settings.

7. Locate the "DisableVivaConnectionsAnalytics" setting.

8. Enable or disable the setting by running the following command:

    Run `Set-SPOTenant -DisableVivaConnectionsAnalytics $True`

9. Run `Get-SPOTenant` to confirm the setting is updated.

## Explanations for common report errors

You might see an error in the Analytics section. Review common errors to learn more about how to resolve them so you can download reports to view usage data for Connections.

### Not enough data to generate a report

This message displays if there isn't enough usage data to generate a report. Finish setting up  Connections and try to access the report again. For more information, see the [guide to getting set up with Viva Connections](/viva/connections/guide-to-setting-up-viva-connections).

:::image type="content" source="../media/connections/viva-connections-analytics/lack-of-data-error.png" alt-text="Screenshot showing error when there isn't enough usage data.":::

### General error

Sometimes due to connectivity issues or other technical problems, the analytics report might not be available. Check your network connection, refresh the page, and try loading the report again.

:::image type="content" source="../media/connections/viva-connections-analytics/general-error.png" alt-text="Screenshot showing a general error when there's a problem generating a report.":::

### Errors within the downloaded report

Within the downloaded Excel report, you might notice that certain sections aren't available due to insufficient usage data. Learn more about how to [amplify your organization’s instance of Viva Connections](/viva/connections/launch-viva-connections) and the available [Microsoft Viva adoption resources](https://adoption.microsoft.com/viva/).

### The report is disabled

You might get the following message: "Viva Connections usage data has been disabled for your organization by your administrator." This message means you can't access usage reports unless your admin enables the feature for your organization.

:::image type="content" source="../media/connections/viva-connections-analytics/data-disabled-error.png" alt-text="Screenshot showing error received when reports have been disabled.":::

## Learn more

[Overview: Viva Connections](/viva/connections/viva-connections-overview)

[Getting started with Microsoft Viva](/viva/getting-started-with-microsoft-viva)

[Add cards to the dashboard](/viva/connections/create-dashboard)

---
title: "Overview: Viva Connections"
ms.reviewer: 
ROBOTS: NOINDEX, NOFOLLOW
ms.author: hokavian
author: Holland-ODSP
manager: pamgreen
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
search.appverid:
- SPO160
- MET150f
ms.custom: intro-overview
description: "Learn how to use Viva Connections experience by using Viva Connections analytics."
---

# View usage data for Viva Connections

Understand how and when users engage with components of the Viva Connections experience by using Viva Connections analytics. Review the number of people who have viewed and engaged with Viva Connections experiences, the content types users engage with, and the platforms used to access Viva Connections.

People with site owner (or higher) permissions to your organization’s [home site](/sharepoint/home-site) can view usage data. To view usage data for Viva Connections, select the **Settings** gear :::image type="icon" source="../media/vc-analytics-error-setting.png" alt-text="Icon that shows the settings."::: and then click **Manage Viva Connections**.

> [!NOTE]
> - This analytics experience is only available to private preview customers. It is expected that this will become generally available in the first quarter of 2023.
> - Currently, up to 28 days of usage data (if available) can be downloaded in an Excel (.xlxs) format.
> - Site member permissions (or higher) to your organization’s [home site](/sharepoint/home-site) are required to download and view usage analytics for Viva Connections. 
> - Usage reports are only supported for Worldwide Production Environments and for some Special Cloud deployments of Microsoft 365. See below for details.

## How to access the report

People with site owner (or higher) permissions to your organization’s [home site](/sharepoint/home-site) can view usage data.

| Component | Description |
| :------------------- | :------------------- |
| :::image type="content" source="../media/manage-vc-panel.png" alt-text="Screenshot that shows the Manage Viva Connections."::: | 1. Navigate to your organization’s home site.<br><br> 2. Select the **Settings** :::image type="icon" source="../media/vc-analytics-error-setting.png" alt-text="Icon that shows the settings."::: icon.<br><br> 3. Then, select **Manage Viva Connections**.<br><br> 4. Next, go to the **Analytics** section and select **Download report**. |

## What’s in the usage report

The usage report contains three separate tabs and sheets of data. Learn more about the data on each sheet and metric definitions.

:::image type="content" source="../media/vc-analytics-spreadsheet.png" alt-text="Screenshot that shows the analytics spreadsheet.":::

**Sheet 1: Overall traffic**

Learn more about usage data for unique users, engaged users, and the total visits. The data on this sheet includes activity for desktop, web, and mobile usage regardless of the platform.

- **Unique active users:** Total number of individual viewers across all Viva Connections platforms. This includes viewers who open the app and view the experience.
- **Unique engaged users:** Total number of individual viewers who interact with Viva Connections experiences. This includes viewers who engage with a dashboard card, a post in the feed, or a link in resources.
- **Total visits:** Total number of individual visits, aggregated across Viva Connections platforms.

**Sheet 2: Usage by experience**

Learn more about the components users engage with across Viva Connections experience. The data on this sheet includes activity for desktop, web, and mobile usage. It also includes the Viva Connections [Dashboard](/viva/connections/use-dashboard-web-part-on-home-site) and [Feed](/viva/connections/use-feed-web-part-for-viva-connections) web parts.

- **Dashboard:** The Dashboard is your employee’s digital toolset. It brings together the tools your employees need, enabling quick and easy access whether they are in the office or in the field. Data includes usage from the [Dashboard web part](/viva/connections/use-dashboard-web-part-on-home-site).
- **Feed:** The Feed delivers updates to the right people at the right time and is tightly integrated with Yammer, SharePoint news, and Stream to display a personalized feed, based on post-level targeting of the groups that employees belong to. Data includes usage from the [Feed web part](/viva/connections/use-feed-web-part-for-viva-connections).
- **Resources:** The Resources experience enables way finding across platforms. It uses navigation elements from the [SharePoint app bar](/viva/connections/sharepoint-app-bar). Data includes usage from the tab in the mobile app, the desktop app, but not the global navigation bar in SharePoint.
 
**Sheet 3: Usage by platform**

Learn more about the platforms used to access Viva Connections.  

- **Microsoft Teams desktop:** Usage in the Teams app for desktop or web.
- **Microsoft Teams mobile:** Usage in the Teams app for mobile.
- **SharePoint:** Usage with the Dashboard, Feed, and Resources in the SharePoint app for desktop, web, and mobile.

## Explanations for common report errors

You may see an error in the Analytics section. Review common errors to learn more about how to resolve them so you can download reports to view usage data for Viva Connections. 

### Not enough data to generate a report

:::image type="content" source="../media/vc-analytics-error-data.png" alt-text="Screenshot that shows the error data.":::

This message will display if your organization has not finished setting up Viva Connections or if there is not enough usage data to generate a report. Finish setting up Viva Connections and try to download the report again. [Learn more about how to set up Viva Connections](/viva/connections/guide-to-setting-up-viva-connections).

### General error

:::image type="content" source="../media/vc-analytics-error-setup.png" alt-text="Screenshot that shows error setup.":::

Sometimes due to connectivity issues or other technical problems, the analytics report may not be available. Check your network connection, refresh the page, and try downloading the report again.

### Errors within the report

Once the report is downloaded, you may notice that the report, or certain sections of the report, are not available due to insufficient usage data. Learn more about how to [amplify your organization’s instance of Viva Connections](/viva/connections/launch-viva-connections) and the available [Microsoft Viva adoption resources](https://adoption.microsoft.com/en-us/viva/).

### The report has been disabled

You may get the following message: "Viva Connections usage data has been disabled for your organization by your administrator." This means you will not be able to access usage reports unless your admin enables the feature for your organization.

## Learn more

[Overview: Viva Connections | Microsoft Docs](/viva/connections/viva-connections-overview)

[Getting started with Microsoft Viva | Microsoft Docs](/viva/getting-started-with-microsoft-viva)

---
ms.date: 03/27/2024
title: Power BI integration
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
- vg-integration
search.appverid:
- MET150
description: "Learn how to integrate your Viva Goals OKRs and initiatives with Power BI."
---

# Power BI integration

Key results and initiatives that use metrics to track completion in Viva Goals can directly connect to data from reports in Power BI. Viva Goals will sync the data at regular intervals, ensuring your key results and initiative always stay up to date with the latest progress.

> [!NOTE]
> To connect to a Power BI report, you'll need [build permissions](/power-bi/connect-data/service-datasets-build-permissions) on the dataset underlying the report.

## Connect a key result to data from Power BI

1. Add a new key result or edit an existing key result by selecting that key result's **More options** (**...**) > **Edit**.

   :::image type="content" source="../media/goals/powerbi-images/edit-kr.png" alt-text="Screenshot that shows how to edit a key result in Viva Goals." lightbox="../media/goals/powerbi-images/edit-kr.png":::

1. Under **Progress and Status**, there's a section with the text "Connect to a data source for automatic progress updates" followed by a list of integration icons. Select the **Power BI** icon.

   :::image type="content" source="../media/goals/powerbi-images/kr-select-power-bi.png" alt-text="Screenshot that shows how to select Power BI from the automatic check-in dropdown list." lightbox="../media/goals/powerbi-images/kr-select-power-bi.png":::

    > [!NOTE]
    > If Power BI is disabled, your Viva Goals administrator will need to enable it for your organization. See [Enable Power BI integration](#enable-power-bi-integration) below.

1. If you haven't already signed in to Power BI or created a connection, you'll be given the chance to do so. Sign in with your Viva Goals credentials. A screen for the new connection will appear. Name the connection and select **Next**.

   > [!IMPORTANT]
   > Only you have access to this connection; it will not be shared with anyone else.

1. Once logged in to Power BI, choose the report you want to link data from and select **Next**.

   :::image type="content" source="../media/goals/powerbi-images/kr-select-report.png" alt-text="Screenshot that shows how to select a Power BI report from the list." lightbox="../media/goals/powerbi-images/kr-select-report.png":::

1. Within the report, you can select a particular chart. Power BI will show you the current value of the data being linked, as well as the filters being applied. Select **Connect** to link the data.

   :::image type="content" source="../media/goals/powerbi-images/kr-select-metric.png" alt-text="Screenshot that shows how to select a metric from the available options." lightbox="../media/goals/powerbi-images/kr-select-metric.png":::

1. When you're done, select **Save** to finalize your changes.

   :::image type="content" source="../media/goals/powerbi-images/kr-save.png" alt-text="Screenshot that shows the save button." lightbox="../media/goals/powerbi-images/kr-save.png":::

The key result will now regularly synchronize data from Power BI and make check-ins on your behalf.

:::image type="content" source="../media/goals/powerbi-images/kr-connected.png" alt-text="Screenshot that shows a successfully connected KR." lightbox="../media/goals/powerbi-images/kr-connected.png":::

## Connect an initiative to data from Power BI

1. Add a new initiative or edit an existing initiative by selecting that initiative's **More options** (**...**) > **Edit**.

   :::image type="content" source="../media/goals/powerbi-images/project-edit.png" alt-text="Screenshot that shows how to edit an initiative." lightbox="../media/goals/powerbi-images/project-edit.png":::

1. Under **Outcome**, select **Add metric**.

   :::image type="content" source="../media/goals/powerbi-images/project-add-metric.png" alt-text="Screenshot that shows the outcome section in the edit panel and where to locate the add metric button." lightbox="../media/goals/powerbi-images/project-add-metric.png":::

1. Specify a metric.

   :::image type="content" source="../media/goals/powerbi-images/project-enter-metric.png" alt-text="Screenshot that shows how to enter a metric." lightbox="../media/goals/powerbi-images/project-enter-metric.png":::

1. Under **Progress and Status**, there's a section with the text "Connect to a data source for automatic progress updates" followed by a list of integration icons. Select the **Power BI** icon.

   :::image type="content" source="../media/goals/powerbi-images/project-progress-data-source.png" alt-text="Screenshot that shows how to select  automatic data source." lightbox="../media/goals/powerbi-images/project-progress-data-source.png":::

   > [!NOTE]
   > If Power BI is disabled, your Viva Goals administrator will need to enable it for your organization. See [Enable Power BI integration](#enable-power-bi-integration )below.

1. If you haven't already signed in to Power BI or created a connection, you'll be given the chance to do so. Sign in with your Viva Goals credentials. A screen for the new connection will appear. Name the connection and select **Next**.

   > [!IMPORTANT]
   > Only you have access to this connection; it will not be shared with anyone else.

1. Once logged in to Power BI, choose the report you want to link data from and select **Next**.

   :::image type="content" source="../media/goals/powerbi-images/kr-select-report.png" alt-text="Screenshot that shows how to select a report from a list of available options." lightbox="../media/goals/powerbi-images/kr-select-report.png":::

1. Within the report, you can select a particular chart. Power BI will show you the current value of the data being linked, as well as the filters being applied. Select **Connect** to link the data.

   :::image type="content" source="../media/goals/powerbi-images/project-select-metric.png" alt-text="Screenshot that shows how to link the data to a report." lightbox="../media/goals/powerbi-images/project-select-metric.png":::

1. When you're done, select **Save** to finalize your changes.

   :::image type="content" source="../media/goals/powerbi-images/project-save.png" alt-text="Screenshot that shows how to save your update." lightbox="../media/goals/powerbi-images/project-save.png":::

Your initiative will now regularly synchronize data from Power BI and make check-ins on your behalf.

:::image type="content" source="../media/goals/powerbi-images/project-connected.png" alt-text="Screenshot of a successful initiative integration with Power BI." lightbox="../media/goals/powerbi-images/project-connected.png":::

## Enable Power BI integration

Before any org members can make use of Power BI integrations, a Viva Goals admin must enable the Power BI Integration for Viva Goals at the tenant level. Look for the Power BI Integration and enable it by following the instructions in [Manage integrations](vg-integrations-administration-overview.md#manage-integrations).

1. Go the Viva Goals Integrations at **Admin** > **Integrations**.

1. Enable Power BI integration under the **Data Integrations** section.

Your Fabric admin will also need to enable the [Create and use metrics](/fabric/admin/service-admin-portal-goals-settings) tenant setting. It should be enabled by default. You can find this in the Metrics settings section of the tenant settings in the admin portal. [Learn more about Fabric tenant settings](/fabric/admin/about-tenant-settings).

> [!NOTE]
> You can disable the integration at any time from the same section.

---
title: "Power BI Integration"
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
search.appverid:
- MET150

description: "Learn how to integrate your Viva Goals OKRs with Power BI."
---

# Power BI Integration

Key Results and Projects that use metrics to track completion in Viva Goals can directly connect to data from reports in Power BI using our simple point and click interface. Viva Goals will sync the data at regular intervals, ensuring your Key Results and Projects always stay up to date with the latest progress. 

## How to connect your Key Result to data from Power BI 

1. Add a new Key Result or open an existing Key Result for Edit.
   
   :::image type="content" source="../media/goals/powerbi-images/edit-kr.png" alt-text="Screenshot that shows how to edit a key result in Viva Goals." lightbox="../media/goals/powerbi-images/edit-kr.png":::    

2. Under the Progress section, select **Automatically from a data source** and then from the list of Integrations, select **Power BI.** 
   
   :::image type="content" source="../media/goals/powerbi-images/kr-select-power-bi.png" alt-text="Screenshot that shows how to select Power BI from the automatic check-in dropdown list." lightbox="../media/goals/powerbi-images/kr-select-power-bi.png":::

    > [!NOTE]
    > If Power BI is disabled, your Viva Goals administrator will need to enable it for your organization. See **How to enable Power BI Integration** below.

3. The first time, you will be presented with a screen to sign in to Power BI. Sign in with your Viva Goals credentials. A screen will appear to save a new connection. Name the connection and select **Next.** 

   > [!IMPORTANT]
   > Only you will have access to this connection, it will not be shared with anyone else. 

4. Once logged in to Power BI, you can select the report you want to link data from and click **Next.**

   :::image type="content" source="../media/goals/powerbi-images/kr-select-report.png" alt-text="Screenshot that shows how to select a power bi report from the list." lightbox="../media/goals/powerbi-images/kr-select-report.png":::

5. Within the report, you can select a particular chart. Power BI will show you the current value of the data being linked as well as the filters being applied. To link the data, click **Connect.**

   :::image type="content" source="../media/goals/powerbi-images/kr-select-metric.png" alt-text="Screenshot that shows how to select a metric from the available options." lightbox="../media/goals/powerbi-images/kr-select-metric.png":::

6. Once it is connected, select **Save.**

   :::image type="content" source="../media/goals/powerbi-images/kr-save.png" alt-text="Screenshot that shows the save button." lightbox="../media/goals/powerbi-images/kr-save.png":::

Your key result will now regularly synchronize data from Power BI and make check-ins on your behalf. If you have any issues, please check the Troubleshooting section below.

:::image type="content" source="../media/goals/powerbi-images/kr-connected.png" alt-text="Screenshot that shows a successfully connected KR." lightbox="../media/goals/powerbi-images/kr-connected.png":::

## How to connect your KPI Project to data from Power BI

1. Add a new Project or edit an existing Project.

   :::image type="content" source="../media/goals/powerbi-images/project-edit.png" alt-text="Screenshot that shows how to edit a project." lightbox="../media/goals/powerbi-images/project-edit.png":::

2. Under the Outcome section, select **Add metric.**

   :::image type="content" source="../media/goals/powerbi-images/project-add-metric.png" alt-text="Screenshot that shows the outcome section in the edit panel and where to locate the add metric button." lightbox="../media/goals/powerbi-images/project-add-metric.png":::

3. Specify a metric.

   :::image type="content" source="../media/goals/powerbi-images/project-enter-metric.png" alt-text="Screenshot that shows how to enter a metric." lightbox="../media/goals/powerbi-images/project-enter-metric.png":::

4. Expand the Progress section and select **Automatically from a data source.**

   :::image type="content" source="../media/goals/powerbi-images/project-progress-data-source.png" alt-text="Screenshot that shows how to select  automatic data source." lightbox="../media/goals/powerbi-images/project-progress-data-source.png":::

5. From the list of Integrations, select Power BI. 

   > [!NOTE]
   > If Power BI is disabled, your Viva Goals administrator will need to enable it for your organization. See **How to enable Power BI Integration** below.

6. The first time, you will be presented with a screen to sign in to Power BI. Sign in with your Viva Goals credentials. A screen will appear to save a new connection. Name the connection and select **Next.**

   :::image type="content" source="../media/goals/powerbi-images/project-select-powee-bi-data-source.png" alt-text="Screenshot that shows how to select Power BI from the available options." lightbox="../media/goals/powerbi-images/project-select-powee-bi-data-source.png"::: 

   > [!IMPORTANT]
   > Only you will have access to this connection, it will not be shared with anyone else.

7. Once logged in to Power BI, you can select the report you want to link data from and select **Next.**

   :::image type="content" source="../media/goals/powerbi-images/kr-select-report.png" alt-text="Screenshot that shows how to select a report from a list of available options." lightbox="../media/goals/powerbi-images/kr-select-report.png":::

8. Within the report, you can select a particular chart. Power BI will show you the current value of the data being linked as well as the filters being applied. To link the data, click **Connect.**

   :::image type="content" source="../media/goals/powerbi-images/project-select-metric.png" alt-text="Screenshot that shows how to link the data to a report." lightbox="../media/goals/powerbi-images/project-select-metric.png":::

9. Once it is connected, select **Save**.

   :::image type="content" source="../media/goals/powerbi-images/project-save.png" alt-text="Screenshot that shows how to save your update." lightbox="../media/goals/powerbi-images/project-save.png":::

Your project will now regularly synchronize data from Power BI and make check-ins on your behalf. If you have any issues, please check the Troubleshooting section below.

:::image type="content" source="../media/goals/powerbi-images/project-connected.png" alt-text="Screenshot of a successful project integration with Dynamics." lightbox="../media/goals/powerbi-images/project-connected.png":::

## How to enable Power BI integration

Global admins must first enable the Power BI Integration for Viva Goals at the tenant level. Look for the Power BI Integration and enable it by following the instructions in [Enable Integrations in Viva Goals > How to manage integrations](vg-integrations-administration-overview.md).

1. Go the Viva Goals Integrations page: **Admin > Integrations**
1. Enable Power BI integration under the Data Integrations category.
1. You can also disable the integration at any time from the same section.

## FAQ (Frequently Asked Questions)

1. What permissions do I need to connect to a Power BI report?  
    1. You will need [build permissions](/power-bi/connect-data/service-datasets-build-permissions) on the dataset underlying the report.

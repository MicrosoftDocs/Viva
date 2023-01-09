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

# Power BI Integration integration

Key Results and Projects that use metrics to track completion in Viva Goals can directly connect to data from reports in Power BI using our simple point and click interface. Viva Goals will sync the data at regular intervals, ensuring your Key Results and Projects always stay up to date with the latest progress. 

## How to connect your Key Result to data from Power BI 

1. Add a new Key Result or open an existing Key Result for Edit
1. Under the Progress section, select **Automatically from a data source** and then from the list of Integrations, select **Power BI.** 
> [!NOTE]
> If Power BI is disabled, your Viva Goals administrator will need to enable it for your organization. See **How to enable Power BI Integration** below.
3. The first time, you will be presented with a screen to sign in to Power BI. Sign in with your Viva Goals credentials. A screen will appear to save a new connection. Name the connection and select **Next.** 
> [!IMPORTANT]
> Only you will have access to this connection, it will not be shared with anyone else. 
4. Once logged in to Power BI, you can select the report you want to link data from and click **Next.**
5. Within the report, you can select a particular chart. Power BI will show you the current value of the data being linked as well as the filters being applied. To link the data, click **Connect.**
6. Once it is connected, select **Save.**

Your key result will now regularly synchronize data from Power BI and make check-ins on your behalf. If you have any issues, please check the Troubleshooting section below.

## How to connect your KPI Project to data from Power BI

1. Add a new Project or edit an existing Project.
1. Under the Outcome section, select **Add metric.**
1. Specify a metric.
1. Expand the Progress section and select **Automatically from a data source.**
1. From the list of Integrations, select Power BI. 
> [!NOTE]
> If Power BI is disabled, your Viva Goals administrator will need to enable it for your organization. See **How to enable Power BI Integration** below.
6. The first time, you will be presented with a screen to sign in to Power BI. Sign in with your Viva Goals credentials. A screen will appear to save a new connection. Name the connection and select **Next.** 
> [!IMPORTANT]
> Only you will have access to this connection, it will not be shared with anyone else. 
7. Once logged in to Power BI, you can select the report you want to link data from and select **Next.**
1. Within the report, you can select a particular chart. Power BI will show you the current value of the data being linked as well as the filters being applied. To link the data, click **Connect.**
1. Once it is connected, select **Save**.

Your project will now regularly synchronize data from Power BI and make check-ins on your behalf. If you have any issues, please check the Troubleshooting section below. 

## How to enable Power BI integration

Admins follow these steps to enable Power BI integration in Viva Goals: 

1. Go the Viva Goals Integrations page: **Admin > Integrations**
1. Enable Power BI integration under the Data Integrations category.
1. You can also disable the integration at any time from the same section.

## Known Issues

The following are known issues the team is working on: 

1. Min/Max button in the Power BI picker control is not working.  
    1. Workaround: use the scrollbars to scroll to the section of the report with the data. 
1. If the user does not have access to the data in a report and requests it, an error message is shown instead of allowing the user to request access. 
    1. Workaround: Open the report in Power BI and follow the permissions flow to request access. 
1. Edit integration must start with the report, currently starts with the report list. 

## FAQ (Frequently Asked Questions)

1. What permissions do I need to connect to a Power BI report?  
    1. You will need [build permissions](/power-bi/connect-data/service-datasets-build-permissions) on the dataset underlying the report.
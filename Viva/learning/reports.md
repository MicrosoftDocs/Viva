---
title: Reporting in Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 07/24/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
  - essentials-manage
ms.localizationpriority: medium
description: Learn how Viva Learning handles customer-facing reports.
---

# Overview of Reports in Viva Learning

## Introduction

Use the Viva Learning admin tab to access analytics and reporting experience for Viva Learning. 
This feature enables organizations to get insights into how Viva Learning is used by their employees.

 We're actively working on adding more metrics in the report section to provide richer insights in future releases.

> [!NOTE]
> The reports feature is not available to tenants hosted in the UK and France due to local compliance. We are working to make reports available to tenants in these two regions and will send communication when this feature becomes available. 

## Data Protection

- Viva Learning follows GDPR guidelines for storing data.

- Viva Learning doesn't collect any personally identifiable information. 

-  All reports are anonymous. Data can't be directly linked to a user or device.  

- Data is stored in Viva Learning for six months. 

- Viva Learning metrics aren't designed to enable evaluation, tracking, automated decision making, profiling, or monitoring.

## Prerequisites

### Permissions to access Viva Learning reports  

Reporting is available for the following roles:

- Knowledge admin

- Knowledge manager  

- Global administrator

You can also manage access to reports through Microsoft 365 groups.  

### Ensure telemetry is enabled in the MAC portal  

In the Microsoft Admin Center, ensure that the required diagnostic data and optional diagnostic data fields are turned on. 

:::image type="content" source="../media/learning/reports-telemetry-enabled-mac.png" alt-text="Screenshot of checked boxes in the MAC settings with Learning Record Sync and Diagnostics data options enabled." lightbox="../media/learning/reports-telemetry-enabled-mac.png":::

## How to access reports 


Access to reports is controlled via Microsoft 365 (Microsoft 365) groups. By default, reports are enabled for learning path Microsoft 365 group, knowledge admins, knowledge managers, and global admins.

Access to reports can be controlled from the **Feature access management** section in the **admin tab**.

Go to the Viva Learning admin tab and select **Reports**.  

:::image type="content" source="../media/learning/reports-adoption.png" alt-text="Screenshot of the adoption view report indicating monthly active users and growth rate of adoption." lightbox="../media/learning/reports-adoption.png":::

### Viva Learning reporting metrics 

| Metric | Description 
|:-----|:----- |
| Monthly Active Users | Total number of unique users who have launched the Viva Learning personal app in the last 30 days. |
|Weekly Active Users | Total number of unique users who have launched the Viva Learning personal app in the last 7 days. |
| Daily Active Users | Total number of unique users who have launched the Viva Learning personal app on that day. |
| Monthly Engaged Users | Total number of unique users who have taken five or more intentional actions. The intentional actions are: Search, Bookmark, Share, Copy Link, Recommendation, Add to calendar, Interest selection, Ratings, and Playing content. | 
|Engaged Quality Learners | Total number of unique users who have taken two or more elective(non-assigned) courses in a month. | 
| Content Played | Total number of courses played by learners in a month. | 
| Content Bookmarked | Total number of courses bookmarked by learners in a month. |
| Learning Paths Viewed | Total number of learning paths viewed by learners in a month. |
| Learning Collections Viewed | Total number of learning collections viewed by learners in a month. |
|Content shared | Total number of courses shared by learners in a month. |
| Content Recommended | Total number of courses recommended by learners in a month. |
|Searches on Personal app | Total number of searches in the Viva Learning personal app in a month. |

## Export reports 

Users can export all the available reports data into a single Excel file using the Export all reports option available at the top on Viva Learning admin reports page:

1. Go to the Viva Learning admin tab and select **Reports**. 

2. Select **Export all reports** to export all the available reports data.


Individual reports data can be exported into an Excel file using the Export option available for each report. 

1. Go to the Viva Learning admin tab and select **Reports**. 

2. Select **Export** to export individual report data.

    
## Data refresh rate 

Daily Active Users (DAU) report data is updated daily. 
Data for all other reports is updated monthly on the third of every month in the GMT time zone.



## FAQ 


- **Why does Viva Learning collect telemetry data?**

    To provide usage insights of Viva Learning to organizations. 

- **Does Viva Learning capture any personally identifiable information (PII)?** 

    We don't collect any PII data. The data collected for these reports can't be directly linked to a user or device.

- **How does Viva Learning keep customers’ data safe?**  

    Data is transmitted using SSL and access is highly restricted. It's only granted to Microsoft personnel who can demonstrate a valid business need (for example, to a product team to fix an issue).  

- **Does Viva Learning follow GDPR guidelines for telemetry?** 

    Yes, we follow GDPR guidelines for storing telemetry data   

- **How often is data refreshed?** 

    Daily Active Users (DAU) report data is updated daily. 
    Data for all other reports is updated monthly in the GMT time zone.


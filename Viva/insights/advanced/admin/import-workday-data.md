---
title: Import organizational data from Workday
description: Learn how to set up a connection and import your data from Workday to the Viva Insights advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data from Workday

Your organizational data can appear in the Microsoft Viva Insights’ advanced insights app in one of four ways: 

* Through Azure Active Directory, which is the default source
* Through a .csv file that you as an Insights Administrator upload
* Through an automated data import that you, your source system admin, and your Microsoft 365 IT admin set up
* Through a connection between Workday and Viva Insights

This article talks about the fourth option: importing data through a Workday connection.

## Prerequisites

Before you can set up a connection between Workday and Viva Insights, you'll need the following information about your Workday environment from your Workday admin:

* Tenant name
* Username
* Password

## Set up your Workday connection

*Applies to: Insights Administrator*

1. In the advanced insights app's admin experience, go to either the **Data hub** or the **Organizational data** page.
    * On the Data hub page, select **Start** under **Data source > Workday connector**.
    * On the **Organizational data** page's **Data connection** tab, select **Manage data sources**. Then, select **Start** under **Workday connector**. 
1. Enter a name for your connection.
1. Under **Set up Workday connection**:
    1. Enter the Workday tenant name, username, and password.
    1. Select how frequently you want Workday to send data to Viva Insights: weekly or monthly.
1. Select the box under **Authorization status** to allow Workday to start sending data to Viva Insights.


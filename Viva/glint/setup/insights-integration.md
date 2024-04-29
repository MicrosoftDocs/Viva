---
title: Integrate Viva Glint into Viva Insights (preview)
description: Connect sentiments about how people work with sentiments about how people feel by sending Viva Glint survey feedback to Viva Insights Power BI.
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/29/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Integrate Viva Glint into Viva Insights (preview)

HR analysts and other leaders can bring Viva Glint survey scores into Viva Insights to integrate how people feel (Glint) with how people work (Insights). Connect Copilot usage metrics to uncover insightful information about employee sentiments by sending survey results from Viva Glint to Viva Insights Power BI.

>[**Introduction to Microsoft Viva Insights**](/../viva/insights/introduction)
>
>[**Connect to Viva Insights using the Power BI Connector**](/../viva/insights/advanced/analyst/power-bi-connector)

## Understand use case for the integration

Integrate your employee engagement survey scores - “how employees feel” - with your Viva Insights data - “how people work” - to understand employees’ work experience and improve key outcomes for your organization more fully.

## What data can be sent to Viva Insights?

 - Only data from recurring or ad-hoc surveys with confidentiality thresholds equal to or above the Viva Glint default of five respondents.
 - Only rating item scores. No comments data is sent.

## Supported languages

All languages supported for question labels and question text by Viva Glint are sent to Viva Insights Power B

>[!NOTE]
>Global admins cannot include Works Council employee data in the Viva Insights integration.

## Setting up the Viva Insights integration from your admin dashboard

>[!IMPORTANT]
> By sending data to Viva Insights, you’re agreeing to have Viva Glint data sent and stored within Insights.

:::image type="content" source="../../media/glint/setup/microsoft-viva-integrations-dashboard.png" alt-text="Screenshot of accessing the Viva Insights configuration feature from the admin dashboard.":::

Select **Set up integration**. 

> :::image type="content" source="../../media/glint/setup/insights-set-up-integration.png" alt-text="Screenshot of Set up integration button.":::

The *Send data to Viva Insights* page opens. **Select the program to send data from**. You may select multiple programs.

Selecting a program sends data for every closed program cycle and sets up the program to automatically send data for future cycles. In Viva Insights, map which program data to display on the Viva Insights dashboard.

Only Viva Glint scores are available in aggregate in the Viva Insights Power BI dashboard. No comments or attributes are shared to Viva Insights. By sending data to Viva Insights.

Select **Send data to Viva Insights**

:::image type="content" source="../../media/glint/setup/insights-select-programs.png" alt-text="Screenshot of choosing program data to send to Viva Insights.":::

**Now, [connect to the Microsoft Copilot dashboard](/../viva/insights/org-team-insights/copilot-dashboard) or any survey data on the [Insights Power BI template.](/../viva/insights/advanced/analyst/templates/introduction-to-templates)**

## Removing a program from the integration

As an admin, you can stop sharing future data with Viva Insights by removing the program. Select **Manage Integration**.

:::image type="content" source="../../media/glint/setup/insights-manage-integration.png" alt-text="Screenshot managing the Viva Glint and Viva Insights integration.":::

Hover over the ellipses net to the program to remove to access the actions available. Select **Remove program.**

:::image type="content" source="../../media/glint/setup/insights-remove-program.png" alt-text="Screenshot of  removing Viva Glint data from being sent to Viva Insights.":::

## Coming soon - bring Viva Insights into Viva Glint! 

Add Viva Insights metrics to Viva Glint to dive deeper into employee sentiment. If you're interested in the private preview, reach out to your CxPM or hotline assistant.

:::image type="content" source="../../media/glint/setup/insights-coming-soon.png" alt-text="Screenshot of Importing Viva Insights Data.":::

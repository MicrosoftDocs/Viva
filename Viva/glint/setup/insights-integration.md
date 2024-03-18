---
title: Integrate Viva Insights into Viva Glint
description: Connect Copilot usage metrics and uncover greater insights about employee sentiments by sending Viva Glint feedback survey results to Viva Insights Power BI.
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
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/18/2024
---

# Integrate Viva Insights into Viva Glint

>[!IMPORTANT]
>This integration is available beginning on April 9, 2024.

Bring Viva Glint feedback scores into Viva Insights to stay on top of Viva Glint data in your everyday dashboard. Connect Copilot usage metrics and uncover insightful information about employee sentiments by sending recurring and ad-hoc survey results from Viva Glint feedback to Viva Insights Power BI.
>[**Introduction to Microsoft Viva Insights**](../viva/insights/introduction)
>
>[**Connect to Viva Insights using the Power BI Connector**](../viva/insights/advanced/analyst/power-bi-connector)
>
>

## Understand use cases for the integration

Two prominent use cases for this data integration:  

- Use the [M365 Copilot Impact Survey in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2261039) to collect feedback from your M365 Copilot users and connect their sentiments with Copilot usage metrics on the Viva Insights Copilot dashboard.  
- Send your employee engagement survey scores to the Viva Insights Power BI template to find behavioral drivers of employee sentiments.

## Which data can be sent to Viva Insights?

 - Only data from recurring or ad-hoc surveys with confidentiality thresholds equal to or above the Viva Glint default of five respondents.
 - Only rating item scores. No comments data is sent.

## Prerequisites for the integration

The Viva Glint Global admin permissions Viva Insights to use Viva Glint feedback data before integration. Integration begins in the Microsoft 365 Admin Center (MAC).

1. Hover over *Manage data sharing with Glint* to open the slider window.
1. Select **I authorize sharing Insights data with Glint**.
2. Select **Save**.
> :::image type="content" source="../../media/glint/setup/insights-consent.png" alt-text="Screenshot of Viva Glint Global admin managing data sharing with Viva Insights."lightbox="../../media/glint/setup/insights-consent.png":::
 
> :::image type="content" source="../../media/glint/setup/insights-consent-slider-window.png" alt-text="Screenshot of Viva Glint Global admin authorizing data sharing with Viva Insights.":::

>[!NOTE!]
>Global admins cannot include Works Council employee data in the Viva Insights integration.

Now the Viva Insights admin contacts the Viva Glint admin.

## Setting up the Viva Insights integration from your admin dashboard

Viva Glint data can be sent from recurring and ad-hoc surveys only. Send survey data to Viva Insights by creating an Employee Experience report. 

:::image type="content" source="../../media/glint/setup/microsoft-viva-integrations-dashboard.png" alt-text="Screenshot of accessing the Viva Insights configuration feature from the admin dashboard.":::

Select the **Set up integration** button. 

> :::image type="content" source="../../media/glint/setup/insights-set-up-integration.png" alt-text="Screenshot of Set up integration button.":::

The *Send data to Viva Insights* page opens. **Select the program to send data from**.

By selecting a program, you are sending data for every closed program cycle and setting up the program to automatically send data for future cycles. In Viva Insights, map which program data to display on the Viva Insights dashboard (available.

Only Viva Glint scores are available in aggregate in the Viva Insights Power BI dashboard. No comments or attributes are shared to Viva Insights. By sending data to Viva Insights, you are agreeing to have Viva Glint data sent and stored within Insights.

Select **Send data to Viva Insights**

:::image type="content" source="../../media/glint/setup/insights-select-programs.png" alt-text="Screenshot of choosing program data to send to Viva Insights.":::

## [Connect to the Microsoft Copilot dashboard](../viva/insights/org-team-insights/copilot-dashboard)


## Coming soon! 

:::image type="content" source="../../media/glint/setup/insights-coming-soon.png" alt-text="Screenshot of Importing Viva Insights Data - coming soon!":::

Add Viva Insights metrics to Viva Glint to dive deeper into employee sentiment.

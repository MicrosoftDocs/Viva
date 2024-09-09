---
title: Integrate Viva Glint and Viva Insights to maximize data insight (public preview)
description: Organizational leaders, HR analysts, and other stakeholders can bring Microsoft Viva Glint and Microsoft Viva Insights together into their business to better understand their people’s full work experience. 
ms.author: v-zachminers
author: zachminers
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
ms.date: 09/09/2024
---

# Integrate Viva Glint and Viva Insights to maximize data insight (preview)

>[!IMPORTANT]
> This feature is available to public preview customers only. Features described here are subject to change.

Organizational leaders, HR analysts, and other stakeholders can bring Microsoft Viva Glint and Microsoft Viva Insights together into the rhythm of their business to better understand their people’s full work experience.   

Integrating your Viva Glint employee survey scores (how employees feel) with your Viva Insights data (how people work) helps identify your teams’ opportunities and strengths to meet organizational goals. 

To send data from Viva Glint surveys to Viva Insights, the survey data must meet [Glint’s confidentiality thresholds](https://go.microsoft.com/fwlink/?linkid=2275271). All languages supported by Glint for question labels and question texts are sent to Insights.

## Scenarios for using Insights and Glint together 

- **As a manager or leader**, you may want to see how different behaviors impact engagement levels for your team after a recent engagement survey. You can use the Glint Team Summary dashboard to see how different behaviors impact engagement.   With this information, you can look for patterns and use those patterns to find strengths and opportunities within your team. Then, in Viva Insights, look at how different advanced metrics - like manager 1:1 time or after-hours work - impact various engagement drivers, and take action if needed.     

- **As a leader**, you may want to look across teams to see how different behaviors impact engagement levels and different engagement drivers. Use the Glint Heatmap report to see how different Viva Insights metrics- like collaboration hours or network size - impact engagement. You can see which teams are doing well for engagement and which teams might be struggling. Filter further in the employee comments by specific behaviors to understand what employees are saying about their experience. With this knowledge, you can work with specific teams in areas to improve productivity.  

- **As an HR analyst**, you may want to better understand how your recent Viva Glint engagement survey relates to collaboration data from Viva Insights. Use the Glint with Viva Insights PowerBI template to see how engagement scores relate to behavior. Use the Overview tab in the PowerBI template to quickly highlight which behaviors have a strong relationship to different engagement drivers. Explore these relationships further by looking at specific Glint survey items and compare them to different behavioral metrics and teams.

## Prerequisites to the integration

To ensure that employee records between Viva Glint and Viva Insights are matched for this integration:

- The employee's **Glint user email** must be added to their [Entra ID](https://go.microsoft.com/fwlink/?linkid=2238425).
- All **Glint user email domains** must be added to your **tenant's MAC domain list**.
- Optional, but highly recommended: Enable **Require Entra ID for links in survey emails** in General Settings from the Glint admin  dashboard.

## Set up the integration

Now that you understand the benefits of integrating Viva Glint and Viva Insights, you’re ready to set up the integration. Use these links:

### Workflow to send Viva Glint data to Viva Insights 

1. The **Viva Insights admin** sets up a new import in the advanced insights app. [Learn more about how to start the process](/viva/insights/advanced/admin/import-survey-glint).

2. The **Viva Insights admin** contacts the **Viva Glint admin** to share Viva Glint survey data, and the **Viva Glint admin** selects specific survey programs and sends the data to Viva Insights. [Learn more about this step](/viva/glint/setup/insights-integration).

3. **Viva Insights** validates and processes the data so it’s ready for use. [Learn more about this step](/viva/insights/advanced/admin/import-survey-glint#3-data-validation-and-processing).

### Workflow to send Viva Insights data to Viva Glint

1. The **Microsoft 365 Global admin** consents to share Viva Insights data with Viva Glint. [Learn more about how to start the process](/viva/insights/advanced/admin/export-insights-data-glint).

2. The **Viva Glint admin** sets up the integration and adds the relevant metrics from Viva Insights. [Learn more about this step](/viva/glint/setup/insights-to-glint).

## Additional resources for Viva Insights admins and analysts

* **Admins**: [Set up partitions that include Glint survey data](/viva/insights/advanced/admin/partitions)

* **Analysts**: [Learn how to run the Glint and organizational insights report](/viva/insights/advanced/analyst/templates/glint)

## Download the playbook

Audience: For HR leadership, HR business partners, people analytics specialists and others who analyze larger groups of employee data in your organization. 

[The Viva Glint + Viva Insights Playbook](https://adoption.microsoft.com/viva/glint/) outlines strategic guidance for combining sentiment and work patterns data and illustrative examples of how these can provide insight value for your organization. Use this playbook to understand how to interpret combined Viva Insights and Viva Glint data to unlock deeper insights into your people's experiences. Drive meaningful action to support improved employee engagement.
---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 01/26/2024
title: Set up your queries using Copilot
description: Learn how to use Microsoft Copilot while setting up your custom queries
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: abelubetk
audience: Admin
---

# Set up your queries using Copilot

>[!IMPORTANT]
> This feature is for private preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

With custom queries, you can investigate and answer specific questions about productivity and collaboration within your organization. For example, you might want to see whether employees are spending more time sending emails after work hours than during work hours. Or, you might want to determine if employees are receiving adequate coaching time with their manager. But sometimes, you might need help to translate your questions into queries that Viva Insights can compute. That’s where Copilot can help.

When you set up a [custom person query](./person-query.md), Copilot can suggest which specific metrics to use for your analysis, and even help you home in on the right questions to investigate. 

This feature is currently only available within person queries, but gradually we’ll roll it out to all analyst query types.

## How to use Copilot with your query

First, to access custom person queries, follow this navigation in the [advanced insights app](https://analysis.insights.cloud.microsoft):

**Analysis** > **Custom queries** > **Person queries** > **Start analysis**

Then, use [these steps](./person-query.md#set-up-your-query) to enter basic information like the query name, time period, and description.

Next, you need to add metrics. This is where Copilot comes in. In the upper right of the page, select **Copilot**.

A panel will appear with suggested focus areas and questions for your query, such as, “How much time do people spend in different collaboration modes?” If you select one of these questions, Copilot will suggest specific metrics for your query.

:::image type="content" source="../images/copilot-analyst-query-01.png" alt-text="Screenshot that shows recommended questions from Copilot to set up the query":::

Or, if you already have a specific question in mind, type it in natural language, and Copilot will suggest metrics for the question you’re looking to answer.

:::image type="content" source="../images/copilot-analyst-query-02.png" alt-text="Screenshot that shows recommended metrics from Copilot to set up the query":::

If you want to use the metrics Copilot suggests, select **Add to this query**. Those metrics will appear in the **Metrics** section on the main setup page, where you can also remove individual metrics from the query.

Or, if you want to rephrase your question or ask a different question for a different set of suggested metrics, type the new question in the Copilot panel.

After you’ve chosen your metrics, if you want to ask another question, type it in the panel. To use the metrics suggested for that new question instead of the metrics you’ve already chosen, select **Replace the current query**.

When you’re ready to run the query, in the screen’s upper right, select **Run**. You can [access the query’s results](./query-results.md) just like you normally would.
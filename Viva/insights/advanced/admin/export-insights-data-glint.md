---
title: Export Viva Insights data to Viva Glint
description: Learn how to set up a connection between Glint and Viva Insights to export your Insights data to the Viva Glint platform.
author: zachminers
ms.author: v-zachminers
ms.date: 08/28/2024
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Export Viva Insights data to Viva Glint (preview)

>[!IMPORTANT]
> This feature is for public preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

You can share specific Viva Insights metrics about your employees with Viva Glint, to add more context to the survey responses employees provide through Glint. Through this integration, you can add more data about how employees work (Viva Insights) to the employee feedback data you have (Viva Glint). This can give you a clearer picture about what might be driving employee sentiment and survey responses.

First, to send Viva Insights data to Viva Glint, your Microsoft 365 Global Administrator must consent to share the data, using the steps below. 

**Workflow**

1. The **Microsoft 365 Global admin** consents to share Viva Insights data with Viva Glint.

2. The **Viva Glint admin** sets up the integration and adds the relevant metrics from Viva Insights.

## Consent to share Viva Insights data with Viva Glint 

>[!Note]
> Only the Microsoft 365 Global admin can enable sharing of Viva Insights data. The Global Reader, Exchange admin, and Insights admin have view privileges for the setting.

1. Log in to the [Microsoft 365 admin center](https://admin.microsoft.com).

2. In the menu on the left, select **Settings**, then **Viva**.

    :::image type="content" source="../images/egress-viva-settings.png" alt-text="Screenshot that shows where to access Viva in settings.":::

3. On the Viva page, select **Viva Insights**.

    :::image type="content" source="../images/egress-viva-insights.png" alt-text="Screenshot that shows where to access the Viva Insights connection.":::

4. Select **Add-on Plan**, then select **Manage data sharing with Glint**.

    :::image type="content" source="../images/egress-manage-data-sharing.png" alt-text="Screenshot that shows where to access the manage data sharing setting.":::

5. Review the authorization, then select **I authorize sharing data with Glint**. Select **Save**.

    :::image type="content" source="../images/egress-authorize.png" alt-text="Screenshot that shows how to authorize the connection.":::

6. The Viva Glint admin can now set up the integration and select the metrics they’d like to connect to their survey data using [these steps](https://go.microsoft.com/fwlink/?linkid=2281411).

## Remove consent to share Viva Insights data with Glint

The steps below must be performed by the Microsoft 365 Global admin.

1. Log in to the [Microsoft 365 admin center](https://admin.microsoft.com).

2. In the menu on the left, select **Settings**, then **Viva**.

    :::image type="content" source="../images/egress-viva-settings.png" alt-text="Screenshot that shows where to access Viva in settings.":::

3. On the Viva page, select **Viva Insights**.

    :::image type="content" source="../images/egress-viva-insights.png" alt-text="Screenshot that shows where to access the Viva Insights connection.":::

4. Select **Add-on Plan**, then select **Manage data sharing with Glint**.

    :::image type="content" source="../images/egress-manage-data-sharing.png" alt-text="Screenshot that shows where to access the manage data sharing setting.":::

5. Uncheck the box for **I authorize sharing data with Glint**. Select **Save**.


## Shareable Viva Insights metrics

Below is a list of all Viva Insights metrics that can be shared with Viva Glint. Once the Microsoft 365 Global admin gives consent, the Glint admin may select which metrics to include for a specific survey and time period.  

* Email hours 
* Call hours 
* After-hours collaboration hours 
* Multitasking hours 
* Collaboration hours 
* Uninterrupted hours 
* Meeting hours 
* Meeting hours with manager 1:1 
* Internal network size 
* Meeting hours with skip level 
* MetricDate

## FAQ

**How long does it take for Viva Insights data to export to Viva Glint after the Glint admin sets up the integration?**

About two hours.

**What happens if the Microsoft 365 Global admin turns off sharing and there is a request to send Viva Insights data to Viva Glint in progress?**

If the Microsoft 365 Global Admin turns off sharing the request will fail.

**Is there a way to change which Viva Insights metrics are available to be shared with Viva Glint?**

It's a fixed list of metrics, and you can’t change which metrics are available.

**What if the survey population does not have Viva Insights licenses? Will there still be Viva Insights data for these users?**

Viva Glint only receives metric data for employees who have a paid Viva Insights license.

**What time period does the shared Viva Insights data cover?**

The Viva Glint admin [controls this setting](https://go.microsoft.com/fwlink/?linkid=2281411).


## Related topics

[Import survey results from Viva Glint](../admin/import-survey-glint.md)

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
ms.date: 05/10/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Integrate Viva Glint into Viva Insights (preview)

HR analysts and other leaders in your organization can bring Microsoft Viva Glint survey scores into Microsoft Viva Insights to learn how people feel – Glint- along with how people work - Insights.  This integration gives your organization a complete picture of the employee's experience.

>[**Introduction to Microsoft Viva Insights**](/../viva/insights/introduction)

>[**Connect to Viva Insights using the Power BI Connector**](/../viva/insights/advanced/analyst/power-bi-connector)

## Workflow overview 

1. The Viva Insights admin sets up a new import in the advanced insights app. 

1. The Viva Glint admin selects specific survey programs and sends the data to Viva Insights. 

1. The Viva Insights admin validates and processes the data. 

## What data can be sent to Viva Insights?
Data that can be sent:
- Data from recurring or ad-hoc surveys with confidentiality thresholds equal to or above the Viva Glint default of five respondents.
- Rating item scores, but no comments.
- All Viva Glint languages supported for question labels (names) and question text are sent to Viva Insights Power BI.

> [!NOTE]
> Global admins cannot include Works Council employee data in the Viva Insights integration.  

> [!IMPORTANT]
> By sending data to Viva Insights, you agree to have Microsoft Viva Glint data sent and stored within Microsoft Viva Insights.

## Set up the Viva Insights integration from your admin dashboard

After the Viva Insights admin sets up the import and contacts you that the process is ready for you to share Viva Glint survey data, follow these steps:

1. From your Glint admin dashboard, select the **Configure symbol** and then **Viva Insights** from the *Microsoft Viva Integrations* section.

   :::image type="content" source="../../media/glint/setup/microsoft-viva-integrations-dashboard.png" alt-text="Screenshot of accessing the Viva Insights configuration feature from the admin dashboard.":::

2. If you’d like, use the **Learn More** button for more information about the integration.

   :::image type="content" source="../../media/glint/setup/glintsights-setup-v2.png" alt-text="Screenshot of the Learn More and Set up integration buttons.":::

## Sending and managing data

This guidance is for the initial data send to Insights only.

1. On the *Send Data to Viva Insights* page, **Select Programs** by enabling the checkbox next to the recurring or ad hoc program listed. You can choose more than one program.

   :::image type="content" source="../../media/glint/setup/glintsights-select-programs-v2.png" alt-text="Screenshot of the Send data to Viva Insights button.":::

2. Select **Send data to Viva Insights.**

3. You see this confirmation:

:::image type="content" source="../../media/glint/setup/glintsights-confirm-v2.png" alt-text="Screenshot of confirmation message that your data is sent to Viva Insights.":::

4. Select **Close.**

### Send other survey programs to Viva Insights

1. In the **Send Data to Viva Insights** section, the button changes to read **Manage Integration**. Use that button to send more programs to Viva Insights.

   :::image type="content" source="../../media/glint/setup/glintsights-manage-integration-v2.png" alt-text="Screenshot of how to send more data to Viva Insights.":::

2. Select **+ Add Programs.**
3. In the *Add Program* window, select any available program to add. You can select multiple programs. Select **Add** next to the program.

   :::image type="content" source="../../media/glint/setup/glintsights-add-program-v2.png" alt-text="Screenshot of how to add programs.":::

4. A message confirms that your program or programs have been added. 

5. Be sure that the name of the program you added now appears under Programs on the Send data to Viva Insights page.
   
> [!IMPORTANT]
> Selecting a program sends data for every closed program cycle and automatically sends data for future cycles. In Viva Insights, you’ll be able to map which program data to display on the Viva Insights dashboard.

### Data validation and processing

After sending data from Viva Glint, the Insights app validates it and provides status messages about the import. 
If processing fails, try running the import again, and resending your survey data. If you’re still getting a failed status, [file a support ticket](/microsoft-365/admin/get-help-support).

## Remove a program after initial setup

After sending data to Viva Insights, you can continue to manage your integration. You can stop sharing future data with Viva Insights by removing the program. Return to your Viva Glint admin dashboard and follow the same instructions as you did in the initial setup. The Setup integration button now reads Manage integration.

1. Select **Manage Integration**.
2. Hover over the ellipses next to the program to reveal the actions available. Select Remove program.

   :::image type="content" source="../../media/glint/setup/glintsights-remove-program-v2.png" alt-text="Screenshot of how to remove programs.":::

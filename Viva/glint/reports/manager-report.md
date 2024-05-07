---
title: The Viva Glint Manager Report
description: "The Manager Report displays a Directs or Roll-up Hierarchy view for two preselected survey items within a specific hierarchy."
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/07/2024
---

# The Viva Glint Manager report in Viva Glint

The Microsoft Viva Glint Manager Report displays a *Directs* or *Roll-up Hierarchy* view of comparisons for two different survey items. These preset items are assigned during survey setup and are the default settings. The manager or Human Resource Business Partners (HRBP) can change which items are displayed by using the **question label** at the top of the column. Similar to other reports, column headers are static and can be used as a sorting feature. 

:::image type="content" source="../../media/glint/reports/manager-report.png" alt-text="Screenshot of the Manager Report access card in the admin Reports tab.":::

## Manager Report terminology

|Hierarchy|Definition|
|---------|---------|
|Directs|Displays data for all *managers* within a specific managerial roll-up hierarchy. It only displays data for employees that report directly to that manager.|  
|Roll-up|Displays data for all *employees* within a manager's hierarchy. This data includes any employees that fall below a manager in the org chart, even if they don't report directly to that manager. In other words, more levels of the organizational chart. |

## Use the Manager Report filter 

The Manager Report has a unique filter option, which isn't present in other reports. 

1. From the *Manager Report* page, select **Add a filter.**

:::image type="content" source="../../media/glint/reports/manager-report-add-a-filter-button.png" alt-  text="Screenshot of the Manager Report Add a filter button.":::

2. In the *Filter By* box, select **+ Add Filters** to open the *Select Filter Type* dropdown menu.
3. From the dropdown box, select either **Managers** or **Respondents**. 
   1. The **Managers** filter looks at HRIS attribute values for the manager themselves. *Manager* refers to a 
    people leader with people reporting up to them at the time of the survey launch and qualified for survey 
    results.
   1. The **Respondents** filter looks at all HRIS attribute values for the individual employees who report into that manager.
  
:::image type="content" source="../../media/glint/reports/manager-report-select-filter.png" alt-        text="Screenshot of the Select Filter Type button.":::

4. After selecting **Managers** or **Respondents**, a new dropdown menu displays all attributes sent to Glint in your HRIS data file. Choose the attribute you want to study. As appropriate, more dropdown menus become availablle to drill down the desired attribute even further.

5. Use the **Close Filter X** to remove the top section from your screen.

## Choose your report settings

1. Select the **Settings** button to open the *Report Settings* window.
2. First, Choose your benchmark to help users interpret survey results within the context of how others are doing. Glint provides several options for benchmark reporting:
   - **Company:** Displays your team's scores compare to your company's scores. This comparitor is the most commonly used benchmark.
   - **My Teams:** Compares a single team's score to an overall score based on all of the teams you have access to. This comparison is recommended if you have more than one area of responsibility.
   - **Average Question:** Displays your team's scores compared to a single, overall score for all questions your team rated. Helpful if you are focused on the variance in scores within your own data, rather than comparing to another group.
3. Use the **Group by** dropdown menu to choose **none, manager**, or **location hierarchy**.
1. Use the **Key Metric** dropdown menu to show the report in terms of **scores** or **favorability**.

## Export and Share

Share your results with leaders and stakeholders in the way that works best for you. Select the **Export and Share** button for access to these options:

:::image type="content" source="../../media/glint/reports/overall-export-share.png" alt-text="Screenshot of exporting and sharing options.":::

   




---
title: Reporting setup in Program Summary of Viva Glint
description: On the Reports page admins, customize how dashboards are set up and how specific roles view them. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Live access, phased access, BTI, broader team insights, aggregate indices, aggregate index 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 01/18/2024
---

# Reporting setup in Program Summary

The Reporting page allows admins to see and customize how dashboards are set up for specific User Roles to view survey results.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting.png" alt-text="Screenshot that shows how to access Reporting in Program Summary.":::

## View and add Program Roles

In the **Program Roles** section, you'll see and set how [User Roles](https://go.microsoft.com/fwlink/?linkid=2230740) have been permissioned to see survey results. 

### View Program Roles already permissioned to see feedback for this program

Roles already set up for this program are listed under the **Program Roles** row, each displaying on its own row.
**Select the row** to view what has been configured for that role. In the example below, the Manager row was previously configured and you can see what permissions have been assigned. Assigned permissions include:

 - **Reporting View** - Whether the manager has been granted [Live or Phased access](https://go.microsoft.com/fwlink/?linkid=2230747).
 - **Concierge Visibility** - Whether this User Role will see the [Manager Concierge]( https://go.microsoft.com/fwlink/?linkid=2231115) feature on their dashboard.
 - **Broader Team Insights** - Whether a high-level summary of this User Role's survey results are visible to their direct reports or roll-up hierarchy. [Learn about Broader Team Inights](https://go.microsoft.com/fwlink/?linkid=2231012).
 - **Default Dashboard** - [Team Summary]( https://go.microsoft.com/fwlink/?linkid=2231116) is the default Viva Glint manager dashboard experience. That can be changed by using the dropdown menu to select a different report; only one report is available if not using Team Summary.
   
 > [!IMPORTANT]
 > Company Admin roles be granted access to the [Executive Summary dashboard](https://go.microsoft.com/fwlink/?linkid=2231010).
   
 - **Report Template Access** - The individual reports this User Role can view. Select the **X** to delete a report or use the Search box to add a report. [Learn about Viva Glint reports](https://go.microsoft.com/fwlink/?linkid=2231109).

:::image type="content" source="/../../media/glint/program-summary-reporting-add-manager-example.png" alt-text="Screenshot that shows the features permissioned for a User Role.":::

### Add Program Roles to permission them to see feedback for this program

To add Uer Roles to a program, select **Add Role**. The dropdown menu displays User Roles already created within the [User Role feature](https://go.microsoft.com/fwlink/?linkid=2230740). Select any roles that should have reporting permissions for this program. The User Role name now appears as its own row.

>[!TIP]
>Use the up or down arrow to view or close permissions set up for each role.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-add-role.png" alt-text="Screenshot of Program Roles and the Add Role feature.":::

## Set up reporting for this program
There are six fields to set up for your program.

### Aggregate Indices

For most surveys, using aggregate indices is not recommended. Aggregates are groups of questions which are similar. For surveys with a large number of items, however, it can make sense to group similar questions into aggregates. Typically, these are statistically validated constructs which contain highly correlated questions. Only rating-type questions can be a part of aggregate indices.

If adding an Aggregate Index:

1. Select **+ Add Aggregate Index** to open the Create Aggregate slider window.
2. In the new window, enter an aggregate name of your choosing. 
3. For **Calculation Method**, choose from one of the following options:
   - Select **Average** - Recommended. Select from all rating questions. Qverage score = (a+b+...+n)/n, with the range from 0 to 100.  
   - Select **eNPS (employeee Net Promoter Score)** - Select only one calculated 11-scale rating question. eNPS = (number of promoters - number of detractors) / (number of respondents) x 100, with the range from -100 to 100.
   >[!CAUTION]
   >If you change the calculation method, you'll need to reselect at least one question below.

   > [!NOTE]
   > Viva People Science doesn't recommend the use of an employee Net Promoter Score<sup>TM</sup> due to its calculation method and inability to act as the best predictor of employee engagement.
   
5. In the **Add Questions** dropdown menu, search and select your items to be grouped together. Your questions should now appear in the **Selected Questions** box. 
6. Select the **Include in Driver Impact Report** checkbox to see this aggregate in the Driver Impact Report.
7. Select **Save and Add to Program**.
8. Select **X** to close the slider window.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-create-aggregate.png" alt-text="Screenshot of the Create Aggregate slide window in Reporting setup.":::

>[!TIP]
> Use Glint's 2-item Standard Engagement Index and no other aggregates. Glint has strong benchmarks on this measurement, which can provide insightful focus areas in results reporting.

>[!NOTE]
> When Glint's 2-item index is used, we recommend using it on every survey to ensure the capture of engagement trends to accumulate benchmark data.

### Key Outcome

Select the desired **Key Outcome** from the dropdown menu. The key outcome is usually the main result of the survey. It can be the score from a single question or an aggregate index. This appears as the most prominent score displayed in most reports.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-key-outcome.png" alt-text="Screenshot of the Key Outcome dropdown menu in Reporting setup.":::

> [!NOTE]
> Changes to key outcome will be displayed immediately upon saving.

### Driver Impact Outcomes

Select the **Driver Impact Outcomes** from the search field. Select a set of outcome questions or aggregates that will be used for driver impact analysis. This analysis will calculate the impact of each question or aggregate on the selected outcome and show it on a chart.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-driver-impact.png" alt-text="Screenshot of the Driver Impact Outcomes section in Reporting setup.":::

### Manager Report Defaults

Select the desired **Manager Report Defaults**. Select up to two questions that will appear by default in the manager report.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-manager-defaults.png" alt-text="Screenshot of an example of survey items that appear on a  manager's dashboard.":::

### PowerPoint Export Template

Select your desired **PowerPoint Export** template. The Viva Glint ACT guide appears as the default export.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-export-template.png" alt-text="Screenshot of the template choices for exporting a reporting PowerPoint.":::

### Boarder Team Insights Export Template 

Select the desired **Broader Team Insights PowerPoint Export** template.

:::image type="content" source="/../../media/glint/setup/program-summary-reporting-bti.png" alt-text="Screenshot of the template choices for exporting a Broader Team Insight report.":::

**To complete this page, select the right-facing arrow to **Save & Continue**.**

> [!div class="nextstepaction"]
> [Move onto Communications setup in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231342)



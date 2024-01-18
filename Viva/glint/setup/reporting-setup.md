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

:::image type="content" source="../../media/glint/setup/program-summary-reporting.png" alt-text="Screenshot that shows how to access Reporting in Program Summary.":::

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
 > Company Admin roles should have the [Executive Summary dashboard](https://go.microsoft.com/fwlink/?linkid=2231010).
   
 - **Report Template Access** - The individual reports this User Role can view. Select the **X** to delete a report or use the Search box to add a report. [Learn about Viva Glint reports](https://go.microsoft.com/fwlink/?linkid=2231109).

:::image type="content" source="../../media/glint/program-summary-reporting-add-manager-example.png" alt-text="Screenshot that shows how to access Reporting in Program Summary.":::

### Add Program Roles to permission them to see feedback for this program

To add Uer Roles to a program, select **Add Role**. The dropdown menu displays User Roles already created within the [User Role feature](https://go.microsoft.com/fwlink/?linkid=2230740). Select any roles that should have reporting permissions for this program. The User Role name will now appear as it's own row.

>[!TIP]
>Use the up or down arrow to view or close permissions set up for each role.

:::image type="content" source="../../media/glint/setup/program-summary-reporting-add-role.png" alt-text="Screenshot of Program Roles and the Add Role feature.":::

## Set up reporting for this program
There are six fields to set up for your program.

### Aggregate Indices

For most surveys, using aggregate indices is not recommended. For surveys with a large number of items, however, it can make sense to group similar questions into aggregates. Typically, these are statistically validated constructs which contain highly correlated questions. Only rating-type questions can be a part of aggregate indices.

If adding an Aggregate Index:

1. Select **+ Add Aggregate Index**.
2. In the **Create Aggregate** panel, enter a name. For example, <Engagement\> or the name, which makes the most sense for your users.
3. For **Calculation Method**, select **Average**.
4. In the **Search Questions** dropdown menu, search and select **eSat** and **Recommend** items.
5. Select the **Include in Driver Impact Report** checkbox to see this aggregate in the Driver Impact Report.
6. Select **Save Add to Program**.
7. Select **X** to close the panel.

To add employee Net Promoter Score<sup>TM</sup> (eNPS):

> [!NOTE]
> Viva Glint People Science doesn't recommend the use of an employee Net Promoter Score<sup>TM</sup> due to its calculation method and inability to act as the best predictor of employee engagement.

1. Select **+ Add Aggregate Index**.
2. In the **Create Aggregate** panel, enter a name. This displays in reports, select a name that makes the most sense for your users.
3. For **Calculation Method**, select **eNPS**.
4. In the **Search Questions** dropdown menu, search and select your eNPS question.

   > [!IMPORTANT]
   > To select eNPS, first set up the question in the Viva Glint [Question Library](https://go.microsoft.com/fwlink/?linkid=2230918) and add to the [Questions section](https://go.microsoft.com/fwlink/?linkid=2231415) in your program.
   
5. Select the **Include in Driver Impact Report** checkbox to see this aggregate in the Driver Impact Report.
6. Select **Save Add to Program**.
7. Select **X** to close the panel.

>[!TIP]
> Use Glint's 2-item Standard Engagement Index and no other aggregates. Glint has strong benchmarks on this measurement, which can provide insightful focus areas in results reporting.

>[!NOTE]
> When Glint's 2-item index is used, we recommend using it on every survey to ensure the capture of engagement trends to accumulate benchmark data.

### Key Outcome

Select the desired **Key Outcome** from the dropdown menu.

### Driver Impact Outcomes

Select the **Driver Impact Outcomes** from the search field.

### Manager Report Defaults

Select the desired **Manager Report Defaults**.

### PowerPoint Export Template

Select the desired **PowerPoint Export** template.

### Boarder Team Insights PowerPoint Export Template

Select the desired **Broader Team Insights PowerPoint Export** template.

To complete this page, select the right-facing arrow to **Save & Continue**.

>[!TIP]
>Now that you have set up your reports for managers to view, move onto [Communications setup in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231342)



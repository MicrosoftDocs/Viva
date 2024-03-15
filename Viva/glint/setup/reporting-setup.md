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
ms.date: 03/15/2024
---

# Reporting setup in Program Summary

The Reporting page allows admins to see and customize how dashboards are set up for specific User Roles to view survey results.

:::image type="content" source="../../media/glint/program-summary-reporting.png" alt-text="Screenshot that shows how to access Reporting in Program Summary.":::

## View and add Program Roles

In the **Program Roles** section, you see and set how [User Roles](https://go.microsoft.com/fwlink/?linkid=2230740) are permissioned to see survey results. 

### View Program Roles already permissioned to see feedback 

:::image type="content" source="../../media/glint/program-summary-reporting-add-role.png" alt-text="Screenshot that shows the features permissioned for a User Role.":::

Roles already set up for this program are listed under the **Program Roles** row, each displaying on its own row.
**Select the role row** to view what is configured. Assigned permissions include:

 - **Reporting Access** - Whether the manager is granted [Live or Phased access](https://go.microsoft.com/fwlink/?linkid=2230747).
 - **Concierge Visibility** - Whether this user sees the [Manager Concierge]( https://go.microsoft.com/fwlink/?linkid=2231115) feature on their dashboard.
 - **Broader Team Insights** - Whether a high-level summary of this role's survey results is visible to their direct reports or roll-up hierarchy. [Learn about Broader Team Insights](https://go.microsoft.com/fwlink/?linkid=2231012).
 - **Default Dashboard** - [Team Summary]( https://go.microsoft.com/fwlink/?linkid=2231116) is the default Viva Glint manager dashboard experience. Change by using the dropdown menu to select a different report. Only one report is available if not using Team Summary.
   
 > [!IMPORTANT]
 > Company Admin roles must be granted access to the [Executive Summary dashboard](https://go.microsoft.com/fwlink/?linkid=2231010).
   
 - **Report Template Access** - The individual reports this user can view. Select the **X** to delete a report or use the Search box to add a report. [Learn about Viva Glint reports](https://go.microsoft.com/fwlink/?linkid=2231109).
 - **Question Access** - By default all roles must have all questions selected. Admins can remove and add questions back as needed.

>[!NOTE]
>The Question Access feature becomes available on April 9, 2024. See *Setting up Question Access* section for guidance.

### Add Program Roles to permission them to see feedback for this program

To add User Roles to a program, select **Add Role**. The dropdown menu displays User Roles already created within the [User Role feature](https://go.microsoft.com/fwlink/?linkid=2230740). Select any roles that should have reporting permissions for this program. The User Role name now appears as its own row.

>[!TIP]
>Use the up or down arrow to view or close permissions set up for each role.

:::image type="content" source="../../media/glint/report-question-access-added" alt-text="Screenshot of Program Roles and the Add Role feature." lightbox="../../media/glint/setup/report-question-access-added.png"::: 

## Set up question access for roles

>[!NOTE]
>This feature becomes available on April 9, 2024.

:::image type="content" source="../../media/glint/report-questions-delete-add.png" alt-text="Screenshot of how to remove and add back survey questions by role."lightbox="../../media/glint/setup/report-questions-delete-add.png":::

### Setting up section-level permissions by role

Select **Select sections** from the *Question Reporting Access* section.
Remove a section by selecting the **X** next to the question. 
Add a section back by selecting **Add More** and then the question to be added.

### Removing and adding survey questions by role

Select **Select questions** from the *Question Reporting Access* section.
Remove a question by selecting the **X** next to the question. 
Add a question back by selecting **Add More** and then the question to be added.

#### Can the key outcome be changed?

The key outcome is added to all roles by default and can't be removed. If changed, the previous key outcome should remain as previously set. You see this message:  
> To change the visibility of reporting results related to the previous key question, go to your question level permission setting, and remove the question manually. This will ensure that the results are no longer visible to all roles. The new key outcome will be added to all roles." 

**Accept** or **Cancel** this change and then add the new key outcome to all roles. 

If necessary, admins must remove the previous key outcome from the roles that have permission to it.

## Set up reporting for this program
There are six fields to set up.

### Aggregate Indices

For most surveys, using aggregate indices is not recommended. Aggregates are groups of questions that are similar. For surveys with a large number of items, however, it can make sense to group similar questions into aggregates. Typically, aggregates are statistically validated constructs which contain highly correlated questions. Only rating-type questions can be a part of aggregate indices.

If adding an Aggregate Index:

1. Select **+ Add Aggregate Index** to open the *Create Aggregate* slider window.
2. In the new window, enter an aggregate name of your choosing. 
3. For **Calculation Method**, choose from:
   - Select **Average** - Recommended. Select from all rating questions. Qverage score = (a+b+...+n)/n, with the range from 0 to 100.  
   - Select **eNPS (employee Net Promoter Score)** - Select only one calculated 11-scale rating question. eNPS = (number of promoters - number of detractors) / (number of respondents) x 100, with the range from -100 to 100.
     
   >[!CAUTION]
   >If you change the calculation method, you'll need to reselect at least one question.

   > [!NOTE]
   > Viva People Science doesn't recommend the use of an employee Net Promoter Score<sup>TM</sup> due to its calculation method and inability to act as the best predictor of employee engagement.
   
5. In the **Add Questions** dropdown menu, search and select items to be grouped together. Your questions now appear in the *Selected Questions*. 
6. Select the **Include in Driver Impact Report** checkbox to see this aggregate in the Driver Impact Report.
7. Select **Save and Add to Program**.
8. Select **X** to close the slider window.

:::image type="content" source="../../media/glint/program-summary-reporting-create-aggregate.png" alt-text="Screenshot of the Create Aggregate slide window in Reporting setup.":::

>[!TIP]
> Use Viva Glint's 2-item Standard Engagement Index and no other aggregates. Viva Glint has strong benchmarks on this measurement, which provide insightful focus areas in results reporting.

>[!NOTE]
> When Glint's 2-item index is used, we recommend using it on every survey to ensure the capture of trends to accumulate benchmark data.

### Key Outcome

Select the desired **Key Outcome** from the dropdown menu. The key outcome is the main result of the survey. It can be the score from a single question or an aggregate index. This score appears as the most prominent score displayed in most reports.

:::image type="content" source="../../media/glint/program-summary-reporting-key-outcome.png" alt-text="Screenshot of the Key Outcome dropdown menu in Reporting setup.":::

> [!NOTE]
> Changes to key outcome will be displayed immediately upon saving.

### Driver Impact Outcomes

Select the **Driver Impact Outcomes** from the search field. Select a set of outcome questions or aggregates to be used for driver impact analysis. This analysis calculates the impact of each question or aggregate on the selected outcome and shows it on a chart.

:::image type="content" source="../../media/glint/program-summary-reporting-driver-impact.png" alt-text="Screenshot of the Driver Impact Outcomes section in Reporting setup.":::

### Manager Report Defaults

Select the desired **Manager Report Defaults**. Select up to two questions to appear by default in the manager report.

:::image type="content" source="../../media/glint/program-summary-reporting-manager-defaults.png" alt-text="Screenshot of an example of survey items that appear on a  manager's dashboard.":::

### PowerPoint Export Template

Select your desired **PowerPoint Export** template. The Viva Glint ACT guide is the default export.

:::image type="content" source="../../media/glint/program-summary-reporting-export-template.png" alt-text="Screenshot of the template choices for exporting a reporting PowerPoint.":::

### Broader Team Insights Export Template 

Select the desired **Broader Team Insights PowerPoint Export** template.

:::image type="content" source="../../media/glint/program-summary-reporting-bti.png" alt-text="Screenshot of the template choices for exporting a Broader Team Insight report.":::

**To complete this page, select the right-facing arrow to **Save & Continue**.**

### Next step

> [!div class="nextstepaction"]
> [Move onto Communications setup in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231342)



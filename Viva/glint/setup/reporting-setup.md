---
title: Reporting setup in Program Summary of Viva Glint
description: On the Reports page, admins customize how dashboards are set up and what reports specific roles can view. 
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
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/18/2024
---

# Reporting setup in Program Summary

The Reporting page allows admins to customize how dashboards are set up for specific User Roles to view their survey results.

:::image type="content" source="../../media/glint/setup/program-summary-reporting-2.png" alt-text="Screenshot that shows how to access Reporting in Program Summary." lightbox="../../media/glint/setup/program-summary-reporting-2.png":::

## Assign permissions to view feedback

In the **Program Roles** section, see and set how [User Roles](/viva/glint/setup/set-up-user-roles) are permissioned. **Select the role** to view what is configured. 

In this example, you see what the Company Admin is permissioned for:

:::image type="content" source="../../media/glint/setup/report-permissions.png" alt-text="Screenshot of report permissions in Program Roles." lightbox="../../media/glint/setup/report-permissions.png":::

As an admin, make these choices:

|Permission|Description|
|-------------|---------------|
|**Reporting view**| Whether the manager is granted [Live View or Phased access](/viva/glint/setup/live-versus-phased-access)|
|**Concierge Visibility**|Whether the manager sees the [Manager Concierge](/viva/glint/reports/manager-concierge-dashboard) feature on their dashboard|
|**Broader Team Insights**|Whether a high-level summary of this role's survey results is visible to their direct reports or roll-up hierarchy. [Learn about Broader Team Insights](/viva/glint/reports/broader-team-insights)
|**Team Conversations**|Managers with this feature enabled and who have a sufficient number of responses can access a [Team Conversations presentation kit](/viva/glint/reports/managers-sharing-team-conversations) once the survey closes and results are released.| 
|**Default Dashboard**|[Team Summary](/viva/glint/reports/managers-use-team-summary-dashboard ) is the default Glint manager dashboard experience. Change by using the dropdown menu to select a different report. Only one report is available when not using Team Summary.<br><br> **Important:** Company Admin roles must be granted access to the [Executive Summary dashboard](/viva/glint/reports/executive-summary-report).   
|**Export Comments**|The default **ON** setting allow managers to export verbatim comments exports using the **Export and Share** button in reports.<br><br> **Note:  To increase survey confidentiality,** you can disable the export functionality for comments at the program level. Disabling the feature enhances confidentiality measures by decreasing the chance that a user can match a specific comment to a survey respondent. When the default ON toggle is changed to **OFF**, the **Export and Share** button is hidden in reports.<br><br> :::image type="content" source="../../media/glint/setup/disable-comment-export.png" alt-text="Screenshot of the button option which isn't available when exporting comments is disabled.":::|
|**Report Template Access**|The individual reports this user can view. Select the **X** to delete a report or use the Search box to add a report. [Learn about Viva Glint reports](/viva/glint/reports/survey-reports-overview).

## Add User Roles to view feedback 

To add User Roles to a program to view feedback, select **Add Role**. The dropdown menu displays User Roles created within the [User Role feature](/viva/glint/setup/set-up-user-roles)). Select roles that should have reporting permissions for this program. The User Role name now appears on its own row.

:::image type="content" source="../../media/glint/setup/reporting-add-role.png" alt-text="Screenshot for adding a role for report viewing." lightbox="../../media/glint/setup/reporting-add-role.png":::

>[!TIP]
>Use the up or down arrow next to the role name to view or close role set up.

:::image type="content" source="../../media/glint/program-summary-reporting-add-role.png" alt-text="Screenshot that shows which features are permissioned for specific User Roles and the Add Role button." lightbox="../../media/glint/program-summary-reporting-add-role.png":::

### Set up Question Reporting Access

Selected questions can be excluded from a survey for specific roles. This example shows the Question Reporting Access permission for the Glint 360 admin role and that three of the 19 survey items are to be excluded for the People at vgAcme role:

:::image type="content" source="../../media/glint/setup/reporting-question-filter-roles.png" alt-text="Screenshot for excluding questions for a survey role." lightbox="../../media/glint/setup/reporting-question-filter-roles.png":::

Select **Select questions** from the **Question Reporting Access** section.
Remove an item by selecting the **X** next to it. 
Add an item back by selecting **Add More** and then select the item to be added.

## Set up reporting 

There are six fields to set up.

### Aggregate Indices

For most surveys, using aggregate indices isn't recommended. Aggregates are groups of items that are similar. For surveys with a large number of items, however, it can make sense to group similar questions into aggregates. Typically, aggregates are statistically validated constructs which contain highly correlated questions. Only rating-type questions can be part of aggregate indices.

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
   
4. In the **Add Questions** dropdown menu, select items to be grouped together. Your questions now appear in **Selected Questions**. 
5. Select the **Include in Driver Impact Report** checkbox to see this aggregate in the Driver Impact Report.
6. Select **Save and Add to Program**.
7. Select **X** to close the slider window.

   :::image type="content" source="../../media/glint/program-summary-reporting-create-aggregate.png" alt-text="Screenshot of the Create Aggregate slide window in Reporting setup." lightbox="../../media/glint/program-summary-reporting-create-aggregate.png":::

>[!TIP]
> Use Viva Glint's 2-item Standard Engagement Index and no other aggregates. Glint has strong benchmarks on this measurement, which provide insightful focus areas in results reporting.

>[!NOTE]
> When Glint's 2-item index is used, we recommend using it on every survey to ensure the capture of trends to accumulate benchmark data.

### Key Outcome

Select the desired **Key Outcome** from the dropdown menu. The key outcome is the main result of the survey. It can be the score from a single item or an aggregate index. This score appears as the most prominent score displayed in most reports.

:::image type="content" source="../../media/glint/program-summary-reporting-key-outcome.png" alt-text="Screenshot of the Key Outcome dropdown menu in Reporting setup." lightbox="../../media/glint/program-summary-reporting-key-outcome.png":::

> [!NOTE]
> Changes to key outcome are displayed immediately upon saving.

#### Can the key outcome be changed?

The key outcome is added to all roles by default and can't be removed. If changed, the previous key outcome should remain as previously set. You see this message:  

> "To change the visibility of reporting results related to the previous key question, go to your question level permission setting, and remove the question manually. This will ensure that the results are no longer visible to all roles. The new key outcome will be added to all roles." 

**Accept** or **Cancel** this change and then add the new key outcome to all roles. An admin must remove the previous key outcome from enabled roles.

### Driver Impact Outcomes

Select the **Driver Impact Outcomes** from the search field. Select a set of outcome items or aggregates to be used for driver impact analysis. This analysis calculates the impact of each item or aggregate on the selected outcome and shows it on a chart.

:::image type="content" source="../../media/glint/program-summary-reporting-driver-impact.png" alt-text="Screenshot of the Driver Impact Outcomes section in Reporting setup." lightbox="../../media/glint/program-summary-reporting-driver-impact.png":::

### Manager Report Defaults

Select the desired **Manager Report Defaults**. Select up to two items to appear by default in the manager report.

:::image type="content" source="../../media/glint/program-summary-reporting-manager-defaults.png" alt-text="Screenshot of an example of survey items that appear on a  manager's dashboard." lightbox="../../media/glint/program-summary-reporting-manager-defaults.png":::

### PowerPoint Export Template

Select the desired **PowerPoint Export** template. The [Glint ACT guide](https://go.microsoft.com/fwlink/?linkid=2286125) is the default export.

:::image type="content" source="../../media/glint/program-summary-reporting-export-template.png" alt-text="Screenshot of the template choices for exporting a reporting PowerPoint." lightbox="../../media/glint/program-summary-reporting-export-template.png":::

### Broader Team Insights Export Template 

Select the desired **Broader Team Insights PowerPoint Export** template.

:::image type="content" source="../../media/glint/program-summary-reporting-bti.png" alt-text="Screenshot of the template choices for exporting a Broader Team Insight report." lightbox="../../media/glint/program-summary-reporting-bti.png":::

To complete this page, select **Save & Continue**.

### Next step

> [!div class="nextstepaction"]
> [Move onto Communications setup in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231342)



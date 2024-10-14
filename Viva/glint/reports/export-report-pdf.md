---
title: Export reports as a PDF
description: Viva Glint users need to export their survey results to share with offline users, read verbatim comments, or to create presentations for their teams. Exporting reports as a PDF in Glint is quick, allows easy consumption of comments.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: alerts, comments, driver impact, executive summary, goals overview, heat map, disable comments, disable comments export, comments export, verbatim comments export, overall results, manager report, response rate, team summary, report access level, add report sections, delete report sections, prescriptive comments, representative comments
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/19/2024
---

# Export reports as a PDF

Microsoft Viva Glint users need to export their survey results to share with offline users, read verbatim comments, or to create presentations for their teams. Exporting reports as a Portable Document Format (PDF) in Glint is quick, allows easy consumption of comments, and supports highlighting, markup, search, and preview functionality. This export technology includes PDF exports for 360 feedback program reports and Focus Area reports.

In 360 feedback reports, the PDF export experience is a valuable and primary way for reports to be shared with external coaches. Glint 360 feedback PDF reports are generated to be consumable, shareable, and easy to use for collaborating on next steps.

## Procedure to export a PDF report

1. In the **Reports** tab, choose the survey and then the report to export. You can also navigate to **Saved Reports.**  For the example in this guidance, *Overall Results* is the report to be exported as a PDF.

   :::image type="content" source="../../media/glint/reports/export-overall-results.png" alt-text="Screenshot of the Overall Results report access card in Reports." lightbox="../../media/glint/reports/export-overall-results.png":::

2. As needed, filter within the report to export other cycles by selecting the **Add a filter option**. Select the cycle to export. Then **Close Filters.**

   In this example, the cycle is changed from July 2020 (the current cycle) to April 2020.

   :::image type="content" source="../../media/glint/reports/export-change-cycle.png" alt-text="Screenshot of the dropdown menu to change cycles in a program.":::

3. Closing the filters allows the report to be shown in its entirety. Now the **Export and Share** dropdown menu is available.

   :::image type="content" source="../../media/glint/reports/export-share-button.png" alt-text="Screenshot of the Export and Share button.":::

4. Select **Export Report to PDF**

   :::image type="content" source="../../media/glint/reports/export-share.png" alt-text="Screenshot of the Export and Share dropdown menu.":::

5.	A preview PDF opens in a new tab. You see this update while it’s generating:

    :::image type="content" source="../../media/glint/reports/export-generating.png" alt-text="Screenshot of the Generating Report popup which displays while a PDF generates.":::

6.	Now, choose **Export or Print** to open a new dialogue box displaying report choices.

    >[!NOTE]
    > This choice brings up the appropriate dialog box for the browser you are using. Choose whether to **Save as a PDF** or to **Print** the file. Report enhancements may include printing, searching, and highlighting if your PDF tool permits. Any filters applied display

    :::image type="content" source="../../media/glint/reports/export-print.png" alt-text="Screenshot of the Export or Print button.":::

## Remove a report section before export

Default toggles are **ON** for each of these sections of the Overview report (the example report used): Overview, Questions, Keywords, Topics, Comments.
To disable a section:

1.	Select the **ellipses** in that section.
2.	Select **Remove.**

    In this example, we're removing the Overview section of the Comments report:

    :::image type="content" source="../../media/glint/reports/export-file-save-pdf.png" alt-text="Screenshot of the option to Save to PDF in your printing window." lightbox="../../media/glint/reports/export-file-save-pdf.png":::

## Export the Comments report

1.	Select the **More** button.
2.	If the Comments report (or any specific report) isn't part of your current reporting view, from the dropdown menu, choose **+ Add section.**

    :::image type="content" source="../../media/glint/reports/export-remove-section.png" alt-text="Screenshot of the Remove section button in Reports.":::

3.	Choose **All Comments** or whichever reporting section you choose to add. An onscreen banner notifies you that the section is added.
4.	Choose whether you want to include all verbatim comments in your PDF download. Choose either:
    - **Prescriptive comments** 
      - Content: These comments provide specific advice or instructions on how to improve or address a particular issue.
      - Purpose: They aim to guide actions and suggest concrete steps for improvement.
    - **Representative comments** 
      -  Content: These comments reflect the views, opinions, or experiences of a larger group. In short - common themes.
      -  Purpose: They aim to illustrate common sentiments or trends among the respondents
5. The **Translation** option is available here for you to use. [Follow guidance for language translations](/viva/glint/setup/language-translations).

   :::image type="content" source="../../media/glint/reports/export-comments.png" alt-text="Screenshot of the Translate button in Comments exporting." 

   >[!NOTE]
   > When this window is closed, the default settings reset for the next use.

## Comments report export control 

This feature gives administrative control to hide the export functionality for comments at the program level. With this feature enabled, users can't generate or export the comments section of a feedback report for any cycle of this program.

The feature enhances confidentiality measures within your organization. It decreases the risk posed by malicious actors who may attempt to de-anonymize survey data. It limits their ability to  match a specific comment with a survey respondent.

### Enabling Comments report export

For comments report generation and export enablement, this process is set up:

From the admin dashboard: **Configuration** symbol > **Survey Programs** > **Select Survey Program** > **Program Setup** > **Reporting** > **Role**
- The toggle reads **ON,** which is the default setting.
- A user can generate and export the Comments report.

### Disabling Comments report export 

If the default ON toggle is changed to **OFF**, the option to Export and Share is hidden. The button doesn't appear.

:::image type="content" source="../../media/glint/reports/disable-comment-export.png" alt-text="Screenshot of the button option which isn't available when exporting comments is disabled.":::




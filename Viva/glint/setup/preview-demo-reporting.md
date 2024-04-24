---
title: Preview pre-launch demo data in Viva Glint reporting
description: For training purposes, admins can use demo data to learn what reporting will look like when a survey is closed and actual reporting is released.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva glint data reports, survey programs, preview demo reports, question targeting, reporting preview window
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/16/2024
---

# Preview pre-launch demo data in Viva Glint reporting

How do your employee attributes and potential survey responses look in Microsoft Viva Glint reporting? Previewing demo data enables admins to familiarize themselves with the Viva Glint dashboard. Previewing reporting also enables an understanding of how data file attributes appear in reporting scenarios. 

Demo surveys are available for engagement surveys only.

>[!IMPORTANT]
>Demo dashboards last for seven days only. Regenerate it to see it after seven days.

>[!CAUTION]
> Demo preview generation is limited to 3 times/day/program/user. Report generation requests queue up in the order that they’re requested across all surveys and users.

## Previewing demo data reports

>[!IMPORTANT]
> To ensure no unintended notifications are sent, Nudges or Team Conversations must be temporarily disabled before proceeding.

1. From the Viva Glint admin dashboard, select the **Configuration symbol** and then **Survey Programs.**

   :::image type="content" source="../../media/glint/setup/configuration-symbol.png" alt-text="Screenshot of the configuration symbol on the admin dashboard.":::
   
2. Select the survey in which to preview reporting. A new page opens.

3. In the *Upcoming and Live* tab, select **Preview** from the vertical ellipses dropdown menu. A *Survey Preview* dialog box opens.

   :::image type="content" source="../../media/glint/setup/preview-dropdown.png" alt-text="Screenshot of the preview dropdown menu within the ellipses next to a survey cycle.":::
 
4. Select **Generate Report Preview** to view a one-time, randomized data survey report. An email lets you know when the report is available; the report may take up to 24 hours to generate. Once generated, your report remains visible for seven days.
   
   :::image type="content" source="../../media/glint/setup/generate-report-preview.png" alt-text="Screenshot of the *Survey Preview for Engagement* dialog box from which to select **Generate Report Preview**.":::

   :::image type="content" source="../../media/glint/setup/report-preview-generated.png" alt-text="Screenshot of the *Report Preview Generated* dialog box.":::

>[!NOTE]
> Until you receive your email, ensure that your survey program remains in an **Approved** status. Your report will not generate successfully if your survey program is not **Approved**.

>[!TIP]
>To make changes to your survey once you have previewed how the reporting will appear, select **Edit** from the vertical ellipses next to the program.

## Can I generate a new demo data report preview after editing a survey?

To *replace* a generated report, preview with newly uploaded employee attributes. , a dialog box tells you that a report preview was previously generated. To replace this demo report with a new version, select **Generate Report Preview**. The seven-day report visibility starts over with the generation of the new report.

## How long does a preview take to generate?

Generally, preview reports for surveys with ~25 questions and <5Kk employees generate almost immediately.
Surveys with ~15 questions and > 200K employees may take as long as 3.5 hours to generate.

## How do I see my demo report?

**From your Viva Glint dashboard:**

1. Select **Reports.**
2. Choose **Demo Data for Engagement**.
3. Select the report to review.

:::image type="content" source="../../media/glint/setup/demo-data-for-engagement.png" alt-text="Screenshot of the *Reports* tab and Demo Data for Engagement.":::

:::image type="content" source="../../media/glint/setup/demo-data-expiration.png" alt-text="Screenshot of a demo data report with the expiration date posted at the top.":::

**Your demo report is also viewable from the program listing on your admin dashboard.** It shows in the list of your programs with the name of the program preceeded by "Demo Data." To leave that program - and remove the demo banner from the top of your screen - use **Switch Program.**

:::image type="content" source="../../media/glint/setup/switch-programs.png" alt-text="Screenshot of how the Demo Data for Engagement program shows on the admin dashboard.":::

## What does demo data reporting include?

Commonly asked questions about demo data dashboards:

### Is preview reporting generated for a survey with question targeting?

Demo data can't be generated for surveys with question targeting or excluded Distribution Lists. To generate a preview from a survey with targeting:
- Deselect the targeted item from the cycle/program, or
- Temporarily remove targeting from the item while the preview generates

### Does the demo preview show Strengths and Opportunities? 

No. Demo data previews rely on fake response data with little variation in scores that doesn’t produce Strengths and Opportunities. 

As a potential workaround, an Admin can filter to a manager team with at least ~20-30 respondents to view a cut of data with more score variance than the company-wide data, but it's trial and error.

### Does the demo preview use items selected for the upcoming cycle or all items that exist at the program level? 

The preview uses all items that are part of the next scheduled survey cycle.

## Should I create Focus Areas from demo preview dashboards? 

Don't create fake focus areas as they then show with other real Focus Areas. If you do create them as a training exercise, delete them afterward.

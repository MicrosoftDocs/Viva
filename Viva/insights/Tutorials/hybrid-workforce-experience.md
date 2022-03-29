---
ROBOTS: NOINDEX, NOFOLLOW
title: Hybrid workforce experience report
description: Learn how to understand how hybrid work affects employees differently through the Hybrid workforce experience Power BI report
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: helayne
audience: Admin
---

# Hybrid workforce experience report

## Introduction

As leaders figure out their organization’s new working models, the Hybrid workforce experience Power BI dashboard report helps them understand how hybrid work affects employees differently. The report identifies opportunities to improve the experience of employees working mostly onsite and mostly remote, as well as those working onsite some days of the week and remote on others.

This report has six sections, which each address different facets of the employee experience that new hybrid working models may impact. Key metrics provide a deep-dive into each topic, along with a **Why it matters** interpretation and **recommended actions**.  

## Prerequisites

Before you can run queries and populate the dashboard in Power BI, make sure you:

* Are assigned the role of [Analyst](/viva/insights/use/user-roles) in Workplace Analytics with Viva Insights.

* Have installed the latest version of Power BI Desktop.
    * If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then, download and install the latest version from [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab).

* Have the following uploaded as part of your organizational data:
     * An attribute identifying the number of days someone works onsite (for example, OnsiteDays)

     * An attribute indicating whether someone is a manager (for example, SupervisorIndicator)

     * An attribute indicating the person’s hire date (for example, HireDate), which is required to be able to load the **New hire onboarding insights**. Without this attribute, the rest of the report will still load, however.

## Set up the template

>[!NOTE]
> This dashboard is currently only available in English and only works with data generated from the English version of Workplace Analytics. Before completing the following steps, confirm that the browser language contains **en-us** in the app's URL, or change it to read: `https://workplaceanalytics.office.com/en-us/Home`.

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Query designer**.
2. In **Create** > **Other templates**, select **Hybrid workforce experience**, which takes you to required setup steps.

    In the second setup step, select **Set up** next to **Hybrid workforce experience** (if repeating this process per step 8 below, select **Strong and diverse ties**).
3. When prompted, select or confirm the options for **Group by**, **Time period**, and **Meeting exclusions**.
4. In **Select metrics**, keep the preselected metrics (these are required for the template to work).
5. In **Select filters**, select **Active only** for **Which measured employees do you want to include in your query results**? Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, refer to [Create a Person Query](/viva/insights/Tutorials/person-queries).
6. In **Organizational data**, add the attribute that specifies someone’s number of onsite work days (for example, **OnsiteDays**), the attribute that indicates whether someone is a manager (for example, **SupervisorIndicator**), and the HireDate. Add any other attributes you want to be able to use in the report. For best performance, stick between five and eight attributes.
7. Select **Run** (located in the upper right) to run the query, which can take between a few minutes and a few hours to complete.
8. When prompted, select to return to the **Query designer**. Repeat preceding steps 2-7, except this time, select the **Strong and diverse ties** query. Make the same selections that you did for the Hybrid workforce experience. There’s no need to include any organizational attributes in this query.
9. When prompted, select to go to **Results**. After both queries successfully run, navigate to **Query designer > Results**. Select the download icon for the **Hybrid workforce experience** query results, select **PBI template**, and then select **OK** to download the template.
10. Open the downloaded **Hybrid workforce experience** template.
11. If prompted to select a program, select **Power BI**.
12. When prompted by Power BI:
    1. In the Workplace Analytics **Query designer > Results**, select the link icon for each query, and select to copy the generated OData URL link.
    1. In Power BI, paste each copied link into its respective URL field.
    1. Map the attribute in your organizational data that specifies someone’s onsite work days (for example, **OnsiteDays**).
    1. Map the attribute that identifies whether someone is a manager (for example, **SupervisorIndicator**).
    1. Map the **HireDate** attribute (if available).
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    1. Select **Load** to import the query results into Power BI. Loading these large files might take between a few minutes and a few hours to complete.
    :::image type="complex" source="../images/wpa/tutorials/hwfe-edit-parameters.png" alt-text="Screenshot of Edit Parameters window in Power BI":::
       Screenshot that shows the "Edit Parameters" window within Power BI. Each part of the image is labeled with the sub-step above to which it corresponds, "b" - "f". The first two sections, "Hybrid work person query file path" and "Hybrid work person-to-person query file path," are highlighted and labeled "b." Beneath each section header is an editable field that contains a file path to a .csv file; the first field, for the Person query, contains a path to a HybridWorkforceExp.csv file and the second field, for the Person-to-person query, contains a path to a StrongAndDiverseTies.csv file. The next field is titled, "Number of onsite days," has a "c" label to its right, and its editable field contains the text, "OnsiteDays." The next field is titled, "SupervisorIndicator," has a "d" label to its right, and its editable field contains the text, "SupervisorIndicator." The second-to-last field is titled, "Hire date," has an "e" label to its right, and its editable field contains the text, "HireDate." The last field is titled, "Minimum group size," has an "f" label to its right, and its editable field contains "5" selected from a dropdown menu.  
    :::image-end:::

1. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. At this point, you’ve completed the setup process and can skip to [Customize the report](#customize-the-report).
1. If you're not signed into Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](/viva/insights/Tutorials/power-bi-templates#troubleshooting) for more details.
1. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

    >[!IMPORTANT]
    > You must sign in to Power BI with the same account you use to access Workplace Analytics.

16. Select **Connect** to prepare and load the data, which can take a few minutes to complete. After the data loads, charts appear in Power BI with insights about the hybrid workforce’s experience.

## Customize the report

After the **Workforce experience** report is set up and populated with Workplace Analytics data in Power BI, you’re prompted to map the following attribute values:

* **Mostly onsite** –  Select the number of onsite days that define the work mode of employees that work mostly onsite (that is, from the company’s main worksite).
* **Hybrid** – Select the number of onsite days that define the work mode of employees that work onsite some days during the week and remote on others.
* **Mostly remote** – Select the number of onsite days that define the work mode of employees that work mostly remote (that is, from home or some other location outside the company’s main worksite).
* **Individual contributor** – Select the attribute values that identify employees as individual contributors who do not manage people within your organization.
* **Manager indicator** – Select the attribute values that identify managers who manage people within your organization, like **Mgr** and **Mgr+**.

    :::image type="complex" source="../images/wpa/tutorials/hwfe-a-couple-of-questions.png" alt-text="Screenshot of pop-up window in Power BI prompting users to assign onsite days to attributes and values to Individual contributors and Managers":::
       Screenshot that shows a pop-up window in Power BI, titled "A couple of questions to get you started..." There are two sections; the first section is titled, "Select which of your onsite days values best map to the following 'work mode' definitions" and the second section is titled "Select which values identify individual contributors, managers and managers of managers," which is parenthetically defined as "Manager" with a plus icon--"Manager-plus." In the first section, there are three fields, and each contain a dropdown menu to their right: "Mostly onsite," which shows "5" in the dropdown menu, "Hybrid," which shows "1,2,3,4" in the dropdown menu, and "Mostly remote," which shows "0" in the dropdown menu. In the second section, there are two fields, and each also contain a dropdown menu to their right: "Individual contributors," which shows "IC" in the dropdown menu, and "Managers," which shows "Multiple selections" in the dropdown menu.
    :::image-end:::

After this initial prompt, you can then select **Settings** in the upper right of any page to view and change the following attribute values:

* **Time period** – Select the time period you want to view data for in the dashboard.
* **Exclusions** – Select the weeks you want to exclude for everyone in the analysis population, such as holiday weeks where everyone is away from work.
* **Organizational** attribute to view the report by – Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.
* **Employee filter** – Select the organizational attribute and values by which you want to filter the employees in the reports.

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, refer to [Power BI tips, FAQ, and troubleshooting](/viva/insights/Tutorials/power-bi-templates).

## Related topic

[View, download, and export query results](/viva/insights/use/view-download-and-export-query-results)
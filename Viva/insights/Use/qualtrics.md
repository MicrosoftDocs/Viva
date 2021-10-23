---
ROBOTS: NOINDEX,NOFOLLOW
title: Viva Insights and Qualtrics integration
description: Learn how to integrate Microsoft Viva Insights and Qualtrics Prism Analytics data for more advanced analysis
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Viva Insights and Qualtrics integration

*This experience is only available through private preview at this time*

The Microsoft Viva Insights and Qualtrics integration combines employee collaboration data from Viva Insights with employee engagement data in Qualtrics.

This integration enables you to combine Viva Insights query data and Qualtrics Employee Experience data. You can then identify behaviors and patterns behind key metrics, such as engagement, prioritization, manager effectiveness, and wellbeing.

For example, the following shows how you can configure the widgets on your dashboard in Qualtrics to include after-hours collaboration data from Viva Insights as breakouts. Your HR and leadership teams can see how after-hours work affects employee engagement and manager effectiveness. They can then use this analysis to take action.

![Qualtrics example data.](../images/wpa/use/qualtrics-example.png)

Also, in Qualtrics, you can include Viva Insights metrics as filters at the top of the dashboard to filter the entire page:

![Qualtrics dashboard metrics example.](../images/wpa/use/qualtrics-example-2.png)

## Setup steps

The following tasks are required to set up this integration.

1. Confirm or complete the [Prerequisites](#prerequisites)
2. [Prepare and upload Qualtrics data](#prepare-and-upload-qualtrics-data)
3. [Set up a Viva Insights query](#query-setup)
4. [Upload the query data to Qualtrics](#upload-to-qualtrics)

## Prerequisites

Before using the Viva Insights Query Designer, you must confirm or complete the following prerequisites:

* Confirm that [Viva Insights in Workplace Analytics is set up](../setup/set-up-workplace-analytics.md) and ready to use.
* Confirm that your analysis population is assigned Viva Insights or Workplace Analytics licenses
* Confirm you have a Viva Insights or Workplace Analytics admin assigned to upload appended organizational (HR) data and a Viva Insights analyst assigned to set up the query data.

## Prepare and Upload Qualtrics data

Before your analysts can create a query in Viva Insights for use in Qualtrics, Viva Insights requires data from Qualtrics.

1. A Qualtrics data manager with the necessary credentials must complete the steps in the following Qualtrics Employee Experience documentation:

   * [Exporting Response Data](https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/data/download-data/export-data-overview/) to export (download) participant responses to your survey questions.
   * [Categories (EX)](https://www.qualtrics.com/support/employee-experience/creating-ee-project/dashboards-tab/dashboard-management/dashboard-settings/categories-ee/) to create, manage, and assign categories for aggregate reporting.
2. Give the newly saved .csv file to the Viva Insights or Workplace Analytics admin. 
3. As the admin, confirm the file has the following attributes in addition to the organizational files required by Viva Insights:

   * **PersonId** - Email address or alias of the person in the survey file
   * **EffectiveDate** - Beginning of the time period reflected in the survey

      * For example, if it’s a quarterly survey that closed on March 30, then the preceding quarter would be the survey time frame of January 1st for the effective date.

   * **Engagement** - Score for survey category one
   * **Motivation** - Score for survey category two
   * **Wellbeing** - Score for survey category three

4. Follow the steps in [Subsequent uploads](../setup/upload-organizational-data.md#file-upload) and select to **Append the existing organizational data** in **Step 7** and **Add attributes** in **Step 7** to add the new Qualtrics (.csv) data into Viva Insights in Workplace Analytics. 
5. When prompted to map the custom fields in Workplace Analytics, for **Engagement**, **Motivation**, and **Wellbeing**, enter the same field names in the **Workplace Analytics attribute** column, and select **Show in report** in the **Report options** column.

## Query setup

After the upload is successfully processed in Viva Insights in Workplace Analytics, a Viva Insights or Workplace Analytics analyst can do the following to set up the query data.

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Query designer**, and then select **Get started** under **Query**.
2. Select **Person query** > **Behavior Patterns for Qualtrics and Workday** to see the required setup steps, and then in step 2, select **Set up**.
3. When prompted, select or confirm the following settings:

   * **Name** - Customize or keep the default name
   * **Group by** – Week
   * **Time period** - Last 1 year
   * **Auto-refresh** - Enable the setting
   * **Meeting exclusions** - Select the preferred rule for your tenant

4. In the **Select metrics** section, keep all the predefined metrics, including:

   * For Wellbeing in Qualtrics - **After hours collaboration** and **Focus hours**
   * For Engagement in Qualtrics - **Manager 1-1 hours**, **Skip level meeting hours**, and **Internal network size**
   * For Prioritization in Qualtrics - **Manager 1-1 hours**

   >[!Important]
   >If you delete a preselected or predefined metric, it will limit your ability to use the query data in Qualtrics.

5. In **Select filters**, select **Active only** for "**Which measured employees do you want to include?**" and then, optionally, you can further filter for the population of interest. For more details about filter and metric options, see [Create a Person Query](../tutorials/person-queries.md).
6. In **Organizational data**, keep the preselected **Organization** and **LevelDesignation** attributes and up to three more that match up with the attributes included in your Qualtrics data.
7. Select **Run** to run the query, which can take a few minutes up to a few hours to complete.
8. When prompted, select to go to **Results**. After the results successfully run, select the **Download** icon for the **Behavior Patterns for Qualtrics and Workday** query results, and then select **OK** to download the query.

## Upload to Qualtrics

As the Qualtrics data manager, do the following to import the Viva Insights query data into Qualtrics Employee Experience.

1. Open the query results .csv file that you downloaded and confirm the file conforms to Qualtrics requirements for the import, which you will import as person metadata. Instead of including raw query data, you'll need to update the Viva Insights metrics into deciles, percentiles, or ranges (such as **Very Low** to **Very High**).

   >[!Note]
   >An upload can have a maximum of 200 columns of person metadata. If you upload metrics after the survey collection, you must sync the metadata with your responses to allow the new metadata to appear in the responses.

2. Follow the instructions in [Creating and Uploading Your Participant File](https://www.qualtrics.com/support/employee-experience/getting-started-employee-experience/employee-engagement-onboarding/step-3-configuring-project-participants-distributing-project/#CreatingUploadingParticipants) (Qualtrics documentation) to import the Viva Insights data into Qualtrics Employee Experience.
3. You can then use the uploaded data as filters in dashboards or breakouts in Qualtrics widgets.

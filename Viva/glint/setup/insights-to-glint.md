---
title: Send Viva Insights data to Viva Glint (preview)
description: Viva Glint admins can import behavioral data from Viva Insights to supplement their Glint survey data for a better understanding of how your organization’s way of working impacts the employee experience.
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
ms.date: 08/28/2024
---

# Send Viva Insights data into Viva Glint (preview)

>[!IMPORTANT]
>This feature is currently availabile to preview customers only. Features described here are subject to change.

Glint admins can import behavioral data from Microsoft Viva Insights to supplement their Microsoft Viva Glint survey data for a better understanding of how your organization’s way of working impacts the employee experience.

-	Explore employee sentiment relative to behaviors
-	Filter employee sentiment by ways of working
-	Control who can access Viva Insights data

To use this integration:
-	Your organization purchased a Viva Insights tenant
-	Your organization purchased Premium Viva Insights licenses

Select **Learn more** in the platform to get more information about the integration.

:::image type="content" source="../../media/glint/setup/glintsights-learn-more.png" alt-text="Screenshot of the banner announcing the new Viva Glint and Viva Insights integration.":::

## Manage data sharing 

On your first visit to the Viva Insights Integrations platform, accessible from your admin configuration dashboard, you see a window requesting you to review and agree to this information:

- Data sharing from Viva Insights to Viva Glint is a feature governed by the Microsoft Viva Preview Agreement. 
-	When Insights-to-Glint data sharing is enabled, Insights advanced insights metrics is shared with Glint and subject to further processing by Glint. Glint stores a copy of the share Insights data, which can be deleted from Glint at any time.
-	By selecting the checkbox, you enable Insights-to-Glint data sharing and agree to the Microsoft viva preview Agreement.

## Set up the Viva Insights integration 

1.	From your Glint admin dashboard, select the **Configuration** symbol and then **Viva Insights** from the **Microsoft Viva Integrations** section.

    :::image type="content" source="../../media/glint/setup/glintsights-integration-new.png" alt-text="Screenshot of the card to access the Viva Glint and Viva Insights integration from the admin dashboard.":::

2.	Select the **Set up integration** button in the **Import Viva Insights** data section.
3.	Review the window that pops up and then select **Get Started.**

    :::image type="content" source="../../media/glint/setup/import-insights-popup-window.png" alt-text="Screenshot of the Get Started importing Viva Insights data into Glint window.":::

## Add behavioral attributes from Viva Insights

There are two steps to this process.

### Step 1

In Step 1 of 2, decide which behavioral attributes to import into Glint. Attributes are numerically split into four different ranges, defined by Glint. Ranges can be customized after setup. Glint will also respect Viva Insights confidentiality thresholds on Glint reports and dashboards.

1.	Select **Add** next to an attribute to continue. You must select at least one attribute to continue.

    :::image type="content" source="../../media/glint/setup/glintsights-add-attribute.png" alt-text="Screenshot of the Add behavioral attributes from Viva Insights window.":::

2.	In the window that opens, select at least one **role** to add to this attribute. Roles are prepopulated from your User Roles configured earlier.

3.	In the **role row**, select if that role should have access to information about this attribute in their **report filters**, **report sections**, or **comment filters**. Roles without these permissions are greyed out and unavailable to select.

    :::image type="content" source="../../media/glint/setup/glintsights-add-slidey.png" alt-text="Screenshot of the Select roles for this attribute window.":::

4.	Select **Save**. This attribute now shows as **Added**.

    :::image type="content" source="../../media/glint/setup/glintsights-added.png" alt-text="Screenshot of the Added confirmation.":::

5.	Continue adding attributes until you have everything you need. 
6.	**Select Programs.**

      :::image type="content" source="../../media/glint/setup/glintsights-select-programs.png" alt-text="Screenshot of the Select Programs button.":::

>[!IMPORTANT]
> Glint respects Viva Insights confidentiality thresholds on Glint reports and dashboards.

## Select Viva Insights metrics

Add a Viva Insights metric as an employee attribute. Assign roles for the attribute. In this example, **after-hours collaboration hours** are chosen as the Insight metric. 

:::image type="content" source="../../media/glint/setup/glintsights-add-metric.png" alt-text="Screenshot of how to add an Insight metric as an attribute.":::

### Make your metric selection from Insights

>[!NOTE]
>Default bucket values are determined by Viva People Science research experts.

|Default metric name |Default metric description| Bucket 1|Bucket 2| Bucket 3|Bucket 4|Unit|
|---------|---------|---------|----|-----|--------|--------|
|Email hours|Number of hours a person spent sending and receiving emails|0 to less than 3|3 to less than 6|6 to less than 8|8 or more|Hour|
|Call hours|Number of hours a person spent in scheduled and unscheduled Teams calls with at least one other person, during and outside of working hours|0 to less than 5|5 to less than 10|10 to less than 15|15 or more|Hour|
|After-hours collaboration hours|Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours|0 to less than 1|1 to less than 3|3 to less than 5|5 or more|Hour|
|Multitasking hours|Number of hours a person spent sending or reading emails or chats during a meeting or Teams call|0 to less than 1|1 to less than 3|3 to less than 5|5 or more|Hour|
|Collaboration hours|Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person. These hours are either internal or external. They are determined after deduplication of time due to overlapping activities. 
|Uninterrupted hours|Sum of block one hour or longer where a person didn't attend a meeting, read or send eamils, read or send Teams chcats, or initiate or receive Teams calls. In other words, uninterrupted hours is the sume of blocks of time, one hour or longer, for deep thinking with no communication. This metric helps organizations understand whether employees have long blocks of uninterrupted time for deep thinking to solve new problems creatively and to fuel innovation|0 to less than 5|5 to less than 10|10 to less than 15|15 or more|Hour|
|Meeting hours|Number of hours a person spent in meetings with at least one other person, during and outside of working hours.|0 to less than 6| 60 to less than 12|10 to less than 15|15 or more|Hour|
|Meeting hours with Manager 1:1|Number of meeting hours involving only the person and their manager|0 to less tha 0.01|0.01 to less than 0.25|0.25 to less than 0.5|0.5 or more|Hour|
|Meeting hours with Skip Level Manager|Number of meeting hours a person attended where their manager's manager also attended the meeting|0 to less than 0.01|0.01 to less than 0.5|0.5 to less than 1| 1 or more|Hour|
|Internal network size|Number of people within the organization with whom a person has had a reciprocal interaction in the past four weeks|0 to less than 15|15 to less than 30|30 to less than 45|45 or more|Count|

### Step 2

In the **Select Programs and Cycles** section, import data from previous cycles and set up automatic imports for future cycles. 

1.	To continue, use the boxes to display a checkmark to select a program. You may select multiple programs.
    1.	Each cycle pulls 12 weeks of Insights data, if available.
    1.	Glint currently supports importing the selected behavioral data for the last two cycles, up to 24 months.
2.	Select **Import behaviors**.

    :::image type="content" source="../../media/glint/setup/glintsights-import-behaviors.png" alt-text="Screenshot of the confirmation that behavioral attributes are added.":::

3. This confirmation shows:

   :::image type="content" source="../../media/glint/setup/glintsights-behaviors-added.png" alt-text="Screenshot of the Select behaviors button.":::

4. Select **Close.**

## Manage added data

Now you’re ready to manage your integration. After closing the confirmation window, the **Set up integration** button now reads **Manage Integration**. 

Select **Manage Integration**. The **Import Viva Insights data** page opens.

:::image type="content" source="../../media/glint/setup/glintsights-manage-insights-integration.png" alt-text="Screenshot of the Manage integration button.":::	

 ## Manage imported attributes

You can see the list of attributes imported. 

1.  To bring in other behaviors, select **+ Add attributes** and follow the same  procedure. Attributes continue to populate in the **Imported Attributes** column.

   :::image type="content" source="../../media/glint/setup/glintsights-manage-add-attributes.png" alt-text="Screenshot of the Import Viva Insights data window.":::	

2. Use the **ellipses** next to each behavior to open a dropdown menu, providing options for you to edit, customize, or delete.

   :::image type="content" source="../../media/glint/setup/glintsights-imported-attributes-dropdown.png" alt-text="Screenshot of the Imported Attributes dropdown menu.":::	

## Edit attributes

To add or delete attributes, check or uncheck any roles or filters. Select **Save**.

### Customize attribute ranges

To view numeric data in heatmaps, filters, and more, the data must be placed into ranges. Default ranges are defined by Glint, but you can configure your own range. 

All data ranges are the same across the entire company.

1.	Adjust the range in the **Max** column.
2.	Select **Save**.

:::image type="content" source="../../media/glint/setup/glintsights-customize-ranges.png" alt-text="Screenshot of the Customize Ranges window.":::

>[!IMPORTANT]
> Glint respects Viva Insights confidentiality thresholds, in addition to Glint’s threshold. Customizing default ranges may result in ranges with employees less than these thresholds and for this reason, results don’t appear in any reports or filters.

## Delete an imported attribute

By deleting an attribute, Glint deletes all previously imported attribute data, and this data is not included in future Glint program cycles. Changes may take a few hours to show on Glint reports. Select **Delete** in the window that opens.

:::image type="content" source="../../media/glint/setup/glintsights-delete-attribute.png" alt-text="Screenshot of a Delete Attribute window.":::

## Manage enabled survey programs

Switch to the **Enabled Programs** tab.

### Add programs 

Glint imports Insights data for previous and future cycles by selecting more programs, which are populated in the **Add Programs** window that opens. Each cycle imports 12 weeks of Insights data. Glint supports importing selected behavioral data for the past two cycles, up to 24 months.

Select the **+ Add Programs** button and then the **Add** button as desired. These programs are now added to the **Enabled Programs** column.

:::image type="content" source="../../media/glint/setup/glintsights-add-program.png" alt-text="Screenshot of the Add programs button.":::

### Remove programs

Use the ellipses next to each program to open the **Remove program** option.

:::image type="content" source="../../media/glint/setup/glintsights-remove-program.png" alt-text="Screenshot of removing a program window.":::

Select **Remove** from the window that opens.


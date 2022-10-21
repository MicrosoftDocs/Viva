---
title: Person query
description: Learn how to run a Custom Person query in the Microsoft Viva Insights advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Create a Custom Person query

>[!Tip]
> You can find a demo video, download sample results, and go through a **Show me how** explanation while you’re building your query. Select these options just above **Query setup**.
:::image type="content" source="../images/person-query-setup-help.png" alt-text="Setup help with link to video, sample, and walk-through above Query setup":::

Set up, select data for, and run your query by following the steps and guidance in this section.

### Query setup

In **Query setup**, you define some basic information about your query, like its name, the time period it will analyze, and whether it will refresh on its own.

#### To set up your query

1. From the [advanced insights app's](https://go.microsoft.com/fwlink/?linkid=2201482) **Analysis** page, navigate to **Custom queries > Person query** and select **Start analysis**.
    >[!Note]
    >If you're an existing Viva Insights customer, refer to the note in the [Introduction](../introduction-to-advanced-insights.md) for more information about using the new platform.

2. Under **Query setup**:

    1. Optional: Name your query. Queries are assigned a default name, which follows this format: Query type, user ID, date, and time. Make sure the name is unique.
    1. Optional: Select a **Time period**. This field defaults to **Last 3 months**, but you can select another time period you want your query to analyze. Pick from **Last 1 year**, **Last 6 months**, **Last 1 month**, or a **Custom** date range. If you choose a **Custom** date range, use the date picker to select the range.
    :::image type="content" source="../images/person-query-timeperiod.png" alt-text="Time period dropdown.":::
    :::image type="content" source="../images/person-query-timeperiod-datepicker.png" alt-text="Time period with date pickers highlighted.":::
    1. Optional: Set the query to automatically update by selecting the **Auto-Refresh** box. When you select the auto-refresh option, your query automatically runs and computes a new result every Viva Insights gets updated collaboration data for licensed people. This option is deselected by default, but you can select it on any query where the **Time period** isn’t customized.
        :::image type="content" source="../images/person-query-auto-refresh1.png" alt-text="Time period with Auto-Refresh highlighted.":::
    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.

    1. Optional: Set how the query is grouped. By default, custom Person queries are grouped by **Month**. To change this setting to **Week**, select **More Settings** beneath the **Description** box.
        :::image type="content" source="../images/more-settings.png" alt-text="Description box with More Settings button highlighted.":::
        Selecting **More Settings** brings you to the **More Settings** pane. Along with **Group by**, this pane shows the metric rules that apply to your query. To find out more about metric rules that apply to your query, select **See metric rule details**.
    >[!Note]
    > Metrics are criteria used to measure the productivity and wellbeing of employees, and metric rules are rules Viva Insights uses to improve the accuracy of your query results.
    >
    > To learn more about metrics used in Viva Insights, refer to [Metric definitions](../reference/metrics.md). To learn more about metric rules, refer to [Metric rules](./metric-rules.md).

### Metrics 

In **Select metrics for what you want to know about your employees**, you specify what you want to find out about the employees you’re analyzing, and also define the employees you’re including in your query.

#### About metrics

Metrics are criteria used to measure the productivity and wellbeing of employees. For example, if you’re wondering how much time employees spend collaborating after their working hours, you could use the **After-hours scheduled call hours** and **After-hours chat hours** metrics in your query.

##### Select metrics pane

###### Metric categories

In the **Select metrics** pane, metrics are grouped by *metric category*. Expand the categories to see which metrics they contain. Let’s say you were looking for the **After-hours scheduled call hours** and **After-hours chat hours** metrics in our earlier example. You’d find them in the **After-hours collaboration** metric category.

:::image type="content" source="../images/person-query-select-metrics-pane.png" alt-text="Add metrics pane with After-hours collaboration metric category expanded":::

###### Filters, keyword search, and more information

There are a few other ways you can find metrics to include in your query. You can filter by type (for example, **Activity count metrics** or **Meeting metrics**) on the left side of the pane, or use the search bar to find metrics by keyword. If you're working with [Power BI templates](./templates/introduction-to-templates.md), use **Filter by Power BI templates** to pick metrics used in particular reports.

To find out more about a metric, hover over its information icon.

:::image type="content" source="../images/person-query-hover-metric-tooltip.png" alt-text="Screenshot of metric tooltip for Call hours.":::

### To add metrics to your query

Here’s how you add metrics to your query:

3. Under **Select metrics for what you want to know about your employees**, select the **Add metrics** button.

    :::image type="content" source="../images/person-query-add-metrics.png" alt-text="Select metrics section, with 'Add metrics' button highlighted":::

4. The **Add metrics** button brings you to the **Select metrics** pane. Using the check marks and the tools described earlier (filter, search, and groupings) select the metrics you want to use in the query, then select **Add to query**.

    The **Add to query** button adds these metrics into your query and takes you back to the setup screen. The metrics you selected appear as tags in the box beneath the section description. 

    :::image type="content" source="../images/person-query-selected-metrics-tags.png" alt-text="Select metrics section, with selected metrics appearing as tags":::

### Employees

Once you determine what you want to know about employees, you select which employees you want to include in your query. In **Select which employees you want to include in the query**, define the employees you want to analyze through *conditions* and *condition groups*.

#### About conditions and condition groups

A condition is a statement about one attribute you want to analyze in your query. A condition only extracts rows from your organizational data that meet certain criteria, which you specify in the condition statement. For example, if your condition statement read, “Organization = Microsoft.com,” the query would only extract rows that equal “Microsoft.com” under the **Organization** column. A condition group is a combination of conditions connected with a conjunction ("and" or "or"). In the following image, the condition group is in the block to the right of the conjunction "or."

:::image type="content" source="../images/person-query-condition-group.png" alt-text="Condition group":::

The app predefines one condition for you: “Is Active.” If you leave this condition set to “True,” the query only analyzes *active employees*. Active employees send at least one email or Teams chat during the unit of time—week or month—defined by the query’s **Group by** setting.

#### To add employees to your query

5. Underneath the predefined "Is Active" filter, select the **Add condition button**, then select **Organizational data**.
    :::image type="content" source="../images/person-query-add-conditions.png" alt-text="Screenshot that shows the Add condition button.":::

    To add a condition group, select the **Add condition group** button and select the **Organizational data** attribute(s), **Operator** (= or !=), and **Value(s)**. The values you select appear as tags.

    >[!Note]
    >
    >The default conjunction for conditions and condition groups is “and.” To select “or” instead, use the dropdown menu.

#### Total and measured employees

Beneath the **Add condition** and **Add condition group** buttons, you’ll see a number for **Total employees** and **Measured employees**. These numbers represent how many employees could be measured and how many employees the query is actually measuring, respectively. Checking these numbers before running your query can help you determine whether you’ve selected the right conditions and condition groups.

### Employee attributes

#### About employee attributes

Employee attributes are the data fields—or columns—that you’ve uploaded in your employee data. In **Select which employee attributes you want to include in the query**, you narrow down which data fields your query includes—for example, **Job level** or **Hire date**—to prevent your output (.csv) file from being larger than necessary. Making selections here:

* Improves data analysis with fewer columns in a smaller file.
* Further protects private data by excluding columns from the file.
* Enables you to select **Clear all** to clear the selected columns.

#### To add employee attributes to your query

6.	Select the **Select attributes** button, then:
    1. On the right pane, use the checklist to make selections.
    1. When you're done picking attributes, select the **Add to query** button.
        :::image type="content" source="../images/person-query-select-attributes.png" alt-text="Select employee attributes section, with 'Select attributes' button highlighted":::
    Attributes appear as tags in the box about the **Select attributes** button.

    >[!Note]
    >
    >If an attribute appears as a red tag, that attribute might have been removed or renamed. You might see red tags if you’re cloning or editing a query and the attributes have changed since the query was last run. You can remove these marked attributes to get the query to run properly.

## Running the query

7.	After you’ve set up your query, selected metrics, set conditions and condition groups, and selected employee attributes, you’re ready to run your query. Select the **Run** button in the screen’s upper right.

### To access your query results

After your query runs, access its results in the **Query results** page. On the **Query results** page, you can also edit and clone your query. For further information, refer to [Access query results and modify existing queries](./query-results.md).

## Example Person query for after-hours communication

Let’s say you wanted to run a Custom Person query to find out how often managers are emailing and sending Teams chats after their working hours. You want to:

* Analyze your company’s “West” organization only, which is provided in your employee data.
* See data for the last six months, grouped by month.
* Exclude Senior managers from the query.

Here’s how you might do that:

1. Set up your query:
    1.  **Query name**: Give your query a custom name by typing in something like “AfterHoursWest.”
    1. **Time period**: Select **Last 6 months**.
    1. **Auto-Refresh**: You just want to have this run once, so leave the **Auto-Refresh** box deselected.
    1. **Description**: Other analysts in your organization might want to know more about this query, so give it a brief description.
    1. **More settings**: You want this query to be grouped by month, not week. Select **More settings**, then change **Group by to Month**.
2. Now you’re ready to add metrics:
    1. Under **Select metrics for what you want to know about your employees**, select the **Add metrics** button.
    1. Because you want to add metrics about collaboration after hours, expand the **After hours collaboration** metric category. 
    1. Select the **After hours email hours** and **After hours instant messages** metrics.
    1. Select the **Add to query** button.
3. Next, specify the employees you want to analyze.
    1. Under **Select which employees you want to include in the query**, leave the "Is Active" filter set to “true.“
    1. Select **Add condition**.
    1. Select **Organizational data**.
    1. Select **Organization**, leave the **Operator** at “=,” and select an employee organization of your company from the dropdown list. As we identified earlier, you’d select “West” from this list. 
    1. Select **Add condition group**. You don’t want to include Senior managers in this query, so:
        1. Select **Level designation** from the **Organizational data** dropdown.
        1. Leave the **Operator** at “=.”
        1. If you want, you can use the search bar to help find titles with “Manager.” Select Manager, Sales manager, and Design manager from the dropdown list.
    1. Check the **Total employees** against the **Measured employees**. If this number seems off, adjust your conditions above.
4. Now you can choose the employee attributes you want to include in your output file.
    1. Under **Select which employee attributes you want to include in the query**, select the **Select attributes** button.
    1. From the right pane, select **PopulationType**.
    1. Select the **Add to query** button.
5. It’s time to run the query. On the upper right of the screen, select the **Run button**.
6. After the query successfully runs, you can find its results in the **Query results** page. To:
    1. Download the .csv output file: Select the CSV icon from the **Downloads** column. If you want to connect the query to another file, like a Power BI visualization, you can select the copy link icon.
    1. **Edit**, **Edit query name**, **Clone**, **Favorite**, or **Delete** the query: Select the ellipses to the right of the **Downloads** column, then select the appropriate choice. 

    > [!Caution]
    > Editing queries overwrites existing results. If you want to keep your query’s results, use the **Clone** feature—which creates an identical copy of the query—instead.

    >[!Note]
    > Only the analyst who originally ran the query can **Edit query name**, **Edit**, or **Delete** the query. Other analysts in the organization can **View**, **Clone**, and **Favorite** the query.

## Related topics

[Metric descriptions](./metrics.md)

[Access query results and modify existing queries](./query-results.md)

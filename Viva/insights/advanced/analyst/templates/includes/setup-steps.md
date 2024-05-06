 3. Under **Query setup**:
    
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    1. Set **Auto-refresh** (optional). You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.
       > [!NOTE]
       > If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing.
     4. Type a **Description** (optional).   
     5. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. For more information about metric rules, refer to [Metric rules](../../metric-rules.md). 
        > [!NOTE]
        > The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you're not able to edit this field.

 1. Under **Predefined template metrics**, view the list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can’t remove them. You can add other metrics by selecting **Add metrics**. 
    > [!IMPORTANT]
    > Low-quality or missing organizational data might affect your metrics and result in warnings or errors. Learn more about data-quality notifications in [Data quality in the analyst experience](../../data-quality-analyst-experience.md).

 1. In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, refer to [Filters](../../filters.md). If you notice a warning or error here, it's because one of your attributes is missing from your organizational data or is of low quality.
 1. Under **Select which employee attributes you want to include in the query**, add up to 20 organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.
    > [!IMPORTANT]
    > This PowerBI query needs some specific attributes to run, and we've preselected them for you. These attributes appear in gray and you can't remove them. We might also include some attributes that help your template, but aren't required for your query to run. These attributes appear in blue and you can remove them.
    >
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is missing that attribute. 
    >
    > Learn more about attributes and data quality in [Data quality in the analyst experience](../../data-quality-analyst-experience.md).
 1. Select **Run** on the upper right side of the screen. The query might take a few minutes to run.

### Access query results 
You can access the report in two different ways: 
1.	View the report in the browser. Use this option if you only want to View the report.
2.	Open the Power BI template in Power BI desktop and connect to your query results. Use this option if you want to customize the report or share it with others in your organization by publishing the report to the Power BI Service.

### View report in the browser
To view the report in the browser, go to the **Query results page** and select the eye icon in the View column. You can select **Open in new tab** if you want to keep the report in the background while doing other tasks in Advanced insights.

### Open the Power BI template in Power BI Desktop

1. Go to the Query results page and select the Power BI icon in the Actions column to download the Power BI template and get the query and partition identifiers. You’ll need these identifiers later.
1. Open the downloaded template.
1. If you're prompted to select a program, select **Power BI**.
1. When you're prompted by Power BI:
   1. Paste in the partition and query identifiers.
   1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
   1. Select **Load** to import the query results into Power BI.
1. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.
    > [!IMPORTANT]
    > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
   > :::image type="content" source="../../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab." :::


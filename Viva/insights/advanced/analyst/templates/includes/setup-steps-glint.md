---
ms.date: 05/19/2023
author: zachminers
ms.author: v-zachminers
ms.topic: include
ms.service: viva-insights
--- 

3. Under **Query setup**:
    
    1. Type a **Query name**.
    2. Type a **Description** (optional).   
    3. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. For more information about metric rules, refer to [Metric rules](../../metric-rules.md). 
    
    >[!Note]
    >You’re not able to edit the date range or turn on auto-refresh for this report. 
    >
    >This report analyzes data 90 days before and after the survey closed. To work, it needs at least 30 days of data before the survey started.
    > 
    >The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you're not able to edit this field.

4. Under **Predefined template metrics**, view the list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can’t remove them. You can add other metrics by selecting **Add metrics**, but these metrics won’t be available to use in the Power BI report at this time. Under the **Is active** filter, select **Add condition**, then select your organizational data.
    > [!IMPORTANT]
    > Low-quality or missing organizational data might affect your metrics and result in warnings or errors. Learn more about data-quality notifications in [Data quality in the analyst experience](../../data-quality-analyst-experience.md).

5. Under **Select which employees you want to include in the query**, choose a filter to identify the employee group you’d like to focus on. We've set one filter for you. You’re not able to add additional filters.
6. Under **Select which employee attributes you want to include in the query**, add your organizational attributes. Once the query runs, use these attributes to group and filter the reports.
    > [!IMPORTANT]
    > This Power BI query needs some specific attributes to run, and we've preselected them for you. These attributes appear in gray and you can't remove them. We might also include some attributes to improve the relevancy of your results, like "Organization," but aren't required for your query to run. These attributes appear in blue and you can remove them.
    >
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is missing that attribute.
    >
    > Learn more about attributes and data quality in [Data quality in the analyst experience](../../data-quality-analyst-experience.md).
7. Select **Run** on the upper right side of the screen. The query might take a few minutes to generate.
    1. When your query results are ready, go to the **Query results page** and select the eye symbol above **Power BI** to view the report.
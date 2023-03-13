 3. Under **Query setup**:
    
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    1. Set **Auto-refresh** (optional). You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.
        >[!Note]
        >If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing.
     4. Type a **Description** (optional).   
     5. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. For more information about metric rules, refer to [Metric rules](../../metric-rules.md). 
        >[!Note]
        >The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you're not able to edit this field.

 1. Under **Predefined template metrics**, view a list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can’t remove them. However, you can add other metrics. 
     1. Customize your keywords (optional). This query uses a set of keywords within the **Calendared learning time** metric to determine training-related events. If you want to customize these keywords, you'll need to create a new metric now. Go to the [To customize your keywords](../new-hire-onboarding.md#to-customize-your-keywords) section for detailed steps on creating a new custom metric. Then, return here to complete the query process.

### Link report to query

10. Open the downloaded template.
1. If you're prompted to select a program, select **Power BI**.
1. When you're prompted by Power BI:
   1. Paste in the partition and query identifiers.
   1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
   1. Select **Load** to import the query results into Power BI.
1. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.
   >[!Important]
   > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
   >:::image type="content" source="../../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab." :::


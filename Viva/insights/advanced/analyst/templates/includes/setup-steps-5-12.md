
5. In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, refer to [Filters](../../filters.md).

    ![Is active filter](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

6. Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    >Some employee attributes are required to set up this Power BI template, and we've preselected them for you in the query. You can't remove these preselected attributes.
    >
    >If you notice attributes marked in red and the query’s **Run** button disabled, it means that these attributes are required and they're missing from your organizational data. Contact your admin to upload them.

7. Select **Run** on the upper right side of the screen. The query might take a few minutes to run.

8. When your query results are ready, go to the **Query results page** and select the Power BI icon. Download the Power BI template and get the partition and query identifiers. You’ll need these identifiers later.

### Link report to query

9. Open the downloaded template.

10. If you're prompted to select a program, select **Power BI**.

11. When you're prompted by Power BI:
    1. Paste in the partition and query identifiers.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.

>[!Important]
> You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
>:::image type="content" source="../../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab." :::


After the report is set up and populated with Viva Insights data in Power BI, review information on the **Summary** page. 
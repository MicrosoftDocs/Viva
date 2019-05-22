---
# Metadata Sample
# required metadata

title: CRM queries in Workplace Analytics 
description: Describes how to use Queries to analyze CRM data in Workplace Analytics 
author: madehmer
ms.author: v-midehm
ms.date: 05/22/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---
# Queries with CRM data

If your organization has [uploaded CRM data](../setup/crm-data-upload.md) into Workplace Analytics, you'll see an additional set of customer filters based on your CRM data. For example, the following graphic shows AccountPotential as the selected Customer filter.

![Customer filter](../Images/WpA/Tutorials/customer-filter.png)

## Person-to-group queries

Person-to-group queries in Workplace Analytics help you understand how an individual invests their time across the rest of the organization and beyond. The query results list individuals ("time investors") by their PersonIDs (de-identified), one or more groups that you define in the query ("their collaborators"), and the amount of time that the time investor spends with the groups that you define.

If you have CRM data available in the **Time investors** section, you can optionally filter the results to include specific time investors from both your CRM data and Organizational data in the query. For example, the following graphic shows an employee filter of **FunctionType** > Equals > **Sales** *and* customer filters of **IsAccountOwner** or **IsSeller** > Equals > **True**, which will include query results for employee time investors in Sales and customer time investors in one of these two CRM roles.

   ![Group and filter time investors for CRM](../Images/WpA/tutorials/p2g-time-investors-crm.png)

    If CRM data is available, you'll also see customer attributes you can select to group collaborators by, including Accounts and AccountName.

9. In the **Their collaborators** section, you can add customer filters to exclude specific collaborators, such as AccountName, AccountType, or ContactDepartment. These are the same as for time investors.

## Group-to-group queries

Group-to-group queries in Workplace Analytics give results that help you understand how a team invested their time across the rest of the organization and beyond. The query results list pairs of groups, as defined by the organizational attributes and if available, the CRM attributes that you choose, along with how much time people in the first group (the "time investors") allocated to other groups ("collaborators").

For example, if CRM data is available, you could analyze how much time your sales team (AccountOwners and Sellers) spent with customers (CRM AccountType = Customer) as compared to time spent on other (non-customer) collaboration.


7. In the **Time investors** section, answer the next question _How do you want to group the time investors?_ by specifying an attribute for this group, for example, FunctionType, IsInternal, or TenureMonths. If CRM data is available, you can also group time investors by customer attributes, such as AccountOwner or Seller.

   ![Group and filter time investors](../Images/WpA/tutorials/g2g-02-group-filter-time-investors.png)

Optionally, you can remove some of the time investors from this analysis by applying one or more filters under the question _Do you want to limit the analysis to only certain time investors?_

9. In the **Their collaborators** section, you can add filters to exclude collaborators, such as Domain, FunctionType, or Organization, which are the same as for the time investors section. If CRM data is available, you can also group the collaborators by customer account and contact attributes, such as AccountName or ContactAccountID.

   At this point, the collaborators are ungrouped, which means the query results will not show you which collaborators interacted with the time investors.

 ![Exclude collaborators](../Images/WpA/tutorials/g2g-03-exclude-collaborators.png)

10. Answer the question _How do you want to group the people who collaborated with the time investors?_ to group the collaborators. This will show you which groups interacted with the time investors. You can also combine groups of collaborators for the purpose of isolating other specific groups who interacted with the time investors.

    ![Group collaborators](../Images/WpA/tutorials/g2g-04-group-collaborators.png)

11. Select **Run** at the top right to run the query.
12. On the **Queries** > **Results** page, the query status shows as **Submitted**. After the query status changes to **Succeeded**, you can view it, share it, download it (in .csv file format), delete it, or [Copy an OData link](https://docs.microsoft.com/en-us/workplace-analytics/use/view-download-and-export-query-results#get-a-link-for-odata-feed-that-you-can-use-in-power-bi) to use in a visualization tool, such as Power BI or Excel.

## Related topics

[Person-to-group queries](../Tutorials/person-to-group-queries.md)

[Group-to-group queries](../Tutorials/group-to-group-queries.md)

[Metric descriptions](../Use/Metric-definitions.md)

[View, download, and export query results](../Use/View-download-and-export-query-results.md)


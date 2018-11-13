---
# Metadata Sample
# required metadata

title: Person queries in Workplace Analytics 
description: Describes how to use Person queries in Workplace Analytics to analyze the collaboration of individuals in your organization, from the point of view of each individual.     
author: madehmer
ms.author: madehmer
ms.date: 9/21/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Person queries

The person query analyzes data from the point of view of each individual in the organization.

This creates a lot of flexibility in analyzing data. For example, you can learn:

* How time use varies by different organizational attributes?
* How specific subgroups in the organization spend their time?
* How one aspect of collaboration influences other time-use habits?

  ![Person query questions](../Images/WpA/Tutorials/Person1.png)

The person query metrics fall within four broad categories. You can add standard metrics from each category to your query. Depending on the analysis, you can summarize a person’s collaboration metrics by day, week, or month.

![Four types of person metrics](../Images/WpA/Tutorials/four-types-of-person-metrics.png)

Each query returns one row per person, per period.

![Query results row](../Images/WpA/tutorials/query-results-row.png)

The file will include any standard or customized metrics you specify. The IsActive column in the output file is True if the employee sent at least one email during the specified time period for the query. 

![Query results metrics](../Images/WpA/Tutorials/query-results-metrics.png)

 And your results will include any employee organizational data attributes that your Workplace Analytics admin has uploaded.

![Query results attributes](../Images/WpA/Tutorials/query-results-attributes.png)

You can use organizational attributes to further summarize the person results and create powerful analyses that compare and contrast the collaboration of different groups in the organization.

![Query results summary](../Images/WpA/Tutorials/query-results-summarize.png)

## Create a person query

It’s simple to set up a person query.

* Select whether you want each person’s metrics summarized by day, week or month, and the period you’d like to analyze.
* Select if you want active, inactive, or all employees included in the query. Active employees are those who sent at least one email during the set time period (the aggregated period set for the query).
* Select a custom rule set to exclude meetings from the calculations, otherwise it'll use the default.

![Create person query](../Images/WpA/Tutorials/create-person-query.png)

## Add filters

You can use filters to exclude certain rows from the output file based on the person’s organizational attributes, such as size or function type.

The Organization filter can limit the query to those in the specified groups. For example, the following filter will only list people from the R&D and Engineering groups.

![Person query filter](../Images/WpA/Tutorials/query-filter.png)

## Add metrics

You can add metrics to further customize your person query data. The options vary based on the type of metric, but can include criteria related to meetings and email.

Meetings:

* When the event occurred
* How many people were involved
* Subject line keywords
* Attendee/organizer attributes

Email:

* When the email was sent
* How many people were included on the email
* Subject line keywords
* Recipient/sender attributes

For example, you can add a metric to get an email count for each person where at least one person from the Sales organization is included in email.

 ![Person query base metric](../Images/WpA/Tutorials/query-base-metric.png)

You can add a filter to a base metric and edit the metric name with the filter. For example, the following shows _Emails sent to Sales_, which will be the column header in the output file.

![Person query custom metric](../Images/WpA/Tutorials/query-custom-metric.png)

To get more details on adding metric filters, see [Customize a metric](../Tutorials/customize-a-metric.md).

### Business scenario example of long meetings

You can create a Person query to investigate if long meetings are a significant factor in the total number of meeting hours for Operations. The following custom query uses metrics and filters to customize the data.

**Query criteria**

* Time frame: Shows the data aggregated weekly
* Who: Filters on Operations
* What data: Metrics
  * Meeting hours are the total of all meeting hours
  * Long meeting hours that include long meetings that last 2 or more hours
  * Meetings is the total number of meetings
  * Emails sent is the total number of emails sent

### To create a custom Person query

1. On the Queries page, select **Person**.
2. In the **Enter query name here** box, enter **Operations long meetings**.
3. In the **Group by** menu, select **Week**, select the date range you want, and then in the **Meeting exclusions** menu, select the exclusion rule set.
4. For **Included employees**, select if you want **Active only**, **Inactive only**, or **All employees** included in the query. Active employees are those who sent at least one email during the aggregated time period (date range) set for this query.
5. In the **Filters** section, select **Add filter**, and then in the menus, select **FunctionType** > **Equals** > **Operations**.
6. To add a metric for total meeting hours, in the **Metrics** section, select **Add metric**, and then select **Meeting hours**. Choose the Edit icon and change the metric's name to **Total meeting hours**.
7. To add a custom metric for long meeting hours, select **Add metric**, and then select **Meeting hours**. Choose the Edit icon and change the metric's name to **Long meeting hours**.

    a. To customize the Long meeting hours metric, select the Edit icon.
    b. Choose **Add filter**.
    c. In the **Long meeting hours where** section, select **Meeting**, and then select **Duration­Hours** > greater than or equal to > **2**.
    d. Select **Confirm**.

8. To add a metric for total number of meetings, select **Add metric**, and then select **Meetings**. Choose the Edit icon and change the name to **Total number of meetings**.
9. To add a metric for sent email, select **Add metric**, and then select **Emails sent**. Choose the Edit icon and change the metric name to **Number of emails sent**.

    > [!Note]
    > * If no data exists for a person/date combination for a metric, the query results will not have a row for that person/date combination.
    > * When aggregating data by the week or the month, you might want to include a metric that has a zero value.
    > * To make sure you have a line of data for every person and date combination for the metrics, add **Emails sent** as one of your metrics.
    > * After you export the results, replace all null values with zeros to ensure that calculations for averages and other statistics include all person and date combinations.

10. Select **Run** at the top right to run the query.
11. On the Results page, you can view the query and its status. When the query results are complete, you can download them as a .csv file to continue your analysis.

**Person query results include the following columns**

* Person ID - De-identified ID number for the person represented in the metric.
* Date - The start date of the aggregation (i.e. if the week is 6/3 to 6/10, then it is 6/3. If it is a month, then it is the start of the month your data encompasses).
* Person Attributes - Each of the person attributes in the data set supplied by the organizational data.
* Metrics - Any other metrics that you included in the query.

**Person ID**|**Date**|**Person attribute 1 (department)**|**Person attribute 2 (role)**|**Metrics - Email hrs**|**Metrics Meeting hrs**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
A|3/1/2017|HR|Administrator|5|11
B|3/1/2017|Marketing|Executive|4|14

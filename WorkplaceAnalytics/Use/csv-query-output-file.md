---
# Metadata Sample
# required metadata

title: Csv file query output in Workplace Analytics
description: An article that helps to understand the meaning of the .csv file query output columns available from Workplace Analytics.
author: buntus
ms.author: v-johtob
ms.date: 10/08/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Understand and interpret query output

After you run a query from the Queries page, the query Results page  opens by default, and displays a download link to a .csv (comma-separated values) file that contains all the results of your query output.

![Csv file download](../images/WpA/Use/csv-download.png)

You can also select the _Copy link_ button to the right of the download link to get a link to an OData feed that you can use to directly load query results into BI analysis tools such as Power BI. For more information, see [Use Workplace Analytics data in Power BI and other data analysis tools](https://docs.microsoft.com/workplace-analytics/use/view-download-and-export-query-results#use-workplace-analytics-data-in-power-bi-and-other-data-analysis-tools).

## Person-to-group query output

You can use person-to-group queries to help you understand how de-identified individuals invest their time internally and externally. Person-to-group queries can be used for either internal or external collaboration. 

The query output lists these de-identified _Time investors_ (licensed employees) by: a) their PersonIds, b) one or more groups that you define in the _Collaborators_ section, and c) the amount of time that the time investor spends with the specified groups. 

So on the "person" side of the query, you will have PersonIds that map to "collaborators" groups on the group side. For group-to-group queries, you will have Time investor groups that map to "collaborators" groups.

In person-to-group queries, the .csv file query output consists of various column headers with single rows for each unique pairing of an individual in the time investor group with any collaborator in the collaborator group during the time periods that the person has collaborated with that group. 

Take the example of a person with a PersonID, P1, who has collaborated with group G1 in weeks one and three of a certain month. Assuming that you run a person-to-group query by selecting "week" as the _Group by_ option (*How do you want to group the people who collaborated with the time investors?*) in the _Time investors_ section, rows are created for (P1, G1) in weeks one and three only. 

![Table of columns](../images/WpA/Use/personId.png)

>[!Note]
> People are assigned randomly-generated PersonIds to maintain de-identification. No individuals can be identified from the query output.

The .csv file query output for person-to-group queries consists of general header columns (categories) and metrics header columns. The output also displays additional organization-related attribute columns that will vary from company to company.

## Header columns

  The following table lists the person-to-group header columns found in the .csv output file:

| Header column | Description |
|---|---|
| **PersonId** | This header column displays a randomly-generated PersonId value for each time investor. When the company administrator initially uploads employee organization information, employee names are used in rows, but these names become de-identified when Workplace Analytics processes the output. |
| **IsInternal** | This header column value equates to true for all internal company employees and equates to false for all people external to the company. |
| **FunctionType** |  This header column represents the function that employees perform within the company, for example, Manufacturing, HR, or Finance. |  
| **Organization**<sup>*</sup> | This header column represents the name of the organization to which a person belongs. For information on other variable organization-related columns, see [Organizational attribute columns](#organizational-attribute-columns). |
|  **Collaborators**_\<collaborator group-by attribute> | The Collaborators header column displays the various values of the attribute by which the collaborators were grouped. For example, if you select "Domain" as the Group by attribute, the values will be all the email domains with which time investors have collaborated.  The name of this header column changes depending on the group by attribute selected for the collaborators part of the query. So if you group collaborators by domain, the column name will be concatenated as Collaborators_Domain. If you selected the FunctionType Group by attribute, the values will be all the various company organizations with which the time investors have collaborated, such as Sales, HR, or Finance.  Similarly, the column name will be concatenated as Collaborators_FunctionType. |  
| **Date** | This column displays either the first day of the week (Sunday) or first day of the month, depending on which date option you originally selected as the group by attribute.|  

<sup>*</sup> The Organization and FunctionType columns are similar in that they both reflect the function of employees within an organization; however, the values of each may differ, as in the following examples:

| Organization | FunctionType |
|---|---|
| Marketing |Branding |   
| Operations  | Supply Chain |   
|Operations| Manufacturing|

### Organizational attribute columns

In addition to the standard columns present in the .csv file output of person-to-person queries, the output  typically contains a variable set of header columns that represent the organizational attributes of employees. Admins upload these  attributes when Workplace Analytics is initially set up. These columns are listed to the right of the Organization column for every person included in the query output. The names of the columns will vary from company to company; however, sample organizational attributes might include items such as: StartDate, tenuremonths, or quotaattainment.

### Metrics header columns

The .csv output file for both person-to-group queries and group-to-group queries will include one or more header columns based on the following standard or customized metrics selected from the Queries page: 

![Table of columns](../images/WpA/Use/select-metrics.png)

The following table lists the person-to-group metrics header columns:


| Metric | Description |
|---|---|
|**Collaboration hours**  |Shows the total amount of time that a de-identified individual has spent collaborating with the collaborator group. This includes time spent in email and meetings. |
| **Email count** |Shows the number of emails sent between the time investor and groups. |
| **Email hours** |Shows the amount of time that the time investor spent writing or reading emails. |
| **Meeting hours** |Shows the number of hours that the time investor spent in meetings.|
| **Meetings** |Shows the number of meetings in which the time investor and the collaborators participated. |
| **Network size** | Shows how many people with whom the time investor had meaningful interactions in the selected collaboration group over the selected time period.  |

**The IsActive attribute** 

The *IsActive* attribute does not display as an option in the person-to-group query. However, *IsActive* comes into play when you select an option from the Included employees menu during the person-to-group query. The header column then shows up in the .csv query output. *IsActive* applies to either Active employees only, Inactive employees only, or All employees, and has a Boolean value of true or false.

![Selected employees](../images/WpA/Use/selected-employees.png)

## Additional attribute values

In addition to the standard attribute values, the _Collaborators_ group can also display four additional attribute values in the .csv file query output for both person-to-group and group-to-group queries:

1. Unclassified_Internal

2. Unclassified_External

3. Other collaborators

4. Collaborators Within Group

### Unclassified_Internal

In the following diagram, under the section _Their collaborators_, the collaborators who match the filter option defined in question 3C, and who are also internal to the company (as indicated by the "IsInternal = true" attribute) will be grouped together under the _Unclassified_Internal_ bucket. Metrics for all such collaborators are added up.

For example, if we run a query for all collaborators who match FunctionType = HR, all those who do not match the filter, say, people from Sales or Marketing, if they are internal employees, will be placed in the _Unclassified_Internal_ category.

![Unclassified internal](../images/WpA/Use/unclassified_int_ext.png)

### Unclassified_External

The collaborators who match the filter option defined in question 3C in the diagram, and who are external to the company (as indicated by the "IsInternal = false" attribute) will be grouped together under the value _Unclassified\_External_. Metrics for all such collaborators are added up.

Similar to the case of Unclassified_Internal, those who do not match the filter, for example, if they are external employees, will be placed in the _Unclassified_External_ category.

### Other collaborators

If the query is using the _Group by_ attribute, both the collaborators who match the filter option defined in question 3C in the diagram and the collaborators who do not have the group-by attribute defined, will be grouped together under the _Other collaborators_ category.

For example, suppose we ran a query for collaborators to find out which organizations they have collaborated with, and passed them through the filter FunctionType = HR. Those who match the filter move forward. Then, if we group the collaborators by city, say, San Francisco and Boston, the query will find all collaborators who had interactions with HR in San Francisco and will place them in the San Francisco category, and similarly for Boston. The query output will now contain entries for each person (or group if it's a group-to-group query) displaying how much time each one spent collaborating with HR in each city. 

In some instances, certain people may not have the organizational attribute defined. (_City_ is an HR attribute). This might be because such employees are mobile and do not have fixed location, and cannot be classified by city. Such employees will be placed in the _Other Collaborators_ category.

### Collaborators Within Group

If the result of a query defines the same set of people as members of both the time investors and collaborators groups, _and_ these individuals also match the filter defined in option 3C, as in the  diagram, then the collaborators are grouped together under the value _Collaborators Within Group_. These additional values also display in the .csv file query output for group-to-group queries.

## Group-to-group query output

You can use group-to-group queries to help you understand how groups or teams invest their time across the internal organizations in the company and also how they invest their time with groups external to the company. The .csv file query output lists pairs of groups, defined by the selected organizational attribute, and shows how much time the first group has allocated to the second group. 

The .csv file query output of a group-to-group query consists of various column headers with a single row for each unique pairing of a time investor group with a collaborator group during the time periods that any person in the time investor group collaborated with a specific collaborator group. Assuming that the group-to-group query is run by selecting "week" as the _Group by_ option, if any individual in group G1 collaborated with any individual in group G2 in, say, weeks one and three of a specific month, then rows will only exist for G1 and G2 in weeks one and three.

![Group-to-group time investors-collaborators](../images/WpA/Use/g2g-time-investors-collaborators.png)

The .csv file query output for group-to-group queries, like person-to-group queries, also consists of general header columns and metrics header columns.

### Header columns

|Header column | Description |  
|---|---|
| **TimeInvestors**_\<time-investor group-by attribute>: | The name of this header column in the .csv output depends on the _Group by_ attribute selected in the time investors part of the query. For example, in the previous table, collaborators are grouped by FunctionType, so the column name is concatenated as TimeInvestors_FunctionType.|   
|  **Collaborators**_\<collaborator group-by attribute>: | The name of this header column depends on the _Group by_ attribute selected in the collaborators part of the query. In the previous table, collaborators are grouped by domain, so the column name is concatenated as Collaborators_Domain.     |   
| **Date** | This column displays either the first day of the week (Sunday) or the first day of the month, depending on the date option you originally selected as the _Group by_ attribute.|  

### Metrics columns

| Metric column | Description   |  
|---|---|
|**Email hours**  | The number of hours spent sending and reading emails between the time investor and collaborator groups.   |   
| **Meeting hours**  |  The number of meeting hours the time investor group has spent meeting with the collaborator group.  |   
| **Meetings** |The number of distinct meetings with at least one attendee from the time investor and collaborator groups. |
| **Meeting attendee count** |  The total number of attendees in all meetings from the time investor and collaborator groups |  
|**Meetings invitee count** | The total number of invitees in all meetings from the time investor and collaborator
| **Collaboration hours**  | The sum of meeting hours and email hours spent between the time investor and collaborator groups.   |  
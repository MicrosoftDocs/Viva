---
# Metadata Sample
# required metadata

title: How to interpret query output in Workplace Analytics
description: Understand and interpret query output is Workplace Analytics
author: madehmer
ms.author: v-midehm
ms.date: 04/08/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---

# Understand and interpret query output

After you run a query in Workplace Analytics, the Results page in Queries will appear in the list with a download link as .csv (comma-separated values) file with the query output.

![.csv file download](../images/WpA/Use/csv-download.png)

You can also select the _Copy link_ button to get a link for an OData feed to directly load query results into Power BI or another data analysis tool, such as Excel. For more details, see [Use Workplace Analytics data in Power BI and other data analysis tools](https://docs.microsoft.com/workplace-analytics/use/view-download-and-export-query-results#use-workplace-analytics-data-in-power-bi-and-other-data-analysis-tools).

## Person query output

Person query output can include a number of different metrics, including the following:

* Person ID - De-identified ID number for the person represented in that data row.
* Date - The start date of the aggregated output (i.e. if the week is 6/3 to 6/10, then it is 6/3. If it is a month, then it is the start of the month your data encompasses).
* Person attributes - Attributes about the person supplied through the latest organizational (HR) data upload.
* Metrics - Any other metrics that you include in the query. See [Person query metrics](../use/metric-definitions.md) for more details.

### Duration hours adjusted for time booked in the calendar

If you add a person's working hours and after hours for email and meetings, do not expect these to equal the totals for working hours or after hours. This is due to slight differences in how the metrics are calculated in Workplace Analytics. 

Think of working hours and after hours totals as “time booked on your calendar” instead of “time in meetings.” Calculations for total meeting hours (time in meetings) adjusts the duration time to account for double booked meetings, where a person has two meetings scheduled at the same time or times that overlap on the calendar. A heuristic logic orders which meetings a person likely attended and assigns time accordingly.

However, this logic doesn't specify a “chunk” of time with start and end dates, but assigns time as a single number. This can cause a variation in meeting hours and after hours, in particular for double booked meetings and meetings that span between working hours and after hours on a person's schedule.

For example, if a person's work day ends at 5 PM and that person attends a scheduled meeting from 4:30 to 5:30 PM that is double booked with another meeting by a half hour (duration hours adjusted = 0.5hr), the calculation uses “time booked in the calendar,” which adds 0.5 hour to working hours, 0.5 hour as after-hours work, and adds 0.5 hour to total meeting hours, which can cause a discrepancy when comparing these totals.

## Person-to-group query output

You can use person-to-group queries to help you understand how de-identified individuals invest their time for either internal or external collaboration.

The query output lists these de-identified _Time investors_ (licensed employees) by:

a) Their PersonIds

b) One or more groups as defined in the _Collaborators_ section

c) The amount of time the time investor spends with the specified groups.

On the "person" side of the query, PersonIds map to "collaborators" groups on the group side. For group-to-group queries, the Time investor groups map to "collaborators" groups.

In person-to-group queries, the query output (.csv file) includes column headers with single rows for each unique pairing of an individual in the time investor group with any collaborator in the collaborator group during the time periods that the person has collaborated with that group.

For example, PersonId of P1 collaborated with group G1 in weeks one and three of the specified month. Assuming that you run a person-to-group query by selecting "week" as the _Group by_ option (*How do you want to group the people who collaborated with the time investors?*) in the _Time investors_ section, rows are created for (P1, G1) in weeks one and three only.

![Table of columns](../images/WpA/Use/personId.png)

>[!Note]
> People are assigned randomly-generated PersonIds to maintain de-identification. No individuals can be identified from the query output.

The query output for person-to-group queries consists of general header columns (categories) and metrics header columns. The output also displays additional organizational attribute columns that vary based on the organization.

## Header columns

  The following table lists the person-to-group header columns found in the output file.

| Header column | Description |
|---|---|
| **PersonId** | This header column displays a randomly-generated PersonId value for each time investor. When the company administrator initially uploads employee organization information, employee names are used in rows, but these names become de-identified when Workplace Analytics processes the output. |
| **IsInternal** | This header column value equates to true for all internal company employees and equates to false for all people external to the company. |
| **FunctionType** |  This header column represents the function that employees perform within the company, for example, Manufacturing, HR, or Finance. |  
| **Organization**<sup>*</sup> | This header column represents the name of the organization to which a person belongs. For information on other variable organization-related columns, see [Organizational attribute columns](#organizational-attribute-columns). |
|  **Collaborators**_\(collaborator group-by attribute) | The Collaborators header column displays the various values of the attribute by which the collaborators were grouped. For example, if you select "Domain" as the *Group by* attribute, the values will be all the email domains with which time investors have collaborated.  The name of this header column changes depending on the *Group by* attribute selected for the collaborators part of the query. So if you group collaborators by domain, the column name will be concatenated as Collaborators_Domain. If you selected the FunctionType Group by attribute, the values will be all the various company organizations with which the time investors have collaborated, such as Sales, HR, or Finance.  Similarly, the column name will be concatenated as Collaborators_FunctionType. |  
| **Date** | This column displays either the first day of the week (Sunday) or first day of the month, depending on which date option you originally selected as the group by attribute.|  


<sup>*</sup> The Organization and FunctionType columns are similar in that they both reflect the function of employees within an organization. However, the values of each might differ, as in the following examples:


| Organization | FunctionType |
|---|---|
| Marketing |Branding |
| Operations  | Supply Chain |
|Operations| Manufacturing|

### Organizational attribute columns

In addition to the standard columns present in the .csv file output of person-to-person queries, the output typically contains a variable set of header columns that represent the organizational attributes of employees. Admins upload these attributes when Workplace Analytics is initially set up. These columns are listed to the right of the Organization column for every person included in the query output. The names of the columns will vary from company to company; however, sample organizational attributes might include items such as, StartDate, tenuremonths, or quotaattainment.

### Metrics header columns

The .csv output file for both person-to-group queries and group-to-group queries will include one or more header columns based on the standard or customized metrics selected when you were creating the query.  

![Table of columns](../images/WpA/Use/select-metrics.png)

For more details about person-to-group metrics, see [Workplace Analytics metrics](../use/metric-definitions.md##person-to-group-metrics
).

**The IsActive attribute**

The *IsActive* attribute doesn't display as an option in the person-to-group query. However, *IsActive* is included when you select an option from the Included employees menu during the person-to-group query, which will show up in the query output. *IsActive* applies to either Active employees only, Inactive employees only, or All employees, and has a Boolean value of true or false.

![Selected employees](../images/WpA/Use/selected-employees.png)

## Additional attributes for group queries

In addition to the standard attribute values, the _Collaborators_ group can also include the following additional attribute values in the query output for both person-to-group and group-to-group queries:

* Unclassified_Internal
* Unclassified_External
* Other collaborators
* Collaborators within group
* Internal collaborators

### Unclassified Internal

In the **Their collaborators** section, the collaborators who match the filter defined in question 3C, and who are also internal to the company (as indicated by the "IsInternal = true" attribute) will be grouped together in the _Unclassified_Internal_ category. Metrics for all such collaborators are added up.

For example, if we run a query for all collaborators who match FunctionType = HR, all those who do not match that filter, such as internal employees from Sales or Marketing, will be included in the _Unclassified_Internal_ category.

![Unclassified internal](../images/WpA/Use/unclassified_int_ext.png)

### Unclassified External

The collaborators who match the filter option defined in question 3C in the diagram, and who are external to the company (as indicated by the "IsInternal = false" attribute) will be grouped together under the value _Unclassified\_External_. Metrics for all such collaborators are added up.

Similar to the case of Unclassified_Internal, those who do not match the filter, for example, if they are external employees, will be placed in the _Unclassified_External_ category.

### Other collaborators

If the query is using the _Group by_ attribute, both the collaborators who match the filter option defined in question 3C in the diagram and the collaborators who do not have the group-by attribute defined, will be grouped together under the _Other collaborators_ category.

For example, suppose we ran a query for collaborators to find out which organizations they have collaborated with, and passed them through the filter FunctionType = HR. Those who match the filter move forward. Then, if we group the collaborators by city, say, San Francisco and Boston, the query will find all collaborators who had interactions with HR in San Francisco and will place them in the San Francisco category, and similarly for Boston. The query output will now contain entries for each person (or group if it's a group-to-group query) displaying how much time each one spent collaborating with HR in each city.

In some instances, certain people may not have the organizational attribute defined. (_City_ is an HR attribute). This might be because such employees are mobile and do not have fixed location, and cannot be classified by city. Such employees will be placed in the _Other collaborators_ category.

### Collaborators within group

For people who are licensed, internal employees and have an org data attribute assigned for the group defined in 3C as people who collaborated with the time investors, then they will be included in the _Collaborators Within Group_. These additional values will also be included in the query output for group-to-group queries.

### Internal collaborators

This output metric is only applicable for “Time Investor Initiated Meeting Hours.”​ If the “Focus” filter in 3C is NOT set, Internal Collaborators will equal all employees who are not in the group selected in 3c. ​The Meeting hours generated by the meeting organizers for others in the company who we don't have an org data file attribute (i.e. no org data file, or no HR attribute)​.

## Group-to-group query output

You can use group-to-group queries to help understand how groups or teams invest their time across internal organizations in the company and also how they invest their time with groups external to the company. The output can list pairs of groups, defined by the selected organizational attribute, and show how much time the first group has allocated to the second group.

The query output for a group-to-group query includes various column headers with a single row for each unique pairing of a time investor group with a collaborator group, during the time periods that any person in the time investor group collaborated with a specific collaborator group. Assuming that the group-to-group query is run by selecting "week" as the _Group by_ option, if any individual in group G1 collaborated with any individual in group G2 in, say, weeks one and three of a specific month, then rows will only exist for G1 and G2 in weeks one and three.

![Group-to-group time investors-collaborators](../images/WpA/Use/g2g-time-investors-collaborators.png)

The query output for group-to-group queries, like person-to-group queries, also consists of the following general header columns and metrics header columns.

### Header columns

|Header column | Description |  
|---|---|
| **TimeInvestors**_\(time-investor group-by attribute) | The name of this header column in the .csv output depends on the _Group by_ attribute selected in the time investors part of the query. For example, in the previous table, collaborators are grouped by FunctionType, so the column name is concatenated as TimeInvestors_FunctionType.|
|  **Collaborators**_\(collaborator group-by attribute) | The name of this header column depends on the _Group by_ attribute selected in the collaborators part of the query. In the previous table, collaborators are grouped by domain, so the column name is concatenated as Collaborators_Domain.|
| **Date** | This column displays either the first day of the week (Sunday) or the first day of the month, depending on the date option you originally selected as the _Group by_ attribute.|  

### Metrics columns

| Metric column | Description |  
|---|---|
|**Email hours**  | The number of hours spent sending and reading emails between the time investor and collaborator groups. |
| **Meeting hours** |  The number of meeting hours the time investor group has spent meeting with the collaborator group. |
| **Meetings** |The number of distinct meetings with at least one attendee from the time investor and collaborator groups. |
| **Meeting attendee count** |  The total number of attendees in all meetings from the time investor and collaborator groups |  
|**Meetings invitee count** | The total number of invitees in all meetings from the time investor and collaborator.
| **Collaboration hours** | The sum of meeting hours and email hours spent between the time investor and collaborator groups. |  
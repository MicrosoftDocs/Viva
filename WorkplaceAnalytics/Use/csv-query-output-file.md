---
title: How to interpret query output in Workplace Analytics
description: Understand and interpret query output is Workplace Analytics
author: madehmer
ms.author: v-mideh
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
* Date - The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it'll be the first day of the month your data encompasses).
* Person attributes - Attributes about the person supplied through the latest organizational (HR) data upload.
* Metrics - Any other metrics that you include in the query. See [Person query metrics](../use/metric-definitions.md) for more details.

### Duration hours adjusted for time booked in the calendar

If you add up a person's email and meeting hours during and outside of their work schedule, do not expect these sums to equal the sums for working hours and after hours. Workplace Analytics calculates these groups of metrics differently.

For working hours and after-hours totals, Workplace Analytics uses "time booked on a person's calendar" instead of “time in meetings.” Calculations for total meeting hours (time in meetings) adjusts the duration time to account for double-booked meetings, where a person has two meetings scheduled at the same time or for times that overlap on the calendar.

Workplace Analytics uses a heuristic logic to order which meetings a person likely attended and assigns time accordingly. This logic doesn't specify a “chunk” of time with start and end dates, but assigns time as a single number. This can cause a variation in meeting hours and after hours, in particular for double booked meetings and meetings that span between working hours and after hours on a person's schedule.

For example, if a person's work day ends at 5 PM and that person attends a scheduled meeting from 4:30 to 5:30 PM that is double booked with another meeting by a half hour (duration hours adjusted = 0.5hr), the calculation uses “time booked in the calendar,” which adds 0.5 hour to working hours, 0.5 hour as after-hours work, and adds 0.5 hour to total meeting hours, which would cause a discrepancy when comparing the totals.

## Person-to-group query output

You can use person-to-group queries to help you understand how de-identified individuals invest their time for either internal or external collaboration.

The query output lists these de-identified *Time investors* (licensed employees) by:

a) Their PersonIds

b) One or more groups as defined in the *Collaborators* section

c) The amount of time the time investor spends with the specified groups

On the "person" side of the query, PersonIds map to groups of "collaborators" on the group side. For group-to-group queries, the "time investor" groups map to the groups of "collaborators."

In person-to-group queries, the query output includes column headers with single rows for each unique pairing of a person in the time investor group with any collaborator in the collaborator group during the time periods that the person  collaborated with that group.

For example, PersonId of P1 collaborated with group G1 in weeks one and three of the specified month. For a person-to-group query that's grouped by "week" in the **Time investors** section (*How do you want to group the people who collaborated with the time investors?*). Then rows will be created for (P1, G1) in weeks one and three only.

![Table of columns with time investors](../images/WpA/Use/personId.png)

>[!Note]
> People are assigned randomly-generated PersonIds to maintain de-identification. No individuals can be identified from the query output.

The query output for person-to-group queries consists of general header columns (categories) and metrics header columns. The output also displays additional organizational attribute columns that vary based on the organization.

## Attribute columns

  The following table lists the person-to-group header columns found in the output file.

| Header column | Description |
|---|---|
| **PersonId** | A randomly-generated PersonId value for each time investor. When the company administrator initially uploads employee organization information, employee names are used in rows, but these names become de-identified when Workplace Analytics processes the output. |
| **IsInternal** | This value is true for all internal company employees and equates to false for all people external to the company. |
| **FunctionType**<sup>*</sup> | Represents the function that employees perform within the company, for example, Manufacturing, HR, or Finance. |  
| **Organization**<sup>*</sup> | Represents the name of the organization to which a person belongs. For information on other variable organization-related columns, see [Organizational attribute columns](#organizational-attribute-columns). |
|  **Collaborators** (collaborator group-by attribute) | Represents the various collaborators by group. For example, if you select "Domain" as the *Group by* attribute, the values will be all the email domains with which time investors have collaborated.  The name of this header column changes depending on the *Group by* attribute selected for the collaborators part of the query. So if you group collaborators by domain, the column name will be concatenated as Collaborators_Domain. If you selected the FunctionType Group by attribute, the values will be all the various company organizations with which the time investors have collaborated, such as Sales, HR, or Finance.  Similarly, the column name will be concatenated as Collaborators_FunctionType. |  
| **Date** | Is either the first day of the week (Sunday) or first day of the month, depending on which date option you originally selected as the group by attribute.|  

<sup>*</sup> The Organization and FunctionType columns are similar in that they both reflect the function of employees within an organization. However, the values of each might differ, as in the following examples:

| Organization | FunctionType |
|---|---|
| Marketing |Branding |
| Operations  | Supply Chain |
|Operations| Manufacturing|

### Organizational attribute columns

In addition to the standard columns present in the .csv file output of person-to-person queries, the output typically contains a variable set of header columns that represent the organizational attributes of employees. Admins upload these attributes when Workplace Analytics is initially set up. These columns are listed to the right of the Organization column for every person included in the query output. The names of the columns will vary from company to company; however, sample organizational attributes might include items such as, StartDate, tenuremonths, or quotaattainment.

### Metric columns

The .csv output file for both person-to-group queries and group-to-group queries will include one or more header columns based on the standard or customized metrics selected when creating the query.  

![Table of columns for group-to-group queries](../images/WpA/Use/select-metrics.png)

For details about person-to-group metrics, see [Workplace Analytics metrics](../use/metric-definitions.md#person-to-group-metrics).

**The IsActive attribute**

For the **Employees** filter in the **Time investors** section, you can select if you want Active only, Inactive only, or All employees as time investors for the query. Active employees are those who sent at least one email or instant message during the aggregated time period (date range) set for the query. This option is only available for person and person-to-group queries, which will be the *IsActive* attribute column with a Boolean value of true or false for each row in the output file.

## Additional attributes for group queries

In addition to the standard attribute values, the *Collaborators* group can also include the following attribute values in the query output for both person-to-group and group-to-group queries:

* [Group C to Group T](#group-c-to-group-t)
* [Group T to Group T](#group-t-to-group-t)
* [Collaborators within group](#collaborators-within-group)
* [Internal collaborators](#internal-collaborators) (only applicable for *Time investor initiated meeting hours*)
* [Other collaborators](#other-collaborators)
* [Unclassified Internal](#unclassified-internal)
* [Unclassified External](#unclassified-external)

### Group C to Group T

Where **Group C** represents a collaborator group and **Group T** represents the time-investor group,  totals include time generated by the time-investor group for all other groups in the company. These totals do not include the time-investor group's time spent in the meetings.

### Group T to Group T

This metric is included in the query output for group-to-group queries, where **Group T** represents the time-investor group. The metric calculations vary for this group depending on the attribute in the query:

* For *Time investor initiated meeting hours* - The totals include time generated in meetings by Group T for other Group T *licensed*, internal employees. These totals don't include the organizers' time and don't follow time-allocation logic.

* For *all other group metrics*, such as meeting hours or collaboration hours - The totals include time generated by Group T in meetings where *unlicensed* employees from Group T are present. Unlicensed employees might be vendors or employees who no longer work in the group (hence unlicensed) but are included in the group because they match the group-by attribute in the organizational (HR) data.

### Collaborators within group

This attribute is also available in the query output for group-to-group queries. Metric calculations vary for this group depending on the attribute in the query:

* For *Time investor initiated meeting hours* - The totals include time generated in meetings organized by the time-investors group that are attended by other licensed employees from other internal groups. These totals don't include the time-investor group's time spent in the meetings.

* For *all other group metrics*, such as meeting hours or collaboration hours - The totals generated where the time investors who are *licensed* employees are the only attendees with no other groups present. These totals include the meeting organizer's time spent in the meetings.

### Internal collaborators

This attribute is only available for the *Time investor initiated meeting hours* metric.​ ​If no *Focus* filter is set, this group includes licensed, internal employees who have no organizational data value or have a different value for the *Group by* attribute. This is the total number of meeting hours created by the time investors who organized meetings with this group.​

### Other collaborators

If a query uses the *Group by* attribute, both the collaborators who match the filter option defined in question C of the graphic and who do not have the group-by attribute defined, are grouped together as *Other collaborators*. This metric is not applicable for *Time investor initiated meeting hours*.

For example, if you run a query to find out which organizations a person collaborated with, and passed them through the filter FunctionType = HR. Those who match the filter are included in the group. Then, if you group the collaborators by city, such as San Francisco and Boston, the query will then group all collaborators who had interactions with HR in San Francisco in the San Francisco group, and similarly for Boston. The query output will include entries for each person (or group for a group-to-group query) that show how much time each person spent collaborating with HR in each city.

In some instances, some people might not have the organizational attribute defined, such as *city*, because they are mobile and don't work in a city where the company has offices. These employees will be grouped as *Other collaborators*.

### Unclassified Internal

In the **Their collaborators** section, the collaborators who don't match the filter defined in question C of the following graphic and who are also internal to the company ("IsInternal = true") will be grouped together in the *Unclassified_Internal* category. Metrics for all such collaborators are added up for this category.

For example, if you run a query for all collaborators who match "FunctionType = HR," those who don't match that filter, such as internal employees from Sales or Marketing, will be included in the *Unclassified_Internal* category.

### Unclassified External

The collaborators who match the filter option defined in question C of the following graphic and who are external to the company ("IsInternal = false") will be grouped together in *Unclassified_External*. Metrics for all such collaborators are added up for this category. This metric is not applicable for *Time investor initiated meeting hours*.

![Query questions](../images/WpA/Use/p2g-query.png)

## Group-to-group query output

You can use group-to-group queries to help understand how groups or teams invest their time across internal organizations in the company and with groups outside the company. The output will list pairs of groups, defined by the selected organizational attribute, and will show how much time the first group has allocated to the second group.

The query output for a group-to-group query includes a number of column headers with a single row for each unique pairing of a time investor group with a collaborator group, for the time periods that any person in the time investor group spent with a collaborator group. For example, if you run a query with the *Group by* option of *week* and a person in group G1 spent time with a person in group G2 in the first and third week of a specific month, then rows will only exist for groups G1 and G2 in weeks one and three of the output file.

![Group-to-group time investors-collaborators](../images/WpA/Use/g2g-time-investors-collaborators.png)

The query output for group-to-group queries, like person-to-group queries, also includes the following general attribute and metric column headings.

### General attribute columns

|General attribute column | Description |  
|---|---|
|**TimeInvestors** (time-investor group-by attribute) | The name of this depends on the *Group by* attribute selected in the time investors part of the query. For example, in the previous table, collaborators are grouped by FunctionType, so the column name is concatenated as TimeInvestors_FunctionType.|
| **Collaborators** (collaborator group-by attribute) | The name of this depends on the *Group by* attribute selected in the collaborators part of the query. In the previous table, collaborators are grouped by domain, so the column name is concatenated as Collaborators_domain.|
|**Date** | Is either the first day of the week (Sunday) or the first day of the month, depending on the date option you originally selected as the *Group by* attribute.|  

### Metric columns

| Metric column | Description |  
|---|---|
|**Email hours** | The number of hours spent sending and reading emails between the time investor and collaborator groups. |
|**Meeting hours** | The number of meeting hours the time investor group has spent meeting with the collaborator group. |
|**Meetings** |The number of distinct meetings with at least one attendee from the time investor and collaborator groups. |
|**Meeting attendee count** | The total number of attendees in all meetings from the time investor and collaborator groups |  
|**Meetings invitee count** | The total number of invitees in all meetings from the time investor and collaborator.
|**Collaboration hours** | The sum of meeting hours and email hours spent between the time investor and collaborator groups. |  

For a complete list of and more details about group query metrics, see [Workplace Analytics metrics](../use/metric-definitions.md#group-to-group-metrics).
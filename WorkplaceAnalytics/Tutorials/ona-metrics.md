---
title: "[]{#ona-metrics .anchor}Organizational network analysis person
  queries"
---

ONA person queries help you measure connectivity within an organization.
In addition to the two influence metrics
([Influence](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#influence-define)
and [Influence
rank](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#influence-rank-define)),
ONA person queries also offer the a selection of tie metrics, starting
with [Diverse
ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#diverse-ties-define)
and [Strong
ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#strong-ties-define).

For basic information about these connectivity metrics, see their
definitions in [Workplace Analytics metrics / ONA
metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics).
For deeper descriptions of the connectivity metrics, see [ONA
metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-metrics.md).

## Run a query to determine ties and influence

You can use any of connectivity metrics in the ONA person query; in this
example procedure, you will query for Influence or Influence rank.

**Role** - Analyst

1.  In Workplace Analytics, select **Analyze** \> **Queries**.

2.  In **Start custom query**, select **Network: Person**:

-   ![ONA person query](media/image1.png){width="3.2916666666666665in"
    height="1.1458333333333333in"}

    ONA person query

3.  Select and change **Enter query name here** to a name, and then
    enter a description for the query.

4.  For **Group by**, select a time-grouping option: **Monthly** or
    **Aggregated**. If you choose Monthly, the query results will
    contain one row with data for each month in the time period that you
    chose. If you choose **Aggregated**, the query results will contain
    one row for the entire time period that you chose.

-   \[!Note\] Currently, the only [meeting-exclusion
    > rule](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/meeting-exclusions-intro.md)
    > that can be used with an ONA query is the [Tenant default meeting
    > exclusion
    > rule](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/meeting-exclusion-concept.md#default-meeting-exclusion-rule).
    > As you build your query, this rule is selected by default; it
    > cannot be deselected.

5.  If you want the query to run repeatedly, on a regular schedule,
    select **Auto-refresh**. (For more information, see [Auto-refresh
    option for
    queries](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/query-auto-refresh.md).)

6.  Under **Select network boundary conditions**, define a filter to
    select the measured employees that you want to analyze in this
    query. You can use the filters of this step, for example, to narrow
    the scope to a division or a group. If you skip this (optional)
    step, all measured employees will remain eligible for analysis.

> More information about this option: If you run this query on the
> entire company, the results will be based on all collaborations across
> the company. If this is your goal, you can retain the default search
> range, which is unlimited. But your goal might be to determine only
> particular people, perhaps to involve them in a pilot project to
> introduce a new tool or procedure. In this case, limit the query to
> search only within a particular division or group.

7.  Under **Select collaboration types**, specify the types of
    collaboration activities that you want to include in your analysis.
    Your choices are **Emails and meetings**, **Teams instant
    messages**, and **Teams calls**.

> **More information about this option:** As the nature of the workplace
> evolves, different ways to collaborate gain or lose popularity, doing
> so at different rates among different populations. Some people and
> organizations are more formal in nature -- for example, a legal
> division or HR -- and they might invariably use email. They might also
> tend to message more recipients at once, for which they might prefer
> email.\
> Other people who have a less traditional, more casual, or more
> personal outlook might prefer Teams IMs or calls. Analysts who study
> this communication can reach different inferences based on formal or
> informal communication. Depending on the types of change they want to
> make in the company, they might want to focus the analysis on one
> group of employees or the other.

8.  Under **Select metrics**, select one or more of the available
    metrics. Optionally, you can also edit the **Display name** of these
    metrics; the names of all selected metrics, whether or not you've
    edited them, will appear as column names in the query results.
    (Other metric customization options are not available.)

9.  Under **Select filters**, select the groups of people for whom you
    want to see results. For example, to query about people in the
    engineering department or financial division, set this filter to
    **Domain Equals Engineering** or **Domain Equals Finance**.

10. Under **Organizational data**, select the attributes that you want
    to appear in the results along with the metrics data. You can use
    these attributes to further summarize the results to create analyses
    that compare and contrast the collaboration of different groups in
    the organization.

11. Select **Run**. The query takes a few minutes to complete.

12. On the **Queries \> Results** page, the query status initially shows
    as **Submitted**. After the query status changes to **Succeeded**,
    you can view it or download it (as a .csv file).

> \[!Note\] You can view, copy, export, and visualize query results in
> different ways for different query types. The topic [View, download,
> and export query
> results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md)
> describes how to see and share results. For example, you can [view
> query
> results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md#view-query-results),
> [download and import query
> results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md#download-and-import-query-results),
> and [use an OData feed in Power
> BI](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA query output

The following columns are included in the query results for ONA queries:

-   **Person ID** - De-identified ID number for the person represented
    in that data row.
-   **Date** - The start date of the aggregated output (for example, for
    the week of June 3rd to June 10th, the start date would be the 3rd.
    For a month, it's the first day of the month that your data
    encompasses).
-   **Person attributes** - Attributes about the person supplied through
    the latest organizational (HR) data upload.
-   **Metrics** - Any metrics that you include in the query. For more
    information, see [Organizational network analysis (ONA)
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions#organizational-network-analysis-ona-metrics).

## Related topics

-   [ONA
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-metrics.md)
-   [ONA person-to-person
    queries](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-person-to-person-query.md)
-   [Metric descriptions / ONA
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics)
-   [View, download, and export query
    results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md)
-   [Best practices for
    influencers](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/tutorials/gm-influencer.md)

Organizational network analysis person-to-person queries

Successful employees and teams use their networks to get work done
effectively. Measuring network attributes tells you what network
resources employees can access. Network size is just one attribute of a
collaborative network. Network connections have other qualities that
tell us more about the type of working relationship and what benefit it
might present to the employee and team.

You can use the Organizational network analysis (ONA) queries to qualify
a network connection between two people as a **strong tie**, a **diverse
tie**, or neither.

A generic network tie is defined liberally: two people who've shared at
least two [meaningful
interactions](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/glossary.md#meaningful-interaction-define)
in the last four weeks.

Some network connections represent significantly more close
collaboration than the generic minimum of just two meaningful
interactions. When a network connection represents significantly more
close collaboration time, Workplace Analytics will classify it as either
a **strong tie** or as a **diverse tie**.

The difference between strong ties and diverse ties is determined by how
many other network connections the two individuals have in common.

If the two people have **many** network connections in common, it is
considered a **strong tie**. Strong ties typically indicate shared
membership in a workgroup or team. Groups of employees with many strong
ties often represent highly cohesive units.

If the two people have **few** network connections in common, it is
considered a **diverse tie**. Although the two people work closely with
each other, they do not typically operate in the same circles. Groups of
employees with many diverse ties often represent teams with high
innovative potential, as they are exposed to lots of information outside
of their shared context.

The article will walk you through a query that will return strong and
diverse tie scores; see the following section, [Run a query to determine
strong ties and diverse
ties](#run-a-query-to-determine-strong-ties-and-diverse-ties).

## Run a query to determine strong ties and diverse ties

You can use the tie metrics in ONA person-to-person queries; in this
example procedure, you will query for strong and diverse tie scores.

**Role** - Analyst

1.  In Workplace Analytics, select **Analyze \> Queries**.

2.  Under **Start custom query**, select **Network: Person-to-person**:

-   ![ONA p2p query](media/image2.png){width="3.1979166666666665in"
    height="1.1145833333333333in"}

    ONA p2p query

3.  Select and change **Enter query name here** to a name, and then,
    optionally, enter a description for the query.

4.  For **Group by**, select a time-grouping option: **Month** or
    **Aggregated**. If you choose Monthly, the query results will
    contain one row with data for each month in the time period that you
    chose. If you choose **Aggregated**, the query results will contain
    one row for the entire time period that you chose.

-   \[!Note\] Currently, the only [meeting-exclusion
    > rule](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/meeting-exclusions-intro.md)
    > that can be used with an ONA query is the [Tenant default meeting
    > exclusion
    > rule](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/meeting-exclusion-concept.md#default-meeting-exclusion-rule).
    > As you build your query, this rule is selected by default; it
    > cannot be deselected.

5.  If you want the query to run repeatedly, on a regular schedule,
    select **Auto-refresh**. (For more information, see [Auto-refresh
    option for
    queries](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/query-auto-refresh.md).)

6.  Under **Select network boundary conditions**, define a filter to
    select the measured employees that you want to analyze in this
    query. For example, you can use the filters of this step to narrow
    the scope to a division or a group. If you skip this (optional)
    step, all measured employees will remain eligible for analysis.

> **More information about this option:** If you run this query on the
> entire company, the results will be based on all collaborations across
> the company. If this is your goal, you can retain the default search
> range, which is unlimited. But your goal might be to understand
> connectivity for a specific group of people, based on collaboration
> happening exclusively within that group. In this case, limit the query
> to search only within a particular division or group.

### Under Select collaboration types, specify the types of collaboration activities that you want to include in your analysis. Your choices are Emails and meetings, Teams instant messages, and Teams calls.

> **More information about this option:** As the nature of the workplace
> evolves, different ways to collaborate gain or lose popularity, doing
> so at different rates among different populations. Some people and
> organizations are more formal in nature -- for example, a legal
> division or HR -- and they might invariably use email. They might also
> tend to message more recipients at once, for which they might prefer
> email. Other people who have a less traditional, more casual, or more
> personal outlook might prefer Teams IMs or calls.
>
> Analysts who study this communication can reach different inferences
> based on formal or informal communication. Depending on the types of
> change they want to make in the company, they might want to focus the
> analysis on one group of employees or the other.

8.  Under **Select metrics**, select **Strong and Diverse tie scores**.

9.  Under **Select filters**, select the groups of people for whom you
    want to see results. This section offers two optional filters, one
    for selecting "tie-origin" employees, and the other for selecting
    "tie-destination" employees. For more information, see [Select
    filters](#select-filters).

10. Under **Organizational data**, select the attributes that you want
    to appear in the results along with the metrics data. You can use
    these attributes to further summarize the results to create analyses
    that compare and contrast the collaboration of different groups in
    the organization.

11. Select **Run**. The query takes a few minutes to complete.

12. On the **Queries \> Results** page, the query status initially shows
    as **Submitted**. After the query status changes to **Succeeded**,
    you can view it or download it (as a .csv file).

> \[!Note\] You can view, copy, export, and visualize query results in
> different ways for different query types. The topic [View, download,
> and export query
> results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md)
> describes how to see and share results. For example, you can [view
> query
> results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md#view-query-results),
> [download and import query
> results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md#download-and-import-query-results),
> and [use an OData feed in Power
> BI](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA person-to-person query output

The query results show the quality of the relationship between two
specific (but de-identified) people. Each row shows the information for
a pair of people between whom a tie exists, or existed, over the time
period of the query.

The following columns appear, from left to right, in the query results
for ONA person-to-person queries:

### The first two columns identify the initiator of the tie

![first columns -- A and
B](media/image3.png){width="5.833333333333333in"
height="0.9004472878390202in"}

first columns -- A and B

*Query results example: Columns A and B*

The column names for these attributes are organizational attribute names
with the prefix \_TieOrigin\_\_. These first two columns appear
automatically:

-   TieOrigin\_[**PersonId**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#personid-define) -
    A de-identified ID number for the person represented in that data
    row. You do not select this column as you build a query; it appears
    automatically.
-   TieOrigin\_[**GroupId**](#groupid-define) - A de-identified ID
    number of the group in the organization to which the person belongs.
    This column can help you discover Strong ties in a team to
    understand how cohesive it is and also discover Diverse ties in a
    team to understand whether there are opportunities for novel
    information to flow into the team. You do not select this column as
    you build a query; it appears automatically.

### The next columns describe the initiator of the tie

![first columns -- C through E](media/image4.png){width="5.2in"
height="2.0in"}

first columns -- C through E

*Query results example: Columns C through E*

The column names for these attributes are organizational attribute names
with the prefix \_TieOrigin\_\_. These three columns represent
attributes that you selected while building the query:

-   TieOrigin\_[**FunctionType**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#functiontype-define).
    The job function that the employee performs.
-   TieOrigin\_[**LevelDesignation**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#leveldesignation-define).
    The employee's level within the organization.
-   TieOrigin\_[**Organization**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#organization-define).
    The internal organization that the employee belongs to.

### The next two columns identify the other participant in the tie

![next columns -- F and G](media/image5.png){width="5.833333333333333in"
height="1.0637248468941383in"}

next columns -- F and G

*Query results example: Columns F and G*

The column names for these attributes are organizational attribute names
with the prefix \_TieDestination\_\_. These first two columns for this
person appear automatically:

-   TieDestination\_[**PersonId**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#personid-define) -
    A de-identified ID number for the person represented in that data
    row. You do not select this column as you build a query; it appears
    automatically.
-   TieDestination\_[**GroupId**](#groupid-define) - A de-identified ID
    number of the group in the organization to which the person belongs.
    This column can help you discover Strong ties into another team to
    understand how well connected one is with that team and also
    discover Diverse ties in another team to understand opportunities
    for novel information to flow from that team. You do not select this
    column as you build a query; it appears automatically.

### The next columns describe the other participant in the tie

![next columns -- H through
J](media/image6.png){width="5.833333333333333in"
height="1.83082895888014in"}

next columns -- H through J

*Query results example: Columns H through J*

The column names for these attributes are organizational attribute names
with the prefix \_TieDestination\_\_. These three columns represent
attributes that you selected while building the query:

-   TieDestination\_[**FunctionType**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#functiontype-define).
    The job function that the employee performs.
-   TieDestination\_[**LevelDesignation**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#leveldesignation-define).
    The employee's level within the organization.
-   TieDestination\_[**Organization**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#organization-define).
    The internal organization that the employee belongs to.

### The last columns give the results

![last columns -- K through
O](media/image7.png){width="5.833333333333333in"
height="1.8436450131233595in"}

last columns -- K through O

*Query results example: Columns K through O*

-   **Date** - The start date of the aggregated output (for example, for
    the week of June 3rd to June 10th, the start date would be the 3rd.
    For a month, it's the first day of the month that your data
    encompasses).

-   **Metrics** - The metrics that you included in the query. For more
    information, see [Metric descriptions / ONA
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics).

```{=html}
<!-- -->
```
-   The results for this query type always include the following
    metrics:

    -   [**StrongTieScore**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#strong-tie-score-define) -
        Sort on this column to find employees with the highest scores.
        These high scores represent strong ties between the two
        individuals.
    -   [**DiverseTieScore**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#diverse-tie-score-define) -
        Sort on this column to find employees with the highest scores.
        These high scores represent diverse ties between the two
        individuals.
    -   [**StrongTieType**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#strong-tie-type-define) -
        This column is present to help analysts quickly find the
        strongest ties. It contains values of 0, 1, or 2, based on the
        distribution of StrongTieScore. The values indicate the
        following:
        -   **1:** This row clearly indicates a strong tie --- 35th
            percentile and above, by strength.
        -   **2:** This row indicates a tie that is significant but less
            strong: at or above the 30th percentile but below the 35th
            percentile.
        -   **0:** This row indicates a tie that is not that strong:
            below the 30th percentile.
    -   [**DiverseTieType**](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#diverse-tie-type-define) -
        This column is present to help analysts quickly find the most
        diverse ties. It contains values of 0, 1, or 2, based on the
        distribution of DiverseTieScore. The values indicate the
        following:
        -   **1:** This row clearly indicates a diverse tie --- 50th
            percentile and above, by diversity.
        -   **2:** This row indicates a tie that is significant but less
            diverse: at or above the 45th percentile but below the 50th
            percentile.
        -   **0:** This row indicates a tie that is not that diverse:
            below the 45th percentile.

## Select filters

In step 6 of the procedure [Run a query to determine strong ties and
diverse ties](#run-a-query-to-determine-strong-ties-and-diverse-ties),
you select filters to determine which person-to-person scores you want
to see in the query results. Before you do this, it's good to understand
the concepts of "tie-origin" and "tie-destination."

Two employees have a connection (or "tie") that this query can report on
if they have collaborated in a way that Workplace Analytics can
quantify. Collaborations include actions such as the sending and
receiving of emails, meeting invitations, and calls or chats in Teams.
In each of these cases, one employee initiated the collaboration action
(for example, sent the email) and the other employee (or employees)
participated in the action. "Tie-origin" refers to the initiator or
originator, and "tie-destination" refers to the other participants.

The **Select filters** section offers two identical filters, one for the
left side of the tie (the tie origin) and another for the right side of
the tie (the tie destination). Both filters are optional.

![Select filters area](media/image8.png){width="5.833333333333333in"
height="1.8769706911636046in"}

Select filters area

If you specify only the tie-origin filter, the query results will
include all rows that match the tie-origin PersonId that you specified
in the filter. Each row depicts a tie between the employee with that
PersonId and another employee who was the destination of the tie.

If you specify only the tie-destination filter, the query results will
include all rows that match tie-destination PersonId that you specified
in the filter. Each row depicts a tie between the employee with that
PersonId and another employee who was the origin of the tie.

If both tie origin and tie destination filters are specified, the query
returns only those rows that match the tie-origin PersonID in the
tie-origin filter AND the tie-destination PersonID in the
tie-destination filter.

### Derived attributes

The following organizational attribute, GroupId, is used in this query
type. Note that this attribute is not among the organization data that
[admins upload to Workplace
Analytics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/upload-organizational-data-1st.md).
Rather, it is derived from the
[ManagerId](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/setup/prepare-organizational-data.md#managerid-define)
attribute, which *is* in the organizational hierarchy data that admins
upload.

  Attribute (column header)   Description
  --------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  GroupId                     A unique, de-identified ID number that identifies a group. All members of a team who report to the same person in the organizational hierarchy have the same GroupId. Analysts can use the GroupId column to aggregate members of a team.

## Related topics

-   [ONA
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-metrics.md)
-   [ONA person
    queries](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-person-query.md)
-   [Metric descriptions / ONA
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics)
-   [View, download, and export query
    results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md)

ONA metrics

The ONA query types (ONA person query) and ONA person-to-person query)
use a selection of connectivity metrics to help analysts investigate the
effects and value of relationships within and beyond groups. These
connectivity relationships are of two broad types, *influence* and
*ties*. Persons in a company can have varying amounts of network
influence over their co-workers; because influencers can act as change
agents, leveraging them can help leaders implement change. Ties reflect
connections between people and are of two types, *diverse* and *strong*;
evaluating these ties can help you determine aspects such as team
alignment and potential for the flow of information and ideas.

You can find the basic definitions of the connectivity metrics in
[Workplace Analytics metrics / ONA
metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics):

  Metric                                                                                                                                                                                Available in this query type
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------
  [Diverse tie score](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#diverse-tie-score-define)                               ONA person-to-person query
  [Diverse tie type](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#diverse-tie-type-define)                                 ONA person query
  [Diverse ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#diverse-ties-define)                                         ONA person query
  [Influence](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#influence-define)                                               ONA person query
  [Influence rank](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#influence-rank-define)                                     ONA person query
  [Manager overlapping strong ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#manager-overlapping-strong-ties-define)   ONA person query
  [Manager unique strong ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#manager-unique-strong-ties-define)             ONA person query
  [Strong tie score](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#strong-tie-score-define)                                 ONA person-to-person query
  [Strong tie type](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#strong-tie-type-define)                                   ONA person query
  [Strong ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared Documents/use/metric-definitions.md#strong-ties-define)                                           ONA person query

The following sections describe the connectivity metrics in greater
detail. They are divided into two groups:

-   [Influence metrics: influence and influence-rank](\l)
-   [Tie metrics: strong and diverse ties](\l)

## Influence metrics: influence and influence rank

It's frequently necessary to implement changes within organizations,
whether this be introducing new procedures or rolling out new systems or
technology. The traditional top-down method of using formal authority to
drive change -- perhaps starting with mass emails -- it's not always the
most effective way. It might fail for any of several reasons including
company culture, technical challenges, or problems with personality.

Instead, a more successful strategy uses change agents, who are
influential, well-connected people in different levels of your company,
not just at the top. Beyond an organization's formal hierarchy, informal
networks of people can exert influence within those networks and between
them. The most influential people have large personal networks with
above-average numbers of relationships with their colleagues. This query
lets you visualize these relationships through various metrics that
reflect influence directly (with *influence* and *influence rank*) and
indirectly (with various measures of ties to people outside your team.)

In other words, to help implement change, it pays to know which people
have the most ties and the most influence. The Workplace Analytics
Organizational network analysis (ONA) queries were designed for this
purpose. They can help you find out who the best-connected people are in
the company based on their collaboration characteristics.

After you learn who the best connected people are in the company,
division, or other group, you can act on the likelihood that these
people can effectively connect within or across groups and become
efficient drivers of change.

Also see [How Workplace Analytics calculates
influence](#X2039c9ad4ded19cc8798cbdf1612e7ef67b8f34).

### Calculation of influence metrics

The terminology in the following description comes from graph theory. In
graph theory, a "node" (also called a "vertex") is an object that can
relate to other nodes -- other objects -- in the graph. This model
becomes useful when we extend it to the workplace, where a "node"
represents a person who has connections to co-workers and others.

Influence indicates a node's potential influence on opinions of the
network or an estimate of social status. Essentially, it uses the number
and strength of connections coming into a node to rank the nodes. The
values are between 0 and 1.

#### Determine node rank for influence metrics

The most meaningful information to glean from Influence is the rank of
the nodes. You can do this by using either of the two pertinent ONA
metrics, Influence and Influence rank.

-   Use [Influence
    rank](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#influence-rank-define).
    This metric assigns to each node a number that corresponds to their
    relative influence, with the lowest number (1) for the most
    influential node. You can use this metric, for example, to obtain a
    simple ranked list or to evaluate whether a node's network influence
    is changing over time.

-   Use
    [Influence](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#influence-define).
    You use this metric in a more nuanced way than you'd use Influence
    rank. For example, assume that node A has an Influence of 0.6 and
    node B has an Influence of 0.3. You can accurately assume that node
    A is a more influential than node B, because node A ranks higher
    than node B. However, you cannot assume node A is twice as
    influential as node B because the values indicate a ranking or
    source of influence, not the amount of influence. The calculations
    for Influence use the relative collaboration time between
    individuals as the strengths of the connections for a person's
    influence measure.

## Tie metrics: strong and diverse ties

You can use the Organizational network analysis (ONA) queries to qualify
a network connection between two people as a [strong
tie](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/strong-ties-define),
a [diverse
tie](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/diverse-ties-define),
or neither.

If two people have many network connections in common, they are
considered to have a *strong tie*. Strong ties typically indicate shared
membership in a workgroup or team. *Diverse ties* reflect the number of
diverse or novel connections that a person has across the company, based
on the time invested by the person with their connection.

> \[!Note\] When Workplace Analytics evaluates a network connection, it
> can only classify that connection as a strong tie or a diverse tie if
> it is between two [measured
> employees](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/glossary.md#measured-employees).

### Distance is a factor

You can derive more value from strong and diverse ties based on
distance. In the following descriptions, "immediate group" refers to one
manager and their direct reports.

-   You could have strong ties that are close: These are strong ties
    with people in your immediate group. These ties are necessary for
    the promotion of overall team efficiency, team effectiveness,
    knowledge transfer, and best-practice development.
-   You could have strong ties that are distant: These are strong ties
    with people outside your immediate group. These ties are good for
    evangelizing and embedding fresh or innovative ideas. However, such
    ties are likely not sustainable because of time demand for deep and
    constant engagement.
-   You could have diverse ties that are close: These are diverse ties
    with people in your immediate group. These ties might appear as a
    result of use cases internal to the group; they can also indicate
    disengagement within the group.
-   You could have diverse ties that are distant: These are diverse ties
    with people outside your immediate group. These ties are good for
    evangelizing and embedding fresh or innovative ideas. The presence
    of such ties in manager networks are considered key for driving
    innovation and creativity in and among teams.

### Ties are directional

Ties (both Strong and Diverse) are directional in nature. If a
Sara-to-Isaiah tie is strong, it does not necessarily follow that the
Isaiah-to-Sara tie is also strong. The strength depends on the
contribution that each person makes. For example, a greater contribution
from Isaiah toward his relationship with Sara makes it more likely that
Isaiah has a Strong tie with Sara, but it does not directly increase the
likelihood of a tie in the opposite direction.

Another example: A manager's tie to a direct report might be Strong, but
not necessarily vice versa.

### Examples of strong ties and diverse ties

#### Example: strong ties

John and Sally on peers on the same team working on the same project.
They collaborate with each other often. They exchange emails several
times a day and meet in various forums several times a week. Due to the
very frequent nature of their interaction, a Strong tie very likely
exists between them. This Strong tie is made even stronger by the fact
that John and Sally share a [common
network](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/glossary.md#common-network).
Each has their own set of people with whom they work and meet. These
sets of people overlap, which creates an indirect bonding or
relationship --- a common network --- which, in turn, strengthens the
Strong tie between John and Sally.

Note that each person's contribution counts. See [Ties are
directional](#ties-are-directional).

#### Example: diverse ties

Preeti is a research scientist in an R&D department, and Rahul is a
supply-chain logistics manager who works in the shipping department of
the same company. They met at a Diversity & Inclusion virtual event at
the company a few months ago, and are now connected to each other on
LinkedIn. They share no commonality in their job functions and there is
limited opportunity for them to interact with each other in small-group
settings.

Both Preeti and Rahul have their own connections, and there is no
overlap in people across their connections. Due to these circumstances,
a Diverse tie very likely exists between them. Recently, Preeti liked an
article on climate science on LinkedIn. Since Preeti is in Rahul's
LinkedIn network, Rahul got to read this article, which he otherwise
might have missed. As shown here, Diverse relationships such as the one
between Preeti and Rahul promote sharing of varied and non-typical
information.

Note that each person's contribution counts. See [Ties are
directional](#ties-are-directional).

#### Example: strong ties and diverse ties

Mark and Matt work as engineers in the same large development team.
However, they work on different products. Due to the nature of their
roles, they are expected to collaborate closely with each other, and
they do these in regular cross-group sync-up meetings and occasional
emails. Based on these frequent collaboration events, a Strong tie could
exist between them.

Now, since they work on separate products, they tend to work with
different people within their own workgroups. This results in some
amount of fresh information flowing to each other through their own
networks. For this reason, it is possible that a Diverse tie could also
exist between the two to some degree.

### Calculation of tie metrics

-   [Diverse
    ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#diverse-ties-define)
    -- Diverse ties reflect the number of diverse or novel connections
    that a person has across the company, based on the time invested by
    the person with their connection. This metric also takes into
    account network differences that exist between the two people where
    both people are investing time. Diverse ties are both directional
    and asymmetrical. For example, if A has a diverse tie with B if A
    either collaborates a lot with B or a lot with a network that they
    have in common with B.
-   [Strong
    ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#strong-ties-define)
    -- If two people have many network connections in common, they are
    considered to have a strong tie. Strong ties typically indicate
    shared membership in a workgroup or team. Like diverse ties, strong
    ties are directional. The strength of a person's tie depends on the
    contribution that the person makes in the relationship with the
    other person. This query also offers the following metrics that
    derive from the strong-tie metric:
    -   [Manager overlapping strong
        ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#manager-overlapping-strong-ties)
        -- Measure the number of strong ties that both a manager has and
        that their direct reports have in common with a manager.
    -   [Manager unique strong
        ties](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#manager-unique-strong-ties-define)
        -- Measure the number of strong ties that are unique in the
        manager's network and subtract from it the number of strong ties
        that their direct reports have.

## Frequently asked questions

The following questions and answers refer to metrics; you can find their
definitions in [Metric descriptions / Person
metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#person-metrics)
and in [Metric descriptions / ONA
metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics).

**Q1. What is the difference between "strong ties" and "Internal network
size"?**

A1. Strong ties takes the network commonality that exists between the
two people into account, a situation in which both people are investing
time together or enabling other forms of bonding. Strong ties also gives
more weight to meetings-based collaboration than to email. This is
because meetings are more inter-personal in nature and enable direct
person-to-person engagement, which results in a formalized engagement.
Email-based collaboration doesn't translate into such an interpersonal
engagement.

Internal network size simply means the number of connections a person
has within the company, based on the number of [meaningful
interactions](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/glossary.md#meaningful-interaction-define)
the person has with their connections. Strong ties means the number of
tight-knit, engaged connections a person has within the company, based
on the time that the person invested with their connections.

In summary: Strong ties differs from Internal network size in that they
reflect the number of a person's connections based on the quality of the
engagement that exists between two people.

**Q2. When should you use "strong ties" and when "Internal network
size"?**

A2. Let's say you need nothing more than a quantitative number of
connections a person has within the company. Also, you have no objection
to including unlicensed users even though restricting your query to
licensed users would return richer data. In this case, feel free to
query for Internal network size.

However, if you restrict your query to licensed users, we recommended
that you query for strong ties because doing so gives you a more
realistic and qualitative view of engaged connections.

**Q3. When should you use "strong ties" and when "External network
size"?**

A3. Strong ties currently does not consider connections that a person
has outside the company. To obtain the number of connections a person
has outside the company, you can use External network size.

**Q4. What is the difference between "diverse ties" and "Networking
outside organization"?**

A4. Diverse ties returns the number of diverse or novel connections a
person has across the company, based on the time invested by the person
with their connection. Diverse ties also looks at network differences
that exists between the two people where both people are investing time,
enabling other forms of indirect sourcing of novel information. Person A
can become a good source of diverse information for Person B if Person A
does not spend too much time with Person B or if their [common
network](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/glossary.md#common-network)
has minimal overlap.

In contrast, Networking outside organization returns the number of
distinct organizations within the company a person has connections to,
based on the number of [meaningful
interactions](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/glossary.md#meaningful-interaction-define)
the person has with their connection. This metric quantifies connections
at the organization attribute level.

Therefore, unlike Networking outside organization, which returns
connections only at the organization attribute level (a very high
level), diverse ties returns the number of connections based on the
*quality* of the engagement and the *variety* of information that can
potentially be conveyed through the connection. Also, diverse ties can
span any organizational attribute, which lets you more flexibly locate
such ties anywhere in the company.

**Q5. When should you use "diverse ties" and when "Networking outside
organization"?**

A5. If you need nothing more than the number of connections a person has
at the organization attribute level within the company, regardless of
whether connections include licensed users or not, use Networking
outside organization.

But if you restrict your query to licensed users, use diverse ties to
obtain a more realistic and qualitative view of the variety of
connections with potential for diverse or novel information. Diverse
ties also allows you to look at connections at any organizational
attribute level, which gives you more useful results than Networking
outside organization would provide.

**Q6. When should you use "diverse ties" and when "Networking outside
company"?**

A6. Diverse ties is internal only: It does not consider connections that
a person has outside the company. Networking outside company counts not
the number of *ties* outside the company but rather the number of
external *unique domains* to which you are networked.

## Related topics

-   [ONA person
    queries](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-person-query.md)
-   [ONA person-to-person
    queries](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/General/ona-person-to-person-query.md)
-   [Metric descriptions / ONA
    metrics](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/metric-definitions.md#organizational-network-analysis-ona-metrics)
-   [View, download, and export query
    results](https://microsoft.sharepoint-df.com/teams/WPADocumentatoinTeam/Shared%20Documents/use/view-download-and-export-query-results.md)

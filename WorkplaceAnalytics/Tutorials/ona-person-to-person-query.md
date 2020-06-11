---

title: Organizational network analysis (ONA) person-to-person queries 
description: Describes how to use Organizational network analysis (ONA) person-to-person queries in Workplace Analytics to determine the "strong ties" and "diverse ties" metrics that measure ties between individuals in your organization
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Organizational network analysis (ONA) person-to-person queries

Measuring the quality, or strength, of an employee’s connections can help improve organizational functioning in various ways. For example, a manager’s effectiveness improves if the manager has high network strength. Such managers have tight connections with their direct reports, they tend to have strong peer connections, and they have the right kind of connections outside the team. Well-connected managers know how to point inquisitive employees to the right people in their network, and makes it more likely that these employees become star performers, which of course reflects positively on the manager. 

As for non-managers, the most effective employees also excel in part because of strong and rich networks. When high performers have broader internal networks, it indicates that they have relationships across a more diverse set of people, which promotes system-level thinking and problem solving. 

The ONA person-to-person query measures the strength of connections through these two metrics:

 * The **Strong ties** metric measures how many strong and tight engagements the person has had. For example, a "strong tie" between a manager and a direct report reflects the amount of direct collaboration they have over time. Typically, a person has only a few strong ties because such ties take more effort to maintain. 
 
 * The **Diverse ties** metric measures how varied and how broad the person's connections are. A person need not have much direct collaboration with their diverse ties, so it’s easy to have more diverse ties than strong ties. Diverse ties present good sources of fresh and varied information from across the company.

## Run a query to determine Strong ties and Diverse ties

**Role:** analyst

1.	In Workplace Analytics, select **Analyze > Queries**.

2.	Under **Start custom query**, select **Network: Person-to-person**:

    ![ONA p2p query](../images/wpa/tutorials/ona-p2p-query.png)

3.	Select and change **Enter query name here** to a name, and then enter a description for the query.
4.	For **Group by**, select a time-grouping option: **Monthly** or **Aggregated**. If you choose Monthly, the query results will contain one row with data for each month in the time period that you chose. If you choose **Aggregated**, the query results will contain one row for the entire time period that you chose. 

    > [!Note] 
    > Currently, the only [meeting-exclusion rule](meeting-exclusions-intro.md) that can be used with an ONA query is the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule). As you build your query, this rule is selected by default; it cannot be deselected.   

5.	Under **Select metrics**, select **Strong and Diverse tie scores**. 
6.	Under **Select filters**, select the groups of people for whom you want to see results. For example, to query about people in the engineering department or financial division, set this filter to **Domain Equals Engineering** or **Domain Equals Finance**. For more information, see [Select filters](#select-filters).
7.	Under **Organizational data**, select the attributes that you want to appear in the results along with the metrics data. You can use these attributes to further summarize the results to create analyses that compare and contrast the collaboration of different groups in the organization.
8.	Select **Run**. The query takes a few minutes to complete. 
9.	On the **Queries > Results** page, the query status initially shows as **Submitted**. After the query status changes to **Succeeded**, you can view it or download it (as a .csv file).

> [!Note] 
> You can view, copy, export, and visualize query results in different ways for different query types. The topic [View, download, and export query results](../use/view-download-and-export-query-results.md) describes how to see and share results. For example, you can [view query results](../use/view-download-and-export-query-results.md#view-query-results), [download and import query results](../use/view-download-and-export-query-results.md#download-and-import-query-results), and [use an OData feed in Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA person-to-person query output

The query results show the quality of the relationship between two specific (but de-identified) people. Each row shows the information for a pair of people between whom a tie exists, or existed, over the time period of the query. 

![ONA p2p query](../images/wpa/tutorials/ona-p2p-query-results-2.png)

The following columns appear, from left toright, in the query results for ONA person-to-person queries:

* **TieOrigin_PersonId.** De-identified ID number for the person represented in that data row.
* **Person attributes.** Organizational attributes about the person who was identified by TieOrigin_PersonId. These are the organizational attributes that you selected as you built the query. The column names for these attributes are "TieOrigin_" followed by the organizational attribute name. The example results show the columns TieOrigin_FunctionType, TieOrigin_Organization, and Tie_Origin_LevelDesignation.  
* **TieDestination_PersonId.** De-identified ID number for the person who has a strong or diverse tie to the person represented by TieOrigin_PersonId. 
* **Person attributes.** Organizational attributes about the person who was identified by TieDestination_PersonId. These are the organizational attributes that you selected as you built the query. The column names for these attributes are "TieDestination_" followed by the organizational attribute name. The example results show the columns TieDestination_FunctionType, TieDestination_Organization, and Tie_Destination_LevelDesignation.  
* **Date.** The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it's the first day of the month that your data encompasses).
* **Metrics.** The metrics that you included in the query. For more information, see [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics). 
   
   The results for this query type always include the following metrics:

  * **StrongTieScore.** Sort on this column to find employees with the highest scores. These high scores represent strong ties between the two individuals. <!--In the example results shown, sorting on this column showed that one director in the financial-planning organization within Sales has, not surprisingly, a very strong tie with a manager in the financial-planning organization within Sales. It could be that the manager reports to the director and this is a natural, even expected, relationship.--> 
  * **DiverseTieScore.** Sort on this column to find employees with the highest scores. These high scores represent diverse ties between the two individuals.  
  * **StrongTieType.** This column is present to help analysts quickly find the strongest ties. It contains values of 0, 1, or 2. The value 1 indicates that this row clearly indicates a strong tie -– roughly, the top 10% of ties, by strength. "2" indicates a tie that is significant but less strong. "0" indicates a tie that's not that strong. 
  * **DiverseTieType.** This column is present to help analysts quickly find the most diverse ties. IT contains values of 0, 1, or 2. The value 1 indicates that this row clearly indicates a diverse tie –- roughly, the top 10% of ties, by diversity. "2" indicates a tie that is significant but less diverse. "0" indicates a tie that’s not that diverse.

## Select filters

In step 6 of the preceding procedure, you select filters to determine which person-person scores you want to see in the query results. Before you do this, it's good to understand the concepts of "tie-origin" and "tie-destination":

Two employees have a connection (or "tie") that this query can report on if they have collaborated in a way that Workplace Analytics can quantify. Collaborations include actions such as the sending and receiving of emails, meeting invitations, and calls or chats in Teams. In each of these cases, one employee initiated the collaboration action (for example, sent the email) and the other employee (or employees) participated in the action. "Tie-origin" refers to the initiator or originator, and "tie-destination" refers to the other participants. 

The **Select filters** section offers two identical filters, one for the left side of the tie (the tie origin) and another for the right side of the tie (the tie destination). Both filters are optional. 

![ONA p2p query](../images/wpa/tutorials/ona-p2p-filters.png)

If you specify only the tie-origin filter, the query results will include
all rows that match the tie-origin PersonId that was specifed in the filter. Each row depicts a tie between the employee with that PersonId and another employee who was the destination of the tie.  

If you specify only the tie-destination filter, the query results will include all rows that match tie-destination PersonId that was specified in the filter. Each row depicts a tie between the employee with that PersonId and another employee who was the origin of the tie.  

If both tie origin and tie destination filters are specified, the query returns only those rows that match the tie-origin PersonID in the tie-origin filter AND the tie-destination PersonID in the tie-destination filter.

## Related topics

[ONA person queries](ona-person-query.md)

[Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics)

[View, download, and export query results](../use/view-download-and-export-query-results.md)

[Best practices for influencers](https://review.docs.microsoft.com/en-us/Workplace-Analytics/tutorials/gm-influencer?branch=pas-sr-ona-flexible-query)


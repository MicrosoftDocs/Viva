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

 * The **Strong ties** metric measures how many strong and tight engagements you've had, based on the amount of direct collaboration you have over time AND the amount of collaboration you have with the people in your common network. 
 
   For example, a "strong tie" between a manager and a direct report reflects the amount of direct collaboration they have over time and the amount of interactions they have with the same set of people who exist in their networks. Typically, a person has only a few strong ties because strong ties take more effort to maintain.

   See [Examples of Strong ties and Diverse ties](#examples-of-strong-ties-and-diverse-ties).
 
 * The **Diverse ties** metric measures how varied and how broad your connections are, based on the amount of direct collaboration you have over time AND the amount of collaboration you have with people NOT in your common network. 
 
   Diverse ties present good sources of fresh and varied information from across the company, especially because access to a set of completely different people in your networks increases your access to new information. Because you need not have much direct collaboration with your diverse ties, it’s easy to have more diverse ties than strong ties. 
   
   Diverse ties not only expose you to varied information, they also help the dissemination of such new information through the network.

   See [Examples of Strong ties and Diverse ties](#examples-of-strong-ties-and-diverse-ties).

> [!Note] 
> * Strong ties and diverse ties are computed and reported for licensed users only.
> * Strong ties pay special attention to meeting-based collaboration. This is because meetings are considered more important than email for establishing a true connection. Similarly, for email-based collaboration, bidirectional emails are considered more important than one-way emails.

## Run a query to determine strong ties and Diverse ties

**Role:** analyst

1.	In Workplace Analytics, select **Analyze > Queries**.

2.	Under **Start custom query**, select **Network: Person-to-person**:

    ![ONA p2p query](../images/wpa/tutorials/ona-p2p-query.png)

3.	Select and change **Enter query name here** to a name, and then enter a description for the query.
4.	For **Group by**, select a time-grouping option: **Monthly** or **Aggregated**. If you choose Monthly, the query results will contain one row with data for each month in the time period that you chose. If you choose **Aggregated**, the query results will contain one row for the entire time period that you chose. 

    > [!Note] 
    > Currently, the only [meeting-exclusion rule](meeting-exclusions-intro.md) that can be used with an ONA query is the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule). As you build your query, this rule is selected by default; it cannot be deselected. 

5. If you want the query to run repeatedly, on a regular schedule, select **Auto-refresh**. (For more information, see [Auto-refresh option for queries](query-auto-refresh.md).) 
6.	Under **Select metrics**, select **Strong and Diverse tie scores**. 
7.	Under **Select filters**, select the groups of people for whom you want to see results. This section offers two optional filters, one for selecting "tie-origin" employees, and the other for selecting "tie-destination" employees. For more information, see [Select filters](#select-filters).
8.	Under **Organizational data**, select the attributes that you want to appear in the results along with the metrics data. You can use these attributes to further summarize the results to create analyses that compare and contrast the collaboration of different groups in the organization.
9.	Select **Run**. The query takes a few minutes to complete. 
10.	On the **Queries > Results** page, the query status initially shows as **Submitted**. After the query status changes to **Succeeded**, you can view it or download it (as a .csv file).

> [!Note] 
> You can view, copy, export, and visualize query results in different ways for different query types. The topic [View, download, and export query results](../use/view-download-and-export-query-results.md) describes how to see and share results. For example, you can [view query results](../use/view-download-and-export-query-results.md#view-query-results), [download and import query results](../use/view-download-and-export-query-results.md#download-and-import-query-results), and [use an OData feed in Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA person-to-person query output

The query results show the quality of the relationship between two specific (but de-identified) people. Each row shows the information for a pair of people between whom a tie exists, or existed, over the time period of the query.

The following columns appear, from left to right, in the query results for ONA person-to-person queries:

### The first columns describe the initiator of the tie

![ONA p2p query](../images/wpa/tutorials/columns-1-4.png)

_Query results example: Columns A through D_

* **TieOrigin_PersonId.** De-identified ID number for the person represented in that data row.
* **Person attributes.** Organizational attributes about the person who was identified by TieOrigin_PersonId. These are the organizational attributes that you selected as you built the query. In this example, we selected three such attributes. 

   The column names for these attributes are the organizational attribute name prefixed with _TieOrigin__. In this example: 
    * _TieOrigin_FunctionType_
    * _TieOrigin_LevelDesignation_
    * _TieOrigin_Organization_

### The next columns describe the other participant in the tie    

![ONA p2p query](../images/wpa/tutorials/columns-5-8.png)

_Query results example: Columns E through H_

* **TieDestination_PersonId.** De-identified ID number for the person with whom the person represented by TieOrigin_PersonId has a strong or diverse tie. 
* **Person attributes.** Organizational attributes about the person who was identified by TieDestination_PersonId. These are the organizational attributes that you selected as you built the query. In this example, we selected three such attributes. 

   The column names for these attributes are the organizational attribute name prefixed with _TieOrigin__. In this example: 
    * _TieDestination_FunctionType_
    * _TieDestination_LevelDesignation_
    * _TieDestination_Organization_

### The last columns give the results

![ONA p2p query](../images/wpa/tutorials/columns-9-13.png)

_Query results example: Columns I through M_

* **Date.** The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it's the first day of the month that your data encompasses).
* **Metrics.** The metrics that you included in the query. For more information, see [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics). 
   
   The results for this query type always include the following metrics:

  * **StrongTieScore.** Sort on this column to find employees with the highest scores. These high scores represent strong ties between the two individuals. 
  * **DiverseTieScore.** Sort on this column to find employees with the highest scores. These high scores represent diverse ties between the two individuals. 
  * **StrongTieType.** This column is present to help analysts quickly find the strongest ties. It contains values of 0, 1, or 2, based on the distribution of StrongTieScore. The values indicate the following:
    * **1:** This row clearly indicates a strong tie &mdash; 20th percentile and above, by strength. 
    * **2:** This row indicates a tie that is significant but less strong: between the 10th and 20th percentiles.
    * **0:** This row indicates a tie that is not that strong: 10th percentile and below.  
  * **DiverseTieType.** This column is present to help analysts quickly find the most diverse ties. It contains values of 0, 1, or 2, based on the distribution of DiverseTieScore. The values indicate the following:
    * **1:** This row clearly indicates a diverse tie &mdash; 20th percentile and above, by diversity. 
    * **2:** This row indicates a tie that is significant but less diverse: between the 10th and 20th percentiles.
    * **0:** This row indicates a tie that is not that diverse: 10th percentile and below. 

## Select filters

In step 6 of the procedure [Run a query to determine Strong ties and Diverse ties](#run-a-query-to-determine-strong-ties-and-diverse-ties), you select filters to determine which person-to-person scores you want to see in the query results. Before you do this, it's good to understand the concepts of "tie-origin" and "tie-destination":

Two employees have a connection (or "tie") that this query can report on if they have collaborated in a way that Workplace Analytics can quantify. Collaborations include actions such as the sending and receiving of emails, meeting invitations, and calls or chats in Teams. In each of these cases, one employee initiated the collaboration action (for example, sent the email) and the other employee (or employees) participated in the action. "Tie-origin" refers to the initiator or originator, and "tie-destination" refers to the other participants. 

The **Select filters** section offers two identical filters, one for the left side of the tie (the tie origin) and another for the right side of the tie (the tie destination). Both filters are optional. 

![ONA p2p query](../images/wpa/tutorials/ona-p2p-filters.png)

If you specify only the tie-origin filter, the query results will include all rows that match the tie-origin PersonId that you specifed in the filter. Each row depicts a tie between the employee with that PersonId and another employee who was the destination of the tie. 

If you specify only the tie-destination filter, the query results will include all rows that match tie-destination PersonId that you specified in the filter. Each row depicts a tie between the employee with that PersonId and another employee who was the origin of the tie. 

If both tie origin and tie destination filters are specified, the query returns only those rows that match the tie-origin PersonID in the tie-origin filter AND the tie-destination PersonID in the tie-destination filter.

## Additional notes 

You can derive additional value from strong and diverse ties based on distance. In the following descriptions, "immediate group" refers to one manager and their direct reports. 

You could have strong ties that are close: These are strong ties with people in your immediate group. These ties are necessary for the promotion of overall team efficiency, team effectiveness, knowledge transfer, and best-practice development. 

You could have strong ties that are distant: These are strong ties with people outside your immediate group. These ties are good for evangelizing and embedding fresh or innovative ideas. However, such ties are likely not sustainable because of time demand for deep and constant engagement. 

You could have diverse ties that are close: These are diverse ties with people in your immediate group. These ties might appear as a result of use cases internal to the group; they can also indicate disengagement within the group. 

You could have diverse ties that are distant: These are diverse ties with people outside your immediate group. These ties are good for evangelizing and embedding fresh or innovative ideas. The presence of such ties in manager networks are considered key for driving innovation and creativity in and among teams. 

### Ties are directional 

Ties (both Strong and Diverse) are directional in nature. If a Sara-to-Isaiah tie is strong, it does not necessarily follow that the Isaiah-to-Sara tie is also strong. The strength depends on the contribution that each person makes. For example, a greater contribution from Isaiah toward his relationship with Sara makes it more likely that Isaiah has a Strong tie with Sara, but it does not directly increase the liklihood of a tie in the opposite direction. 

Another example: A manager's tie to a direct report might be Strong, but not necessarily vice versa. 

### Examples of Strong ties and Diverse ties

#### Strong ties

John and Sally on peers on the same team working on the same project. They collaborate with each other often. They exchange emails several times a day and meet in various forums several times a week. Due to the very frequent nature of their interaction, a Strong tie very likely exists between them. This Strong tie is made even stronger by the fact that John and Sally share a common network. Each has their own set of people with whom they work and meet. These sets of people overlap, which creates an indirect bonding or relationship -- a common network -- which, in turn, strengthens the Strong tie between John and Sally. 

Note, however, that each person's contribution counts. See [Ties are directional](#ties-are-directional).

#### Diverse ties 

Preeti is a research scientist in an R&D department, and Rahul is a supply-chain logistics manager who works in the shipping department of the same company. They met at a Diversity & Inclusion virtual event at the company a few months ago, and are now connected to each other on LinkedIn. They share no commonality in their job functions and there is limited opportunity for them to interact with each other in small-group settings. 

Both Preeti and Rahul have their own connections, and there is no overlap in people across their connections. Due to these circumstances, a Diverse tie very likely exists between them. Recently, Preeti liked an article on climate science on LinkedIn. Since Preeti is in Rahul's LinkedIn network, Rahul got to read this article, which he otherwise might have missed. As shown here, Diverse relationships such as the one between Preeti and Rahul promote sharing of varied and non-typical information.

#### Strong ties and Diverse ties 

Mark and Matt work as engineers in the same large development team. However, they work on different products. Due to the nature of their roles, they are expected to collaborate closely with each other, and they do these in regular cross-group sync-up meetings and occasional emails. Based on these frequent collaboration events, a Strong tie could exist between them. 

Now, since they work on separate products, they tend to work with different people within their own workgroups. This results in some amount of fresh information flowing to each other through their own networks. For this reason, it is possible that a Diverse tie could also exist between the two to some degree.

## Frequently asked questions

The following questions and answers refer to metrics; you can find their definitions in [Metric descriptions / Person metrics](../use/metric-definitions.md#person-metrics) and in [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics). 

**Q1. What is the difference between "Strong ties" and "Internal network size"?**

A1. Strong ties takes the network commonality that exists between the two people into account, a situation in which both people are investing time together or enabling other forms of bonding. Strong ties also gives more weight to meetings-based collaboration than to email. This is because meetings are more inter-personal in nature and enable direct person-to-person engagement, which results in a formalized engagement. Email-based collaboration doesn't translate into such an interpersonal engagement. 

Internal network size simply means the number of connections a person has within the company, based on the number of meaningful interactions the person has with their connections. Strong ties means the number of tight-knit, engaged connections a person has within the company, based on the time that the person invested with their connections. 

In summary: Strong ties differs from Internal network size in that they reflect the number of a person's connections based on the quality of the engagement that exists between two people.

**Q2. When should you use "Strong ties" and when "Internal network size"?**

A2. Let's say you need nothing more than a quantitative number of connections a person has within the company. Also, you have no objection to including unlicensed users even though restricting your query to licensed users would return richer data. In this case, feel free to query for Internal network size. 

However, if you restrict your query to licensed users, we recommended that you query for Strong ties because this gives you a more realistic and qualitative view of engaged connections.

**Q3. When should you use "Strong ties" and when "External network size"?**

A3. Strong ties currently does not consider connections that a person has outside the company. To obtain the number of connections a person has outside the company, you can use External network size.

**Q4. What is the difference between "Diverse ties" and "Networking outside organization"?**

A4. Diverse ties returns the number of diverse or novel connections a person has across the company, based on the time invested by the person with their connection. Diverse ties also looks at network differences that exists between the two people where both people are investing time, enabling other forms of indirect sourcing of novel information. Person A can become a good source of diverse information for Person B if Person A does not spend too much time with Person B or if their common network has minimal overlap. 

In contrast, Networking outside organization returns the number of distinct organizations within the company a person has connections to, based on the number of meaningful interactions the person has with their connection. This metric quantifies connections at the organization attribute level. 

Therefore, unlike Networking outside organization, which returns connections only at the organization attribute level (a very high level), Diverse ties returns the number of connections based on the _quality_ of the engagement and the _variety_ of information that can potentially be conveyed through the connection. Also, Diverse ties can span any organizational attribute, which lets you more flexibly locate such ties anywhere in the company.

**Q5. When should you use "Diverse ties" and when "Networking outside organization"?**

A5. If you need nothing more than the number of connections a person has at the organization attribute level within the company, regardless of whether connections include licensed users or not, use Networking outside organization. 

But if you restrict your query to licensed users, use Diverse ties to obtain a more realistic and qualitative view of the variety of connections with potential for diverse or novel information. Diverse ties also allows you to look at connections at any organizational attribute level, which gives you more useful results than Networking outside organization would provide.

**Q6. When should you use "Diverse ties" and when "Networking outside company"?**

A6. Diverse ties currently does not consider connections that a person has outside the company. To obtain the number of connections a person has outside the company, you can use Networking outside company.


## Related topics

[ONA person queries](ona-person-query.md)

[Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics)

[View, download, and export query results](../use/view-download-and-export-query-results.md)


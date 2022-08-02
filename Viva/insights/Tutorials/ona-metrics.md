---
ROBOTS: NOINDEX,FOLLOW
title: Network metrics 
description: Describes the metrics that are used in network queries
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
manager: scott.ruble
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
---

# Network query metrics

The [Network person query](ona-person-query.md) and [Network person-to-person query](ona-person-to-person-query.md) use a number of connectivity metrics to help analysts investigate the effects and value of relationships within and beyond groups.

These connectivity relationships are of two broad types, _influence_ and _ties_. People in a company can have varying amounts of influence over their coworkers. Because influencers can act as change agents, identifying them can help leaders implement change. Ties reflect connections between people including, _diverse_ and _strong_. Identifying these ties can help you determine aspects such as, team alignment and potential for the flow of information and ideas.

You can find the basic definitions of the connectivity metrics in [network metrics](../use/metric-definitions.md#network-metrics):

| Metric | Available in this query type |
| ------ | ---------------------------- |
| [Diverse tie score](../use/metric-definitions.md#diverse-tie-score-define) | [Network person-to-person query](ona-person-to-person-query.md) |
| [Diverse tie type](../use/metric-definitions.md#diverse-tie-type-define) | [Network person query](ona-person-query.md) |
| [Diverse ties](../use/metric-definitions.md#diverse-ties-define) | [Network person query](ona-person-query.md) |
| [Influence](../use/metric-definitions.md#influence-define) | [Network person query](ona-person-query.md) |
| [Influence rank](../use/metric-definitions.md#influence-rank-define) | [Network person query](ona-person-query.md) |
| [Manager overlapping strong ties](../use/metric-definitions.md#manager-overlapping-strong-ties-define) | [Network person query](ona-person-query.md) |
| [Manager unique strong ties](../use/metric-definitions.md#manager-unique-strong-ties-define) | [Network person query](ona-person-query.md) |
| [Strong tie score](../use/metric-definitions.md#strong-tie-score-define) | [Network person-to-person query](ona-person-to-person-query.md) |
| [Strong tie type](../use/metric-definitions.md#strong-tie-type-define) | [Network person query](ona-person-query.md) |
| [Strong ties](../use/metric-definitions.md#strong-ties-define) | [Network person query](ona-person-query.md) |

The following sections describe the connectivity metrics in greater detail.

* [Influence and influence-rank metrics](#influence-and-influence-rank-metrics)
* [Strong and diverse tie metrics](#strong-and-diverse-tie-metrics)

## Influence and influence rank metrics

It's frequently necessary to implement changes within organizations, whether this means introducing new procedures or rolling out new systems or technology. The traditional top-down method of using formal authority to drive change &ndash; perhaps starting with mass emails &ndash; it's not always the most effective way. It might fail for any of several reasons including company culture, technical challenges, or problems with personality.

Instead, a more successful strategy uses change agents, who are influential, well-connected people in different levels of your company, not just at the top. Beyond an organization's formal hierarchy, informal networks of people can exert influence within those networks and between them. The most influential people have large personal networks with above-average numbers of relationships with their colleagues. This query lets you visualize these relationships through various metrics that reflect influence directly (with *influence* and *influence rank*) and indirectly (with various measures of ties to people outside your team.)

In other words, to help implement change, it pays to know which people have the most ties and the most influence. The Network queries were designed for this purpose. They can help you find the best-connected people in the company based on their collaboration characteristics.

After you learn who the best connected people are in the company, division, or other group, you can act on the likelihood that these people can effectively connect within or across groups and become
efficient drivers of change.

### How influence is calculated

The terminology in the following description comes from graph theory. In graph theory, a "node" (also called a "vertex") is an object that can relate to other nodes &ndash; other objects &ndash; in the graph. This model becomes useful when we extend it to the workplace, where a "node" represents a person who has connections to coworkers and others.

Influence indicates a node's potential influence on opinions of the network or an estimate of social status. Essentially, it uses the number and strength of connections coming into a node to rank the nodes. The values are between 0 and 1.

### Determine node rank for influence metrics

The most meaningful information to glean from Influence is the rank of the nodes. You can do this by using either of the two pertinent Network metrics, Influence and Influence rank.

* Use [Influence rank](../use/metric-definitions.md#influence-rank-define). This metric assigns to each node a number that corresponds to their relative influence, with the lowest number (1) for the most
influential node. You can use this metric, for example, to obtain a simple ranked list or to evaluate whether a node's network influence is changing over time.

* Use [Influence](../use/metric-definitions.md#influence-define). You use this metric in a more nuanced way than you'd use Influence rank. For example, assume that node A has an Influence of 0.6 and node B has an Influence of 0.3. You can accurately assume that node A is a more influential than node B, because node A ranks higher than node B. However, you cannot assume node A is twice as influential as node B because the values indicate a ranking or source of influence, not the amount of influence. The calculations for Influence use the relative collaboration time between individuals as the strengths of the connections for a person's influence measure.

## Strong and diverse tie metrics

You can use the Network queries to qualify a network connection between two people as a [strong tie](../use/metric-definitions.md#strong-ties-define), a [diverse tie](../use/metric-definitions.md#diverse-ties-define), or neither.

* [Diverse ties](../use/metric-definitions.md#diverse-ties-define) &ndash; *Diverse ties* reflect the number of diverse or novel connections that a person has across the company, based on the time invested by the person with their connection. This metric also takes into account network differences that exist between the two people where both people are investing time. Diverse ties are both directional and asymmetrical. For example, if A has a diverse tie with B if A either collaborates a lot with B or a lot with a network that they have in common with B.
* [Strong ties](../use/metric-definitions.md#strong-ties-define) &ndash; If two people have many network connections in common, they are considered to have a *strong tie*. Strong ties typically indicate shared membership in a workgroup or team. Like diverse ties, strong ties are directional. The strength of a person's tie depends on the contribution that the person makes in the relationship with the other person. Network queries also offer the following metrics that derive from the strong-tie metric:

  * [Manager overlapping strong ties](../use/metric-definitions.md#manager-overlapping-strong-ties-define) &ndash; A count of the number of strong ties that both a manager has and that their direct reports have in common with the manager.
  * [Manager unique strong ties](../use/metric-definitions.md#manager-unique-strong-ties-define) &ndash; A count of the number of strong ties that are unique in a manager's network that do not exist in the strong ties of any of that manager's direct reports.

>[!Note]
>When Viva Insights evaluates a network connection, it can only classify that connection as a strong tie or a diverse tie if it is between two [measured employees](../use/glossary.md#measured-employees-define).
<!--
For more details about how strong and diverse ties are calculated, see [Network metric calculations](ona-metric-calculations.md) and, in particular, the following sections:

* [Calculation factors](ona-metric-calculations.md)
* [Metric computations](ona-metric-calculations.md#metric-computations)-->

## Distance

You can derive more value from strong and diverse ties based on distance. In the following descriptions, "immediate group" refers to one manager and their direct reports.

* You can have strong ties that are close: These are strong ties with people in your immediate group. These ties are necessary for the promotion of overall team efficiency, team effectiveness, knowledge transfer, and best-practice development.
* You can have strong ties that are distant: These are strong ties with people outside your immediate group. These ties are good for evangelizing and embedding fresh or innovative ideas. However, such ties are likely not sustainable because of time demand for deep and constant engagement.
* You can have diverse ties that are close: These are diverse ties with people in your immediate group. These ties might appear as a result of use cases internal to the group; they can also indicate disengagement within the group.
* You can have diverse ties that are distant: These are diverse ties with people outside your immediate group. These ties are good for evangelizing and embedding fresh or innovative ideas. The presence of such ties in manager networks is considered key for driving innovation and creativity in and among teams.

## Directionality

Ties (both strong and diverse) are directional in nature.

In general, if a Sara-to-Isaiah tie is strong, it doesn't necessarily follow that the Isaiah-to-Sara tie is also strong. The strength depends on the contribution that each person makes. A greater contribution from Isaiah toward his relationship with Sara makes it more likely that Isaiah has a strong tie with Sara, but not necessarily in the opposite direction.

Moreover, it's possible that Isaiah's network is a subset of Sara's network. Hence although Sara can be a source of new information to Isaiah (since Sara collaborates with people that Isaiah does not) Isaiah would not be a source of new or diverse information to Sara. Hence in this case Sara is a diverse tie to Isaiah, but Isaiah is not a diverse tie to Sara.

Another example: A manager's tie to a direct report might be strong, but not necessarily vice versa.

### Strong ties example

John and Sally are peers on the same team working on the same project. They collaborate with each other often. They exchange emails several times a day and meet in various forums several times a week. Due to the frequent nature of their interaction, a Strong tie likely exists between them. This Strong tie is made even stronger by the fact that John and Sally share a [common network](../use/glossary.md#common-network).  Each has their own set of people with whom they work and meet. These sets of people overlap, which creates an indirect bonding or relationship &ndash; a common network &ndash; which, in turn, strengthens the Strong tie between John and Sally.

Each person's contribution counts. See [Directionality](ona-metric-calculations.md#directionality) for more details.

### Diverse ties example

Preeti is a research scientist in an R&D department, and Rahul is a supply-chain logistics manager who works in the shipping department of the same company. They met at a Diversity & Inclusion virtual event at the company a few months ago, and are now connected to each other on LinkedIn. They share no commonality in their job functions and there is limited opportunity for them to interact with each other in small-group settings.

Both Preeti and Rahul have their own connections, and there is no overlap in people across their connections. Due to these circumstances, a Diverse tie likely exists between them. Recently, Preeti liked an article on climate science on LinkedIn. Since Preeti is in Rahul's LinkedIn network, Rahul got to read this article, which he otherwise might have missed. As shown here, Diverse relationships such as the one between Preeti and Rahul promote sharing of varied and non-typical information.

Each person's contribution counts. See [Directionality](ona-metric-calculations.md#directionality) for more details.

### Strong and diverse ties example

Mark and Matt work as engineers in the same large development team. However, they work on different products. Due to the nature of their roles, they are expected to collaborate closely with each other, and they do these in regular cross-group sync-up meetings and occasional emails. Based on these frequent collaboration events, a Strong tie could exist between them.

Now, since they work on separate products, they tend to work with different people within their own workgroups. This results in some amount of fresh information flowing to each other through their own networks. For this reason, it is possible that a Diverse tie could also exist between the two to some degree.

## FAQ

The following questions and answers refer to metrics, which you can find definitions for in [Person metrics](../use/metric-definitions.md#person-metrics) and in [Network metrics](../use/metric-definitions.md#network-metrics).

**Q1. What is the difference between strong ties and internal network size?**

A1. Strong ties takes the network commonality that exists between the two people into account, a situation in which both people are investing time together or enabling other forms of bonding. Strong ties also gives more weight to meetings-based collaboration than to email. This is because meetings are more inter-personal in nature and enable direct person-to-person engagement, which results in a formalized engagement. Email-based collaboration doesn't translate into such an interpersonal engagement.

Internal network size simply means the number of connections a person has within the company, based on the number of [meaningful interactions](../use/glossary.md#meaningful-interaction-define) the person has with their connections. Strong ties means the number of tight-knit, engaged connections a person has within the company, based on the time that the person invested with their connections.

In summary: Strong ties differs from Internal network size in that they reflect the number of a person's connections based on the quality of the engagement that exists between two people.

**Q2. When should you use "strong ties" and when "Internal network size"?**

A2. Let's say you need nothing more than a quantitative number of connections a person has within the company. Also, you have no objection to including unlicensed users even though restricting your query to licensed users would return richer data. In this case, feel free to query for Internal network size.

However, if you restrict your query to licensed users, we recommended that you query for strong ties because doing so gives you a more realistic and qualitative view of engaged connections.

**Q3. When should you use "strong ties" and when "External network size"?**

A3. Strong ties currently does not consider connections that a person has outside the company. To obtain the number of connections a person has outside the company, you can use External network size.

**Q4. What is the difference between "diverse ties" and "Networking outside organization"?**

A4. Diverse ties returns the number of diverse or novel connections a person has across the company, based on the time invested by the person with their connection. Diverse ties also looks at network differences that exist between the two people where both people are investing time, enabling other forms of indirect sourcing of novel information. Person A can become a good source of diverse information for Person B if Person A does not spend too much time with Person B or if their [common network](../use/glossary.md#common-network) has minimal overlap.

In contrast, Networking outside organization returns the number of distinct organizations within the company a person has connections to, based on the number of [meaningful interactions](../use/glossary.md#meaningful-interaction-define) the person has with their connection. This metric quantifies connections at the organization attribute level.

Therefore, unlike Networking outside organization, which returns connections only at the organization attribute level (a very high level), diverse ties returns the number of connections based on the _quality_ of the engagement and the _variety_ of information that can potentially be conveyed through the connection. Also, diverse ties can span any organizational attribute, which lets you more flexibly locate such ties anywhere in the company.

**Q5. When should you use "diverse ties" and when "Networking outside organization"?**

A5. If you need nothing more than the number of connections a person has at the organization attribute level within the company, regardless of whether connections include licensed users or not, use Networking outside organization.

But if you restrict your query to licensed users, use diverse ties to obtain a more realistic and qualitative view of the variety of connections with potential for diverse or novel information. Diverse ties also allows you to look at connections at any organizational attribute level, which gives you more useful results than Networking outside organization would provide.

**Q6. When should you use "diverse ties" and when "Networking outside company"?**

A6. Diverse ties is internal only: It does not consider connections that a person has outside the company. Networking outside company counts not the number of _ties_ outside the company but rather the number of external _unique domains_ to which you are networked.

## Related topics

* [Network person queries](ona-person-query.md)
* [Network person-to-person queries](ona-person-to-person-query.md)
* [Network metric descriptions](../use/metric-definitions.md#network-metrics)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)

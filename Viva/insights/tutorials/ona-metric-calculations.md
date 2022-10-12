---
ROBOTS: NOINDEX,NOFOLLOW
title: Network query metric calculations 
description: Describes how the metrics are calculated for Viva Insights Network queries
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

# Network metric calculations

The following factors influence the calculation of values for strong ties and diverse ties:

* [Distance](#distance)
* [Directionality](#directionality)
* [Collaboration across the network](#collaboration-across-the-network)
* [Exclusivity](#exclusivity)

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

## Collaboration across the network

Network collaboration information is an important factor to consider while computing strong and diverse ties. Considering only direct collaboration between two people for deciding the type of tie can be lossy. If we only consider direct collaboration between people to identify strong or diverse ties, we end up missing the influence the network has on such ties.

**Example 1** &ndash;  If A has a lot of collaboration with B, does it imply that it is not a diverse tie? Based on direct collaboration alone, it could indicate that it is a strong tie, but it does not tell us much about how diverse the tie is. We need additional signals to comment on the diversity of the tie. However, if we look at B’s network and the collaboration that B has with people that A does not know, then we could determine if B is indeed a source of diverse information to A or not. If yes, then B could also be a diverse connection to A along with being a strong connection.

**Example 2** &ndash; If A has less collaboration with B, then does it mean A’s tie with B is weak? With direct collaboration as the only signal, that would probably be the case. However, here we missed another important factor that affects or influences the strength of the tie between people: and that is the network that they share. Even if A collaborates less with B, if they share a large common network, this common network can be leveraged to achieve the same effect that’s possible with a direct tie (for example, trust, commonality of purpose, and therefore faster completion of tasks).

This pattern is also seen in extended families where people have strong connections with extended members of a family due to a strong common network (family in this case) that they have even in cases where direct collaboration is limited.

Including network collaboration in diverse ties has enabled us to better compute who could be a source of new or diverse information. However, including network collaboration can conclusively help us understand if that is indeed the case. The more people that A collaborates with that B does not collaborate with, the greater the probability that A is a source of diverse or new information to B.

Including network collaboration for strong ties helps capture the impact of a strong common network on the tie between two people.

## Exclusivity

Strong and diverse ties are not exclusive. A tie could be both strong and diverse. One could have a strong tie with someone who has access to a diverse source of information. Such ties that are both strong and diverse are highly effective because they provide a bridge to people and information through someone with whom you has a strong connection. A good example is a tie between a manager and an employee. A manager could be both a strong and diverse tie to the employee, because the manager might have a strong connection with the employee and at the same time might be connected to a lot of other people with whom the employee is not connected and therefore can serve as a source of new or diverse information to the employee.

## Metric computations

### Computation of strong tie score

The following formula yields the strength of the tie that A has with B.

> Strong tie score (A → B)= ∛(CTS (A → B) * CTS (A → (AN ∩ BN)) * CTS (B → (AN ∩ BN)))

The terms in this formula mean the following:

> CTS (A → B) = Collaboration time spent by A with B

> AN ∩ BN = Common network between A and B

> CTS (A → (AN ∩ BN)) = Collaboration time spent by A with the common network between A and B

> CTS (B → (AN ∩ BN)) = Collaboration time spent by B with the common network between A and B

In other words, this formula gives the investment that was made by A in collaboration with B and the investment that was made by both A and B in collaboration with their common network. Therefore, it represents a combination of the strengths of their mutual tie strength and the strength of the common network that they share.

### Computation of diverse tie score

The following formula yields the diverse tie score from A to B. It defines how much of a diverse source of information, knowledge, and ideas that B is to A.

> Diverse tie score (A → B) = CTS (B) - CTS (B → (AN ∩ BN)) - CTS (B → A)

The terms in this formula mean the following:

> CTS (B) = Collaboration time spent by B

> AN ∩ BN = Common network between A and B

> CTS (B → (AN ∩ BN)) = Collaboration time spent by B with the common network between A and B

> CTS (B → A) = Collaboration time spent by B with A

In other words, this formula gives the investment made by B in collaboration with a network outside A and common network with A. Therefore, it represents the potential of B’s diversity of information and therefore the potential of A acquiring it from B when A collaborates with B. This could mean new information, knowledge, connections, and so on.

### Measuring effective collaboration

The collaboration time mentioned in the preceding formulae is a combination of the time spent in collaboration media such as email, meetings, and Teams.

Ties are most effective when collaboration is effective and bidirectional, that is, both parties are equally invested in the tie. The tie may not be effective if the investment in collaboration is one-sided. This is especially important for asynchronous communication media such as email. We currently employ the following formula to compute effectiveness of collaboration:

>Effective email collaboration score (A → B) = 1 -
   {
     ((| emails sent (A → B) - emails sent (B → A)| )) /
     (( emails sent (A → B) + emails sent (B → A) ))
   }

In the preceding formulae for strong and diverse ties, this computed effective score is multiplied with actual email collaboration time spent, to understand how effective the tie is, based on email collaboration.

### Determining the type of tie based on score

These computations compute the strong tie and diverse tie scores for every pair of employees. While these are raw scores, which aren’t normalized yet, we also provide additional data columns to make it easier to use the raw scores. Based on our analysis, we use percentile thresholds to categorize whether a certain tie is indeed strong or diverse. The thresholds are currently as follows:

| Data column | Description |
| ----------- | ----------- |
| [StrongTieType](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#strong-tie-type-define) | This column is present to help analysts quickly find the strongest ties. It contains values of 0, 1, or 2, based on the distribution of [StrongTieScore](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#strong-tie-score-define). The values indicate the following: <ul><li>1: This row clearly indicates a strong tie — 35th percentile and above, by strength</li><li>2: This row indicates a tie that is significant but less strong: at or above the 30th percentile but below the 35th percentile</li><li>0: This row indicates a tie that is not that strong: below the 30th percentile</li></ul> |
| [DiverseTieType](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#diverse-tie-type-define) | This column is present to help analysts quickly find the most diverse ties. It contains values of 0, 1, or 2, based on the distribution of [DiverseTieScore](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#diverse-tie-score-define). The values indicate the following:<ul><li>1: This row clearly indicates a diverse tie — 50th percentile and above, by diversity</li><li>2: This row indicates a tie that is significant but less diverse: at or above the 45th percentile but below the 50th percentile</li><li>0: This row indicates a tie that is not that diverse: below the 45th percentile</li></ul> | 

## Related topics

* [Network metrics](/viva/insights/tutorials/ona-metrics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Network person queries](/viva/insights/tutorials/ona-person-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Network person-to-person queries](/viva/insights/tutorials/ona-person-to-person-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Network metric descriptions](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#network-metrics)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)

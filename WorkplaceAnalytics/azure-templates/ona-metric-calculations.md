---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Organizational Network Analysis Azure Template metric calculations
description: Learn how the metrics are calculated by the Organizational Network Analysis Azure Template for Workplace Analytics
author: madehmer
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Organizational Network Analysis Azure Template metric calculations for Workplace Analytics

_This template is only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates include the Organizational Network Analysis template has several metrics to help you visualize and analyze formal and informal relationships within your organization. 

### Closeness Centrality

Closeness Centrality is a measure of how close a node is to all other nodes in the network. It was originally defined as the inverse of a node’s farness, where farness is the sum of the distances from the node to all the other nodes in the network.  This definition requires the network to be fully connected, which means that each node can reach all other nodes in the network. This assumption is not always true in directed graphs and never true for disconnected graphs. Accordingly, we make several modifications to our calculation of closeness because of the directed nature (and possibly disconnected as well) of our social network graphs. For more details about the calculations, see [Closeness Centrality metric calculations]().

#### Employee level

Traditionally, closeness centrality (C_i) is calculated as follows:  


Where **n** is the total number of nodes in the network and **d(i,j)** is the distance from **node i** to **node j**.

If the graph is disconnected, then the closeness centrality will be calculated as zero (0). To correct for this, the template will take the sum of the inverse distances:

Now, the nodes that can’t be reached will not contribute to the sum if the graph is disconnected. This modification gives different values for the centrality for an individual than the original measure, but approximately maintains the ratio of an individual’s score to others in the network. Since a disconnected graph can be considered with this implementation, the closeness scores are normalized by n-1. Note that this normalization considers all the nodes in the network, not just those in the largest, connected component of the network.

Weights between nodes are not considered for the current implementation of closeness.  Hence the distance is defined as the number of nodes (i.e., people) between nodes i and j on the shortest path p.  The distances between nodes are calculated by using the single-source shortest path algorithm [5].   The higher the value of closeness the fewer nodes on average it takes that node to reach others in the network.

#### Group level

The equation used for employee level closeness is also used to calculate the group level closeness. Essentially, the group closeness only considers the distances from nodes inside the group to nodes outside of the group.  Within group distances are ignored [1]. Again, we consider only the shortest paths between nodes. It is normalized by the number of nodes outside of the source node’s group C.

### Degree Centrality

Degree centrality is based on the number of edges connected to a node. The overall degree is the number of incoming and outgoing edges connected to a node. The Indegree centrality is the number of incoming edges. The Outdegree centrality is the number of outgoing edges from the node.

* **Employee level**: These are all calculated with [GraphX by Apache Spark](https://spark.apache.org/graphx/).
* **Group level**: The group degree centrality is the number of nodes outside the group that are connected to members of the group. The normalized group degree centrality is calculated as follows:

    **Degree Centrality** = |**N**(**C**)|/(|**V**|-|**D**|)
   
   Where |**N**(**C**)| is the number of unique nodes which are not in **group C** but are adjacent to a member of **C**. And |**V**| is the number of nodes in the network and |**D**| is the number of nodes in group C. You can apply this same formula  to calculate indegree and outdegree measures by considering only “indegree” nodes or “outdegree” nodes.
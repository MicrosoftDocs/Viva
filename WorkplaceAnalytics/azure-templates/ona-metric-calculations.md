---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Measure calculations for Organizational Network Analysis Azure template
description: Learn how the metrics are calculated for the Organizational Network Analysis Azure Template for Workplace Analytics
author: madehmer
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Measure calculations for the Organizational Network Analysis Azure template

_This template is only available as part of a Microsoft service engagement._

The Organizational Network Analysis Azure template for Workplace Analytics has a number of measures to help you visualize and analyze formal and informal relationships within your organization.

Each dot or node in the template's network graph represents either an employee or a group. The lines between the nodes represent connections, which are collaborative relationships between the connected employees or groups.

The node measures for employees are de-identified to maintain their privacy. Group node measures represent the group's measures, such as for a department (Sales) or a functional group (program managers) within the organization.

## Highlight key network connections

You can size the nodes and connections based on what you want to highlight by using the **Scale Nodes** option (No Measure by default) at the top. The following shows the measures available in a *Network View* of the graph:

![Combined View measures](./images/ona-network-measures.png)

And the measure options available for the *Combined View* of the graph, which include Density as an additional Scale Node option that’s only available in this view:

![Network View measures](./images/ona-combined-measures.png)

## How are connections measured?

Each of the measures are based on the connections between the nodes. To ensure the calculations accurately represent the interactions between people or groups within the organization, the measures account for connection weight and direction:

* Connections are weighted based on the amount of collaboration time in meetings and email between two nodes (connection strength).
* They are also directed because they specifically account for who sent and who received email. For these calculations, meetings do not have direction.

## How are the measures for people and graph different?

The measure interpretations for employees and groups are the same. For example:

* If an employee has a high degree, it indicates the person has more connections in the network than those with lower scores.
* If a group has a high degree, it indicates the group has more connections in the network than other groups with lower scores.

However, group measures are not simply the average (or median, maximum, or minimum) of the scores of the employees within the group. Instead it’s the cumulative score of how the people within the group interact with people in other groups. In some cases, the two may be equal but that's generally not the case.

A simple example of this is a water molecule, which is made up of two hydrogen atoms and one oxygen atom. If you average together the properties of hydrogen and oxygen (both gases), it won't generate the properties of a water molecule.

Just like atoms and molecules, how people are connected within an organizational group makes the properties of the group different than the average properties of the individual people within the group. You can generate summary statistics of employees within the group from the employee-level (de-identified) measures.

For more general information about these network measures, see [Centrality](https://en.wikipedia.org/wiki/Centrality).



## Boundary Spanning

For a defined group, Boundary Spanning measures an employee’s collaboration with members of other groups, with a boost for the diversity of their connections (number of groups). This does not consider ties inside their own group.

It measures the extent to which employees act as representatives of their group across the organization. Depending on the direction of the relationships, it can indicate resources to other functions, or cross-functional liaisons.

* **Employee level**: Boundary Spanning is the geometric mean between the total collaboration time a person gave to those outside of their group and the total number of unique groups this same person collaborated with.

* **Group level**: This is the same for groups as for employees, except that the totals represent a group instead of a person. It's the geometric mean between the total collaboration time a specified group spent with people outside its own group and the total number of unique, external groups that the group collaborated with.

The following is an example of a simplified Boundary Spanning network.

![Boundary Spanning graph](./images/boundary-spanning.png)

## Bridging Index

Bridging Index is the number of times a person or group is on the most probable path of information flow between two other people or groups. Meaning these nodes represent the potential control over the flow of information in your organization.

Information flow through a network is often characterized by random-walk betweenness measures, which do not limit the flow of information through a network to the shortest paths. The traditional definition of current-flow bridging is computationally expensive. As such, this template uses a more computationally efficient measure of the importance score of an edge and the probability that information visiting an edge through a node will stay at the edge.

* **Employee level**: The Bridging Index calculates the importance scores for all edges in the network and then sums up the importance scores for edges incident to the employee of interest.

  When comparing the average across aggregated employees, you need to normalize this measure by the size of each person’s group. You can either divide by the group’s maximum, or by the adjusted group size: [(n-1)*(n-2)]/2. For groups, use the group level measures instead.

* **Group level**: At a group level, the Bridging Index sums the importance scores of a group’s incident edges, where the importance score of edges is the same for both employee and group level metrics. As such, we calculate the importance scores for all edges in the network and then sum up the importance scores for edges incident to the group of interest.

The following shows the largest node as the bridge between the other nodes in the graph.

![Bridging Index graph](./images/bridging.png)

## Degrees

Degrees is based on the number of connections to a node. The overall degree is the number of incoming and outgoing edges connected to a node. <!-- The Indegree centrality is the number of incoming edges. The Outdegree centrality is the number of outgoing edges from the node.-->

Degrees measures the degrees (number of links) of all nodes in the graph, which does not count any self-links (links that have the same node at both ends). Where there are multiple links between two nodes, each link is counted.

* **Employee level**: These are all calculated with [GraphX by Apache Spark](https://spark.apache.org/graphx/).

* **Group level**: The group degree centrality is the number of nodes outside the group that are connected to members of the group. The normalized group degrees is calculated as:
 
   **Degrees** = |**N**(**C**)|/(|**V**|-|**D**|)

   Where |**N**(**C**)| is the number of unique nodes which are not in **group C** but are adjacent to a member of **C**. And |**V**| is the number of nodes in the network and |**D**| is the number of nodes in group C. You can apply this same formula to calculate indegree and outdegree measures by considering only “indegree” nodes or “outdegree” nodes.

The following is an example of a simplified Degrees graph.

![Degrees graph](./images/degrees.png)

## Density

Density measures the number of actual connections out of the number of possible connections within a network or subgroup.

Higher density indicates higher levels of connectivity. Large groups tend to have small values since it’s much harder for everyone to connect with everyone else. Be careful comparing across groups. Proportion of possible intra-community edge weight based on each node’s max edge weight. Higher density scores represent a better inwardly-connected community.

This measure uses directionality, which means the density between group A and group B will only count the interactions that went from A to B, but not those interactions that went from B to A. This also means that the densities between groups will vary depending on whether the density is from Group A to Group B or from Group B to Group A. In other words, the density matrix is not symmetrical.

The following table depicts the density score within and across the respective groups, where:

 **Density** = **Actual connections**/**Potential connections**

![Density table](./images/ona-density-table.png)

The following is an example of a simplified Density graph.

![Density graph](./images/density.png)

## Influence Index

Influence Index is a centrality measure for social networks that measures a node’s potential influence on opinions of the network or as an estimate of social status.  Basically, Influence Index counts the number and quality of edges coming into a node.

* **Employee level**: The calculations use the relative collaboration time between individuals as the weights of the edges in our determination of influence for a node.

* **Group level**: For group metrics, the Influence Index is the number and quality of edges coming into the group. Intra-group connections do not contribute to the Influence Index for the group. The network is collapsed into group nodes where the edge weights between groups is the sum of the individual node weights connecting the two groups.

The following is an example of a simplified Influence Index graph.

![Influence Index graph](./images/influence.png)

## Reach Index

Reach Index measures how close a node is to all other nodes in the network. It was originally defined as the inverse of a node’s farness, where farness is the sum of the distances from the node to all the other nodes in the network.

This measure requires the network to be fully connected, which means that each node can reach all other nodes in the network. This assumption is not always true in directed graphs and never true for disconnected graphs. Accordingly, we make several modifications to our calculation of closeness because of the directed nature (and possibly disconnected as well) of our social network graphs.

* **Employee level**: In a fully connected graph, where there is a path from any node to any other node, closeness is calculated as the reciprocal of "farness" (for example: 1/farness). The farness of a node is defined as the sum of the distances to each of the other nodes.

* **Group level**: The group equation is the same as the employee level one. Essentially, the group closeness only considers the distances from nodes inside the group to nodes outside of the group. Within group distances are ignored and only the shortest paths between nodes are considered. It is normalized by the number of nodes outside of the source node’s group. Within group distances are ignored. Again, we consider only the shortest paths between nodes. It is normalized by the number of nodes outside of the source node’s group C.

This value will be between 0 and 1 and usually larger than the reach of individual nodes, due to higher connectivity. Reach index values do not typically have large separation among the top ranked members. This means that those nodes highest in reach are all quite similar to each other in how they can connect to the rest of the network.

The following is an example of a simplified Reach Index graph.

![Reach Index graph](./images/reach.png)


## Related topics

* [Organizational Network Analysis Azure Template](./organization-network-analysis.md)
* [Workplace Analytics Azure Templates overview](./overview.md)
* [What's new in Workplace Analytics Azure Templates](./release-notes.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
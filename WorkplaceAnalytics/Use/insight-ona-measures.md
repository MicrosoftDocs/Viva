---
ROBOTS: NOINDEX,NOFOLLOW
title: Organizational network measures for Workplace Analytics visual insights
description: Learn more about the network graphs used in Workplace Analytics visual insights
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Organizational network measures

The organizational network graphs used for some of the Workplace Analytics visual insights use a number of measures to help you visualize and analyze collaborative relationships within your organization.

The following is an example of an Employee empowerment network graph.

![Employee empowerment network graph](../images/wpa/use/ee-ona-graph.png)

## Nodes

In the network graphs, each dot or node represents an employee or a group. The edges are the lines between the nodes, which represent connections that are collaborative relationships between them.

The node measures for employees are de-identified to maintain their privacy. Group node measures represent the group's measures, such as for a department (Sales) or a functional group (program managers) within the organization.

## Colors

The node colors represent the level of it in the graph as indicated by the legend. The darker the color the greater representation that node has in comparison with others in the network. The lighter the node color is, the less representative it is as compared to the population shown in the graph.

## Clusters

The node clusters shown are formed naturally in an organizational network graph when it uses the force-directed graph drawing algorithm. A node with strong connections are very likely clustered together in a graph. For the majority, a cluster represents a division or department in an organization.

## Connection measures

Each of the measures are based on the connections between the nodes. To ensure the calculations accurately represent the interactions between people or groups within the organization, the measures account for connection weight and direction:

* **Weight** - Connections are weighted based on the amount of collaboration time in instant messages, meetings, and email between two nodes (connection strength).
* **Direction** - They are also directed because they specifically account for who sent and who received instant messages or email. For these calculations, meetings do not have direction.

## Available network graphs

For calculation information about a specific network graph, select the following applicable visual insight.

* [Employee empowerment](improve-agility.md#about-the-insights) - Shows the number of empowered employees and disempowered employees in your organization.
* [Cohesion within teams](boost-engagement.md#about-the-insights) - Shows the teams who are the most cohesive and those who are not very cohesive based on the average monthly collaboration activity within the team’s network.
* [Collaboration across groups](foster-innovation.md#about-the-insights) - Shows the number of teams with high cross-group collaboration and those with low cross-group collaboration.
* [Distribution of potential manager candidates](accelerate-change.md#about-the-insights) - Represents the current managers, potential managers, and other employees based on their network connections within your organization.
* [Internal network connections by employee network strength](customer-focus.md#about-the-insights) - Shows the number of employees with strong internal networks as compared to other employees in your organization.
* [Reach of influencers](accelerate-change.md#about-the-insights) - Shows the reach of influencers, their connections, and how they compare to other employees in your organization.

## Are the measures for employees and groups different?

No, the measure interpretations for employees and groups are the same. For example:

* If an employee has a high degree, it indicates the person has more connections in the network than those with lower scores and therefore has more exposure or access to information.
* If a group has a high degree, it indicates the group has more connections in the network than other groups with lower scores and therefore has more exposure or access to information.

In terms of calculations, group measures are not simply the average (or median, maximum, or minimum) of the scores of the employees within the group. Instead, the measures are the cumulative scores of how the people within the group interact with people in other groups. In some cases, the two may be equal but that's generally not the case. The key difference is that the group measures do not account for connections that occur between members of the same group.

A simple analogy of this is a water molecule, which is made up of two hydrogen atoms and one oxygen atom. If you average together the properties of hydrogen and oxygen (both gases), it won't generate the properties of a water molecule because the bonds between atoms are important to its properties.

Just like atoms and molecules, how people are connected within an organizational group makes the properties of the group different than the average properties of the individual people within the group.

For more general information about these network measures, see [Centrality](https://wikipedia.org/wiki/Centrality).

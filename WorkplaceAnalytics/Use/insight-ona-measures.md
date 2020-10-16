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

In the network graphs, each dot or node represents an employee in the organization. Node size corresponds to an individual’s influence score. Employees with greater scores are represented by larger nodes in the graphs.

## Colors

The node colors represent the level of it in the graph as indicated by the legend. The darker the color the greater representation that node has in comparison with others in the network. The lighter the node color is, the less representative it is as compared to the population shown in the graph.

## Clusters

The node clusters shown are formed naturally in an organizational network graph when it uses the force-directed graph drawing algorithm. Nodes with strong connections are very likely clustered together in a graph.

The force-directed algorithm assigns forces among the set of edges and nodes, so they overlap as little as possible and are distributed evenly. This is a good overall view for any kind or size of data and is useful for finding patterns and symmetries.

## Available network graphs

For calculation information about a specific network graph, select the applicable visual insight.

* [Employee empowerment](improve-agility.md#visual-insights) - Shows the number of empowered employees and disempowered employees in your organization. This helps identify who controls information and where it is concentrated in your organization. You can use these insights to democratize information to improve transparency and decision-making throughout.<!--* [Cohesion within teams](boost-engagement.md#visual-insights) - Shows the teams with strong cohesion and those without strong cohesion based on average monthly collaboration activity within the team’s network. * [Collaboration across groups](improve-agility.md#visual-insights) - Shows the number of groups with high cross-group collaboration and those with low cross-group collaboration, which helps identify organizational silos and agile teams currently working within the network. * [Collaboration across teams](foster-innovation.md#visual-insights) - Shows the number of teams with high cross-group collaboration as compared to other teams in your organization.-->
* [Distribution of potential manager candidates](accelerate-change.md#visual-insights) - Represents the current managers and potential managers as compared with the other employees within your organization, based on their network connections.<!--* [Internal network connections by employee network strength](customer-focus.md#visual-insights) - Shows the number of employees with strong internal networks as compared to all other employees in your organization. * [Managers and cross-group connectivity](develop-managers.md#visual-insights) - Shows the number of well-connected managers and less-connected managers as compared to all other employees within your organization, based on their network connections. Enables you to see the impact a manager's network has on engagement and the networks of direct reports. These insights enable you to build more effective manager training programs to improve engagement and broader organizational connectivity.-->
* [Reach of influencers](accelerate-change.md#visual-insights) - Shows the reach of influencers, their connections, and how they compare to other employees within your organization. This identifies groups who power the unobservable communication networks that shape culture and drive change. You can then target these influencers to accelerate the adoption of new technology.

## Node measures

A large or darker node represents an individual who has more connections in the network and therefore higher scores than those with lower scores and therefore has more exposure or access to information.

For example, influence indicates a node's potential influence on opinions of the network or an estimate of social status. Essentially, it uses the number and strength of connections coming into a node to rank the nodes. The values are between 0 and 1.

The most meaningful information about Influence is the rank of the nodes. For example, assume that node A has an Influence of 0.6 and node B has an Influence of 0.3. You can accurately assume that node A is more influential than node B, because node A ranks higher than node B. However, you cannot assume node A is twice as influential as node B because the values indicate a ranking or source of influence, not the amount of influence. The calculations for Influence use the relative collaboration time between individuals as the strengths of the connections for a person's influence measure.

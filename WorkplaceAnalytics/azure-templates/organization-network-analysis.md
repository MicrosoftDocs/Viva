---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Organizational Network Analysis Azure Template for Workplace Analytics 
description: Learn about the Organizational Network Analysis Azure Template for Workplace Analytics and how to use it for advanced data analysis
author: madehmer
ms.author: v-midehm
ms.date: 05/02/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Organizational Network Analysis Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates include the Organizational Network Analysis template that enables you to visualize connections within your organization, pinpoint collaboration patterns, and drive change.

Workplace Analytics has several metrics to help you visualize and analyze formal and informal relationships within your organization. This analysis can help you shape a business strategy that improves communication, making your business more effective and sustainable.

## To add new network analysis

1. In Workplace Analytics Azure Templates, select **Organizational Network Analysis**.
2. On the **Organizational Network Analysis** page, select **Add New Analysis** at top right in the table heading.
3. For **Define Analysis Settings**, enter a name and select a path to the dataset for the new network graph.

   ![Add New Analysis](./images/azure-add-new.png)

4. For **Specify Interaction Thresholds**, select the following thresholds and then select **Next**:

   * **Max Duration Threshold of each interaction** - select the maximum number of hours for each interaction.
   * **Max # of members involved in each interaction** - select the maximum number of people involved in each interaction.
   * **Min # of interactions** - select the minimum number of interactions between the selected groups or people.
   * **Rolling Weeks** - select the number of weeks prior to today that you want to analyze.

5. Optionally, for **Exclude Meetings based on keywords**, enter one or more terms separated by a comma to exclude meetings with these keywords in the meeting subject line from this analysis.
6. Select **Run**.
7. When the **Dataset Submitted** message appears, select **OK**.
8. Your new analysis is listed in the table with the following information and actions:

   * When the **Status** changes to a green check mark, you can then [render a network analysis graph](#to-render-a-network-analysis-graph) with the new analysis.
   * If the analysis fails, you can select the **Job Details** (i) icon next to Status to view details and see what might've caused the failure.
   * Select a table column heading, such as Name or Submitted, to sort by it.
   * Select the **Dataset Parameters** icon next to the name to view them for the analysis in that row.
   * Select the **Delete Dataset** (trashcan) icon to delete the analysis from the list.


   ![Dataset parameters](./images/azure-ds-params-1.png)

## To render a network analysis graph

1. On the **Organizational Network Analysis** page, select the name of the analysis in the table.
2. Select one or more filters for the graph. The available filters match up to the HR attributes included in the imported [organizational data](../setup/prepare-organizational-data.md##attribute-reference) from Workplace Analytics. For example, Domain, Engagement, FunctionType, KeyTalent, and LevelDesignation are HR attributes, as shown in the following graphic.

   ![Organizational Network Analysis](./images/ona-filter-options.png)

3. Select **Render Graph**. Based on the data size, it might take a few minutes for the graph to appear.
4. By default, the graph is shown in the **Network View** with **No Measure** applied. Use the following options to customize, save, or download a graph.

   View option |Name |Description
   ------------|--------------|------------
   ![ONA no measure](./images/ona-no-measure.png)| No Measure | Changes how the data is measured and shown in the graph based on the Node Sizing option you choose.
   ![ONA legend](./images/ona-legend.png)| Show or Hide Legend  | Opens or closes the legend of assigned node colors for the HR attribute shown in the graph.
   ![ONA link color](./images/ona-link-color.png) | Link Color |Select a different color for the line links shown in the graph.
   ![ONA dataset parameters](./images/ona-dataset-parameters.png) | Dataset Parameters |Choose to view the network parameter details that you set for the selected dataset.
   ![ONA network view](./images/ona-network-icons.png)| Network View  | Changes how the graph shows the network, which you can view in either the **Force-directed**, **Lens**, or **Structural** layout.
   ![ONA combined view](./images/ona-combined-view-icon.png) |Combined View | Changes the graph view to Combined View, which prompts you to select an HR attribute meeting metric to display the nodes for , such as FunctionType.
   ![OnA change color nodes](./images/ona-color-icon.png) | Change Node Colors | You can select to change the color of any of the nodes shown in the graph.
   ![ONA change settings](./images/ona-settings.png) | Change Settings |Scales the thickness or color darkness of the link lines. You can also use this to turn tool tips on or off for selected nodes.
   ![ONA filter](./images/ona-filter-icon.png) | Filter by HR attributes |Changes the filters selected for the rendered graph.
   ![ONA table view](./images/ona-table-icon.png) | View as Table |Choose to see a table view of the graph data.
   ![ONA download graph](./images/ona-download-icon.png) | Download Chart |Choose to download an image of this graph view as a PNG file.
   ![ONA save graph](./images/ona-save.png) | Save Graph |Choose to save this graph as shown in the template to load and view later.

## To load and view a saved graph

1. On the **Organizational Network Analysis** page, select the name of the analysis in the table.
2. At the top right of the **Graph Analysis** page, select **Load Saved Graph**.
3. Select the name of the graph that you want to view.

## Scale nodes

You can select a measure to scale the data and change how it's shown in the graph. The data and the filters you select for the graph determine what a node represents (people or groups) and what graph measures are available, such as Number of employees or Density.

![Organization Network Analysis measures](./images/ona-measures.png)

### Number of employees

The node size is based on the number of people in that particular group. The larger node sizes represent the nodes with the larger number of people in that network.

### Betweenness

Betweenness measures how much of a key connector a person or group (node) is in the network. This is calculated by finding the shortest paths between all nodes to all other nodes in the network and finding the number of times a node appears on the shortest path. The more times a node appears on the shortest path between other nodes, the more of a key connector that node is and therefore the higher the node’s betweenness score is.

### Closeness

Closeness measures the closeness between nodes in a network, based on their ability to reach them. It then calculates each node’s shortest path to every other node, then assigns each node a score based on the sum of all the paths. Nodes with a high closeness value have a lower distance to all other nodes and therefore are efficient broadcasters of information.

### Degrees

Degrees measures the highest number of links to other nodes within the network. Nodes with a high degree of links are those people or groups who have the best connections to others in the network. These people or groups can be key influencers or might just be strategically important for communication.

### Density

Density measures cohesion within groups and across groups by density. This measure only shows as a table and not a graph. The table view depicts the density score within or across the respective groups. 

Density is measured as follows:
* 

### Eigen Centrality

Eigen Centrality is a measure of influence that considers the number of links each person or group (node) has and the number of links their connections have, and so on throughout the network. The larger nodes represent the people or groups with high centrality and can be key influencers in their network.
As shown in the following graphic, Engineering, R&D, and Sales are key influencers that connect all the other groups.

![Eigen Centrality](./images/ona-eigen.png)

### Interconnectedness

Interconnectedness is a measure of how diverse a node’s connections are. The higher the interconnection for a node, the more that node’s connections come from other nodes. The nodes with high interconnection can be good ambassadors and help drive collaboration for the intersecting nodes.

### Graph notes

* **Insufficient group size** - If one or more nodes represent groups that are smaller than the set Minimum Group Size, they're combined and listed as an insufficient group (such as in the color node list) and won't show in the graph.

* **Delete a node** - If you want to exclude a node from the graph, you can use the filter options or select the node in the graph to highlight it, and then press **Delete** (on your keyboard). Before saving the graph, you can right-click in the graph, and then select **Show Hidden** to undo a delete.

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
* [Topic Analysis Azure Template](./topic-analysis.md)
* [Process Explorer Azure Template](./process-explorer.md)

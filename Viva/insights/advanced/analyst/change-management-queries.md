---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 02/05/2024
title: Create change management queries
description: Learn how to use organizational network analysis or ONA to measure the impact on collaboration after a large-scale company change.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Create change management queries

>[!IMPORTANT]
> This feature is for private preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

The **Change management** query uses organizational network analysis (ONA) to help you understand how collaboration and team working patterns were impacted after a major company change, such as a reorganization, an agile transformation or even a change in the working model like a move from remote to a hybrid work mode.

With the query, you can uncover insights such as:

* Are specific groups working more closely with each other, as was intended? If so, which ones, and what is the extent of the collaboration change?

* Are any groups now collaborating less with each other? If so, which ones, and how much less?

* How is the collaboration behavior of the sub-groups contributing to the change (increase/decrease) in collaboration strength of the overarching group?

* Are any groups demonstrating increased tendency towards within-group collaboration? If so, which groups?  

### Prerequisites

Before you can run the ONA query and populate the report in the advanced insights app, you’ll need to be assigned the role of **Insights Analyst** in Viva Insights. [Learn about assigning roles](../../advanced/setup-maint/assign-user-roles.md).

## Set up a Network Analysis

1. In the advanced insights app’s **Analysis** page, in the **Network analysis** section, under “Change management,” select **Start analysis**.

2. Name the analysis. Make sure the name is unique and consider including the date. 

3. Select a **Time period before change**, and a **Time period after change**. These two periods represent the range of time you want to analyze and compare before the change event, and after the change event. We recommend each period be at least three months for accuracy of results.

4. Optional: Type a **Description**.

5. Under **Employee attributes and filters**, select two organizational attributes you’d like to use to factor into your analysis. These attributes control how employees are grouped in the ONA experience. Your choice of attributes depends on the specific questions you’d like to address with the analysis. [Learn more about organizational data](../../advanced/admin/org-data-overview.md).

    >[!Note]
    > You’ll be able to select HR attributes soon as we include more capabilities.

6. Under **Which employee population do you want to analyze**, select which employee population you want your analysis to apply to. Use filters like function type or job level to home in on the specific employee population that you want to analyze. For example: instead of analyzing your entire licensed population, you may just want to examine a subset of the licensed population. The subset of the licensed population that you would like to analyze constitutes your population scope.

7. Now that you’ve set up the template, you’re ready to run it. At the screen’s upper right, select **Run**.

## About template results

### How to access your results

After you run the template, go to the **Analysis results** page to check its status. When the template is ready, a green checkmark appears under the **Status** column. To download your results as a .csv file, select the CSV icon under the **Export data** column.

:::image type="content" source="../images/ona-analysis-results.png" alt-text="Screenshot showing the ONA query results page.":::

To view the results, find your query under **Query name**, then select the Network icon under **View**.

### Explore insights in summary view

At the top of the screen, you’ll see two cards that provide two categories of insights relevant to your query: **Significant change in collaboration** and **Potential to become insular**. These two cards provide two different types of insights and data points related to collaboration and working patterns.

Let’s now discuss the insights provided by each category, and how you can navigate the ONA experience for each.

## Insight category #1 - Significant change in collaboration

### Summary page

**Significant change in collaboration** highlights significant changes in collaboration patterns following the event. You can use this insight category to analyze how collaboration increased or decreased between specific groups, as well as between smaller groups of people or subgroups within the larger groups. For example, with this card, you could analyze the changes in collaboration between the Product and Marketing groups following a reorganization.

Learn more about how these insights are generated.

At the top of this summary page, the **People grouped by field** will default to the first HR attribute you selected when defining the analysis. The insights surfaced within the categories and the associated key observations are controlled by the grouping attribute selected. You can also change the attribute here, which will produce different insights.

:::image type="content" source="../images/ona-people-grouped-by.png" alt-text="Screenshot showing the People grouped by field.":::

Each card provides a list of **top highlights** for that particular insight category, and an accompanying visual graph of the groups you selected. Hover over each highlight to see which area of the graph it relates to.

These highlights call out the most significant changes in group collaboration patterns following the event.

To provide these top highlights, we utilize a ranking hierarchy to determine which highlights to surface, including the order in which they’re listed. The most important highlights are listed first.

Here is the ranking system we use – from most to least important – to determine these top highlights and the order in which we present them:

1. New collaboration patterns between existing groups following the change event

2. Lost collaboration patterns between existing groups

3. Significant changes in existing collaboration patterns between groups

4. Net new groups and their collaboration patterns

5. Groups that were completely lost following the change event

Now that you’ve got a handle on the top highlights, let’s dive in to the network view for this insight category. This view allows you drill down further into the collaboration behaviors between specific groups and subgroups for the time period you selected. To enter this view, at the bottom left of the summary page, select **Explore more**.

### Side-by-side view

This is the first view you’ll see after you select **Explore more**. It provides a network visualization comprised of nodes. The graph on the left provides the “before” view of collaboration based on the dates you provided during setup, while the graph on the right is the “after” view.

:::image type="content" source="../images/ona-hotspot-1-side-by-side.png" alt-text="Screenshot showing the side-by-side view for the first insight category.":::

Here’s how to interpret this view of nodes:

* The nodes are grouped based on the “People grouped by” selection, and their size is based on the number of people in the group.

* As long as 2 groups have engaged in reciprocal communication in a month and there is a row depicting that communication in the Group-to-Group cross-collaboration query output, then the groups will be surfaced in the network visualization.

* A gray “other” node contains  other groups which have been filtered out of the network view in order to facilitate a more readable network visualization. You can use the **Filter groups** tool described below to display these groups as individual nodes.

* The colors around the nodes represent how the groups are segmented, such as by employee level or geography. The segments that constitute a group is governed by the “Segment groups by” selection.

* The thickness of the line or edge connecting any two nodes is based on the extent of the collaboration change between those groups compared to the “before” view. The thickness of the edges represents the amount of collaboration.

* The color of the edges in the “after” view depicts where collaboration has increased or decreased. A green color on the edge between two nodes indicates that the collaboration between the nodes has gone up. Whereas a purple color on the edge between two nodes indicates that the collaboration between the two nodes has gone down.

Here are a few ways you can interact with the network view to learn more about the insights:

1. **Explore overall group collaboration**. Select a node. You’ll see a breakdown of the collaboration data by sub-groups that constitute the uber group.

    :::image type="content" source="../images/ona-hotspot-1-uber-group.png" alt-text="Screenshot showing the collaboration data breakdown for the uber group.":::

2. **See collaboration trends with other groups**. Hover over the edge connecting two groups in the “after” view to get a perspective into the amount of collaboration and the percent change in collaboration between the two groups in the after period compared to the “before” period. You could also hover over the edge in the “before” view in to examine the extent of collaboration between the two groups.

    :::image type="content" source="../images/ona-hotspot-1-collab-between-groups.png" alt-text="Screenshot showing the collaboration data breakdown between two groups.":::

3. **Explore subgroups**. To view the collaboration data for the individual members of the connecting two groups, select **Expand both groups**. The view will zoom in to those two groups and their members. Hover over each connecting edge see the collaboration changes for individual members. A green edge indicates increased collaboration between members, while a purple edge indicates decreased collaboration.

    >[!Tip]
    > To analyze subgroup members in the matrix view for more quantitative analysis, select **Drill down in matrix**.

    :::image type="content" source="../images/ona-hotspot-1-subgroups-connect.png" alt-text="Screenshot showing the collaboration data amongst subgroup members.":::

    You can also select an individual subgroup node for a more focused look at how that member collaborated with members of the other uber group.  To revert back to the preview view, select one of the uber nodes, then select **Collapse group**.

    :::image type="content" source="../images/ona-hotspot-1-marketing-subgroup.png" alt-text="Screenshot showing the collaboration data for an individual subgroup member.":::

4. **Adjust the view**. Select the plus or minus icon at the top right to zoom in and out. If your mouse has a click wheel, you can also zoom in and out with your mouse.

    :::image type="content" source="../images/ona-hotspot-1-zoom.png" alt-text="Screenshot showing the zoom in and out toggle.":::

5. **Share and download the view**. Select the camera icon to download the current view.

6. **Find a node**. Select the magnifying glass for a list of the groups in your analysis. Select the icon next to any group to navigate to it in the graph.

:::image type="content" source="../images/ona-hotspot-1-find-node.png" alt-text="Screenshot showing the find a node button.":::

**Filtering options:**

>[!Note]
> Any changes you make to the filters below will not change the top highlights or insights provided in the initial summary view.

1. **Filter for different views**. Experiment with the filters **Filter groups** and **Segment groups by** to get different perspectives on the flow of information between groups.

    :::image type="content" source="../images/ona-hotspot-1-filter.png" alt-text="Screenshot showing the filters.":::

2. **Customize time periods**. In the top left of either view, select the dropdown next to the time period to change the timeframe. 

3. **Revisit summary insights**. Want a refresher on key insights? Inside the card at the top of the page, select **View highlights**. You’ll be brought back to the summary page. Just remember, these insights apply to the original “before/after” timeframe you set.

### Full screen view

The “before/after” view described above provides a quick snapshot that shows which groups had big changes and how they collaborated after the change event. To dig deeper into a single “before” or “after” view, you can select the outlined box in the top right of either view to further investigate how groups and subgroups worked together during that time period alone.

Here are a few ways you can explore this view.

1. **Analyze how information flows**. Just like in the “before/after” view, you can select the line connecting any two nodes, then select **Expand both groups** to see how information flowed between subgroups of the larger groups during the selected time period. To analyze collaboration between different groups, select anywhere outside the graph region to reset the view.

2. **Filter for different views**. Like in the “before/after” view, you can use the filters **Filter groups** and **Segment groups by** to get different perspectives on the flow of information between the groups.

3. **Share results**. In the top right of the view, select the camera icon to share a snapshot of the changes with a colleague.

4. **Go back to before/after view**. At the top right, select the arrows. Any time period changes you made in the full screen view will carry over to the “before/after” view.

### Matrix view

The network view provides a visual story of collaboration that’s great for qualitative analysis. But you can also explore the matrix view, which provides the specific numerical analytics on how collaboration changed between groups.

Here’s how to explore the matrix view.

1. **Explore the matrix**. At the top of any network view, under “Visualize as,” select **Matrix**. The matrix shows how collaboration changed between the “before” and “after” time periods. Each cell represents the collaboration change between two groups. The numbers inside each cell signify the change in collaboration among those two groups between the “before” and “after” period. You can toggle between viewing the changes as hours or percentages.

    In this scenario below, for instance, collaboration between Sales and Finance grew by almost 200 percent. The bold outline identifies the change as one of the top highlights from the summary view page:

    :::image type="content" source="../images/ona-hotspot-1-matrix.png" alt-text="Screenshot showing the matrix view.":::

2. **Color shows collaboration changes**. Refer to the gradient chart to see how the different colors correspond to the changes in collaboration.

    :::image type="content" source="../images/ona-hotspot-1-matrix-legend.png" alt-text="Screenshot showing the color gradient legend.":::

3. **Fine-tune your view**. Use the **Filter groups** option to narrow down specific values for the organizational attribute you’ve chosen. 

4. **Switch back to network view**. Under “Visualize as,” select **Graph** to explore the network visualizations within the same “before” and “after” view.

### Matrix view with subgroups

Just like with the network view, you can use the matrix view to analyze collaboration changes between two specific groups and their subgroup members. Here’s how you can explore this view.  

1. **Select your subgroup view**. In the matrix, select the cell of the intersection for the two groups you’d like to analyze. Keep in mind that you can only explore subgroups for two groups while in the matrix view. Select **Expand both groups**.

2. **See the results**. Each cell in the matrix now shows the collaboration changes between each subgroup within the two parent groups you selected. The same color gradient used for the broader matrix view also illustrates the collaboration changes. The example below, for instance, provides the subgroup view for the Finance and Sales groups, segmented by their members. To go back to the previous view without subgroups, at the top left, select **Go back**.

    :::image type="content" source="../images/ona-hotspot-1-matrix-subgroups.png" alt-text="Screenshot showing the matrix view with subgroups.":::

### Metrics used for analysis

The insights provided by the Significant change in collaboration insight category are calculated using the following two metrics:

* **Group collaboration time invested**, which determines the connecting lines between the nodes

* **Group size**, which determines the size of the nodes and the size of the segments around them

Let’s dive a little bit deeper into some of these metrics and how their results are calculated.

#### Group collaboration time invested

This is a group-to-group collaboration metric, and it’s calculated between a primary collaborator and a secondary collaborator. A collaborator is a group of people defined by one or more HR attributes.  

In the scenario below, we’re using two HR attributes to group employees. For example, if the analysis groups employees by organization and by role, a group would be a combination of values from both attributes, like “Engineering_IC” or “Product_Manager.” In this example, Engineering and Product would be values of the organization attribute, and IC and Manager would be values of the role attribute.  

The **Group collaboration time invested** metric is the sum of time spent **in minutes** by each member of the primary group collaborating with members of the secondary group. The metric is computed at a monthly aggregation.  

The output found in a typical .csv file might look like the sample output table below.

| Metric date | Primary Collaborator | Secondary Collaborator | Group collaboration time invested |
|----|----|----|----|
| 11/1/2023   | Engineering_IC    |  Product_IC   | 60 |
| 11/1/2023  | Engineering_Manager   | Product_Manager  | 90 |
| 11/1/2023  | Engineering_IC   | Product_Manager  | 120 |
| 11/1/2023  | Engineering_Manager | Product_IC  | 150 |
| 11/1/2023  | Product_IC | Engineering_IC | 80 |
| 11/1/2023  | Product_Manager | Engineering_Manager | 110 |
| 11/1/2023  | Product_Manager | Engineering_IC | 130 |
| 11/1/2023  | Product_IC | Engineering_Manager | 90 |
| 12/1/2023  | Engineering_IC | Product_IC | 70 |
| 12/1/2023  | Engineering_Manager | Product_Manager | 100 |
| 12/1/2023  | Engineering_IC | Product_Manager | 100 |
| 12/1/2023  | Engineering_Manager | Product_IC | 180 |

For the ONA analysis, however, we perform multiple levels of aggregation on top of the results shown above, to provide a more user-friendly experience. These aggregations include:  

* Aggregation of directional collaboration between groups  

* Aggregation of collaboration across segments to groups

* Aggregation of collaboration across time periods  

The aggregation takes place in the order listed above, whereby aggregation across time periods happens last, based on the time filters the user provides. 

Let’s take a closer look at how each of these aggregations play out.

**Aggregation of directional collaboration between groups**  

We can have the **Group collaboration time invested** metric computed between the same groups in two directions: Group A to Group B, and Group B to Group A. To reduce this complexity, our analysis averages the metric values between Group A to Group B and Group B to Group A.

With this aggregation, the table becomes:

| Metric date | Primary Collaborator | Secondary Collaborator | Group collaboration time invested |
|----|----|----|----|
| 11/1/2023   | Engineering_IC    |  Product_IC   | 70 *(Avg of 60 and 80)*  |
| 11/1/2023  | Engineering_Manager   | Product_Manager  | 100 *(Avg of 90 and 110)* |
| 11/1/2023  | Engineering_IC   | Product_Manager  | 125 *(Avg of 120 and 130)*  |
| 11/1/2023  | Engineering_Manager | Product_IC  | 120 *(Avg of 150 and 90)* |
| 12/1/2023  | Engineering_IC | Product_IC | 70 |
| 12/1/2023  | Engineering_Manager | Product_Manager | 100 |
| 12/1/2023  | Engineering_IC | Product_Manager | 100 |
| 12/1/2023  | Engineering_Manager | Product_IC | 180 |

**Aggregation of collaboration across segments**

We compute the **Group collaboration time invested** metric for a group formed using two HR attributes, like “Organization” and “Role.” We call the first attribute the **GroupBy** attribute, and the second attribute the **SegmentBy** attribute, since the first attribute makes the boundary of the group and the second further segments the group. We compute the metrics at a segment level, to facilitate aggregation to the group level. For this aggregation, we use a simple sum for a given metric date.

With this aggregation, the table becomes:

| Metric date | Primary Collaborator | Secondary Collaborator | Group collaboration time invested |
|----|----|----|----|
| 11/1/2023   | Engineering    |  Product | 415 *(Sum of 70, 100, 125, 120)* |
| 12/1/2023  | Engineering | Product | 480 *(Sum of 70, 100, 100, 180)* |

**Aggregation of collaboration across time periods**

Once the metric has gone through the aggregations mentioned above, we have the correct metric value for a given date. For aggregating the metric across time periods, we sum up all the values.  

With this final aggregation, the table becomes:

| Metric date | Primary Collaborator | Secondary Collaborator | Group collaboration time invested |
|----|----|----|----|
| 11/1/2023 – 12/1/2023  | Engineering    |  Product | 895 *(Sum of 415, 480)* |

#### Group size

Group size functions more like an attribute of a group rather than a metric. In a collaboration, there are two collaborators: “Primary collaborator” and “Secondary collaborator.” The group size is the total number of employees who have been part of a group during the time period of the query.  

The output found in a typical .csv file might look like the sample output table below.
---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 04/02/2024
title: Create change management queries
description: Learn how to use organizational network analysis or ONA to measure the impact on collaboration after a large-scale company change.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
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

:::image type="content" source="../images/ona-analysis-results.png" alt-text="Screenshot showing the ONA query results page." lightbox="../images/ona-analysis-results.png":::

To view the results, find your query under **Query name**, then select the Network icon under **View**.

### Explore insights in summary view

At the top of the screen, you’ll see two cards that provide two categories of insights relevant to your query: **Significant change in collaboration** and **Potential to become insular**. These two cards provide two different types of insights and data points related to collaboration and working patterns.

Let’s now discuss the insights provided by each category, and how you can navigate the ONA experience for each.

## Insight category #1 - Significant change in collaboration

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1k3fg]

### Summary page

**Significant change in collaboration** highlights significant changes in collaboration patterns following the event. You can use this insight category to analyze how collaboration increased or decreased between specific groups, as well as between smaller groups of people or subgroups within the larger groups. For example, with this card, you could analyze the changes in collaboration between the Product and Marketing groups following a reorganization.

[Learn more about how these insights are generated](#metrics-used-for-insight-category-1).

At the top of this summary page, the **People grouped by field** will default to the first HR attribute you selected when defining the analysis. The insights surfaced within the categories and the associated key observations are controlled by the grouping attribute selected. You can also change the attribute here, which will produce different insights.

:::image type="content" source="../images/ona-people-grouped-by.png#lightbox" alt-text="Screenshot showing the People grouped by field.":::

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

:::image type="content" source="../images/ona-hotspot-1-side-by-side.png" alt-text="Screenshot showing the side-by-side view for the first insight category." lightbox="../images/ona-hotspot-1-side-by-side.png":::

Here’s how to interpret this view of nodes:

* The nodes are grouped based on the “People grouped by” selection, and their size is based on the number of people in the group.

* As long as 2 groups have engaged in reciprocal communication in a month and there is a row depicting that communication in the Group-to-Group cross-collaboration query output, then the groups will be surfaced in the network visualization.

* A gray “other” node contains  other groups which have been filtered out of the network view in order to facilitate a more readable network visualization. You can use the **Filter groups** tool described below to display these groups as individual nodes.

* The colors around the nodes represent how the groups are segmented, such as by employee level or geography. The segments that constitute a group is governed by the “Segment groups by” selection.

* The thickness of the line or edge connecting any two nodes is based on the extent of the collaboration change between those groups compared to the “before” view. The thickness of the edges represents the amount of collaboration.

* The color of the edges in the “after” view depicts where collaboration has increased or decreased. A green color on the edge between two nodes indicates that the collaboration between the nodes has gone up. Whereas a purple color on the edge between two nodes indicates that the collaboration between the two nodes has gone down.

Here are a few ways you can interact with the network view to learn more about the insights:

1. **Explore overall group collaboration**. Select a node. You’ll see a breakdown of the collaboration data by sub-groups that constitute the uber group.

    :::image type="content" source="../images/ona-hotspot-1-uber-group.png#lightbox" alt-text="Screenshot showing the collaboration data breakdown for the uber group.":::

2. **See collaboration trends with other groups**. Hover over the edge connecting two groups in the “after” view to get a perspective into the amount of collaboration and the percent change in collaboration between the two groups in the after period compared to the “before” period. You could also hover over the edge in the “before” view in to examine the extent of collaboration between the two groups.

    :::image type="content" source="../images/ona-hotspot-1-collab-between-groups.png#lightbox" alt-text="Screenshot showing the collaboration data breakdown between two groups.":::

3. **Explore subgroups**. To view the collaboration data for the individual members of the connecting two groups, select **Expand both groups**. The view will zoom in to those two groups and their members. Hover over each connecting edge see the collaboration changes for individual members. A green edge indicates increased collaboration between members, while a purple edge indicates decreased collaboration.

    >[!Tip]
    > To analyze subgroup members in the matrix view for more quantitative analysis, select **Drill down in matrix**.

    :::image type="content" source="../images/ona-hotspot-1-subgroups-connect.png" alt-text="Screenshot showing the collaboration data amongst subgroup members." lightbox="../images/ona-hotspot-1-subgroups-connect.png":::

    You can also select an individual subgroup node for a more focused look at how that member collaborated with members of the other uber group.  To revert back to the preview view, select one of the uber nodes, then select **Collapse group**.

    :::image type="content" source="../images/ona-hotspot-1-marketing-subgroup.png#lightbox" alt-text="Screenshot showing the collaboration data for an individual subgroup member.":::

4. **Adjust the view**. Select the plus or minus icon at the top right to zoom in and out. If your mouse has a click wheel, you can also zoom in and out with your mouse.

    :::image type="content" source="../images/ona-hotspot-1-zoom.png#lightbox" alt-text="Screenshot showing the zoom in and out toggle.":::

5. **Share and download the view**. Select the camera icon to download the current view.

6. **Find a node**. Select the magnifying glass for a list of the groups in your analysis. Select the icon next to any group to navigate to it in the graph.

    :::image type="content" source="../images/ona-hotspot-1-find-node.png#lightbox" alt-text="Screenshot showing the find a node button.":::

**Filtering options:**

>[!Note]
> Any changes you make to the filters below will not change the top highlights or insights provided in the initial summary view.

1. **Filter for different views**. Experiment with the filters **Filter groups** and **Segment groups by** to get different perspectives on the flow of information between groups.

    :::image type="content" source="../images/ona-hotspot-1-filter.png#lightbox" alt-text="Screenshot showing the filters.":::

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

    :::image type="content" source="../images/ona-hotspot-1-matrix.png" alt-text="Screenshot showing the matrix view." lightbox="../images/ona-hotspot-1-matrix.png":::

2. **Color shows collaboration changes**. Refer to the gradient chart to see how the different colors correspond to the changes in collaboration.

    :::image type="content" source="../images/ona-hotspot-1-matrix-legend.png#lightbox" alt-text="Screenshot showing the color gradient legend.":::

3. **Fine-tune your view**. Use the **Filter groups** option to narrow down specific values for the organizational attribute you’ve chosen. 

4. **Switch back to network view**. Under “Visualize as,” select **Graph** to explore the network visualizations within the same “before” and “after” view.

### Matrix view with subgroups

Just like with the network view, you can use the matrix view to analyze collaboration changes between two specific groups and their subgroup members. Here’s how you can explore this view.  

1. **Select your subgroup view**. In the matrix, select the cell of the intersection for the two groups you’d like to analyze. Keep in mind that you can only explore subgroups for two groups while in the matrix view. Select **Expand both groups**.

2. **See the results**. Each cell in the matrix now shows the collaboration changes between each subgroup within the two parent groups you selected. The same color gradient used for the broader matrix view also illustrates the collaboration changes. The example below, for instance, provides the subgroup view for the Finance and Sales groups, segmented by their members. To go back to the previous view without subgroups, at the top left, select **Go back**.

    :::image type="content" source="../images/ona-hotspot-1-matrix-subgroups.png" alt-text="Screenshot showing the matrix view with subgroups." lightbox="../images/ona-hotspot-1-matrix-subgroups.png":::

### Metrics used for insight category #1

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

| Metric date | Primary Collaborator | Primary Collaborator Group Size | Secondary Collaborator | Secondary Collaborator Group Size |
|----|----|----|----|-----|
| 11/1/2023   | Engineering_IC    | 30 | Product_IC | 26 |
| 11/1/2023  | Engineering_Manager   | 14 | Product_Manager | 15 |
| 11/1/2023  | Engineering_IC  | 30 | Product_Manager | 15 |
| 11/1/2023  | Engineering_Manager  | 14 | Product_IC | 26 |
| 11/1/2023  | Product_IC  | 22 | Engineering_IC | 32 |
| 11/1/2023  | Product_Manager  | 12 | Engineering_Manager | 16 |
| 11/1/2023  | Product_Manager  | 12 | Engineering_IC | 32 |
| 11/1/2023  | Product_IC  | 22 | Engineering_Manager | 16 |
| 12/1/2023  | Engineering_IC  | 30 | Product_IC | 24 |
| 12/1/2023  | Engineering_Manager  | 14 | Product_Manager | 13 |
| 12/1/2023  | Engineering_IC | 30 | Product_Manager | 13 |
| 12/1/2023  | Engineering_Manager | 14 | Product_IC | 24 |

As you can see, the Group size values for a group plus segment combination can vary between time periods and depending on whether the group is the primary collaborator or secondary collaborator.

To provide the most appropriate Group size number, we perform the below processing of the group size values:  

* Process group size values across collaboration positions

* Process group size values across segments to groups

* Process group size values across time periods

**Group size values across collaboration positions**

Since Group size is based on the number of individual collaborators from a group, it varies depending on whether they are initiating the collaboration (primary collaborators) or participating in the collaboration (secondary collaborators). Because the collaboration is directional, we can call out the Group size values for a group depending on whether it is primary or secondary in the .csv file. But in the ONA query insights, since we make the network direction agnostic, we need to find the right group size value.  

To do this, we consider all the group size values for a given group in either primary or secondary positions, and we pick the maximum value.

**Processing action: Max**

As part of this processing, the aggregated table of collaborations becomes direction-agnostic. The group size values for the direction-agnostic collaborations would look something like this:

| Metric date | Primary Collaborator | Primary Collaborator Group Size | Secondary Collaborator | Secondary Collaborator Group Size |
|----|----|----|----|-----|
| 11/1/2023   | Engineering_IC    | 32 *(Max of 30, 32)*  | Product_IC | 26 *(Max of 22, 26)*  |
| 11/1/2023   | Engineering_Manager  | 16 *(Max of 14, 16)*  | Product_Manager | 15 *(Max of 12, 15)*  |
| 11/1/2023   | Engineering_IC  | 32 *(Max of 30, 32)* | Product_Manager | 15 *(Max of 12, 15)*  |
| 11/1/2023   | Engineering_Manager | 16 *(Max of 14, 16)*  | Product_IC | 26 *(Max of 22, 26)*  |
| 12/1/2023   | Engineering_IC | 30 | Product_IC | 24  |
| 12/1/2023   | Engineering_Manager | 14 | Product_Manager | 13  |
| 12/1/2023   | Engineering_IC | 30 | Product_Manager | 13  |
| 12/1/2023   | Engineering_Manager | 14 | Product_IC | 24 |

**Group size values across segments to groups**

We compute the “Group collaboration time invested” for a group formed using two HR attributes, like “Organization” and “Role”. We call the first attribute the **GroupBy** attribute, and the second attribute the **SegmentBy** attribute, since the first one marks the boundary of the group and the second one further segments the groups. We compute the metrics at a segment level, to facilitate aggregation to the group level. For the aggregation of group size, we use a simple sum for a given metric date.  

With this aggregation, the output table becomes:

| Metric date | Primary Collaborator | Primary Collaborator Group Size | Secondary Collaborator | Secondary Collaborator Group Size |
|----|----|----|----|-----|
| 11/1/2023   | Engineering  | 48 *(Sum of 16, 32)*  | Product | 41 *(Sum of 15, 26)*  |
| 12/1/2023   | Engineering  | 44 *(Sum of 14, 30)*  | Product | 37  *(Sum of 13, 24)*  |

**Group size values across time periods**

Group sizes may vary across the time periods used for the query. One month, the Group size of a group might by 30, and the next month it might be 36. When visualizing the network across both these months, we would need to show a group size that is relatable.  

Therefore, for a given group, we average all the group size values that we have computed per month over the different time periods to come up with the right value to show for the aggregated view. The table then becomes:

| Metric date | Primary Collaborator | Primary Collaborator Group Size | Secondary Collaborator | Secondary Collaborator Group Size |
|----|----|----|----|-----|
| 11/1/2023 - 12/1/2023  | Engineering  | 46 *(Avg of 44, 48)*  | Product | 39 *(Avg  of 37, 41)* |

## Insight category #2 - Potential to become insular

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1k3fj]

### Summary page

The **Potential to become insular** insight category details which groups are connecting more within their own group than expected, in comparison to connecting with other groups outside their own group. This tendency toward within-group collaboration is referred to as “insularity.”

An increase in insularity for a group, for instance, could mean that the group is at risk of becoming siloed from the rest of the organization, which could be a worrisome trend.

[Learn more about how these insights are generated](#metrics-used-for-insight-category-2).

Just like the first insight category, the card provides a list of **top highlights** for this second insight category. Hover over each highlight to see which area of the graph it relates to.

Here is the ranking system we use – from most to least important – to determine these top highlights and the order in which we present them:

1. Significant new increases in insularity, or within-group collaboration, for existing groups following the change event

2. Groups that continue to show insular collaboration patterns in the “before” and “after” time periods

3. Decreases in insularity for groups; in other words, groups that collaborated more closely than expected with other groups following the change event

Now that you’ve got a handle on the top highlights, let’s dive in to the network view for this second insight category. Select **Explore more**.

### Side-by-side view

Just like the first insight category, this view provides a network visualization comprised of nodes. There are some differences with this second insight category, however, in the visual representation of the analysis.

Here’s how to interpret this view of nodes:

* The nodes are still grouped based on your “People grouped by” selection, but now their size is based on the degree of insularity; the bigger the size of the node the more insular a group is.  

* Groups that experienced a significant increase in insular collaboration (i.e. more than expected internal group connectivity) since the change event or groups which continue to showcase insular collaboration across both the before/after periods will also be marked with inward facing triangles, which is meant to indicate that the group is showcasing more internal focus.

* Groups that were previously insular but are no longer insular and are exhibiting more external focus/connectivity in the “after” period will have outward facing triangles around the node’s circumference.

In the scenario below, for instance, the inward facing triangles signify that the Product Management group is exhibiting insular patterns after the change event.

:::image type="content" source="../images/ona-hotspot-2-product-sales-collab.png" alt-text="Screenshot showing insular collaboration for the Product Management group." lightbox="../images/ona-hotspot-2-product-sales-collab.png":::

Here are a few other characteristics of this insight category to be aware of:

* Like the previous insight category, the thickness of the line connecting any two nodes is based on the amount of collaboration between those groups.

* Also like the previous insight category, the colors around the nodes represent how the groups are segmented, such as by employee level or geography. The segments are governed by your **Segment groups by** selection.

Here are a few ways you can interact with this graph to learn more about the insights:

1. **See collaboration trends**. Select any group to see their total collaboration hours, as well as the collaboration activity for each subgroup member, including the percentage of collaboration that was outside the group versus inside the group. You’ll also find the EI index for that group. [Learn more about the EI index and underlying metrics](#metrics-used-for-insight-category-2).

2. **See collaboration trends with other groups**. Select the connecting edge between any two nodes to see how collaboration changed between those specific groups.

3. **Explore subgroups**. Select the node you want to explore further. Then select **Expand group**. The node will show the subgroups that make up the larger group; the subgroup nodes that are contributing towards the insular collaboration behavior of the overarching group will be marked with inward facing triangles. In the below scenario, for instance, Brown, Lee, Miller, Davis, and Jones are subgroups within the Product Management group who are contributing to the insular collaboration behavior of the uber Product Management group. To revert back to the preview view, select the node again, then select **Collapse group**.

    :::image type="content" source="../images/ona-hotspot-2-product-subgroups.png#lightbox" alt-text="Screenshot showing the subgroup members of the Product Management group.":::

4. **Dive deeper into cross-group collaboration between subgroups**. Select the edge that connects any two groups, then select **Expand both groups**. You’ll see a focused view of how the subgroups are collaborating with each other. Hover over each connecting edge see the collaboration changes for individual members. A green edge indicates increased collaboration between members, while a purple edge indicates decreased collaboration. You can also select an individual subgroup node for a more focused look at how that member collaborated with members of the other uber group.

**Filtering options:**

1. **Filter for different views**. Experiment with the filters **Filter groups** and **Segment groups by** to get different perspectives on the flow of information between groups.

2. **Customize time periods**. In the top left of either view, select the dropdown next to the time period to change the timeframe.

3. **Revisit summary insights**. Want another look at the key insights? Inside the card at the top of the page, select **View highlights**. You’ll be brought back to the summary view. These insights apply to the original “before/after” timeframe you set.

### Full screen view

The “before/after” view described above provides a quick snapshot that shows which groups had changes in insularity and how they collaborated after the change event. To dig deeper into a single “before” or “after” view, you can select the outlined box in the top right of either view to investigate how groups and subgroups worked together during that time period alone.

Here are a few ways you can explore this view.

1. **Analyze cross-group collaboration between subgroups**. Select the edge connecting any two nodes Then select **Expand both groups** to see how members of the two uber groups collaborated with each other, just like you would in the “before/after” view described above.

2. **Share results**. In the top right of the view, select the camera icon to share a snapshot of the changes with a colleague.

3. **Go back to before/after view**. At the top left, select the arrows. Any time period changes you made in the full screen view will carry over to the “before/after” view.

### Chart view

The network view provides a visual story of insularity that’s great for qualitative analysis. But you can also explore the chart view for this insight category, which provides the specific numerical analytics on insularity within groups and between groups.

Here’s how to explore the chart view.

1. **Explore the chart**. At the top of any network view, under “Visualize as,” select **Chart**. The chart showcases whether a group is leaning more towards insular behavior (i.e. more than expected within-group collaboration) or if a group is more inclined towards external-ness (i.e., more than expected outside-group collaboration). For any given group, a dark blue circle indicates the “after” state whereas the lighter blue circle indicates the “before” state.

2. **Circle color and movement show collaboration changes**. Movement from the right to the left (past the mid-point of the chart) illustrates more than expected within-group connectivity– or increased insularity – for that group following the change event. Movement from left to right (past the mid-point of the chart) represents an inclination towards more than expected outside of group connectivity. In the scenario below, for instance, the Sales, and G&A groups are tending towards more insular collaboration behavior, as denoted by the movement of their darker circles from right to left:

    :::image type="content" source="../images/ona-hotspot-2-chart-insular.png" alt-text="Screenshot showing the chart view for several groups." lightbox="../images/ona-hotspot-2-chart-insular.png":::

3. **Fine-tune your view**. Use the **Filter groups** option to narrow down specific values for the grouping attribute you’ve chosen.

4. **Explore subgroups**. Within the chart view, you can also analyze changes in insularity for subgroups within the larger groups. To do so, select the dropdown to the left of the group you want to analyze. Individual bars will appear for each of the subgroups which show the changes in insularity for those subgroups.

    For instance, in the example below, Miller’s collaboration time within the R&D group increased to nearly 92 percent following the change event.

    :::image type="content" source="../images/ona-hotspot-2-chart-subgroups.png" alt-text="Screenshot showing the chart view with subgroups for the R&D group." lightbox="../images/ona-hotspot-2-chart-subgroups.png":::

5. **Switch back to network view**. Under “Visualize as,” select **Graph** to explore the network visualizations within the same “before” and “after” view.

### Metrics used for insight category #2

The insights provided by the Potential to become insular insight category are calculated using the following three metrics:

* **Group collaboration time invested**, which determines the connecting lines between the nodes

* **EI index**, which determines the size of the nodes

* **Group size**, which determines the size of the segments around the nodes  

Let’s dive a little bit deeper into the EI index metric and how its results are calculated.

#### EI index

The EI index provides an indication of the size of an imbalance between external and internal ties of an individual. External and internal are relative to a defined group within the organization. No person can belong to more than one group.  The EI index was designed to test how well organizations respond to crises.  The original study suggested that organizations performed better when employees were strongly connected to many other employees outside of their own group compared to organizations where employees’ connections were concentrated within their same group.

The index value is between –1 (when all collaboration is within the group) and +1 (when all communication is with other groups). A value of 0 represents an equal amount of within-group and cross-group collaboration.

A value of –0.67 corresponds to a 5:1 in-group to cross-group collaboration ratio. Therefore, values between –0.67 and –1 indicate that a group might be at risk of being siloed. A value of exactly –1 indicates that the group is completely siloed. Values between 0 and –0.67 may also indicate insular collaboration patterns, though there is a lower risk of the group becoming siloed.

For individuals, an external tie for person A is defined as someone to whom person A is connected and has a different HR attribute value than person A. An internal tie for person A is defined as someone to whom person A is connected and has the same HR attribute value as person A. HR attributes can represent organizational hierarchy, demographic information, hybrid working styles, and so on. For this documentation, let us consider the same two HR attributes, **Organization** and **Role**, to group the employees. As part of the report, we compute the EI index of individuals using both the HR attributes as context and we aggregate it to a group level before we output the metric values.

In the .csv file, we aggregate the EI index metric value to the segment level as shown below. The .csv output would contain the EI index value of segments for both the HR attributes. For the purposes of the documentation, we’re showcasing only the EI index based on the Organization attribute.

| Metric date | Primary Collaborator | Primary Collaborator  Organization EI index  | Secondary Collaborator | Secondary Collaborator Organization EI index  |
|----|----|----|----|-----|
| 11/1/2023 | Engineering_IC  | -0.40 | Product_IC | 0.20 |
| 11/1/2023 | Engineering_Manager  | 0.15 | Product_Manager | 0.30 |
| 11/1/2023 | Engineering_IC | -0.40 | Product_Manager | 0.30 |
| 11/1/2023 | Engineering_Manager | 0.15 | Product_IC | 0.20 |
| 12/1/2023 | Engineering_IC | -0.30 | Product_IC | 0.30 |
| 12/1/2023 | Engineering_Manager | 0.05 | Product_Manager | 0.10 |
| 12/1/2023 | Engineering_IC | -0.30 | Product_Manager | 0.10 |
| 12/1/2023 | Engineering_Manager | 0.05 | Product_IC | 0.30 |

Here you can see that the EI index value for a segment (Organization_Role) is constant for a given metric date regardless of whether that group is a primary collaborator or secondary collaborator.  

As you can see, the EI index in the .csv is provided at the segment level and varies from time to time. In the ONA product, we facilitate users to analyze the groups based on either of the attributes, and segments based on either of the attributes. That is, we support analysis when the GroupBy attribute is Organization and the SegmentBy attribute is Role, and vice versa. We also support understanding the network across various time periods. For this purpose, we perform some aggregation of the metrics in the UX.  

In the UX, we perform the following processing steps on the EI index values:

* Process EI index values across segments to groups

* Process EI index values across time periods

**Process EI index values across segments to groups**

EI index values can be aggregated from the individual level to the segment and group level. To aggregate the EI index values from individuals to the segment Engineering_IC, we need to average the EI index values of all individuals in this segment. This is the number we provide as part of the .csv.  

For the UX, we need to aggregate the individual EI index values to a group level instead of a segment level, such as to get EI index value of Engineering. This can be done in two ways.

* Perform an average of the EI index value of all individuals in the group

* Perform a weighted average of the EI index values of all segments in the group

We are using the second approach to aggregate the EI index values for segments to the group.

**Processing action:** Weighted Average. Weight is greater than or equal to group size.

| Metric date | Primary Collaborator | Primary Collaborator  Organization EI index  | Secondary Collaborator | Secondary Collaborator Organization EI index  |
|----|----|----|----|-----|
| 11/1/2023 | Engineering  | -0.27 <br /> <br /> *=((-0.40*32 + 0.15*16) / 32 + 16)*  | Product | 0.24 <br /><br />  *=((0.20*26 + 0.30*15) / 26 + 15)*  |
| 12/1/2023 | Engineering | -0.19 <br /><br /> *=((-0.30*30 + 0.05*14) / 30 + 14)*  | Product | 0.23 <br /><br /> *=((0.30*24 + 0.10*13) / 24 + 13)*  |

Please refer to the group size of these segments in the previous section.

**Process EI index values across time periods**

Aggregating EI index scores for the same group or segment across time periods is like the segment to group value aggregation. We perform a weighted average of the EI index values using the group or size of the groups or segments from the respective months to derive the EI index value of the entity across time periods.

**Processing action:** Weighted Average. Weight is greater than or equal to group size.

| Metric date | Primary Collaborator | Primary Collaborator  Organization EI index  | Secondary Collaborator | Secondary Collaborator Organization EI index  |
|----|----|----|----|-----|
| 11/1/2023 - 12/1/2023  | Engineering  | -0.23 <br /> <br /> *=((-0.27*48  -0.19*44) / 48 + 44)*  | Product | 0.24 <br /><br />  *=((0.24*41 + 0.23*37) / 41 + 37)*  |

Please refer to the group size of these segments in the previous section.
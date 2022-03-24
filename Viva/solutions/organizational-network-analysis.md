---
title: Organizational network analysis
description: Explains how to use Organizational network analysis in concert with Viva Insights queries
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: helayne
audience: Admin
---

# Organizational network analysis

Organizational network analysis (ONA) is a structured way to analyze how communications occur within the organization. Workplace Analytics with Viva Insights has a variety of measures to help you visualize and analyze relationships within your organization and get visibility and understanding into individual and team productivity, innovation, organizational change, etc. The analysis can also help you shape a business strategy that improves communication, making your business more effective and sustainable.

## Who should be included in the analysis?

To identify the network boundary:

1. Use hypotheses about how work gets done to inform boundary-setting for analysis (like Division or Business unit).

2. Confirm the network population in question is fully licensed with Viva Insights.
Think about how work gets done in your organization to inform who to include in the analysis. Maybe you want to analyze the entire network, or maybe you’re interested in interactions within one particular group.

Keep in mind that for any employee not included in the network, the information pathways to/from these employees will be excluded. So, if you were to choose people at random, it would result in an inaccurate understanding of the network.

If you choose to analyze HR only, you will get visibility only into collaboration within the HR group. For accurate analysis, ensure your network population is fully licensed.

:::image type="complex" source="images/ona-population-segment.png" alt-text="Screenshot of a network diagram":::
   Screenshot of a network diagram
:::image-end:::

### ONA datasets

Viva Insights provides the following out-of-the-box ONA queries.

#### Person-level analysis

##### Network person query

Metrics provided: **Influencer** and **Influencer rank**. Metric definitions can be found [here](../insights/use/metric-definitions#network-metrics).

<!--"influence index" vs. "influence metric" in review-->

**Influence** is a score of how well connected an employee is in the organization. If an employee is connected to others who are well connected, the employee will benefit from these connections. Employees with a higher **Influence** metric are more likely to connect effectively within or across groups to drive change.

Use the Network person query to analyze the influence metric in the measured population. Aggregate the metric by attribute—like team, level, or location—to rank, compare, and contrast influencers in the organization.

##### Network person-to-person query

Metrics provided: **Strong** and **Diverse tie** scores. Metric definitions can be found [here](../insights/use/metric-definitions#network-metrics).

Network ties are connections between employees with at least two meaningful interactions. **Strong ties** have many connections in common, and **Diverse ties** have fewer connections in common. Groups with many **Diverse ties** can represent teams with high innovative potential.

Use the **Network person-to-person query** to analyze **Strong** and **Diverse ties** between individuals or groups in the measured population.

**Which Viva Insights ONA measure is right for me?**

|Influence index   |Strong/Diverse ties  |
|----------|-----------|
|Are there individuals in the organization with many well-connected connections? Where?  |Where in the organization are employees connected in their group vs connected with others outside their group?       |
|How can we improve communication on strategic initiatives? |Where should we encourage connectivity to foster innovation?   |
|How can we accelerate improvement plans for the organization?|Are there inefficiencies that suggest opportunity to improve team cohesion?

Additionally, you can leverage the **Group-to-group** and **Person-to-group** queries to generate a person-level interaction matrix for analysis.

##### Group-to-group query transformed into person-to-person query

<!---revisit "these queries..."--->

Use these queries to analyze and graph the collaboration patterns within your organization at the group-to-group or person-to-person level through metrics like collaboration hours or meeting counts. You can apply open-source ONA tools on this type of data for visualization purposes or for more in-depth ONA analysis.

Person-to-person query is a transformation of the Group-to-group query, with an assigned identifier for each person to use as the “group.” This is a specialized technique that requires privacy approval.

Refer to [Dataset preparation](#you-can-use-network-person-to-person-query-results-as-a-form-of-person-to-person-interaction-matrix-along-with-open-source-ona-tools-however-please-consider-the-limitations-mentioned-in-the-ona-datasets-section-above) to learn how to transform Group-to-group queries into Person-to-person queries.

#### Group-level analysis

##### Group-to-group query

Use a **Group-to-group query** to analyze collaboration patterns between teams, understand where groups are investing their collaboration time, and identify silos and bridging organizations.

##### Network person-to-person query

> [!NOTE]
> In this section, we share detailed information on how the **Network person-to-person query** metrics are generated and filtered.
> This information highlights the differences between the underlying interaction matrix and the query results to provide guidance on:
> * identifying the correct application and usage of the query metrics, and
> * correctly interpreting the analysis.

The underlying person-to-person matrix for ONA calculations is defined based on these interactions:

* **Meetings** with a maximum of 18 attendees
* **Emails** with a maximum of 18 recipients
* **Meetings and calls** with a maximum duration of four hours
* **Chats and calls** with a minimum of two and a maximum of eight participants

    Missed calls and voicemails are excluded from calls. The total time of these interactions is allocated equally between each pair of participants.

This underlying matrix is then filtered and applied in the various network algorithms to produce the network measures available in query format. This means that any result from the network queries in the analyst tool will not match the underlying person-to-person matrix.

The **Network person-to-person query** or the **Strong/Diverse ties** algorithm filters the underlying person-to-person matrix to those interactions where two individuals had 10 or more minutes of interaction per month. This algorithm filters out approximately 40% of the connections present in the underlying person-to-person matrix. Additionally, there is no custom control in the analyst tool where an analyst can specify which collaboration signals to include or how much time represents meaningful connections. Finally, analysts should not use the scores in the **Strong/Diverse ties** query output as edge weights between individuals, because those weights do not represent time spent between two individuals or count of interactions. If an analyst were to do that, it would lead to inaccurate results.

The **Strong ties** algorithm also considers the common network between two people and their interaction with the common network while computing the score. The **Diverse ties** algorithm, meanwhile, considers the non-overlapping network and interactions with the non-overlapping network. So, the results represent a score that’s different from a generic person-to-person interaction. Using **Strong ties** as a proxy or in place of person-to-person interaction as a graph would result in biased results based on what further computation is performed on that result.

Take this example: an analyst uses **Strong ties** as a proxy for person-to-person interaction to compute communities. Their result will have biased communities since the **Strong tie** score computation already biases results towards common networks. Therefore, **Strong/Diverse ties** should be used for analysis of ties and not as a proxy.

Similar logic applies to the **Group-to-group query** transformed into **person-to-person query**. A **Group-to-group** query has its own computation logic, and based on inputs, its result would be different from a generic person-to-person interaction matrix.

#### Dataset preparation

To run each of the following queries:

* **Network person query**: Follow the steps in [Network person queries](/Viva/insights/Tutorials/ona-person-query.md).

* **Network person-to-person query**: Follow the steps in [Network person-to-person queries](/Viva/insights/Tutorials/ona-person-to-person-query.md)

* **Group-to-group query**: Follow the steps in [Group-to-group queries](/Viva/insights/Tutorials/Group-to-group-queries.md). A list of metrics is provided [here](/Viva/insights/Use/Metric-definitions#group-to-group-metrics.md).

* **Person-to-person query** via **Group-to-group query**: Refer to the following section.

##### Person-to-person query via Group-to-group query

Workplace Analytics doesn't have a Person-to-person query as an out-of-the-box query template. However, you can turn a **Group-to-group query** into a Person-to-person query by following this guidance.

**PersonId**, the main person identifier in the Workplace Analytics Organizational data, will be hashed (de-identified) in your reports and not available to be selected as your group **Collaborator** in the **Group-to-group query**. However, if you add an additional person identifier to your HR org file when uploading (that is, you generate a column that has anonymized PersonId for each person), you can use that metric in **Time investors** and **Their collaborators** sections of the **Group-to-group query** to change the group collaboration to a person-level collaboration. In the following image, **zId** is that additional person identifier.

<!-- should explictly state that folks need to choose zID-->

> [!IMPORTANT]
> Make sure the additional person identifier (**zId**) is not an employee ID or any identifiable number that would allow the analyst to identify and analyze the interactions at the person level. For privacy reasons, Workplace Analytics de-identifies the **PersonId** by default when the HR org file is uploaded.

:::image type="complex" source="images/ona-zid.png" alt-text="Screenshot of Workplace Analytics query designer step 2":::
   Screenshot that shows the Workplace Analytics Query designer's interface. Under step 2, Time Investors, zID is selected from the dropdown menu beneath the prompt, How do you want to group the time investors.
:::image-end:::

To create the interaction matrix (or Edge list) for the ONA calculation, open a **Group-to-group query**:

1. Navigate to the **Query designer > Group-to-group query in Workplace Analytics**.
2. Set up a query with your desired data aggregation level and time period.
3. Select metrics, like **Collaboration hours**, **Email hours**, and **Meeting hours**. Set filters as needed.
4. Select the **zId** in the **Their collaborators** and **Organizational data** sections of the **Person-to-group query**.
5. Run the query and export the results once the run is complete.
6. In the exported file, select the following columns and rename as indicated in this table:

|Original name|New name|
|-------------|---------|
TimeInvestors_zId (zId)|Source
Collaborators_zId |Target
Collaboration_hours (or any other metric that you prefer to be used) |Weight/ONAmetric

> [!NOTE]
> If you want to see the metrics available in the Person-to-group query (like email counts) as part of the interaction table, you can transform the **Person-to-group query** to a **Person-to-person query** using the same process as steps 1-6 above.
> In this case, the selection and renaming of the columns should match the following table:

<!--Below is in review; appears to be the same info-->

|Original name|New name|
|-------------|---------|
TimeInvestors_zId (zId)|Source
Collaborators_zId |Target
Collaboration_hours (or any other metric that you prefer to be used) |Weight/ONAmetric

The list of **Person-to-group query metrics** is available [here](/Viva/insights/Use/Metric-definitions#person-to-group-metrics.md).

### ONA analysis

#### Network person query

<!--Below is in review-->

Within Workplace Analytics, you can find visualizations of the **Influence** metric in two places:

**Accelerate change**, which you can reach from the **Accelerate change** card on the home page.

:::image type="content" source="images/ona-find-accelerate-change.png" alt-text="Screenshot of Workplace Analytics Accelerate change page":::

:::image type="complex" source="images/ona-accelerate-change.png" alt-text="Screenshot of Workplace Analytics Accelerate change page":::
   Screenshot that shows the Workplace Analytics Accelerate change page. The sub-header reads, Engage influencers, and the text below reads, Leveraging the right people to promote new technology can help drive adoption at scale. Well-connected people share information efficiently and are not always easy to identify. Beneath the introductory text is a metric in large font that reads, 2% of employees can drive change with 60% of your workforce. A graph showing a network is displayed below a header that reads, Reach of influencers. Graph and percentage displayed on this page draw data from the Influence metric.
:::image-end:::

**Accelerate decision making**, which you can reach from the **Improve agility** card on the home page.

##### Where are the influencers?

Through Power BI or any other visualization tool, you can create simple visuals to explain the results of the Network person query—that is, the distribution of influencers and where the top influencers in the company are placed. The following image shows an example Power BI visual.
 
To see a sample analysis of the Network person query result, view the one we created here in Power BI.

##### Cohort analysis

You can also leverage cohort analysis to understand similar characteristics of top influencers. Identifying influencer cohorts can help create actionable insights, which can help effect a change in a company.

Here’s a simple way to create a cohort analysis:

1. Run a **Network person query**.
2. Select a population of top influencers based on the Influence metric: 
    1. Set a threshold or sort based on the Influence metric.
    1. Select the top 10% of the whole company population.
3. Flag the selected individuals in step 2 as influencers.
4. Pivot the data in Excel with various HR attribute combinations using the flag in step 3.

To see a sample manual cohort analysis, view the one we created here in Excel.

#### Network person-to-person query

Creating bidirectional charts (like doughnut, Sankey, and chord) in visualization tools like Power BI is a good first step to identify connection patterns. The following images show a few sample visuals:
  
You can use **Network person-to-person query** results as a form of person-to-person interaction matrix along with open-source ONA tools. However, please consider the limitations mentioned in the ONA datasets section above.

#### Group-to-group query

You can use Power BI visualizations—for example, matrix heatmap and network visualizations like Network Navigator—to reveal collaboration patterns between groups.
 
#### Person-to-person data export using Group-to-group or Person-to-group queries

Network analysis and visualization tools are the best 

### Tools for advanced ONA query analysis

#### wpa R package

wpa R package is an open-source R library of over 180 tools and functions for analyzing and visualizing data from Microsoft Viva Insights. The package is publicly available on GitHub and published on CRAN.

##### Functions

* **Group-to-group queries**: To analyze and visualize Group-to-group queries, use `network_g2g()`.
 
* **Person-to-person queries**: To analyze and visualize person-to-person queries, use `network_p2p()`. This function has the added capability to perform community detection.
 
#### Gephi

Gephi is the leading visualization and exploration software for all kinds of graphs and networks. Gephi is a great tool for:

* Visualizing and interacting with large graphs
* Adding extra attributes to nodes and partitioning a graph based on those attributes
* Sizing nodes based on attributes and nodes graph measures like degree, weighted degree, etc.
* Comparing partitions based on different attributes with static visualization of the network
* Filtering the network based on attributes and working in subgraphs
* Calculating standard network statistics like degree, network diameter, and density

##### Gephi handbook

The Gephi handbook provides instructions on:

* Installing Gephi
* Running Viva Insights queries and transforming the results
* Configuring Gephi to create a Person-to-person and Group-to-group visualization

The Gephi handbook and a sample template are available here.

#### FindingCohorts Python script

The FindingCohorts Python script provided on GitHub is a machine-learning-based solution to identify cohorts and common characteristics of the top influencers in a population.

Before you use the script, run a Network person query with Influence_rank and Influence metrics and HR attributes included.

Then:

1. Download the script from GitHub. To make sure the script can successfully read the input data, modify the script as necessary in **Step 1: read the input file**.
2. Configure the parameters in **Step 1: read the input file**.
3. Complete **Step 2: Add isInfluencer flag**, **Step 3: Training a DecisionTree model**, and **Step 4: DecisionTree text representation**.

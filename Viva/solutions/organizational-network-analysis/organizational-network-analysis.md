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

1. Think about how work gets done in your organization to inform who to include in the analysis. Maybe you want to analyze the entire network, or maybe you’re interested in interactions within one particular group (like Division or Business unit).

2. Confirm the network population in question is fully licensed with Viva Insights.


Keep in mind that for any employee not included in the network, the information pathways to/from these employees will be excluded. So, if you were to choose people at random, it would result in an inaccurate understanding of the network. If you choose to analyze HR only, you will get visibility only into collaboration within the HR group. For accurate analysis, ensure your network population is fully licensed.

:::image type="complex" source="../images/ona-population-segment(2).png" alt-text="Screenshot of a network diagram":::
   Screenshot that shows a network diagram with dots of various colors. One section on the right-hand side of the diagram is encircled in yellow and labeled, "Population segment included in the analysis."
:::image-end:::

## ONA datasets

Viva Insights provides the following out-of-the-box ONA queries.

### Person-level analysis

#### Network person query

* **Metrics provided**: **Influencer** and **Influencer rank**

    * **Influence** is a score of how well connected an employee is in the organization. If an employee is connected to others who are well connected, the employee will benefit from these connections. Employees with a higher **Influence** metric are more likely to connect effectively within or across groups to drive change. Find metric definitions [here](/viva/insights/use/metric-definitions#network-metrics).
* **How to use the query**: Use the **Network person query** to analyze the influence metric in the measured population. Aggregate the metric by attribute—like team, level, or location—to rank, compare, and contrast influencers in the organization.

#### Network person-to-person query

* **Metrics provided**: **Strong** and **Diverse tie** scores
    * Network ties are connections between employees with at least two meaningful interactions. **Strong ties** have many connections in common, and **Diverse ties** have fewer connections in common. Groups with many **Diverse ties** can represent teams with high innovative potential. Find metric definitions [here](/viva/insights/use/metric-definitions#network-metrics).
* **How to use the query**: Use the **Network person-to-person query** to analyze **Strong** and **Diverse ties** between individuals or groups in the measured population.

#### Which Viva Insights ONA measure is right for me?

To help determine whether to use **Influence** index or **Strong/Diverse ties**, consult the following table.

|Influence index   |Strong/Diverse ties  |
|----------|-----------|
|Are there individuals in the organization with many well-connected connections? Where?  |Where in the organization are employees connected in their group vs connected with others outside their group?       |
|How can we improve communication on strategic initiatives? |Where should we encourage connectivity to foster innovation?   |
|How can we accelerate improvement plans for the organization?|Are there inefficiencies that suggest opportunities to improve team cohesion?

Additionally, you can leverage the **Group-to-group** and **Person-to-group** queries to generate a person-level interaction matrix for analysis.

##### Person-to-person query through a Group-to-group query

To analyze and graph the collaboration patterns within your organization at the group-to-group level, through metrics like collaboration hours or meeting counts, you can use a **Group-to-group query**. You can apply open-source ONA tools on this type of data to visualize it, or to perform more in-depth ONA analysis.

This type of analysis is possible at the person-to-person level, too. Workplace Analytics doesn't have a **Person-to-person query** as an out-of-the-box query template; however, you can create a **Person-to-person query** by transforming the **Group-to-group query**. You'll use an assigned identifier for each person to use as the “group.” This is a specialized technique that requires privacy approval.

Refer to [Dataset preparation](#dataset-preparation) to learn how to transform **Group-to-group queries** into **Person-to-person queries**.

### Group-level analysis

#### Group-to-group query

Find list of metrics and their definitions [here](/viva/insights/use/metric-definitions#group-to-group-metrics).

Use a **Group-to-group query** to analyze collaboration patterns between teams, understand where groups are investing their collaboration time, and identify silos and bridging organizations.

#### Filtering and assumptions applied on interaction data

> [!NOTE]
> In this section, we share detailed information on how the **Network person-to-person query** metrics are generated and filtered.
> This information highlights the differences between the underlying interaction matrix and the query results to provide guidance on:
> * identifying the correct application and usage of the query metrics, and
> * correctly interpreting the analysis.

##### Underlying interaction matrix filtering

The underlying person-to-person matrix for ONA calculations is defined based on these interactions:

* **Meetings** with a maximum of 18 attendees
* **Emails** with a maximum of 18 recipients
* **Meetings and calls** with a maximum duration of four hours
* **Chats and calls** with a minimum of two and a maximum of eight participants

    Missed calls and voicemails are excluded from calls. The total time of these interactions is allocated equally between each pair of participants.

##### Queries and algorithms

The underlying matrix is then filtered and applied in the various network algorithms to produce the network measures available in query format. This means that any result from the network queries in the analyst tool will not match the underlying person-to-person matrix.

The **Network person-to-person query** or the **Strong/Diverse ties** algorithm filters the underlying person-to-person matrix to those interactions where two individuals had 10 or more minutes of interaction per month. This algorithm filters out approximately 40% of the connections present in the underlying person-to-person matrix. Additionally, there is no custom control in the analyst tool where an analyst can specify which collaboration signals to include or how much time represents meaningful connections. Finally, analysts should not use the scores in the **Strong/Diverse ties** query output as edge weights between individuals, because those weights do not represent time spent between two individuals or count of interactions. Doing so would lead to inaccurate results.

The **Strong ties** algorithm also considers the common network between two people and their interaction with the common network while computing the score. The **Diverse ties** algorithm, meanwhile, considers the non-overlapping network and interactions with the non-overlapping network. So, the results represent a score that’s different from a generic person-to-person interaction. Using **Strong ties** as a proxy or in place of person-to-person interaction as a graph would result in biased results based on what further computation is performed on that result.

Take this example: an analyst uses **Strong ties** as a proxy for person-to-person interaction to compute communities. Their result will have biased communities since the **Strong tie** score computation already biases results towards common networks. Therefore, **Strong/Diverse ties** should be used for analysis of ties and not as a proxy.

Similar logic applies to a **Group-to-group query** transformed into a **Person-to-person query**. A **Group-to-group** query has its own computation logic, and based on inputs, its result would be different from a generic person-to-person interaction matrix.

## Dataset preparation

To run each of the following queries:

* **Network person query**: Follow the steps in [Network person queries](/viva/insights/tutorials/ona-person-query).

* **Network person-to-person query**: Follow the steps in [Network person-to-person queries](/viva/insights/tutorials/ona-person-to-person-query).

* **Group-to-group query**: Follow the steps in [Group-to-group queries](/viva/insights/tutorials/group-to-group-queries). A list of metrics is provided [here](/viva/insights/use/metric-definitions#group-to-group-metrics).

* **Person-to-person query** through a **Group-to-group query**: Refer to the following section.

### Turning a Group-to-group query into a Person-to-person query

As mentioned earlier, Workplace Analytics doesn't have a **Person-to-person query** as an out-of-the-box query template. However, you can turn a **Group-to-group query** into a **Person-to-person query** by following this guidance.

**PersonId**, the main person identifier in the Workplace Analytics Organizational data, will be hashed (de-identified) in your reports and not available to be selected as your group **Collaborator** in the **Group-to-group query**. However, if you add an additional person identifier to your HR org file when uploading (that is, you generate a column that has anonymized PersonId for each person), you can use that metric in **Time investors** and **Their collaborators** sections of the **Group-to-group query** to change the group collaboration to a person-level collaboration. In the following image, **zId** is that additional person identifier.

> [!IMPORTANT]
> Make sure the additional person identifier (**zId**) is not an employee ID or any identifiable number that would allow the analyst to identify and analyze the interactions at the person level. For privacy reasons, Workplace Analytics de-identifies the **PersonId** by default when the HR org file is uploaded.

:::image type="complex" source="../images/ona-zid(1).png" alt-text="Screenshot of Workplace Analytics Query designer step 2":::
   Screenshot that shows the Workplace Analytics Query designer's interface. Under step 2, Time Investors, zID is selected from the dropdown menu beneath the prompt, "How do you want to group the time investors".
:::image-end:::

To create the interaction matrix (or Edge list) for the ONA calculation, open a **Group-to-group query**:

1. In Workplace Analytics, navigate to the  **Query designer > Group-to-group query**.
2. Set up a query with your desired data aggregation level and time period.
3. Select metrics, like **Collaboration hours**, **Email hours**, and **Meeting hours**. Set filters as needed.
4. Select the **zId** under **Time investors** and **Their collaborators**.
5. Run the query and export the results once the run is complete.
6. In the exported file, select the following columns and rename as indicated in this table:

|Original name|New name|
|-------------|---------|
TimeInvestors_zId (zId)|Source
Collaborators_zId |Target
Collaboration_hours (or any other metric that you prefer to be used) |Weight/ONAmetric

> [!NOTE]
> If you want to see the metrics available in the Person-to-group query (like email counts) as part of the interaction table, you can transform the **Person-to-group query** to a **Person-to-person query** using the same process as steps 1-6 above (in step 4, Select the **zId** in the **Their Collaborators** and **Organizational data** sections of the query).
> In this case, the selection and renaming of the columns should match the following table:

|Original name|New name|
|-------------|---------|
zId (zId)|Source
Collaborators_zId |Target
Collaboration_hours (or any other metric that you prefer to be used) |Weight/ONAmetric

The list of **Person-to-group query metrics** is available [here](/viva/insights/use/metric-definitions#person-to-group-metrics).

### ONA analysis

#### Network person query

Within Workplace Analytics, you can find visualizations of the **Influence** metric in two places:

* **Accelerate change**, which you can reach from the **Accelerate change** card on the Home page.

    :::image type="content" source="../images/ona-find-accelerate-change.png" alt-text="Screenshot of Workplace Analytics Home page, with nine behavior cards; 'Accelerate change is highlighted'":::

    :::image type="complex" source="../images/ona-accelerate-change.png" alt-text="Screenshot of Workplace Analytics Accelerate change page":::
   Screenshot that shows the Workplace Analytics Accelerate change page. The sub-header reads, "Engage influencers," and the text below reads, "Leveraging the right people to promote new technology can help drive adoption at scale. Well-connected people share information efficiently and are not always easy to identify." Beneath the introductory text, on the left side of the image, is a metric in large font that reads, "2% of employees can drive change with 60% of your workforce." Beneath the metric are two hyperlinks: "Supporting evidence" and "How we define the reach of influencers," which includes a tooltip. On the right side of the image, a network diagram is displayed below a header that reads, "Reach of influencers." Diagram and percentage displayed on this page draw data from the Influence metric.
:::image-end:::

Learn more about **Accelerate change** [here](/viva/insights/use/accelerate-change#accelerate-change-with-viva-insights).

* **Accelerate decision making**, which you can reach from the **Improve agility** card on the Home page.

    :::image type="content" source="../images/ona-find-accelerate-decision-making.png" alt-text="Screenshot of Workplace Analytics Home page, with nine behavior cards; 'Improve agility' is highlighted":::

    :::image type="complex" source="../images/ona-accelerate-decision-making.png" alt-text="Screenshot of Workplace Analytics Improve agility page":::
   Screenshot that shows the Accelerate decision making section of the Workplace Analytics Improve agility page. A sub-header reads, "Accelerate decision making," and the text below it reads, "Agile organizations are transparent and freely share information to avoid miscommunication and enable smart and timely decision making." Beneath the introductory text, on the left side of the image, is a metric in large font that reads, "36% of employees could be empowered to make faster decisions." Beneath the metric are two hyperlinks: "Supporting evidence" and "How we define the reach of influencers," which includes a tooltip. On the right side of the image, a network diagram is displayed below a header that reads, "Employee empowerment." Diagram and percentage displayed on this page draw data from the Influence metric.
:::image-end:::

Learn more about **Accelerate decision making** [here](/viva/insights/use/improve-agility#accelerate-decision-making).

##### Where are the influencers?

Through Power BI or any other visualization tool, you can create simple visuals to explain the results of the Network person query—that is, the distribution of influencers and where the top influencers in the company are placed.

:::image type="complex" source="../images/ona-influencerank.png" alt-text="Screenshot of a box-and-whisker chart that displays results from the Network person query":::
   Screenshot that shows three colorful box-and-whisker charts. The first chart is titled, "Average of InfluenceRank by leveldesignation and organization." The X axis contains job titles Senior Executive, Executive, Director, Manager, Senior IC, Junior IC, and Support. The Y axis ranges from -0.20K to 1.40K, increasing by increments of .20. Box-and-whisker points are composed of various thicknesses and whisker ranges. The second chart is titled, "Average of InfluenceRank by functiontype and organization." The X axis contains different business segments: Marketing, Product Management, HR, G&A, Sales, R&D, and Operations. The Y axis ranges from 0.20K to 1.10K, increasing by increments of .10. Box-and-whisker points are composed of various thicknesses and whisker ranges. The third chart is titled, "Average of InfluenceRank by region and organization." The X axis contains geographical areas: Central, East, South, and West. The Y axis ranges from 0.20K to 1.10K, increasing by increments of .10. Box-and-whisker points are composed of various thicknesses and whisker ranges.
:::image-end:::

To see a sample analysis of the Network person query result, view the one we created [here](<https://github.com/microsoft/VivaSolutions/tree/main/Sample Solutions/ONA/SampleAnalysis>) in Power BI.

##### Cohort analysis

You can also leverage cohort analysis to understand similar characteristics of top influencers. Identifying influencer cohorts can help create actionable insights, which can help effect a change in a company.

Here’s a simple way to create a cohort analysis:

1. Run a **Network person query**.
2. Select a population of top influencers based on the Influence metric: 
    1. Set a threshold or sort based on the Influence metric.
    1. Select the top 10% of the whole company population (or any other percentage you want to address in the analysis).
3. Flag the selected individuals in step 2 as influencers.
4. Pivot the data in Excel with various HR attribute combinations using the flag in step 3.

To see a sample manual cohort analysis, view the one we created [here](<https://github.com/microsoft/VivaSolutions/tree/main/Sample Solutions/ONA/SampleAnalysis>) in Excel.

For an advanced cohort analysis, refer to [FindingCohorts Python script](#findingcohorts-python-script)  in this article.

#### Network person-to-person query

Creating bidirectional charts (like doughnut, Sankey, and chord) in visualization tools like Power BI is a good first step to identify connection patterns. The following images show a few sample visuals:

:::image type="complex" source="../images/ona-bidirectional-charts(1)(1).png" alt-text="Screenshot of two doughnut charts":::
   Screenshot that shows two doughnut charts made in Power BI. The first chart is titled, "StrongTieScore for All Employees." It has two sections; the first reads "3.58K" with "4.09%" in parentheses and the second reads, "83.37K" with "95.88%" in parentheses. The second chart is titled, "DiverseTieScore for All Employees." It has five sections. In clockwise order, they read: "2.64K" with "3.02%" in parentheses; "26.23K" with "29.98%" in parentheses; "25.23K" with "28.84%" in parentheses; "23.11K" with "26.42%" in parentheses; and "10.16K" with "11.61%" in parentheses.
:::image-end:::

:::image type="complex" source="../images/ona-bidirectional-charts(2)(1).png" alt-text="Screenshot of two Sankey charts":::
   Screenshot that shows two Sankey charts made in Power BI. The first chart is titled, "Average of StrongTieScore by SupervisorIndicator." It has three fields on the left and three fields on the right. The fields on the left are titled, from top to bottom: "Mgr"-plus, "IC," and "Mgr." The fields on the right are titled, from top to bottom: "Mgr," "IC," and "Mgr"-plus. Lines of various thicknesses connect groups on the left to groups on the right. The second chart is also titled, "Average of StrongTieScore by SupervisorIndicator." It has three fields on the left and three fields on the right. The fields on the left are titled, from top to bottom: "IC," "Mgr", and "Mgr"-plus. The fields on the right are titled, from top to bottom: "Mgr"-plus, "IC," and "Mgr." Lines of various thicknesses connect groups on the left to groups on the right. An explanatory box, connected to the first chart's "Mgr"-plus, reads, "TieOrigin_SupervisorIndicator Mgr-plus," TieDestination_SupervisorIndicator IC," and "Average of StrongTieScore 5.344128700133655.".
:::image-end:::

:::image type="complex" source="../images/ona-bidirectional-charts(3).png" alt-text="Screenshot of two chord charts":::
   Screenshot that shows two chord charts made in Power BI. The first chart is titled, "Average of StrongTieScore by LevelDesignation." It has several sections, which are labeled by role. These roles read, in clockwise order: "Senior Executive," "Senior IC," "Support," "Executive," "Director." There are also numbers within each section; they read, in clockwise order: "0," "0," "1.4," "0," "7.18," "0," "7.82," "6.51," "0," "13.09," "0," "15.34." Beneath the first chart is a score in large font that reads "0.77." The label beneath the score reads, "Average of StrongTieScore." The second chart is titled, "Average of DiverseTieScore by LevelDesignation." It has several sections, which are labeled by role. These roles read, in clockwise order: "Director," "Support," "Junior IC," "Senior IC," "Manager," and "Senior Executive.  The numbers within each section  read, in clockwise order: "34.63," "0," "52.59," "0," "55.29," "0," "53.75," "0," "67.91," "0," "51.72." Beneath the second chart is a score in large font that reads "9.07" The label beneath the score reads, "Average of DiverseTieScore." Some roles and numbers of each chart may be obscured by an explanatory box in the center of the graph that reads, "Director->Junior IC 5.633232069789529" and "Junior IC->Director 3.9378525449415105.".
:::image-end:::

You can use **Network person-to-person query** results as a form of person-to-person interaction matrix along with open-source ONA tools. However, please consider the limitations mentioned in the [ONA datasets section](#ona-datasets) above.

#### Group-to-group query

You can use Power BI visualizations—for example, matrix heatmap (shown in the image below) and network visualizations like Network Navigator—to reveal collaboration patterns between groups.

:::image type="complex" source="../images/ona-matrix-heatmap.png" alt-text="Screenshot of a matrix heatmap made in a spreadsheet":::
   Screenshot that shows a matrix heatmap made in Excel. The matrix shows collaboration patterns between divisions within an organization, expressed in percentages. There are 16 columns containing collaborators and 16 rows containing Time investors, and these rows and columns each share the same titles. The "Biz Dev" row corresponds with the "Biz Dev" column, the "CEO" row corresponds with the "CEO" column, and so forth. Cells containing percentages less than or equal to 1.0 are red; cells containing percentages between 1.1 and presumably 20 are yellow; and cells containing percentages above presumably 20 are green.
:::image-end:::

> [!NOTE]
> You'll need to import Power BI visuals.

### Tools for advanced ONA analysis
Several tools allow you to visualize or further analyze person- or group-level ONA analysis. In the following section, we introduce a few options. However, any tool specifically designed for network analysis can be used with the interaction matrix.

#### wpa R package

wpa R package is an open-source R library of over 180 tools and functions for analyzing and visualizing data from Microsoft Viva Insights. The package is publicly available on GitHub and published on CRAN.

##### Functions

* **Group-to-group queries**: To analyze and visualize Group-to-group queries, use `network_g2g()`.

    :::image type="complex" source="../images/ona-wpar-g2g(1).png" alt-text="Screenshot of network diagram representing groups":::
   Screenshot that shows a network diagram representing the relationship between groups. The diagram is titled, "Group to Group Collaboration" and sub-titled, "Collaboration Across Organizations." 15 groups are represented in the diagram. 13 of these groups form a network web; two are outliers on the left-hand side of the image. A note in the bottom right-hand corner of the image reads, "Displays only collaboration above 10% of node's total collaboration.".
:::image-end:::
 
* **Person-to-person queries**: To analyze and visualize person-to-person queries, use `network_p2p()`. This function has the added capability to perform community detection.

    :::image type="complex" source="../images/ona-wpar-p2p(1).png" alt-text="Screenshot of person-to-person network diagram color-coded to show communities":::
   Screenshot that shows a network diagram representing the relationship between people in an organization. The diagram's dots are color-coded to represent communities; there are four communities represented in this image.
:::image-end:::

    :::image type="complex" source="../images/ona-wpar-p2p(2).png" alt-text="Screenshot of a Sankey diagram to the left of a screenshot of a network diagram":::
   There are two screenshots in this image. The first screenshot shows a Sankey diagram with eight groups; the left groups are labeled alphabetically, "Org A" through "Org H." The right groups are labeled numerically, "1" through "8." Lines of various thicknesses connect the left and right groups. The second screenshot shows a person-to-person network diagram representing the relationship between people in an organization. The diagram's dots are color-coded to represent communities; there are seven communities represented in this image. There is a key at the bottom-center of the screen titled, "cluster," and there are seven dots to its right; each dot is assigned a separate color and a numerical value, 1-7, to its right. The label on the bottom right-hand side of the image reads, "Person to person collaboration with Community Detection based on the Leiden algorithm.".
:::image-end:::

#### Gephi

Gephi is the leading visualization and exploration software for all kinds of graphs and networks. Gephi is a great tool for:

* Visualizing and interacting with large graphs
* Adding extra attributes to nodes and partitioning a graph based on those attributes
* Sizing nodes based on attributes and graph measures like degree and weighted degree
* Comparing partitions based on different attributes, with static visualization of the network
* Filtering the network based on attributes and working in subgraphs
* Calculating standard network statistics like degree, network diameter, and density

##### Gephi handbook

The Gephi handbook provides instructions on:

* Installing Gephi
* Running Viva Insights queries and transforming the results
* Configuring Gephi to create a Person-to-person and Group-to-group visualization

A sample template is available [here](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions/ONA/Gephi).

 :::image type="complex" source="../images/ona-gephi-combined.png" alt-text="Two screenshot of network diagrams":::
   There are two screenshots in this image. The first screenshot shows a network diagram with five groups in the middle and 10 groups surrounding those middle groups. Middle groups connect to each other; groups on the outside connect only to groups in the middle and not to each other. Groups are labeled in varying font size. Some groups labeled in larger type include "G&A Central," "IT-Corporate," and "Facilities." The second screenshot shows a similar network diagram to the first screenshot, except that connections to and from "G&A Central" are highlighted and other connection lines are faded.  
:::image-end:::

 :::image type="complex" source="../images/ona-gephi-interface.png" alt-text="Screenshot of the Gephi interface":::
   Screenshot that shows the Gephi interface. There is a ribbon with commands and tabs. A side panel on the right of the screen shows formatting settings. A side panel on the left of the screen shows other settings and a pie chart. The center of the screen shows a network diagram. The screen's text is not readable.
:::image-end:::

#### FindingCohorts Python script

The FindingCohorts Python script provided on GitHub is a machine-learning-based solution to identify cohorts and common characteristics of the top influencers in a population.

Before you use the script, run a Network person query with Influence_rank and Influence metrics and HR attributes included.

Then:

1. Download the script from GitHub. To make sure the script can successfully read the input data, modify the script as necessary in **Step 1: read the input file**.

    :::image type="complex" source="../images/ona-gephi-python-script.png" alt-text="Screenshot of the Python script's Step 1: read the input file ":::
       Screenshot that shows Step 1: read the input file of the Python script in GitHub. A note beneath the Step 1 header reads, "Modify this cell to read the input data: csv from a local path, Azure blob storage with access key, etc.," which is highlighted. In the first code block, the content after ".format" is highlighted.
    :::image-end:::

1. Configure the parameters in **Step 1: read the input file**.
1. Complete **Step 2: Add isInfluencer flag**, **Step 3: Training a DecisionTree model**, and **Step 4: DecisionTree text representation**.

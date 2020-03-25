---

ROBOTS: NOINDEX,NOFOLLOW
title: Business Continuity Dashboard in Power BI
description: Use the Power BI template to run a query, export its results, and visualize the data in the Business Continuity Dashboard in Power BI
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Business Continuity Dashboard in Power BI

You can use the Business Continuity Dashboard in Power BI to visually analyze Workplace Analytics data to answer questions about how your organization is adapting to suddenly having all or a significant number of your employees working remotely.

Workplace Analytics uses Office 365 data activity to provide near real-time, behavioral data about how your company is adapting and evolving to meet challenges associated with a move to remote work during a disruption, such as: 100 percent remote work (maybe for the first time ever), work-from-home requirements, social isolation, and school closures.

The following are a few of the top-level business questions asked by leaders and analysts about continuing business during a disruption.

|Business question |Analysis |
|-------------|------------------|
|Is business running as usual? |<ul><li>High-level overview of community activity level spanning before and after the disruption </li><li>Trendline of activity </li></ul>|
|What is being disrupted? |<ul><li>Engagement with customers and suppliers </li><li>Cross-functional teaming and partnering </li></ul>|
|How are employees adapting to the disruption?  |<ul><li>Activity shifts throughout a workday or workweek, including: Activity by time of day, After-hours work, and Workweek span activity </li><li>Channels used to replace in-person connections </li></ul>|
|How do you foster employee community and engagement? |<ul><li>Employees who've lost connection points with their manager </li><li>Meaningful connection points within informal interactions </li></ul>|

The template enables you to connect query data in Workplace Analytics to Power BI, and then use it in the Business Continuity Dashboard to visualize and report about your organization's workplace patterns and trends.

This Power BI template uses the following predefined Workplace Analytics Person queries where you select the applicable chart data to use in Power BI.

* Business Continuity
* Activity by Time of Day

## To set up

Use the following steps to download the template and generate the Workplace Analytics query data that's required to populate the Business Continuity dashboard in Power BI.

1. Download and save the Workplace Analytics Power BI template.
2. Open [Workplace Analytics](https://workplaceanalytics.office.com/).
3. In **Queries**, run a query for each of the following predefined Person queries in the **Start from preselected filters and metrics** section:

   * Business Continuity
   * Activity by Time of Day

4. Enter or select the following for each query.

   |Query setting |Required entry or selection |
   |-------------|------------------|
   |Query Name |Name of the applicable query, Business Continuity or Activity by Time of Day|
   |Group by |Week |
   |Time Period |Custom range |
   |Auto-refresh |Select to enable |
   |Date Range | Sun, 01/05/2020 to the Latest Date Available |
   |Meeting Exclusions | Select the Tenant Default Meeting Exclusion Rule as applicable for the tenant |

    ![Business Continuity query settings](../Images/WpA/tutorials/business-continuity-query.png)

5. Optionally, you can specify additional metrics and filters for each query:

   * **Metrics** - The template automatically includes all applicable metrics. However, you can add and customize additional metrics that you want to use in Power BI. For example, collaboration levels between communities of interest and trending topics.
   * **Filters** - You can add filters to focus on specific populations of measured employees. Otherwise, it's preset to return data for all active employees within the measured population.
   * **Organizational data** - Select all or some of the Organizational Data columns to use in Power BI as pivot points or population filters. At a minimum, you must select the **Organization**, the **LevelDesignation**, and the **TimeZone**.

6. After confirming the settings, select **Run** to run the query. Repeat these steps to create the **Activity by Time of Day** query.
7. After the queries successfully run and their status shows as a green check mark, continue to the next step to connect the query data to Power BI.

For more details about metrics and filters available for Person queries, see [Create a Person Query](./person-queries.md).

## To connect query data to Power BI

1. Open the Power BI template for Business Continuity that you downloaded in the previous steps.
2. When prompted for the OData URL, go to Workplace Analytics **Queries** > **Results**, select the **link** icon for the **Business Continuity** query results (with a green check mark status), and then select **Copy**.
3. In the Power BI **Business Continuity Dashboard** prompt, paste the query results link, and then select **Load**.
4. When prompted to **Sign in** in Power BI, enter your **Workplace Analytics login credentials** to connect to the query results.
5. If prompted to sign in to your account, select **Organization Account**, enter your **Microsoft Office 365 credentials** that you use to access Workplace Analytics, then select **Connect**.
6. Repeat these steps for the **Activity by Time of Day** query results.

## Data analysis

1. After connecting Power BI to your Workplace Analytics data, you can open and use the Business Continuity Dashboard in Power BI to view organizational data.
2. The following sections highlight metrics that indicate how your business is responding to a business disruption and related changes:

   * [Business as usual indicators](#business-as-usual-indicators)
   * [External engagement](#external-engagement)
   * [Employee work spans](#employee-work-spans)
   * [Modes of communication](#modes-of-communication)
   * [Ensuring community and transparency](ensuring-community-and-transparency)

### Business as usual indicators

Activity levels within your company might change significantly in response to a business disruption introduced by social distancing requirements, perhaps permanently. Collaboration patterns give you visibility into the size of the impact, how it is trending over time, and the path back to a "new normal."

The degree of impact can vary across employee communities and functions. Identifying areas within the company undergoing the greatest change can focus transition efforts to preserve employee productivity.

**Specific analysis**

* Trend in activity by collaboration mode over time
* Change in activity between baseline and current time periods
* Breakdown in collaboration activity across analyzed communities

### External engagement

Ability to work with external customers, vendors, and partners might be impeded as counterparts are forced to refocus on mission-critical activities. The impacts of this shift can affect different roles in differing ways.

For example, sales teams might find difficulty in scheduling time with customers who are refocusing on higher order priorities. Conversely, customer and partner support teams might be juggling scarce workday attention with increasing inbound requests.

**Specific analysis**

* Groups who have seen the most change in the amount of time that they are spending with external contacts
* Change in externally organized meetings
* Change in internally organized meetings that contain external counterparts
* Change in the amount of email activity that includes external participants

### Employee work spans

Additional collaboration burden might be shouldered in surprising parts of the business. Changes in activity levels can indicate which groups are struggling to maintain pace and highlight those with more seamless transitions.

Workweek span data indicates the spread of time that employees are "on" during the workweek. Gaps of activity within areas of the company, where work spans are increasing the most, are potentially undergoing the most significant adaptation.

**Specific analysis**

* Change in the share of employees whose collaboration hours have increased or decreased in excess of a user configurable threshold; the charts show data by organizational group
* Change in workweek span by organizational group

### Modes of communication

Activity levels and profiles tend to shift as people move from in-office to remote work. Work-life balance changes to work-life integration. Meetings, calls, and chats might replace in-person conversations and hallway conversations. Asynchronous collaboration channels like email tend to flex across the workday and into after hours.

Changes in activity levels are possibly uneven across employees. For some, remote work might force a juggling of personal and professional responsibilities. For others, it might enable additional time for focused work and increased productivity.

**Specific analysis**

* Comparison in activity levels across meetings, calls, email, and IMs for the duration of a workday or workweek
* Highlight of the amount of after hours collaboration has changed from the baseline period across each major mode of collaboration
* Change in the share of employees whose after hours collaboration activity levels have increased/decreased in excess of a user configurable threshold. This chart is broken out by organizational group.

### Ensuring community and transparency

Community and transparency is one of the biggest drivers of team cohesion. As employees are adapting to working in isolation, a heightened focus should be maintained on promoting cohesion and belonging. Regular manager 1:1 check-ins are critical to demonstrate empathy, establish trust and help employees manage these challenges.

Maintaining horizontal employee relationships allows employees to continue feeling part of the team – using virtual team meetings not only for work but also social and personal sharing can help combat loneliness and disengagement. This sense of isolation has been reported [reference] as the biggest impediment to successful long term work from home programs.

**Specific analysis**

* The number of employees who have not had active 1:1 engagement with their manager, counted by organizational group.
* Breakdown of the number of meaningful internal connections that employees experience over (near) synchronous collaboration mechanisms, such as by calls, meetings, and instant messages or chats. Activity levels are shown across groups or related segments to help find groups that shows signs of stress due to isolation and lack of connection.

### Trending topics

Activity levels around distinct themes and topic areas might surge as business responds to this disruption. Coordination of corporate responses, reassessing priorities and shifting of attention back to core activities, and a heightened interest in maintaining connectivity and wellbeing within teams are some of the topics that might gain newfound traction.

**Specific analysis**

* Collaboration hours invested by the company in a set of predefined topics.
* The shift to remote work: Keywords include work from home, remote, best practice, coping, cope, tips, wellbeing
* Reassessment and refining of organizational priorities: Keywords include Reassess, priority, refocus, response

## Frequently asked questions

### Q1 How do I set up and run a Workplace Analytics query?

See [Create a Person Query](./person-queries.md) for details.

### Q2 How do I change the axis of a chart to use a different Organizational data attribute?

See [Customize a base metric in a query](../customize-a-metric.md) to learn more about how to customize your Workplace Analytics query output. Also, see [Transform, shape, and model data in Power BI](https://docs.microsoft.com/power-bi/transform-model/) for details about how to change chart views in Power BI.

### Q3 How do I integrate additional metrics or data sources with this dashboard?

See [Connect to data in Power BI](https://docs.microsoft.com/power-bi/connect-data/) to learn more about how to connect data in Power BI. See [Prepare organizational data](../setup/prepare-organizational-data.md) to learn about what organizational data you can analyze in Workplace Analytics and see [Data sources](../use/data-sourcesv2.md) to see what data sources you can connect to and analyze from within Workplace Analytics.

### Q4 How do I use Power BI?

See [Power BI documentation](https://docs.microsoft.com/power-bi/) for details on how to use Power BI.

### Q5 How do I share these insights with others in my organization?

You can share the Business Continuity Dashboard with your organization. Or you can export and distribute Power BI reports as PDF files. See [Share Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/power-bi/service-share-dashboards) for details.

## Support

* **Dashboard support** - Contact the Workplace Analytics team member that referred you to this page for support about onboarding, usage, and interpretation of the data contained within the dashboard.
* **Workplace Analytics support** - Refer to [Workplace Analytics documentation](../index.md) or [Workplace Analytics Support](../overview/getting-support.md) for additional help.
* **Support with other Microsoft products and tools** - Support for Power BI and other tools used in the context of this dashboard can be found through each product's associated support channels.

## Related topics

* [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)

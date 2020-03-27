---

ROBOTS: NOINDEX,NOFOLLOW
title: Power BI Business Continuity Dashboard
description: Use the Power BI Business Continuity Dashboard to visualize predefined query data from Workplace Analytics in Power BI
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Power BI Business Continuity Dashboard

You can use the Power BI Business Continuity Dashboard populated by Workplace Analytics data to answer questions about how your organization is adapting to business disruption, such as a switch to 100 percent remote work.

Workplace Analytics collaboration data directionally highlights where disruption to ways of working is having the largest impact, which is a measurable starting point for identifying how leaders, tools, and processes can support and sustain a new way of working.

The following are a few of the top-level business questions asked by leaders about continuing business during a disruption that this dashboard enables you to visualize and explore.

|Business question |Analysis |
|-------------|------------------|
|How is business as usual changing? |<ul><li>How are activity levels changing in response to a disruption? </li><li>Which lines of business are more impacted? </li></ul>|
|How are employees adapting to the disruption?  |<ul><li>How many employees are experiencing significant shifts in workweek span and collaboration demand? </li><li>How are employees shifting their work patterns across the collaboration activities, such as calls and chats? </li></ul>|
|Are we maintaining external relationships? |<ul><li>How much has changed with customer, partner, and vendor collaboration? </li><li>Which lines of business are experiencing the largest increases and decreases in external demand? </li></ul>|
|How do you foster employee community and engagement? |<ul><li>Are your managers regularly checking in with their employees about their wellbeing and health? </li><li>Are employees managing to stay engaged while in an all-remote work environment? </li></ul>|

To populate the Business Continuity Dashboard in Power BI, you must set up and successfully run the following predefined **Business Continuity** and **Hourly Collaboration** queries in Workplace Analytics. The results of these queries will refresh your downloaded Power BI dashboard on a weekly basis.  

After you successfully run these required queries, you'll see the Power BI template that's required to create the dashboard only . After you download the Power BI template, you can connect the query data from Workplace Analytics to Power BI, and then use it in the Business Continuity Dashboard to visualize and report about your organization's workplace patterns and trends.

## Set up and run the query data

Use the following steps to download the template and generate the Workplace Analytics query data that's required to populate the Business Continuity dashboard in Power BI.

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under the **Start from preselected filters and metrics** section, run a query for each of the following predefined Person queries in the :

   * **Business Continuity**
   * **Hourly Collaboration**

3. Enter or select the following for each query.

   |Query setting |Required entry or selection |
   |-------------|------------------|
   |Query Name |Name of the applicable query, Business Continuity or Hourly Collaboration|
   |Group by |Week |
   |Time Period |Last six months |
   |Auto-refresh |Select to enable |
   |Date Range | Automatically selected |
   |Meeting Exclusions | Select the Tenant Default Meeting Exclusion Rule as applicable for the tenant |

4. Optionally, you can specify additional metrics and filters for each query:

   * **Metrics** - The template automatically includes all applicable metrics. However, you can add and customize additional metrics that you might want to use in Power BI. For example, collaboration levels between communities of interest and trending topics.

   > [!Important]
   > Do not change the names or delete any of the preselected metrics for this template because if you do, it'll cause errors within the Power BI dashboard.

   * **Filters** - You can add filters to focus on specific populations of measured employees. Otherwise, it's preset to return data for all active employees within the measured population.
   * **Organizational data** - Select all or some of the Organizational Data columns to use in Power BI as pivot points or population filters. At a minimum, you must select the **Organization**, the **LevelDesignation**, and the **TimeZone**.

5. After confirming the settings, select **Run** to run the query. Repeat these steps to create the **Hourly Collaboration** query.
6. After the queries successfully run and their status shows as a green check mark, continue to the next step to connect the query data to Power BI.

For more details about metrics and filters available for Person queries, see [Create a Person Query](./person-queries.md).

### Query data settings and scope

As you continue to analyze the data over time, you'll might need to update the settings and scope to be sure you're analyzing considering any data that is changing in response to the disruption.

* View and update settings for **Baseline time frame**
* View and Change settings for **Selected time frame** to compare with the baseline
* Scope the population to the **Organizations** and **Time zones** you want to analyze
* Confirm the size of the scoped population after changing any of these settings

> [!Note]
> As additional data is processed on a weekly basis, you'll need to adjust the **Selected Time Frame** if you want to view the most recently included data.

## Connect query data to Power BI

1. In Workplace Analytics **Queries** > **Results**, select the **download** icon for the **Business Continuity** query results, and then select **PBI template** to save and open the template.
2. When prompted for the OData URL, in Workplace Analytics **Queries** > **Results**, select the **link** icon for the **Business Continuity** query results, and then select **Copy**.
3. In the Power BI **Business Continuity Dashboard** prompt, paste the query results link, and then select **Load**.
4. When prompted to **Sign in** in Power BI, enter your **Workplace Analytics login credentials** to connect to the query results.
5. If prompted to sign in to your account, select **Organization Account**, enter your **Microsoft Office 365 credentials** that you use to access Workplace Analytics, then select **Connect**.
6. Repeat these steps for the **Hourly Collaboration** query results.

## Data analysis

> [!Important]
> Workplace Analytics utilizes pseudonymized and aggregated behavioral data to provide a focused lens into how groups are getting work done. As with any behavioral dataset, you must view this data directionally about how groups act and respond to stimuli. Additionally, a number of underlying factors are used to calculate group-level, summary metrics. **For example**: Insights about changes in after-hours activity blends data about how people are experiencing large increases in overall activity levels with other individuals who are forced to work split schedules to integrate work and their out-of-work responsibilities. As such, the insights within this dashboard should be used as a lens perspective on how work is getting done, and not used in isolation of more traditional management approaches.

1. After connecting Power BI to your Workplace Analytics data, you can open and use the Business Continuity Dashboard in Power BI to view organizational data.
2. The following sections highlight metrics that indicate how your business is responding and adapting to a business disruption:

   * [Business as usual indicators](#business-as-usual-indicators)
   * [Employee work span](#employee-work-span)
   * [Modes of communication](#modes-of-communication)
   * [External engagement](#external-engagement)
   * [Ensuring community and transparency](#ensuring-community-and-transparency)
   * [Trending topics](#trending-topics)

### Business as usual indicators

Activity levels within your company might change significantly in response to a business disruption introduced by social distancing requirements, perhaps permanently. Collaboration patterns give you visibility into the size of the impact, how it is trending over time, and the path back to a "new normal."

The degree of impact can vary across employee communities and functions. Identifying areas within the company undergoing the greatest change can focus transition efforts to preserve employee productivity.

**Specific analysis**

* Trend in activity by collaboration mode over time
* Change in activity between the Baseline time frame and a Selected time frame
* Breakdown in collaboration activity across analyzed communities

### Employee work span

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
* Highlight of the amount of after-hours collaboration has changed from the Baseline time frame across each major mode of collaboration
* Change in the number of employees whose after-hours collaboration activity levels have increased or decreased in excess of a user-configurable threshold. This chart shows data by organizational group.

### External engagement

Ability to work with external customers, vendors, and partners might be impeded as counterparts are forced to refocus on mission-critical activities. The impacts of this shift can affect different roles in differing ways.

For example, sales teams might find difficulty in scheduling time with customers who are refocusing on higher order priorities. Conversely, customer and partner support teams might be juggling scarce workday attention with increasing inbound requests.

**Specific analysis**

* Groups who have seen the most change in the amount of time that they are spending with external contacts
* Change in externally organized meetings
* Change in internally organized meetings that contain external counterparts
* Change in email activity that includes external participants

### Ensuring community and transparency

Community and transparency is one of the biggest drivers of team cohesion. As employees are adapting to working in isolation, a heightened focus should be maintained on promoting cohesion and belonging. Regular 1:1 check-ins with managers demonstrate empathy, establish trust, and help employees manage these challenges.

Isolation has been reported as one of the biggest impediments to successful, long-term, work-from-home programs. Maintaining horizontal employee relationships enables employees to continue feeling part of the team. Allowing employees to connect by using virtual team meetings and chats for work, social, and personal sharing can help combat possible loneliness and disengagement.

**Specific analysis**

* The number of employees who have not had active 1:1 meetings with their managers, counted by organizational group.
* The number of meaningful internal connections that employees experience over (near) synchronous collaboration mechanisms, such as by calls, meetings, and instant messages or chats; activity levels are shown across groups or related segments to help discover any groups that show signs of stress due to isolation and lack of connection.

### Trending topics

Activity levels around distinct themes and topic areas might surge as business responds to a disruption. Coordination of corporate responses, reassessing priorities, and shifting attention back to core activities, with a heightened interest in maintaining connectivity and wellbeing within teams, are some of the topics that might gain newfound traction.

**Specific analysis**

* Collaboration hours invested by the company in a set of predefined topics
* The shift to remote work with keywords, such as: work from home, remote, best practice, coping, cope, tips, and wellbeing
* Reassessment and refining of organizational priorities with keywords, such as: reassess, priority, refocus, and response

## Frequently asked questions

#### Q1 How do I set up and run a Workplace Analytics query?

See [Create a Person Query](./person-queries.md) for details.

#### Q2 How do I change the axis of a chart to use a different Organizational data attribute?

See [Customize a base metric in a query](customize-a-metric.md) to learn more about how to customize your Workplace Analytics query output. Also, see [Transform, shape, and model data in Power BI](https://docs.microsoft.com/power-bi/transform-model/) for details about how to change chart views in Power BI.

#### Q3 How do I integrate additional metrics or data sources with this dashboard?

See [Connect to data in Power BI](https://docs.microsoft.com/power-bi/connect-data/) to learn more about how to connect data in Power BI. See [Prepare organizational data](../setup/prepare-organizational-data.md) to learn about what organizational data you can analyze in Workplace Analytics and see [Data sources](../use/data-sourcesv2.md) to see what data sources you can connect to and analyze from within Workplace Analytics.

#### Q4 How do I use Power BI?

See [Power BI documentation](https://docs.microsoft.com/power-bi/) for details on how to use Power BI.

#### Q5 How do I share these insights with others in my organization?

You can share the Business Continuity Dashboard with your organization. Or you can export and distribute Power BI reports as PDF or PowerPoint files. See [Share Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/power-bi/service-share-dashboards) for details.

## Support

* **Dashboard support** - Contact the Workplace Analytics team member that referred you to this page for support about onboarding, usage, and interpretation of the data contained within the dashboard.
* **Workplace Analytics support** - Refer to [Workplace Analytics documentation](../index.md) or [Workplace Analytics Support](../overview/getting-support.md) for additional help.
* **Support with other Microsoft products and tools** - Support for Power BI and other tools used in the context of this dashboard can be found through each product's associated support channels.

## Related topics

* [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)

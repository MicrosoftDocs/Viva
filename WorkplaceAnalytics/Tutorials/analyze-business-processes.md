---

title: Analyze business processes 
description: Analyze business processes -- Introduction and walkthrough   
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble

---

# Introduction

**Role:** Analyst

When you and your co-workers perform an organized series of steps to reach a goal, you've participated in a business process. For example, your organization's hiring process might consist of obtaining leads, screening candidates, conducting interviews, making an offer, and sending new hires to HR for onboarding. Later business processes might have goals of training or coaching.

You can improve your business processes by analyzing them; for example, by measuring their cost &ndash; in time and money. For example, your business might conduct an information-security audit from time to time. Your CFO or CIO might want to know whether too little, too much, or just the right amount of time is being spent on these audits, and whether the right roles of employees are participating in them.

To make these determinations, conduct an analysis by running a Workplace Analytics query in which you designate the business process (in this case, auditing) as a [metric filter](../use/metric-filters.md) for the query. <!-- *** CALL THESE NEW FILTERS OUT IN THAT TOPIC *** --> To improve the query's accuracy, you first define a _data set_ to limit the data that the query examines.

Here are the procedures to follow to analyze a business process:

1. [Define a data set](#define-a-data-set) &ndash; Make sure that you're analyzing only data that is relevant in every aspect, such as organizationally and geographically.

2. [Define a business process](#define-a-business-process) &ndash; Define the business process that you want to analyze.

3. [Analyze a business process](#analyze-a-business-process) &ndash; Compose and run a Workplace Analytics query in which you select the data set and business process as parameters.

The following sections describe these processes.

> [!Note]
> After you define a data set, it becomes available to all other analysts in your partition. Similarly, after you define a business process, it also becomes available to all other analysts in your partition.

## Define a data set

Before you define a business process, you need to select the data set that's applicable to that process. For example, your company might have a global footprint, but you want to analyze only the processes of one subsidiary. You limit the data set for your query by filtering out organizational data that does not apply &ndash; for example, data from subsidiaries in other locations.

To define a data set, use the following procedure:

### Data set steps

Every business process that you create must be based on a data set. For that reason, creating at least one data set is mandatory before you can proceed to [Define a business process](#define-a-business-process). 

In this example, we restrict the analysis data to meetings of a particular length that took place in a particular city.

1. In Workplace Analytics, on the left navigation pane, expand **Settings** and select **Analysis settings**.

1. On the **Analysis settings** page, select **Data sets** and then, on the right side of the page, select **Add data set**.

1. On the **New data set** page, type a name and, optionally, a description for your new data set. (In this example, we type **Bangalore hiring** for the name.) Select **Continue**.

1. Under **Time period** select start and end dates. All meetings that took place outside of this time period will be excluded from the data set.

1. Under **Meeting exclusions**, specify a [meeting exclusion rule](meeting-exclusions-intro.md) or accept the default, the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule).

1. Under **Which meetings do you want to include in your query results?**, define filters to scope the data set to the business-process analysis that you want to perform. You'll use these filters to filter out meetings. Select **Add filter**.

1. Select **Meeting**:

   ![Add a Meeting filter](../images/wpa/tutorials/meeting-filter-1.png)

1. In the boxes to the right of **Meeting's**, select **Duration (in hours)**, **<** (less than), and **30** minutes.

1. On the next line, select **Organizer**. This lets us choose a geographic location for the meetings.

   ![Add an Organizer filter](../images/wpa/tutorials/organizer.png)

1. In the boxes to the right of **Organizer's**, select **city**, **Equals**, and **Bangalore**. (The choices that are available are determined by the [organizational data](../setup/prepare-organizational-data.md) that the Workplace Analytics admin has uploaded.)

1. Select **Submit**.

This starts the creation of a data set that only contains data that matches these criteria. After the data set is ready, you can use it in your upcoming business-definition process and analysis.

## Define a business process

Before you can run a query to analyze business processes within your organization, you need to define them. This way, you can later use them in filters in your query.

You define a business process by selecting meetings in which people  contributed to the furtherance of the process. This set of selected meetings provides the data that constitutes the business-process filter.

You select meetings by using the **New business process** page in the **Analyze** area of Workplace Analytics:  

![Biz process start page](../images/wpa/tutorials/start-page.png)

To select meetings, you assemble a list of keywords that match words in the subject lines of meetings that you want to include or exclude. These keywords then determine which meetings constitute the business process.

>[!Note]
>Currently, you can use only English keywords in this process. 

### Business process steps

1. In Workplace Analytics, on the left navigation pane, expand **Analyze** and select **Business process analysis**.
2. 




### Business process statuses

The following are the list of statuses for any Business process (including OOTB topics): 
 
* Draft &ndash; This indicates that a Business process is being created or edited but not yet submitted to the system. This is an intermittent state until the analyst feels that the Business process is ready to be submitted for processing by the system 
 
* In progress &ndash; This indicates that a Business process has just been created and is being processed by the system 
 
* Ready &ndash; This indicates that a Business process has been successfully published and is readily accessible across WpA (scopes permitting of course) 

* Archived &ndash; This indicates that a Business process has been archived 

* Error: This is a generic catch-all failed state that indicates that processing of the Business process itself has failed, when it is switching from “In progress” to the “Ready” state 

### Analyze a business process

You analyze business processes by using Workplace Analytics [queries](query-basics.md). You can use the following query types in this kind of analysis:

* Meeting
* Person 

## Related topics

* [Meeting exclusions in Workplace Analytics](meeting-exclusions-intro.md)

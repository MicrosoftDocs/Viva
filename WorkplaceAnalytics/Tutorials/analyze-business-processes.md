---

title: Analyze business processes 
description: Analyze business processes -- Introduction and walkthrough   
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---

# Introduction

**Role:** Analyst

When you and your co-workers perform an organized series of steps to reach a goal, you've participated in a business process. For example, your organization's hiring process might consist of obtaining leads, screening candidates, conducting interviews, making an offer, and sending new hires to HR for onboarding. Later business processes might have goals of training or coaching.

You can improve your business processes by analyzing them; for example, by measuring their cost &ndash; in time and money. You conduct such an analysis by running a Workplace Analytics query in which you designate the business process as a [metric filter](../use/metric-filters.md) for the query. And to improve the query's accuracy, you should first define a data set to limit the data that the query examines.

Here are the procedures to follow to analyze a business process:

1. [Define a data set](#define-a-data-set) &ndash; Make sure that you're analyzing only data that is relevant in every aspect, including organizationally and geographically.

2. [Define a business process](#define-a-business-process) &ndash; Define the business process that you want to analyze.

3. [Analyze a business process](#analyze-a-business-process) &ndash; Compose and run a Workplace Analytics query in which you select the data set and business process as parameters.

The following sections describe these processes.

> [!Note]
> After you define a data set, it becomes available to all other analysts in your partition. Similarly, after you define a business process, it also becomes available to all other analysts in your partition.

## Define a data set

Before you define a business process, you need to select the data set that's applicable to that process. For example, your company might have a global footprint, but you want to analyze only the processes of one subsidiary. You limit the data set for your query by filtering out organizational data that does not apply &ndash; for example, data from subsidiaries in other locations.
  
## Define a business process

Before you can run a query to analyze business processes within your organization, you need to define them. This way, you can later use them in filters in your query.

### Business process statuses

The following are the list of statuses for any Business process (including OOTB topics): 
 
* Draft &ndash; This indicates that a Business process is being created or edited but not yet submitted to the system. This is an intermittent state until the analyst feels that the Business process is ready to be submitted for processing by the system 
 
* In progress &ndash; This indicates that a Business process has just been created and is being processed by the system 
 
* Ready &ndash; This indicates that a Business process has been successfully published and is readily accessible across WpA (scopes permitting of course) 

* Archived &ndash; This indicates that a Business process has been archived 

* Error: This is a generic catch-all failed state that indicates that processing of the Business process itself has failed, when it is switching from “In progress” to the “Ready” state 



## Analyze a business process
analyze them with queries. Formerly, customers had to tackle these analysis problems through custom work but now we’re building the capability into the product.

## Related topics

* [Meeting exclusions in Workplace Analytics](meeting-exclusions-intro.md)

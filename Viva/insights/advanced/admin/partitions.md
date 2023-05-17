---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 05/17/2023
title: Partitions in Viva Insights
description: Learn how to create analyst workspaces in the advanced insights app.
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---


# Partitions in Viva Insights

*Applies to: private preview customers only*

Partitions are analyst workspaces that only contain certain employee data and attributes. In a partition, analysts can only create queries based on the data in that partition.

You can think of partitions like buckets. Each bucket (partition) contains a certain scoop of data from the reservoir (your entire dataset, also known as the **global partition**). For example, one bucket might only contain data from employees who work in your company’s marketing division.

As the Insights Administrator (admin), you assign analysts to one or more buckets. When those analysts run queries, they can only pull from the data in their assigned buckets. Let’s say you assign Analyst 1 to your bucket that contains data from employees in the marketing division. When Analyst 1 sets up a query, they’ll only see and pick from this marketing-division data.

Or maybe you create a bucket just for employees in your company’s US offices. Let’s say you assign Analyst 2 to this bucket. When Analyst 2 goes to run their queries, they’ll only see data from US-based employees. If you created another bucket for employees in Europe, but didn’t assign Analyst 2 to that bucket, Analyst 2 wouldn’t be able to see any data from employees in Europe.

Also, you might choose to assign a few analysts to the reservoir (the global partition). These analysts can access your entire company’s dataset, see all data, and run queries on all employees in the organization. We go into more detail about the global partition later on in this article.

Here’s a visual representation of how partitions work. In this scenario, the admin set up three partitions. Notice that some analysts are assigned to multiple partitions, some are assigned to the global partition, and some are only assigned to a single partition.

:::image type="complex" source="../images/admin-partitions.png" alt-text="<alt text>"lightbox="./images/admin-partitions-expanded.png":::
   Diagram that shows a Global partition, represented as a cylinder, with five arrows. The first three, top-level arrows point to buckets labeled "Partition 1," "Partition 2," "Partition 3." Each bucket has three second-level arrows leading down to analysts, represented as employee badges. The second two top-level arrows from the global partition point directly to two analysts. 
:::image-end:::

## Row and column data

A partition is both a row-level and a column-level control for data access. In other words, by using a partition, you can decide which:

* *Employees* analysts can run queries about. Each employee is one row of your organizational data file.
* *Attributes* analysts can use to build queries and rules. Each attribute is one column of your organizational data file.

:::image type="content" source="../images/admin-partitions-row-column-control.png" alt-text="Diagram of a table that shows employee data as rows, attributes as columns, and partitions as the space in the middle." lightbox="../images/admin-partitions-row-column-control-expanded.png":::

You'll filter employees and add attributes while you build your partition.

## Tenant- vs. partition-level actions

Most of the settings that you work with as an admin are only available at the tenant level—that is, they apply to everyone in your organization. The assets that analysts create within a partition—customized metrics and metric rules—are only available to other analysts in that partition.

|Tenant level| Partition level|
|------------|----------------|
|Privacy settings|Customized metrics|
|Manager settings|Metric rules|
|Data upload| |

In other words, what analysts create in their partitions stay within their partitions. What you set as an admin (unless you’re setting up a partition) applies across your organization. For more information about partition-level actions, refer to How analysts use partitions.

## About the Partitions page

Before we get into discussing how to use partitions, let’s discuss where you can find and create them: the **Partitions** page. To get to the **Partitions** page from the advanced insights app analyst experience, select **Partitions** from the left pane.

The **Partitions** page contains all partitions admins in your company have created, along with the global partition.
 
This page provides details about each partition, like its description, how many licensed users it contains, how many analysts are assigned to it, and when it was last updated. 

From the **Partitions** page, you can **Create a new partition** and **Search** for an existing partition.

### About the global partition

As we mentioned earlier, the global partition contains all the data you’ve brought to Viva Insights. Viva Insights makes the global partition by default, so you don’t need to do anything to create it. You’ll just need to pick which analysts to assign to it.

If your organizational data contains values for small organizations or few employees—for example, CXOs or Senior LT—and attributes like salary or gender, you might want to restrict who can access this sensitive information. With partitions, this restriction is straightforward. You can assign a few analysts to the global partition and other analysts to partitions that don’t contain this sensitive data.

>[!Note]
>While you can add and remove analysts from it, you can’t edit the global partition. 

#### Access

If analysts were assigned their analyst role before your organization started using partitions, they can automatically access the global partition.

If analysts were assigned their analyst role after your organization started using partitions, they can’t automatically access the global partition or any other partition. You'll need to grant analysts access—to the global or to any partition—expressly. 

To assign an analyst access to the global partition, select **Global partition** on the **Partitions** page in the advanced insights app. Then, follow step 6 below.

## How to create a partition and assign analyst access

Create as many partitions as you want by following these steps:

1.	In the advanced insights app's admin experience, select **Partitions** from the left pane.
1. Select **Create new partition**.
1.	Under **Partition setup**:
    1. Enter a name for your partition.
    1. Enter a description (optional).
1.	Filter which employee data you want your partition to include by adding one or more conditions. These conditions are based on your organizational data’s employee attributes.

    For example, if you want to create your partition based on employees in the engineering organization, you'd select **Add condition**, set the **Organizational data** attribute dropdown to "Organization," leave the **Operator** at "=," and set the **Value** to "Engineering."

    >[!Note]
    > The **Total employees**/**Filtered employees** counter reports how many employees are included in the partition. If this value is higher or lower than you want, try adjusting your conditions above. There’s no maximum **Filtered employees** you can have in a partition.
    >
    >Need more information about using filters? Refer to our [Filters](../analyst/filters.md) article.
5. Add employee attributes.

    >[!Important]
    >You can’t remove required attributes, which appear as gray tags here. When you add new attributes to your organizational data, they won’t add themselves to your existing partitions. In this release, you’re not able to edit partitions to add new attributes, but you’ll be able to in later releases. 
    >
    >Learn more about attributes a little later in this article.
6.	Pick which analysts you want to assign to work in this partition. The analysts you assign here can create queries based on employee data you defined in step 4.

    >[!Note]
    >For now, you can only add analysts when you first set up the partition. In later releases, you’ll be able to add new analysts later.
    >You can assign analysts to any number of partitions.
    
Your new partition won’t immediately appear in the partition switcher—you’ll need to refresh the page.

### About required attributes in partitions

As we mentioned earlier, you’ll notice a few required attributes in **Select attributes** when you set up your partition. Partitions need required attributes to work, and you can’t remove them. These attributes—which appear as gray tags when you’re building a partition—either come from the data you’ve uploaded to Viva Insights, or they’re system generated. 

|Attribute|Source|
|---------|------|
|**PersonId**|Organizational data|
|**ManagerId**|Organizational data|
|**Organization**|Organizational data|
|**EffectiveDate**|Organizational data|
|**Domain**|System – SMTP address|
|**PopulationType**|System - SMTP address|
|**TimeZone**|System – Outlook/Exchange settings|

## How analysts use partitions

As we discussed earlier, analysts assigned to a partition only see and use the data contained in that partition. What they create in their partition stays in that partition, and only other analysts assigned to that partition can view their work.

Here’s what that means in practice:

### Queries

When creating queries, analysts can only see and use the data that you’ve added to a partition. For example, let’s say you created several partitions based on time zone, only assigned two analysts to each, and didn’t assign any analysts to multiple partitions. When creating a query, an analyst assigned to the Europe/Warsaw partition couldn’t see or pick from any data from employees in the Asia/Bangkok partition. If an analyst ran a Power BI query, their downloaded Power BI report would also only contain the data from their assigned partition.

Also, analysts can only work with the attributes you add to their partition. For example, if you didn’t include **LevelDesignation** in a partition, an analyst couldn’t see or use that attribute in their queries. Their queries then couldn’t contain any information about employees’ seniority level within the company, like “Director.”

### Metric rules

If an analyst created a metric rule in one partition, an analyst in another partition couldn’t see it or use it in their queries. When analysts set a rule as default in their partition, that default rule doesn’t apply to queries created in other partitions.

### Custom metrics

Metrics that analysts create in one partition don’t transfer to other partitions. 

### About the partition switcher

If you assign an analyst to multiple partitions, they’ll use the partition switcher to move between their assigned partitions.

We explain more about analyst functionality in our analyst document, Partitions in Viva Insights for analysts.

## About upcoming features

During this private preview release, you’re able to create partitions and add analysts to the global partition. As we mentioned earlier, we’re working on a few upcoming features that give you greater control over your existing partitions:

* Read partition – View, but don’t edit, an existing partition.
* Edit partition – Change how your partition is set up, and which analysts can access it.
* Manage access – Add or remove analyst access from a partition without editing the entire partition.
* Delete partition – Remove your partition completely.


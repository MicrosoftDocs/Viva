---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 05/17/2023
title: Partitions in Viva Insights
description: Learn how to use analyst workspaces in the advanced insights app.
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

# Partitions in Viva Insights for analysts

Partitions are analyst workspaces that only contain certain employee data and attributes. In a partition, you’ll create queries, custom metrics, and metric rules based on the data in that partition. As an analyst, you’ll use the advanced insights app like normal—the only difference is the data you can access and run analyses from.

You can think of partitions like buckets. Each bucket (partition) contains a certain scoop of data from the reservoir (your company’s entire dataset, also known as the **global partition**). For example, one bucket might only contain data from employees who work in your company’s marketing division.
An admin in your organization assigns you to one or more buckets. When you run queries, you pull from the data in your assigned buckets when you create queries, metric rules, and custom metrics. For example, maybe you’re assigned to a bucket that contains data from employees in the marketing division. When you set up a query, you’d only see and pick from this marketing-division data.

Here's another example. Let’s say an admin assigns you to a bucket just for employees in your company’s US offices. When you go to run your queries, you’d only see and pick data from US-based employees. If your admin assigned someone else on the analyst team to another bucket for employees in Europe, but didn’t also assign you to that bucket, you wouldn’t see any data from employees in Europe.

A few analysts on your team might be assigned to the reservoir (the global partition). These analysts can access your entire company’s dataset, see all data, and run queries on all employees in the organization. We go into more detail about the global partition later on in this article.

Here’s a visual representation of how partitions work. In this scenario, the admin set up three partitions. Notice that some analysts are assigned to multiple partitions, some are assigned to the global partition, and some are only assigned to a single partition.

:::image type="complex" source="../images/admin-partitions.png" alt-text="<alt text>"lightbox="../images/admin-partitions-expanded.png":::
   Diagram that shows a Global partition, represented as a cylinder, with five arrows. The first three, top-level arrows point to buckets labeled "Partition 1," "Partition 2," "Partition 3." Each bucket has three second-level arrows leading down to analysts, represented as employee badges. The second two top-level arrows from the global partition point directly to two analysts. 
:::image-end:::
 
## About the global partition

Some organizations might want to grant certain analysts access to all employee data. The admin can do that by assigning analysts to the global partition. 

### About access

If your admin assigns you to the global partition, you can:

* Run queries on all the organizational data your company has in Viva Insights.
* Create filters and metric rules using any organizational attribute your admin has uploaded.

If one of your teammates creates a metric rule or custom metric in their partition, but you’re not assigned to that partition, you won’t be able to use that metric rule or metric.

## Creating queries, metric rules, and custom metrics in partitions

### Queries

When creating queries, you’ll only see and use the data that your admin has added to your assigned partition (or “bucket”). Let’s say your admin created several partitions based on time zone. You’re assigned to the Europe/Warsaw partition, but not to other partitions. When creating a query, you wouldn’t be able to see or pick from any data from employees in the Asia/Bangkok partition. If you ran a Power BI query, your downloaded Power BI report would also only contain data from your assigned partition.

Also, when creating queries, you’ll work with the attributes admins add to your partition. If you’re assigned multiple partitions, you might see different attribute options in each.
However, you can view and clone the queries other analysts in your partition have run. 

### Metric rules

If you create a metric rule in one partition, an analyst in another partition couldn’t see it or use it in their queries. Also, when you set a rule as default in your partition, that default rule doesn’t apply to queries created in other partitions. However, you can view and use metric rules that other analysts have created in your partition. 

### Custom metrics

Metrics you create in one partition don’t transfer to other partitions, but other analysts in your partition can use them.

## Switch between your assigned partitions

If your admin assigns you to multiple partitions, use the partition switcher to move between them.

To get to the partition switcher, go to the top left-hand corner of your screen and select the dropdown under **Partitions**. Select the partition you want to switch to. You can switch at any time.

:::image type="content" source="../images/admin-partitions-switcher.png" alt-text="Diagram of a table that shows employee data as rows, attributes as columns, and partitions as the space in the middle." :::
 

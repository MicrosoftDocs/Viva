---
ms.date: 03/17/2023
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

Partitions are analyst workspaces that only contain certain employee data and attributes. In a partition, analysts can only create queries based on the data in that partition.

For example, a multinational company might create partitions based on countries or parts of countries. They might create one partition for their employees in Brazil, another for their employees in Japan, and another for their employees in Great Britain. They might even decide to add a partition for employees in Wales or England. 

If one of this company's analysts was assigned to the partition for employees in Japan, their queries wouldn't contain data from employees in Brazil. Likewise, queries created by analysts in the partition for Great Britain wouldn't contain data from employees in Japan.

Here's another example. A company might create partitions based on organization, which separates employee data by employee group or team. An analyst assigned to a partition for the research and development organization couldn't create queries with information from the creative organization. 

Similarly, another organization might set up partitions based on role. Analysts assigned to the accounting partition, for example, could only run queries on data from accounting personnel.

## About the global partition

Some organizations might want to grant some analysts access to all employee data. They can do that by assigning analysts to the global partition.

While Viva Insights creates the global partition by default, no analysts have automatic access to it. You'll need to grant analysts access—to this or to any partition—expressly.

To assign an analyst access to the global partition, select **Global partition** on the **Partitions** page in the advanced insights app. Then, follow step 6 below.


## How to create a partition and assign analyst access

As an admin, you create partitions, but you don't work within them. Here's how to create and assign partitions in the advanced insights app:

1. In the advanced insights app's admin experience, select **Partitions** from the left pane.
1. Select **Create new partition**.
1. Under **Partition setup**:
    1. Enter a name for your partition.
    1. Enter a description (optional).
1. Filter which employee data you want your partition to include by adding one or more conditions.

    For example, if you want to create your partition based on employees in the engineering organization, you'd select **Add condition**, set the **Organizational data attribute** dropdown to "Organization," leave the **Operator** at "=," and set the **Value** to "Engineering." <!--will the internal roles/org data dropdown be there?-->
    
    Need more information about using filters? Refer to our [Filters](../analyst/filters.md) article.

    >[!Note]
    >The **Total employees**/**Filtered employees** counter reports how many employees are included in the partition. If this value is higher or lower than you want, try adjusting your condition(s) above.
    >
    >Partitions need to have at least 10 employees in them. You'll get a warning if the conditions you set result in fewer than 10 filtered employees.
1. Add employee attributes. <!--what does this do?-->
1. Pick which analysts you want to assign to this partition. The analysts you assign here can create queries based on employee data you defined in step 4.


FAQ <!--should we keep any of this?-->

Q1. How can I start using partitions? 

Currently the partitions feature is being rolled out on a per-customer basis. To have it enabled for your organization, reach out to your customer service contact at Microsoft. 

Q2. Why are newly uploaded attributes not being reflected inside non-global partitions? 

New attributes are not added automatically. After you upload a new attribute (in an organizational data upload), you must explicitly add the attribute to a partition by editing the partition. 

Q3. Why am I not able to see analyst settings in a partition? 

All analyst settings are applied to all partitions. For this reason the settings tab is visible only in the Global partition. 

 
---

ROBOTS: NOINDEX,NOFOLLOW
title: Partitions in Workplace Analytics
description: Description of partitions plus how to use and set up partitions in Workplace Analytics 
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Partitions in Workplace Analytics

A partition is a data workspace for an analyst. A partition delimits the employee data and organizational attributes that an analyst can use for analysis. Companies create partitions that contain subsets of employee data. To do this, they use various criteria. Here are examples:

* **Organization:** A company can create a partition for data about all the employees in one division, or in a functional group or team. Example: R & D
* **Geography:** A multi-national corporation might create different partitions for the data of employees of different countries or parts of countries. Example: Wales
* **Role:** A company could select the data of all the employees who have a particular function to include in a partition. Example: Accounting personnel

## Partitions give access to data

A partition defines what data you work with in Workplace Analytics. If you have one of the analyst roles (analyst or analyst limited), you can work with data on the **Explore the stats** and **Queries** pages of Workplace Analytics. You are also assigned one or more partitions, and your partition determines whose data you work with on those pages. If you have the program manager role, you can work on **Plans** and your role there is not limited, so you have access to all Plans.

For example, if you are an analyst with the job of finding workplace trends in the sales organization, you must be assigned a partition that encompasses the data of salespeople. You can then view data about salespeople on the **Explore the stats** pages and create queries about salespeople on the **Queries** page.

> [!Note]
> Analysts (and limited analysts) are not the only Workplace Analytics users who use partitions. Program managers who work in [Plans](../tutorials/solutionsv2-intro.md) must also be granted explicit access to a partition, after which they can create and view solution [plans](../tutorials/solutionsv2-task.md#create-a-plan) only in that partition.

## The Global partition

One particular partition encompasses everyone’s data: the "Global" partition. If an analyst has this partition, they can work with all employee data that’s been uploaded to Workplace Analytics. The Global partition is created by the system. While it exists by default, no analysts are given access to it by default. Analysts must be granted access&mdash;to this or to any partition&mdash;expressly, by an admin. See [To create a partition](#to-create-a-partition) for more information about assigning analysts to a partition.

> [!Note]
> For existing users, as part of one-time migration in 2019, all existing analysts and their existing queries and settings are being moved to the Global partition.

## Use partitions

If you are an analyst, you must have a partition selected to view **Explore the stats** and **Queries**. If you are a program manager, you work in the Global partition by default and you can go right to **Plans** to manage programs. If you are an admin, you create partitions, but you do not work within one.

### To use a partition

* **Roles**: Workplace Analytics analyst, PM, or admin

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, enter your work credentials. If you are a PM or analyst and you have not been assigned a partition, you'll see a notice that "to proceed, you have to be part of at least one partition."

    If you see this notice, ask your Workplace Analytics admin to assign you to a partition. You cannot start using Workplace Analytics until an admin assigns you to one or more partitions. If you do not see this notice, go on to the next step.

2. What you see now depends on your role and partition assignments: If you are analyst (you have the analyst role or analyst limited role), go to step 3; if you have any other role, go to Step 4.

3. Step for analysts:

    * If you have only one partition (even the default "Global" partition), this is the partition that you will use. Skip the rest of these steps. You can view **Explore the stats** and **Queries** for advanced analysis. This analysis will only show data for the partition you are granted access.  
    * If you have more than one partition, the **Partition** drop-down menu at the top of the **Home** page displays the partitions that you are linked to. Open this menu and select one:

       ![Select a partition](../images/wpa/setup/partition-menu.png)

      After you’ve chosen the partition to work with, you can skip the rest of these steps and view **Explore the stats** and **Queries**.  

4. If you have a non-analyst role, your choice depends on the role (or roles) that you've been assigned:

    * **Both a manager and an analyst:** If you have both a program manager role and an analyst role, the data you see depends on the page that you open. Plans are accessible only in the Global partition. A person with both a manager and analyst roles can access plans in Global partition and access **Explore the stats** and **Queries** in other partitions that they have been granted.
    * **Manager only:** Managers do not need to select a partition because they automatically use Global partition. If you’re a manager, go to the **Plans** page.
    * **Admin:** If you’re signed in to Workplace Analytics as an admin, then partitions don't affect you or your access to **Settings**.

## Create, edit, and delete partitions

* **Role**: Workplace Analytics admin

To administer partitions, see the following sections:

* [To create a partition](#to-create-a-partition)
* [To edit a partition](#to-edit-a-partition)
* [To delete a partition](#to-delete-a-partition)

### To create a partition

Workplace Analytics admins create partitions on the **Settings** page. This procedure consists of four sub-tasks, which you complete at the indicated step in the following procedure:

| Sub-task | Step | Notes |
| -------- | ---- | ----------- |
| Name the partition | 4 | Also, optionally, type a description |
| Create filters  | 5 | Select the employees whose data the partition will contain |
| Set attributes  | 6, 7 | Select organizational-data attributes to include in the partition |
| Give access |  8  | Select one or more analysts who will have access to this partition |

> [!Important]
> Plan your partitions carefully before you start to create them. Partions have limits in both number and size. For more information, see 
[Number and size limits](#number-and-size-limits).

1. Open the Workplace Analytics **Home** page. If prompted, sign in with your work account.  
2. Open the **Settings** page and select **Access control**.
3. In the **Partition-based access control** area, select **New partition**:

    ![New partition option](../images/wpa/setup/access-control-page.png)

4. On the **Access control > New partition** page, type the name of the new partition and optionally type a description.

5. **Create filters.** Under **Select employees for partition**, add one or more filters to define the employee data that will fall within the new partition:

    ![New partition](../images/wpa/setup/create-partitions-filters.png)

    > [!Note]
    > You can filter by only one attribute. For example, if you create a filter that uses the Organization attribute, you could produce the following filter clauses:  
    >  * Organization + Equals + <name_of_manager_1> AND
    >
    >    Organization + Equals + <name_of_manager_2>
    >
    > But you cannot add another clause that uses a different attribute, such as:
    >   * Domain + Equals + <domain_name>

6. **Select attributes**. Select which attributes from the organizational data to include in the partition. To exclude an attribute from the partition, leave it unselected.

7. **Select visibility of attributes**. You might want one or more attributes to not be visible to analysts who work in this partition. For example, "sales quota" might be a sensitive attribute that nevertheless has been uploaded in the organizational data. To hide the "sales quota" attribute, select it and then set its **Visibility** to **Hash in report**.

    ![Select visibility](../images/wpa/setup/create-partitions-attributes.png)

8. **Give access**. Under **Analysts**, select one or more analysts who will have access to this partition. Only the analysts that you select will be able to perform analyses in Workplace Analytics.

    ![Select analysts](../images/wpa/setup/create-partitions-access.png)

### To edit a partition

1. Open the Workplace Analytics **Home** page. If prompted, enter your Microsoft credentials.  
2. Open the **Settings** page and select **Access control**.
3. In the **Partition-based access control** area, locate the partition that you want to edit.
4. Select the ellipsis (...) in that partition's row and then select **Edit partition**:

    ![Edit partition](../images/wpa/setup/part-based-access-control-edit.png)

5. Edit any of the aspects of the partition that you specified previously. After you edit one aspect, move to the next one by selecting **Next**:

   * Edit filters to change the employees whose data you want to include.
   * Select different attributes to include in the partition.
   * Select different analysts who will have access to this partition.

6. Review and select impact on the analyses that already exist. You need to perform this step because editing a partition usually changes its data, which renders previously run analyses and queries (and their results) invalid. You can now choose to delete those invalid query results or to retain them:

    ![Review impact](../images/wpa/setup/edit-partition-review-impact.png)

   After you select **Retain all existing analyses** or **Delete query results**, confirm that the current settings are correct and select **Save**.

### To delete a partition

1. Open the Workplace Analytics **Home** page. If prompted, enter your Microsoft credentials.  

2. Open the **Settings** page and select **Access control**.

3. In the **Partition-based access control** area, locate the partition that you want to edit.

4. Select the ellipsis (...) in that partition's row and then select **Delete partition**:

    ![Admin settings](../images/wpa/setup/part-based-access-control-delete.png)

   > [!Note]
   > You cannot delete the Global partition. Only user-created partitions can be deleted.

## Frequently asked questions

#### Q1. How can I start using partitions?

A1. Currently the partitions feature is being rolled out on a per-customer basis. To have it enabled for your organization, reach out to your customer service contact at Microsoft.

#### Q2. Why are newly uploaded attributes not being reflected inside non-global partitions?

A2. New attributes are not added automatically. After you upload a new attribute (in an [organizational data upload](../setup/upload-organizational-data.md)), you must explicitly add the attribute to a partition by [editing the partition](#to-edit-a-partition).

#### Q3. Why am I not able to see admin settings in a partition?

A3. All admin settings are applied to all partitions. For this reason the settings tab is visible only in the [Global partition](#the-global-partition).

#### Q4. We regularly upload updates to our organizational data. How can these updates affect partitions?

A4. See the following section, [Partitions and organizational data](#partitions-and-organizational-data).

## Number and size limits

Partitions have limits both in number and size:

* An organization can have a maximum of ten partitions.
* Any new partition that you create can contain a maximum of 10,000 licensed users. Also see [Actions that can change partition size](#actions-that-can-change-partition-size).

> [!Note]
>  * The Global partition does _not_ count toward this total of ten partitions and has no limit of licensed users.
>  * If you need more than 10 partitions or more than 10,000 licenses in a partition, you can request these exemptions by contacting [Workplace Analytics Support](../overview/getting-support.md).

### Actions that can change partition size

The following scenarios can push the size of a partition beyond the allowed limit:

* **Role**: Workplace Analytics admin

| Scenario | Admin action | Result | 
| -------- | ------------ | ------ |
| You are creating a new partition or editing an existing partition that has fewer than 10,000 users. | You select a filter (in step 5 under [To create a partition](#to-create-a-partition)) that increases the partition size beyond 10,000 users. | You see a warning that indicates that the partition size has exceeded the limit. You can create this partition only if you reduce the size to below the limit. |
| You have a current partition  | <ul><li>You upload organizational data. This upload increases the size of a partition to greater than 10,000 users.</li><li>A refresh of collaboration data increases the size of the partition because of license assignment or reallocation. This causes the partition size to exceed the limit.</li></ul> | The upload succeeds and the partition size exceeds the limit. You receive a notification that warns you to address this issue. <br> Select the link in the notification to open the **Partition-based access control** area, which shows the partitions that have exceeded the limit. | 
| You have a partition that contains more than 10,000 users. | You are editing the partition and changing the number of licences. | You can reduce but not increase the number of licenses. | 

> [!Note] 
> The preceding scenarios assume a limit of 10,000 licensed users. If you are working with a partition that starts with a higher number of licenses (because, for example, you contacted Workplace Analytics Support and requested a higher limit), these restrictions apply to the actual limit of the partition. 

## Partitions and organizational data

Partitions depend on organizational data in two ways:

* Partitions can depend on organizational data columns. As described in the **Create filters** step of [To create a partition](#to-create-a-partition), you can define a partition by filtering by organizational data columns. For example, you can define a partition by filtering on an organizational data column called _Country_.
* As described in the **Select attributes** step of [To create a partition](#to-create-a-partition), organizational-data attributes can be configured to be included in the partition for analysts to use.

Because of these dependencies, existing partitions can be affected when an admin, after [uploading organizational data for the first time](upload-organizational-data-1st.md), uploads new data in a [subsequent upload](upload-organizational-data.md). In step 9 of [upload organizational data](upload-organizational-data.md#important-upload-considerations), the admin can select either **Append the existing organization data** or **Replace all existing organizational data with this file**.

Choosing the **Append** option does not affect partitions, regardless of the structure of the new data.

However, the admin can select the **Replace all existing organizational data** option, and the organizational data that they upload could have a new data schema. For example, if the _Country_ column is not present in the new organizational-data upload schema (and if the column is either used as a filter or included in a partition), the definition of any partition that refers to this column is violated.

Because of this possibility, during organizational-data upload (between the mapping step and the validation step), Workplace Analytics checks for partition schema violations. If the schemas of one or more partitions are violated, Workplace Analytics displays the following error:

![Partition violation](../images/wpa/setup/partition-violation.png)

In the lower half of this page, Workplace Analytics identifies the columns that are omitted in the uploaded file but present in the earlier uploaded data (and its schema) and are present in existing partitions. It also names the partitions that are affected by the missing columns.  

   > [!Note]
   > If a column in a new set of data is missing, this affects the schema of a partition only if that column is referred to in the schema. If no partition's schema refers to the missing column, the missing column will not cause an error, and the organizational-data upload will continue on to the validation phase.

In the case of an error such as this, the admin cannot proceed with the current data upload. The admin has these choices:

* Start over by selecting **Back** and then attempt organizational-data upload with data that has a different schema.

* [Edit the affected partition](#to-edit-a-partition) (or partitions). Consider removing from the partition the column that is referred to in the schema, the column that caused the dependency that was violated. You can do this by de-selecting the corresponding attribute in the **Organizational data** table on the **Set attributes** page:

    ![Select visibility](../images/wpa/setup/create-partitions-attributes.png)

  After you remove the column from the partition, try again to upload the .csv file that caused the schema violation.

* [Delete the affected partition](#to-delete-a-partition) (or partitions) and then try again to upload the .csv file that caused the schema violation.

   > [!Note]
   > Schema errors can occur only in user-created partitions. Uploading organizational data does not affect the definition of the Global partition.

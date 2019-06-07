---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Partitions in Workplace Analytics
description: Description of partitions plus how to use and set up partitions in Workplace Analytics 
author: paul9955
ms.author: v-pascha
ms.date: 06/07/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Partitions in Workplace Analytics

A partition is a data workspace for an analyst. A partition delimits the employee data and organizational attributes that an analyst can use for analysis. Companies create partitions that contain subsets of employee data. To do this, they use various criteria. Here are examples:
 
 * **Organization:** A company can create a partition to be the data of all the employees in one division, or under a particular manager. Example: R & D
 * **Geography:** A multi-national corporation might create different partitions for the data of employees of different countries or parts of countries. Example: Wales 
 * **Role:** A company could select the data of all the employees who have a particular function to include in a partition. Example: Accounting personnel

## Partitions give access to data 

A partition defines what data you work with in Workplace Analytics. If you have one of the analyst roles (analyst or analyst limited), you work with data on the **Explore** and **Queries** pages of Workplace Analytics. You are also assigned one or more partitions, and your partition determines whose data you work with on those pages. If you have the program manager (PM) role, you work on the **Solutions** page and your role there is not limited, so you have access to all Solutions plans. 

For example, if you are an analyst with the job of finding workplace trends in the sales organization, you must be assigned a partition that encompasses the data of salespeople. You can then view data about salespeople on the **Explore** pages and create queries about salespeople on the **Queries** page. 

## The Global partition

One particular partition encompasses everyone’s data: the "Global" partition. If an analyst has this partition, they can work with all employee data that’s been uploaded to Workplace Analytics. The Global partition is created by the system. While it exists by default, no analysts are given access to it by default. Analysts must be granted access&mdash;to this or to any partition&mdash;expressly, by an admin. See [Define a partition](#define-a-partition) for more information about assigning analysts to a partition. 

> [!Note] 
> For existing users, as part of one-time migration in 2019, all existing analysts and their existing queries and settings are being moved to the Global partition. 

## Use a partition

If you are an analyst, you must have a partition selected to be able to go to the **Explore** or **Queries** pages. If you are a PM, you work in the Global partition by default and you can go right to the **Solution** page to manage programs. If you are an admin, you create partitions, but you do not work within one. 

### To use a partition

1.	Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, enter your work credentials. If you are a PM or analyst and you have not been assigned a partition, you’ll see a notice that alerts you to that fact:

    ![Must have at least one partition](../images/wpa/setup/at-least-one-partition.png)  
 
If you see this notice, ask your Workplace Analytics admin to assign you to a partition. You cannot start using Workplace Analytics until an admin assigns you to one or more partitions. If you do not see this notice, go on to the next step.

2.	What you see now depends on your role and partition assignments: If you are analyst (you have the analyst or analyst limited role), go to step 3; if you have any other role, go to step 4. 

3.	Step for analysts: 

    * If you have only one partition (even the default "Global" partition), this is the partition that you will use. Skip the rest of these steps. You can go to the **Explore** page or the **Queries** page to start your work. On those pages, you will see only the data to which your partition grants you access.  
    * If you have more than one partition, the **Partition** drop-down menu at the top of the **Home** page displays the partitions that you are linked to. Open this menu and select one:

       ![Select a partition](../images/wpa/setup/select-one-no-global.png)
 
      After you’ve chosen the partition to work with, you can skip the rest of these steps and go to the **Explore** page or the **Queries** page.  

4.	If you have a non-analyst role, your choice depends on the role (or roles) that you've been assigned:

    * **Both PM and analyst:** If you have both the PM role and an analyst role, the data you see depends on the page that you open. Solutions are accessible only in the Global partition. A person with both the PM and analyst roles can access solutions in Global partition and access the **Explore** and **Queries** pages in other partitions that they have been granted. 
    * **PM only:** PMs do not need to select a partition because they automatically use Global partition. If you’re a PM, go to the **Solution** page. 
    * **Not an analyst or program manager:** If you’re signed in to Workplace Analytics and you do not have an analyst or PM role, you are an admin and partition doesn’t affect you. Go to the **Settings** page. 

## Define a partition

Workplace Analytics admins create partitions on the Settings page. One aspect of this task is assigning partitions to analysts. As you, the admin, create a partition, you can assign the partition to one or more analysts.

> [!Important] 
> Plan your partitions carefully before you start to create them. Note the following:
>  * **No more than five partitions.** An organization can have a maximum of five partitions.
>  * **Partitions are not editable.** After you create a partition, the partition cannot be edited. 

### To create a partition

1.	Open the Workplace Analytics **Home** page. If prompted, enter your Microsoft credentials. 
2.	Open the **Settings** page and select **Access control**.
3.	In the **Partition-based access control** area, select **Add partition**:

    ![Admin settings](../images/wpa/setup/admin-settings.png)
 
4.	On the **Access control > New partition** page, type the name of the new partition and optionally type a description. 
5.	**Define filters.** Under **Filters**, add one or more filters to define the data that will fall within the partition that you are creating:

    ![New partition](../images/wpa/setup/new-partition.png)
 
    > [!Note] 
    > You can filter by only one attribute. For example, if you create a filter that uses the Organization attribute, you could produce the following filter clauses:  
    >  * Organization + Equals + <name_of_manager_1> AND 
    >   
    >    Organization + Equals + <name_of_manager_2>
    >   
    > But you cannot add another clause that uses a different attribute, such as:
    >   * Domain + Equals + <domain_name> 

6.	**Select analysts**. Under **Analysts**, select one or more analysts who will have access to this partition. Only the analysts that you select will be able to perform analyses in Workplace Analytics.    
 
    ![Select analysts](../images/wpa/setup/analysts.png)
 
7.	**Select attributes**. Select which attributes from the organizational data to include in the partition. To exclude an attribute from the partition, leave it unselected. 
 
8.	**Select visibility of attributes**. You might want one or more attributes to not be visible to analysts who work in this partition. For example, "sales quota" might be a sensitive attribute that nevertheless has been uploaded in the organizational data. To hide the "sales quota" attribute, select it and then set its **Visibility** to **Hash in report**. 

    ![Select visibility](../images/wpa/setup/select-visibility.png)

## How can I start using partitions?

Currently this feature is being rolled out on a per-customer basis. To have the feature enabled, please reach out to your customer solutions contact or email us at wpasupport@microsoft.com. 


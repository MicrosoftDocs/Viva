---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Seller success solution in Workplace Analytics 
description: Describes the seller success solution and how to create a seller success plan 
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Seller success solution

Sales departments are the most profitable for any company, but their effectiveness can be unpredictable because of the variability in how salespeople work. With this in mind, Workplace Analytics offers the seller success solution. Its purpose is to help sales organizations learn more about the behaviors that differentiate their most successful salespeople, and build plans that help salespeople acquire those behaviors. 

It's not the purpose of the seller success solution to make sellers more productive simply by giving them more data. Rather, it aims to encourage sellers to reflect on how they use their limited time, and to make decisions that align their use of time with the company’s strategic priorities. 

The solution displays insights to help salespeople optimally use their limited time to maximize productivity, conversion rates, and sales revenues. In this case, productivity is defined as spending more time with the right set of customers, leveraging internal networks, and involving their manager and leadership in strategic customer meetings, as needed.

## Create a seller success plan 

**Role:** analyst or limited analyst 

**Prerequisite:** To create a seller success plan, you must have CRM data uploaded. For more information, see [CRM data in Workplace Analytics](../setup/crm-data-upload.md).

Complete the following tasks to create and run a seller success plan: 

 * [Create the plan](#create-the-plan): Take the initial steps to create a plan.  
 * [Select participants](#select-participants): Select participants for the plan either by uploading a .csv file or by using filters.
 * [Start the plan](#start-the-plan): After your list of participants has been validated, start the plan for them.

### Create the plan 

1.	Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, sign in with your work account. 

2.	In the left navigation pane, select **Solutions**. 

3.	On the **Solutions** page, under **Available plans**, on the **Seller success** card, select **Start now**. 
 
    ![Solutions main page](../images/wpa/tutorials/solutions-main-page-w-highlight.png)

    The **Seller success plan** page opens: 

    ![New Seller success plan](../images/wpa/tutorials/set-up-new-seller-plan.png)
 
4.	(Optional) Change the plan name from the default name. 

5.	Go to [Select participants](#select-participants). 

### Select participants

If you have a particular group in mind, you can identify the group in either of the following ways: 

 * [Upload a .csv file](#upload-a-csv-file) 
 * [Use filters](#use-filters)

#### Upload a .csv file

**Prerequisite:** A .csv file that lists the employees you want to participate in the plan. The format of this file is simple: a list of email addresses in a single column. To obtain this file, you might have exported it from an HR system. 

1.	Obtain the .csv file to upload.
2.	Select **Upload .csv file**.
3.	Select **Browse**, select a .csv file, and then select **Open**. 
4.	After the file has been uploaded, select **Validate**.

    Workplace Analytics validates each potential participant. Workplace Analytics reports whether the group successfully validated, and it also displays any warnings that are generated. For more information, see [Validation](#validation). 

5.	After the group validates successfully and the number of participants meets or exceeds the minimum group size, you can proceed with the group that you selected. Go to [Start the plan](#start-the-plan).

#### Use filters

1.	Select **Use filters**.

2.	Add filters to define your group. For example, select **Organization**, **Equals**, and **Sales** in the fields to select the people who work in sales as your group. 

    Optionally, add more function types to expand this group, or add more filtering criteria to refine the selection: 

    ![Use filters to find group](../images/wpa/tutorials/seller-plan-filters.png)

3.	After you have selected the group(s) of participants, select **Validate**.
  
    Workplace Analytics validates each potential participant. Workplace Analytics reports whether the group successfully validated, and it also displays any warnings that are generated. For more information, see [Validation](#validation).

4.	After the group validates successfully and the number of participants meets or exceeds the minimum group size, you can proceed with the group that you selected. Go to [Start the plan](#start-the-plan). 

### Start the plan

1.	(Optional) Change the dates of the **Plan duration**. Do this by editing the start date of the plan. 

2.	Select **Create plan**. This starts the plan for the plan participants. For an overview of their experience, see [Participant experience](#participant-experience). 

## Task notes

### Validation

After you select **Validate**, Workplace Analytics checks for licenses of potential plan participants. Participants must have both a MyAnalytics license and a Workplace Analytics license. If the user is missing either license, or has opted out of MyA, an error is generated and displayed for that user. That user is then removed from the list of potential plan participants. (In validation results, you see only the number of users for whom errors were found; no individual users are identified.) 

After the validation checks have run, if the final list of participants has enough people to meet or exceed the [minimum group size](../use/settings.md#minimum-group-size) set for the organization, you can continue to use this group in creating your plan. 

<!-- ADD THIS CONTENT AFTER THE TRACK PAGE APPEARS
Note: After you start the plan, you can end it by selecting the Stop button on the [what page is this? Show how to navigate there and what other actions you can take there] page. -->
<br>

<!-- Get FWLink to here for use in the product UI -->

[!INCLUDE [Seller success cards](../includes/seller-success-cards.md)]

## Privacy note

The data that is shown in the seller success email belongs to the person who receives that mail. Only they have access to it. Their manager, their admin, and their teammates cannot see it. As is stated at the top of the email, this data is "for your eyes only." For more information, see [Seller insights Q & A](../overview/seller-insights.md#seller-insights-q--a). 


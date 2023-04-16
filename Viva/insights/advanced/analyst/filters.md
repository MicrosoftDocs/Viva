---
ms.date: 02/28/2023
title: Filters in advanced insights queries
description: Learn more about filters in queries
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Filters in advanced insights queries

You'll encounter filters across the advanced insights app: while you're building a query, while you're customizing metrics, and while you're setting up metric rules. In a nutshell, by only picking out values that match certain conditions, filters focus your queries on the data you want to analyze.

>[!Note]
>If you're creating a meeting query, you can only set certain kinds of filters. Read our meeting query documentation for more information on predefined filters.

## Filters and organizational data

### Accessing filters

In each process we described above—queries, metric customization, and metric rules—you'll notice an option to **Add condition** or **Add condition group**. Select these options to start setting up a filter. We describe the difference between conditions and condition groups a little later in this article.

### Filter data

Filters work with two types of data:

* Organizational data your admin uploads or syncs with the advanced insights app - You'll set these kinds of filters up when you run custom person queries and Power BI queries.
* Meeting data - You'll set these kinds of filters up when you run meeting queries.

#### Organizational data

Organizational data is arranged into columns and rows. Columns each contain a different *organizational attribute*, which are categories of non-personal employee information, like **TimeZone**. Rows each contain a specific employee's data related to that attribute. Here's an excerpted example of organizational data: 

|Employee ID       |Organization|TimeZone|Layer|
|------------------|---------|--------|------|
|**Employee 12345**|Engineering  |Pacific| 3
|**Employee 12346**|Operations |Europe/London|4
|**Employee 12347**|Engineering |Europe/Berlin|4
|**Employee 12348**|Engineering |Pacific|4
|**Employee 12349**|Marketing |New York|3

#### Meeting data

Meeting data is arranged in the same way that organizational data is, except that it contains *meeting attributes* instead of organizational attributes. Here's an excerpted example of meeting data:

|Activity ID       |Attendee meeting hours|Number of attendees multitasking|Number of chats sent during the meeting|
|------------------|---------|--------|------|
|**123456789123456789123456781**|0.8333333  |0| 1
|**123456789123456789123456782**|1 |1|1
|**123456789123456789123456783**|10 |1|1
|**123456789123456789123456784**|2 |1|1
|**123456789123456789123456785**|0.5 |1|1

### What filters do

When you set a filter, your query looks at your organizational or meeting data, and then only picks out and analyzes values for the attributes you tell it to. For example, if you set a filter that limited your person query to the Engineering department, your query would find the *Organization* column in your organizational data, and then only analyze rows where the value is "Engineering." In this scenario, the data that the query uses would look like this:

|Employee ID       |Organization
|------------------|---------|
|**Employee 12345**|Engineering
|**Employee 12347**|Engineering |  
|**Employee 12348**|Engineering |


### Using multiple filters

Viva Insights evaluates filters in the order you add them, so you can use several filters to further narrow down the data your query analyzes. Here's a quick example of multiple filters. In this case, the analyst is running a meeting query, and they've set three ["and" condition statements](#using-the-and-conjunction). As Viva Insights processes each of these "and" statements, the number of analyzed meetings reduces:

1. *Recurring = true*. Viva Insights checks whether meetings recur. If they do, the query will use those meetings.
1. *Attendees Timezone = New York*. From those recurring meetings, the query will only use meetings where the attendees are in the New York timezone.
1. *Subject Contains Design*. From those recurring meetings in the New York timezone, the query will only analyze meetings where the meeting title contains the word "Design." 


A visual representation of these filters might look like this:

:::image type="content" source="../images/analyst-filter-meetings-diagram.png" alt-text="Screenshot that shows a flow diagram of condition 1 -> condition 2 -> condition 3"lightbox="../images/analyst-filter-meetings-diagram.png":::

*Filter* is a collective term, because filters are made up of *conditions* and *condition groups*, which we discuss in more detail in the next section.

## About conditions and condition groups

A *condition* is a statement about *one* attribute you want to analyze in your query. Conditions have three parts:

* Attribute, like *Organization*
* Operator, like *=*
* Value, like *Engineering*

>[!Note]
>As we discussed earlier, you can only pick organizational attributes based on what your data already contains. To add new attributes, you'll need to contact your admin.

A *condition group* is a combination of conditions connected with a conjunction ("and" or "or"). Condition groups have more than one condition. Instead of considering conditions hierarchically (condition 1, condition 2, condition 3), Viva Insights considers condition groups altogether (condition 1 & condition 2 & condition 3) when it runs queries.

### The employees counter

Below your condition statements and condition groups, you'll notice a counter that shows two numbers:

* **Total employees** – The number of employees in the whole company who are assigned Viva Insights licenses and *could* be analyzed by a query
* **Measured employees** – Based on the conditions you set, the total number of employees that your query *will* analyze

:::image type="content" source="../images/analyst-filter-total-measured-employees.png" alt-text="Screenshot that shows the Total employees and Measured employees counter.":::

Use **Measured employees** to find out whether your conditions are narrowing down your query like you want them to. If the **Measured employees** count is larger or smaller than expected, you might need to adjust a condition statement or condition group to reflect the right data.


#### Using the "and" conjunction

If you're *only* adding "and" statements, there isn't a big distinction between individual condition statements and condition groups. For example, the number of people a query analyzes will be the same in both of these scenarios:

##### Scenario 1 – separate conditions with "and"

|Condition #|Conjunction|Statement|Measured employees|
|---------|----|-----|------------------|
|1     |-|*Layer = 4*|5015
|2     |and|*Organization = Engineering*| 429
|3     |and|*TimeZone = Europe/Berlin*|26

:::image type="content" source="../images/analyst-filter-andconditions2.png" alt-text="Screenshot that shows three separate and statements.":::

##### Scenario 2 – condition and condition group with "and"

|Condition #|Conjunction|Statement|Measured employees|
|---------|---------|---|---------------|
|1     |-|*Layer = 4*|5015
|2 & 3    |and|*Organization = Engineering* **and** *TimeZone = Europe/Berlin*| 26

:::image type="content" source="../images/analyst-filter-andconditiongroup1.png" alt-text="Screenshot that shows an and condition and an and condition group."lightbox="../images/analyst-filter-andconditiongroup1.png":::

#### Using the "or" conjunction

Things get a little more complex when you start adding "or." Let's discuss a few scenarios where you might use "or" statements.

##### Scenario 1 – separate conditions with "or"

"Or" statements are helpful when you want your query to apply to *any* one of several conditions. For example, let's say you want to capture *all* of these kinds of employees in one query. They don't have to meet multiple conditions for your query to count them:

* People in the Europe/Berlin timezone
* People who have three reporting layers above them, anywhere in the world
* People in the engineering department, anywhere in the world

Between each statement, you'd use the "or" conjunction.

Here's how that would look in a query. Notice how large the number of **Measured employees** is:

|Condition #|Conjunction|Statement|Measured employees|
|---------|---------|---|---------------|
|1     |-|*Layer = 4*|5015
|2| or|*TimeZone = Europe/Berlin*|13673
|3    |or|*Organization = Engineering*| 26925

:::image type="content" source="../images/analyst-filter-orstatements.png" alt-text="Screenshot that shows three individual or statments.":::

When you use "or" in an *individual* condition statement (that is, not a condition group) any other individual condition statements you add also need to be "or" statements. In other words, you can't add an "or" statement and then add an "and" statement as another separate condition statement. 

##### Scenario 2 – creating an "or" group after an "and" statement

You can, however do this:

1. Add an individual "and" condition statement.
1. Add a condition group after that "and" statement.
1. Place an "or" statement within the condition group. 

For example, maybe you actually want to measure:

* Those with three reporting layers above them, who either:
    * Are in the engineering department, anywhere in the world

        *or*

    * Are in the Europe/Berlin timezone

In this case, you'd:

1. Add your first condition, which is *Layer = 4*. 
1. Select the "and" conjunction.
1. Add a condition group. 
1. In the condition group:
    1. Set a new condition, which is *Organization = Engineering*.
    1. Select the "or" conjunction.
    1. Set a new condition, which is *TimeZone = Europe/Berlin*.

Notice how the number of **Measured employees** changes when we turn our "and" condition group from last time into an "or" condition group.

|Condition #|Conjunction|Statement|Measured employees|
|---------|---------|---|---------------|
|1     |-|*Layer = 4*|5015
|2 & 3    |and|*Organization = Engineering* **or** *TimeZone = Europe/Berlin*| 523

:::image type="content" source="../images/analyst-filter-orconditiongroup.png" alt-text="Screenshot that shows an and condition statement and a condition group with an or conjunction."lightbox="../images/analyst-filter-orconditiongroup.png":::

This filter first checks whether employees are Layer 4s. Then, it checks whether employees are in the engineering department ***or*** in the Europe/Berlin timezone.

##### Scenario 3 – creating an "and" group after an "or" statement

Now let's say you want to measure:

* Those with three reporting layers above them

    or
    
* Those who are in the engineering department and also in the Europe/Berlin timezone (that is, Engineers in Berlin)

In this case, you'd:

1. Add your first condition, which is *Layer = 4*. 
1. Select the "or" conjunction.
1. Add a condition group. 
1. In the condition group:
    1. Set a new condition, which is *Organization = Engineering*.
    1. Select the "and" conjunction.
    1. Set a new condition, which is *TimeZone = Europe/Berlin*.

Here's how that would look in a query:

|Condition #|Conjunction|Statement|Measured employees|
|---------|---------|---|---------------|
|1     |-|*Layer = 4*|5015
|2 & 3    |or|*Organization = Engineering* **and** *TimeZone = Europe/Berlin*| 6069

:::image type="content" source="../images/analyst-filter-orstatement-andcondition.png" alt-text="Screenshot that shows an or statement and a condition group with an and conjunction."lightbox="../images/analyst-filter-orstatement-andcondition.png":::

This filter first checks whether employees are Layer 4s. Then, it checks whether employees are in the engineering department ***and*** in the Europe/Berlin timezone. 

#### Using conditions and condition groups in meeting queries

The same ideas apply when you're using filters in a meeting query. However, as we mentioned earlier in this article, the attributes you'll work with will be from meeting rather than organizational data. If you run a filter based on the meeting attendees or organizer, you'll also select organizational data for them.

Here's an example. Let's say you wanted to know how many recurring meetings are organized by marketing or sales departments.

Here's how you'd set up the filters:

1. Add an individual condition statement. Set it to *Recurring = true*.
1. Add a condition group. In the condition group:
    1. Add a condition, which is *Organizer Organization = Marketing*.
    1. Add another condition, which is *Organizer Organization = Design*.

:::image type="content" source="../images/analyst-filter-meeting.png" alt-text="Screenshot that shows an and statement and a condition group with an or conjunction for meeting queries."lightbox="../images/analyst-filter-meeting.png":::
---
title: Comments suppression in Viva Glint  
description: Factors that influence suppression in Glint comments reporting include factors such as filters and question type.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: representative comments, prescriptive comments, exporting comments, sharing commments, saving comments, choosing benchmark, filtering comments, redacting comments, quarantining comments 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 08/06/2024
---

# Comments suppression in Viva Glint

Factors that influence suppression in the Glint Comments report - **or comment reporting in any other report** - include factors such as filters and item (question) type.

**Comment suppression** refers to comments not being visible when the response rate doesn't meet the confidentiality threshold set. Suppression protects the confidentiality of respondents when their identity could possibly be identified. 

These features influence comment suppression:

 - Item (question) type
 - Attribute filters
 - Keywords vs topics
 - Topics and Advanced Filtering

 ## Question types that influence comment suppression

Typically, the confidentiality threshold for comment suppression is 10. At least 10 unique respondents must leave a comment in order for verbatim comments to show in reportion. 

|Survey item type|Relationship to comments|Effect on comment suppression|
|--------|-------------|
|Open-ended|Item that requires a comment only| Meets the confidentiality threshold with 10 unique respondents|
|Multiple choice and rating items| Comments are often optional| If confidentiality threshold is met, comments are visible on the report, even if not all respondents left a comment.|

## Viewing comments

In the **All Comments** section, where no filters are applied, the platform displays the full respondent pool for items that were *answered* by at least 10 respondents. If targeting items to specific groups or basing access on a previous item response, this smaller population impacts the availability to view comments.

:::image type="content" source="../../media/glint/reports/comments-all.png" alt-text="Screenshot of the All Comments section in the Comments report.":::

### Example

**Scenario:**
One item has seven comments and when selected, it indicates suppression. Another item has only two comments but when selected, the comments are displayed. Why aren’t both questions suppressed if neither have at least 10 comments?

**Explanation:**
This section pulls in comments based on mixed item types. Open-ended items must have at least 10 responses to protect confidentiality. 
- Responses from the first item are suppressed because it's open-ended and doesn't meet the confidentiality threshold.
- The second item is a rating or multiple choice item. Even with only two comment responses, comments are visibile because the item itself meets the threshold of having at least 10 respondents. 

## Comments when filtering for multiple surveys

When the Multiple Surveys filter is selected, it brings in data from all the surveys within your selected timeframe. **Comment suppression works on a per cycle basis**, which may cause some results to be suppressed when the Multiple Surveys filter is on. 

Select **Multiple Surveys** from the dropdown menu of the card for the survey you're currently looking at.

:::image type="content" source="../../media/glint/reports/comments-multiple-surveys.png" alt-text="Screenshot of the dropdown menu for selecting the Multiple Surveys filter.":::

### Example

**Scenario:** 
While filtering for multiple surveys, the **Top Questions by Volume** section shows seven items that have comments but the **All Comments** section shows only three of the seven items. When selecting one of the four items that didn't appear in the **All Comments** section, responses appear in the side menu. 

- Why don’t all the questions appear in the **All Comments** section?
- Why do comments display in the side menu when I select one of the top questions by volume?

**Explanation:** 
The **Top Questions by Volume** section lists the most responded to items based on the last time the item was on a survey, which may be one or more cycles before filtering for multiple surveys. As comment suppression is applied on a per cycle basis, it  causes suppression if the confidentiality threshold isn't met for the item in the cycle it's pulling from.

**All Comments** only display comments from the most recent survey during which the item was used. For example, if the filter is pulling in cycles between April 2024 and July 2024, only comments from the July survey display if the April cycle didn't meet the confidentiality threshold. In this scenario, only three of the seven questions met the threshold, which is why they appeared in the **All Comments** section. 

The side menu displays comment responses only for items that met the confidentiality threshold. 

## Comments in the Keywords vs Topics section

**Q: Why is a *topic* that has four comments suppressed when selected, but a *keyword* that also has four comments, displays those comments?**

**A**:
- Topics must meet the confidentiality threshold to display.
- Keywords display no matter the number of respondents.

The **Keywords** section shows the words and phrases that occur most frequently across comments. 

The **Topics** section represents a high-level summary of comments - themes which provide deeper insights into groups of comments. Select any topic to see the comments within. Since the confidentiality threshold applies, if set to 10, at least 10 unique people must leave comments on the topic (within each cycle) to display the open-ended feedback. If enough people don't comment on the topic in any given cycle, the comments are suppressed.

## Topics and Advanced Filtering

**Scenario:**
A topic has 17 comments but when selected, comments are suppressed. This reporting happens for a couple of reasons:

**Explanation 1**
This happens when Advanced Filtering is used. Advanced filtering requires a threshold of 10 responses per item. If the topic is made of many items and none have 10 responses, all comments for the topic are suppressed. If one of the items meets the confidentiality threshold, then comments for that item are displayed, but no others.

**Explanation 2** 
This happens if one person left multiple comments on the same topic. For example, if eight people left 10 comments, they're suppressed.


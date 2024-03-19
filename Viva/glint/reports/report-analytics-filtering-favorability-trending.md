---
title: Viva Glint reporting features
description: "Viva Glint reports can be filtered and analyzed in various combinations to surface insightful and actionable results."
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/18/2024
---

# Viva Glint reporting features

The following terms help you understand Viva People Science terms and ensure that you get the most useful information from your Viva Glint reports. 

|**Term**| **Definition**|
|-----------|-----------|
|Mean score | The average for all provided questions/items in a survey, transformed into a 100-point scale.|
|Engagement score | Calculated by computing the average score for eSat (Employee Satisfaction) - or eSat and Recommend (key driver) - or a customized aggregate. The overall score has the highest correlation with the drivers of engagement, along with outcomes like productivity and retention. This overall score helps managers understand how happy their team is at work. |
|Favorability | Favorability provides the distribution of responses that make up the overall average score. It’s useful to know if there's a strong consistency in responses or if the average is a result of a wide and divided range of opinions. |
|Favorability score  | Favorability is calculated by looking at responses that fall within a specific range based on the rating scale used. <br> In Viva Glint reporting schematics: <br> - Questions scored as favorable show in blue. <br> - Questions scored as neutral show in grey. <br> - Questions scored as unfavorable show in red. <br> For items scored on a 5-point rating scale (Viva Glint’s best practice), <br> - Items scoring mostly 4 s and 5 s are considered favorable.<br> - Items scoring mostly 3 s are considered neutral. <br> - Items scoring mostly 1 s and 2 s are considered unfavorable.   |

## Filter a Viva Glint report 

Viva Glint survey reports use one process across all reports for filtering. This fixed panel identifies survey programs, attributes, and survey item subsets in which your data can be filtered for interpretation. 

Select the **filter symbol** at the top of the dashboard to expand the *Filters* panel. Select **+ Add Filters** to select attributes available in either the *People* section or the *Question Responses* section. Select **X** to hide the filter panel.

### What is advanced filtering? 

Advanced filtering shows how one program impacts another. For example, you can review engagement results filtered by those who had a good onboarding experience.

1. Select **Advanced**.  
2. Select **Yes, enable advanced filtering**. 
3. Select the **+ symbol** that has been added to the Filter panel. Choose the program from the dropdown menu.  

## Understand the scores calculation overview 

**The primary metric (average score)** 

- Best demonstrates how a group rates a particular question or item 
- Provides the strongest insight across different scenarios, including viewing scores for small populations and trends over time 

The average score for each question is the average of all the responses when converted to a 0-100 rating scale.  

**The favorability score** 

In addition to the converted 0-100 rating scale, the Viva Glint platform reports favorability in percentages. There are three categories: Unfavorable, Neutral and Favorable.  

Favorability provides an understanding of the spread and variability of the scores within the average. Looking at how the favorability distribution has changed over time also lets managers know where the movement occurred.    

## Using the mean score over the favorability score is recommended 

Mean scores are: 

- More robust and meaningful to track over time, even for smaller teams. 
- Highly correlated with behavioral, and business outcomes. 
- Consistent with other analysis performed. 

Favorability helps with understanding the spread and variability of responses, but there are drawbacks: 

- The mean score isn't shown. 
- External benchmarks aren't available for favorability scores. 
- Calculations to measure engagement and other areas of sentiment are based on the mean score, not favorability. 
- Percent favorability is prone to error and instability in smaller teams. 
- The mean score is the better statistical predictor of behavioral and business outcomes.  
- Percent favorable isn't consistent with other analyses. 
- Percent favorable only shows the respondents who agree with the statement. No other information is provided (neutral or unfavorable). 
- Percent favorable doesn't reflect changes in scores over time. 

## Understand color coding in Viva Glint reports

**Color coding for Strengths and Opportunities** 

All items are ranked by comparing them to an existing benchmark. The top half of the items are strengths exhibited by your team, and the bottom half are opportunities for your team to focus on. 

- Red: Opportunity - Scores may be above or below benchmark, but items in red are considered opportunities. 
- Blue: Strength - Scores may be above or below benchmark, but items in blue are considered strengths. 
- Gray: Items are excluded from scoring because there's no benchmark comparison, or they're low to medium impact drivers.

**Color coding for the Favorability scale** 

Favorability is calculated by looking at responses that fall within a specific range based on the rating scale used. 

In Viva Glint reporting schematics: 

- Questions scored as favorable show in blue. 
- Questions scored as neutral show in gray. 
- Questions scored as unfavorable show in red.  

**Color coding for the Heat Map report** 

The colors in the Heat Map are meant to allow quick identification of systemic patterns and outliers. Color coding is relative and not absolute. To determine the relative coloring within a Heat Map, Viva Glint looks at the range of scores displayed.  

- The maximum and minimum are always displayed as dark blue and dark red.  
- All scores between the maximum and minimum are evenly bucketed in up to seven different colored buckets, with the median score being shown in the gray middle bucket.  
- For example: If the minimum and maximum scores are 52 and 80, then Viva Glint will create 7 evenly spaced buckets between 52 and 80. 
  - Dark red would be 52-55
  - Dark blue would be 77-80
  - Gray would be 64-68 with the other shades being in between
    *(For changes and differences, the middle gray is used for 0 change or difference. 	Dark red is used for the biggest negative difference/change, and dark blue for the 	biggest positive change, and the other color buckets are evenly spaced between the 	maximum/minimum values and 0 on either side.)* 

## [Understand aggregate trending](https://go.microsoft.com/fwlink/?linkid=2234925)

Aggregate trending supplies historical data over time. A trend point reflects matching items from one cycle to the cycle immediately preceding it. Changing items within an aggregate (group) interrupts trend. 


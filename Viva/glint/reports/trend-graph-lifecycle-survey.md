---
title: Use the trend graph in a Viva Glint Employee Lifecycle program
description: "The Trend Graph for Employee Lifecycle surveys behaves differently than that of recurring survey programs."
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
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/03/2024
---

# Use the trend graph in a Viva Glint Employee Lifecycle program

The Trend Graph for an Employee Lifecycle (ELC) survey behaves differently than the Trend Graph of a Viva Glint *recurring* program. 

- ELC surveys, by default, display scores filtered to responses received in the last 90 days. 
- ELC surveys are always active so reports group based on the date range selected or the default 90 days.  
- ELC responses appear on the dashboard in real time. A manager sees responses on their dashboard after the program thresholds are met and according to their user permissions. 

## When the default period is used 

- The latest data point on the graph is any surveys received within the past 90 days. 
- The next point is the 90 days before the first data point (180 days - 91 days before today). 
- The point on the graph before that date is 90 days before the second data point (270 days - 181 days before today), and so on.  

The date displayed when you hover over data points is Day 1 of that range - meaning that *the most recent* data point is 90 days before today's date (the date being studied). This date isn't capped by the survey launch date. A date earlier than the survey launch date can be displayed on one of these data points. 

  >**Example**: 
   > - Today's date is May 21, 2022. 
   > - The Exit survey launched on January 9, 2022. 
   > - The first data point on the trend graph shows February 21, 202 - 90 days before today's date. 
   > - The second data point on the trend graph shows November 23, 2021 - 180 days before today's date.   

>[!NOTE]
 The trend graph doesn't reference the actual survey launch date when determining the date to display. It uses 90-day intervals. In this scenario, no responses were     received from November 23 - January 8th as the program did not open until January 9th

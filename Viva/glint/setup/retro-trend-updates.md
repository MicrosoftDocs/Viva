---
title: Retroactive updates for employee trend reporting
description: For data to follow an employee, a retroactive update is applied to the previous survey. 
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 07/01/2024
---

# Retroactive updates for employee trend reporting

For data to follow the employee, a retroactive update needs to be applied to the previous program cycle. Scores are updated either at an attribute or global level to reflect today’s organizational structure. Considerations include:
 - **Retroactive updates are not reversible and impact trend.**
 - Applies the current version of your Human Resources Information System (HRIS) attributes to the past surveys. *Exception: a change in an employees' status (ACTIVE to INACTIVE) doesn't remove or update participation, headcount, or score. If someone is invited to take the survey, they're always part of that survey data.
- If an employee participated in a survey cycle but is no longer ACTIVE for the current cycle, their response isn'tremoved. This 
response still rolls up to their same manager from that cycle. 
- Retroactive updates impact the ability to look at past data as it was originally. Previous data structure is no longer available.
- Retroactive updates move all data to current hierarchical structures.  
- In some cases, leaders may inherit lower scores; communication is recommended.
- Past Action Plan recommendations aren't automatically updated based on the new data set.

## Retroactive update examples:

|Example step|Survey 1| Survey 2|Retroactive update|
|:-------:|---------|------------|--------------|
|Manager hierarchy| <ul><li>Scott is the head of **HR**<li>Scott directs 22 employees<li> Scott's eSat score = 92</ul>|<ul><li>Scott is the head of **Sales**<li>Scott has 50 employees<li>Scott's eSat score = 87</ul>|<ul><li>HR Survey 1 score is updated to show the score of the 50 Survey 1 employees to calculate the trend of Scott's current employees.s<li>HR Survey 1 score is updated to show the score of the 50 **Sales** employees at the time of Survey 1. The eSat score is no longer 92.</ul>|
|Retroactive behavior|<ul><li>Mindy is in **Finance**<li>Mindy's eSat score = 71.</ul>|<ul><li>Mindy moves to **Marketing**<li>Mindy's eSat score = 75.</ul>|Trend <ul><li>Mindy takes their eSat score of 71 to Marketing.<li>Marketing shows Mindy's score as if it was part of Survey 1 for **Marketing,** *not Finance.*</ul>|
|Effect on organizational scores at employee level|**Finance** <ul><li>8 employees <li>eSat = 78 </ul> **Marketing** <li> 10 employees <li>eSat = 56</ul>|**Finance** <li>20 Employees <li>eSat = 82<li>5 from Marketing + 7 new<br> </ul><br> **Marketing** <li>5 employees<li>eSat = 67 <li> 5 employees left to go to Finance and no new employees </ul> | **Finance** <ul><li>Shows 13 employees, now including 5 from Marketing <li> the 7 new employees aren't included<li>New eSat score no longer shows trend, which existed in Survey 1 </ul> **Marketing**<li>Shows 5 employees, as 5 employees moved to Finance<li>New eSat score and trend aren't  as seen previously  <li> **Trend is recalculated based on 5 employees.** </ul>|


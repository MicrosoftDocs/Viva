---
title: Manager reporting access when changing team or role
description: Viva Glint uses a "data follows the manager" approach. If a manager moves to a different team, recent survey scores go with them until the first survey cycle for their new team is available.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: trend, manager trend, adding managers, managers changing teams
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 08/19/2024
---

# Manager reporting access when changing team or role

Viva Glint uses a "data follows the manager" approach. If a manager moves to a different team, their recent survey scores go with them until the first survey cycle for their new team is available.

Each survey is a “snapshot in time." Survey results are based on the current organization and 
manager hierarchy during the window of the survey. 

## Add new managers to the User Roles feature

The Glint admin needs to add a *new* manager to the appropriate Manager role in [User Roles](https://go.microsoft.com/fwlink/?linkid=2230740).  

A manager *changing* teams is automatically updated in the platform to their current team.

## Trend follows managers

When data follows the manager, the data is always preserved within that survey cycle. The cycle is always available for review,
regardless of organizational changes. Responses roll-up through the manager hierarchy so a manager's upline always sees the roll-up of all responses.

>[!TIP]
> Viva Glint recommends that trend follows the manager because:
> - Survey results are frozen and apply the current organization and manager hierarchy during the survey window.
> - When data follows the manager, the data is preserved. In the reporting platform, you can toggle to a previous program cycle and view the exact scores the manager saw. 
in that time period regardless of future organizational changes.
> - Historical scores stay the same for managers, reducing the potential for confusion. 
> - If a retroactive update is applied, the previous data is no longer available.

**When a manager views trend, it's based on any scores previously collected.**

### Trend example: Manager hierarchy - employee

:::image type="content" source="../../media/glint/setup/manager-hierarchy-employee.png" alt-text="Screenshot of a Manager hierarchy, employee trend example.":::

Trend for employee **Ben**

**Survey 1**
- Ben’s manager is Mike (HR).
- Ben’s eSat score of 76 is part of Mike’s Team score and feeds into the HR overall score.

**Survey 2**
- Ben moves to Finance and now reports to Lucy.
- Ben's eSat score of 76 stays as part Mike’s trend. 

**Future organizational changes don't affect any scores.**
- Ben always has the eSat score of 76 for Survey 1.
- Ben's score always feeds into the trend score for Mike.

### Trend example: Manager hierarchy - manager

:::image type="content" source="../../media/glint/setup/manager-hierarchy-manager.png" alt-text="Screenshot of a Manager hierarchy, manager in new role trend example.":::

Trend for manager **David**

**Survey 1** 
- David is a manager under manager Brian.
  - David manages Team 1.
  - David's team has an engagement score of 82. 

**Survey 2**
- Michelle left the company.
- David takes over to manage team 2.
  - David takes his score from survey 1 for engagement with him (82).
  - David doesn't inherit Michelle’s score from survey 1.
  - The trend score for Michelle in survey 1 was a snapshot in time based on employees' feedback.
  - There's no link of Michelle's score to David.

**In this scenario, the team can share Michelle’s report from survey 1.**

### Trend example: Manager hierarchy

:::image type="content" source="../../media/glint/setup/manager-hierarchy-3.png" alt-text="Screenshot of a Manager hierarchy, new manager trend example.":::

**Survey 1**
- Caroline is the manager for Team HR.
- The HR team's eSat score is 91.

**Survey 2**

- Tracey left the company.
   - Tracey continues to show in historical reports in the manager hierarchy.
- Caroline moved over to Team Comms as manager.
  - Caroline keeps the history of the 91 eSat score.
- Team HR gets a new manager.

**Organizational restructure:** 
- New managers don't appear in the trend
- Changes in organizational levels don't appear in data.
- The new HR manager doesn't inherit Caroline's trend

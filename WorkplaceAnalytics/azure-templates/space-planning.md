---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Workspace Planning Azure Template for Workplace Analytics 
description: Learn about the Workspace Planning Azure Template for Workplace Analytics and how to use it for advanced data analysis
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Workspace Planning Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates include the Workspace Planning template that enables a quantitative solution to effectively identify and seat teams in a specified workspace. This planning can help maximize and foster physical workspace for teams and for cross-team productivity and collaboration.

The template combines Workplace Analytics data with your team size and workspace floor capacity and distances between floors and buildings to generate floor plans with recommended seating.

## Use cases

* **Moving to a new workspace** and your organization wants to know the best workspace plan for employees within a building that'll promote the most effective team and cross-team collaboration.
* **Reorganizing an existing workspace** and your organization wants to generate an optimized floor plan and compare it to the current floor plan, based on current communication patterns.

## How it works

This template combines Workplace Analytics data with your team size, workspace floor capacity, and the distances between the floors and the buildings to generate floor plans with recommended seating.

 * [Interaction](#create-the-interaction-file): This is a Workplace Analytics group-to-group query that includes meeting and email activity for insight into current work and collaboration patterns.
 * [Space capacity](#create-the-space-capacity-file): This file includes details about the maximum capacity for the workspace.
 * [Distance](#create-the-distance-file): This file includes details about the walking distances in a unit you specify, such as minutes or meters that can be estimates, between floors or buildings.
 * [Team size](#create-the-team-size-file): This file includes details about the number of employees in each team in your organization.

This template combines the data in these files and generates a table that shows where to seat people in the specified floor plan.

   ![Workspace Planning data](./images/wsp-data.png)

## Key features

* **Interactive mode**: Enables you to interactively change the floor plan results, such as the number of team members on each floor or in each office, within the application, and then it updates the results to reflect these changes.
* **Fixed seats mode**: Enables you to specify a constraint that a certain number of seats for a team must be adjacent to another team. For example, certain number of seats of Team 1 are always close to Team 2. Requires a different version of the team_size .csv input file.
* **Office-level seats**: Enables you to differentiate between two seat types, such as Office and Workpoint, or two other variables of your choosing. For example, if your team requires 100 regular desks, and 5 offices, you can modify your base files set those as constrains when trying to optimize your team’s placement within a floor. Requires a different version of the space_capacity and team_size .csv input file.
* **Relative constraints**: Specify a specific distance or collaboration constraint for certain teams. For example, Team 1 be seated less than 15 minutes from Team 3. Requires an additional **Constraints.csv** input file.

## Deploy and configure the template

1. Confirm you meet the [Prerequisites](deploy-configure.md#prerequisites) for deploying the template.
2. Complete the steps to [Deploy and configure](deploy-configure.md#deployment) the template.

## Create the Interaction file

1. Confirm you are assigned the [Analyst role in Workplace Analytics](../use/user-roles.md), which is required to create this file.
2. Sign in as an Analyst and open [Workplace Analytics](https://workplaceanalytics.office.com/Home).
3. Select **Analyze** > **Queries**.
4. In **Start custom query**, select **Group-to-group query**.

   ![Interaction group-to-group query](./images/wsp-g2g-query.png)

5. Enter or select the following to create the query.

   * Name: **Interaction**
   * Group by: **Week**
   * Time period: **3 months** (to start with)
   * Meeting exclusion: **Tenant Default Meeting Exclusion Rule**
   * Select metrics: **Collaboration Hours**
   * Time investors
      * Group the time investors by: **Organization**
      * Limit the analysis to certain time investors: *None*
   * Their collaborators
      * Exclude collaborators: *None*
      * Group people who collaborated with time investors: **Organization**
      * Focus analysis on a set of collaborators: *None*

6. At the top right, select **Run** to create the query.
7. After the query is successfully created, in **Queries** > **Results**, locate and select the **Download** icon for your new Interactions query, and then save the zipped file.

   ![Download query](./images/wsp-download.png)

8. Locate and right-click the **interaction.zip** file, select **Extract all**, and then select **Extract** and specify the folder.
9. Confirm the new file is named (or rename it as) **interaction.csv** (exact file name is required).

## Create the Space capacity file

### Key term

**Total_Capacity** is the total number of individual desks and office seats that are available within a specified workspace.

1. Open and save the [space_capacity.csv](https://docs.microsoft.com/Workplace-Analytics/azure-templates/images/space_capacity.csv) file to local storage.
2. In the **Floor** (first) column*, replace the example floor names with your own that match the same format of [**Building name** - **Floor number**], as shown in the following graphic.

   * Use valid characters, which include: a-z, A-Z, 0-9, "-", and “ ” (spaces)
   * Do not use invalid characters, which include: “_” (underscores) and “,” (commas)

3. In the **Total Capacity** row, replace the example numbers with the maximum capacity for each of the corresponding floors listed.
4. If you have office-level seats to define, continue to the next set of steps. Otherwise, save and close the file.

   ![Space capacity table](./images/wsp-space-table.png)

### For Office-level seats

1. Open the space_capacity.csv file you just created in the previous steps.
2. Add a new column and name it **Workpoint Seats**.
3. Add another new column and name it **Office Seats**.
4. In the **Workpoint Seats** column for the associated space, list how many seats are standard desks within that workspace. If the workspace has no available seats, enter 0 (zero).
5. In the **Office Seats** column for the associated spaces, list how many office seats are available within that workspace.
6. Your final floor plan should look similar to the graphic in the next section.
7. Save and close the file.

## Create the Distance file

> [!Note]
> * You need the measures of distances between floors, which can be any unit, such as minutes, seconds, or meters, and can also be estimates.
> * For distances between floors directly above and below each other, use a default value of 15.
> * Start your distance measurements by walking at a normal pace across the furthest distance of teams on a single floor. This will be used as the benchmark distances of all teams throughout the campus.

### About floor distance

The following graphic depicts a building with four floors. The distance between each parallel floor needs to be the same consistent value. You can use the default value of 15 for parallel floors, which is a good estimate of how long it takes to get from one floor to the next in the same building.

   ![Floor distance explained](./images/wsp-distance-estimate.png)

1. Open and save the [distance.csv](https://docs.microsoft.com/Workplace-Analytics/azure-templates/images/distance.csv) file to local storage.
2. In the first row and the first column, replace the example data with the locations you want processed with the structure that match the same format of [**Building name**-**Floor number**], similar to the data shown in the following graphic.
3. Starting in the second row and column, enter the distances where the corresponding locations intersect to denote the distance between the two locations.
4. Save and close the file.

   ![Distance table](./images/wsp-distance-table.png)

## Create a Team size file

> [!Note]
>Employees can only be included in one team.

### Key terms

* **Team** is the name of the team or group that is being moved, which should match the names of the teams within the Interaction file.
* **Actual Size** is the total number of people that are a part of the team to account for during the move.

1. Open and save the [team_size.csv](https://docs.microsoft.com/Workplace-Analytics/azure-templates/images/team_size.csv) file to local storage.
2. Starting in the second row, replace the example data with your own that matches the same format, similar to what's shown in the following graphic.

   * **Team**: Enter the name or function of each team.
   * **Actual Size**: Enter the number of employees that are in each corresponding team.

3. For fixed seat formats, continue to the next set of steps. Otherwise, save and close the file.

   ![Team size table](./images/wsp-team-table.png)

## To generate a Floor Plan

1. In the Workspace Planning Azure Template, select **Space Planning** on the left.
2. Click **Select Data Files** at the top right.
3. Select **Choose File**, and then select all four .csv data files that you created in the previous steps (interaction, floor_capacity, distance, and team_size).
4. Select **Submit**, which results in a new page for each file and a Floor Plan page
that shows the calculated floor plans and how many employees from a team can sit where.

   ![Workspace Planning Floor Plan](./images/wsp-floor-plan.png)

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [What's new in Workplace Analytics Azure Templates](./release-notes.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
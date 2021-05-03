---
title: Workspace planning introduction
description: About the Workspace planning tool and how to use it to create seating plans
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin

---
# Workspace planning tool

If your team or company is moving to a new worksite or you need to reorganize an existing workspace, this tool can help. Workspace planning can identify and seat teams together in a workspace that maximizes and fosters cross-team productivity and collaboration. You can use this tool to generate floor plans quickly and objectively, in a data-driven way that optimizes employee collaboration by seating teams together.

The algorithm for this Workspace planning tool accounts for the following rules and constraints:

* **Teams stay together** - When a workspace can seat everyone on the team, it will keep them all together.
* **Teams who collaborate the most sit together** - Based on the collaboration patterns and the distances between spaces, if team A spends most of its time with team B, the two teams are assigned workspaces that are as close together as possible.
* **The most central team is in the most central workspace** - As lower priority than the previous two, the tool can help you determine which floor plans are better than others for seating specific teams in central locations.
* **Everyone gets a seat** - All team members get an assigned seat in a workspace.
* **People and seat assignments must match** - No workspace is assigned more people than it has seats for and no workspace can have a negative number of people assigned to seats.

You can create seating plans that require different variables, such as the following:

* Colocate teams who collaborate the most with each other within the same multi-floored building that has multiple zones or neighborhoods.
* Cross-team collaboration around constraints for specific teams. For example, the HR team must be located together on the first floor in the same neighborhood and Zone A must be next to the file room.
* Create seating for alternating or rotating work schedules for teams who share a workspace on different weeks or days.

## Prerequisites

Before you can use the tool, confirm the following required prerequisites are met.

* **Anaconda** - Use to install and manage the following required versions of Python and Jupyter Notebook. See [Anaconda](https://www.anaconda.com/products/individual#windows) to install it. During the installation, select to **Register Anaconda as your default for Python**.
* **Python** - Latest available or version 3.3 or later is required.
* **Jupyter Notebook** - An open-source application that's required to run the Workspace planning tool.

## File prep

The tool requires the following Jupyter Notebooks and a text file that you must save in a **master copy folder**. You'll use this folder to create a copy of for each workspace project.

* **Distance helper notebook** - Creates a distance file between specified zones or neighborhoods. This uses the following input files to help you define the walking distances in a unit you specify, such as estimated minutes or meters between floors or buildings.
* **File validations notebook** - Validates all the input files, including the distance file that's created from the Distance helper notebook.
* **Generate Floorplan notebook** - Creates a floor plan from the validated input files and reruns the algorithm on the floor plan.
* **Requirements text file** - Documentation for the tool.

### Input files

You also need the following input (.csv) files to define the relevant information for each workspace project, such as team size and workspace capacity. The tool uses these to generate floor plans with recommended seating.

* [Interaction](space-planning.md#create-an-interaction-file) - This is a Workplace Analytics group-to-group query that shows current work and collaboration patterns across the different teams.
* [Space capacity](space-planning.md#create-a-space-capacity-file) - Defines the workspace, which an be a combination of buildings, floors, and zones or neighborhoods, and the maximum capacities for each.
* [Team size](space-planning.md#create-a-team-size-file) - Defines the number of employees in each team in your organization.

The tool combines the data in these files to generate a table that shows where to seat people in the specified floor plan.

   ![Example floor plan](./images/wsp-example.png)

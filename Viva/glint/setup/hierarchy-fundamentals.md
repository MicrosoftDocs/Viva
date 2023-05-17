---
title: Viva Glint organizational hierarchy fundamentals
description: Learn how Viva Glint uses managerial hierarchy as the primary hierarchy ranking and processes the levels automatically, with a capacity of up to 10 levels.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: managerial hierarchy, locational hierarchy, departmental hierarchy
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/04/2023
---

# Viva Glint organizational hierarchy fundamentals

## Understand and set up hierarchies

A hierarchy filters down an employee's attributes into levels from highest to lowest, or largest to smallest, to provide precise insights into a survey. There are three main hierarchies within the Employee Attribute Template:

- Managerial
- Locational
- Departmental

## Establish your managerial hierarchy

Managerial hierarchy is typically used as the primary hierarchy ranking. Managerial hierarchy is the only hierarchical level that Microsoft Viva Glint processes automatically. Every employee in your organization should have a manager. The only person on your Employee Data File who won't have a manager associated with them is your organization's CEO or top-level person. 

### Example of setting up managerial hierarchy

- In this scenario:
  - Harper reports to Tate
  - Tate reports to Gabriel
  - Gabriel reports to Dana
- In the Employee Attribute File:
  - Harper's row would list Tate's Manager ID or email in the Manager ID column 
  - Tate's row would list Gabriel's Manager ID
  - Gabriel's row would list Dana's Manager ID
- The hierarchy ends with Dana, as Dana is the CEO, who doesn't report to anyone

The Viva Glint system automatically configures Harper's hierarchy level within their company as:

- Level 1 – Dana
- Level 2 – Gabriel
- Level 3 – Tate
- Level 4 - Harper

## Establish your locational hierarchy

The size and proximity of your organization will determine if you choose to use locational hierarchies within your custom attributes. 

### Example of setting up locational hierarchy

*North America > United States > California > Sunnyvale*

In this example, four columns are needed on the Employee Attribute Template

- Locational Level 1 – Continent
- Locational Level 2 – Country
- Locational Level 3 – State
- Locational Level 4 - City

You can customize the locational hierarchies for your organization. This example was four levels, but your organization may only have two of the maximum 10 levels.

## Establish your departmental hierarchies

Like locational hierarchy, the size of your organization will determine if you choose to use departmental levels within your custom attributes. 

### Example of setting up departmental hierarchies

*Company name > Department > Function > Subfunction*

Four columns are needed to enter this departmental hierarchy on the Employee Attribute File:

- Departmental Level 1 – Company (ex: Thrive)
- Departmental Level 2 – Department (ex: IT)
- Departmental Level 3 – Function (ex: Operations)
- Departmental Level 4 – Subfunction (ex: User Support)
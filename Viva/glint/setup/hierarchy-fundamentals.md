---
title: Viva Glint organizational hierarchy fundamentals
description: Learn how Viva Glint uses managerial hierarchy as the primary hierarchy ranking and processes the levels automatically, with a capacity of up to 10 levels.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: managerial hierarchy, locational hierarchy, departmental hierarchy, matrix hierarchies
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/30/2024
---

# Viva Glint organizational hierarchy fundamentals

A reporting hierarchy in Microsoft Viva Glint filters data into levels from highest to lowest, or largest to smallest, to provide precise insights into employee feedback. 

> [!NOTE]
> Viva Glint allows for up to 10 reporting hierarchies, including a manager hierarchy. Each reporting hierarchy can have up to 10 levels, except for the manager hierarchy, which calculates up to 25 levels.

## Manager hierarchy

Manager hierarchy is typically used as the primary reporting hierarchy and is the only hierarchy that Viva Glint processes automatically with file uploads. Every employee in your organization should have a Manager ID except your organization's CEO or top-level leader.

> [!IMPORTANT]
> The Viva Glint label for your managerial hierarchy is "Manager." Ensure that no attributes in your employee data are also labeled "Manager." This results in file upload issues.

### Example

In this scenario:
  - Leonie reports to Marcio
  - Marcio reports to Archie
  - Archie reports to Angel

In an employee data file:
  - Leonie's row would list Marcio's ID in the Manager ID column 
  - Marcio's row would list Archie's ID
  - Archie's row would list Angel's ID
 
 The hierarchy ends with Angel, as Angel is the CEO, who doesn't report to anyone.

:::image type="content" source="../../media/glint/setup/mgr-hierarchy-filter.png" alt-text="Screenshot of manager hierarchy filters in Glint reporting, drilling down from level 1 to level 3.":::

The Viva Glint system automatically configures Leonie's hierarchy level within their company as:

- Level 1 – Angel
- Level 2 – Archie
- Level 3 – Marcio
- Level 4 - Leonie

> [!IMPORTANT]
> Matrix manager hierarchies aren't recommended in employee data. Viva Glint only calculates levels for one manager hierarchy and Viva Glint Admins can't add new hierarchies after initial attribute setup. Matrix manager levels require manual maintenance and updates by your organization.

### Multiple CEOs

Viva Glint's best practice is to select a single user in your employee data as the top level/CEO whose Manager ID value is blank. If your organization has multiple leaders that should sit at the top of your manager hierarchy, your organization can add a placeholder "CEO." All top-level users can then report to this placeholder CEO and appear as level 2 managers in Glint reporting and filters:

:::image type="content" source="../../media/glint/setup/placeholder-ceo-filter.png" alt-text="Screenshot of manager hierarchy filters in Glint reporting, with a placeholder CEO as the top-level user and multiple CEOs as level 2 managers.":::

#### Considerations

Before adding a placeholder CEO to your employee data:

- Determine whether your organization can manually insert a placeholder CEO in employee data files each time they're uploaded to Glint.
- Ensure that the Top-Level Manager selection in [General Settings](manage-general-settings.md) aligns with your placeholder CEO user or is left blank.

## Hierarchy groups

Depending on the size of your organization and reporting needs, Viva Glint Admins can set up other non-manager reporting hierarchies. Include attributes in employee data for each level of these hierarchies, which commonly include location or department information.

### Example: location hierarchy

**NAMER > USA > Chicago**

:::image type="content" source="../../media/glint/setup/location-hierarchy-filter.png" alt-text="Screenshot of location hierarchy filters in Glint reporting, drilling down from level 1 to level 3.":::

In this example, three columns are needed in employee data to create a location hierarchy in Viva Glint:

- Level 1 – Region
- Level 2 – Country
- Level 3 – City

This example includes three levels, but Viva Glint admins can customize the location hierarchies for your organization to include up to 10 levels.

### Example: department hierarchy

**Department > Division**

:::image type="content" source="../../media/glint/setup/dept-hierarchy-filter.png" alt-text="Screenshot of department hierarchy filters in Glint reporting, drilling down from level 1 to level 2.":::

Two columns are needed in employee data to create a department hierarchy in Viva Glint:

- Level 1 – Department
- Level 2 – Division

## Next step
Use Viva Glint attribute and hierarchy information to populate your Viva Glint Employee Attribute Template, which serves as a planning tool for your employee data file attributes, layout, and format.

> [!div class="nextstepaction"]
> [Viva Glint Employee Attribute Template](create-employee-attribute-template.md)

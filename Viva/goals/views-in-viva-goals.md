---
title: Views in Viva Goals
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn about the customizable views to easily surface OKRs and projects as you navigate across teams."
---

# Views in Viva Goals

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## What are views

Views in Viva Goals let you find OKRs & Projects across different entity (Company/Team/My OKR) pages easily. You can use the rich filtering capabilities and grouping controls on how OKRs and projects are grouped and listed. You can also select from a list of preset views, create custom views and share them, or set them as the default view for an entity.

## Default view

The default view across the **Company**, **Team**, and **My OKR** pages will show the list of **all active OKRs** in the current active time period your organization is in. This default view is the one initially set by Viva Goals. You can create a custom view or use any of the preset views as the default view.

:::image type="content" source="../media/goals/default-view.png" alt-text="The default view displaying all the OKRs":::

## How can I set a view as default?

To set a new view as default:

1. Open the views dropdown and hover over the view of your choice.
1. Click on the “More Options” right next to the view name and click **Set as default view**.

   :::image type="content" source="../media/goals/set-as-default-view.gif" alt-text="Setting the default view":::

   Alternatively, if you wish to set a view that you’re seeing as the default option, you can use the “More Options” next to the view title and click **Set as default view**.

## Who can set default views? 


|Pages to set Default View For  |Entity  |
|---------|---------|
|My OKRs and Projects page     |   Every individual can set their own default view for their OKR and project pages.       |
|Team OKRs and Projects page     |  Team owners and administrators are allowed to set default views for Team and Sub-team OKRs and Projects page.       |
|Company OKRs and Projects page     |   Only organizational administrators are allowed to set default views for Company OKRs and Projects page.      |

## View options

Each view has a list of ‘More Options’ that lets users perform a set of actions on the view such as:

- Duplicate
- Rename
- Delete
- Set as Default View
- Get Info 
- Print

:::image type="content" source="../media/goals/list-of-actions-on-a-view.gif" alt-text="The list of actions that can be performed on a view":::

## Preset Views

Preset views are readily available views that categorize OKRs and projects based on their status, time period, and so on, and help easily surface OKRs and projects you’re looking for. The list of preset views varies according to the Company/Team/My OKR page. Here’s the list of preset views available across each entity OKR page in Viva Goals.

|Preset OKR views  |Entity (Individual/Team/Company OKR page)  |Description  |
|---------|---------|---------|
|Active period OKRs     |   My OKRs, Team OKRs, Company OKRs      |     List of all OKRs that are active time periods. “Active time period” is derived based on the time periods that are grouped together as “Active” in the time period picker. For example - Annual + Q2 + H1 can be grouped together and considered as “Active” |
|Upcoming OKRs     |   My OKRs, Team OKRs, Company OKRs      |     List of all OKRs associated with the immediate upcoming time period.     |
|Previous OKRs     |   My OKRs, Team OKRs, Company OKRs      |     List of all OKRs associated in the immediate previous time period.     |
|OKRs needing attention     |   My OKRs, Team OKRs, Company OKRs      |    List of all OKRs that have the ‘Not Started’, ‘Behind’ and ‘At Risk’ status.      |
|Manager & Direct Reports’ Active OKRs    |   My OKRs      |   List of your Manager and Direct Reports’ OKRs that are active in the current time period.      |
|Manager & Direct Reports’ OKRs needing attention     |    My OKRs     |     List of your Manager and Direct Reports’ OKRs that have the ‘Not Started’, ‘Behind’ and ‘At Risk’ status.    |
|Current OKRs     |   My OKRs, Team OKRs, Company OKRs      |    List of OKRs that are in the current time period. “Current time period” is derived based on the time period setting of your organization.      |
|Immediate Sub-Team’s Active OKRs     |   Team OKRs      |     List of all the Sub-Team’s OKRs that are active in the current time period.    |
|Immediate Sub-Team’s OKRs needing attention     |    Team OKRs     |      List of all the Sub-Team’s OKRs that have the ‘Not Started’, ‘Behind’ and ‘At Risk’ status.   |

## Creating a custom view

To create a custom view:

1. Select any preset view of your choice and click on **More Options**. 
1. Click on the **Duplicate** option or **Rename** option.

> [!NOTE]
> - If you click on Duplicate: Add filters to customize the view.
> - If you click on Rename: You can choose to save it as a new view and customize it.
 
3. Name your view and choose if you want to keep the view private or make it available for everyone in the organization.
4. Save your view!.

   :::image type="content" source="../media/goals/creating-a-custom-view.gif" alt-text="Creation of a custom view":::

## Who can create custom views?

All users can create and share custom views. The custom views created for any entity will be listed on the same entity’s view page.

## Filters

Filters help you customize your OKR and Project views according to your requirements. The list of filters available right now are described in the following table:

|Filter Name  |Description  |
|---------|---------|
|Time period     |   Filter by the active, previous or upcoming time periods.      |
|OKR Type     |    Filter by the entity the OKR/project belongs to (individual, team, organization).      |
|Owner     |   Filter by the owner of the OKR/project. You can also refine the list by enabling or disabling the **Include Managers**, **Include Direct Reports** check boxes.       |
|Status     |    Filter by the OKR status.     |

:::image type="content" source="../media/goals/filters.gif" alt-text="The various filters":::

## Group By

The grouping option lets you streamline your OKR and Project views even further. You can group your OKR or project list by the following categories:

- Time period
- Entity
- Owner
- Status

The default group by option is relative to the applied filters or preset views. For example, if you’ve selected the **OKRs needing attention**” view, the OKRs are automatically grouped and listed by **Status**.

:::image type="content" source="../media/goals/grouping.gif" alt-text="Grouping the filters":::

## Flat-list OKR views

The flat-list view for OKRs gives users the ability to view all OKRs of any particular entity (Org/Team/Individual) and the time period in a single flat-list view without having to expand them every time i.e. in case an OKR of the entity (Organization) and time-period  (Q3 2021) has a child belonging to the same entity and time-period, usually the child is aligned, hidden under the parent. With this 'view option' users can flatten the list view and see the children right below the parents.

### How can users toggle between only parent OKRs and all OKRs?

1. Choose the entity and time period of the OKRs.
1. Click on the **View Options** dropdown list. Turn on the **Show flat-list view** toggle if you wish to view both parent & child OKRs one below the other.

   :::image type="content" source="../media/goals/flat-list-view.png" alt-text="The flat-list view":::
1. If the users wish to view only parent OKRs, the toggle needs to be turned off and the children will be hidden under the parent (visible on expanding the row).

## Custom multi-selection of time periods

The multi-select option for the time period filter in OKR views allows you to view all your OKRs across multiple time periods. With this feature, you will have the ability to select and view OKRs across all time periods or multiple active/upcoming/previous time periods and have a single view of your OKRs grouped by each time period.  This is especially useful when you have active OKRs for more than one time period that need to be worked upon or tracked.

For example, say you want to view active OKRs across different time periods (Annual, Q2 2021, and Q3 2021), you can multi-select these time periods and save them as a view.

### How to multi-select time periods in Viva Goals?

1. Log in to Viva Goals and view and click on individual-level, team-level, or organization-level OKRs from the left panel.

   > [!NOTE]
   > Your default view will list "Active Period OKRs"; this view contains the list of all the OKRs for the active time period. "Active time period" is derived based on the time periods that are grouped together as “Active” in the time period picker.

   :::image type="content" source="../media/goals/active-period-okrs.png" alt-text="The variouss active period OKRs that are listed":::

   :::image type="content" source="../media/goals/active-time-period.png" alt-text="Active time period":::

2. To select multiple other time periods, click the **Filter** option and select all the time periods that apply, and hit **Done**.

   :::image type="content" source="../media/goals/selecting-multiple-time-periods.png" alt-text="Selecting multiple time periods":::

You can also save this view as a new view by clicking the **Save View** icon right next to the view header.

:::image type="content" source="../media/goals/save-view-icon.png" alt-text="The save-view icon":::

You can now view the list of all OKRs across multiple time periods.

> [!NOTE]
> With the introduction of Views in Viva Goals, the time period picker in Viva Goals has been moved as a filter in the filters panel. Learn more about Views in Viva Goals [here](https://help.ally.io/en/articles/5319075-views-in-ally-io).

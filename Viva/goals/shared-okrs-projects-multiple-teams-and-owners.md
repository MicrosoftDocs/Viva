---
title: Shared OKRs/projects - Multiple teams and owners
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
description: "Learn how to have an OKR/project shared across multiple teams and owners on Viva Goals"
---

# Shared OKRs/projects - Multiple teams and owners

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

The Shared OKRs/projects feature in Viva Goals is a great method for multiple teams and owners to collaborate on their key priorities and initiatives with equal ownership.

## When to create shared OKRs/Projects with Multiple Teams/Owners?

- When an OKR is a key priority for two or more functional teams and the team leads need to have shared accountability as the exact contribution cannot be proportioned or separately broken down between them. When both the teams are supposed to commonly own and work toward the outcomes, it's good to tag multiple stakeholders and not just a single team/owner as accountable.


    ```azurepowershell
    Example 1:
    OBJECTIVE: Enhance the onboarding strategy.
    KEY RESULT: Implement a new program to increase the repeat rate of 1st-time bookers. 
    [Entity: Team(s) - CRM Team & Marketing Team]
    [Owners: CRM Lead & Marketing Lead]
    
    Example 2: 
    OBJECTIVE: Build a world class Engineering org.
    KR/INITIATIVE: Invest in 2 Training & Development sessions + Capstone Projects for all 4 engg. teams this quarter
    [Entity: Engineering Department]
    [Owner: VP-Engineering & All Engineering Managers]
    
    Example 3:
    OKR: Facilitate seamless Annual & Quarterly Goal planning across the org.
    [Entity: Org level]
    [Owners: CEO & VP - Strategy & Operations]
    ```

In the above examples, if not for Viva Goals' flexible shared OKR model, it gets cumbersome to create duplicate and redundant OKRs for every team/individual when they're supposed to be commonly owned, worded, and measured.

### What are the different types of Shared OKRs possible in Viva Goals?

|Shared OKRs |Description  |
|---------|---------|
|OKRs at an Organizational-entity level     |   These OKRs can have Multiple Owners.      |
|OKRs at team-entity level     |    These OKRs can have multiple teams tagged and respective Team administrators/members tagged as owners.     |
|OKRs at individual-entity level    |    These OKRs can have multiple users assigned as owners.     |

A DRI (Directly Responsible Individual) is accountable for ensuring that OKRs are being properly defined, measured, and accomplished. Multiple owner assignments can hamper accountability and encourage lack of discipline. Check whether it's absolutely essential for your OKR process before adopting it.

## When NOT to create shared OKRs?

- For organizational/team/individual-level OKRs, where there is clarity on the exact key result metrics or projects to be owned by respective teams and owners, don't create a single OKR and share it among all; instead, create an objective at the required entity level and create respective single team-level key results owned by a single DRI so that it's deconflicted.

    ```azurepowershell-interactive
    Example:
    
    OBJECTIVE: Skyrocket revenue in 2021!
    [Entity: Org level]
    [Owner: CEO]
    
    KR1: Double the ARR every quarter.
    [Entity: Sales]
    [Owner: VP-Sales] 
    
    KR2: Maintain a 120% Net Revenue Retention Rate.
    [Entity: Customer Success]
    [Owner: VP-CS]
    ```
- For cross-functional teams where all different stakeholders are part of respective mission teams, the objective can be owned by a single team with KRs being worked upon by respective function-related DRIs within the team.

    ```azurepowershell-interactive
    Example:
    
    OBJECTIVE: Provide best-in-class integration experience for customers.
    [Entity: Team - Integrations & Partnerships Mission team]
    [Owner: Mission Team Owner]
    
    KR1: Go above & beyond on 5 Enterprise & 5 SMB platform integrations.
    [Team: Integrations & Partnerships Mission team]
    [Owner: Product lead]
    KR2: Enhance the Integration sync time performance by 3x.
    [Team: Integrations & Partnerships Mission team]
    [Owner: Engineering lead]
    KR3: Partner with the top 3 industry leading HRIS providers.
    [Team: Integrations & Partnerships Mission team]
    [Owner: Marketing/Partnership lead]
    ```

## Enabling the Shared OKRs feature for your organization

OKR administrators can turn on the "Shared OKRs" feature from the **OKR & Projects** tab within the admin settings.

:::image type="content" source="../media/goals/enable-shared-okrs-feature.png" alt-text="Enable Shared OKRs feature":::

In case you disable the feature, multiple teams and owners who had been assigned to OKRs will continue to exist. Once this feature is disabled, users can only add single owners to OKRs and projects.

## How to create shared OKRs for multiple teams?

1. Log in to Viva Goals and select the **+** button on the top panel to create a new OKR.
1. Once you enter the objective/key result and want to share it with another team, select **Team** from the dropdown list under **Type**. 
1. Scroll down or search in the search bar for the team of choice.
1. Select the team and save the objective/key result. You'll start sharing the OKR with that team.

Users can also assign multiple teams to projects by implementing this procedure.

## How to create shared OKRs with multiple users as owners?

1. Log in to Viva Goals and select the **+** button on the top panel to create a new OKR.
1. Once you enter the objective/key result and want to share it with another individual, select **Owners** from dropdown list under **Owners**. Here, you can assign multiple owners for the OKR.
1. Once you select the owner, save the objective/key result. You'll start sharing the OKR with that individual, and the user who has been assigned as the owner will also receive an in-app notification of the assignation.

## Registrations for single and multiple owners

If there is just one owner or multiple owners assigned to an OKR and you would want a user within the organization to check in and update the progress of the OKR, you can use the "check-in responsibility" feature. The check-in owner will be able to check-in on the OKR (manual check-in) and set up a data link on the OKR (to auto-check-in). This user will be receiving the check-in reminders. In the case of multiple owners, this feature will prevent all of the owners from receiving reminders, and only the user set as 'check-in responsible owner' will receive the reminders.

To assign responsibility for check-ins, perform the following steps:

1. Log in to Viva Goals and select the **+** button on the top panel to create a new OKR.
1. Once you enter the objective/key result and want to share it with another individual, select **Owners** from dropdown list under **Owners**. Here, you can assign multiple owners for the OKR.
1. Once you assign an owner, select the user who will be responsible for making check-ins from the **Who is responsible for making check-ins?** drop-down. Once you make the selection, the user will start receiving the check-in reminders.

By default, the owner (the first owner in the case of multiple owners) is set as the person responsible for check-in and users need not explicitly choose, unless necessary.
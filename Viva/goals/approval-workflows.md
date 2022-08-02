---
title: "Approval workflows"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Viva Goals offers the ability to enable a workflow to gain manager approval when setting OKRs."
---

# Approval workflows 

The approval workflow in Viva Goals gives managers the ability to regulate OKR workflows in their organization. There are four stages in the OKR approval workflow:

1. Planning

2. Review

3. Approved

4. Closed

![approval workflows](../media/goals/4/44/a.png)
   
Planning and Review are similar and are used to indicate status. For example, an employee might plan out their OKRs, and tell their manager when their OKRs are ready to be looked at. The manager would then set it to the Review stage.

They would then have a discussion to finalize OKRs before the manager moves the OKR to the Approved stage.

At that point, the OKRs are **locked** and can't be changed by the employee. In order for a manager (also called the approver) to make changes, they need to go back and change the status back to review.

## How to enable the approval workflow

Go to **Admin Tools -> OKRs & Projects -> OKR Workflow -> Enable Approval Workflow -> Save**.

Once this feature is enabled, an additional option becomes available to block changes to OKRs after approval.
   
### Configuring Approval Workflow 

You can configure who can approve OKRs in Viva Goals. 

:::image type="content" source="../media/goals/enable-approval-workflows.png" alt-text="Configuring approval workflow in Viva Goals." lightbox="../media/goals/enable-approval-workflows.png":::

#### Approval of Organization OKRs 

By default, Organization OKRs can be approved by org owners & org admins only. This option cannot be changed. 

#### Approval of Team OKRs 

By default, Team OKRs can be approved by managers of team owners. Apart from them, you can also enable team owners and team admins to approve the team OKRs. 

#### Approval of Individual OKRs 

By default, Individual OKRs can be approved by managers of individuals only. This option cannot be changed. 

## How to change workflow statuses for an OKR 
  
1. Once the Approval Workflow feature is enabled, navigate to the entity for which you'd like to change the workflow status.
  
2. On the top-right corner of your screen, select the **...** button to view all possible actions for the current entity.

3. Select **Change Status**.
    
4. From the pop-up, select the status drop-down.
   
5. Select the status you'd like to set.
 
6. Select **Save**.
  
## Permissions available for each workflow stage

This setting allows for more regulation, although there is more effort on the part of the objective owner and the managers. Admins should consider this before enabling the feature.

It is not advisable to enable this setting while you are in the middle of an OKR period.

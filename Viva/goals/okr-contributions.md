---
title: "OKR Contributions"
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
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to use OKR Contribution in Viva Goals."
---

# OKR Contributions

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)
  
Viva Goals’ OKR Contribution feature allows users (OKR owners and creators) more flexibility and customizability in specifying how much weight each Objective, Key Result, and Project has in moving towards a goal. This helps with tracking progress and understanding which OKRs and Projects to prioritize first. 
  
Users will now be able to define and control contribution at the parent level. All the contributions add up to a total of 100% and objective owners and creators have an option to mark a child’s contribution as fixed. This is available only for OKRs that have progress mode as "Updated via roll-up from key results". 

**Any Viva Goals user who has edit permissions for an OKR (including check-in owners) can edit the contributions of children OKRs.**

## How to manage OKR Contributions
  
1. You can set or edit your OKRs’ contribution from the “More actions” dropdown by selecting the "Manage contributions" option. 

> [!NOTE] 
> You can also open the "Manage contributions" modal from the objective quick view and detail view.

2. This opens up the “Manage contributions” dialog box, where you can add or edit contributions of the children OKRs and Projects

You can enable or disable the “Newly aligned items should start contributing by default” toggle. By enabling this, you will allow a newly created child OKR or Project to contribute to the parent. This will readjust the contributions you’d have assigned to each child OKR or Project.  
  
> [!Note]
> The “New children should start contributing by default” will be enabled by default. 

3. Once you edit the contributions, click on “Save” to save all the changes.  

## Key considerations for OKR Contributions

1. OKR contribution is available only for OKRs that have progress mode as "Updated via roll-up from key results"

2. All contributions will add up to a total of 100%. The default contribution is automatically assigned to children equally. For example, if an objective has three key results (children), the default contribution assigned to each child will be 33.33%. 

3. As soon as a child’s contribution is edited, the contribution is considered “fixed”. This means that if a new child gets added or if an existing child gets removed, the contributions marked as Fixed will not be adjusted. For example, if an objective has three key results (children), and the contribution of the first key result is edited as 50%, the contributions of second and third key result will be automatically adjusted to 25% each. In the future, if there is a fourth key result that gets added, only the contribution of the second and third key result will be adjusted. 

You can reset all the custom contributions to default by clicking the “Reset to default” option. 

---
title: Deployment and administrator setup for Microsoft 365 Copilot in Viva Glint (preview)
description: Viva Glint administrators grant user permissions for Microsoft 365 Copilot in Viva Glint.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/12/2024
---

# Deployment and administrator setup for Microsoft 365 Copilot in Viva Glint (preview)

> [!NOTE]
> This feature is available to preview customers only, beginning June 29, 2024. Features described here are subject to change.

## Viva Glint Administrators assign Microsoft 365 Copilot in Viva Glint permissions

There are two levels of controls:
- The MAC Viva Feature Access Management (VFAM) control 
- The Glint program level control

>[!IMPORTANT]
>The MAC control always supersedes the Glint program control.

In some cases, when Microsoft 365 Copilot is disabled in MAC,  the Copilot in Viva Glint control is hidden. There are scenarios when it is not. 
This table explains the scenarios: 

|Scenario|Tenant policy|User/VFAM policy|Group policy|Feature toggle visibility|User Role feature toggle status|Feature functionality|User A| User B|User C| User D|
|----|------|-----|-----|------|----|----|----|----|----|----|
|1|Enabled (no action taken)|None created|Copilot enabled for all users|Visible |Enabled|Copilot available for users enabled by Viva Glint Admin|Disabled|Disabled|Enabled|Enabled|
|2|Disabled|None created|Copilot not enabled for any users.<br><br> Copilot disabled for all users in tenant|Not visible|Disabled|Copilot not available for any users|Disabled|Disabled|Disabled|Disabled|
|3|Disabled|Certain users/groups enabled|Copilot enabled only for certain users|Visible|Enabled|Copilot available for users enabled at VFAM level and enabled at Viva Glint Admin level|Disabled|Disabled|Enabled|Enabled|
|4|Enabled(no action taken)|Certain users/groups enabled|Copilot disabled only for certain users|Visible|Enabled|Copilot available for users enabled at VFAM level and enabled at Viva Glint Admin level|Disabled|Disabled|Disabled|Enabled|

**View these diagrams to support your understanding of the table.**

:::image type="content" source="../media/glint/setup/scenario-1-2.png" alt-text="Screenshot that shows scenarios 1 and 2 for Tenant Policy.":::

:::image type="content" source="../media/glint/setup/scenario-3-4.png" alt-text="Screenshot that shows scenarios 3 and 4 for Tenant Policy.":::

## Deployment considerations

Think about:
- **Current usage** – does your rollout group have experience with Viva Glint?
- **Comment count** – do you expect a high number of comments?
- **Survey timing** – can you align with an upcoming survey? 
- **Comfort with AI** – can you engage superusers to help others with the rollout?
- **Amount of change** – is your organization already going through change? Is this time right to add a new tool?

## Microsoft 365 Copilot in Viva Glint can be used across roles

Use Microsoft 365nCopilot in Viva Glint for admins, HR leaders, org leaders, and managers.
<br>
- **Admins and HR** can use Copilot in Viva Glint to summarize large sets of data, allowing this group to quickly find key insights and support ad-hoc requests from stakeholders.
- **Org leaders** can use Copilot in Viva Glint to summarize comments for their teams. They can uncover similarities and unique needs based on comments people are leaving using prompts and filters for different populations across their org.
- **Managers** can use Copilot in Viva Glint to get access to comment summarization services. Managers can quickly uncover comments bundled by common subject matter or theme, identifying areas to explore deeper in their ACT conversations.

> [!NOTE]
> Copilot in Viva Glint defaults to **Off** for all User Roles, including company owners. Every user who should have Copilot enabled needs to be placed into a User Role category with that permission. Copilot in Viva Glint can be activated for any number of user subsets designated.

## Choose a method to roll out Copilot in Viva Glint

Copilot in Viva Glint gives you the flexibility to roll out to one or many user roles. Consider what approach is right for your organization. 

||Admin Release|	Selective deployment|	Full deployment|
|-----------|----------|------------|-----|
|**Users**|	Viva Glint admins only|Select group of users|	All User Roles|
|**Details**|This setting is the default setting for Copilot in Viva Glint.<br><br>You may decide that for the first deployment you don’t want to provide access beyond this group. This option is a way to test and better understand the functionality.<br> <br> As a testing method, admins can use the Copilot in Viva Glint functionality for previously closed surveys.|You may decide to deploy to a group beyond admins but not to your entire eligible population. <br><br> Consider which groups (User Roles) can benefit from the feature. Prioritize those with large sets of comments.|You may decide to deploy to a group beyond admins but not to your entire eligible population. <br><br> Consider which groups (User Roles) can benefit from the feature. Prioritize those survey items with large sets of comments.|













## More Resources

[**Learn how managers can use Copilot in Viva Glint**](https://go.microsoft.com/fwlink/?linkid=2274072)<br>
[**Find answers to technical FAQs**](https://go.microsoft.com/fwlink/?linkid=2274071)<br>
[**Copilot for Microsoft 365**](https://adoption.microsoft.com/copilot/)


---
ms.date: 02/28/2024
title: Use your Microsoft 365 groups as teams in Viva Goals
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn how to use your Microsoft 365 groups as teams in Viva Goals."
---

# Use your Microsoft 365 groups as teams in Viva Goals

Before you can use your Microsoft 365 groups as teams in Viva Goals, you need permission to create teams within your organization. By default, all members in an org can create teams unless the org owner has restricted team creation to specific members.

## Create a Viva Goals team from one of your Microsoft 365 groups

There are two ways to create teams from your groups in Viva Goals:

### Use the left nav

If you already own a Microsoft 365 group or Microsoft Teams team, you'll find that group under *Create team from groups* in the left nav in Viva Goals. Select the group, then select **Confirm** in the resulting dialog.

![Screenshot that shows a view of a Viva Goals user's OKRs tab, including the Create team from groups section in the left nav.](..\media\goals\viva-goals-teams\m365-team-creation.png)

![Screenshot that shows the Creating team from Microsoft 365 group dialog, with the More information dropdown opened.](..\media\goals\viva-goals-teams\more-information.png)

If you want to make it so that only members of the team can see the team's OKRs, select **More information** from the confirmation screen and set the **Members in this organization can view OKRs and related content** toggle to off.

Because the Viva Goals team is created from the Microsoft 365 group, all members and owners of that group will become part of the Viva Goals team.

### Use All Teams or Admin

1. If you don't want to use the left nav, you can go to **All Teams** > **Create a new team** or **Admin** > **Teams** > **Add Team**.

1. A dialog box will appear with two options:

    - **Use an existing Microsoft 365 group** - This will create a Microsoft 365 group-connected team, which is probably what you want if you're reading this article.

    - **Create a team from scratch** - This will *not* create a Microsoft 365 group-connected team: instead, you'll be creating a new Viva Goals team from scratch.

        ![Screenshot that shows the New team dialog and its two options: Use an existing Microsoft 365 group and Start from scratch](..\media\goals\viva-goals-teams\new-team.png)

1. Assuming you chose **Use an existing Microsoft 365 group**, a new dialog will appear. Choose which of the Microsoft 365 groups you own you want to use to create a new Viva Goals team.

    ![Screenshot that shows the What group do you want to use? dialog, with the More settings dropdown expanded.](..\media\goals\viva-goals-teams\what-group-do-you-want-to-use.png)

1. Under **More settings**, you'll find three additional settings: **Privacy**, **Parent team**, and **Visibility toggle**.

    - **Privacy** - This privacy setting uses the same values as the Microsoft 365 group you based the team on, so you can't change them here.

    - **Parent team** - If your team is a division, department, or subteam of another team, you can select that team as your parent team here. Once you select a parent team, your team will use the parent team's OKR settings (such as check-in frequency and OKR creation permissions) as its defaults. Your team will also appear as a subteam underneath your parent team in the navigation.

    - **Visibility toggle** - If you want all members of your Viva Goals organization to be able to view your team's OKRs and related content, this toggle should be set to on: otherwise, set it to off. By default, the toggle is on.

---
ms.date: 02/28/2024
title: Delete, archive, or restore a Microsoft 365 group-connected team
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
description: "Learn how to delete, archive, or restore a Microsoft 365 group-connected team in Viva Goals."
---

# Delete, archive, or restore a Microsoft 365 group-connected team

When a team is dissolved or retired due to an organizational change, org owners and team owners have two options in Viva Goals: delete the team or archive the team.

## Delete a team

Microsoft 365 group-connected teams can't be deleted from within Viva Goals. However, the associated Microsoft 365 group can be deleted in its own service, whether that service is Microsoft Teams, the Microsoft Azure portal, or something else.

If the connected group is deleted, the Viva Goals team connected to that group will be archived. If the group is restored within the [soft-delete period](/microsoft-365/admin/create-groups/restore-deleted-group), the Viva Goals team is automatically reactivated. If the group is permanently deleted, org owners and team owners won't be able to restore the team, but they'll be able to delete the archived team so long as it doesn't contain any OKRs.

## Archive a team

In general, it's better to archive teams that are no longer in service so that the collection of teams remains relevant for use. Once a team has been archived, you'll no longer be able to create OKRs and initiatives for that team, and no user will be considered a part of that team. Furthermore, any subteams will become independent teams in Viva Goals. OKRs previously assigned to the archived team will still be accessible: that is, you'll still be able to perform actions on them, such as check-ins.

Even though you won't be able to see the archived team on the All Teams page now, you'll be able to see the assigned OKRs by expanding the parent OKRs they're aligned to. You can also view those OKRs and initiatives in the Explorer by applying the **Type** filter and selecting the archived team's name.

Any activities related to the archive team will be halted, including the assigning of new team members and any team-level notifications. These activities won't resume unless the team is restored.

To archive a team as an org owner or administrator, go to **Admin** > **Teams** > **Actions** and select **Archive** for the team you want to archive.

To archive a team as an org or team owner or administrator, go to the team's Goals page, select the three dots in the upper right, and choose **Archive this team**.

![Screenshot that shows the Goals page, with the three dots menu expanded and the Archive this team option highlighted.](..\media\goals\viva-goals-teams\archive-this-team.png)

Once a team has been archived, it is marked as **Archived** on the **Teams** tab in the admin console and won't be visible anywhere else. Any objectives previously owned by the team will remain unchanged, but you won't be able to assign new objectives to the team.

## Restore an archived team

Archiving a team isn't permanent. To restore an archived team, go to **Admin** > **Teams** > **Actions** and select **Restore** for the team you want to restore. Alternatively, you can visit the team's OKRs page, select the three dots in the upper right, and choose **Restore this team**.

## End of lifecycle options

If the connected group is deleted, the Viva Goals team connected to the group will be archived. The OKR owner will still have access to the OKRs. For each OKR, the OKR owner can assign it to another Viva Goals team or leave it unassigned.

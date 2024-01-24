---
ms.date: 01/23/2024
title: Delete, archive, or restore a Microsoft 365 group-connected team
ms.reviewer: 
ms.author: v-nstockwell
author: DefinitelyNotNitza
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
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

Microsoft 365 group-connected teams cannot be deleted from within Viva Goals. However, the associated Microsoft 365 group can be deleted in its own service, whether that service is Microsoft Teams, the Microsoft Azure portal, or something else.

If the connected group is deleted, the Viva Goals team connected to that group will be archived. If the group is restored within the [soft-delete period](..\..\admin\create-groups\restore-deleted-group.md), <!--Editor's Note: Check to ensure that link actually works.-->the Viva Goals team will be automatically reactivated. If the group is permanently deleted, org owners and team owners won't be able to restore the team, but they will be able to delete the archived team so long as it does not contain any OKRs.

## Archive a team

In general, it's better to archive teams that are no longer in service so that the collection of teams remains relevant for use. Once a team has been archived, you will no longer be able to create OKRs and initiatives for that team, and no user will be considered a part of that team. Furthermore, any sub-teams will become independent teams in Viva Goals. OKRs previously assigned to the archived team will still be accessible: that is, you will still be able to perform actions on them, such as check-ins.

Even though you won't be able to see the archived team on the All Teams page. <!--Editor's Note: I'd like clarification on "All Teams" vs "Teams" tab. Are they the same? If so, which is correct? Let's make sure we're using the correct terminology here. Claririfcation: "All Teams" is a page. "Teams" is a tab.-->now, you will be able to see the assigned OKRs by expanding the parent OKRs they're aligned to. you can also view those OKRs and initiatives in the Explorer by applying the **Type** filter and selecting the archived team's name.

Any activities related to the archive team will be halted, including the assigning of new team members and any team-level notifications. These activities will not resume unless the team is restored.

To archive a team as an org owner or administrator, go to **Admin** > **Teams** > **Actions** and select **Archive** for the team you want to archive.

To archive a team as an org or team owner or administrator, go to the team's Goals page, select the three dots in the upper right, and choose **Archive this team**.

![Screenshot that shows the Goals page, with the three dots menu expanded and the Archive this team option highlighted.](..\media\goals\viva-goals-teams\archive-this-team.png)

Once a team has been archived, it will be marked as **Archived** on the **Teams** tab in the admin console and won't be visible anywhere else. Any objectives previously owned by the team will remain unchanged, but you won't be able to assign new objectives to the team.

## Restore an archived team

Archiving a team isn't permanent. To restore an archived team, go to **Admin** > **Teams** > **Actions** and select **Restore** for the team you want to restore. Alternatively, you can visit the team's OKRs page, select the three dots in the upper right, and choose **Restore this team**. <!--Editor's Note: Again, see above: we have 'Team OKRs page,' 'team's OKR page,' and now 'team OKRs page'. I need to know what the differences between these are, if any. Clarification: There are no differences. There the same thing.-->

## End of lifecycle options

If the connected group is deleted, the Viva Goals team connected to the group will be archived. The OKR owner will still have access to the OKRs. For each OKR, the OKR owner can assign it to another Viva Goals team or leave it unassigned.

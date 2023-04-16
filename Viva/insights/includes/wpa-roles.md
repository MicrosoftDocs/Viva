---

ms.date: 05/08/2018
title: Viva Insights roles
description: (include file) Viva Insights roles 
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
---

The following roles are assigned by your admin as described in [Assign user roles](/viva/insights/setup/assign-user-roles?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json):

* **Insights Administrator** &ndash; Has access to **Data sources**, **Upload** pages within Data sources, and **Analyst settings**. The [Insights Administrator](/azure/active-directory/roles/permissions-reference#insights-administrator) and the legacy Workplace Analytics admin are interchangeable roles. The admin is responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data for Viva Insights.

  >[!NOTE]
  >Insights Administrators are not Microsoft 365 admins. Unless they are *also* assigned the role of Microsoft 365 admin, they only have access to organizational data, not to Microsoft 365 data.

* **Insights Business Leader**- [Insights Business leaders](/azure/active-directory/roles/permissions-reference#insights-business-leader) can see organizational insights on the [My organization](../org-team-insights/org-insights.md) page within the Viva Insights app.

* **People Manager** &ndash; People managers are assigned access by the Viva Insights admin. Managers can see their team's [organization trends](../org-team-insights/org-insights.md) within the Viva Insights app.

* **Analyst** &ndash; Has full access to all service features except **Upload** and some **Analyst settings** that are only available to admins. An Analyst has the most complete access to data, including the ability to launch, manage, and track **Plans** in the advanced insights app.

* **Analyst (Limited Access)** &ndash; Has the same access as people who have the **Analyst** role but with the following restrictions:

  * No access to **Query designer**.
  * _Read-only_ access to **Analyst settings** where the [meeting and attendee exclusion rules](/viva/insights/tutorials/exclusions-introduction?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) are defined.

* **Program Manager** &ndash; Has access to organizational data for Viva Insights within the advanced insights app. A Program Manager can also open, manage, and track **Plans** in the advanced insights app.


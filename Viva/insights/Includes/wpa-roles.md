---

title: Workplace Analytics roles
description: (include file) Workplace Analytics roles 
author: paul9955
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
ms.prod: wpa
---

The following roles must be assigned by a Microsoft 365 admin as described in [Assign user roles](../setup/assign-user-roles.md):

* **Analyst** &ndash; Has full access to all service features except **Upload** and **Admin settings**, which are only available to admins. An Analyst has the most complete access to data, including the ability to launch, manage, and track **Plans** in Workplace Analytics.

* **Analyst (Limited Access)** &ndash; Has the same access as people who have the **Analyst** role but with the following restrictions:

  * No access to **Query designer**.
  * _Read-only_ access to **Analyst settings** where the [meeting and attendee exclusion rules](../tutorials/exclusions-introduction.md) are defined.

* **Administrator** &ndash; Has access to **Data sources**, **Upload**, and **Admin settings**. A Workplace Analytics admin is responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data.

  >[!NOTE]
  >Workplace Analytics admins are not Microsoft 365 admins. Therefore, unless they are *also* assigned the role of Microsoft 365 admin, they only have access to organizational data, not to Microsoft 365 data.

* **Program Manager** &ndash; Has access to organizational **Insights** in Workplace Analytics. A Program Manager can also open, manage, and track **Plans** in Workplace Analytics.

The following role must be assigned by a Workplace Analytics admin in **Admin settings** > [**Manager settings**](../use/manager-settings.md) in Workplace Analytics:

* **People Manager** &ndash; Has access to **Insights** only about their team. A People Manager can also open, manage, and track **Plans** only for their team in Workplace Analytics.

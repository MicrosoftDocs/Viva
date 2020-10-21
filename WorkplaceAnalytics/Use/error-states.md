---
ROBOTS: NOINDEX,NOFOLLOW
title: Error states in Workplace Analytics
description: Describes the different error states that might be encountered when viewing Workplace Analytics insights
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Error state reference
Access, connectivity, or other issues can cause pages to not appear or to appear but showing incomplete data. This article describes various possibilities and, where possible, gives solutions.

## Permissions errors
| Error message &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| Why is this happening? | Recommended actions  |
| --- | --- | --- | 
| **You don’t have access yet** <p>Contact your IT admin for access to Microsoft 365 Insights. | This error takes place if you do not have the right role assigned for viewing the Workplace Analytics experience. Roles are assigned by the Workplace Analytics admin. <br> <br>For more information, see [Assign roles](https://docs.microsoft.com/en-us/workplace-analytics/setup/assign-roles-to-wpa-admins.md). | There is an easy fix for this problem: Reach out to your to your Workplace Analytics admin and request to be assigned the role of _limited analyst_. <br><br> To find out who has admin permissions in your organization, see [Admin center overview / Who has admin permissions?](https://docs.microsoft.com/microsoft-365/admin/admin-overview/admin-overview?view=o365-worldwide#who-has-admin-permissions-in-my-business) | 

## Errors in insight generation
| Error message &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Why is this happening? &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Recommended actions  |
| --- | --- | --- | 
| **Insight unavailable** <p>This insight isn’t available because of a technical issue. Please try again later. <br><p> or <br><p> **Something went wrong.** <p>Please try again later. | These errors appear when something goes wrong in the system that generates the insights. | The Workplace Analytics team is notified about such errors automatically, but if they persist, please report them using the feedback system. You can submit feedback by selecting the smiley face icon (at the top), entering your question or feedback, and then selecting **Send**. <br><br> For more about support, see [Get support for Workplace Analytics](../overview/getting-support.md). | 

## Data-access errors
| Error message &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| Why is this happening? | Recommended actions  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |
| --- | --- | --- | 
| This insight is unavailable because the required minimum number of employees is not met | This error takes place if certain privacy thresholds are not being met. For example, if the number of measured employees falls below the minimum number of required employees as configured by your Workplace Analytics admin, this error appears. | Contact your Office 365 admin to discuss one or both of the following remedies:<ul><li>License more employees so that your organization has enough employees to power the insight.</li><li>Update the minimum group size.</li></ul> <br><br> Minimum group size used to protect privacy. For more about privacy protections, see [Privacy and data access / You decide](../privacy/privacy-and-data-access.md?branch=pas-am-error-codes#you-decide-who-gets-to-see-what-data) and [Workplace Analytics settings / Minimum group size](settings.md?branch=pas-am-error-codes#minimum-group-size). |
		
## Related topic

[Business outcomes overview](insights.md)
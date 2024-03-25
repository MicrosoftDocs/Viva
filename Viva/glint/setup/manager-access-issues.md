---
title: Address Viva Glint access issues as a manager
description: Use this guidance to determine how to address access issues in Viva Glint as a manager. 
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: access, error, connection error, maintenance, insufficient results
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/25/2024
---

# Address Viva Glint access issues as a manager
Microsoft Viva Glint survey programs allow your organization to collect data and listen to feedback about how happy employees are at work. As a manager, you may occasionally encounter unexpected connection or maintenance messages when trying to view results for your team. Use this guidance to determine how to address access issues.

## Access Viva Glint
To access your Viva Glint dashboard, use one of the following links to log in based on the region that your organization sits in.
 
- US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
- EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)

## Phased and Live survey access
During a live Viva Glint survey, your Glint admin team often gives managers access to past survey results only. Live survey results access is usually restricted to admins and HR only. [Learn more](live-versus-phased-access.md).

## Monthly maintenance
To strive for consistent improvement, Viva Glint undergoes [monthly maintenance](monthly-release-dates.md) to release new features, enhancements, and fixes. If when attempting to access your results, you’re presented with a maintenance message, revisit your dashboard the following day.

## No Viva Glint access
If you’re presented with a message stating that you don’t have access, your organization hasn’t granted you access to the Viva Glint application. Reach out to your Glint admin to confirm if you should be granted access to Viva Glint.

:::image type="content" source="../../media/glint/setup/glint-mgr-no-access.png" alt-text="Screenshot of access error in Viva Glint.":::

## No User Role assigned
If you see a **Welcome to Viva Glint** message but don’t have access to any results, you haven’t been assigned a User Role to access reports in Viva Glint. Reach out to your Glint admin to confirm and have your User Role membership updated if needed.

:::image type="content" source="../../media/glint/setup/glint-mgr-no-role.png" alt-text="Screenshot of a Viva Glint dashboard for a user with no role assigned.":::

## No results access
If you see a message in your dashboard that indicates that there aren’t enough respondents to see results, it can mean that:

- There aren’t enough respondents to view results (usually at least 5 respondents are required to protect [confidentiality](quick-guide-confidentiality.md)).
  - Select the **View Guide for Smaller Teams** link to view guidance on small team results.
  - If your organization uses Broader Team Insights, view a summary of your manager’s team results.
- You haven’t been granted access to a segment of data to view results. Contact your Glint admin to confirm if your data access needs to be updated.

:::image type="content" source="../../media/glint/setup/glint-mgr-no-results.png" alt-text="Screenshot of a Viva Glint dashboard for a user with insufficient results.":::

## Incorrect team information
If recent team changes don’t appear in your Viva Glint dashboard, it may mean that the HR data in place before a survey launched wasn’t up to date. For example, if some team members have left and others joined your team and this isn’t shown in your dashboard, contact your Glint admin to confirm whether they can process an update to your results data.

## Connection issue
If you see a message indicating that a connection can’t be made to the Glint service, there is likely an issue with matching your information between the Viva Glint application and Microsoft Entra ID. Contact your Glint or Entra admin to confirm that your data matches between systems.

:::image type="content" source="../../media/glint/setup/glint-mgr-no-connection.png" alt-text="Screenshot of a Viva Glint error message for a connection issue.":::

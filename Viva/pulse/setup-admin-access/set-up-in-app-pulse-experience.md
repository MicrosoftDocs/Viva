---
title: Set up the in-app Viva Pulse experience
description: "Set up the in-app Viva Pulse experience"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 03/08/2023
ms.topic: article
ms.service: viva
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
ROBOTS: NOINDEX, NOFOLLOW
---

# Set up the in-app Viva Pulse experience

> [!NOTE]
> This article applies to a preview version of Microsoft Viva Pulse. You must be in the Private Preview program to access it. Features are subject to change.

The Viva Pulse in-app experience can be configured by users with both the Viva Pulse Admin role and the Global Admin role. To manage configurations for Viva Pulse in-app, the user must have the Global Microsoft 365 Administrator role or Viva Pulse Admin role.

## Privacy & Confidentiality

As an Admin, you can set the privacy and confidentiality for your organization. All Pulse surveys require at least five responses for authors to see unattributed feedback to respect employee confidentiality. You can increase this minimum requirement  to a maximum of 25 responses, and doing so will not affect any currently deployed pulses.

Furthermore, you can control privacy for your organization’s level of privacy. As Admin, you can choose to turn off the collection of user diagnostic data to Microsoft.

## Customization

Customization is turned on by default, but as an Admin, you can control whether feedback authors can add their own questions to existing stock templates or turn off this setting.

## Delete User Data

As an Admin, you can also delete a user’s past pulse requests and responses on the user’s behalf. Deletion of a user’s data is a hard deletion, and no record of the user’s data will remain. You can only delete one user’s data at a time, and there is no limit as to how many times a user’s data can be deleted.

## Diagnostic Data

There are two types of data that we collect: Required Diagnostic Data (RDD) and Optional Diagnostic Data (ODD). By default, ODD and RDD will be enabled. As an Admin, you can go into the Admin Center in the Viva Pulse app and de-enable the collection of diagnostic data. Once collection of diagnostic data has been de-enabled, previously collected data for the tenant will still be available, but additional data will no longer continued to be collected.

* Required Diagnostic Data (RDD): Telemetry collected to help us make product improvements and provide enhanced information to help us detect, diagnose, and remediate issues.
* Optional Diagnostic Data (ODD): Telemetry gathered to ensure the customers are secure, up to date, and performing as expected.

## Minimum Response Required to See Feedback Default Value

All Pulse surveys require at least five responses for authors to see unattributed feedback. As an Admin, you can increase this minimum requirement to a maximum of 25 responses. Changing this value will not affect any Pulses that were previously sent or are currently being circulated.

---
ROBOTS: NOINDEX,FOLLOW
title: De-identification of personal data in Viva Insights 
description: De-identification of personal data in Microsoft Viva Insights
author: madehmer
ms.author: helayne
ms.topic: conceptual
ms.localizationpriority: medium 
ms.collection: 
- viva-insights-personal
- viva-insights-advanced
- viva-insights-leader
- viva-insights-manager
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# De-identification of personal data

To keep from disclosing personal data, Microsoft Viva Insights de-identifies an individual's data through the use of pseudonymization and other techniques, such as aggregation.

The following [illustrative example](#illustrative-example) describes how Viva Insights secures information in query results. For more examples of how various types of data are de-identified, see **Examples** in [Types of data for analysis](data-protection-considerations.md#types-of-data-used-in-analysis).

See the [Glossary](../use/glossary.md) for definitions of the terms related to privacy, such as: aggregation, anonymization, de-identification, hashing, and personal data.

>[!Note]
>To balance the requirements of protecting individual privacy and providing useful information, Viva Insights is gradually incorporating a nuanced approach known as [differential privacy](differential-privacy.md).

## Illustrative example

With Viva Insights, all metrics that are computed from Microsoft 365 collaboration data and from the organizational data that you choose to include are de-identified and aggregated data. The following example shows one line from a “people” report that Viva Insights created:

| Person Identifier | After Hours | Email Hours | Function | Title | Org | Region |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| T5Y07H4VfKWcCC3 | 7 | 6 | HR | Director | HR – Corp | Central |

In this example, Viva Insights computes After Hours and Email Hours for some individual, and reports on this information, associating it with the person’s attributes that you choose to include. The computed information is de-identified; that is, you cannot identify the individual from these fields. The Person Identifier is pseudonymized with a cryptographically generated identifier derived from the person’s Microsoft 365 email address. The other attributes (such as function, title, organization, and region) are effectively personal data. While it might not be possible to identify the user with any single attribute, together these attributes might enable you to identify the user whose metrics have been computed. Therefore, this group of attributes is considered personal data.

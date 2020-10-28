---

title: De-identification of personal data in Workplace Analytics 
description: De-identification of personal data in Workplace Analytics
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# De-identification of personal data

To keep from disclosing personal data, Workplace Analytics de-identifies an individual's data through the use of pseudonymization and other techniques, such as aggregation.

For examples of how it does this for various types of data, see the Examples column in the table in [Types of data for analysis](data-protection-considerations.md#types-of-data-for-analysis-in-workplace-analytics). 

The following [illustrative example](#illustrative-example) describes how Workplace Analytics secures information in query results.

Finally, see the [Glossary](../use/glossary.md) for definitions of the terms related to privacy, such as: aggregation, anonymization, de-identification, hashing, and personal data.

> [!Note]
> To balance the requirements of protecting individual privacy and providing useful information, Workplace Analytics is gradually incorporating a nuanced approach known as [differential privacy](differential-privacy.md).

## Illustrative example

With Workplace Analytics, all metrics that are computed from Office 365 collaboration data and from the organizational data that you choose to include are anonymized and aggregated data. The following example shows one line from a “people” report that Workplace Analytics created:

| Person Identifier | After Hours | Email Hours | Function | Title | Org | Region |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| T5Y07H4VfKWcCC3 | 7 | 6 | HR | Director | HR – Corp | Central |

In this example, Workplace Analytics computes After Hours and Email Hours for some individual, and reports on this information, associating it with the person’s attributes that you choose to include. The computed information is anonymized; that is, you cannot identify the individual from these fields. The Person Identifier is pseudonymized with a cryptographically generated identifier derived from the person’s Office 365 email address. The other attributes (Function, Title, Org, and Region) are effectively personal data. While it might not be possible to identify the user with any single attribute, together these attributes might enable you to identify the user whose metrics have been computed. Therefore, you should treat these attributes as personal data.

---
title: Understand GDPR and special categories of data collection
description: Learn about GDPR and the special categories of data collection here.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: confidentiality, personal data, data privacy, privacy, trust, sensitive data
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/10/2023
---

# Understand GDPR and special categories of data collection

At Microsoft Viva Glint, data privacy and trust are key priorities. Strict adherence to protecting the confidentiality of your people encourages elevated levels of survey participation with honest and useful feedback. Our products are [General Data Protection Regulation (GDPR) compliant](https://www.microsoft.com/professionalservices/gdpr)

## What is GDPR?

GDPR is a set of rules designed to give EU citizens control over their personal data. It aims to simplify the regulatory environment for business and applies in every EU member state. Viva Glint takes a global approach to privacy and data protection, applying GDPR as its standard for data privacy compliance around the world. 

In Viva Glint’s role as data processor, we support our customers, who are the controllers for their data being processed, and the individual right to privacy of each of their employees. [Read about the rights of the data subject in GDPR](https://www.microsoft.com/professionalservices/gdpr).

## Personal data is separated from survey results

Survey responses are stored within database tables, which are separate from the user table, where employee attributes are stored. Each table contains a unique identifier. The unique identifier stored with responses isn't the *external* user ID provided by the customer but is an *internal* user ID created randomly by the system. This randomly generated unique identifier enables Viva Glint’s technology to analyze survey responses against the attributes provided by the customer. The randomly assigned identifier in the survey results table is associated by the system with a customer-assigned external user ID stored in the separate user table. The association between the internal and external user IDs aren't visible to customers.
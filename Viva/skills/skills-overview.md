---
title: Overview of Skills in Viva 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 11/29/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: medium
description: An introduction to Skills in Viva, 
---

# Overview of Skills in Viva 

 Skills in Viva is an AI-powered service in the Microsoft Viva Suite that delivers personalized skills-based experiences throughout supported Microsoft 365 and Viva applications for employees, business leaders, and HR. 

It uses data from the [Microsoft Graph](/graph/overview) and skills from the [LinkedIn Skills Graph](https://engineering.linkedin.com/blog/2022/building-linkedin-s-skills-graph-to-power-a-skills-first-world) to predict a user’s skills and offer tailored skill suggestions, while providing you with a better understanding of your organization’s current workforce skills distribution. Learn more about [Skills in Viva](https://techcommunity.microsoft.com/t5/microsoft-viva-blog/introducing-ai-powered-skills-in-microsoft-viva-a-new-way-to/ba-p/3947844). 



Future releases plan to include other signals, like expertise in Viva Topics and data from human capital management systems. 

If you’d like to learn more or apply for the Skills in Viva preview, contact your Microsoft representative. 

## Prerequisites 

To help ensure a productive private preview that enables Skills in Viva to meet and exceed your company's goals, the following are the requirements for private preview participation: 

1. Private preview must be deployed on a production tenant where users are spending at least 80% of their time on emails, documents, and other Microsoft 365 and Viva applications. 

2. More than 100 end users who are licensed for either Viva Suite or Viva Learning.  

3. End users included in the Skills private preview program have Viva Learning deployed and available for use.

> [!NOTE]
> - Private preview will be available in English language only. Default language for Viva Learning must also be English for this private preview 
> - All users in your tenant will lose “Interests” they have selected in Viva Learning when you enable skills.  This action is not reversible. 


## Admin roles 

The following roles and permissions are required to set up Skills in Viva. Review the documentation for [assigning roles](/entra/identity/role-based-access-control/manage-roles-portal)


| Roles |  Permissions | 
| - | - | 
| Microsoft 365 Global Administrator | Microsoft 365 Global Administrator has global access to most management features and data across Microsoft online services. For Skills in Viva, the Microsoft 365 Global Administrator can configure and manage your organization’s skills library related settings from the Microsoft 365 admin center.| 
| Knowledge Administrator | The Knowledge Administrator needs to be assigned by the Microsoft 365 Global Administrator or the Privileged Role Administrator. The Knowledge Administrator can configure and your organization’s skills library and related settings from the Microsoft 365 admin center. | 

### Next steps

[Set up skills in Viva](skills-get-started.md)

[Manage your skills library](manage-skills-library.md)

---
title: "Overview of security and compliance in Microsoft Viva"
ms.reviewer: 
ms.author: loreenl
author: LoreenLa
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.collection:  
- M365initiative-viva
search.appverid:
- MET150

description: "Learn about security and compliance features for each module in Microsoft Viva"
---
# Overview of Microsoft Viva security and compliance
  
Microsoft Viva benefits from the advanced [security](/microsoft-365/security/microsoft-365-zero-trust) and [compliance](/microsoft-365/compliance/compliance-quick-tasks) capabilities that are [built into Microsoft 365 and Office 365](/microsoft-365/security) as well as specific settings and policies of the apps each module interacts with. For example, Viva Connections uses not only Microsoft 365 security and compliance features, but also the security settings in SharePoint, Teams, and other apps that are used with Viva Connections.

## Viva Topics
Viva Topics uses existing file permissions in Microsoft 365, along with administrative controls, to control what AI-discovered topics are shown to users in your organization. It is the combination of Microsoft 365 security settings and Viva Topics admin settings that determine what a given user can see in topics.

Setting up Viva Topics does not modify any existing access controls on content in your organization. Users will only see what they already have access to.

[Learn more about security and privacy in Microsoft Topics](/viva/topics/topic-experiences-security-privacy)

## Viva Insights

Microsoft Viva Insights produces useful insights about how your organization and employees function. It does this by analyzing Microsoft 365 collaboration data and organizational (HR) data that you provide through an upload or that's presented in Microsoft Azure Active Directory (Azure AD). Because of the potential sensitivity about how data could be used, successful implementation and use of Viva Insights requires planning.

[Learn more about data protection for Viva Insights](/viva/insights/privacy/data-protection-intro)

## Viva Learning
Viva Learning is enabled by default for all Microsoft Teams users in your organization, and, like Teams, it leverages the advanced security and compliance capabilities that are built into Microsoft 365 and Office 365. You can turn off or turn on Viva Learning at the organization level on the Manage apps page in the Microsoft Teams admin center. For more information, see [Manage your apps in the Microsoft Teams admin center](/microsoftteams/manage-apps).

To allow or block specific users in your organization from using Viva Learning, make sure Viva Learning is turned on for your organization on the Manage apps page in the Microsoft Teams admin center. Then create a custom app permission policy and assign it to those users. For more information, see [Manage app permission policies in Teams](/microsoftteams/teams-app-permission-policies).

Viva Learning brings in content from different sources including Microsoft Learn, your organization’s SharePoint sites, LinkedIn Learning, and third-party content providers and learning management systems depending on what you’ve enabled in the Microsoft 365 admin center. Content accessible through Viva Learning is therefore subject to terms other than the Microsoft product terms. [Learn more about Viva Learning content terms and conditions](/viva/learning/terms-and-conditions).

Learn more

[Security guide for Microsoft Teams](/microsoftteams/teams-security-guide)

[Introduction to Microsoft Viva Learning](/viva/learning/)
 
## Viva Connections
Microsoft Viva Connections brings together relevant news, conversations, and resources in one place for your organization. It's built on your current Microsoft 365 ecosystem and is powered by SharePoint. The Viva Connections experience is deployed and accessed in Microsoft Teams desktop and the mobile app. 

Viva Connections uses a combination of existing Microsoft 365 apps and features. Security and permission settings are managed and inherited from the original Microsoft 365 app. There are no specific security settings that need to be managed for Viva Connections. For example, the Viva Connections Dashboard permissions are  governed by the [SharePoint home site](/sharepoint/home-site). Another example is [content in the Feed comes from three main sources](/SharePoint/faqs-viva-connections-feed), one being posts in Yammer. Only users who have permissions to specific Yammer communities will be able to view posts from that Yammer community in the Viva Connections Feed.

## Viva Goals
Microsoft Viva Goals connects employees to your organization’s goals, helps them stay aligned at scale, and drives business results to empower people and teams to understand their impact.

Viva Goals leverages the advanced security and compliance capabilities that are built into Microsoft 365 and Teams.

### Learn more about security for Microsoft Viva

[Settings interactions between Microsoft 365 Groups, Teams and SharePoint](/microsoft-365/solutions/groups-sharepoint-teams-governance)

[Overview of security and compliance in Microsoft Teams](/microsoftteams/security-compliance-overview)

[Managing SharePoint Online Security: A Team Effort](/microsoft-365/community/sharepoint-security-a-team-effort)

[Overview of security and compliance in Yammer](/Yammer/manage-security-and-compliance/security-and-compliance) 


## Related information
[Set up your infrastructure for hybrid work with Microsoft 365](/microsoft-365/solutions/empower-people-to-work-remotely)

[Data residency: Learn about where Microsoft Viva data is stored](/microsoft-365/enterprise/o365-data-locations#what-are-the-considerations-for-microsoft-viva-data-locations)

---
title: "Understand how security works in Microsoft Viva"
ms.reviewer: loreenl
ms.author: elizapo
author: elizapo
manager: pamgreen
ms.date: 4/20/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Find Microsoft Viva security information."
---

# Understand how security works in Microsoft Viva

Microsoft Viva and the Viva apps work with and integrate into Microsoft 365. This means that the Microsoft 365 security capabilities - like role-based access, identity and app management, and others - apply to Microsoft Viva. The Viva apps can also use specific settings and policies of the apps that Viva interacts with. For example, while all users can access Viva Learning in Microsoft Teams by default, you can use app permissions policies in Teams to allow or block access for specific users. 

Before setting up Microsoft Viva, consider the following security recommendations:
 
- Protect data by implementing appropriate access controls and role-based access controls so only authorized users have access to certain data and features. Use Azure AD to handle user authentication and authorization. 
- Provide another layer of security for users by setting up multi-factor authentication (MFA).
- Make sure that you have a plan for incident response to tackle any security breaches that may occur.

> [!NOTE]
> All the scenarios and suggestions provided are general in nature and may vary depending on the type of business and organization. It's important to consult with security experts and conduct your own risk assessments to ensure that you have adequate security measures in place for your specific environment.


## Understand Teams and SharePoint security
Depending on which Viva app you’re using, you may inherit much of your security configuration and options from Teams and SharePoint, which in turn rely on identity management through Microsoft 365 users and groups. Check out [Settings interactions between Microsoft 365 Groups, Teams and SharePoint](/microsoft-365/solutions/groups-sharepoint-teams-governance?view=o365-worldwide) for information about how changes to one area can affect other services. For more information about configuring secure access and collaboration in Microsoft 365, see [Set up secure file and document sharing and collaboration with Teams in Microsoft 365](/microsoft-365/solutions/setup-secure-collaboration-with-teams?view=o365-worldwide).

## Viva apps security options and controls
In addition to the security capabilities available to Microsoft Viva through Microsoft 365, SharePoint, and Teams, each app has its own security controls and considerations.

### Viva Connections
 
Viva Connections integrates your organization's SharePoint intranet into Microsoft Teams, providing employees with relevant news, information, and resources accessible from desktop or mobile devices. 

Security for Viva Connections is largely inherited from Microsoft 365, SharePoint, and Teams.  For example, if you configure Viva Connections to include content from Viva Engage in the Feed, your users only see community content from the Engage communities that they already have access to. 

> [!IMPORTANT] 
> This applies to content and cards sourced from Microsoft apps.

When you’re setting up Viva Connections, be sure to [confirm who has access to certain sites within SharePoint](https://support.microsoft.com/office/share-a-site-958771a8-d041-4eb8-b51c-afea2eae3658) to ensure only authorized users have access to certain data and features.

For more information about Viva Connections, see [Overview of Viva Connections](connections/viva-connections-overview.md).

### Viva Learning
Viva Learning is a centralized learning hub in Microsoft Teams that brings in content from different sources including Microsoft Learn, your organization’s SharePoint sites, LinkedIn Learning, and third-party content providers and learning management systems. Non-Microsoft content that is accessible through Viva Learning is subject to terms other than the Microsoft product terms. Learn more about [Viva Learning content terms and conditions](learning/terms-and-conditions.md). 

Viva Learning is enabled by default for all Microsoft Teams users in your organization. 

You can turn off or turn on Viva Learning at the organization level on the Manage apps page in the Microsoft Teams admin center. For more information, see [Manage your apps in the Microsoft Teams admin center](/microsoftteams/manage-apps). To control whether specific users have access to Viva Learning, create a custom app permission policy and assign it to those users. For more information, see [Manage app permission policies in Teams](/microsoftteams/teams-app-permission-policies).

For more information about Viva Learning, see [Microsoft Viva Learning](/viva/learning/).

### Viva Insights
Microsoft Viva Insights produces useful insights about how your organization and employees function by analyzing Microsoft 365 collaboration data and organizational (HR) data that you provide or that's used in Microsoft Azure Active Directory. 

Because of the potential sensitivity about how data could be used, Viva Insights uses role-based access to control who has access. 

The Personal Insights feature is built on Microsoft Graph, which includes a set of REST-based API calls that enable developers to interact with the Microsoft technologies used by your organization. To use these API calls, developers must have specific permissions to access any data they request. Admins control both the deployment of any Microsoft Graph application and permissions to access these applications. You can’t turn access to Microsoft Graph on or off globally in the Microsoft 365 Admin Center; instead you can achieve the same effect by blocking employees’ ability to install third-party apps or by restricting developer access permissions. For more information, see [Microsoft Graph and Microsoft Graph security API](/graph/security-concept-overview).

For more information about Viva Insights, see [Introducing Viva Insights](insights/introduction.md).

### Viva Topics
Viva Topics uses existing content security features in Microsoft 365, along with administrative controls, to control what AI-generated content is shown to users in your organization. What an individual can see in topics is determined by the combination of [Microsoft 365 security](/microsoft-365/security/?view=o365-worldwide) settings (permissions to sites, files, and folders) and [Topics admin settings](topics/topic-experiences-security-privacy.md).
 
Viva Topics doesn’t modify any existing access controls on content in your organization. Users see only what they already have access to. Admins can also indicate which [SharePoint sites are scanned for information](topics/topic-experiences-discovery.md#select-sharepoint-topic-sources) or [prevent topic viewers from seeing specific topics](topics/topic-experiences-knowledge-rules.md). Admins can access the topic center to see a list of created topics for more granular control. Admins can also [use sensitivity labels to restrict topic and resource discovery](topics/topic-experiences-discovery.md#exclude-resources-based-on-sensitivity-labels).

For more information, see [Security and privacy in Microsoft Viva Topics](topics/topic-experiences-security-privacy.md).

### Viva Engage
Your organization's privacy and security settings from Microsoft Yammer are shared with Viva Engage. Because of this, you need a Viva Engage Enterprise license to set up and ensure Engage is secure and compliant. The admin tools help protect your Engage data and who can access your Engage network, along with controlling access, managing users, providing secure access on mobile devices via Microsoft Intune, [assigning roles](engage/eac-key-admin-roles-permissions.md), and limiting file uploads. The Engage admin can set up and configure Engage for your organization and manage data, network-related settings, and the various core or premium features within the application. To make someone an Engage admin, make them an [Yammer administrators](/microsoft-365/admin/add-users/assign-admin-roles?view=o365-worldwide) in Azure AD.


For more information about security in Viva Engage, see 
[Configure and review privacy and security settings](engage/setup.md#configure-and-review-privacy-and-security-settings).

### Viva Goals
 
Microsoft Viva Goals is a goal-alignment solution that connects teams to your organization’s strategic priorities, unites them around your mission and purpose, and drives business results. This is done by using in-boundary Microsoft 365 integrations (Microsoft Teams, Excel Online, Planner), cross-boundary integrations (Azure Data Explorer, Azure DevOps, Power BI), and third-party API integrations (Salesforce, Slack, Asana) to pull data from multiple sources. Admins of their organizations within Viva Goals can manage which integrations are used and how frequently Viva Goals checks for new data. Each integration has its own set-up and must first be [enabled in order to appear within the organization’s choices for integrations](goals/vg-integrations-administration-overview.md#how-to-manage-integrations). 

Carefully review any terms and relevant documentation for any third party Application Programming Interfaces (APIs) that you plan to integrate with Viva Goals and decide if your users can add these from a curated list or if, instead, they can only use what has been vetted at the admin level. 

For more information about security in Viva Goals, see [Viva Goals security, privacy, and compliance](goals/vg-privacy-and-security.md).

### Viva Sales
Viva Sales is designed to help sellers boost productivity, lighten workloads, save time, and help salespeople sell more. It uses Microsoft 365 and Teams to capture, access, and register data into your organization's existing Customer Relationship Management (CRM) system (Microsoft Dynamics 365, Salesforce, etc.). A Microsoft 365 administrator is needed to deploy and install the Viva Sales add-in for Outlook, and a Teams administrator to install Viva Sales for Teams and pin it as an app.  Learn more about [installing Viva Sales for Outlook](/viva/sales/install-viva-sales-individual-add-in-admin-center#microsoft-outlook), and how to [install Viva Sales for Microsoft Teams](/viva/sales/install-pin-viva-sales-teams). 

There are more role requirements if you're using Microsoft Dynamics 365 as your CRM system, and permission requirements if you're using Salesforce as your CRM system. Learn more about [role requirements for Dynamics 365](/viva/sales/introduction#role-requirements) and [permissions required for Salesforce administrators](/viva/sales/install-viva-sales#permissions-required-for-salesforce-administrators).

To support Viva Sales in Microsoft Outlook, Viva Sales uses Microsoft Graph, which includes a set of REST-based API calls that enable developers to interact with the Microsoft technologies used by your organization. To use these API calls, developers must have specific permissions to access any data they request. Admins control both the deployment of any Microsoft Graph application and permissions to access these applications. You can’t turn access to Microsoft Graph on or off globally in the Microsoft 365 Admin Center; instead you can achieve the same effect by blocking employees’ ability to install third-party apps or by restricting developer access permissions. For more information, see [Microsoft Graph and Microsoft Graph security API](/graph/security-concept-overview).

To learn more about Viva Sales, see [Introduction to Viva Sales](/viva/sales/introduction).
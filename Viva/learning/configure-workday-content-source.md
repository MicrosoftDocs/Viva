---
title: Configure Workday as a content source for Microsoft Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 6/14/2022
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: Learn how to configure Workday as a learning content source for Microsoft Viva Learning.
ROBOTS: NOINDEX
---

# Configure Workday as a content source for Microsoft Viva Learning

> [!IMPORTANT]
> Workday integration is currently only available for private preview customers. The capabilities here are subject to change.

This article shows you how to configure Workday as a third-party content source for Microsoft Viva Learning. First, you'll need to create and set up an integration system user and set up security in Workday. Then you'll need to complete the configuration in the Microsoft 365 admin center.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Workday content and any associated services are subject to the Workday privacy and service terms.

## Configure in Workday

You'll need to complete the following steps in Workday:

1. [Create an integration system user](#create-an-integration-system-user).
2. [Set up integration system user security](#set-up-integration-system-user-security).
3. [Set up course-segmented security](#set-up-course-segmented-security).
4. [Edit domain security policies](#edit-domain-security-policies).
5. [Activate pending security policy changes](#activate-pending-security-policy-changes).
6. [Retrieve the WWS endpoint](#retrieve-the-workday-web-service-endpoint).

If you require more support, contact Workday.

### Create an integration system user

Create an integration system user (ISU) for Microsoft Viva Learning to access your Workday tenant. Assign the ISU to a security group with permission to access Workday Learning Web Services and your learning catalog.

1. Access the **Create Integration System User** task.

    >[!NOTE]
    >Workday automatically sets the value of **Session Timeout Minutes** to zero to prevent the integration system user session from expiring. Expired sessions can cause the integration to stop before it successfully completes.

2. Create a username and password. Workday recommends using **ISU_Microsoft_Viva_Learning** for the username.
    1. Keep the session timeout value at zero to prevent session expiration.
    2. Tick the **Do Not Allow UI Sessions** checkbox to prevent the ISU from signing into Workday through the user interface.

3. Access the **Create Security Group** task and select **Integration System Security Group (Unconstrained)**.

4. Provide a group name. Workday recommends using **ISU_Microsoft_Viva_Learning**.

5. Link your group to the integration system user. This lets Workday assign the integration system user as part of the Microsoft Viva Learning security group.

### Set up integration system user security

You'll need these domains in the Integration and System functional areas:

- Integration Security
- Security Configuration

You'll need to have already [created an integration system user](#create-an-integration-system-user).

1. Access the **Maintain Permissions for Security Group** task to update domain security policies.

2. Add the Domain Security Policy Permission **Get Only** access to the **Manage: Learning Content** domain.

3. Run the **Activate Pending Security Policy Changes** task.

### Set up course-segmented security

You can configure which learning content displays in Viva Learning. You do this by restricting the integration system user's access by using segmented security. You can segment security based on security categories or topics.

>[!NOTE]
>Setting up segmented security is optional.

1. Access the **Create Learning Security Category** task or the **Create Learning Topic** task. Create security segments or topics to restrict access and add these to your learning content. You'll need the **Learning Segment Setup** domain in the System functional area.

2. Select the **Inactive** checkbox if you want to disable permissions for members of the security group. You can't inactivate the security group when you:
    1. Grant the security group permission to the **Security Configuration** domain.
    2. Include the security group as a member of another security group.
    3. Specify the security group as an administrator for another security group.

3. From the **Security Groups** prompt, select security groups to identify who has permission to access the securable content.

4. From the **Access to Segments** prompt, select security segments that you want members of the specified security groups to be able to access. Workday-owned security groups include:
    1. Job Application - Contingent Worker
    2. Job Application - Employee
    3. Job Application - External

You can't combine different types of security segments in a segment-based security group.

#### Example scenario

You want a Benefits Administrator to be able to manage only benefits-related documents. You don't want them to be able to manage payroll-related documents. Workday secures access to manage all worker documents to the Worker Data: Add Worker Documents and Worker Data: Edit and Delete Worker Documents domains. You can create a Document Categories - Benefits segment to identify benefits-related documents. You can then use the security segment to create a segment-based security group so Benefits Administrators can access only the benefits-related documents.

#### Next steps

Users with access to a domain through both a segment-based and a non-segment-based security group have permission to access all segments. Make sure you associate non-segment-based security groups with users who have permission to access all segments by:

- Reviewing all security groups on the policy before adding segment-based security groups.
- Reviewing the included security groups in an aggregation security group.

To provide security permissions:

- Add the security group to security policies.
- Activate pending security policy changes.
- Activate the security group when you want to enable the permissions on an inactive security group.

### Edit domain security policies

You can configure which security groups have permission to access the secured items in a domain.

You'll need the **Security Configuration** domain in the System functional area.

1. Access the **Domain Security Policies for Functional Area** report.

2. Select a security policy.

3. Select **Edit Permissions**.

4. Select the **View** or **Modify** checkbox to grant the security groups access to the report or task securable items.

5. Select the **Get** or **Put** checkbox to grant the security groups access to integration and report or task securable actions.

### Activate pending security policy changes

Create an active timestamp using the Activate Pending Security Policy Changes task. Security policy changes made since the previous active timestamp take effect immediately. The active timestamp now reflects the current time, regardless of pending changes.

You can run these reports to view a detailed list of the security policy changes you’re activating:

- Domain security policies with pending changes
- Business process security policies with pending changes

1. Access the **Activate Pending Security Policy Changes** task.

2. Describe your changes in the **Comment** field.

3. Tick the **Confirm** checkbox to activate your changes.

You can use the **View All Security Timestamps** report to roll back to a previous timestamp.

### Retrieve the Workday Web Service endpoint

You can find the required Workday Web Service endpoint on the **Workday Data Centers** page on **Community**.

1. Use [this page in Workday](https://resourcecenter.workday.com/) to identify which Workday Production Data Center your tenant is in.

2. Now that you know your data center, fill in your information (in the bolded areas) to get your URL. You'll need this URL for integration in your Microsoft 365 admin center. "https:// {**Production Data Center URL Prefix**}/ccx/service/{**Tenant name**}/Learning/v38.0".

    For example, your URL could look like this: "https://wd3.myworkday.com/ccx/service/yourorg/Learning/v38.0".

## Configure in your Microsoft 365 admin center

>[!Note]
> You'll need to have admin permissions in Microsoft 365 to complete these steps.

1. Sign in to your [Microsoft 365 admin center](https://admin.microsoft.com).

2. Navigate to **Settings**, then **Org settings**. Select Viva Learning, and choose Workday in the panel.

3. Fill in the following required configuration details:
    1. **Display name:** This is the name of the carousel under which Workday learning content will appear for your organization in Viva Learning. If you don't enter a name, it will display the name "Workday".
    2. **Learning Workday Web Service (WWS) endpoint:** This is the URL that you got when you [retrieved the endpoint](#retrieve-the-workday-web-service-endpoint).
    3. **Username:** This is the username that you chose when you [created the integration system user](#create-an-integration-system-user).
    4. **Password:** This is the password that you chose when you created the integration system user.

4. Select **Save** to save the configuration details and complete the setup process.

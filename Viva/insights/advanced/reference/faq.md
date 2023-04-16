---
ms.date: 07/15/2022
title: Advanced insights FAQ
description: Get answers to frequently asked questions about Microsoft Viva Insights' advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Advanced insights FAQ

In this article, we address the most commonly asked questions about the analysis tools in Microsoft Viva Insights' advanced insights app. We've grouped these questions into the following sections:

* [Functionality and features](#functionality-and-features)
    * [Roles](#roles)
    * [Privacy and compliance](#privacy-and-compliance)
    * [Language support](#language-support)
* [Setup and configuration](#setup-and-configuration)
* [Organizational data](#organizational-data)
* [Use advanced insights](#use-advanced-insights)
    * [Meeting exclusions](#meeting-exclusions)
    * [Data validation, verification, and use](#data-validation-verification-and-use)
    * [Queries](#queries)


## Functionality and features

### Roles

#### Q1. Is Viva Insights a tool for human-resource planning?

A1. No. Viva Insights is a collaboration analysis tool for analyzing behavior and network patterns.

#### Q2. How do personal, manager, leader, and advanced insights differ?

A2.

* Personal and private insights are for individual use only.
* Manager insights are for people managers or team leads.
* Leader insights are for business leaders.
* Advanced insights are for analysts to run top-down analysis on advanced insights with aggregated and de-identified metrics.

### Privacy and compliance

#### Q1. How much data does Viva Insights collect?

A1. Initially 13 months' worth of data is collected and processed for Viva Insights. Through weekly refreshes, the system continues to increase this history until 27 months’ worth of data is collected. As a Microsoft customer, you can file a request, such as for security reasons, to provide Viva Insights with less than this default amount; in that case, the minimum amount that can be collected is one month.

#### Q2. Does advanced insights support a separate data environment that adheres to compliance and regulatory requirements such as those required by the government?

A2. Advanced insights are not currently available in data cloud environments that Microsoft maintains for government agencies.

#### Q3. How does Viva Insights adhere to regional data storage and processing requirements (such as those required by GDPR)?

A3. Viva Insights stores and processes customer data in a compliant location as required by regional and state regulations. For more information on Microsoft’s commitment to data residency, visit  [Microsoft EU Data Boundary Overview](https://www.microsoft.com/en-us/trust-center/privacy/european-data-boundary-eudb). For more information on where data is stored and processed for your location, refer to the following links:

* [Personal insights – Data Residency for Other Microsoft 365 Services](/microsoft-365/enterprise/m365-dr-workload-other#viva-insights--personal)
* [Advanced, manager, and leader insights – Data Residency for Other Microsoft 365 Services](/microsoft-365/enterprise/m365-dr-workload-other#viva-insights--advanced-mgr-leader)

### Language support

#### Q1. Can I use the advanced insights app in a language other than English?

A1. Yes, you can use the webapp in languages other than English. There are a few features, though, that are available in English only: system-reserved names for employee attributes and meeting attributes. We plan to translate these features in the future.

#### Q2. Can I upload an organizational data file that has non-English words or letters?

A2. Yes. The organizational data file can have non-English words or letters. However, note the following:

* File names and individual rows can have non-English words or letters.
* Each column header must be mapped to an attribute with an English name.

#### Q3. Can I create a query with filters or meeting subject lines that contain non-English words or letters?

A3. Yes. You can use filters in queries that include:

* Attributes or values from your organizational data that include non-English words or characters.
* Meeting subject lines (which can include non-English words or characters) as specific filter criteria.

### Setup and configuration

#### Q1. What do I need to do to enable advanced insights?

A1. To enable advanced insights for your organization, you'll need to:

* Assign licenses. 
* Assign roles.

Optionally, after you sign in, you can:

* Configure settings.
* Upload organizational data.  

For details about setup, refer to [Set up Advanced insights](../setup-maint/setup.md).

>[!Important]
> For the advanced insights app to run, at least 10 people in your organization need Viva Insights licenses. The app requires this number because credible analyses need at least 10 employees. For more information, refer to [Assign licenses overview](../setup-maint/assign-licenses.md).

#### Q2. Is the number of analyst role assignments limited?

A2. No limit is imposed for **Insights Analyst** roles.

#### Q3. Does Viva Insights ignore people who aren't assigned a license?

A3. Viva Insights doesn't ignore people without licenses, but it doesn't measure them or process their data. However, because these people are internal collaborators of measured employees, Viva Insights uses their collaboration data for analysis when measured employees collaborate with them through meetings, email, unscheduled calls, or chats.  

#### Q4. Our admin assigned the required licenses. Why can't Insights Analysts access the advanced insights app?

A4. It might take a few days for Viva Insights to process Microsoft 365 collaboration data and for assigned users to get the right permissions. Most customers are able to access the app four to five days after the Insights admin assigns licenses.

If you're getting an error, you might want to ask the following questions:

* **Do I have the right role assigned?** Before you can access the advanced insights app, you'll need a Viva Insights-specific role assigned to you in the Microsoft 365 admin center. Analysts need the **Insights Analyst** role. You might need to ask your organization Microsoft 365 admin to check if the role was assigned to you in the admin center. Learn more about role assignment in [Assign user roles for Viva Insights](../setup-maint/assign-user-roles.md).

    >[!Note]
    >Before they can use the app, customers with Privileged Identity Management might need to complete a few additional steps to activate their role. Refer to [Assign Azure AD roles in Privileged Identity Management](/azure/active-directory/privileged-identity-management/pim-how-to-add-role-to-user#assign-a-role) for more information.

* **With my role, can I access this feature?** Only certain roles can access some parts of the app. To learn which features are available for which role, refer to [User roles](../setup-maint/user-roles.md#feature-access).

* **Do enough people have licenses assigned to them?** For analysts to access the advanced insights app, your admin team needs to assign a certain number of licenses to people in your organization. This number needs to be equal to or greater than your [minimum group size](../setup-maint/setup.md#minimum-group-size). The default minimum group size is 10, so at least 10 people in your organization need a license before analysts can sign in and start using advanced insights.

### Organizational data

#### Q1. What causes a failed or an invalid upload?

A1. An upload can fail if the data has invalid values, if it is missing required data, or for other reasons. Refer to these articles for details:

* [Validation fails](../admin/upload-org-data-first.md#validation-fails) in [Upload organizational data (first upload)](../admin/upload-org-data-first.md)

* [Validation fails](../admin/upload-org-data-subsequent.md#validation-fails) in [Upload organizational data (subsequent uploads)](../admin/upload-org-data-subsequent.md)

#### Q2. For the required fields, what percentage is required for the validity threshold?

A2. **PersonId** and **EffectiveDate** fields need to meet 100 percent of the validity threshold, because each row of data needs to have a **PersonId** for each person in your organization. The other required fields (such as **ManagerId**) need to exceed 95 percent of the validity threshold. The calculations for validity threshold consider only two kinds of data values: valid values and blank values. For the 95-percent validity threshold, the column will pass validation if fewer than five percent of the values in the column are blank and the rest are valid. However, if even one cell contains malformed data, the entire file upload will fail.

#### Q3. What happens if an employee (represented by a PersonId) has more than one manager (represented by ManagerIds)?

A3. Viva Insights doesn’t fail an upload if a person doesn’t have one single, primary manager. However, one manager per employee is recommended. This manager is represented by the **ManagerId** for that **PersonId** on a given **EffectiveDate**. Note that the **Insights Admin** ("admin" in this article) can use the **EffectiveDate** field in the organizational data to indicate that an employee’s primary manager has changed from one month to the next.

#### Q4. Who gets the organizational data to upload?

A4. While Azure Active Directory is the default data source, a manual file upload is preferred. Usually, HR gives this data to the admin, who then prepares and uploads it.

#### Q5. Who can access organizational data after it's uploaded?

A5. For privacy reasons, no one can download the raw data that was uploaded. Viva Insights admins and analysts can view metadata about the organizational data on the **Data quality** page, but they can’t see how the attribute values map to individual people.

### Use advanced insights

#### Meeting exclusions

##### Q1. How are privacy settings and metric rules different?

A1. Admins set up the privacy settings for how data is extracted, such as preventing data from ever being included in any calculation. Note that changes to privacy settings apply to future data extractions and aren't retroactive to past data. To learn about Insights privacy, refer to [Privacy](../privacy/privacy.md). 

#### Data validation, verification, and use

##### Q1. Why is my measured population less than the number of employees with assigned licenses?

A1. This scenario can occur if:

* You selected only a subset of the population for the analysis.
* Your admin excluded a subset of the population from the organizational data that's uploaded. 

For more information, refer to [Assign licenses](../setup-maint/assign-licenses.md).

##### Q2. Why doesn't the email or meeting trend line extend back for the entire historical 13-month period (or for the selected custom time period)?

A2. Business policies can affect the historical data processed for Viva Insights. As you view historical data, if you see a steady decline or point-in-time drop in email and/or meeting activity, it might be because:

* An email was archived.
* Recurring meetings were deleted before the data was extracted. 

However, these actions only impact initial baseline data. Future deletions don't affect weekly data that was previously collected.  

##### Q3. How does Viva Insights process data for meetings and emails sent to distribution lists?

A3. Viva Insights processes email and meetings data for a distribution list as a single entity or person. It doesn't expand the distribution list and assign meeting and email hours to the list's members. For more accurate data, upload the organizational data attributes for these lists by adding attributes of the distribution-list members or whatever best describes the list population. 

##### Q4. What collaboration information is processed from Microsoft Teams?

A4. Teams provides information about collaboration activities, namely direct messages (chats) and calls. It does not provide information about Teams channels.

##### Q5. When a person sends a message or meeting invite for a group’s shared mailbox or on behalf of another person, who gets credit for sending it?

A5. It depends on the type of mailbox and which permissions are set for the Exchange Online mailbox. For details, see [Mailbox permissions](/Exchange/recipients/mailbox-permissions).

* A shared mailbox (Microsoft 365 group mailbox) typically has a number of group members that share access and permissions for the group mailbox. An example of a shared mailbox is LeadershipTeam@Contoso.com. For details, see [Which permissions you should use in shared mailboxes](/exchange/collaboration-exo/shared-mailboxes#which-permissions-should-you-use).
    * **Send As** permission - When a group member with Send As permission for a shared mailbox sends a message or meeting invitation from the group mailbox, Exchange gives credit to the shared mailbox instead of any single person in the group. Viva Insights does not use this action in its calculations.
    * **Send on Behalf** permission – This permission isn't available for shared mailboxes in Exchange Admin Center. However, if it is set with PowerShell (GrantSendonBehalf parameter), the person who sends the message gets credit for it in Viva Insights calculations.
* An individual mailbox (or a linked mailbox) with a primary mailbox owner can link or give delegate access and one of the following permissions to another person to send messages or meeting invites for the primary mailbox owner. For example, an assistant with delegate access can send a message or meeting invite from their manager's mailbox. A delegate can have one of the following permissions. For details, see [Give mailbox permissions to another user](/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user).
    * **Send As** permission – The primary owner of the mailbox gets credit for sending the message or invite in Viva Insights calculations.
    * **Send on Behalf** permission – The person who sends the message on behalf of the mailbox owner gets the credit in Viva Insights calculations.
    * Both **Send As** and **Send on Behalf** permissions – If the delegate person has both permissions set, the Send As permissions are used and that person does not get credit for sending the message or invite in Exchange and therefore Viva Insights credits the owner of the mailbox in calculations.

##### Q6. Why don't I see data from this week in my analyses?

A6. Microsoft 365 collaboration data is updated weekly for advanced insights and other applicable analysis. Each Monday, Viva Insights processes your organization's collaboration data from the preceding week, which includes the previous Sunday through Saturday. For example, on Monday, November 15th, analysis will include data through the previous Saturday, November 13th.

##### Q7. Why don't I see last week's data in my analyses?

A8. If you expect your analysis to include last week's collaboration data and you only see data through the previous Sunday, this is because all multi-day periods (weeks and months) that are included in analysis reflect the first day of the specified time period. For example, for a query aggregated by week, you’ll see it starts with Sunday. If you see a "November 7th” row in a weekly aggregated query, it means that the metrics include data through Saturday, November 13th.

#### Queries  

##### Q1. Why don't totals for meeting hours and email hours match up with totals for working hours and after hours in person query output?

A1. Because totals for working hours and after hours calculate the "time booked on your calendar" instead of "time in meetings." Calculations for total meeting hours (time in meetings) adjusts the duration time to account for double-booked meetings, where a person has two meetings scheduled at the same time or times that overlap on the calendar. A heuristic logic orders which meetings a person likely attended and assigns time accordingly.

##### Q2. When I download and view a query, why is the data unreadable or not shown correctly in Excel?

A2. You probably opened the .csv file as-is. For Excel to show the data correctly, you need to import the .csv file into Excel. If you're using Excel 2016, follow the steps in Access query results and modify existing queries . For other versions of Excel, open **Help** in Excel and then search for the instructions on how to import a .csv file.

##### Q3. Why don’t a person’s low-quality meeting hours equal the sum of their redundant, conflicting, and multitasking meeting hours in my query?

A3. You might expect the total number of redundant, conflicting, and multitasking meeting hours to equal the total number of low-quality meeting hours. However, sometimes they won’t equal because of how conflicting meeting hours are calculated.

## Community and learning

##### Q1. How can I stay updated with the latest Viva Insights features and learn from peers who are using the tool for their organizational needs?

A1. We encourage all Viva insights users to visit and register on the [Viva Insights community](https://community.vivainsights.microsoft.com/t5/Viva-Insights-blogs/bg-p/viva-insights-blog). The community has:

* Forums to connect with peers and discuss shared experiences.
* Forums to contribute and receive support on common issues which are routinely reviewed by our team of experts.
* Monthly blog posts to learn about new features and tools.
* Spaces to share ideas and engage with the product development team.

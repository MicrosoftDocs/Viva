---
title: FAQs for Configuring Workday in Microsoft Viva Learning 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 04/30/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - highpri
  - Tier1
ms.localizationpriority: medium
description: FAQs for how to configure and manage Workday for Microsoft Viva Learning.

---

# FAQs in Configuring Workday in Microsoft Viva Learning

This article outlines answers for frequently asked questions for the integration between Workday and Microsoft Viva Learning.

**1. When will the content reflect in the Viva Learning app after configuration?**

Our estimate 24 - 48 hours for a full sync. This is dependent on the catalog size.

**2. When will assignments reflect in Viva Learning app after configuration?**

Our estimate 24 - 48 hours for a full sync. This is dependent on the assignment size.

**3.	What are the sync frequencies?**

|     Data Type    |     Sync   frequency    |
|---|---|
|     Catalog     |     Delta   sync runs every 24 hours, capture delta for last 24 hrs    |
|     Workday   hosted thumbnails    |     Delta   sync runs every 24 hours, capture delta for last 24 hrs    |
|     3P   Thumbnails    |     Delta   sync runs every 24 hours, capture delta for last 24 hrs    |
|     User RaaS    |     Full sync   every 12 hours    |
|     Assignments    |     Delta   sync runs every 12 hours, capture delta for last 12 hrs    |
|     Assignment   completions    |     Delta   sync runs every 12 hours, capture delta for last 12 hrs    |
|     Self-enrolment   completions    |     Delta   sync runs every 12 hours, capture delta for last 12 hrs    |

Note that these frequencies might vary for some customers in case of any custom implementation.

**4. How can I trigger the manual full sync?**

Admins can trigger the manual sync from the Manage Providers within the Viva Learning Admin tab. Admins require Global Admin, Knowledge Admin, and Knowledge Manager permissions. The full trigger option is available for catalog sync.

**5. What if the admin user creating the refresh token leaves the organization?**

The Refresh token is tied to a Workday account, which is the Information System User and not any specific user. This refresh token is additionally available in the context of the Client which Admin creates in Workday. This client isn't tied to Admin user who created it, rather it's available to all the admins in the tenant.

**6. Are there any other “grant type”, apart from “refresh_token"?**

No, Workday only supports “refresh_token” grant type for System-to-System integrations. Types like “client_credentials” isn't supported.

**7. How is the refresh_token stored?**
 
The refresh token can be stored as an encrypted object. This is similar to password and user IDs.

**8. What are the required permissions for the user creating the report and providing the permissions?**

This action requires the **Get Only** access to the **Reports: Learning Record** domain. For more information, see the steps mentioned for enabling LRS.

**9. How do I execute the RaaS reports?**

Once a RaaS report is created, you can execute or run it from the Workday portal.


**10.	How does Viva Learning generate access token for OAuth?**

The refresh token is generated based on client ID, client secret and refreshes token. The admin needs to update all three fields in the MAC portal. The refresh token is a nonexpiring one analogous to the client secret or passwords that we stored for other providers. The refresh token’s infinite TTL shouldn’t be a concern.

**11.	What happens if the sync fails?**

If the sync fails, the admin can export the catalog logs for details around sync errors.

**12. How can I edit scopes in API client?**

Go to the “View API Client” task. You can select the client under “API Clients for Integration” and update the scope.

![A screenshot of the Workday API client with the option to upgrade the scope.](/viva/media/learning/workday-FAQ-1.png)


**13.	How can I filter the providers integrated into Workday in Catalog RaaS?**

This scenario isn't supported.

**14. How can I test if my report is working as expected?**

Go to **Report** and select **Run** or **Test** and then add desired time field values. If configured correctly, the report successfully runs.

![A screenshot of the action window with the option to run the report.](/viva/media/learning/workday-FAQ-4.png)

**15. How does Viva Learning store thumbnail images?**

Thumbnail images for providers integrated in Workday (for example, LinkedIn configured in Workday) are ingested using the RaaS report. Thumbnail image for Workday-hosted content is pulled through the APIs. The thumbnail image format supported by Workday is also supported by Viva Learning. 

**16. What if an API configuration isn't added in Viva Learning?**

This is a required field for configuration.

**17. What is the payload size which can be handled by RaaS reports?**

For a single report API call, a maximum of 3 million records (2GBs) is returned and the maximum execution time of single API call is 30 mins. 
You can make a maximum of 75,000 requests in a 24 hour period (15k requests per hour). Report execution timeout is 30 mins but can hit a session or http gateway timeout before that time. For more information, see the [Workday support article on RaaS](https://docs.workato.com/connectors/workday/workday_raas.html).

**18. What happens to the courses if `InNonSearchable` is `True` in Workday?**

These courses aren't available for search in Viva Learning. 

**19. What happens to the courses if `IsEffectiveDate` is set to the future?**

The course isn't ingested in Viva Learning.

**20. What special characters can be stored in content title and description?**

Special characters can be added on Workday in the content title and description. Viva Learning doesn't support the different text formatting for descriptions that are available in Workday.

**21. What if the client ID, secrets and auth token are expired?**

You need to regenerate it from the Workday portal and reconfigure Workday on Viva Learning with new parameters. 

**22. Does Viva Learning supports learning journeys or paths from Workday?**

We don't support these scenarios.

**23. Are permissions from Workday supported in Viva Learning?**

We don't support these scenarios.

**24. Can you provide a list of the end points that Viva Learning is accessing?** 

To fetch RaaS reports, Viva Learning uses REST API. The URL for this report isn't fixed and depends on the user and Workday account name.  The following [SOAP APIs](https://community.workday.com/sites/default/files/file-hosting/productionapi/Learning/v39.2/Learning.html) end points are used to fetch thumbnail images for Workday hosted content:

- [Get Learning Digital Courses](https://community.workday.com/sites/default/files/file-hosting/productionapi/Learning/v39.2/Get_Learning_Digital_Courses.html)
- [Get Learning Blended Courses](https://community.workday.com/sites/default/files/file-hosting/productionapi/Learning/v39.2/Get_Learning_Blended_Courses.html)
- [Get Learning Lesson](https://community.workday.com/sites/default/files/file-hosting/productionapi/Learning/v39.2/Get_Learning_Lessons.html)
- [Get Learning Programs](https://community.workday.com/sites/default/files/file-hosting/productionapi/Learning/v39.2/Get_Learning_Programs.html)

**25. Which of the RaaS reports are indexed? Can reports handle large data volumes?**

|RaaS report | Indexed? |
|--| --| 
| Catalog RaaS | **Indexed** | 
| User RaaS | **Indexed** | 
| LRS RaaS | **Not indexed**. The org ID-based report filtering is in place to handle large data sets| 
| Self enrollment RaaS | **Not indexed**. Unlike the LRS RaaS, this report isn't filterable on org ID. | 

**26. What are the guidelines in server migration?**

If the server migration is expected to change the WWS endpoint, RaaS URL, and deep links to courses, reach out to Viva Learning product team. 
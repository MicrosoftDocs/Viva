---
title: FAQs for Configuring Workday in Microsoft Viva Learning 
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 11/08/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
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

These are the frequently asked questions for the integration between Workday and Microsoft Viva Learning.

**1. When will the content reflect in the Viva Learning app after configuration?**

Our estimate 24 - 48 hours for a full sync. This is dependent on the catalog size.

**2. When will assignments reflect in Viva Learning app after configuration?**

Our estimate 24 - 48 hours for a full sync. This is dependent on the assignment size.

**3.	What are the sync frequencies?**

Daily delta sync is in place for all data types, including catalog, assignments, completion, and API-thumbnails. Full user RaaS sync happens every two days.
	
**4.	How can I trigger the manual full sync?**

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

Go to the task “View API Client”. You can select on the client under “API Clients for Integration” and update the scope.

![A screenshot of the Workday API client with the option to upgrade the scope.](/viva/media/learning/workday-FAQ-1.png)


**13.	How can I filter the providers integrated into Workday in Catalog RaaS?**

This scenario isn't supported.

**14. What is the guidance on direct integration of 3Ps in Viva Learning or integration in LMS?** 

These are our recommendations on Workday integrations that include 3P content providers:

- **Scenario:** Organizations have the learning management system (LMS) integrated with other 3P content providers such as LinkedIn, Udemy, and Coursera for tracking user completion records.

- **Common practice:** Organizations choose to have compliance trainings come from the LMS and growth, skill, and optional trainings come from digital content providers. 
    - Compliance trainings have to be audited and tracked with a few exceptions based on the regional policies.
    - Growth, skill, and optional trainings don't have to be tracked, but can be recommended to others.

- **Deciding factors:** Do you need content coming from 3P content providers to be tracked or audited for compliance reasons?
    - If **yes**: Choose **LMS including 3P content providers**.
    - If **no**: Choose **LMS NOT including 3P content providers**.
  
- For **LMS including 3P content providers:** Viva Learning is integrated with LMS that includes 3P content providers; 
    It’s highly recommended not to have individual connector configurations for the included 3P content providers in LMS to prevent content duplication. 
    - **Admin experience:** 
        - Less overhead in managing only the connector for the LMS. 
        - Less overhead in maintaining the 3P content that is part of learning paths, collections, and other experiences.  
    - **End user experience:** 
        - Consistent consumption experience for content coming from both LMS and 3P providers.
        - The “Assigned to you” tab shows the content assignment for 3P content.
        - The “Completed” tab shows the history of completion status for 3P content.
-  For **LMS NOT including 3P sources:** 
    - **Admin experience:**
        - Manage multiple connectors for LMS and each 3P content provider.
        - Manually update the 3P content that is part of learning paths, collections, and other experiences when the connectors for 3P content are updated or removed.
    - **End user experience:** 
        - Mixed consumption experience for contents coming from LMS and 3P content providers.
        - The “Assigned to you” tab won't show any assignments for 3P contents as they can be only recommended. 
        - The “Completed” tab won't show the history of completion status for 3P contents.
      
> [!NOTE]
> Deleting connectors from the admin interface will only remove the courses from LMS and 3P content providers based on the connectors being deleted.  
> That certain LMS connectors need to be reconfigured only after the content catalog is cleaned up. Please contact Microsoft Viva Learning support. 

**15. How can I test if my report is working as expected?**

Go to **Report** and select **Run** or **Test** and then add desired time field values. If configured correctly, the report successfully runs.

![A screenshot of the action window with the option to run the report.](/viva/media/learning/workday-FAQ-4.png)

**16. How does Viva Learning store thumbnail images?**

Thumbnail images for providers integrated in Workday (for example, LinkedIn configured in Workday) are ingested using the RaaS report. Thumbnail image for Workday-hosted content is pulled through the APIs. The thumbnail image format supported by Workday is also supported by Viva Learning. 

**17. What if an API configuration isn't added in Viva Learning?**

This is a required field for configuration.

**18. What is the payload size which can be handled by RaaS reports?**

For a single report API call, a maximum of 3 million records (2GBs) is returned and the maximum execution time of single API call is 30 mins. 
You can make a maximum of 75,000 requests in a 24 hour period (15k requests per hour). Report execution timeout is 30 mins but may hit a session or http gateway timeout before that. For more information, see the [Workday support article on RaaS](https://docs.workato.com/connectors/workday/workday_raas.html).

**19. What happens to the courses if `InNonSearchable` is `True` in Workday?**

These courses aren't available for search in Viva Learning. 

**20. What happens to the courses if `IsEffectiveDate` is set to the future?**

The course isn't ingested in Viva Learning.

**21. What special characters can be stored in content title and description?**

Special characters can be added on Workday in the content title and description. Viva Learning doesn't support the different text formatting for descriptions that are available in Workday.

**22. What if the client ID, secrets and auth token are expired?**

You need to regenerate it from the Workday portal and reconfigure Workday on Viva Learning with new parameters. 


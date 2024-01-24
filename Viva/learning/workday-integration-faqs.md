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

A daily delta sync is in place for all data types: catalog, user, assignments, completion and thumbnails).
	
**4.	How can I trigger the manual full sync?**

Admins can trigger the manual sync from the Manage Providers within the Viva Learning Admin tab. Admins require Global Admin, Knowledge Admin, and Knowledge Manager permissions. The full trigger option is available for catalog sync.

**5. What if the admin user creating the refresh token leaves the organization?**

The Refresh token is tied to a Workday account, which will be the Information System User and not any specific user. This refresh token is additionally available in the context of the Client which Admin creates in Workday. This client isn't tied to Admin user who created it, rather it's available to all the admins in the tenant.

**6. Are there any other “grant type”, apart from “refresh_token"?**

No, Workday only supports “refresh_token” grant type for System-to-System integrations. Types like “client_credentials” isn't supported.

**7. How is the refresh_token stored?**
 
The refresh token can be stored as an encrypted object. This is similar to password and user IDs.

**8. What are the required permissions for the user creating the report and providing the permissions?**

This action requires the **Get Only** access to the **Reports: Learning Record** domain. For more information, see the steps mentioned for enabling LRS.

**9. How do I execute the RaaS reports?**

One a RaaS report is created, you can execute or run it from the Workday portal.


**10.	How does Viva Learning generate access token for OAuth?**

The refresh token is generated based on client ID, client secret and refreshes token. The admin needs to update all three fields in the MAC portal. The refresh token is a nonexpiring one. It's analogous to the client secret or passwords that we have stored for other providers. The refresh token’s infinite TTL shouldn’t be a concern.

**11.	What happens if the sync fails?**

If the sync fails, the admin can export the catalog logs for details around sync errors.

**12. How can I edit scopes in API client?**

Go to the task “View API Client”. You can select on the client under “API Clients for Integration” and update the scope.

![A screenshot of the Workday API client with the option to upgrade the scope.](/viva/media/learning/workday-FAQ-1.png)


**13.	How can I filter the providers integrated into Workday in Catalog RaaS?**

- **Option 1:** Filter on the RaaS report. This makes sure that only the courses you want are syncing Viva Learning.

![A screenshot of the filters on the RaaS report that ensures that only your specified sources are syncing with Viva Learning.](/viva/media/learning/workday-FAQ-2.png)


- **Option 2**: Disable the provider channel on the Workday portal.

    - Go to the task “Configure External content provider”
    
    - Select the provider.
    
    - Select **Deselect All** under **channels**.
    - This removes the course from both Workday and Viva Learning

![A screenshot of the configure external content provider option with the "deselect all" checkbox highlighted.](/viva/media/learning/workday-FAQ-3.png)

**14. How can I test the outcome once the report is created. Can I execute it and see the results?**

Go to **Report** and select **Run** or **Test** and then add desired time field values. If configured correctly, the report successfully runs.

![A screenshot of the action window with the option to run the report.](/viva/media/learning/workday-FAQ-4.png)

**15. How does Viva Learning store thumbnail images?**

Thumbnail images for providers integrated in Workday (for example, LinkedIn configured in Workday) are ingested using the RaaS report. Thumbnail image for Workday-hosted content is pulled through the APIs. 

**16. What if an API configuration isn't added in Viva Learning?**

This is a required field for configuration.

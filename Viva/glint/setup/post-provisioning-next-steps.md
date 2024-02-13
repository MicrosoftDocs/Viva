---
title: Set up admins in up Viva Glint instance
description: Take care of a few items of business before you begin your first Viva Glint program journey.
ms.author: judithweiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Add administrators to Viva Glint, Viva Glint sites, Viva Glint learning paths and modules, training
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 04/21/2023
---

# Set up admins in your Viva Glint instance

Welcome to Microsoft Viva Glint! If you have landed on this page, you should already have your tenant provisioned.

- If you haven't already completed tenant provisioning, [set up a Microsoft Viva tenant](viva-glint-tenant-provision.md).
- If you have completed tenant provisioning, follow these next steps to continue Viva Glint deployment:

## Add administrators to your Viva Glint instance

As the tenant Global Admin, you're the default Microsoft Viva Glint Service Admin. This means you have ultimate control over the subscriptions in your Viva Glint product and you can access all data. Additionally - **and importantly** - you can assign Viva Glint Service admin roles to other users.

> [!NOTE]
> Administrators for Viva Glint are assigned within the Viva Glint product only, not through the Microsoft Administrator Center (MAC).

> [!TIP]
> Viva Glint recommends no more than five (5) administrators for your Viva Glint instance.

### Collect administrator information

Compile a file of administrators to upload to Viva Glint with the following columns and user information. Save as **.csv with UTF-8 encoding and a comma separator**.

- **Email:** Work email address
- **Employee ID:** ID value exactly as it appears in your HRIS
- **First Name:** User first name
- **Last Name:** User last name
- **Status:** ACTIVE, in all caps

> [!IMPORTANT]
> To prevent duplication errors with future file uploads, ensure that the Employee ID values for these users match the Employee ID from the HR Information System (HRIS) that will be used to transfer data to Viva Glint.

> [!CAUTION]
> Don't add admin users as Support users. They must be uploaded with a status of ACTIVE to have all Viva Glint permissions.

### Upload administrators to Viva Glint

Upload your administrators to Viva Glint Advanced Configuration:

1. From the admin dashboard, select the **Configure** symbol, then in **Service Configuration**, choose **Advanced Configuration**.
   1. If there is no **Advanced Configuration** option, go to your user profile and in the **Company Admin: Advanced Configuration Access** section, select the pencil symbol to edit. In the **Advanced Configuration Access** dialog, switch the toggle on to **Enable access** and select **Save**.
1. In the **Advanced Configuration** menu, select **Uploads**.
1. In the **Choose job type** dropdown list, select **USERS_UPLOAD**.
1. Switch the **Incremental** toggle on.
1. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section and select **Upload**.
1. In *Upload Job Details**, confirm that **Upload Lines Summary** shows the correct number of users to ADD in the **Lines** column.
1. Select **Apply Upload to Database** to upload new users and select **Yes**.
1. Go to the **Uploads** menu and confirm that the file **State** is SUCCESS and that the **Total Lines** and **Processed Lines** match the number of users in the uploaded file.

### Add administrators to the Company Admin User Role

When users are successfully uploaded, add them to the Company Admin User Role and grant Advanced Configuration access:

1. Select the **Configure** symbol, then in the **Employees** section, choose **People**.
1. Select each user, and on their profile under **User Roles**, select the pencil symbol to edit.
1. In the **Customize User Role** dialog, select the checkbox for **Company Admin** and then choose **Save**.
1. In the **Confirm Role** dialog, select **Grant All Access**.
1. On the user profile, in the **Company Admin: Advanced Configuration Access** section, select the pencil symbol to edit.
1. In the **Advanced Configuration Access** dialog, switch the toggle on to **Enable access** and select **Save**.

## Steps to set up your Viva Glint program instance

As a Viva Glint admin, use the following guidance to complete platform setup and prepare to launch your first Viva Glint survey: [Learn more](https://go.microsoft.com/fwlink/?linkid=2240651).

## What do I do if I need help?

[Get support from Microsoft 365](/microsoft-365/admin/get-help-support?view=o365-worldwide&preserve-view=true)

## Learning and community resources

Viva Glint is a "voice of the employee" solution helping organizations understand and improve employee engagement. Use the following Microsoft sites to help your business get the most from Viva Glint. Seamlessly visit one page to the next to find just what you're looking for, right when you need it.

Build skills that open doors. [See all that you can do with documentation, hands-on training, and certifications to help you get the most from Microsoft products.](https://learn.microsoft.com)

Within Viva Glint Learn, you'll be busy in these two areas, accessible from the top navigation menu.

- Documentation- [See all you can do with resources and solutions.](https://go.microsoft.com/fwlink/?linkid=2230911)
- Training - [Browse the full catalog of Learning Paths and Modules](/training/browse/?terms=glint)

### Learn before you leap

Within Microsoft Learn, admins are recommended to invest time in learning about Viva Glint before introducing these listening programs to their teams:

- [**Introduction to Microsoft Viva Glint:**](https://go.microsoft.com/fwlink/?linkid=2238926) Designed to give an overview of what Viva Glint is, who should use it, and how your organization will benefit from using this app.
- [**Viva Glint's Modern Approach to Measuring Engagement:**](https://go.microsoft.com/fwlink/?linkid=2239110) Designed to introduce the methodology of People Success, describe how we use it, and detail how Viva Glint methodology can be embedded into your daily flow of work.
- [**Viva Glint Program Design and Setup:**](https://go.microsoft.com/fwlink/?linkid=2238496) Designed to give high level information about dashboard settings, setting up a first recurring survey, and sharing results.

## Microsoft Viva Community

[Explore the Viva Community that you'll be part of.](https://techcommunity.microsoft.com/t5/welcome-to-the-microsoft-viva/ct-p/Microsoft-Viva) The Viva Community is public facing for all the Viva apps and Viva Glint has its own community, as well.

- [**Register for the Viva Community**](https://techcommunity.microsoft.com/t5/getting-started/getting-started-on-the-tech-community/ta-p/3512627) to be part of private user groups, post in forums, and to receive invitations to special events. Select **Sign In** to create an account.

### Get started with the Viva Glint community

1. [Sign up for the](https://techcommunity.microsoft.com/t5/viva-glint-customer-user-group/gh-p/Viva_Glint_Customer_User_Group)Viva Glint Customer Private User group. In this group you'll find customer-only content and a gated space to chat with your peers. Our team will review member requests and accept customers regularly.
2. [Subscribe for updates to the Viva Glint Customer Private User Group blog](https://techcommunity.microsoft.com/t5/viva-glint-customer-user-group/bg-p/Viva_Glint_Customer_User_Groupblog-board). Once you're a member of the private user group, subscribe to the blog to receive customer-only updates about product news, thought leadership content, upcoming events, and more.

:::image type="content" source="../../media/glint/start/viva-community.png" alt-text="Screenshot that displays the first look of Viva Glint community.":::

## Microsoft Viva Adoption

Find resources to go from inspiration to execution. Adoption resources will give you the tools you need to implement Viva Glint. Our papers will guide you through some of the most pressing issues in the employee experience space. [Find resources to support your Viva Glint adoption here.](https://adoption.microsoft.com/viva/glint/)

## Microsoft Viva Support

[Resources and guides for survey participants to help answer questions and provide background on Viva Glint methodology](https://go.microsoft.com/fwlink/?linkid=2239301).

## How to take a survey - for all survey takers in your organization
[How to take a Viva Glint survey](https://support.microsoft.com/en-us/topic/how-to-take-a-viva-glint-survey-6691b3c7-d7f4-48f5-a69f-d1fe5ce528a5)

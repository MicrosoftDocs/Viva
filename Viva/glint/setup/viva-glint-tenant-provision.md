---
title: Set up a Microsoft Viva Glint tenant
description: When a new customer purchases Viva Glint or Viva Suite, they're entitled to the Viva Glint product, and tenant provisioning should occur within days. 
ms.author: SarahBerg
author: SarahAnneBerg
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: tenant, viva glint tenant
ms.collection: 
 - m365initiative-viva
 - selfserve
 - essentials-get-started
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/21/2024
---

# Set up a Microsoft Viva Glint tenant

To deploy apps that use the Microsoft platform for identity and access management, you first need access to a Microsoft Entra ID *tenant*. In the Microsoft Entra tenant, register and manage your Viva Glint apps, configure access to data and other web APIs, and enable features like Conditional Access. 

A tenant represents an organization. It's a dedicated instance of the Microsoft Entra tenant that an organization or app developer receives at the beginning of a relationship with Microsoft. 

Each Microsoft Entra tenant is distinct and separate from other Microsoft Entra tenants. It has its own representation of work and school identities, consumer identities (if it's an Azure AD B2C tenant), and app registrations. An app registration inside your tenant can allow authentications only from accounts within your tenant or all tenants. 

When a new customer purchases Viva Glint, they're entitled to the Viva Glint product, and tenant provisioning should occur within days of the purchase. Customer instances can be hosted on Viva Glint’s US or EU server. 

> [!NOTE]
> If you don't already have a Microsoft Entra user account, you can [create one for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).

> [!IMPORTANT]
> If you’re migrating from LinkedIn Glint, don’t provision a new Viva Glint tenant. This step is completed for you as part of your technical migration to Microsoft Viva Glint.

## Customers entitled for Viva Glint provisioning 

- Net new Viva Glint standalone customers
- Viva Suite customers
- LinkedIn Glint standalone customers
- Existing Viva suite and LinkedIn Glint customer

> [!NOTE]
>
> - A Viva Glint tenant is not available for GCC/GCC H entities as it is intended for commercial services only.
> - A minimum number of 50 active user licenses are required for tenant provisioning. Licenses requested below 50 will prompt a screen message and email to inform you to contact your Microsoft Account Manager or adjust the number of licenses purchased in the Microsoft Admin Center, if you purchased via our self-serve checkout flow. 

## Begin your Viva Glint provisioning experience

Choose the US or EU URL for Azure login to begin, based on the region of your tenant. [Learn more](/microsoft-365/enterprise/m365-dr-workload-other?view=o365-worldwide#viva-glint&preserve-view=true).

- US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
- EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)

On the sign-in page that appears, enter your User Principal Name (UPN) and password:

:::image type="content" source="../../media/glint/start/glint-provision-signin.png" alt-text="Screenshot of Viva Glint provisioning sign-in page.":::

>[!TIP]
> If you are unsure which URL to choose, begin with the US URL.

## Complete the Welcome to Viva Glint page

After logging into your preferred URL, the Welcome to Viva Glint page displays: 

:::image type="content" source="../../media/glint/start/glint-provision-welcome.png" alt-text="Screenshot of Viva Glint tenant provisioning welcome page.":::

Check the box for notification to be sent and enter an email address if you would like to receive an email notification once your tenant provisioning is complete. Select **Continue** to begin tenant provisioning.

>[!NOTE]
> Tenant provisioning can only be initiated by the Tenant Global Administrator. 

Depending on whether you choose to receive a notification, one of the following screens appear: 

- With notification requested, these messages display: 
    - We’ll notify you when it’s ready.  
    - We’ll add tenant global administrators as your default Viva Glint service administrators. You can update this or add more Viva Glint service administrators within the product anytime.  
    - Select **Learn more** to be taken to post-provisioning next steps while your tenant is getting provisioned. 

- Without notification requested, these messages display: 
    - Check here later to see if it’s ready. Allow a couple of days for this step. 
    - We’ll add tenant global administrators as your default Viva Glint service administrators. You can update this or add more Viva Glint service administrators within the product anytime. 
    - Select **Learn more** to be taken to post-provisioning next steps while your tenant is getting provisioned.

### What if I run into an error?

If your tenant can't be provisioned, this message appears. Select **Request support** and a tab will open for Microsoft 365 support.

:::image type="content" source="../../media/glint/start/tenant-issue.png" alt-text="Screenshot that displays Microsoft Viva Glint tenant facing an issue.":::

## Your view as your tenant is being readied

Dependent upon whether you’ve requested notification to be sent, you’ll receive one of the following messages: 

:::image type="content" source="../../media/glint/start/tenant-ready.png" alt-text="Screenshot that displays Viva Glint's tenant getting ready.":::

> [!NOTE]
> It can take up to five (5) days for a tenant to be ready.

## Proceed to post-provisioning once your tenant is ready

Once you receive the email notification (if you requested notification in the earlier step), select **Get Started**. You're automatically taken to the Viva Glint Learn page for post-provisioning to proceed with setting up your Viva Glint program. 

You can also choose to **Open Viva Glint** from this page:

:::image type="content" source="../../media/glint/start/viva-glint-tenant.png" alt-text="Screenshot that displays Viva Glint tenant ready to use.":::

## Use Microsoft FastTrack for more support 

Microsoft FastTrack can provide help with Microsoft Viva foundational products and capabilities - at no extra cost for the life of your eligible subscription. 

If you’re already registered for Microsoft FastTrack and need support, [use this link](https://www.microsoft.com/fasttrack/microsoft-viva).

To check your eligibility for FastTrack support, [use this link](/microsoft-365/fasttrack/eligibility).

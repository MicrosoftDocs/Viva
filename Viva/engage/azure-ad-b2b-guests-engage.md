---
ms.date: 12/14/2022
title: "Work with AzureAD-B2B guests in Viva Engage communities"
description: "Learn about working with Azure Active Directory-B2B guests in Viva Engage communities."
ms.reviewer: ethli
ms.author: v-whitfieldd
author: dwhitfield233
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Work with Azure Active Directory-B2B guests in Viva Engage communities

The Viva Engage guests feature enables organizations to call in experts such as vendors, suppliers, or consultants from outside the organization to supercharge collaboration. Viva Engage tenants that are aligned to native mode use the Azure Active Directory Business-Business (Azure AD-B2B) guest framework to power guests. Azure Active Directory (Azure AD)-B2B is a secure, compliant external collaboration framework that's used by many apps in the Microsoft 365 suite, including Microsoft SharePoint, Outlook, and Teams.

Any Microsoft 365 user who isn't part of your organization can be added as guest to a Viva Engage community by a Community admin. Azure AD-B2B guests in Viva Engage communities are covered by the same compliance and auditing protection as the rest of Microsoft 365. You can manage them in Azure AD. Guest access is subject to Azure AD and Microsoft 365 service limits.

## Prerequisites for adding an Azure AD-B2B guest to a Viva Engage community

Your Viva Engage tenant should be aligned to native mode before you invite guests as Azure AD-B2B guests to a Viva Engage community. To invite guests, you need to configure settings in Viva Engage and other Microsoft 365 services, including Azure AD, Microsoft 365 Groups, and SharePoint.

If your organization is ready to start inviting guests to Viva Engage communities, configure the following settings.

Engage admins can enable guest access on their networks from the Viva Engage admin center. Within the Viva Engage admin center, navigate to the **Compliance & Governance** tab and click on **Manage data**. You will be redirected to the Yammer admin webpage, where you can enable guest access by navigating to **Security settings** and selecting **External Messaging**.

> [!div class="mx-imgBorder"]
> :::image type="content" source="../media/azure-ad-b2b-guests-engage-external-messaging.png" alt-text="Screen shot shows the Yammer admin panel external user settings.":::

This setting is a Viva Engage tenant-wide setting. It enables community admins to add guests to any Viva Engage community in the network. You control guest access to individual Viva Engage communities [by using sensitivity labels](/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).

External collaboration is a key ingredient for the success of any organization. Viva Engage guests allows you to call in experts, such as consultants or vendors, from outside your organization. Users can invite guests to a community and start a conversation by sharing access to community resources like files. This ease of use makes external collaboration one of the most-used features in Viva Engage.

> [!NOTE]
> If your Viva Engage tenant was provisioned after December 15, 2020, Azure AD-B2B guest functionality is already enabled for your organization by default.

To configure Azure AD, Microsoft 365 Groups, and SharePoint settings, see [Collaborate with guests in a team](/microsoft-365/solutions/collaborate-as-team).

## How to invite a guest to a Viva Engage community

1. Community admins add guests to a Viva Engage community by entering the email address of the guest in the **Add Member** panel of the community.

2. The guest receives a welcome email message. This message includes information about the Viva Engage community to which the user is being invited and the name of the community admin who invited the guest. To accept the invitation and access the Viva Engage community, the guest must select **Go To Community** in the email.

4. Use the network switcher in the suite header to switch between the home Viva Engage network, any external Viva Engage communities where the user is a guest, and external networks.

    :::image type="content" source="../media/azure-ad-b2b-guests-engage-network-switch.png" alt-text="Screenshot of globe icon for switching networks.":::

5. Everyone in the Viva Engage community can easily identify who is a guest. An "external" badge appears next to the guest in Viva Engage community posts, comments, the community membership page, and search results. A Viva Engage community with guests also has a globe icon next to it.

    :::image type="content" source="../media/engage-aad-b2b-externaluser-post.png" alt-text="Screenshot showing a post from an external user.":::

    The Viva Engage community with guests has a globe icon next to it.

    ![Screenshot showing external community with a globe icon.](../media/azure-ad-b2b-guests-engage-network-switch.png)

6. Guests can leave the Viva Engage community at any time by hovering over the "Joined" button in the community header.

    :::image type="content" source="../media/engage-aad-b2b-external-community-leave.png" alt-text="Screenshot showing the button to leave an external community.":::

    > [!NOTE]
    > Leaving the Viva Engage community doesn't remove the guest account from your organization's directory. That must be done by a Microsoft 365 global admin or an Azure AD admin.

## Guest capabilities and limitations

Following is a list of limitations that apply to Azure AD-B2B guests in Viva Engage communities.

- Guests can't discover communities. Guests can access only the communities that they're invited into.

- Guests can't create new communities.

- Guests can't be a community admin and can't change community settings.

   Settings that guests can't change include:
  - Add new members to the community and removing membership
  - Promote and demote community owners
  - Edit community info
  - Add related groups
  - Add connectors
  - Add pinned files or links (guests can view pinned files and links)
  - View community or group insights

## Licensing for guest access

Guest access is included with all Microsoft 365 Business Standard, Microsoft 365 Enterprise, and Microsoft 365 Education subscriptions. No other Microsoft 365 license is necessary. Viva Engage doesn't restrict the number of guests you can add. However, the total number of guests that can be added to your tenant may be restricted by the paid features of Azure AD. For more information, see [Billing model for Azure AD External Identities](/azure/active-directory/external-identities/external-identities-pricing).

## What features aren't supported for guests?

We're working hard to bring all Viva Engage functionality to the new B2B guests in Viva Engage. Here's the list of features still in development:

- **Personal email, non-Microsoft 365 business email, and phone number-based legacy accounts** – Users with Microsoft 365 Business email accounts can be added as guests. Other email domains like Gmail and Yahoo mail aren't yet supported. 
- **Cross-Geography guests** – Currently, organizations can host Viva Engage in two data centers, Europe and North America. Users can add guests from the same geography. Check [the Yammer public roadmap](https://go.microsoft.com/fwlink/?linkid=2132131) to see timelines for cross-geography support.

- **Private messages** – Private messages are disabled for B2B guests in Viva Engage.
- **Live events** – Currently, guests can't participate in live events because guests aren't yet supported by Microsoft Stream. To learn when these features may become available, see the [Microsoft 365 roadmap](https://go.microsoft.com/fwlink/?linkid=2132131).
- **Add guests during community creation** – Community owners can invite guests by using the edit membership flow for any community. In the current release, community owners can't add guest email addresses at the time of community creation.
- **Interactive Viva Engage email notifications in Outlook** – B2B guests continue to receive the legacy email notifications from the communities that they're added to as guests instead of the new interactive email notifications. In the communities where these users aren't guests, the interactive email notifications work as expected.
- **Addition of guests to the All Company community** – Guests can't be added to the All Company community.

## Frequently asked questions

**Q: Is the Azure AD-B2B guest experience in Viva Engage available for customers that have a Viva Engage network with EU data residency?**
A: Yes!

**Q: Can we invite Azure AD-B2B guests to Viva Engage External Networks?**

A: AzureAD-B2B guests can't be invited to Viva Engage External Networks. External Networks continue to work as is with Viva Engage guest access.

**Q: Are Viva Engage guest settings aligned to Microsoft 365 Groups settings?**

A: Yes. With Native Mode for Microsoft 365 for Viva Engage, all communities and users are supported via Microsoft 365 Groups. The Azure AD guest settings for Microsoft 365 Groups now also apply to Viva Engage communities.

**Q: Can Viva Engage enable dynamic membership groups to include guests from a domain?**

A: Yes. Admins can create dynamic membership rules for guests in a Viva Engage community via the Azure portal. Here's an example: **user.userType -eq "Guest"** and user.email **-contains "@xyz.com"**. This rule adds all guests from the domain xyz.com to the specified Viva Engage community.

**Q: I don’t want to allow guests in the Viva Engage communities of our network. How do I disable guests from participating in our communities?**

A: Viva Engage relies on and is based on the [external collaboration settings](/azure/active-directory/external-identities/delegate-invitations) of Azure AD. We recommend that you use Azure AD controls to configure external collaboration settings.

To prevent guests from being added to Viva Engage communities but allow them to access the rest of Microsoft 365 apps, access the external messaging security settings described earlier in this article to deny community admins from adding guests.

> [!NOTE]
> When you deny guests from being added to Viva Engage communities, community admins can't add any new guests to Viva Engage communities. But existing guests aren't removed from Viva Engage communities.

## Related articles

[Viva Engage admin Help](./admin-key-concepts.md)

[Native Mode for Viva Engage](./overview-native-mode.md)


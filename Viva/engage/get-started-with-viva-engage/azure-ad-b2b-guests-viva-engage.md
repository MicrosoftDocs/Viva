---
title: "Work with AzureAD-B2B guests in Viva Engage communities"
f1.keywords:
- NOCSH
ms.author: elizapo
author: Starshine89
manager: elizapo
ms.date: 09/22/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
description: "Learn more about working with Microsoft Entra B2B guests in Viva Engage communities."
---

# Work with Microsoft Entra B2B guests in Viva Engage communities

The Viva Engage guest feature allows organizations to call in experts such as vendors, suppliers, or consultants from outside the organization to supercharge collaboration. Viva Engage networks aligned to Native Mode use the Microsoft Entra Business-Business (Microsoft Entra B2B) guest framework to power guests. Microsoft Entra B2B is a secure, compliant external collaboration framework. Many apps in the Microsoft 365 suite use Microsoft Entra ID (for example, Microsoft SharePoint, Microsoft Outlook, and Microsoft Teams).

Any Microsoft 365 user who isn't part of your organization can be added as a guest to a Viva Engage community by a Community admin. Microsoft Entra B2B guests in Viva Engage communities are covered by the same compliance and auditing protection as the rest of Microsoft 365 and can be managed within Microsoft Entra ID. Guest access is subject to Microsoft Entra ID and Microsoft 365 service limits.

## Prerequisites for adding an external user as a Microsoft Entra B2B guest to a Viva Engage community

Align your Viva Engage network to native mode before inviting an external user as a Microsoft Entra B2B guest to a Viva Engage community. Inviting a guest requires that you configure settings in Viva Engage and other Microsoft 365 services, including settings in Microsoft Entra ID, Microsoft 365 Groups, and SharePoint.

If your organization is ready to start inviting guests to Viva Engage communities, then configure the following settings.

Viva Engage network admins need to enable guest access on their networks from **Viva Engage network admin settings > Security settings > External Messaging**.

>[!NOTE]
>If your network was provisioned after December 15th, 2020, Microsoft Entra B2B guest functionality is enabled by default for your organization.

> [!div class="mx-imgBorder"]
> :::image type="content" source="../../media/yammer-adminpanel-externalusers-allowdeny.png" alt-text="Screenshot of guest settings in the Viva Engage admin center.":::

This setting is a Viva Engage network-wide setting. Enabling guest access lets community admins add guests to any Viva Engage community in the network. You can control guest access to individual Viva Engage communities [by using sensitivity labels](/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).

External collaboration is a key ingredient for the success of any organization. The guest feature allows you to call in experts, such as consultants or vendors, from outside your organization. Users can invite guests to a community and quickly start a rich conversation by sharing access to community resources like files. This ease-of-use makes external collaboration one of the most used features in Viva Engage today.

:::image type="content" source="../../media/yammer-b2b-azure-guests.png" alt-text="Screenshot of the Viva Engage business-to-business guest support.":::

To configure Microsoft Entra ID, Microsoft 365 Groups, and SharePoint settings, see [Collaborate with guests in a team](/microsoft-365/solutions/collaborate-as-team).

## How to invite an external user as guest to a Viva Engage community

1. A community admin can add a guest to a Viva Engage community by entering the email address of the guest in the **Add Member** panel of the community.

2. The guest receives a welcome email message. This message includes information about the Viva Engage community and Viva Engage network to which the user is being invited, and the name of the community admin inviting the guest. The guest must accept the invitation by selecting **Go To Community** in the email message before accessing the Viva Engage community.

    :::image type="content" source="../../media/yammer-aad-b2b-external-message.png" alt-text="Screenshot of the Viva Engage Microsoft Entra B2B external message.":::

3. By visiting the **Go to Community** link, the guest accepts the invitation. After a guest accepts the invitation, they can participate in the Viva Engage community.

    >[!NOTE]
    >External users must accept guest invitations on the desktop app or in a web browser. This functionality isn't currently supported on mobile devices (Android or iOS).

4. Network switcher located in the suite header can be used to switch between the home Viva Engage network, any Viva Engage networks the user is a guest in, and external networks.

    :::image type="content" source="../../media/yammer-aad-b2b-external-globe.png" alt-text="Screenshot of globe icon for switching networks.":::

5. Everyone in the Viva Engage community can identify easily who is a guest. An External badge appears next to the guest in Viva Engage community posts, comments, community membership page, and search results. The Viva Engage community with guests has a Globe icon next to it.

    :::image type="content" source="../../media/yammer-aad-b2b-externaluser-post.png" alt-text="Screenshot showing a post from a guest.":::

    The Viva Engage community with guests has a Globe icon next to it.

    :::image type="content" source="../../media/yammer-aad-b2b-external-globe.png" alt-text="Screenshot showing external community with a globe icon.":::

6. Guests can leave the Viva Engage community at any time by hovering over the **Joined** button in the community header.

     :::image type="content" source="../../media/yammer-aad-b2b-external-community-leave.png" alt-text="Screenshot of the button that lets you leave an external community.":::

    > [!NOTE]
    > Leaving the Viva Engage community doesn't remove the guest account from your organization's directory. This must be done by a Microsoft Entra administrator.

## Guest capabilities and limitations

The guest experience has limitations by design. Following is a list of limitations that applies to Microsoft Entra B2B guests in Viva Engage communities.

- Guests can't discover communities. Guests can access only the communities that they're invited into.

- Guests can't create new communities in the network they're invited to.

- A guest can't be a community admin, nor can they change community settings like these:
  - Adding new members to the community and removing membership
  - Promoting and demoting the owners
  - Editing community info
  - Adding related groups
  - Adding connectors
  - Adding pinned files or links (they can view the pinned files and links)
  - Viewing community or group insights

## Licensing for guest access

Guest access is included with all Microsoft 365 Business Standard, Microsoft 365 Enterprise, and Microsoft 365 Education subscriptions. No other Microsoft 365 license is necessary. Viva Engage doesn't restrict the number of guests you can add. However, the paid features of Microsoft Entra ID restrict the total number of guests you can add to your tenant. For more information, see [Billing model for Microsoft Entra External ID](/azure/active-directory/external-identities/external-identities-pricing).

## What features aren't supported for Guests?

We're working hard to bring all Viva Engage functionality to the new B2B guests in Viva Engage. Here's a list of features that are in progress:

- **Personal email, non-Microsoft 365 business email, and phone number-based legacy accounts** – Users with Microsoft 365 Business email accounts can be added as guests. Email domains like Gmail and Yahoo mail aren't supported in this release.
- **Private messages** – Private messages are disabled for B2B guests in Viva Engage.
- **Live events** – Guests can't attend live events.
- **Adding guests during community creation** – Community owners can invite guest users by using edit membership flow for any community. In the current release, community owners aren't able to add guest emails at the time of community creation.
- **Interactive Viva Engage email notifications in Outlook** – Interactive email notifications for B2B guests users aren't available in this preview. B2B guests can expect to receive the legacy email notifications from the communities that they're added to as guests, instead of the new interactive email notifications. In the communities where these users aren't guests, the interactive email notifications function as expected.
- **Addition of Guests to the All Company community** – Guests can't be added to the All Company community.

## FAQ

**Q: Is the Microsoft Entra B2B guest experience in Viva Engage available for customers who have a Viva Engage network with EU data residency?**

A: Yes!

**Q: Can we invite Microsoft Entra B2B guests to Viva Engage External Networks?**

A: Microsoft Entra B2B guests can't be invited to Viva Engage External Networks. External Networks work as-is with Viva Engage guest access.

**Q: Will Viva Engage guest settings be aligned to Microsoft 365 Groups settings?**

A: Yes. With Native Mode for Microsoft 365 for Viva Engage, all communities and users are supported via Microsoft 365 Groups. The Microsoft Entra guest settings for Microsoft 365 Groups apply to Viva Engage communities.

**Q: Can Viva Engage have dynamic membership groups include guests from a domain?**

A: Yes. Admins can create dynamic membership rules for guests in a Viva Engage community through the Azure portal. An example is: user.userType -eq "Guest" and user.email -contains "@xyz.com" - this rule adds all guests from the domain xyz.com to the specified Viva Engage community.

**Q: I don’t want to allow guests in the Viva Engage communities of our network. How do I disable external users from participating in our communities?**

A: Viva Engage relies on and builds upon the [external collaboration settings](/azure/active-directory/external-identities/delegate-invitations) offered by Microsoft Entra ID. We recommend that you use Microsoft Entra ID controls to configure external collaboration settings.

You can prevent guests from being added to Viva Engage communities while allowing them to access the rest of Microsoft 365 apps. To deny community admins from adding guests, go to the Viva Engage Network admin settings > **External messaging security**.

> [!NOTE]
> When you deny external users from being added to Viva Engage communities, community admins won't be able to add any new external users to the Viva Engage communities. Existing external users won't be removed from Viva Engage communities.

**Q: Does the Microsoft Entra B2B guest experience allow cross-geo guest access?**

A: Yes. Microsoft Entra B2B guests from another Geo can be invited to a Viva Engage network in Native mode. However, if a tenant migrates to another geo, the existing guest access doesn't automatically change to cross-geo guest access. All guest access must be renewed (that is, the host must issue new invites and guests must accept them) after a cross-geo tenant migration.

## Related articles

[Viva Engage admin Help](./admin-key-concepts.md)

[Native Mode for Microsoft 365 for Viva Engage](../overview-native-mode.md)

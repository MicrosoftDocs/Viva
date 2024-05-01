---
title: "External messaging in Viva Engage - Frequently asked questions"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 7/11/2023
audience: Admin
ms.topic: reference
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 35b59d6c-bb1c-4541-bf19-9f67d2f2b199
description: "Find answers to questions about adding external participants to your Viva Engage network, and related questions about permissions, security, and opting out of external messaging."
---

# External messaging in Viva Engage - Frequently asked questions

You can include people outside of your Viva Engage network in your conversations and private messages that are posted in external groups. You add people as external participants, and they can reply to messages and posts in your Viva Engage network without having to join. 
  
Find answers to frequently asked questions about external participants in this article.
 
>[!NOTE] 
>External messaging, including exernal networks, external groups, and external participants, is not available for Viva Engage Enterprise networks in the [EU Geo](../manage-security-and-compliance/data-residency.md).
    
## General questions
<a name="General"> </a>

### Q: What's the difference between external participants and external networks?

A: External networks are great for hosting external communities and managing long-term projects. The external participants feature is meant for one-off, short-term communications, which don't warrant the need of provisioning a new network.
  
### Q: Can I invite external participants to my Viva Engage groups?

A: You can [create external groups in Viva Engage](create-and-manage-external-groups.md) and invite external participants to those groups. 
  
### Q: What happens when I remove an external participant?

A: When you remove someone from a Viva Engage conversation, it removes the entire conversation from their Viva Engage inbox, and they can no longer access it.
  
The user that added the external participant can remove them from the conversation. In addition, both network and group admins can remove users from conversations.
  
### Q: What happens if I accidentally add an external participant to the conversation?

A: You can remove the external participant by selecting **Remove Participant** on the system-generated comment that announces that participant has been added to the thread. For more information, see [Add external participants to your Viva Engage conversations](add-external-participants.md).
  
### Q: What happens if I select "Stop following in inbox" for an external message?

A: The message is removed from your inbox.
  
### Q: Do Viva Engage users who unsubscribe from email notifications receive an invitation when they've been added to a conversation?

A: No.
  
### Q: What if I add an external participant who isn't a Viva Engage user?

A: If you add someone and they aren't a Viva Engage user, they receive a copy of the message in their email inbox. They also receive an invitation to join their Viva Engage network.
  
### Q: Can I add a user with a personal email address (like Hotmail or Gmail) to a Viva Engage conversation with External Messaging?

A: No. You must invite people using their company or work email address.
  
### Q: Does a pending Viva Engage user who's been added to a conversation receive an email to join Viva Engage?

A: Yes.
  
### Q: Can I see external participants in my type-ahead search box when I create or reply to a message?

A: After an external participant has been added to a conversation, their name appears in the type-ahead search. Their name appears higher or lower on the suggested list depending on how frequently you communicate with that person on Viva Engage. Because of permission restrictions (which depend on the privacy settings of a group and whether the participant is internal or external), the type-ahead search experience varies. The following table explains the permissions and experience for type-ahead search with external participants:
  
|**Situation**|**Experience for internal members**|**Experience for external participants**|
|:-----|:-----|:-----|
|An external participant is added to a conversation in a public group.  <br/> |Type-ahead search includes the external participant for all members of the network.  <br/> |Type-ahead search is limited to participating members in the conversation.  <br/> |
|An external participant is added to a conversation in a private group.  <br/> |Type-ahead search includes the external participant for all members belonging to that group.  <br/> |Type-ahead search is limited to participating members in the conversation.  <br/> |
|An external participant is added to a private message.  <br/> |Type-ahead search is limited to participants in the private message.  <br/> |Type-ahead search is limited to participants in the private message.  <br/> |
|A public group is made private.  <br/> |Type-ahead search includes the external participant for all members of the network.  <br/> |Type-ahead search is limited to members that have participated in the conversation the external participant has been invited to join.  <br/> |
|A private group is made public.  <br/> |Type-ahead search includes the external participant for all members of the network.  <br/> |Type-ahead search is limited to members that have participated in the conversation the external participant has been invited to join.  <br/> |
   
## Permissions and security questions
<a name="Security"> </a>

### Q: How can I protect against risk and maintain our privacy?

A: Privacy and security are important to us, too. We've invested in building tools to monitor and proactively protect your company's IP and employees. As part of External Messaging, we've built these security features:
  
- **Clear UI warnings:** Warnings ensure that users are consciously aware before they add an external participant. When you add an external participant to a conversation or reply to a conversation with an external participant, a clear warning appears in the UI. See [Add an external participant](add-external-participants.md#AddExternal).
    
- **Disable external messaging:** [Verified admins](../manage-viva-engage-users/manage-viva-engage-admins.md) can use these options to turn off external collaboration.  See [Disable external messaging](disable-external-messaging.md).
    
- **Remove users:** You can remove external participants from a conversation. Once removed, a user can't view that conversation anymore. Both network and group admins can remove users from conversations. See [Remove an external participant from a conversation](add-external-participants.md#RemoveExternal).
    
- **Data export:** Viva Engage verified admins can keep track of all conversations and files that include external participants and monitor conversations their users are having outside of your network. See [Find external participants in a Viva Engage network](find-external-participants.md).
    
- **Keyword monitoring:** Viva Engage verified admins can set up keyword monitoring to alert admins of potential breaches. See [Monitor Keywords](../manage-security-and-compliance/manage-data-compliance.md#MonitorKeywords)
    
### Q: When I add an external participant to a conversation, what can they see?

External participants can only see conversations that they have been explicitly invited to. They can see anything included on that conversation—for example, a file that has been uploaded. But they can never find or join another conversation on your network without an explicit invitation.
  
### Q: Can external participants upload files to the conversation?

A: Yes.
  
### Q: Can external participants invite other participants as well?

Yes, external participants can add others to the conversation, just as they can @-mention people in that conversation. They can only invite people to conversations they have already been explicitly included on.
  
### Q: What information can external participants see about me?

A: External participants can only see a limited view of your hover card. Fields listed on the hover card include your name, title, email address, and network. Your profile picture, phone number, and more remain hidden to external participants.
  
### Q: What permissions do external participants have for content that is uploaded to a conversation?

A: External participants can view and download files. External participants can only view notes.
  
### Q: Can an external participant share this conversation?

A: No. Because permissions restrict the audience to privileged members, external participants must be added individually to the conversation.
  
### Q: Where does the data for external participants live?

A: The conversation data is available to [verified admins](../manage-viva-engage-users/manage-viva-engage-admins.md) (by using data export) of any participant on the conversation. So if your employee is participating in a conversation on another network, because that conversation shows up in their inbox, it's available in your network's data export. For more information, see [Find external participants in a Viva Engage network](find-external-participants.md).
  
### Q: When I add an external participant to a conversation do they enter my network?

A: No. External participants can only participate in conversations they have been explicitly invited to. They access these conversations via their Viva Engage inbox (on their network). They have no access to the rest of your network.
  
### Q: What rights do verified admins have?

A: [Verified admins](../manage-viva-engage-users/manage-viva-engage-admins.md) can remove all external participants from any conversation any time. They can also see which files and conversations are accessible to external participants by using data export. For more information, see [Find external participants in a Viva Engage network.](find-external-participants.md)
  
### Q: If I have keyword monitoring in place, does it apply to messages that external participants post in my network?

Yes. Keyword monitoring applies to any posts in your network, including those from external participants.

  
## Related articles

[Add external participants to your Viva Engage conversations](add-external-participants.md)
  
[Create and manage external groups in Viva Engage](create-and-manage-external-groups.md)
  
[Find external participants in a Viva Engage network](find-external-participants.md)
  
[Disable external messaging in a Viva Engage network](disable-external-messaging.md)

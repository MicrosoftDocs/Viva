---
title: "Disable external messaging in a Viva Engage network"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 7/13/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: f8fd6403-c8f3-4307-9230-65304d6000d9
description: "Disable external messaging, with options for preventing external users in groups and conversations, and preventing users from joining a Viva Engage network in another organization."
---
# Disable external messaging in a Viva Engage network

For Viva Engage Enterprise networks in the US Geo, users can add external participants to their Viva Engage conversations and Viva Engage groups. Also, members of your Viva Engage network can participate in another company's Viva Engage network, if invited. You can turn off this external collaboration, if needed.

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.
    
2. In the **External Messaging** section, select the option that makes sense for your organization: 

     -  **Allow users in this network to participate in groups or conversations in other networks, and allow external users to participate in groups or conversations in this network.**    
   
     - **Allow users in this network to participate in groups or conversations in other networks, but don't allow external users to participate in groups or conversations in this network.**     
   
     - **Don't allow users in this network to participate in groups or conversations in other networks, and don't allow external users to participate in groups or conversations in this network.**

 ## What each option does

| Option | Users can participate in other networks <sup>1</sup> | External participants can participate in groups and conversations <sup>2</sup> |
|--------|-------------------------------|----------------|
|**Allow users in this network to participate in groups or conversations in other networks, and allow external users to participate in groups or conversations in this network.**| Yes | Yes|
|**Allow users in this network to participate in groups or conversations in other networks, but don't allow external users to participate in groups or conversations in this network.** | Yes | No|
|**Don't allow users in this network to participate in groups or conversations in other networks, and don't allow external users to participate in groups or conversations in this network.**| No | No|

1. When you prevent users from being able to participate in other networks:

    - Users are blocked from receiving invitations from Viva Engage networks on other domains.

2. When you disable external access to your groups and conversations:

    - When a user tries to add an external participant in Viva Engage, the user receives an error message stating that they are unable to add external participants because it violates their company's policy. The user will not be allowed to post the message. 

    - Any current external participants are blocked from using external conversations or threads that they may have been participating in.

    - No new external groups can be created. 

 
## Related articles

[Add external participants to your Viva Engage conversations](add-external-participants.md)
  
[Find external participants in a Viva Engage network](find-external-participants.md)
  
[External Viva Engage participants FAQ](external-messaging-faq.md)

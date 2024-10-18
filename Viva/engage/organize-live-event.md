---
title: "Organize a Viva Engage live event"
description: "Learn what's needed for group admins to host live video events for Viva Engage users."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 10/17/2023
audience: Admin
ms.topic: overview
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
ms.collection:
- m365solution-spcomms
- m365solution-scenario
- highpri
search.appverid:
- MET150
---

# Organize a Microsoft Teams powered live event in Viva Engage 

Microsoft Viva Engage uses Microsoft Teams to process and record video for all live events. To understand how Viva Engage and Teams work together, see [Overview of live events](/microsoftteams/teams-live-events/what-are-teams-live-events).

This article provides guidance for Viva Engage group admins to produce the best live event experiences for their groups and communities. If you're planning a large event (up to 100,000 attendees), the Microsoft 365 live events assistance team can give you the best options for your live event. [Learn more about this program.](https://adoption.microsoft.com/virtual-event-guidance/assistance)

> [!NOTE]
> Starting January 31, 2024, Microsoft Stream events are unavailable. Use [Microsoft Teams live events](/microsoftteams/overview-meetings-webinars-town-halls) to schedule events.

### Choose a setup that works for your live event

The size and complexity of your live event determines whether you create the event in Viva Engage or in Microsoft Teams. Review these descriptions to determine which one best fits your needs. 

> [!IMPORTANT]
> When setting up a live event, we recommend that you configure your video, community, and user permissions at least 24 hours before the event for the best experience. This includes such settings as adding users, updating video permissions, and changing a community from private to public. It can take up to two hours for certain changes to propagate across Microsoft Teams and Viva Engage. Allowing 24 hours or more can provide time for testing and adjusting if needed.

- **Microsoft Teams QuickStart**

  Use this method used to produce simple live events. All you need to have are the audio and video devices connected to the presenter’s computer. This setup is great when you've invited a remote presenter for the event.

  - Teams encodes the broadcast stream.
  - Content shared from the presenter’s webcam and screen is shared across Teams.
  - Attendees can view the event on Viva Engage.
  - Video is stored in the SharePoint library connected to the Viva Engage community where the live event was produced. The video is displayed on the Viva Engage event page for 180 days after the event is over.

- **Teams external app or device**

  This type of production is best for large-scale events, such as executive town halls. Here, a single stream from a media mixer is broadcast to the audience. 
    - Teams broadcasts the live event 
    - Requires an external encoder (app or device) to produce the event 
    - Attendees can view the event in Viva Engage. 
    - Video is stored in the SharePoint library connected to the Viva Engage community where the live event was produced. The video is displayed on the Viva Engage event page for 180 days after the event is over.


## Review licenses and permissions

As a live event organizer, make sure that you and your audience have the necessary licensing and permissions to participate in live events.

### Create and schedule a live event

- You must be an admin in the Viva Engage group or community in which you create and schedule the event. 
- You must own a Teams license and set up specific policies. For details, see [Who can create and schedule live events in Teams](/microsoftteams/teams-live-events/plan-for-teams-live-events) and [Set up live events policies](/microsoftteams/teams-live-events/set-up-for-teams-live-events#step-3-set-up-live-events-policies). 
 
- You must be an admin to assign roles for the live event (producers, presenters, and so on). Only assigned roles receive an invite, allowing them to join the event through a link. Learn more about [roles assigned through Teams](https://support.microsoft.com/office/schedule-and-produce-a-live-event-in-new-yammer-using-teams-d891bff6-eda2-493f-8b0d-d87932e7937d#roles) or through an [external app or device](https://support.microsoft.com/office/schedule-and-produce-a-live-event-in-new-yammer-using-an-external-app-or-device-975f596a-8fc5-4400-8bf5-7ec77ec18415#roles).

- Co-producers and presenters that you assign must also have a Teams license and Teams must be enabled. (Select the Microsoft 365 app launcher and look for a Teams icon.) 

- Your public or private group must be connected to Microsoft 365 and **Enforce Office 365 identity** setting must be selected for the organization. To restrict attendance to members only, use a private community. Non-members can attend and participate in live events scheduled in a public community.  

For more information, see [Enforce Office 365 identity for Viva Engage users](/yammer/configure-your-yammer-network/enforce-office-365-identity) and Viva Engage and Microsoft 365 groups. 
 
#### Attend a live event

- Attendees must have a Microsoft 365 or Office 365 plan that includes a license for Viva Engage and Microsoft Teams (for example, Office 365 A3, A5, F1, E1, E3, or E5).
- You must be a member of the Viva Engage network in which the event is hosted to attend a live event in a public group. **Guests and external users have no access to live events.**
- You must be a member of the private group in which the event is hosted to attend a live event in a private group.


## Configure video and permissions in advance
Before you can create a live event, you must configure video, community, and user permissions. Tasks you may need to complete include adding users, updating video permissions, and changing a community from private to public. Permissions take up to two hours to propagate across Teams and Viva Engage.

We recommend that you configure these settings at least 24 hours in advance to allow time to test and adjust your settings.   

## Learn by creating a test event
Let your first live event be a kind of dress rehearsal for the real thing. A practice session helps you and your team members get comfortable with your responsibilities and what needs to happen. This is especially important when you’re producing live events that broadcast to thousands of people. 

Enlist helpers for the key roles: organizer, presenter, and attendee. If you produce events through an external app or device, include someone on the AV staff to run the mixer to provide the encoder information. Consider creating a separate Viva Engage community of your volunteers specifically for the test. 

 
## Restrict creation of live events in Viva Engage

You can prevent the creation of live events produced in Teams, live events produced with other tools, or both.

- To prevent creation of live events produced in Teams, remove permissions in Teams for live event scheduling. That way, unlicensed and unauthorized users won't have the produce in Teams option if they try to create a live event in Viva Engage.

## FAQ

**Q: Can I create a live event in All Company?**

If your network’s All Company community is a Microsoft 365 connected group, then you can host events in this community. All Company functions like other Viva Engage communities.

**Q: How many attendees can view a live event at once?**

A. Currently, the limit is 10,000 attendees. For larger attendee sizes, contact the Microsoft 365 [Live Events Assistance Program](https://adoption.microsoft.com/virtual-event-guidance/assistance/).

**Q: What media player is used for live events?**

The new live events are broadcast using the Teams media player and can be viewed live or on-demand on the Viva Engage web and mobile apps (iOS and Android).

**Q: Why can't I view the video?**

To maintain the privacy of live event content, only authorized users can join a live event and are authenticated as they load the live event page. Authentication must be successful for video to be viewable. Use your browser's settings to make sure that cookies are enabled and that any extensions that block tokens are disabled. After changing the settings, refresh the event page.

**Q: Where are the videos stored once they are produced?**

The Video-on-Demand is stored in the SharePoint Community where the event was hosted and is automatically shared with members of the private community. If the event was produced in a public community, the video is shared with everyone across the Viva Engage network.

**Q: Can Event Producers edit videos?**

Yes, the videos can be edited in SharePoint. The edited video in SharePoint is automatically updated for attendees to watch. It can take up to 10 minutes before producers can edit their videos after the event is completed.

**Q: What happens to the old live events videos that were produced using Microsoft Stream?**

For now, attendees can watch live events videos that were created using Stream on Microsoft Stream. However, we recommend that you [migrate Stream videos to SharePoint](/stream/streamnew/stream-classic-to-new-migration-overview).

**Q: How can I cancel a scheduled live event?** 

1.  In Viva Engage, go to the group page to view the event. 
2.  In the Group Events section, select the event, and then select Cancel Event.  
>[!Tip] 
>If the event announcement has been live for a while, post a message in the community saying that the event was cancelled. If you sent out a calendar invite, send out a cancellation.

**Q: Can our event team moderate the conversations, or will all attendees see all the questions?**

All questions and conversations are visible within the Viva Engage community. 

**Q: Do I have to create a transcript or does the tool transcribe the video? How does closed captioning work after the event?**

Teams powered AI closed captioning is available in real-time during and after the event is over.

**Q: Can the landing page for the event be customized?**

You can edit the title, description, date, and time for the event landing page. The landing page includes the recording after the event has occurred.

**Q: What are good ways to promote an event?**

Include the link from the event page in your Outlook emails and announcements when you invite attendees to join your event.

- For public communities, post an announcement in the community with a link to the event page. For wider reach, you can also post an announcement in the All Company community.

- For private communities, post an announcement in the community with a link to the event page.

- For all communities, pin announcements to the top of the community feed.


## Related articles

[Organize a live event in Viva Engage](https://support.office.com/article/organize-a-live-event-in-yammer-105dd7af-9caf-4a5e-8a44-56d203e96551)

[Microsoft Teams lives events overview](https://support.office.com/article/get-started-with-microsoft-teams-live-events-d077fec2-a058-483e-9ab5-1494afda578a)

[Get help producing a live event](https://support.office.com/article/0cedb557-cbe4-40d3-8147-112633f087eb)


---
ROBOTS: NOINDEX,NOFOLLOW
title: Network in Viva Insights
description: Use the Network page in the Microsoft Viva Insights app to help you understand who you collaborate with most often
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Network

Use the **Network** page in Microsoft Viva Insights to understand who you collaborate with most and when. On this page, you'll find:

* Suggested important contacts, along with tips to improve connections with existing important contacts.
* A map view of your top collaborators, which provides details about the important people in your network.
* Your collaboration habits.

You can get to the **Network** page from your **Teamwork** tab in the Viva Insights app in Teams and web. Under the **Build better relationships** section, in the **Time spent collaborating with others** card, select **View my network**.

:::image type="content" source="images/teamwork-ic3.png" alt-text="Screenshot that shows a Suggested important contact card with a profile image and name at the top and Pin button and Next person link at the bottom." lightbox="images/teamwork-ic3.png":::

Now, let's discuss the **Network** page's two sections: **Collaborators** and **Communication habits**.

## Collaborators

If you hold a meeting or exchange email, chats, or calls with coworkers, Viva Insights considers those coworkers *collaborators*. 

You'll notice two kinds of collaborators on the **Network** page:

* *Important collaborators* – Coworkers you've marked as important in Viva Insights. Marking people as important (or "pinning" them) helps you keep up with their requests in **Suggested tasks** and find them quickly on your collaboration map. We discuss pinning contacts a little [later](#to-edit-your-important-people-list) in this article.
* *Active collaborators* – Coworkers you've collaborated with in the past four weeks.

### About the collaboration map

The **Collaborators** section arranges your active collaborators in a three-ring map view—from **Most frequent** to **Least frequent** collaboration time. Viva Insights estimates total collaboration time based on the number of hours and minutes you've spent collaborating with a contact, both during and outside of your working hours, over the past four weeks.  

If you want more information about how much time you’re spending with a contact, select their profile image. The tooltip shows you your total collaboration time with that contact, and then breaks down collaboration time by each communication channel—emails, meetings, and chats and calls.

:::image type="complex" source="images/teamwork-network-small.png" alt-text="Screenshot that shows Collaborators section on the Teamwork tab." lightbox="images/teamwork-network-expanded.png":::
   Screenshot of the "Collaborators" section of the Network page. The subtitle reads, "Who did you work closely with in the last 4 weeks?". The image is arranged as a map, with the user's profile picture on the far left of the image, and collaborators they've recently worked with in three semi-rings. These rings go from "Most frequent" closest to the user's image to "Least frequent" on the right side of the image. The image shows hovering over a collaborator in the "Most frequent" ring. A card beneath this collaborator's profile image shows their name, a star to indicate they're an important contact, and how much total time the user has spent collaborating with them. Below the total collaboration time, the card lists how much time this collaborator has worked with the user by communication each channel: over email, in meetings, and in chats and calls.
:::image-end:::

### To edit your important people list

#### Add

You can add someone to your important people list in a couple of ways:

* At the top of your **Network** page, you might notice they're a suggested contact. To add them to your important list, select the **Pin** button.

     :::image type="content" source="images/teamwork-suggested-important-contact.png" alt-text="Screenshot that shows a Suggested important contact card with a profile image and name at the top and Pin button and Next person link at the bottom.":::

* If the person you want to pin isn't suggested, use the search bar just above your collaborator map. Type in their name, and then select **Pin**.

After you mark a contact as important, and if they're also an active collaborator, they'll show up in your map with a star next to their name. If an important contact isn't an active collaborator, you'll still get their tasks prioritized in [Suggested tasks](suggested-tasks.md). If you search for them in the **Collaborators** section, they'll show as pinned.

#### Remove

To remove someone from your important people list, select the **Unpin** icon, which looks like a star on the collaboration map. To quickly find a contact, use the search bar.

>[!Tip]
>Here are a couple tips to keep your network up to date:
>
> * Keep adding top collaborators to your important people list, and remove some if you need to. Things change, so you want to make sure the folks in your list reflect the time you spend working with them.
>
>* Make time for networking. Making time to foster relationships and grow your network has proven to contribute to professional advancement. A team partner study showed a correlation between successful salespeople and large networks. The top salespeople boasted internal networks that were 33% larger than those who performed below average. In this case, an investment in meaningful coworker relationships translated to higher performance

 
## Communication habits

**Communication habits** shows how you communicate with people in your network. We break up your total communication over the last four weeks by communication type: emails sent, emails read, and chats and calls. On a graph, you'll find a distribution of communication throughout your day—for example, your graph might show that you send most of your emails around 8am, but chat and call with colleagues around 3pm. Hover on each bar for a breakdown of collaboration activity by hour.

:::image type="complex" source="images/teamwork-communication-habits1.png" alt-text="Screenshot that shows Communication habits section on the Teamwork tab." lightbox="images/teamwork-communication-habits1.png":::
   Screenshot of the "Communication habits" section of the Teamwork tab. The subtitle reads, "How connected are you with people in your network?" and contains a "Learn more" link. Below the subtitle, there's a section that contains a bar graph. To the left of the graph, there's a subsection titled, ""Your habits in the last 4 weeks," which contains three numbers arranged vertically. The first number's label reads, "Emails sent." The second number's label reads, "Emails read." The last number's label reads, "Chats and calls." The graph's Y axis goes from 0 - 75 in increments of 25. The X axis goes from 8:00 AM to 6:00 PM in increments of 2 hours. The graph's key corresponds to the section to the left: "Emails sent," "Emails read," and "Chats and calls." Each hour on the graph contains one stacked bar representing these three categories. The image shows a hover tooltip over 3:00 PM, which reports the exact number for each category in that hour. There's an "Is this helpful?" link in the bottom left corner, with "Yes" and "No" options.
:::image-end:::


### How Viva Insights calculates your communication habits

Let's discuss how Viva Insights arrives at the numbers you see in **Communication habits**.

#### Email  

**Emails sent** and **Emails read** estimate how much time you've spent sending and reading emails across all devices, like laptops and mobile phones. 

To figure out which emails to include in its **Emails read** calculations, Viva Insights uses an email's **To** and **Cc** lines. If you, or a group you're a member of, are on an email's **To** or **Cc** line, Viva Insights uses that email to calculate **Emails read**. Viva Insights *doesn't* use emails you delete without opening in its calculations.

##### Sending and reading time

For each email you *send*, Viva Insights assigns five minutes of sending time. For each email you *open*, Viva Insights assigns two and a half minutes of reading time.

However, in the following situations, Viva Insights assigns shorter times:  

* You send one email and then open or send another one within five minutes. In this case, Viva Insights assigns the time between the two actions to the *first* email (that is, the sent email).
* You open one email and then open or send another one within two and a half minutes. In this case, Viva Insights also assigns the time between the two actions to the first email (that is, the opened email).  

>[!Note]
>The time you spend sending or reading email outside your Outlook-defined working hours affects some insights you get on the **Wellbeing** tab.  

#### Chats and calls  

Your audio calls, video calls, and chats in Teams also count as collaboration activities. Here's how Viva Insights calculates those activities:

##### Chats

For each chat you *send*, Viva Insights assigns 30 seconds of sending time. Viva Insights doesn't assign any time for chats received, because the time you spend sending chats is a good indicator of how much time you spent in a chat conversation.

Viva Insights counts all chats you send within a 15-minute window as one chat.

>[!Note]
>Viva Insights doesn't use chats from Teams channels in its calculations.

##### Calls

For each call that isn't scheduled as a meeting on your calendar, Viva Insights uses the actual duration of the call. Viva Insights doesn't assign any time for calls scheduled as meetings in your calendar, because it's already counting those calls as meeting time. 

Learn more about how Viva Insights derives meeting insights in [Meeting habits](meeting-habits.md).

#### Insight calculation reference

|Insight | Time assigned|
|----|----|
|Emails sent| 5 minutes
|Emails read| 2.5 minutes
|Chats sent| 30 seconds
|Chats read| 0 seconds
|Unscheduled calls| Call duration
|Scheduled calls| 0 seconds

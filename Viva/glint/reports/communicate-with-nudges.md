---
ms.date: 03/29/2023
title: Communicate with Viva Glint Nudges
ms.reviewer: 
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Nudges are personalized email notifications designed to meet managers where they are in their flow of work. Team Summary is easily enabled from the Viva Glint admin dashboard, allowing program roles permissions to relevant reports."
---

# Communicate with Viva Glint Nudges

Microsoft Viva Glint Nudges is a system of intelligent, personalized email notifications designed to meet managers where they are in their flow of work. Nudges encourage managers to take simple steps to drive their team’s engagement and performance. Nudge notifications can include a link to the manager dashboard.

Who receives a Nudge is set up at the user role level. You're also able to determine which Nudges each User Role receives.
 
Nudges has filters to ensure they're only sent when relevant. If a user repeatedly doesn't open or interact with Nudge emails, they're automatically unsubscribed. 

## Nudges are sent on a recurring schedule

Recurring communications keep employees on track over time. Managers receive unique messages with each Nudge to keep the experience fresh, focused, and relevant. Nudges simplify key behaviors into lightweight, bite-sized steps and make action taking collaborative.

Notifications that survey results are ready for viewing aren't sent to managers of small teams or to managers who didn’t receive enough feedback to meet confidentiality thresholds. 

If a user is in multiple recipient groups, they may receive emails from either group depending on the cadence of each group and its next send date. Users are guaranteed to never receive more than one email per week. 

## Understand Nudge terminology

| **Term** | **Definition** | 
|---|---|
| **Recipient group** | Defines who receives Nudges and at what frequency |
| **Teammates** | This term has a different meaning dependent upon the employee role:<br>- Individual contributors: Managers + peers <br>- First-line manager: Manager + directs <br>- Manager of Mangers: Manager + direct |
| **Social proof** | Highlights others in your organization who have taken similar actions. Makes the process of action taking collaborative across teams. |

## How admins set up Nudges 

To set up Nudges, recipient groups must be created and enabled. Only one User Role can be selected per recipient group. You may create multiple groups to reach more User Roles or choose to send Nudges at a different frequency for each group.

From the Microsoft Viva Glint admin dashboard, select **Configure**, then  **Nudges**  in the  **Notifications** section. 

   > [!NOTE]
   >Nudge configuration may also be accessed via the Communications set up page in Program Summary for a specific survey.

### Add a new recipient group

There are several sections to set up.

### Recipients 

1. Select **+ New Recipient Group**.
1. Choose who will receive the Nudges: 
    1. User Role: Select a role from the dropdown menu. Add only one User Role per group. If you have one User Role that includes all managers, it reduces the number of recipient groups you need to create.
    2. Exclude: Select individual users or Distribution Lists from the search bar. A Distribution List must already be created for it to be available. 
    3. Recipient List: Download the list of recipients to a *.csv* file to have it for reference.  
    
### Timing

Defines when and how frequently users receive Nudges. Messages are sent between 8:00 am-12:00 pm in the recipient's time zone.

- Frequency: From the dropdown menu, choose to send Nudges from every one to eight weeks. Frequency can be adjusted after a survey launches.
  > [!TIP]
  >Send Nudges every two to four weeks.
  >Send Day: Choose a business day of the week.
  >Window: Select the number of days Nudge messages will send after a survey closes.  
  >Align Nudges to your survey cadence, i.e., 90 days for quarterly surveys, 180 days for biannual survey.
      
### Content 

Configure the emails that will be sent to your recipient group. 

Select the **Nudge #** to enable, disable, or preview. The corresponding slider window opens.

- Enable or disable by using ON and OFF. 
- Preview what your Nudge looks like: It includes your company logo, the survey name, highlight where the user is in the results process, and a link to view results.
- Results process: 
  - Nudge #1: Interpret results 
  - Nudge #2: Share with your team 
  - Nudge #3: Choose a Focus Area (or whatever term your organization uses) 
  - Nudge #4: Focus Area reminder 

### Advanced 

The following items can be enabled, disabled, or customized:  

- Social Proof: Manage by choosing one of the following: 
   - Include full names of teammates and aggregated data. For example, *Natalie Morris, Jacob Madsen, and 12 others are committed to Recognition*. 
   - Include only anonymized, aggregated data. As above but doesn't include names. For example, *14 others in your organization are committed to Recognition*.
   - Off: Disables this feature  

   > [!NOTE]
   >Social Proof doesn't disclose that a user is working on a goal if the recipient doesn’t have the permission to see that goal.

- Unsubscribed Users: Managers can unsubscribe from Nudges. To view managers who have and to resubscribe them: 
   - Select **View and Resubscribe**.
   - Follow on-screen guidance to download a list of unsubscribed users and then select a user to resubscribe or batch resubscribe all users. Users won't be notified that they've been resubscribed; they'll begin receiving Nudge notifications again.

### Enabled programs 

Nudges are enabled at the program level within each specific survey program. Your Recipient Group appears on the Nudges landing page under **Configuration**.

## Send an email preview 

Select the **Email Preview** button to view the email a recipient sees:    

1. Select **Recipient** from the dropdown menu.
1. Select **Language** from the dropdown menu.
1. Select **Options** and choose:
    1. Hide social proof in preview, or 
    2. Send preview email to yourself (your email address should appear) 
1. Select **Generate Preview**.

## Edit Nudge details 

Once Nudge details are saved, they can't be edited within specific programs or cycles. All editing must be done by first selecting **Configure** on the admin dashboard, then **Nudges**.
For each recipient group for which changes will be made: 

1. Select **Disable**, then **Disable Recipient Group**, then **Edit Details**.  
1. Make changes and then select **Save Changes**.  
1. Now select **Enable** and then **Enable Recipient Group** on the Configuration section of the Nudges landing page to incorporate the changes into your programs.

### How long will Nudges continue to send?

Nudges will send only within 90 days of the survey closing, regardless of the date Nudges are enabled. For example, if a program is on a quarterly cadence, Nudges will stop when the next cycle starts.

### Include or exclude programs from receiving Nudges

Switch the **Eligible for Nudges** feature to **YES** or **NO** on the **Program Setup** page in **Program Summary**. **Suggested Action Plans** must be switched to **ON**, to enable Nudges.

### View a list of programs enabled for roles in Nudges

From the admin dashboard select **Nudges**, then **View Details** (for an enabled User Role within the Configuration section). The Recipient Group Setup page opens for that User Role. The bottom section displays *Enabled Programs*.  

## Use the Send History section 

View Nudge dates, recipient groups, number of targeted emails, and number of emails delivered here. 

### Export data from the Send History section 

From the *vertical ellipses* next to the group, you can download a *.csv* of email recipients. To export a full file of all Nudges sent, use the *Export* button.  



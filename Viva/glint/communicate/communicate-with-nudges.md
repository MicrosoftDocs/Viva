---
title: Communicate with Viva Glint Nudges
description: "Nudges are personalized email notifications designed to meet managers where they are in their flow of work. Team Summary is easily enabled from the Viva Glint admin dashboard, allowing program roles permissions to relevant reports."
ms.author: Judithweiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 08/27/2024
---

# Communicate with Viva Glint Nudges

Microsoft Viva Glint Nudges is a system of intelligent, personalized email notifications designed to meet managers where they are in their flow of work. Nudges encourage managers to take simple steps to drive their team’s engagement and performance. Nudge notifications can include a link to the manager dashboard.

Who receives a Nudge - and which Nudge - is set up at the User Role level. 
 
Nudges has filters to ensure they're only sent when relevant. If a user repeatedly doesn't open or interact with Nudge emails, they're automatically unsubscribed. 

## Nudges are sent on a recurring schedule

Recurring communications keep employees on track over time. Managers receive unique messages with each Nudge to keep the experience fresh, focused, and relevant. Nudges simplify key behaviors into lightweight, bite-sized steps and make action taking collaborative.

Notifications that survey results are ready for viewing aren't sent to managers of small teams or to managers who didn’t receive enough feedback to meet confidentiality thresholds. 

If a user is in multiple recipient groups, they may receive emails from either group depending on the cadence of each group and its next send date. Users are guaranteed to never receive more than one email per week. 

> [!NOTE]
> Nudge communications might not send exactly between the two hour window specified during platform configuration. The total email send time is dependent upon the number of communications being sent.

## Understand Nudge terminology

| Term | Definition | 
|---|---|
| **Recipient group** | Defines who receives Nudges and at what frequency |
| **Teammates** | This term has a different meaning dependent upon the employee role:<br>- Individual contributors: Managers + peers <br>- First-line manager: Manager + directs <br>- Manager of Mangers: Manager + direct |

## How admins set up Nudges 

To set up Nudges, recipient groups must be created and enabled. Only one User Role can be selected per recipient group. You may create multiple groups to reach more User Roles or choose to send Nudges at a different frequency for each group.

From the Glint admin dashboard, select **Configure**, then  **Nudges**  in the  **Notifications** section. 

   > [!NOTE]
   >Nudge configuration may also be accessed via the **Communications** set up page in **Program Summary** for a specific survey.

### Add a new recipient group

There are several sections to set up.

### Recipients 

1. Select **+ New Recipient Group**.
1. Choose who receives the Nudges: 
    1. User Role: Select a role from the dropdown menu. Add only one User Role per group. If you have one User Role that includes all managers, it reduces the number of recipient groups you need to create.
    2. Exclude: Select individual users or Distribution Lists from the search bar. A Distribution List must already be created for it to be available. 
    3. Recipient List: Download the list of recipients to a *.csv* file to have it for reference.  
    
### Timing

Defines when and how frequently users receive Nudges.

- Frequency: From the dropdown menu, choose to send Nudges from every one to eight weeks. Frequency can be adjusted after a survey launches.
  > [!TIP]
  >Send Nudges every two to four weeks.
  >Send Day: Choose a business day of the week.
  >Window: Select the number of days Nudge messages will send after a survey closes.  
  >Align Nudges to your survey cadence, i.e., 90 days for quarterly surveys, 180 days for biannual survey.
      
### Content 

Configure the emails that are sent to your recipient group. 

Select the **Nudge #** to enable, disable, or preview. The corresponding slider window opens.

- Enable or disable by using ON and OFF. 
- Preview what your Nudge looks like: It includes your company logo, the survey name, highlight where the user is in the results process, and a link to view results.
- Results process: 
  - Nudge #1: Interpret results 
  - Nudge #2: Share with your team 
  - Nudge #3: Choose a Focus Area (or whatever term your organization uses) 
  - Nudge #4: Focus Area reminder 

### Enabled programs 

Nudges are enabled at the program level within each specific survey program. Your Recipient Group shows on the Nudges landing page under **Configuration**.

## Edit Nudge details 

Once Nudge details are saved, they can't be edited within specific programs or cycles. All editing must be done by selecting **Configure** on the admin dashboard, then **Nudges**.
To make changes to a recipient group: 

1. Select **Disable**, then **Disable Recipient Group**, then **Edit Details**.  
1. Make changes and select **Save Changes**.  
1. Select **Enable** and then **Enable Recipient Group** on the Configuration section of the Nudges landing page to incorporate the changes into your programs.

### How long will Nudges continue to send?

Nudges send within 90 days of the survey closing, regardless of the date Nudges are enabled. For example, if a program is on a quarterly cadence, Nudges stop when the next cycle starts.

### Include or exclude programs from receiving Nudges

Switch the **Eligible for Nudges** feature to **YES** or **NO** on the **Program Setup** page in **Program Summary**. **Suggested Action Plans** must be switched to **ON**, to enable Nudges.

### View a list of programs enabled for roles in Nudges

From the admin dashboard select **Nudges**, then **View Details** (for an enabled User Role within the Configuration section). The Recipient Group Setup page opens for that User Role. The bottom section displays **Enabled Programs**.



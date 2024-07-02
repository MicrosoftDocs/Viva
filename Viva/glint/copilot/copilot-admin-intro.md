---
title: Introduction and admin setup for Copilot in Viva Glint (preview)
description: Copilot in Viva Glint enables leaders and HR to understand and act on employee feedback by quickly summarizing large quantities of comments. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 06/29/2024
---

# Introduction and admin setup for Copilot in Viva Glint (preview)

> [!NOTE]
> This feature is available to preview customers only, beginning June 29, 2024. Features described here are subject to change.

HR users and leaders of large organizations spend a lot of valuable time interpreting Glint survey results and comments. Copilot in Viva Glint enables them to understand and act on employee feedback by quickly summarizing large quantities of comments. 
Copilot in Viva Glint is available for all enabled users whose teams meet the threshold for verbatim comment results.

## What is Copilot in Viva Glint?

Copilot in Viva Glint is built to answer questions about your survey comments. It's your partner for all comment analysis and can:
- Summarize your comments
- Identify key themes across comments
- Summarize comments by demographics
- Summarize comments by items
- Identify what action employees are asking for

### Does Copilot have any limitations?

- Copilot works on completed survey cycles for Recurring and Ad hoc programs. It isn’t currently available for Employee Lifecycle, Always-On, or 360 Feedback programs. 
- There must be at least one Recurring or Ad hoc program survey administered or closed on your Glint platform to use the feature. 
- Copilot doesn’t take quantitative survey results into consideration. It can’t answer questions that require comparison scores between questions or employee groups. 
- Any AI can make mistakes representing the information it finds. If you encounter harmful, inappropriate, or inaccurate responses, immediately provide feedback. Report a concern through our feedback button in Copilot in Viva Glint or in the Viva Glint app.
- Copilot samples a subset of comments from each question, proportionate to the overall comment count per question. The current limit for this feature is 1000 comments.
- Currently Copilot can't manage language translations beyond its default English.

### Are more Copilot features planned?

Yes! As with all Viva Glint features, we post as soon as new features are available. 

## How can my organization use Copilot in Viva Glint?

Copilot answers queries related to your comment data in Glint, such as:

|Survey goal|	Example Copilot prompt|
|------|-----|
|Discover more about your opportunities|	Summarize comments related to the barriers to execution item.|
|Understand experiences of unique sub-populations|What are Engineers in North America saying about opportunities for growth?|
|Uncover action people hope you take|What are people requesting leaders do to increase communication?|

## Copilot can be used across roles

Use Copilot in Viva Glint for admins, HR leaders, org leaders, and managers.
- **Admins and HR** can use Copilot to summarize large sets of data, allowing this group to quickly find key insights and support ad-hoc requests from stakeholders.
- **Org leaders** can use Copilot to summarize comments for their teams. They can uncover similarities and unique needs based on comments people are leaving using prompts and filters for different populations across their org.
- **Managers** can use Copilot to get access to comment summarization services. Managers can quickly uncover comments bundled by common subject matter or theme, identifying areas to explore deeper in their ACT conversations.

> [!NOTE]
> Copilot in Viva Glint defaults to **Off** for all User Roles, including company owners. Every user who should have Copilot enabled needs to be placed into a User Role category with that permission. Copilot can be activated for any number of user subsets designated.

### Microsoft’s commitment to responsible AI

Copilot in Viva Glint aligns with our [AI principles](https://www.microsoft.com/ai/principles-and-approach) and undergoes rigorous internal stress testing. We actively identify and address systematic issues, ensuring Copilot comment summarization remains free from undesirable content or behavior such as hate speech, incitement to violence, or misinformation. We're vigilant about protecting privacy and preventing the disclosure of sensitive information.

## Choose a method to roll out Copilot 

Copilot gives you the flexibility to roll out to one or many user roles. Consider what approach is right for your organization. 

||Admin Release|	Selective deployment|	Full deployment|
|-----------|----------|------------|-----|
|**Users**|	Viva Glint admins only|Select group of users|	All User Roles|
|**Details**|This setting is the default setting for Copilot in Viva Glint.<br><br>You may decide that for the first deployment you don’t want to provide access beyond this group. This option is a way to test and better understand the functionality.<br> <br> As a testing method, admins can use the Copilot functionality for previously closed surveys.|You may decide to deploy to a group beyond admins but not to your entire eligible population. <br><br> Consider which groups (User Roles) can benefit from the feature. Prioritize those with large sets of comments.|You may decide to deploy to a group beyond admins but not to your entire eligible population. <br><br> Consider which groups (User Roles) can benefit from the feature. Prioritize those survey items with large sets of comments.|

### Deployment considerations

Think about:
- **Current usage** – does your rollout group have experience with Viva Glint?
- **Comment count** – do you expect a high number of comments?
- **Survey timing** – can you align with an upcoming survey? 
- **Comfort with AI** – can you engage superusers to help others with the rollout?
- **Amount of change** – is your organization already going through change? Is this time right to add a new tool?

## Best practices for Copilot

Use our best practices to maximize the benefits from Copilot in Viva Glint. Use programs and survey formats that align with the strengths and current capabilities of Copilot in Viva Glint.  

- **Enable comments** – allows for more detailed feedback and context, enhancing the data's richness and usefulness for summarization purposes. This approach provides a comprehensive view of feedback, allowing the generation of accurate and insightful summaries.
- **Ask open-ended items** – Open-ended survey items capture a wide range of feedback. Open-eneded items allow respondents to express thoughts on topics not covered explicitly in the survey. These responses are often detailed and can reveal rich data insights not apparent from quantitative data alone.
- **Use relevant attribute filters** – Copilot in Viva Glint uses the attributes you send to Viva Glint to filter data. Enable filter attributes that are meaning for User Roles interacting with Copilot. Filters ensure that insights and summaries are applicable and useful.
- **Use Recurring and Ad hoc programs** - Where it makes sense, use Recurring and Ad hoc programs. Currently Copilot in Viva Glint is unable to tap into Always-On and Employee Lifecycle programs. To maximize your ability to use Copilot in Viva Glint, use Recurring program setup for ongoing topics (Engagement) and Ad hoc for one-off topics (Change Management). 

## Enable Copilot 

Prerequisites to enabling Copilot:
- You have at least one Recurring or Ad hoc survey administered or closed on the Viva Glint platform
- Your dashboard default language is set to English

Admins enable Copilot in Viva Glint. Microsoft privacy policies prohibit Copilot from being enabled by default for any User Roles. 

You must assign yourself and others using Copilot to a new User Role. Create a new User Role with access to the Comments Report enabled. Add that User Role to the survey program *Reporting* page, as described in *Grant User Roles Comment Reports access*. 

>[!IMPORTANT]
>Users without access to the Comment Report can’t access Copilot in Viva Glint.

### Grant Comment Report permission

From your admin dashboard, follow this process:

1.	Select the **configuration (cogwheel)** symbol.
2.	In the *Employees* section, select **User Roles**.
3.	Select the User Role to provide Comment Report access. In this example, Company Admin is chosen.
   
   :::image type="content" source="../../media/glint/setup/copilot-select-user.png" alt-text="Screenshot of how to give a User Role Copilot in Viva Glint permissions."lightbox="../../media/glint/setup/copilot-select-user.png":::

>[!NOTE]
>The Manager role has Comment Report permission enabled as a default setting.

4. Select **Permissions**.
  
   :::image type="content" source="../../media/glint/setup/copilot-permissions.png" alt-text="Screenshot of the Permissions    access row in *Role Settings*."lightbox="../../media/glint/setup/copilot-permissions.png":::

5.	In the *Reporting* section of the Permissions and Access page, enable **View Comments**.

   :::image type="content" source="../../media/glint/setup/copilot-view-comments-toggle.png" alt-text="Screenshot of the View Comments    checkbox."lightbox="../../media/glint/setup/copilot-view-comments-toggle.png":::

## Grant Comment Reports access 

The second step to enabling the Copilot feature for User Roles happens in the program’s *Reporting* section. This step allows users enabled for the Comments Reports to access the report.

From your admin dashboard, follow this process:

1.	Select the **configuration (cogwheel)** symbol.
2.	In the *Surveys* section, select **Survey Programs**.
3.	**Select the closed Recurring or Ad hoc program** for which you want to grant access.
4.	In *Program Summary*, select **Reporting**.

   :::image type="content" source="../../media/glint/setup/copilot-reporting.png" alt-text="Screenshot of the Reporting    section in Program Summary."lightbox="../../media/glint/setup/copilot-reporting.png":::

5. In *Program Roles*, select the User Role to enable with Copilot. *In this example, the customized role of VI is chosen.*

   :::image type="content" source="../../media/glint/setup/copilot-program-roles.png" alt-text="Screenshot of an example User Role."lightbox="../../media/glint/setup/copilot-program-roles.png":::

6. Toggle *Copilot in Viva Glint* to **On** and then **Save Changes.**

   :::image type="content" source="../../media/glint/setup/copilot-enabled.png" alt-text="Screenshot of the Role Permissions sections within the Reporting section."lightbox="../../media/glint/setup/copilot-enabled.png":::

### Ensure Copilot is enabled

From your admin dashboard, follow this process:

1.	Select the **Configuration** symbol.
2.	Select **User Roles** in the *Employees* section to see the list of all users assigned to a particular role.
3.	Select any employee in a User Role in which you expect Copilot to be enabled.
4.	Once you are on that user’s profile, select **View A**s to validate the user’s reporting experience.

   :::image type="content" source="../../media/glint/setup/copilot-view-as.png" alt-text="Screenshot of the View As button in User Roles."lightbox="../../media/glint/setup/copilot-view-as.png":::

5. Be sure you see the Copilot button on that user's Viva Glint dashboard.

   :::image type="content" source="../../media/glint/setup/copilot-access-button.png" alt-text="Screenshot of the Copilot capability on the manager dashboard ."lightbox="../../media/glint/setup/copilot-access-button.png":::

## More Resources

[**Learn how managers can use Copilot in Viva Glint**](https://go.microsoft.com/fwlink/?linkid=2274072)
[**Find answers to technical FAQs**](https://go.microsoft.com/fwlink/?linkid=2274071)
[**Copilot for Microsoft 365**](https://adoption.microsoft.com/copilot/)














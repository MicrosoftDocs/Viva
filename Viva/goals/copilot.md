---
ms.date: 01/02/2024
title: Create, manage, and summarize goals with Copilot in Viva Goals
ms.reviewer: 
ms.author: v-nstockwell
author: DefinitelyNotNitza
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn how to use Copilot in Viva Goals to create, share, manage, and summarize organizational goals."
---

# Create, manage, and summarize goals with Copilot in Viva Goals

<!--Should it be "Copilot in Viva Goals" or "Viva Goals Copilot"?-->

Copilot in Viva Goals lets you leverage next-gen AI to create, share, manage, and summarize your organizational goals quicker and easier than ever. It offers in-app guidance for creating and refining goals, providing a productivity boost to users regardless of their familiarity with whatever goals framework their team follows.

## Prerequisites

During the preview, the Copilot feature in Viva Goals will be disabled by default. Before anyone in an organization can use Copilot in Viva Goals, that org's tenant admins must enable Copilot from the Admin portal. Tenant admins have complete control over the rollout of Copilot in Viva Goals within their org. They can also decide which users or security groups are allowed to access Copilot. Tenant admins can access these and other Copilot admin settings by selecting the Viva Goals admin center icon in the top header and scrolling to *Who can see Viva Goals Copilot in TENANT NAME?* under the **General** tab.

![Screenshot that shows a view of a product team's OKRs and emphasises the Admin portal icon.](..\media\goals\copilot\admin-portal.png)

![Screenshot that shows the Admin portal and emphasizes the setting for deciding who can see Viva Goals Copilot in the tenant.](..\media\goals\copilot\who-can-see-copilot.png)

## What are some things I can do using Copilot in Viva Goals?

### Generate goals using a strategy document

Copilot in Viva Goals can read through strategy or planning documents and propose appropriate goals or OKRs.  

Viva Goals does not store your documents or conversational prompts for any purpose. You can find more information about how Microsoft uses Copilot data in Viva Goals [here](..\viva-privacy.md).

![Screenshot that shows a view of a product team's OKRs with a view of suggested Copilot actions on the right side.](..\media\goals\copilot\suggested-copilot-actions.png)

![Screenshot that shows a view of a product team's OKRs with Copilot requesting a strategy document from which to generate OKRs on the right side.](..\media\goals\copilot\strategy-document-request.png)

![Screenshot that shows a view of a product team's OKRs with the user having provided a strategy document on the right side.](..\media\goals\copilot\strategy-document-provided.png)

![Screenshot that shows a view of a product team's OKRs with Copilot suggesting OKRs based on the strategy document given on the right side.](..\media\goals\copilot\strategy-doc-okr-suggestions.png)

### Generate key results for existing goals

Select **Generate key results using Copilot** in the "add child items" menu (see below), and Copilot in Viva Goals will generate appropriate key results for the relevant objective.

![Screenshot that shows a view of a product team's OKRs with one objective's "add child items" menu open.](..\media\goals\copilot\add-child-items-menu.png)

![Screenshot that shows a view of a product team's OKRs with Copilot offering key results for a certain objective on the right side.](..\media\goals\copilot\suggested-key-results.png)

### Generate goals using the conversational Copilot bot

When you're in the planning stage, you can chat with Copilot in Viva Goals to get ideas for new OKRs. Copilot will suggest goals based on your organization's OKR data, user profiles shared with Viva Goals, and any information you provide in conversation with Copilot.

> [!TIP]
> When you're giving Copilot instructions to help you generate goals, it helps to be as descriptive as possible. Mention your business industry, department, and three to five topics or themes you think your team or org should focus on. For example, you might say this:
>
> *I work for a retail company in the marketing department. This year, we want to become the market leader, expand to new geographic regions, and increase our product offerings.*

![Screenshot that shows a view of a sales team with no OKRs, but for which the user has requested and received suggested OKRs through conversing with Copilot on the right side.](..\media\goals\copilot\conversational-okr-suggestions.png)

### Summarize goals

You can use Copilot in Viva Goals to access summaries of goals, including team goals and collections of OKRs. Team managers and department leaders can easily generate summaries of their teams' progress. Copilot will analyze check-in data, status updates, and progress details associated with child items to prepare a quick summary. Users can share these summaries as updates, use them to prepare for review meetings, or let them serve as check-ins for their objectives.

![Screenshot that shows a view of a product team's OKRs, with an emphasis on the "Generate a summary" option.](..\media\goals\copilot\generate-a-summary.png)

![Screenshot that shows a view of a product team's OKRs, with Copilot having generated a summary of the OKRs on the right side.](..\media\goals\copilot\okr-summary.png)

![Screenshot that shows a view of a product team's OKRs, with two specific OKRs selected and an emphasis on the "Summarize" option.](..\media\goals\copilot\summarize-specific-okrs.png)

### Understand goals

Copilot in Viva Goals can answer questions about goals methodology, such as what exactly OKRs are, the best ways to run OKR rhythms, and how to plan around OKRs.

![Screenshot that shows a view of a product team's OKRs, with the user asking Copilot questions about OKR methodology on the right side.](..\media\goals\copilot\okr-methodology-conversation.png)

> [!NOTE]
> Copilot in Viva Goals is under constant development. The content generated by Copilot will not always be reliable: for example, Copilot is great at generating OKRs and answering questions related to OKRs, but it's not capable of understanding what's true or factual. Use your own judgment and verify AI-generated content when using Copilot.

## Frequently asked questions

### What sort of reviews has Copilot in Viva Goals gone through?

In anticipation of the preview, Copilot in Viva Goals has gone through the Microsoft Trust review process. Among other things, this includes a Responsible AI review, security review, and privacy review. At present, Copilot in Viva Goals should only be used for evaluation.

When dealing with any Copilot experience, we recommend users review the responses generated by the AI before acting. Always make sure the results are accurate and compliant with your organization's guidelines.

### What AI model are you using?

We are currently using GPT 3.5 Turbo and GPT-4 PPO models through the Substrate LLM.

### Did you fine tune the model for Microsoft Viva Goals? How did OpenAI contribute to these new products specifically?
<!--Heading does not match body text-->

No, Copilot in Viva Goals is leveraging a base model. It works based on a prompt that is grounded on common Viva Goals OKR sample data, common instructions, and the given customer’s specific existing OKRs that the user has access to.

### How does Copilot in Viva Goals ensure it is not exposing sensitive data in the organization to individual employees?

The output of Copilot in Viva Goals depends on the prompt that is passed to the model. This prompt consists of:

1. Any text or data that the user supplies to Copilot in Viva Goals.  

2. OKRs in Viva Goals that users<!--All users in the org, or the specific user?--> have access to.  

3. Common instructions and sample OKR data.  

By enforcing access and permissions in Viva Goals, Copilot ensures that users only see data they are allowed to see.

### Will my employer (or Microsoft) be able to monitor my work through Copilot in Viva Goals?

No. Copilot does not give Microsoft or your employer the ability to monitor your work. Microsoft's use of artificial intelligence is governed by the Responsible AI Standard, which you can learn more about [here](https://www.microsoft.com/ai/responsible-ai).

### Are there any limits to Copilot in Viva Goals that I should be aware of?

Copilot in Viva Goals only provides suggestions for goals, which the user is advised to review and iterate on before accepting. Sometimes the suggestions are correct and relevant to the user, ready for immediate use. Other times, the suggestions are a good starting point for the user to build on. Copilot in Viva Goals makes this philosophy very explicit via an information bar at the top, which states "AI-generated content may be incorrect."

### Once available, can admins block all capabilities related to Copilot in Viva Goals in one command or through Group Policy?

Yes. There is a setting in the Viva Goals Admin portal that allows tenant admins to disable all capabilities related to Copilot in Viva Goals.  

### Will Copilot in Viva Goals be available in other languages?

At present, Viva Goals is committed to improving its quality and relevance in US English. Other languages will be considered for future development.

### Will other users be able to access org information since Copilot in Viva Goals uses OpenAI?

No. Copilot in Viva Goals uses its own instance of the Substrate LLM model. Neither the Substrate LLM model nor the data entered by user is shared with any other users or customers. Within Viva Goals, Copilot adheres to all security and privacy controls, ensuring the tenant's data is stored and used in a compliant manner.

### Where are the OKRs saved when I use Copilot in Viva Goals on any given entity page?

At present, Copilot in Viva Goals defaults to saving OKRs in the same entity page where it is invoked. In the future, users will be given an option to select the entity and time period where they would like to save their OKRs.

### Do I need to do any manual work once the goals are saved?

Goals created using Copilot in Viva Goals function the same as manually created goals. Users can modify the details of any objectives or key results by selecting **Edit** as normal. Remember that anything generated by AI is only *suggested* content. Before saving, please ensure the content is accurate and appropriate for your organization's guidelines.

### How are owners, time periods, and teams defined for AI-generated goals?

The user who generates an goal using Copilot in Viva Goals will be that goal's default owner. When saving a Copilot-generated goal, the user can select a time period and the team for the goal.

### How do goal permissions work when creating goals using Copilot in Viva Goals?

Goals created by Copilot in Viva Goals honor the same entity permissions as goals created manually.

### What should I keep in mind when generating goals using Copilot in Viva Goals?

In general, Copilot in Viva Goals will give its most relevant responses when the context provided to it is as accurate as possible. Always remember that these responses are suggestions generated by AI. Before saving, make sure the content is accurate and appropriate for your organization's guidelines.  

---
title:  Copilot in Viva Glint FAQs (preview)
description: Scan the most commonly asked questions about the comments summarization tool in Microsoft Viva Glint.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 06/29/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Copilot in Viva Glint FAQs (preview)

> [!NOTE]
> This feature is available to preview customers only, beginning June 29, 2024. Features described here are subject to change.

## Foundational and enablement questions

**Q: Should we have concerns about bias in Copilot in Viva Glint? What metrics are used to measure performance?**

**A:** At Microsoft, our commitment to responsible AI is paramount. Copilot in Viva Glint aligns with our AI principles and undergoes rigorous internal stress testing. We ensure Copilot’s comment summarization remains free from undesirable content or behavior such as hate speech, incitement to violence, or misinformation. We're vigilant about protecting privacy and preventing the disclosure of sensitive information. Our ongoing evaluation process incorporates feedback from early adopters and customers, helping us continuously enhance Copilot's performance.

<br>**Q: How often is the Large Language Model (LLM) updated for Copilot in Viva Glint?**

**A:** Copilot in Viva Glint uses the latest Open AI LLM model, GPT 4.0 turbo, trained with data up to April 2023. While it currently relies solely on customer survey data without external references, prompt engineering is continuously updated to ensure Copilot delivers accurate and relevant responses based on survey inputs.

<br>**Q: What’s the licensing for Copilot in Viva Glint?** **Is it part of the Microsoft 365 Copilot, or Viva Glint licensing?**

**A:** Copilot in Viva Glint is separate from the Microsoft 365 Copilot license and is available with a Viva Glint or Microsoft Viva license.

<br>**Q: Is Copilot in Viva Glint included in the Viva Glint subscription or as part of Viva Suite?**

**A:** Copilot in Viva Glint is available for all Viva Glint customers with a Microsoft Viva and Viva Glint licenses.
 
<br>**Q: If I have a Microsoft 365 Copilot license and a license for Viva Glint, does that augment the Copilot in Viva Glint responses by having more scope to ground responses in (e.g., an Excel sheet with data to correlate the survey responses with)?**

**A:** Currently, no.

<br>**Q: How is Copilot in Viva Glint enabled?**

**A:** Admins enable Copilot in Viva Glint for within programs.
 
<br>**Q: What operational factors and settings allow for effective and responsible use of Copilot in Viva Glint?**

**A:** Viva Glint admins can enable or disable Copilot in Viva Glint for any role, in any survey program. Copilot in Viva Glint launches as ‘disabled’ or ‘off’ for all users by default.

## Current capabilities

<br>**Q: What features does enabling Copilot in Viva Glint provide access to?**

**A:** Through an interactive question and response format, users can request comment summarization across survey items, and filter attributes. Current functionality includes the ability to summarize, in English:
- All Comments
- Comments by Item
- Comments by Comment Sentiment
- Comments by Filter Attribute
- Prescriptive Comments
 
<br>**Q: Can customers participate in multiple private previews, such as Viva Glint and Viva Insights integration, and Copilot in Viva Glint?**

**A:** Yes, customers can enroll in multiple private previews by joining the Viva Customer Connection Program (VCCP), a prerequisite for any Viva private preview.

<br>**Q: Is there a cut-off date for the Copilot in Viva Glint private preview?**

**A:** The private preview ends with the public launch on June 29, 2024. Existing private preview customers can continue their private preview interviews after the June 29 public launch.
 
<br>**Q: Does Copilot in Viva Glint work retroactively on past surveys, including those migrated from LinkedIn Glint?**

**A:** Yes. Copilot can analyze comment data from the previous two cycles within a program, including surveys migrated from LinkedIn Glint.
 
<br>**Q: Does Copilot pull from the program level or generic settings for confidentiality thresholds?**

**A:** Copilot aligns with the threshold configured on the dashboard or report being viewed.
 
<br>**Q: What data controls are in place?**

**A:** Copilot in Viva Glint has access to Viva Glint survey data only. Each user only sees survey data they’re granted access to by their Viva Glint admin. Viva Glint admins can control which roles use Copilot in Viva Glint and for which survey programs.

<br>**Q: Can the end user see variables in summarization, based on the user's question or prompt?**

**A:** Yes, Copilot shows attributes in its response so you can adjust them for your next prompt. For example, when filtering a particular tenure group or location, it shows what filter attributes are included in the summary provided.
 
<br>**Q: If I ask Copilot in Viva Glint for key topics, does it use the same topic model as Viva Glint today? If not, what did you train on?**

**A:** For now, we only tap into the items, not the topics from the NLP. Copilot pulls topics from its own semantic matching system that is similar to the NLP already available in Viva Glint but not exactly the same. 
  
<br>**Q: How does Copilot in Viva Glint identify teams?** 

**A:** Team identification is based on the manager hierarchy within your data file.

<br>**Q: Is it possible to start a conversation in the dashboard to address comments (e.g., for a manager to acknowledge a comment and address it)?**

**A:** Currently, no.

<br>**Q: Does Copilot in Viva Glint have the ability to look across multiple surveys or just 
one at time?**

**A:** One at a time for now. Additionally, Ad hoc and Recurring survey programs only, but we are looking to add the feature to employee lifecycle and always-on programs in the future.

<br>**Q: Can Copilot in Viva Glint generate a PowerPoint from the results?**

**A:** Not yet, but it’s another feature we would like to explore.
 
<br>**Q: Can Copilot recognize when some groups (based on attributes) have more of a negative or positive reactions to a certain question? Can it determine cultural bias or language/translation problems?**

**A:** Currently, Copilot in Viva Glint can’t detect potential biases between survey comments left in different languages, as English is currently the only language available.

## Copilot roadmap

<br>**Q: Are new features planned for Copilot in Viva Glint?**

**A:** Yes! We let you know as soon as new features are available for Copilot in Viva Glint. All items mentioned as currently unavailable are on our list for consideration.

<br>**Q: Does Copilot have any limitations?**

**A:** Currently, but under consideration for the future:
- Copilot works on completed survey cycles for Recurring and Ad hoc programs only. It isn’t currently available for Employee Lifecycle, Always-On, or 360 Feedback programs. 
- There must be at least one Recurring or Ad hoc program survey *administered* or *closed* on your Glint platform to use the feature. 
- Copilot doesn’t take quantitative survey results into consideration. It can’t answer questions that require comparison scores between questions or employee groups. 
- Any AI can make mistakes misrepresenting the information it finds. If you encounter harmful, inappropriate, or inaccurate responses, immediately provide feedback or report a concern through our feedback button in Copilot in Viva Glint or in the Viva Glint app.
- Copilot samples a subset of comments from each question proportionate to the overall comment count per question. The current limit for this feature is 1000 comments (seeded comments - they come from the same 1000 questions if the prompt is regenerated).
- Copilot doesn’t currently support cross-program filters.
- Copilot doesn’t currently support plug-ins.

<br>**Q: What languages does Copilot support for comment summarization?**

**A:**  We let you know when Copilot can manage language translations beyond its default English. We’re actively evaluating the accuracy of non-English language comment summarization.



 





---
ms.date: 02/28/2023
title: Keyword suppression in Viva Insights
description: Learn how to suppress sensitive keywords in email subject lines and meeting titles with Viva Insights. 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Keyword suppression

In the Microsoft Viva Insights advanced insights app, you can specify sensitive keywords that might appear in email subject lines or meeting titles across your organization. After you set them, subject lines or meeting titles that contain these keywords won't appear in any surface that uses Viva Insights data, including query output.

>[!Important]
> Viva Insights suppresses *all* email subject lines and meeting titles by default. To get the most out of all Viva Insights features, you'll need to change this setting. Refer to [Default setting and feature availability](#default-setting-and-feature-availability) for more information.

## How it works

When Viva Insights finds one of the sensitive keywords set by an admin in a meeting title or email subject line, it suppresses that entire title or subject line in query outputs. So, while Viva Insights might use a meeting or email with suppressed keywords in aggregated insights, analysts won't see the title or subject line in their query results. In the following image of a meeting query result, the **Subject** column omits certain values. These values are meeting titles that contained sensitive keywords set by an admin.

:::image type="content" source="../images/meeting-query-output-keywords-suppressed2.png" alt-text="Screenshot that shows a meeting query .csv output with some missing text in the Subject column." lightbox="../images/meeting-query-output-keywords-suppressed2.png":::

In other words, if you set up keywords, analysts won't be able to associate query data about affected meetings or emails with their title or subject line.

### Default setting and feature availability

By default, Viva Insights suppresses *all* email subject lines and meeting titles. Some Viva Insights metrics use title and subject line data, for example, **Urgent email hours**. Those metrics feed into features, like certain Power BI reports. If you keep keyword suppression turned off, those metrics and features won't be available to you.

When analysts try to run a query that depends on keywords, and all keywords are suppressed, they'll run into warnings and errors.

## How to change keyword-suppression settings

In the advanced insight app's admin experience, go to **Privacy settings**.

Under **Suppress email subject lines and meeting titles**, you'll find these three options:

* **Suppress all email subject lines and meeting titles**
* **Don't suppress any email subject lines or meeting titles**
* **Only suppress email subject lines and meeting titles that have these keywords**:

:::image type="complex" source="../images/admin-keyword-suppression1.png" alt-text="Screenshot that shows the keyword suppression section of the Privacy settings page.":::
   Screenshot of the "Suppress email subject lines and meeting titles" section of the Privacy settings page. The subtitle says, "When you suppress email subject lines and meeting titles, Viva Insights hides those subjects and titles from appearing in query results. Changes you make here only apply to future queries, and not to queries that analysts in your organization have already run." Underneath the subtitle, there are three radio buttons, with labels corresponding to the bulleted list items above. The first radio button is selected. 
:::image-end:::

### Suppress all subject lines and meeting titles (default setting)

When you **Suppress all email subject lines and meeting titles**, Viva Insights won't include *any* meeting titles or subject lines in queries. As discussed earlier, we made this the default setting for everyone. You don't need to take any action if you want all meeting titles and subject lines suppressed.

### Don't suppress any subject lines and meeting titles

When you **Don't suppress any email subject lines or meeting titles**, you turn off keyword suppression. Viva Insights makes *all* subject lines or meeting titles available for query analysis, so any title or subject line could show up in query output.

### Only suppress email subject lines and meeting titles that have these keywords

When you **Only suppress email subject lines and meeting titles that have these keywords**, you suppress titles and subject lines with specific keywords, but not all titles and subject lines. Viva Insights only suppresses titles and subject lines with the keywords you set.

To set keywords, enter them in the text box provided. Viva Insights checks each keyword against subject lines, so enter each word separately, even if they're part of a phrase. For example, if you want to suppress a meeting title or subject line that contains the phrase, "Fire drill," you'd enter "fire" and "drill" as separate words. Keywords need to have at least three letters, and they're case insensitive. After you're done adding keywords, select the **Save changes** button at the bottom of the screen. 

:::image type="complex" source="../images/admin-add-keywords1.png" alt-text="Screenshot that shows adding keywords.":::
   Screenshot showing the last radio button selected on the keyword suppression section, "Only suppress email subject lines and meeting titles that have these keywords:", with an information icon to the right of the button label. Below the button, there's a text-input field, which shows a word being typed in; the field contains a "+" label at its far-right edge. Beneath the text-input field, various other entered keywords appear as tags in a box. Under the box, there is a label to the left that shows how many keywords are selected. A link to the left reads, "Clear all."
:::image-end:::

>[!Important]
>Keyword suppression only applies to queries that analysts run in the future. When you set keywords, they won't apply to queries that analysts have already run.

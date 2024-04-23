---
title: Use the Viva Glint Question Library
description: "Choose from hundreds of questions and statements to surface feedback that will provide data to support your company goals."
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: question mapping, standard questions, survey items,
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/21/2024
---

# Use the Viva Glint Question Library

From the admin dashboard, in the *Survey* section, you'll find the **Question Library**. Microsoft Viva Glint’s Question Library contains hundreds of questions and statements that can be included in your surveys. If you choose a template for a specific survey type, the questions and statements that best support the survey goal are prepopulated into the template. You can create and edit items from the Question Library, but Viva Glint suggests that you use our standard questions as most are mapped to benchmarks.

>[!IMPORTANT]
>[Use this Learn guidance to understand question mapping](question-mapping.md).

>[!NOTE]
>Not all items in the Question Library are posed in question format. Many library items are statements for the survery taker to rate on a given scale. For this reason, note that the term "items" is often used to refer to the contents of the Question Library.

From the Question Library you can: 

- Search items by question type, key driver, benchmark, and whether translations are available 
- Import and export questions for language translations 
- Edit or create questions 
- Sort by Viva Glint standard questions or a custom question you created or edited 
- View the number of your programs which have used this question or statement 

   > [!NOTE]
   > Changes made to the Question Library: 
   >  - When a reporting label is changed, it instantly propagates to all programs, past and present.
   >  - When question text is changed, it propagates to future programs only.

## The implication of customizing Question Library items 

Viva Glint has done extensive research to identify the most reliable and valid items linked to survey goals, and our benchmarks are created using the exact text from these items. Even a slight change to a question or statement can alter the meaning enough to invalidate a comparison to the benchmark.  

   > [!TIP]
   > **In cases where text is altered to sufficiently alter the item's meaning, the benchmark comparison is no longer valid.** For major item changes, create a copy of the standard item to customize so that it isn't tied to an invalid bencharmk for comparison. While losing a benchmark might seem like a disadvantage, using items that are most relevant to your organizational needs and measuring progress over time are more impactful.

Customized standard survey items may not map to external benchmarks. If making a change to our standard survey items, we recommend duplicating the question and creating a customized version. [Read about question mapping](/../../viva/glint/setup/question-mapping).

## Edit items from the Question Library 

There may be cases where slight edits to wording can be accommodated without altering the meaning. In these cases, make small edits to Viva Glint standard items to retain benchmark data.  

Any item can be edited by hovering over and selecting the row that the item appears on in the Question Library. An *Edit Question* slider panel displays. From this panel you can: 

1. Edit the question, and  
1. View associated programs 

### Editing a question: 

1. Choose the language. Languages for which this item has been translated will be visible in the dropdown menu. 
1. Edit the reporting label, if desired. 
1. Edit the item text, if desired. 
1. Add instruction text that helps the user understand the meaning of the item. 
1. Add comment placeholder text, if desired. 
1. Change the rating scale, if applicable. 
1. Indicate whether the label explanation for ratings should be shown. 
1. Enable or disable commenting. 
1. Choose whether the item is optional or mandatory.
1. Map the item to a Suggested Action Template, if desired. 
1. Select **Save Changes**. 

#### Examples of edits that retain a valid benchmark comparison

|Example|Standard|Modified|Recommendation|
|-------|--------|-------|-------|
|**1 - Matching the language of the business**| I would recommend my *manager* to others.|I would recommend my *supervisor* to others.| Modifying a term in the item to make it more specific to your organizational language is acceptable and doesn't affect the benchmark. Edit the standard item without creating a copy to retain the benchmark.| 
|**2 - Using synonyms**|The recruitment process was *excellent*.|The recruitment process was *great*.|If the replacement word is likely to be interpreted similarly, the item change is acceptable. Edit the standard item without creating a copy to retain the benchmark.| 

#### Examples of edits that don't retain a valid benchmark comparison

|Example|Standard|Modified|Recommendation|
|-------|--------|-------|-------|
|**1 - Altering the subject** | *I feel empowered* to make decisions regarding my work.|*My manager empowers me* to make decisions regarding my work.|  Altering the subject in an item changes the way people respond, and the benchmark will no longer be valid. Create a copy of the standard item and customize the copy so that there isn't an invalid benchmark tied to the edited item.|
|**2 - Altering the subject** | My manager *provides me with feedback that helps me improve my performance*.|My manager and *I have regular conversations*.| When the meaning of an item has been fundamentally altered, the change isn't recommended, and the benchmark is no longer valid. Create a copy of the standard item and customize the copy so that there isn't an invalid benchmark tied to the edited item.|  

## View associated programs 

Use this tab to see if this item is associated with any existing program. To add it to a program, use the [Questions page in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231415). 

## Add new items to the Question Library 

Select the **+ Create Question** button on *Question Library* page. In the *Create Question* slider panel that opens, edit the question (as above, in *Edit the question*). Upon completion, you see new item in the *Name* column, sorted alphabetically by key driver. 

## Export, translate, and import items 

English is the default language for all Viva Glint programs. You may choose to survey and send email communications to your employees in their preferred language, rather than the default language. Viva Glint provides its customers with more than 70 language translations for standard content. Language translations are set during the initial survey configuration or added later, as needed. 

To support translations, Viva Glint allows admins to export all program content - including all items from the Question Library - into .csv and .xlsx format. Exporting a file that includes English and all relevant translations in one place, provides an efficient way for users to review, add or edit translations and import them back into the platform. 

Use these steps for translating Question Library items: 

1. Export the items. 
1. Employ a translator to make translations. 
1. Use a translation reviewer to verify translations. 
1. Import the items back into the platform. 

### Export your items for language translation 

The first step for translating language translations is to export the list of items.  

1. Select **Export Questions** from the **Actions** dropdown menu. 
1. Choose the language(s) to include from the search box in the *Choose Which Language to Export* dialog box. 
1. Select your export format from *.csv* or *.xlsx*. 
1. Select **Export**. A dialog box lets you know that your file is being downloaded. 
1. After the report is downloaded, select **Close Window**. 

### Translate the exported items 

From the file that has been generated: 

1. Use a translator to make exact changes to the items in column C for the approved English text in column B. 
1. Further to the right, consider other items that might require translation: reporting labels, multiple choice questions, and ratings labels.  
1. Use your translation reviewer to ensure that translated items match exactly to the approved item from the Question Library. 

### For translators:

|Do|Don't|
|-------|--------|
|Keep the translated content in the same cell and columns|Don't edit, translate, or delete any bracketed text such as {user first name}, `<COMPANY_NAME>` or {{company name}}. It must stay the same for personalization coding. There's no need to translate anything in brackets. If questions containing brackets are changed, ensure brackets around the text are balanced (one bracket at the start and one at the end, or two at the start and end).| 
|Ensure that there are no spaces added before or after the updated content|Don't make visual, format, or other stylistic changes unless it improves clarity. Changes shouldn't alter the meaning conveyed in the original English text. Don't add personal comments.|
|Ensure there is consistent punctuation at the end of sentences (that is, all using a period or none using a period)|Don't add personal comments.|
|Check for grammatical errors|Don't add new or additional columns or remove columns.| 

### For translation reviewers

|Do|Don't|
|-------|--------|
|Focus on copy-editing by fixing any typos or grammatical errors|Don't rewrite entire sentences|
|Confirm that the original meaning of the question remains intact|Don't move translated content to different cells or columns|
Keep translated content in the same cell and columns|Don't add personal comments|
   
### Import your translated items 

Back on the **Question Library** page, select **Import Questions** from the dropdown **Actions** menu. 

1. Drag and drop or browse to find the translated file and place it in the box. 
1. Select **Next**. 
1. If everything looks as expected, select **Make Changes**.

### [Change survey item IDS for expired survey cycles](/../../viva/glint/setup/change-item-id)

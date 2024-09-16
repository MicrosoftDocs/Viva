---
title: Find validated items in the Viva Glint Question Library 
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
ms.date: 09/16/2024
---

# Find validated items in the Viva Glint Question Library

Access the **Question Library** from the admin dashboard, in the **Survey** section. The Microsoft Viva Glint Question Library contains hundreds of questions and statements (we call them *items*) that can be included in your surveys. If you choose a template for a specific survey type, the questions and statements that best support the survey goal are prepopulated in the template. You can create and edit items from the Question Library, but Glint suggests using our standard questions as most are mapped to benchmarks.

>[!NOTE]
> Not all items in the Question Library are posed in question format. Many library items are statements for the survery taker to rate on a given scale. For this reason, note that the term "items" is often used to refer to the contents of the Question Library.

## There are two versions of some Glint standard Question Library items

Some Glint standard items (questions) have two versions

- Standard items: items validated by Viva People Science that are mapped to benchmarks using *exact* text for recurring, Engagement-type programs.

- Standard items for Employee Lifecycle (Onboarding and Exit) programs: items validated by Viva People Science that are mapped to benchmarks using text specific to Employee Lifecycle programs.

 - Using the search bar, begin to key in "Onboarding" or "Exit" to bring up the items specifically indicated for Employee Lifecycle program.
   
   :::image type="content" source="../../media/glint/setup/question-library-elc-specific.png" lightbox= "../../media/glint/setup/question-library-elc-specific.png" alt-text="Screenshot of how to find Employee Lifecycle specific items in the Question Library.":::

## Uses for the Question Library 
- Search items by question type, key driver, benchmark, and whether translations are available 
- Import and export questions for language translations 
- Edit or create questions 
- Sort by Glint standard questions or a custom question you created or edited 
- View the number of your programs which have used this item

> [!NOTE]
>  - When a reporting (item) label is changed, it instantly propagates to all programs, past and present.
>  - When question text is changed, it propagates to future programs only.

## The implication of customizing (editing) Question Library items 

Glint has done extensive research to identify the most reliable and valid items linked to survey goals. Our benchmarks are created using the *exact* text from these items. Even a slight change to a question or statement can alter the meaning enough to invalidate a comparison to the benchmark.  

   > [!IMPORTANT]
   > In cases where text is altered to sufficiently alter the item's meaning, the benchmark comparison is no longer valid and the items is now referred to as "customized," not "standard."
   > - For these items, create a copy of the standard item so that it isn't tied to an invalid benchmark for comparison.
   > - Customized items don't map to external benchmarks. For this reason, if you make a change to a standard survey item, duplicate the question and create a customized version. [Question mapping](/../../viva/glint/setup/question-mapping).

## Edit items from the Question Library 

Any item can be edited by hovering over and selecting the row that the item appears on in the Question Library. An **Edit Question** panel displays. From this panel, edit the item and view programs that have used this item.

1. Choose the language. Languages for which this item has been translated are visible in the dropdown menu. 
1. Edit the reporting label, if desired. 
1. Edit the item text, if desired. 
1. Add instruction text that helps the user understand the meaning of the item. 
1. Add comment placeholder text, if desired. 
1. Change the rating scale, if applicable. 
1. Indicate whether the rating label explanation should be shown. 
1. Enable or disable commenting. 
1. Choose whether the item is optional or mandatory.
1. Map the item to a Suggested Action Template, if desired. 
1. Select **Save Changes**. 

### Examples of edits that retain a valid benchmark comparison

There may be cases where slight edits to wording can be accommodated without altering the meaning. In these cases, benchmark data is retained.  

|Example|Standard|Modified|Recommendation|
|-------|--------|-------|-------|
|**1 - Matching the language of the business**| I would recommend my *manager* to others.|I would recommend my *supervisor* to others.| Modifying a term in the item to make it more specific to your organizational language is acceptable and doesn't affect the benchmark. Edit the standard item without creating a copy to retain the benchmark.| 
|**2 - Using synonyms**|The recruitment process was *excellent*.|The recruitment process was *great*.|If the replacement word is likely to be interpreted similarly, the item change is acceptable. Edit the standard item without creating a copy to retain the benchmark.|

### Examples of edits that don't retain a valid benchmark comparison

| Example | Standard | Modified | Recommendation |
|-------|--------|-------|-------|
| **1 - Altering the subject** | *I feel empowered* to make decisions regarding my work. | *My manager empowers me* to make decisions regarding my work. |  Altering the subject in an item changes the way people respond, and the benchmark will no longer be valid. Create a copy of the standard item and customize the copy so that there isn't an invalid benchmark tied to the edited item. |
| **2 - Altering the subject** | My manager *provides me with feedback that helps me improve my performance*. | My manager and *I have regular conversations*. | When the meaning of an item has been fundamentally altered, the change isn't recommended, and the benchmark is no longer valid. Create a copy of the standard item and customize the copy so that there isn't an invalid benchmark tied to the edited item. |

## View associated programs 

Use this tab to see if an item is being used with any existing program. To add it to a program, use the [Questions page in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231415). 

English is the default language for all Glint programs. Of course, you should survey and communicate to your employees in their preferred language. Glint provides its customers with more than many language translations for standard content. Language translations are set during the initial survey configuration in [General Settings](https://go.microsoft.com/fwlink/?linkid=2230744) or added later, as needed. 

## Add new items to the Question Library 

Select the **+ Create Question** button on the **Question Library** page. In the **Create Question** panel, edit the question. Upon completion, you see new item in the **Name** column, sorted alphabetically by key driver. 

## Language translations for Question Library items

> [!div class="languagetranslations"]
> [Manage language translations](https://go.microsoft.com/fwlink/?linkid=2286458)
   
## More resources

[Use this Learn guidance to understand question mapping](question-mapping.md)<br/>
[Change survey item IDs for expired survey cycles](/../../viva/glint/setup/change-item-id)





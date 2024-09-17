---
title: Manage language translations in Viva Glint programs 
description: Survey content and email communications should be sent to employees in their preferred language. Managing language translations is easy within Viva Glint program.
ms.author: JudithWeiner
author: JudyWeiner
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: language codes, language IDs
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/17/2024
---

# Manage language translations in Viva Glint programs 

English is the default language for all Microsoft Viva Glint programs, but admins can send surveys and email communications to employees in their preferred language. Glint provides customers with about 70 language translations for standard program content. Language translations are set during the initial survey configuration or added later as needed. Use Viva Glint's export/import option to review, add, or edit translations for survey emails and content (items, responses, survey text). 

There are four steps for language translations: 

1. Export content from the Viva Glint program into a *.csv* or *.xlsx* file 
2. Translate content 
3. Review translations 
4. Import content back into the Viva Glint program

> [!TIP]
> Find valid language codes for Viva Glint on the Language Codes tab of the Viva Glint [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533).

## Export survey and email text for translation

>[!IMPORTANT]
> The Glint system requires that one language document is initially exported and then imported back into the program before the process can be repeated for other languages.

1. Navigate to the survey program. 
2. From the **Actions** dropdown menu, select **Export Program Content**. 
3. Choose to export **email content**, **survey content**, or **both.**  
4. Select the languages you need from the **Languages to include** section. Options in this menu are based on your organization's default language and other languages selected for this survey program.
5. Select **Generate CSV**. 
6. From the file generated, make manual translations to import back into Viva Glint. 

>[!NOTE]
> Email content is downloaded as its own document. Survey content downloads as a zip file, with one file containing survey questions and text snippets.

## Translate Question Library items

Export the items. 
<br>From the file that has been generated: 

1. **Use a translator** to make exact changes to the items in column C for the approved English text from column B. 
1. To the right, consider other items which might require translation: reporting labels, multiple choice questions, and ratings labels.  
1. **Use a translation reviewer** to ensure that translated items match exactly to the approved item from the Question Library.

### Translater tips

|Do|Don't|
|-------|--------|
|Keep the translated content in the same cell and columns|Don't edit, translate, or delete any bracketed text such as {user first name}, `<COMPANY_NAME>` or {{company name}}. It must stay the same for personalization coding. There's no need to translate anything in brackets. If questions containing brackets are changed, ensure brackets around the text are balanced (one bracket at the start and one at the end, or two at the start and end).| 
|Ensure that there are no spaces added before or after the updated content|Don't make visual, format, or other stylistic changes unless it improves clarity. Changes shouldn't alter the meaning conveyed in the original English text. Don't add personal comments.|
|Ensure there is consistent punctuation at the end of sentences (that is, all using a period or none using a period)|Don't add personal comments.|
|Check for grammatical errors|Don't add new or additional columns or remove columns.| 

## Translation reviewer tips

|Do|Don't|
|-------|--------|
|Focus on copy-editing by fixing any typos or grammatical errors|Don't rewrite entire sentences|
|Confirm that the original meaning of the question remains intact|Don't move translated content to different cells or columns|
Keep translated content in the same cell and columns|Don't add personal comments|

## Import translated items back into the Glint platform

From the **Question Library** page, select **Import Questions** from the dropdown **Actions** menu. 

1. Drag and drop or browse to find the translated file and place it in the box indicated. 
1. Select **Next**. 
1. If everything looks as expected, select **Make Changes**.

> [!IMPORTANT]
> To prevent import errors, don't change any file name or column label in any exported files.


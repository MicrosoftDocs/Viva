---
title: Advanced Searching within Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 02/26/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: A guide to advanced search options that help you search for content within Viva Learning. 
---

# Advanced Search in Viva Learning

Use advanced search options in Viva Learning to narrow down and refine search results for specific content.

## Find an exact match

Find an exact learning content by using double quotes (“ “). 

Viva Learning matches the query with its exact match across fields like Title, Description and metadata like tags and additional keywords.
Only the exact matches are returned. Searching without quotes broadens the search with relevant search results. 

## Search using a query

You can search across multiple fields using your own queries to further refine search results:  

A query consists of two main parts

- Field Attributes
- Operators

### Field attributes

The following learning content attributes can be used by both admins and learners in queries:

|Attributes | Description|
|-----------|-----------|
|Title | The title of the learning content|
|Description| A description of the learning content|
|Author | The creator of the learning content|
|Provider| The name of the learning content provider. For example: LinkedIn Learning|
|Type| The type of learning content. For example: course, learning path, module|
|Duration| The Duration of the learning content in seconds|
|Source| The sub-source of the learning content in a provider|
|Premium| A true/false field indicating whether to include free or premium content|
|||

Searching for language attributes is not currently supported.

#### Metadata attributes 

The following attributes are available to Viva Learning knowledge admins. These are not visible to learners. 

|Attributes | Description|
|-----------|-----------|
|Id | The unique ID of the learning content from the external provider|
|LOId | The unique ID of a learning content in Viva Learning|
|ProviderId | The unique ID of a provider when registered with Viva Learning|
|Keywords | Set of keywords associated with a content |
|Skills | Skill tags asociated with content in Viva Learning |
|||

### Operators

You can combine field attributes using operators. Viva Learning supports the **OR** and **AND** operator. 
Operators are identified only if written in capital letters

- The **OR** operator refines searches through an either/or relation across fields or items.
- The **AND** operator broadens to include all attributes across fields and items (includes all)


>[!NOTE]
> The **NOT** operator is currently not supported. We are working on this capability for future releases.

#### Creating Queries 

Some attributes require exact match of all characters, upper-case, lower-case for the query to work correctly. 

These attributes are:

- Author
- Format
- Id
- LOId
- Premium
- Source

Some fields support approximate matching of queries. The exact match feature mentioned above can be used with these fields using double quotes. 
Using quotes in these fields will result in exact match in that field:

- Description
- Keywords
- Skills
- Title

Note the following considerations: 

- Parentheses or round brackets are needed to understand that there are multiple queries for a single attribute.
- Nested parentheses (parentheses inside parentheses) are not supported currently. Using this construction may give unexpected results.
- Using **AND** in some attributes may give empty results as the field may not support multiple values.
- There is no limit to the number of stacking queries. The only limit applied is the size of text box.


##### Single attribute queries

Use the following formats to search using an attribute for specific cases:

|Query type| Format | Example use case | Input| 
|------|-----|------|------|
|Single attribute| `<attribute>`:`<value>` | Search for content by an author | `Author`: `Firstname Lastname`|
Single attribute-multiple values using OR| `<attribute>`:`(<value1> OR <value2>)`| Search for content by either Author A OR Author B| `Author`: `(Author A  OR Author B)`|

##### Multiple attribute queries

You can combine multiple attributes and multiple values across attributes using **OR** and **AND** operators: 

1. Prepare a query for every attribute
1. Combine both the queries using the **OR** and **AND** operator.

Use the following formats to search using attributes for advanced filtering:

|Query type| Format | Example use case | Input|
|------|-----|------|------|
Multiple attribute - multiple value| `<attribute>`:`(<value> OR <value2>...)` AND/OR `<attribute>`:`(<value> OR <value2>...)`|Search for Modules (courses in Microsoft Learn) related to React (content having term in title)| `Title`: `(React)` AND `Type`:`(Module)`

#### Intuitive UI for advanced search options

We are working on improving our advanced search capabilities through an intuitive user interface and experience.

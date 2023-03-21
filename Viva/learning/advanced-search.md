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

Use the advanced search options in Viva Learning to expand and refine search results when looking for specific content.

## Find an exact match

Find an exact learning content by using double quotes (“ “). Viva Learning matches the query with its exact match across fields like Title, Description and metadata like skills and keywords.


## Find content using custom queries

You can search across multiple fields using your own queries to further refine search results:  

A query consists of two main parts

- [Field attributes](#field-attributes)
- [Operators](#operators)

## Field attributes

### User accessible attributes

The following learning content attributes can be used by both admins and learners in queries:

|Attributes | Description|
|-----------|-----------|
|Title | Title of the learning content|
|Description| Description of the learning content|
|Author | Creator of the learning content|
|Provider| Name of the learning content provider. For example: LinkedIn Learning|
|Type| Type of learning content. For example: course, learning path, module|
|Duration| Duration of the learning content in seconds|
|Source| Subsource of the learning content in a provider|
|Premium| Field indicating whether to include free or premium content designated by "True" or "False"|  
|Language| Language of the learning content in ISO format. For example: en-US|

### Admin accessible attributes 

The following attributes are available to Viva Learning knowledge admins. These aren't visible to learners. 

|Attributes | Description|
|-----------|-----------|
|Id | Unique ID of the learning content from the external provider|
|LOId | Unique ID of a learning content in Viva Learning|
|ProviderId | The unique ID of a provider when registered with Viva Learning|
|Keywords | Set of keywords associated with a content |
|Skills | Skill tags associated with content in Viva Learning |

## Operators

You can combine field attributes and values using operators. Viva Learning supports the **OR** and **AND** operator. 
Operators are identified only if written in capital letters

- The **OR** operator broadens searches through an either/or relation across attributes or values.
- The **AND** operator narrows to include only the attributes that are common across all attributes or values.


>[!NOTE]
> The **NOT** operator is currently not supported. We are working on this capability for future releases.

## Creating Queries 

When creating queries, some attributes require precise values while others support approximate values.

>[!IMPORTANT]
> 

The following attributes requires you to input precise values matching all characters, letter case, and spaces with the content in Viva Learning.

- Author
- Type
- Language
- Id
- LOId
- Provider
- ProviderId
- Premium
- Source

Some fields support approximate matching of queries. The [exact match](#find-an-exact-match) feature mentioned above can be used with these fields using double quotes.
Using quotes in these fields will result in exact match in that field:

- Title
- Description
- Skills
- Keywords



### Single attribute queries

Use the following formats to search using an attribute for specific cases:

|Query type| Format | Example |
|------|-----|------|
|Single attribute| `<attribute>`:`<value>` | `Author`: `Firstname Lastname`|
Single attribute-multiple values using OR| `<attribute>`:`(<value1> OR <value2>)`|`Author`: `(Author A  OR Author B)`|


Note the following considerations: 

- Parentheses or round brackets are needed to understand that there are multiple queries for a single attribute.
- Nested parentheses (parentheses inside parentheses) aren't supported currently. Using this construction may give unexpected results.
- Using **AND** in some attributes may give empty results as the field may not support multiple values.
- There's no limit to the number of stacking queries. The only limit applied is the size of text box.

#### Single attribute query examples


|Case| Sample Query |
|------|-----|
|Find content by a particular author | `Author: Lori Mullen`|
|Find content part of a learning path or module | `Type (Learning Paths OR Modules)`|
|Find content that is 10 minutes long| `Duration: 600`|
|Find content using IDs| `Id:(learn-bizapps.power-bi-admin-automate OR urn:li:lyndaCourse:3007803)` |


### Multiple attribute queries

You can combine multiple attributes and multiple values across attributes using **OR** and **AND** operators: 


1. Prepare a query for every attribute
1. Combine both the queries using the **OR** and **AND** operator.

Use the following format to search using attributes for advanced filtering:

|Query type| Format | Example|
|------|-----|------|
Multiple attribute - multiple value| `<attribute>`:`(<value> OR <value2>...)` AND/OR `<attribute>`:`(<value> OR <value2>...)`| `Title`: `(React)` AND `Type`:`(Module)`|

#### Multiple attribute query examples:


|Case| Sample Query |
|------|-----|
|Find specific content by a particular provider | `Provider: (Microsoft Learn) AND Title: (“React”)` |
|Find non-premium content in LinkedIn Learning| `Premium:(False) AND Provider:(LinkedIn Learning)`|
|Find modules that are either 10 or 15 minutes long| `Duration: (600 OR 900) AND Type: (Module)`|
|Find content by a specific author within a particular provider| `Author:(Lori Mullen) AND Provider:(LinkedIn Learning)` |

## Supported spaces

The advanced search capabilities are available to all learners and admins within Viva Learning application. The supported search spaces are: 

- Home tab 
- My Learning tab 
- Search results tab 
- Academy tab 
- Admin tab 
- Feature Set 
- Learning Paths 
- Manage Permissions 
- Manage Academy 

## Intuitive UI for advanced search options

We're working on improving our advanced search capabilities through an intuitive user interface and experience.

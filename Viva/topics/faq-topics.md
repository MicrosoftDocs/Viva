---
ms.date: 11/29/2021
title: Frequently asked questions about Microsoft Viva Topics
ms.author: ruthhollands
author: ruthholls
manager: pamgreen
audience: admin
ms.reviewer: cjtan
ms.topic: article
ms.collection: 
- m365initiative-viva-topics
- highpri
ms.service: viva 
ms.subservice: viva-topics 
search.appverid:
- MET150  
localization_priority: Normal
description: Read commonly asked questions and answers about using Microsoft Viva Topics.

---

# Frequently asked questions about Microsoft Viva Topics 

## Topic discovery and curation

### How are topics discovered and updated?

There are two ways that topics are discovered:

- Users can add topics manually.
- AI can identify topics automatically.

Once a topic is identified, AI can discover alternate names, description, related people and resources. For manually added topics, AI may also be able to enrich it with more content based on what has been added to the topic page. In addition, users can manually update topic pages to adjust the topic description or highlight new resources and connections. These scenarios are part of the human and AI story where machine learning and human curation together can build a better experience for end users. 
 
AI models are run in two steps:

- A pattern recognition that runs in a massively parallel manner on every update on every document to detect an initial set of candidate.
- An aggregation process that actually performs inferencing of topics and their metadata. Aggregation is executed in a centralized manner on a set of worker VMs.

The topics and metadata are updated incrementally as the changes are received in the system.

### How does Viva Topics work when discovering new topics?

Viva Topics builds an index similar to search, and relies on the SharePoint Online search crawler to keep the index up to date. The search crawler detects changes in SharePoint Online, performs basic parsing of various document formats; examples of this include files with the extensions: aspx, doc, docx, htm, html, mht, msg, one, pdf, ppt, pptx, pub, txt, xls, xlsx, visio. This list is subject to change as we learn more about what files are important to customers to include. We do not currently index image, video or audio file types. The file name, title, subject, author, last saved person, create date and its recent activities all play a role in contributing to the information used to discover topics. To inform suggestions for the topic description, people and resources, information from people and collaboration insights in the Microsoft Cloud that are available through [Microsoft Graph](/graph/overview) are used. Viva Topics observes existing content security features in Microsoft 365.

Viva Topics listens for changes in these documents, processing them for changes to the topics it has discovered. The main difference between Viva Topics and search is that Viva Topics builds a knowledge graph, not a full-text search index, making it possible to execute queries such as:

- Find all topics by name.
- Look up metadata of a given topic, such as alternative names.
- Find all related topics of a given topic. 

For more information about topic discovery and curation, see the following help articles:

- [Topic discovery and curation in Microsoft Viva Topics](topic-experiences-discovery-curation.md)
- [Create a new topic in Microsoft Viva Topics](create-a-topic.md)

## Security and compliance

### When data is being indexed and analyzed, where is it stored and how long is it stored?

The storage is a tenant-wide service separated by geographical regions. Viva Topics respects geo-sovereignty of the data it processes. The resulting topics and any intermediate state is shared into the corresponding regions where the data originates from.

For example, if topic A is identified from a file in NAM (North America), the topic will be present in the NAM region of the storage, with the corresponding relationship to the file and any metadata derived from it. In a multi-regional tenant, a single topic can span regions. Part of the topic can be physically stored in one region and another part can be stored in a different region, according to the origin of the underlying resources.

When content is migrated between regions, Viva Topics data structures are updated accordingly, so if a file is migrated from EUR to GBR, the corresponding topic metadata will follow and be removed from EUR and created in the GBR.

Viva Topics index metadata and state are kept as long as the underlying content is present in the tenancy, similar to search index. A topic is deleted when there is no evidence that contributes to the topic are present in the tenancy.

### Will data be decrypted or still be in encrypted form?

All the data is kept within the Microsoft 365 compliance boundary, which is encrypted at rest and in transit. The content is decrypted when being processed. When the data is written to storage, it will be encrypted according to the tenant configuration.

### How does Viva Topics protect security and compliance of content?

Viva Topics is based on the security and compliance of content enforced across Microsoft 365. For example, access, retention labels, data sovereignty, and information barriers are all maintained consistently before and after the activation of Viva Topics. Organizations can apply even more stringent restrictions on the scope and availability of topic information shared by Viva Topics.  
 
User permissions are enforced in a similar way to search. Users can only see metadata from topics if they have read permissions to at least one file or document where the metadata was derived from. Viva Topics maintains access control lists (ACLs) from the original content and checks permissions on every piece of topic metadata independently.

For more information about security and compliance, see the following help articles:

- [Security and privacy in Microsoft Viva Topics](topic-experiences-security-privacy.md)
- [Manage topic permissions in Microsoft Viva Topics](topic-experiences-user-permissions.md)
- [Security trimming in Microsoft Viva Topics](topic-experiences-security-trimming.md)

## User experience

### Will Viva Topics show topics highlighted when viewers compose documents or emails, when they receive an email, or when they read a completed document?

This part of the product is still evolving. SharePoint pages currently show topics to any reader. Email will show a rollup control, with appropriate opt-out by users. Topics can also be suggested to the user at authoring time.

### Does the knowledge manager or contributor need to have explicit access to all the SharePoint sites being indexed?

There is no requirement for the knowledge admin to have access to all sites, but it is helpful if the knowledge manager has sufficient access to perform knowledge organization in the tenancy. A contributor does not need to have any more access than is required to contribute to a particular topic.

### How does scanning happen on SharePoint pages, Word documents, PowerPoint slides, Outlook email, and so on, for Viva Topics to identify topic keywords and highlight for users?

Viva Topics relies on the search crawler for detecting changes and initial parsing of the document formats. Viva Topics only deals with text content, so all document formats are processed in the same way.

### Even if we decide not to transform our Topic Center into an app in Microsoft Teams, will Viva Topics appear in users’ chats?

Transforming your Topic Center into [an app](https://aka.ms/TopicsApp) now gives your users access to topics in Microsoft Teams before the Viva Topics integration (that is, topics appear in chats) in Teams is available. Once the integration is available, you won't need to keep the Topic Center app to see the integration.

For more information about the user experience, see the following help articles:

- [Get started with Microsoft Viva Topics](get-started-with-viva-topics.md)
- [Manage topics in the topic center in Microsoft Viva Topics](manage-topics.md)


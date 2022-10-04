---
published: true
layout: post
title: 'Demystifying Identifiers'
image: /images/posts/2022-09-06-demystifying-dentifiers.jpg
author:
  name: pascal
tags:
- API
- extensions
- metadata
---
Identifiers are used everywhere to be able to unambiguously reference resources. Examples, amongst many, include a passport number, a domain name, a book ISBN, a database record key, a UUID, a network card MAC address, a shortened URL, a string hash, a vehicle identification number, a digital object identifier, and the lkes. They play a fundamental role in the API, data, and metadata spaces.

When maintaining identiffers, whether handcrafted or code generated, or creating tools, database, and APIs, there are many aspects and facets that we need to consider. Here is a summary of the ones I can think of. 

- <i>Format</i>: an identifier should always be expressed as a string (even if its a numeric value). We never perform mathematical operations on identifiers.
- <i>Character Set</i>: Technically an identifier can use any character, but most systems and standards have restrictions. In my experience, to ensure an identifier works in most situations, only use alphanumeric characters, numbers, and underscore, and never start with a number.
- <i>Length</i>: the length of an identifier is typically influenced by its character set, uniqueness requirement, or algorithm (e.g. uuid, guid, hash). We ideally want identifiers to be as short as possible, as they may repeat many times and bloat up the size of resources, files, database, network traffic. Finding the right balance between length and clash probability is important
- <i>Case sensitivity</i>: Identifiers should always be case sensitive.
- <i>Persistence</i>: It is commonly expected for identifiers to exist for at least the lifetime of its underlying resource,  but often beyond as a resource may be deleted but its metadata or concept continues to exist. You may always want to keep track of identifiers to ensure it does not get reused.
- <i>Deletion</i>: Once published, an identifier should never be deleted, unless we know how to  remove all references using it. So this is typically only an option in the early existence of the identifier, or when used within a closed sandboxed environment.
- <i>Context</i>: An identifier always exists in a context that defines its uniqueness. We often talk about globally unique identifiers, which is commonly a desirable characteristic. Understanding the context of an identifier is important, so this should be properly documented.
- <i>Structure</i>: identifiers can sometimes be composed and multiple elements, which can be other identifiers (e.g. compound keys) or other keywords and metadata elements. This can be useful to broaden the scope of uniqueness or provide  details about the nature of the resource.
- <i>UR*</i>: There will likely be forever debate and confusion around URI, URN,  URL and IRI. I won’t solve that in one sentence. One point I would make is that, if you use a URL, it should return something. Otherwise there is no need for an identifier to have a protocol. I do like URNs, and I’m often guilty of using non-registered NIDs. But at the end of the day, an identifier is a unique string.
- <i>Multiplicity</i>: It is essential to keep in mind a resource can have many identifiers. There is nothing wrong with that and we do not need one to rule them all. Understanding which one to use depending on the context can be the challenge. Properties carrying identifiers (e.g. a JSON key) must as much as possible inform of the nature of the identifier (e.g by using namespaces or through schema documentation).
- <i>Physical vs Digital</i>: Identifiers equally apply to physical and digital resources. Don’t discriminate, use broadly.
- <i>Personal Identifiers</i>: some identifiers are sensitive in nature and on their own or when combined with other elements, may reveal the identity of individuals, companies, and other entities. These must be protected at all times. Statistical disclosure control techniques should be used to assess or reduce such risk when releasing data containing such information.
- <i>Generated vs Handcrafted</i>: Most of the time, you want identifiers to be machine/software generated, to minimize burde and ensure consistency (uniqueness, typos, etc.). Now it is common for humans to use an abbreviation or nickname for known resources, but this should then be captured as such (different property) or clearly recorded as a ‘user identifier’.
- <i>Generators</i>: algorithms, libraries, utilities, APIs should be made available to generate identifiers, with relevant documentation and guidance.
- <i>Registries</i>: When identifiers and resources live in disparate systems or locations, it is highly desirable to have a way to register them for discovery and resolution purposes. Establishing a central or distributed registries, equipped with proper APIs, 
- <i>Resolvers</i>: Identifiers should not exist without a mechanism in place to retrieve the underlying resources. Note that this may not always return the actual resource due privacy or accessibility constraints. But the metadata associated with the identifier should however always provide information describing access modalities. Ideally this should always be machine actionable. 

I’m designing metamodels and implementing tools and APIs based on these needs and principles. Let me know what I missed and if you have any thoughts, comments, suggestions!
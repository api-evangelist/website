---
published: true
layout: post
title: 'Taking Inventory: APIs Are Defined As API Contracts'
tags:
  - Strategy
  - Contract
  - APIs.jso
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-under-socialism-factory-road.jpg
---
An API contract represents a shared machine-readable understanding of the business and technical requirements established between the producer and consumers of programmatic interfaces used across desktop, web, mobile, device, and artificial intelligence applications. API contracts are defined as a combination of APIs.json for the business definition and OpenAPI as the technical definition, along with other supporting human and machine-readable artifacts rounding off a contract. API contracts go beyond the current notion of API discovery and catalogs and is more about taking inventory of digital resources and capabilities used to operate the enterprise.

[APIs being defined as API contracts(https://github.com/api-search/search-api?tab=readme-ov-file#api-contract-for-the-apisio-search-api)] means that all of the needs of business and engineering are accounted for. API contracts inventory and organizes all of the digital resources and capabilities used to power desktop, web, mobile, device, and AI applications. API contracts give us the ability to organize our APIs into useful and relevant bounded contexts with the following metadata:

- **Identifiers** - Each grouping of APIs possesses a unique identifier that allows it to be easily referenced, organized, and used to identify APIs.
- **Name** - What is the name of the bounded context for a grouping of APIs, logically breaking down where they fit into the business.
- **Description** - Providing more detail about this bounded context and where it fits in with business and provides value to consumers.
- **Image** - Offering a visual representation of a collection, helping make a richer first impression during discovery and working with contracts.
- **Types** - Allowing for indexing APIs for discovery, providing blueprints, base templates, and providing producer and consumer contracts.
- **Tags** - Keywords and phrases that help shape the bounded context a group of APIs is being organized and made available  by.
- **Timestamps** - Defining when a contract was initiated and tracking each change being made to any of the APIs being showcased.
- **APIs** - Organizing one or many APIs within a contract defining each APIs metadata, properties, and relevant parts for overall contract.
- **Maintainer** - The individual or team responsible for maintaining the contract and is acting as librarian and key stakeholder in contract.
- **Includes** - Other API contracts that are relevant to a contract, referring supporting APIs, or others related to team or line of business.

Each API contract is an accounting of digital resources and capabilities applied within a specific domain, line of business, or other relevant enterprise bounded context. You can think of this in the context of an API product catalog, but this is a more fundamentally about operations than that. API contracts represent all of the raw resources, 3rd-party resources, and digital capabilities that are used across the enterprise. API contracts are how you take inventory, and then you can use it to shape portals, product catalogs, and other resources. API contracts are how you make sure you know where all the APIs are that you use and have created, and ensure they possess the business and technical needed to properly use a resource or capability in any part of the business.

The existence of an API contract can be validated as part of governance, as well as each of the properties listed above. Every API, internal, partner, or 3rd-party should be included in at least one API contract, and should be validated for all of the properties listed above. API contract inventory should live in source control, but then synced with API portals, catalogs, and other business or engineering infrastructure and services using APIs and WebHooks automated through CI/CD, CRON Jobs, or other means. API contracts make sure you have your enterprise digital supply chain in order, as well as the business and technical details needed to operate your digital factory floor—then contracts can be used to govern wholesale and retail distribution of your digital resources and capabilities to consumers.
---
published: true
layout: post
title: 'What API Common Schema Are Needed for APIs.json Properties and Overlays'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-seatlle-shipping-mountain.jpg
author:
    name: kinlane
tags:
- APIs.json
- API Commons
- Schema
- Properties
- Overlays
---
I am beginning to do work on what Steve and I have negotiated as the next generation of [API Commons](http://apicommons.org/). As I do with most of my work, I’ll be doing it out in the open, working through my thoughts here on API Evangelist. [The API Commons emerged to provide a licensing schema after it was clear that API copyright was going to the base line in the United States back in 2014](https://apievangelist.com/2021/04/13/My-oracle-vs-google-api-copyright-journey/). In 2024 we’d like to continue to do the licensing work, but also begin work on the other schema that will be needed to automate discovery and integration across the API landscape. 

The vision for the next generation of the API Commons is to make it where the essential human-readable building blocks of API operations are transformed into machine-readable ones. This is something that will help us automate and orchestrate better across the API sprawl that has emerged, and do for API operations what OpenAPI did for APIs. In addition to OpenAPI, and the other existing machine-readable API artifacts out there, we are looking to begin investing in v2.0 of API Commons licensing, but also introduce a suite of v1.0 schemas.

## Common Schema
The purpose of the commons is to identify the most common building blocks used as [APIs.json](https://apisjson.org) properties and ensure they are available in not just human-readable formats, but also machine-readable ones that can be used to automate onboarding and integration with APIs by any application, system, or agent.

- **Getting Started** - The distilled down steps you need to onboard with an API. 
- **Authentication** - How you obtain your application and keys used for authentication.
- **Pricing** - The business details of what it will cost you to actually put the API to use.
- **SDKs** - Sharing what code is available to use when it comes to integrating with an API.
- **Interface License** - The legal side of integrating an API into your applications.
- **Road Map** - The details of what is being planned for the future of an API.
- **Change Log** - the details of what has changed for each version of an API over time.

[I already have a schema for all of these](https://github.com/api-search/developer-portal/tree/main/_data). They aren’t complicated. I just need to get them standardized and presented as part of the API Common GitHub organization and published to a new version of the website. I am not worried about them not being perfect—-I am just looking to get the conversation started.

## Community Schema
As inspiration for the common schema, there are a range of existing artifacts in use across API providers to describe the surface areas of their APIs, which end up being published as APIs.json properties. These machine-readable artifacts are providing the technical details of what each API can do, and are increasingly used to power documentation, but also [being shared by providers via GitHub](https://apievangelist.com/2024/03/31/using-github-to-manage-your-openapis/) and other channels.

- **AsyncAPI** - Providing an artifact to describe our event-driven API infrastructure.
- **RSS / Atom Feed** - A good ol Atom or RSS feed for our blog or other property.
- **GraphQL Schema** - A GraphQL schema describing the graph APIs we make available.
- **JSON Schema** - Allowing us to define and validate the objects we pass back and forth.
- **OpenAPI** - Providing an artifact to describe our request and response API infrastructure.
- **Postman Collection** - Publishing collections that can be used in the Postman API client.
- **WADL** - Providing a way for legacy systems to express the surface area in XML.
- **WSDL** - Utilizing the WSDL that is published by legacy systems that are still in use.

One thing that all of these schemas have in common is that they describe the technical bits of our APIs. The API Commons wants to leave this technical specification work to the existing players. The API Commons is looking to translate the benefits these specifications have brought to APIs, but more evenly spread it across API operations, benefiting API discovery as well as other stop along the entire API lifecycle.

## Vendor Overlays
Overlapping with the properties in which common and community schema deliver value, I’d like to find a way to shine a light on the potential of [APIs.json overlays](https://apisjson.org/2024/02/24/a-proposal-for-apis-json-version-017/) when it comes to the enrichment of API operations. I have fleshed out the APIs.json overlay property using [APIs.io Search](https://apis.io), as well as API Evangelist Ratings, but I’d like to quickly evolve to address all of these essential areas:

- **Search** - Fine tuning the names, summaries, descriptions, and tags to improve discovery.
- **Ratings** - Applying a variety of Spectral-driven rules which each carry different points.
- **Security** - Looking at the security of APIs, and providing a summary of what is found.
- **Testing** - Executing contracts and other types of tests and overlaying the results.
- **Monitoring** - Keeping an eye on the uptime and performance of APIs being indexed.
- **SDKs** - Defining what software development kits are available for integrating with APIs.
- **Localization** - Providing translation of names, summaries, descriptions, and tags for APIs.

These are just a handful of the introductory areas we’d like to see vendor overlays being invested in as part of the commons. We are confident that an open source set of schema defining these areas of our API operations combined with the commercial services brought to the table by vendors can coexist and be used to power API operations.

## Rebooting the API Commons
Now that we got the [latest proposal for APIs.json v.17](https://apisjson.org/2024/02/24/a-proposal-for-apis-json-version-017/) out the door including some new properties and the overlays property, we are turning to rebooting the [API Commons](http://apicommons.org/). We will continue to push forward the APIs.json standard using the index of public APIs we are assembling under the project name—Artisanal. However, we need to begin work on establishing a common set of machine-readable artifacts we can use to build indexes of the most common building blocks you find across the APIs we index. We also need to begin putting more structure in place around the concept of APIs.json overlay, building on what we provide with APIs.io search and API Evangelist ratings overlays. 

The API Commons is just the side project of Steve Willmott and I. We are both finding some renewed energy for the APIs.json specification, but also the APIs.io search engine which is powered by APIs.json. API Commons is an essential part of this work. Next, we’ll have a new version of the website published, and individual GitHub repositories, JSON Schema, and documentation for each of the common schemas. We’ll also refine how we talk about community schema and vendor overlays across apis.json and API Commons. This blog post is intended to just gather the thoughts around the information architecture for the new API Commons strategy website, as well as the overlap with the wider APIs.json work.
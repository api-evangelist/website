---
published: true
layout: post
title: 'Taking A Fresh Look At The Nuance Of API Search'
date: 2019-07-11T09:00:00.000Z
tags:
  - API Evangelist
  - Search
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/stories-beach-rocks-currents-internet-numbers.jpg
author:
 name: kinlane
tags:
    - None
---
I have a mess of APIs.json and OpenAPI definitions I need to make sense of. Something that I could easily fire up an ElasticSearch instance, point at my API “data lake”, and begin defining facets and angles for making sense of what is in there. I’ve done this with other datasets, but I think this round I’m going to go a more manual route. Take my time to actually understand the nuance of API search over other types of search, take a fresh look at how I define and store API definitions, but also how I search across a large volume of data to find exactly the API I am looking for. I may end up going back to a more industrial grade solution in the end, but I am guessing I will at least learn a lot along the way.

I am using API standards as the core of my API index—APIs.json and OpenAPI. I’m importing other formats like API Blueprint, Postman, RAML, HAR, and others, but the core of my index will be APIs.json and OpenAPI. This is where I feel solutions like ElasticSearch might overlook some of the semantics of each standard, and I may not immediately be able to dial-in on the preciseness of the APIs.json schema when it comes to searching API operations, and OpenAPI schema when it comes to searching the granular details of what each individual API method delivers. While this process may not get me to my end solution, I feel like it will allow me to more intimately understand each data point within my API index in a way that helps me dial-in exactly the type of search I envision.

The first dimensions are of my API search index are derived from APIs.json schema properties I use to define every entity within my API search index:

- **Name** - The name of a company, organization, institution, or government agency.
- **Description** - The details of what a particular entity brings to the table.
- **Tags** - Specific tags applied to an entity, or even a collection of entities.
- **Kin Rank** - What Kin thinks of the entity being indexed with APIs.json.
- **Alexa Rank** - What Alex thinks of the entity being indexed with APIs.json.
- **Common Properties** - Using common properties like blog, Twitter, and GitHub.
- **Included** - Other related APIs that are included within the index.
- **Maintainers** - Details about who is the maintainer of the API definition.
- **API Name** - The name of specific API program or project that an entity possesses.
- **API Description** - The details of a specific API program or project that an entity possesses.
- **API Tags** - How the individual API program or project is tagged for organization.
- **API Properties** - The details of specific properties of an API like documentation, pricing, etc.

After indexing the 100K view with APIs.json, providing references to the different layers of API operations, I’m indexing the following OpenAPI schema properties:

- **Title** - The title of an individual API program or project that an entity possesses.
- **Description** - The description of an individual API program or project that an entity possesses.
- **Domain** - The subdomain, or top level domain that an API operates within.
- **Version** - The version of each individual API.
- **Tags** - The tags that are applied to a specific API program or project that an entity possesses.
- **API Path** - The actual path of each API.
- **API Method Summary** - The summary for an individual API method.
- **API Method Description** - The description for an individual API method.
- **API Method Operation ID** - The operation id for an individual API method.
- **API Method Query Parameters** - The query parameters for an individual API method.
- **API Method Headers**  - The headers for an individual API method.
- **API Method Body** - The body of an individual API method.
- **API Method Tags** - The tags applied to each individual API methods.
- **Schema Object Name** - The name of each of the schema objects.
- **Schema Object Description** - The description of each of the schema objects.
- **Schema Properties** - The properties of each of the schema objects.
- **Schema Tags** - The tags of each of the schema objects.

These details provide to be by the OpenAPI definition for each API provides me with the long tail of my search, going beyond just the names and description of each API, allowing me to turn on or turn off different facets of the OpenAPI specification when indexing, and delivering search results.  My biggest challenges in building this index center around:

- **Completeness** - I struggle with being able to invest the resources to properly complete the profile for each API.
- **Inconsistency** - Navigating the inconsistency of APIs, trying to nail down a single definition across thousands of the is hard.
- **Performance** - The performance of basic JavaScript search against such a large set of YAML / JSON documents isn’t optimal.
- **Accuracy** - The accuracy of API methods is difficult to ascertain without actually getting a key and firing up Postman, or other script.
- **Up to Date** - Understanding when information has become out of date, obsolete, or deprecated is a huge challenge with search.

Right now I have about 2K APIs defined with APIs.json, with a variety of OpenAPI artifacts to support. With more coming in each day through my search engine spiders, trolling GitHub and the open web for signs of API life. I’m working to refine my current index of APIs, making sure they are complete-enough for making available publicly. Then I want to be able to provide a basic keyword search tool, then slowly add each of these individual data points to some sort of advanced filter setting for this search tool. I’m not convinced I’ll end up with a usable solution in the end, but I convinced that I will flesh out more of the valuable data points that exist within an APIs.json and OpenAPI index.

This prototype will at least give me something to play with when it comes to crafting a JavaScript interface for the YAML API index I am publishing to GitHub. I feel like these API search knobs will help me better define my search index, and craft cleaner OpenAPI definitions for use in this API search index. As the index grows I can dial in the search filters, and look for the truly interesting patterns that exist across the API landscape. Then I’m hoping to add an API ratings layer to further help me cut through the noise, and identify the truly interesting APIs amidst the chaos and trash. Not all APIs are created equal and I will need a way to better index, rank, and then ultimately search for the APIs I need. While also helping me more easily discover entirely new types of APIs that I may not notice in my insanely busy world.

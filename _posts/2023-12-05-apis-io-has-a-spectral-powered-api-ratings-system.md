---
published: true
layout: post
title: 'Using Spectral As An API Ratings System'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/bf-skinner-fox-oakland-day.jpeg
author:
    name: kinlane
tags:
- API
- Ratings
- Spectral
- Scores
---
When Steve asked me what we could do with [APIs.io](https://apis.io), I knew I wanted to improve upon what APIs.io v1 was as an API search, but I also lay the groundwork for what we need to help alleviate our API discovery pain. Every time I have made an investment in API discovery over the last decade, I also find myself considering what constitutes a good API, as well as a bad API, but also effectively dealing with the change that is inevitable across the API landscape. I knew that search would be important for the new APIs.io, something I”ll write a separate post about, but I new that an APIs rating system for APIs.io would play just as an important of a role.

APIs.io has a ratings API which the engine uses to rate the APIs.json as well as the APIs that are indexed within them. This API ratings system is defined and driven using the open source API listing tool Spectral. The open source Spectral is best known for listing OpenAPI and AsyncAPI, but it will work for any JSON or YAML schema, so we [developed a base set of rules for APIs.json](https://apis.io/rules/). Effectively linting not just your API, but your API operations. There is a Spectral rule for each APIs.json property, spanning potentially multiple APIs, but also the variety of properties of those APIs like having a sign up page, documentation, plans, terms of service, SDKs, and other common building blocks of our public and private API portals. 

We have Spectral rules for linting the APIs.json, as well as OpenAPIs that are indexed for any API. We will eventually develop Spectral rules for AsyncAPI, JSON Schema, and other machine-readable properties. Each Spectral rule has points associated with it. Right now we have applied scores based upon my gut feeling as we crafted each rule, but it is something we will adjust over time to “dial-in” the ratings algorithm—rewarding the API operational patterns that matter the most. We am running the rules against all APIs indexed via APIs.io every week, so we will have a record over time regarding how an API has increased or decreased its overall rating based upon things inside and outside the control of each API producer.

We am using Spectral to map the positive patterns we are looking for from API producers, then identify which of those patterns are present across many API producers. This is different than the way it is used for API governance, where you tend to highlight the patterns that are missing from an API. It is easy to quickly adapt the Spectral rules applied to API operations using APIs.json to help guide API producers when it comes to adding common building blocks, or essentially governing the delivery of an API across the API lifecycle. We will spend time grouping rules into different areas of the common API lifecycle, platform, or other view of our API operations to help reduce cognitive load when it comes to rating each API.

We are just getting started. We have 73 APIs.json for top API producers, indexing 215 APIs and growing. Right now we are [hand-crafting artisanal APIs.json for providers](https://github.com/apis-json/artisanal) to push forward the index as well as the ratings system. Over time API producers can begin maintaining their own APIs.json and we can focus exclusively on the Spectral powered API ratings system. Our goal with this wave of work was to prove the concept out, demonstrate the rating of APIs.json and OpenAPI, and then use to power the search ordering for APIs.io. Next we’ll focus on better coverage across the individual as well as common API properties we’ve identified across the 73 API producers we’ve indexed, and better organize and score each Spectral rule, until we find the optimal approach to rating APIs.
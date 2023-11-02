---
published: true
layout: post
title: 'Exploring an Idea for an APIs.json Defined Workflow'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-under-socialism-water-fountain-many-shooting.jpg
author:
    name: kinlane
tags:
- Workflows
- OpenAPI
- APIs.json
- Scripts
- Automation
---
I have been thinking deeply about API workflows lately. Meaning, how do you chain API requests together in a certain order. There are many valuable API resources available out there that become even more valuable once you bundle them together. API workflows start with single APIs, maybe paginating through results or searching for results, then incrementally pulling detail pages. Then there are API workflows spanning multiple APIs where you can really start seeing the value of API interoperability, such as crawling the web and harvesting data via scraping APIs, then publishing results to AWS S3, and organizing via your CMS APIs. Individual APIs are the individual Lego building blocks, and API workflows with many APIs are how you build more meaningful sets of Lego villages and spaceships. 

The OpenAPI Initiative (OAI) community is doing great work in their [workflows special interest group](https://github.com/OAI/sig-workflows), which I’ll be tuning into when it comes to defining API workflows using OpenAPI. However, like the [SLA for the OpenAPI specification](https://github.com/isa-group/SLA4OAI-Specification), I think we are hanging too much on the OpenAPI specification. I get it, OpenAPI is the hello world API spec for folks, but JSON Schema, AsyncAPI, and other specs are shaping the landscape too. I am biased, because I believe that [APIs.json](https://apisjson.org/) should be the layer where we hang all of these building blocks of API operations. With this bias, I have been thinking hard about how APIs.json can also support API workflows by approaching from a slightly different direction. 

Using APIs.json you can organize one or more APIs, with a mix of properties like OpenAPI-—ordering many different APIs in a specific order, which could be executed, using the OpenAPI as the definition, keeping each API a modular, reusable, and separate OpenAPI definition. 

```
name: Workflow API
description: This is a workflow API, chaining multiple APIs together.
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
tags:
- API
- Workflows
created: ‘2023-10-31’
modified: ‘2023-10-31’
url: http://example.com/apis.json
specificationVersion: '0.16’
apis:
- name: API One
  description: This is the first API in my workflow.
  image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: http://example.com
  baseURL: http://api.example.com
  tags:
  - Step One
  properties:
  - type: openapi
    url: http://example.com/openapi.json
- name: API Two
  description: This is the second API in my workflow.
  image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: http://example.com
  baseURL: http://api.example.com
  tags:
  - Step Two
  properties:
  - type: openapi
    url: http://example.com/openapi.json
maintainers:
- FN: Kin Lane
  X-twitter: apievangelist
  email: info@apievangelist.com
```

The challenge here, which is something being solved in different ways by different providers, centers around how you daisy chain each of these calls together, mapping JSON properties from each response with the input parameters for the following response. I feel like this isn’t how you would want to tackle this problem in a variety of situations.  I feel like there should just be a central data "store" property for APIs.json that I can reference when each step in the workflow occurs.

```
name: Workflow API
description: This is a workflow API, chaining multiple APIs together.
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
tags:
- API
- Workflows
created: ‘2023-10-31’
modified: ‘2023-10-31’
url: http://example.com/apis.json
specificationVersion: '0.16’
apis:
- name: API One
  description: This is the first API in my workflow.
  image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: http://example.com
  baseURL: http://api.example.com
  tags:
  - Step One
  properties:
  - type: openapi
    url: http://example.com/openapi.json
- name: API Two
  description: This is the second API in my workflow.
  image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: http://example.com
  baseURL: http://api.example.com
  tags:
  - Step Two
  properties:
  - type: openapi
    url: http://example.com/openapi.json
store:
  key1: Seed Data 	
  key2: Response Data
maintainers:
- FN: Kin Lane
  X-twitter: apievangelist
  email: info@apievangelist.com
```

With a central data store, I can just add scripts to each APIs properties that would execute as a pre-request or post-request for each step in the workflow. The OpenAPI and script for each step in the workflow would live as separate properties for each step, that the workflow engine can use to make things work.

```
name: Workflow API
description: This is a workflow API, chaining multiple APIs together.
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
tags:
- API
- Workflows
created: ‘2023-10-31’
modified: ‘2023-10-31’
url: http://example.com/apis.json
specificationVersion: '0.16’
apis:
- name: API One
  description: This is the first API in my workflow.
  image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: http://example.com
  baseURL: http://api.example.com
  tags:
  - Step One
  properties:
  - type: openapi
    url: http://example.com/openapi.json
  - type: pre-request-script
    url: http://example.com/script.js
  - type: post-request-script
    url: http://example.com/script.js
- name: API Two
  description: This is the second API in my workflow.
  image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: http://example.com
  baseURL: http://api.example.com
  tags:
  - Step Two
  properties:
  - type: openapi
    url: http://example.com/openapi.json
  - type: pre-request-script
    url: http://example.com/script.js
  - type: post-request-script
    url: http://example.com/script.js
store:
  key1: Seed Data 	
  key2: Response Data
maintainers:
- FN: Kin Lane
  X-twitter: apievangelist
  email: info@apievangelist.com
```
The workflow engine can provide a JSON path library for use within scripts that allow you to pull data from, as well as publish data to your central data store. You could use it to store the data harvest making a series of paginated API requests. Now you don’t have to daisy chain API calls together, you just bundle OpenAPI and scripts in a certain order, and push and pull data from your central JSON key value store. This just seems like a scrappier approach to defining API workflows without having to create dependencies between your APIs, keeping all your digital resources decoupled, while still being able to orchestrate workflows across them.

I will play with a couple of APIs.json defined workflows to demonstrate what I am talking about. Then I will publish a simple APIs.json workflow engine API to execute. I am looking to use the specification to define my workflows, explain the business value they deliver, as well as provide the technical details of each API request, while leveraging and cultivating a central data store that informs and shapes the API workflow. I like this modular and reusable approach that keeps my API resource separated, keeping my OpenAPI and pre-request and post-request scripts script, but also potentially my JSON Schema I would use to validate, and Spectral rules I’d use to govern the workflow. There are a lot of possibilities here, but I need to validate my idea with a working prototype, otherwise it is just API blah blah blah.
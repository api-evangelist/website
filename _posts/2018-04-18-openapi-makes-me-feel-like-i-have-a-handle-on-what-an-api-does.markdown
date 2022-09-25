---
published: true
layout: post
title: OpenAPI Makes Me Feel Like I Have A Handle On What An API Does
date: 2018-04-18T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Documentation
  - Communication
  - Collaboration
image: 'https://s3.amazonaws.com/kinlane-productions/openapi/OpenAPI_Pantone.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>APIs are hard to talk about across large groups of people, while ensuring everyone is on the page. APIs don't have much a visual side to them, providing a tangible reference for everyone to use by default. This is where OpenAPI comes in, helping us "see" an API, and establish a human and machine readable document that we can produce, pass around, and use as a reference to what an API does. OpenAPI makes me feel like I have a handle on what an API does, in a way that can actually have a conversation around with other people--without it, things are much fuzzier.

Many folks associate OpenAPI with documentation, code generation, or some other tooling or service that uses the specification--putting their emphasis on the tangible thing, over the definition. While working on projects, I spend a lot of time educating folks about what OpenAPI is, what it is not, and how it can facilitate communication across teams and API stakeholders. While this work can be time consuming, and a little frustrating sometimes, it is worth it. A little education, and OpenAPI adoption can go a long way to moving projects along, because (almost) everyone involved is able to be actively involved in moving API operations forward.

Without OpenAPI it is hard to consistently design API paths, as well as articulate the headers, parameters, status codes, and responses being applied across many APIs, and teams. If I ask, "are we using the sort parameter across APIs?" If there is no OpenAPI, I can't get an immediate or timely answer, it is something that might not be reliably answered. Making OpenAPI a pretty critical conversation and collaboration driver across the API projects I'm working on. I am not even getting to the part where we are deploying, managing, documenting, or testing APIs. I'm just talking about APIs in general, and making sure everyone involved in a meeting is on the same page when we are talking about one or many APIs. 

Almost every API I'm working on starts as a basic OpenAPI, even with just a title and description, published to a Github, Gitlab, Bitbucket, or other repository. Then I usually add schema definitions, which drive conversations about how the schema will be accessed, as we add paths, parameters, and other details of the requests, and responses for each API. With OpenAPI acting as the guide throughout the process, ensuring we are all on the same page, and ensuring all stakeholders, as well as myself have a handle on what is going on with each API being developed. Without OpenAPI, we can never quite be sure we are all talking about the same thing, let alone having a machine readable definition that we can all take back to our corners to get work done.

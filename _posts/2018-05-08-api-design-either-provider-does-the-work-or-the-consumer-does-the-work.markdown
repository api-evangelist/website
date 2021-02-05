---
published: true
layout: post
title: 'API Design, Either the Provider Does the Work or the Consumer Will Have To'
date: 2018-05-08T09:00:00.000Z
tags:
  - API Evangelist
  - Design
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/109_201_800_500_0_max_0_1_-5.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm always fascinated by the API design debate, and how many entrenched positions there are when it comes to the right way of doing it. Personally, I don't see any right way of doing it, I just see many different ways to put the responsibility on the provider or the consumer shoulders, or sharing the load between them. I spend a lot of time profiling APIs, crafting OpenAPI definitions that try to capture 100% of the surface area of an API. Something that is pretty difficult to do when you aren't the provider, and you are just working from existing static documentation. It is just hard to find every parameter and potential value, exhaustively detailing what is possible when you use an API.

When designing APIs I tend to lean towards exposing the surface area of an API in the path. This is my personal preference for when I'm using an API, but I also do this to try and make APIs more accessible to non-developers. However, I regularly get folks who freak out at how many API paths I have, preferring to have the complexity at the parameter level. This conversation continues with the GraphQL and other query language folks who prefer to craft more complex queries that can be passed in the body, to define exactly what is desired. I do not feel there is a right way of doing this, but it does reflect what I said early about balancing the load between provider and consumer.

The burden for defining and designing the surface area of an API resides in the providers court--only the provider truly knows the entire surface area. Then I'd add that when you offload the responsibility to the consumer using GraphQL, you are limiting who will be able to craft a query, putting API access beyond the reach of business users, and many developers. I feel that exposing the surface area of an API in the URL makes sense to a lot of people, and puts it all out in the open. Unless you are going to provide every possible enum value for all parameters, this is the only way to make 100% of the surface area of an API visible and known. However, depending on the complexity of an API, this is something that can get pretty unwieldy pretty quickly, making parameters the next stop be defining and designing the surface area of your API. 

I know my view of API design doesn't sync with many API believers, across many different disciplines. I'm not concerned with that. I'm happy to hear all the pros and cons of any approach. My objective is to lower the bar for entry into the API game, not raise the bar, or hide the bar. I'm all for pushing API providers to be more responsible for defining the surface area of their API, and not just offloading it on consumers to do all the work, unless they implicitly ask for it. In the end, I'm just a fan of simple, elegantly designed APIs that are intuitive and well documented using OpenAPI. I want ALL APIs to be accessible to everyone, even non-developers. I want them accessible to developers, minimizing the load on them to understand what is happening, and what all the possibilities are. I just don't want to spend too much time on-boarding with an API. I just want to go from discovery to exploration in as little time as possible.

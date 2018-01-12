---
published: true
layout: post
title: "API Transit Basics: SDKs\t"
date: 2018-01-12T11:00:00.000Z
tags:
  - API Evangelist
  - SDK
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-sdk.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-sdk.png" align="right" width="45%" style="padding: 15px;" /></p>Software Development Kits (SDKs), and code libraries in a variety of programming languages have always been a hallmark of API operations. Some API pundits feel that SDKs aren't worth the effort to maintain, and keep in development alongside the rest of API operations, while others have done well delivering robust SDKs that span very valuable API stacks--consider the AWS JavaScript SDK as an example. Amidst this debate, SDKs continue to maintain their presence, and even have been evolving to support a more continuous integration (CI) and continuous deployment (CD) approach to delivering APIs and the applications that depend on them.

Supporting SDKs in a variety of programming languages can be difficult for some API providers. Luckily there is tooling available that help auto-generate SDKs from API definitions, helping make the SDK part of the conversation a little smoother. Of course, it depends on the scope and complexity of your APIs, but increasingly auto-generated SDKs and code as part of a CI/CD process is becoming the normal way of getting things done, whether you are just making them available to your API consumers, or you are actually doing the consuming yourself.

- [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) - The leading open source effort for generating SDKs from OpenAPI.
- [APIMATIC](https://apimatic.io/) - The leading service for generating SDKs from OpenAPI, and including as part of existing CI/CD efforts.
- [RESTUnited](https://restunited.com/) - The easiest way to generate SDKs (REST API libraries):
PHP, Python, Ruby, ActionScript (Flash), C#, Android, Objective-C, Scala, Java

Depending on your versioning and build processes, SDK generation can be done alongside all the other stops along this life cycle. When you iterate on an API, you simply auto-generate documentation, tests, SDKs, and other aspects of supporting your services. Not all providers I talk with are easily able to jump into the aspect of producing code, as their build processes aren't as streamline, and some of their APIs are too large to expect auto-generated code to perform as expected. However, it is something they are working towards, along with other microservices, and decoupling efforts going on across their teams.

Once you realize an API definition driven approach to delivering APIs, the line between deployment and SDKs blurs--it is all about generating code from your definitions. Sometimes the code is providing resources, and other times it is consuming them. It just comes down to whether you are deploying code server or client side. Another significant shift I'm seeing in the landscape with SDKs, are things moving beyond just programming languages, and providing platform specific libraries for managing SalesForce, AWS, Docker, and other common components of our operations--further evolving the notion of what an SDK is and does in 2018.

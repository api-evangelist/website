---
published: true
layout: post
title: 'Standardizing and Templatizing API Design Editor Validation Tips'
date: 2017-07-06T09:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/apicurio/apicurio-feedback-loop.png
---
<p><a href="http://www.apicur.io/"><img src="https://s3.amazonaws.com/kinlane-productions/apicurio/apicurio-feedback-loop.png" align="right" width="40%" style="padding: 15px;" /></a></p>I've been playing with [Apicurio](http://www.apicur.io/), the [open source API design editor I've been waiting for](https://apievangelist.com/2017/05/30/apicurio-is-the-open-source-api-editor-i-was-looking-for/), and saw a potential opportunity for design time collaboration, instruction, and feedback loop. When you are designing an API in Apicurio it gives you alerts based upon JSON schema validation of the underlying OpenAPI, providing a nice visual feedback loop--forcing you to complete your API definition until it properly validates.

Visual alerts and feedback based upon JSON schema validation isn't really new or that interesting--you see it in the Swagger Editor, and many other JSON tooling. Where I see an opportunity is specifically when it comes to an open source visual API design editor like Apicurio, and when the JSON schema engine for the validation responses is opened up as part of the architecture. Allowing users to import and export JSON schema that goes beyond the default OpenAPI schema, which gets us to a minimum viable OpenAPI definition--while this is good, we can do better.

I'd like to see a marketplace of JSON schema to emerge helping API designers and architects push the completeness and precision of their OpenAPI definitions beyond the speed at which the core OpenAPI spec can move, and go in directions, and cover niche definitions that the core OpenAPI schema will never cover. I want to be able to load a schema that will help me push forward my API responses beyond just a default 200. I want to be able to load custom JSON schema crafted by API design experts who have more skills than I do, and learn from them. I want my API design editor to help me take my APIs to the next level, while also be pushing my API design skills forward along the way.

Apicurio takes does a good job at giving plain english responses to validation errors--much better than some tools I've used. You can click on the detail of each alert, to get more information about what is going on. I could see this entire structure opened up as part of Apicurio's architecture allowing custom JSON schema templates that can be be imported, and made more informative with plain english responses, more detail, and even links to learn more about how you can improve your API. Turning the basic validation responses into more of an API design knowledge-base, and even structured curriculum walking you through best practices when it comes to API design, and what is working in the industry.

Just some thoughts as I'm playing with [Apicurio](http://www.apicur.io/). I'm very happy to see this API design editor emerge, and I have been having fun thinking about what is possible when it comes to the road map. I feel a common visual API design interface is an important part of the next step in the evolution of the API sector. Which is [why I have been advocating for an open source API design editor](http://apievangelist.com/2015/08/13/a-common-open-source-api-design-editor-is-needed-for-api-service-providers/) that any API provider can use to design their APIs, and any API service provider can bake into their services and tooling--standardizing how we all craft and communicate around our API designs. The validation feedback loop during this phase will be an important channel for pushing API designers to do what is right, make their API definitions more complete, while educating them about common API design practices, and building a more literate API workforce.

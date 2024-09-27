---
published: true
layout: post
title: 'API Snacks for AI'
tags:
  - Snacks
  - API Commons
  - AI
  - Artificial Intelligence
  - Messages
  - Twilio
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/1939-new-york-worlds-fair-corner-restaurant.jpeg
---
I have been trying to prioritize something AI related as part of my regular API work, but the closest I've come is using ChatGPT API for writing descriptions and summaries of [APIs I am profiling for APIs.io](https://apis.io/blog/). Eventually I intend to create a small language model from API Evangelist content, just so I understand how AI works, but I just haven’t had time, and honestly it doesn’t seem to be rising up as a priority in my work. However, as I am profiling APIs for inclusion in my API search engine, I keep thinking that [APIs.json](https://apisjson.org) could have some benefits when it comes to the modularity, semantics, and execution of API capabilities as part of the AI conversations.

I am calling my new prototypes—-[API Snacks for AI](https://github.com/api-commons/snacks-twilio-messages). They aren’t meant to be confused with what an OpenAPI or Postman Collection does, or even what is happening with the Arazzo spec. These are meant to be snackable API capabilities with operational context and semantics baked in. I am using the media type and data properties of APIs.json, but I am also considering adding a JSON-LD property with the next iteration of the discovery specification.

<script src="https://gist.github.com/kinlane/97570d88f64209e22edc6ff5665e2d79.js"></script>

This is my first crack at making these API Snacks for AI. I am working on an ALPS version to complement the Schema.org JSON-LD version. Then I am going to consider how I want to craft the property for APIs.json, if I want it to be JSON-LD and ALPS specific, or a more general semantics property. I want to get more verbs into the discussion, and explore the action part of Schema.org, but also looking at other verb and action centered standards. I am rather pleased to uncover the multiple dimensions of semantics involving an API Snack for API, in that semantics can apply to a resource defined as an APIs.json API, but also each individual property—this combined with the type and media type properties gives you a lot of flexibility.

I have included an [OpenAPI](https://github.com/api-commons/snacks-twilio-messages/blob/main/openapi.yml) as well as [Postman Collection](https://github.com/api-commons/snacks-twilio-messages/blob/main/postman-collection.json) to describe the surface area of the API. The OpenAPI has a JSON Schema, but the Postman Collection is designed for execution with variables and complimentary [Postman environment](https://github.com/api-commons/snacks-twilio-messages/blob/main/postman-environment.json) that could be used to execute the individual API request. There is a lot of context required to send a message using Twilio, which is something the AI may not have. My goals is to get all of this context on the table and represented in a machine readable way. I want be able to see all the nuance of sending a message, but also what the conversation looks like when getting to ready to send a message, maybe having multiple providers and channels available, as well as the authentication, pricing, and other quality, performance, and legal considerations.

I am going to create Stripe payments, New York Times news, and some other API Snacks. Then I will play around with the semantics and limitations of using it in a conversation. I think developing these API Snacks provide an excellent opportunity for talking about APIs.json, but also the business and technical details involved with putting APIs to work in an automated way. Folks like to think all you will need is an OpenAPI to make this work, when you’ll need authentication, pricing, rate limits, terms of service, and other details and context to make work properly. The greater opportunity in my opinion will be to crack open the registration and obtaining a token in an automated way, and building trust among both API producers and consumers--something I will revisit later. Right now, I am just looking to play around with APIs.json, revisit early semantic API work that seems relevant again in the AI gold rush, and explore what is possible in redefining API capabilities as API Snacks for AI.
---
published: true
layout: post
title: Nexmo Manages Their OpenAPI 3.0 Definition Using Github
date: 2018-03-26T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Messaging
  - Github
  - Management
image: >-
  https://s3.amazonaws.com/kinlane-productions/nexmo/nexmo-api-specifications.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>
I'm big on supporting API providers that publish their OpenAPI definitions to Github. It is important for the wider API community that ALL API definitions are machine readable, and available in a way that can be forked, and integrated into continuous integration pipelines. I'm not even talking about the benefits to the API providers when it comes to managing their own API lifecycle. I'm just focusing on the benefits to API consumers, and helping make on-boarding, integration, and keeping in sync with the road map as frictionless as possible.

To help incentivize API providers doing this I'm committed to writing up stories for each API provider that publishes their OpenAPI, APIs.json, or Postman Collections to Github. Bonus points if you are doing it in an interesting way that further benefits your operations, as well as your community. Today's API provider to showcase is [the SMS, voice and phone verifications API provider Nexmo](https://www.nexmo.com), who tweeted [the Github repository at me, which contains their OpenAPI definition for their APIs](https://github.com/Nexmo/api-specification). As they say, it is a work in progress, but it provides a damn good start for a machine readable definition for their API(s), and I mean c'mon, aren't all of our APIs a working progress?

Nexmo uses their API definition as "a single point of truth that can be used end-to-end can we used to:"

- Planning Shared during product discussions for planning API functionality
- Implementation Inform engineering during development
- Testing As the basis for testing or mocking API endpoints
- Documentation For producing thorough and interactive documentation
- Tooling To generate server stubs and client SDKs.

Nexmo has adopted version 3.0 of the OpenAPI definition, which is forward leaning for the API provider. They also provide a list of resources, tooling, and their API definition available as Ruby packages for easier integration. Another thing they do that I think is interesting, is they list the owner, and contributors for each API definition they have published, or are working on. Which is a concept I fully support, and would like to bake into my own API stack work. Working on API definitions is hard work, and we should be showcasing, and supporting anyone that steps up to do the hard work, as well as providing a point of contact for each available definition. 

I am going to spend some time going through Nexmo's API definition, and learning more about OpenAPI 3.0. I will also be spending time going through their API developer portal creating an APIs.json, and Postman Collection for their API. I'm looking to add their API to the Postman API Network, as well as my API Stack, Streamdata.io API Gallery, and other API aggregation, integration, and discovery projects I am working on. Thanks for bringing to my attention Nexmo, and keep up the good work. I'll keep paying attention to what you are doing, with Github, and your OpenAPI definition being a conduit for guiding my attention.

---
published: true
layout: post
title: 'API Contracts Shape the Gateway'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/norman-rockwell-ruby-bridges-gatew-into-field.jpg
author:
 name: kinlane
tags:
- Gateways
- Specifications
- Contracts
---
I’ve looked at all the gateways out there today. I’ve been studying API management since 2010. While there are numerous characteristics that define the next generation of API gateways, in my mind the number one thing that will determine the future of API gateways will be their support for API contracts. This means how they adopt OpenAPI, AsyncAPI, JSON Schema, GraphQL, and Protocol Buffers. You see some of what I am talking about int he way that GraphQL and gRPC APIs operate, but it is starker when you look at how gateways support OpenAPI today. More specifically whether they provide only one of the following areas, or support the spectrum.

- **Import** - You can import an API contract to override the definition of an API at any stage.
- **CI/CD** - You can configure a gateway using the Open via existing CI/CD workflows.
- **Publish** - The API contract can be published or discoverable as part of the gateway operation.
- **Export** - You can export an API contract from a gateway that represents the current truth.
- **API** - You can programmatically manipulate the API contract for any API in a gateway via the API.

Gateways who are earlier on in their own API journey employ publishing of OpenAPIs to support documentation, where those who are further along in their journey allow you to import and export OpenAPI, allow for CI/CD configuration of OpenAPI contracts, as well as programmability of API contracts via an API. The holy grail is when you have inception level contract activity occurring, and you can configure the entire surface area of an API via the gateway using an OpenAPI via the gateway API, and the the gateway APIs possesses an OpenAPI—-replicate this behavior for multi-protocol event-driven APIs using AsyncAPI, and you'll begin to see the future.

API contracts govern the relationship between producer and consumer, and will be the only way that we are able to automate and scale this relationship. When you have the trifecta of contract + CI/CD + gateway present you can then begin to achieve a more honest source of truth that reflects not just the design of an API, but also the reality of what is happening in production, eliminating the drift that enterprises face today.
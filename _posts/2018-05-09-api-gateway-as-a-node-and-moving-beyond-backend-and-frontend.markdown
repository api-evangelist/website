---
published: true
layout: post
title: API Gateway As A Node And Moving Beyond Backend and Frontend
date: 2018-05-09T09:00:00.000Z
tags:
  - API Evangelist
  - Integration
  - Deployment
  - Gateway
  - Proxy
  - Management
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/docks_copper_circuit.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>The more I study where the API management, gateway, and proxy layer is headed, the less I'm seeing a front-end or a backend, I'm seeing just a node. A node that can connect to existing databases, or what is traditionally considered a backend system, but also can just as easily proxy and be a gateway to any existing API. A lot has been talked about when it comes to API gateways deploying APIs from an existing database. There has also been considerable discussion around proxying existing internal APIs or web services, so that we can deploy newer APIs. However, I don't think there has been near as much discussion around proxying other 3rd party public APIs--which flips the backend and frontend discuss on its head for me.

After profiling the connector and plugin marketplaces for a handful of the leading API management providers I am seeing a number of API deployment opportunities for Twilio, Twitter, SendGrid, etc. Allowing API providers to publish API facades for commonly used public APIs, and obfuscate away the 3rd party provider, and make the API your own. Allowing providers to build a stack of APIs from existing backend systems, private APIs and services, as well as 3rd party public APIs. Shifting gateways and proxies from being API deployment and management gatekeepers for backend systems, to being nodes of connectivity for any system, service, and API that you can get your hand on. Changing how we think about designing, deploying, and managing APIs at scale.

I feel like this conversation is why API deployment is such a hard thing to discuss. It can mean so many different things, and be accomplished in so many ways. It can be driven by a databases, or strictly using code, or be just taking an existing API and turning it into something new. I don't think it is something that is well understood amongst developer circles, let alone in the business world. An API gateway can be integration just as much as it can be about deployment. It can be both simultaneously. Further complexing what APIs are all about, but also making the concept of the API gateway a more powerful concept, continuing to renew this relic of our web services past, into something that will accommodate the future.

What I really like about this notion, is that it ensures we will all be API providers as well as consumers. The one-sided nature of API providers in recent years has always frustrated me. It has allowed people to stay isolated within their organizations, and not see the world from the API consumer perspective. While API gateways as a node won't bring everyone out of their bubble, it will force some API providers to experience more pain than they have historically. Understanding what it takes to to not just provide APIs, but what it takes to do so in a more reliable, consistent and friendly way. If we all feel the pain our integration and have to depend on each other, the chances we will show a little more empathy will increase.

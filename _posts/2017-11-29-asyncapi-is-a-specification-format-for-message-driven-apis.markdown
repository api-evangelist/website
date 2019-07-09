---
published: true
layout: post
title: AsyncAPI Is A Specification Format For Message-Driven APIs
date: 2017-11-29T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Real Time
image: >-
  https://s3.amazonaws.com/kinlane-productions/asyncapi/asyncapi-editor-sample.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/asyncapi/asyncapi-editor-sample.png" align="right" width="45%" style="padding: 15px;" /></p>I've been learning about a new API definition format called AsyncAPI that allows you to define message-driven APIs in a machine-readable format. It is protocol-agnostic, which means you can use it for APIs that work over MQTT, AMQP, WebSockets, STOMP, and other real-time, and Internet of Things focused APIs. The specification format mirrors OpenAPI, making it pretty easy to get up to speed understanding what is going on.

There are two primary concepts at play with the AsyncAPI:

1. Messages - Consumer(s) communicate with your API via messages. A message is a piece of information two or more programs exchange. Most of the times to notify the other end(s) that, either an event has occurred or you want to trigger a command. Technically speaking the events and actions will always be sent in the same way. These are just messages, and their content can be anything. So when we talk about the difference between events and actions, this is only a semantic differentiation of message’s content. We do not enforce you to make any difference between them, although we encourage you to do it. A message can contain headers and a payload. However, both are optional. The specification allows you to define any header, to remain as much protocol-agnostic as possible.
2. Topics -  Message-driven protocols usually contain something called topic (MQTT), routing key (AMQP), destination (STOMP), etc. To some extent, they can compare to URLs in HTTP APIs. So, when you send a message to your API, it will be routed depending on the topic you published on. This feature allows you to create APIs that subscribe to specific topics and publish to other ones.
There’s no standard way of naming topics, so we recommend you to have a look at our proposal here.

I don't have any APIs I can apply AsyncAPI to, so I have to just learn from the examples and any other work I come across. It makes me happy to see folks developing API specifications like this, going beyond what OpenAPI is doing, but also keeping so closely in alignment with the existing work out of the OAI. I'm always hearing folks say that the OpenAPI specification doesn't do what they want it to do, yet they don't invest in vendor extensions, or even augment the work that is going on with a complimentary set of specifications. Good to see people just make it happen!

I'm adding AsyncAPI to [my API definition research](http://definitions.apievangelist.com/) so I can keep in tune with where it goes. I'm talking with some folks regarding how it should viewed by the OAI. In my opinion, the OAI is going to have to begin considering how it will embrace specs that go beyond what it can do, as well as [begin to adopt industry specific OAI implementations that may require acknwoledging some vendor extensions that may never get brought into the core specification](http://apievangelist.com/2017/09/25/considering-the-future-of-the-openapi-initiative/). Anyways, it's good to see movement in this area. Nice work [Fran](https://twitter.com/fmvilas), [Bruno](https://twitter.com/bpedro), and [Mike](https://twitter.com/PermittedSoc)--you guys are rocking it.

---
published: true
layout: post
title: My Evolving Definition Of A Robust And Diverse API Toolbox
date: 2018-01-02T15:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Definitions
  - Protocol
  - gRPC
  - GraphQL
  - HTTP/2
image: 'https://s3.amazonaws.com/kinlane-productions/api-toolbox/API+Toolbox.png'
---
It is always telling when folks assume I mean REST when I say API. While the web dominates my definition of API, and REST is definitely a leading architectural style, these assumptions always define the people who bring them to the table, more than they ever do me. I'm in the business of studying how people are applying programmatic interfaces using the web. To reflect my research I've been evolving a diagram of my toolbox that I've been publishing as part of workshops, presentations, and some talks I'm preparing for 2018. It reflects what I'm seeing as the evolving API toolbox that I'm seeing companies working with, and a diversity in which I'm encouraging others to think about more, as we choose to ignore the polarizing forces in the API sector.

<p><img src="https://s3.amazonaws.com/kinlane-productions/api-toolbox/API+Toolbox.png" width="100%" style="padding: 15px;" /></p>

To set the tone for any API conversation I am participating in, I prefer to introduce the concept of the API toolbox including more tools than just REST, acknowledging that their are a growing number of tools in our API infrastructure toolbox which can be applied to different APIs, to solve a variety of problems and challenges we face. Also we need to be more honest about the fact that there are many legacy solutions still in use across large organizations, even as we consider adopting the latest in leading edge approaches to API deployment in newer projects.

- HTTP - Leverage the web, and the HTTP standard across ALL API efforts.
- SOAP - Acknowledging there are still a number of SOAP services in use.
- RPC - Understand how and why RPC APIs still might be viable in production.
- REST - Making REST, and a resource-centered approach the focus of the operations.
- Microservices - Emphasis on independently deployable and module API services.
- Verbs - Knowing, and putting to use HTTP verbs across API implementations.
- Content-Type - Understanding the negotiation between XML, JSON, and other types.
- Hypermedia - Considering how hypermedia design, and content types play a role.
- GraphQL - Thinking about GraphQL when it comes to data intensive API projects.
- HTTP/2 - Understanding and embracing the evolution of the HTTP standard.
- gRPC - Considering two-speed APIs, and using gRPC for higher volume API implementations.
- Webhooks - Seeing APIs as a two-way street, and pushing data to APIs as well as receiving.
- Server-Sent Events (SSE) - Leveraging HTTP push technology to make things real time.
- Websockets - Opening up two streams that allow for bi-directional API interactions.
- PubSubHubbub - Considering a distributed publish-subscribe approach to API interactions.
- Apache - Being aware of the Apache stack which includes Spark, Kafka, and other real time data solutions.

While HTTP and REST are definitely the focal point of many API conversations I am in, SOAP and RPC are legacy realities we must accept are still getting the job done in many environments, and we shouldn't be shaming the folks who own this infrastructure. At the same time I'm helping folks unwind this legacy infrastructure, I also find myself participating in discussions around event-driven architecture, streaming, and HTTP/2 which represent where API architecture is headed. I'm needing a toolbox that reflects this spectrum of API tooling, as well as where we've been, and find ourselves still supporting in 2018.

I'm still evaluating the Apache stack, as well as GraphQL and gRPC, to better understand how they fit in my definition. This work, as well as part new partnership with [Streamdata.io](http://streamdata.io) is pushing me to re-evaluate exactly what is real time and streaming using webhooks and server-sent events, alongside a more event-driven approach I am seeing emerge within many leading organizers. People love to say that APIs are done. I wish I could show how silly this way of thinking makes y'all look. The idea that using the web to exchange data, content, and algorithms in a machine readable formats is going anywhere is laughable. My objective is to keep tracking on the tools people are using to get this job done, and help folks ensure their toolbox is as robust and diverse as possible, not traffic in silly dogmatic fantasies about API trends and religions.

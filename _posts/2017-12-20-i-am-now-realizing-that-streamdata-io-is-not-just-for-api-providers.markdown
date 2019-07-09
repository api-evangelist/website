---
published: true
layout: post
title: I Am Now Realizing That Streamdata.io Is Not Just For API Providers
date: 2017-12-20T11:00:00.000Z
tags:
  - API Evangelist
  - Event Architecture
  - Streaming
  - Real Time
image: ''
---
<p><a href="https://streamdata.io"><img src="https://s3.amazonaws.com/kinlane-productions/streamdata/streamdata-push.png" align="right" width="45%" style="padding: 15px;" /></a></p>When I first started diving into what [Streamdata.io](https://streamdata.io) does, and thinking of their role in the wider API landscape, I was pretty exclusively focused API providers. Meaning, if you are an API provider, depending on the resources you are serving up, you should consider augmenting it with a real time stream using Streamdata.io. This still holds true, but after using Streamdata.io more as a developer, it is becoming clear of Streamdata.io's value in my toolbox as an API consumer, and thinking about how I can make my applications more efficient, real time, and event-driven.

Right now, I'm just taking a wide variety of existing web APIs and running through the Streamdata.io proxy, and seeing what comes out the other end. I'm in the phase where I'm just understanding what Server-Sent Events (SSE) combined with JSON Patch does to existing web APIs, and their resources. This process is helping me understand the possibilities with streaming existing web APIs, but as I fire up each API I'm seeing it also reveal a new layer of events that exist in between providing APIs, and consuming APIs. I feel like this layer isn't always evident to API providers, who haven't made it very far in their API journey.

While I study how the bleeding, and leading edge developers are deploying event-driven architecture, mining for the event value that exists within big data, I'm thinking there is also a pretty interesting opportunity in mining the event layer for existing web APIs. Once I turn on streaming for a web API, the immediate value you see is when a new resource is added. However, this really isn't that amazing beyond just subscribing to a webhook, or polling an API. I feel like the valuable events we don't fully see without Server-Sent Events (SSE) is the changes. When a price changes. When a link is modified. When content is refreshed. The subtle events that occur that might not be noticed in regular operations.

I've had this conversation with Nicolas Rigaud, the VP Marketing & Partners for Streamdata.io several times recently. That there is unrealized value in these changes to any system. The more they are known, recognized, and responded to, the more value they will possess. I feel like this is potentially the value that is driving the wider event-driven architecture movement at the moment. Understanding the subtle, but important changes that exist across systems and the data that is generated. Not just individual events, but also aggregate events at scale, which equal something much, much bigger. While I feel like "hoovering" up all the data you can find, and dialing in Kafka, or some other event-driven, streaming solution, is how you mine this value at scale, I think there is an equally great opportunity to tune into web APIs, and the unrealized events that happen via everyday platforms.

I'm working on a target list of around 100 APIs to proxy with Streamdata.io so that I can get a handle on the types of events that are occurring within some of the most used APIs out there. I'm guessing that the API providers who have the resources and skills on staff are already jumping at this opportunity, but I'm guessing there are many other APIs that have a significant amount of untapped potential for defining the event layer. This is where I see the potential for Streamdata.io as a tool in the hands of API consumers, and the average developer. To step in from an external vantage point and identify the most meaningful events that are occurring, and make them accessible to other systems, and within applications. Depending on the industry, I'm guessing there will become a growing number of monetization opportunities to emerge from these newfound events as we discover them in the real time streams.

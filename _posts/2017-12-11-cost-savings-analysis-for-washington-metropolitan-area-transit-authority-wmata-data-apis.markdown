---
published: true
layout: post
title: >-
  Cost Saving Analysis For Washington Metropolitan Area Transit Authority
  (WMATA) Data APIs
date: 2017-12-11T12:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Streaming
  - Monetization
  - Transit
  - Transportation
image: >-
  https://s3.amazonaws.com/kinlane-productions/transit/washington-metropolitan-area-transit-authority-api.pn
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/transit/washington-metropolitan-area-transit-authority-api.png" align="right" width="45%" style="padding: 15px;" /></p>Even before I engaged with Streamdata.io on our current partnership, I was working with them to quantity the value they bring to the table with their service. As I was working on my story regarding [the roubling terms of service changes From Washington Metropolitan Area Transit Authority (WMATA) data APIs](http://apievangelist.com/2017/11/30/licensing-over-dc-transit-data/), the Streamdata.io team was running a cost savings analysis on the WMATA APIs. This is where they take their web API, and see what they could save if they used Streamdata.io, and turned it into a streaming API.

The Streamdata.io team took [the WMATA Real-Time Bus PredictionsAPI](https://developer.wmata.com/docs/services/5476365e031f590f38092508/operations/5476365e031f5909e4fe331e), and assessed the efficiency gains for WMATA when it comes to their most demanding API consumers. Here are the bandwidth and CPU savings:

- Client Bandwidth (BW) Savings - 88%
- Server Bandwidth (BW) Savings - 99%
- Server CPU Savings - 87%

Streamdata.io does this by being stood up in front of the WMATA web API and caching the results, then only showing changes to clients--in real-time. This isn't just about making something real-time, it is about reducing the number of times API consumers need to be polling an API. When it comes to transit data you can imagine that the client is probably polling every second to see what has changed.

I'm learning about Streamdata.io's process for calculating these savings, which is why I'm writing this story. I'm going to work to help apply this to many other APIs, as well as look at productizing the tool so that maybe it can become a self-service tool for other API providers to evaluate their own cost savings, if they went to a real-time way of doing things. To help me understand the savings beyond WMATA, I'm going to be doing benchmarks across all the other US transit provides, and see what kind of numbers I can generate.

_**Disclosure:** Streamdata.io is a paid API Evangelists partner._

---
published: true
layout: post
title: Reducing Polling Of Your Existing API Using Streamdata.io
date: 2017-12-18T09:00:00.000Z
tags:
  - API Evangelist
  - Polling
  - Reliability
  - Performance
  - Caching
image: >-
  https://s3.amazonaws.com/kinlane-productions/streamdata/cloud-architecture-1024x519.png
---
<p><a href="https://streamdata.io"><img src="https://s3.amazonaws.com/kinlane-productions/streamdata/cloud-architecture-1024x519.png" align="right" width="45%" style="padding: 15px;" /></a></p>[I've partnered with Streamdata.io](https://streamdata.io), resulting in me getting more acquainted with their API solutions, and telling the story of that process here on API Evangelist. I figured I would dive right in and start with the basics of what Streamdata.io does--turning your existing web API into a real-time stream. Streamdata.io acts as a reverse proxy that translates REST API polling into a stream of data. Instead of constantly polling your API for changes, your API clients will poll Streamdata.io and get a [JSON Patch update](https://tools.ietf.org/html/rfc6902) if anything has changed, and reducing the impact of the requests your clients will make to your API.

When thinking about what Streamdata.io does it is easy to get caught up on the real time and streaming nature of what they do, but the most immediate value they bring to the table is about making your relationship with your API clients more efficient. Streamdata.io reduces the costs associated with operating your API, stepping in between you and your demanding clients, and act as a buffer that will reduce the load on your servers. Eliminating one of the biggest headaches for API providers, and reigning in the behavior by our most demanding, and demanding clients.

I'm always surprised by the answers I get from API providers when I ask them why they rate limit their APIs. I'd say that 80% of the time it is based upon reducing the overhead and impact on backend systems, and dealing with the bad behavior of API consumers. Streamdata.io provides a pretty compelling solution to help alleviate this reality of operating APIs for most API providers. It isn't just about making things real-time, it is more about cost savings, and minimizing the impact of API consumption on our back-end solutions. Making rate limiting irrelevant, unless you have some other specific business needs behind your decision.

There are numerous other benefits Streamdata.io brings to the table, but reducing the load on your APIs probably the most relevant to ALL of my readers who operate APIs. We can always do better when it comes to making our APIs more efficient, and [Streamdata.io](https://streamdata.io) is a way we can do this with minimal costs, in minutes, not days, weeks, or months. Which is one of the primary reasons I am partnering with Streamdata.io. It is a service I find easy to push as part of my API storytelling here on the blog, and happy to have become part of the team.

_**Disclosure:** [Streamdata.io](https://streamdata.io) is the primary partner for the API Evangelist website._

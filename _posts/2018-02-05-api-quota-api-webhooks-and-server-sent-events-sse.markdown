---
published: true
layout: post
title: 'API Quota API, Webhooks, and Server-Sent Events (SSE)'
date: 2018-02-05T15:00:00.000Z
tags:
  - API Evangelist
  - Management
  - Rate Limiting
  - Monetization
  - Plans
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/goldsilverfalls/creativity/file-00_00_40_84.jpg
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/goldsilverfalls/creativity/file-00_00_40_84.jpg" align="right" width="45%" style="padding: 15px;" /></p>I am profiling market data APIs as part of my partnership with [Streamdata.io](http://apis.how/streamdata). It is a process I enjoy, because it provides me with a number of interesting stories I can tell here on API Evangelist. Many of the APIs I profile just frustrate me, but there are always the gems who are doing interesting things with their APIs, and understand providing APIs, as well as consuming APIs. One API that I've been profiling, and I am able to put to use in my work to build a gallery of real time data APIs, was [1Forge](https://1forge.com).

[1Forge provides dead simple APIs for accessing market data](https://1forge.com/forex-data-api/api-documentation), and surprise!! -- you can sign up for a key, and begin making API calls within minutes. It might not sound like that big of a deal, but after going through 25+ APIs, I only have about 5 API keys. I'm working on an OpenAPI definition for 1Forge, so I can begin to poll, and stream the data they make available, including it in the Streamdata.io API gallery I'm building. However, as I was getting up and running with the API, I noticed [their quota endpoint](https://1forge.com/forex-data-api/api-documentation), which allows me to check my usage quote with the 1Forge API--something that I thought was story worthy.

The idea of an endpoint to check my applications usage quota for an API seems like a pretty fundamental concept, but sadly it is something I do not see very often. It is something that should be default for ALL APIs, but additionally I'd like to see a webhook for, letting me know when my API consumption reaches different levels. Since I'm talking about Streamdata.io, it would also make sense to offer a Server-Sent Event (SSE) for the API quote endpoint, allowing me to bake the usage quota for all the APIs I depend on into a single API dashboard--streaming real time usage information across the APIs depend on, and maybe displaying things in RED when I reach certain levels.

An API quota API is useful for when you depend on a single API, but is something that becomes almost critical when it comes to depending on many APIs. These are one of those APIs that API providers are going to need to realize has to be present by default for their API platforms. It is something that can keep us humans in tune with our consumption, but more importantly can help us programmatically manage our API consumption, and adjust our polling frequency automatically as reach the limits of our API access tier, or even upgrade as we realize our rate limit constraints are too tight for a specific application. I'm going to add an API quota API to my list of default administrative APIs that API providers should be offering. Updating the default set of resources we should have available for ALL APIs we are operating.

---
published: true
layout: post
title: Connecting Service Level Agreements To API Monitoring
date: 2017-10-10T13:00:00.000Z
tags:
  - API Evangelist
  - Monitoring
  - Service Level Agreements
  - Performance
  - Reliability
image: >-
  https://s3.amazonaws.com/kinlane-productions/apimetrics/api-metrics-latency-sla.png
---
<p><a href="https://apimetrics.io"><img src="https://s3.amazonaws.com/kinlane-productions/apimetrics/api-metrics-latency-sla.png" align="right" width="40%" style="padding: 15px;" /></a></p>Monitoring your API availability should be standard practice for internal and external APIs. If you have the resources to custom build API monitoring, testing, and performance infrastructure, I am guessing you already have some pretty cool stuff in place. If you don't, then you should not be reinventing the wheel out there, and you should be leveraging one of the existing API monitoring services out there on the market. When you are getting started with monitoring your APIs I recommend you begin with uptime and downtime, and once you deliver successfully on that front, I recommend you work on API performance, and the responsiveness of your APIs.

You should begin with making sure you are delivering the service level agreement you have in place with your API consumers. What, you don't have a service level agreement? No better time to start than now. If you don't already have an explicitly stated SLA in place, I recommend creating one internally, and see what you can do to live up to your API SLA, then once you ensure things are operating at acceptable levels, you share with your API consumers. I am guessing they will be pretty pleased to hear that you are taking the initiative to offer an SLA, and are committed enough to your API to work towards such a high bar for API operations.

To help you manage defining, and then ultimately monitoring and living up to your API SLA, I recommend taking a look at [APIMetrics](https://apimetrics.io), who is obsessively focused on API quality, performance, and reliability. They spend a lot of time monitoring public APIs, and have [developed a pretty sophisticated approach to ranking and scoring your API to ensure you meet your SLA](https://apievangelist.com/2017/04/24/a-ranking-score-to-determine-if-your-api-was-sla-compliant/). As you can see in the picture for this story, the APIMetrics administrative dashboard provides a pretty robust way for you to measure any API you want, and establish metrics and triggers that let you know if you've met or failed to meet your SLA requirements. As I said, you could start out by monitoring internally if you are nervous about the results, but once you are ready to go prime time you have the tools to help you regularly reporting internally, as well as externally to your API consumers.

I wish that every stop along the life cycle had a common definition for defining a specific aspect of service level agreements, and was something that multiple API providers could measure and report upon similar to what APIMetrics does for monitoring and performance. I'd like to see API design begin to have a baseline definition, that was verifiable through a common set of machine readable API assertions. I'd love for API plans, pricing, and even terms of service measurable, reportable, in a similar way. These are all things that should be observable through existing outputs, and reflected as part of service level agreements. I'd love to see the concept of the SLA evolve to cover all aspects of the quality of service beyond just availability. APIMetrics provides a good look at how the services we use to manage our APIs can be used to define the level of service we provide, something that we can be emulating more across our API operations.

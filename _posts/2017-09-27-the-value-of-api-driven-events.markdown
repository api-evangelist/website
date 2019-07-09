---
published: true
layout: post
title: The Value of API Driven Events
date: 2017-09-27T13:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Webhooks
  - Event Sourcing
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/hermosabeach/dark_dali/file-00_00_11_64.jpg
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/hermosabeach/dark_dali/file-00_00_11_64.jpg" align="right" width="40%" style="padding: 15px;" /></p>I am spending a lot of time lately thinking about event sourcing, evented architecture, real time, and webhooks. I'm revisiting some of the existing aspects of how we move our bits around the Internet in real time and at scale as part of existing conversation I am having, as well as some projects I'm working on. [I recently wrote about making sense of API activity with webhook events](http://apievangelist.com/2017/08/21/making-sense-of-api-activity-with-webhook-events/), and as I'm crafting a list of meaningful events for [my Human Services Data API (HSDA) work](http://org.open.referral.adopta.agency/), I'm thinking about how these events reflect the value that occurs via API platforms.

As I'm going through the different APIs I'm exposing via a platform, I am working to identify and catalog events in which folks can subscribe to using webhooks. These are the events that occur, like adding a new organization, updating a service, or completing a batch import--all the things people will care about the most. These are the events and activities that occur because their is an API, which have the most value to API consumers, and platform operators. This is what actually matters, and why we are doing an API in the first place, to enable these events to occur. The more these events are triggered, and the more people we have subscribing and engaging with these events, the more value that is generated using an API.

In aggregate, using modern approaches to API management, we might provide analytics and reports that demonstrate all this value being created, to justify the existence of our API. In some implementations, this value created is how we might be charging our API consumers, partners, and other stakeholders. However, in some cases we might even considering paying API consumers when these events occur, incentivizing a certain event-driven behavior that benefits the platform. It is easy to think of API value generation simply as the number of API calls, but I think webhooks has helped establish a new way to look at how value is generated, based upon the number of subscribers to any particular event, or possible a type of of event.

I feel like this is one of the reason we are finally seeing more investment in event sourcing, and evented architecture, and the real time streaming of data and content. The events that matter are getting prioritized, and the technology is advancing to support these events that matter. IDK. As I push forward with my webhook research, and revisit my real time API research, and expand into new realms of messaging and focusing on events, I'm rethinking how we measure and quantify value generation via API platforms. For a long time the measure has been number of API consumers, and the number of API calls, but I feel like things are shifting to the types of events that occur, and how meaningful these events are to API providers, consumers, and their application end-users.

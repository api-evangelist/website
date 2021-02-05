---
published: true
layout: post
title: Making Sense Of API Activity With Webhook Events
date: 2017-08-21T13:00:00.000Z
tags:
  - API Evangelist
  - Webhooks
  - Evented
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/border-traffic.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/border-traffic.jpg" align="right" width="40%" style="padding: 15px;" /></p>[I was doing some webhooks research as part of my human services work](http://apievangelist.com/2017/08/15/where-to-begin-with-webhooks-for-the-human-services-data-api/) and I found myself studying the types of events used as part of webhook orchestration for [Github](https://developer.github.com/webhooks/), [Box](https://developer.box.com/reference#event-triggers), [Stripe](https://stripe.com/docs/api#event_types), and [Slack](https://api.slack.com/events/api). Each of the event type lists for each of these platforms tell a lot about what is possible with each API, and the webhooks that get triggered as part of these events show what is important to developers who are integrating with each of these APIs. These event type lists really help make sense of the API activity for each of these APIs, providing a nice list to follow when developing your integration strategy.

What I really like as I look through each of these webhook event lists is that they are usually in pretty plain language, describing events that matter, not just row updates with a timestamp. These events can be very broad, triggering a webhook when anything happens to a resource, or it could be granular and be all about a specific type of change, or anything in between. Each event type represents something API consumers want from an API, and would be normally polling the API for, but since there are webhook events, developers can get a push of data or a ping whenever an event occurs.

Another thing that the presence of webhooks, and a robust list of events represent for me is the maturity of a platform. Github, Box, Stripe, and Slack are all very mature and robust platforms. There are meaningful events defined, and the platform behaves as a two way street, accepting requests, but also making requests whenever a meaningful event occurs. I'm getting to a place where I feel like basic webhook infrastructure should be default for all API providers. The problem is I don't think there are well enough defined models for API providers to follow when they are planning this part of their API operations. Something we will need to tackle as an industry pretty soon, helping make sure webhooks behave in consistent ways, and have a standard API interface for orchestrating with.

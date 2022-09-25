---
published: true
layout: post
title: Understanding Events Across Your API Platform In Real Time
date: 2018-01-08T09:00:00.000Z
tags:
  - API Evangelist
  - Event Architecture
  - Real Time
  - Streaming
  - Webhooks
  - Payments
image: >-
  https://s3.amazonaws.com/kinlane-productions/stripe/stripe-the-event-object.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/stripe/stripe-the-event-object.png" align="right" width="45%" style="padding: 15px;" /></p>I spend a lot of time trying to understand and define what is API. With [my new partnership with Streamdata.io](http://apis.how/streamdata) I'm pushing that work into understanding APIs in real time, and as part of event-driven architecture. As the Streamdata.io team and I work to identify interesting APIs out there that would benefit from streaming using the service, a picture of the real time nature of API platforms begins to emerge. I'm beginning to see all of this as a maturity aspect of API platforms, and those who are further along in their journey, have a better understanding the meaningful events that are occurring via their operations.

As part of this research I've been studying the Stripe API, looking for aspects of the platform that you could make more real time, and streaming. Immediately I come across [the Stripe Events API](https://stripe.com/docs/api#events), which is a "way of letting you know when something interesting happens in your account". Using the Stripe Events API, "you can retrieve an individual event or a list of events from the API. We also have a separate system for sending the event objects directly to an endpoint on your server, called webhooks." This is the heartbeat of the Stripe platform, and represents the "events" that API providers and consumers want to know about, and understand across platform usage.

I think about the awareness API management has brought to the table in the form of metrics and analytics. Then I consider the blueprint the more mature platforms like Stripe have established when it comes to codifying this awareness in a way that can be accessed via API, and begin to make more real time, or at least asynchronous using webhooks. Then I think about what Streamdata.io provides with Server-Sent Events, and JSON Patch, providing a stream of these meaningful events in real time, as soon as these events happen--no polling necessary. This is what I find interesting about what they do, and why I've signed up to partner with them. Well, that combined with them supporting me financially. ;-) 

Even before working with Streamdata.io, [I have been studying the value of API driven events](http://apievangelist.com/2017/09/27/the-value-of-api-driven-events/), and working to identify the API platforms who are mature enough to be mapping this value exchange out. This has led to me to desire a better understanding of event-driven architecture, not necessarily because it is the next thing with APIs, but because there is some substance in there. There is a reason why events matter. They represent the meaningful exchanges that are occurring via platforms. The valuable ones. The percentage of transactions we should be tuning into. I want to better understand this realm, and continue collecting a wealth of blueprints regarding how companies like Stripe are maximizing these exchanges.

_**Disclosure:** In case it isn't clear, [Streamdata.io](http://apis.how/streamdata) is my primary partner, paying me to do research in this area, and helping support me as the API Evangelist._

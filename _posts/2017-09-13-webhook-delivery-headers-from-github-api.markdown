---
published: true
layout: post
title: Webhook Delivery Headers From Github API
date: 2017-09-13T09:00:00.000Z
tags:
  - API Evangelist
  - Github
  - Webhooks
  - Headers
  - Design
image: 'https://s3.amazonaws.com/kinlane-productions/github/github-circle-icon.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/github-circle-icon.png" align="right" width="30%" style="padding: 15px;" /></p>I am continuing my learning about Webhooks, and [Github keeps my notebook full with interesting building blocks we can use when crafting our own webhook strategies](https://developer.github.com/webhooks/). I'm not using everything I'm learning from Github in my current strategy, but I like adding each of these building blocks to my [webhook research](http://webhooks.apievangelist.com/), so that I can use in future guides that I publish. Today's post overlaps two areas of my research into webhooks, and how headers are being used by a variety of API providers.

Github is using HTTP headers as part of the webhook response, providing the recipients of webhooks with more information about what is happening with each outgoing request. They are providing three custom headers along with each payload:

- **X-GitHub-Event** - Name of the event that triggered this delivery.
- **X-Hub-Signature** - HMAC hex digest of the payload, using the hook's secret as the key (if configured).
- **X-GitHub-Delivery** - Unique ID for this delivery.

In addition to these three custom headers, the User-Agent for the requests will have the prefix GitHub-Hookshot--so that your systems can identify these incoming requests more specifically. I like getting the name of the event, and definitely like the example of using the signature to make sure the payload hasn't been tampered with, or from an untrustworthy source. Additionally you get a unique identifier for the delivery, allowing you to be able to record, and pull up unique webhook receipts. 

I'm adding these all as building blocks to my webhook research. I still have a notebook full of other Github, Stripe, Twilio, and leading approaches to webhooks. Once I get through this round I'm going to apply what I've learned to the project I'm working on, and then see about pushing out the first draft of my webhooks guide--something I've never done before. If nothing else, I'm learning a lot. I'm learning from all the leaders in the space, who are several versions into their webhook designs. I'm finding the biggest challenge right now, is how I hold back and don't do everything, keeping my webhook designs simple, intuitive, but as powerful as possible.
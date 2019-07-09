---
published: true
layout: post
title: The OpenAPI-Powered Mock API Server From Stripe
date: 2017-11-28T11:00:00.000Z
tags:
  - API Evangelist
  - Mock
  - Virtualization
  - Payments
  - Definitions
image: 'https://s3.amazonaws.com/kinlane-productions/stripe/stripe-mock-api-server.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/stripe/stripe-mock-api-server.png" align="right" width="45%" style="padding: 15px;" /></p>I showcased Stripe's OpenAPI definition the other week, so I wanted to also highlight a side effect of Stripe deciding to be OpenAPI-Driven. [Stripe recently published an OpenAPI-powered mock server](https://github.com/stripe/stripe-mock#development), allowing Stripe API consumers to test drive, and play with the Stripe API in a simulated environment. "It operates statelessly (i.e. it won't remember new resources that are created with it) and responds with sample data that's generated using a similar scheme to the one found in the API reference."

The Stripe Mock Server is written in Go, and [is available on Github](https://github.com/stripe/stripe-mock). You can rebuild the Stripe API mock server from an updated OpenAPI anytime. It is a pretty dead simple mock server that seems like should be standard practice for any API. Providing a simple, safe, and portable way to play with an API. I'm going to fork the Stripe Mock API and play with it, see what is possible with the tool.

I will be keeping an eye out for any other OpenAPI-powered tools out of Stripe, now they are actively working with it. Adoption of OpenAPI at this level of API provider is helpful to the rest of the community, by providing an example of how you can bake OpenAPI into your operations, but also the open source tooling these companies produce. It's an important community effect that makes this whole API thing work so well.

Ideally, the leading API providers, with the most resources, could coordinate their efforts and deliver a suite of open source tooling. However, I'm patient, I'm just happy that big companies like Stripe, Slack, Box, New York Times are doing OpenAPI at all. I can wait for all the cool tooling to happen next. I'll keep an eye on Stripe's Github organization to see what pops up.

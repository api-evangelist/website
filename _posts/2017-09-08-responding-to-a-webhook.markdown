---
published: true
layout: post
title: Responding To A Webhook
date: 2017-09-08T11:00:00.000Z
tags:
  - API Evangelist
  - Webhooks
image: 'https://s3.amazonaws.com/kinlane-productions/stripe/stripe-using-webhooks.png'
---
<p><a href="https://stripe.com/docs/webhooks"><img src="https://s3.amazonaws.com/kinlane-productions/stripe/stripe-using-webhooks.png" align="right" width="40%" style="padding: 15px;" /></a></p>There are many details of doing APIs you don't think about until you either a) gain the experience from doing APIs, or b) learn from the API providers already in the space. When you are just getting going with your API efforts you pretty much have to rely on b), unless you have the resources to hire a team with existing API experience. Which many of my readers will not have the luxury to do, so they need as much helping learning from the pioneers who came first, wherever they can.

One of the API pioneers you should be learning from is the payment API provider Stripe. [I've been studying their approach to webhooks lately](https://stripe.com/docs/webhooks), and I've managed to extract a number of interesting nuggets I will be sharing in separate blog posts. Today's topic is responding to a webhook, which Stripe provides the following guidance:

_To acknowledge receipt of a webhook, your endpoint should return a 2xx HTTP status code. Any other information returned in the request headers or request body is ignored. All response codes outside this range, including 3xx codes, will indicate to Stripe that you did not receive the webhook. This does mean that a URL redirection or a "Not Modified" response will be treated as a failure._

To be honest, I had never thought I should be responding to the webhooks I've setup. I treated them like a UDP request and once they went out the door and I processed, I didn't need to response at all. How rude! I hadn't seen any of my existing API providers offer up guidance in this area, or more likely I never noticed it. This is one of the reasons I like going though API providers documentation when I'm not integrating with them, because I tend to have a different eye for what is going on.

Anyways, I'm adding webhook responses to my list of building blocks for [my webhook research](http://webhooks.apievangelist.com/), and will be including it in future guidance. It seems like a pretty significant thing to help API consumers deliver to complete the webhook loop, and it injects more HTTP status code awareness and literacy into the conversation, which I think is always a good thing for everyone. Thinking about how we are signaling back and forth in the API game is always an important part of the equation.

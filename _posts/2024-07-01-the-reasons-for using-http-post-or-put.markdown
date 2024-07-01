---
published: true
layout: post
title: 'The Reasons for Using HTTP POST or PUT'
tags:
  - HTTP
  - Methods
  - POST
  - PUT
  - Stripe
  - Twilio
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/citizenship-old-bearded-man-thinking.jpeg
---
I wrote about [Stripe and Twilio not using PUT for updates a couple months back](https://apievangelist.com/2024/02/07/twilio-and-stripe-do-not-use-put-for-http-resource-updates/). Since then a co-worker happened to have the chance to sit next to the CTO of Stripe at an event, and was able to ask them directly why they made the decision to use POST for both creating and updating their resources. The answer was simple, their customers utilized integration solutions that couldn’t support HTTP PUT, revealing the influence API consumers can have of our API design.

For me, this is a lesson in the importance of understanding the industry you are operating an API in, as well as having a feedback loop with your consumers. I know we all wish that technology would move forward at the speeds we envision and like to tell ourselves, but the realities of the world aren’t always in agreement or alignment. Developing an industry level, as well as a customer level awareness of how they operate and integrate with data and other digital resources provides essential evidence you need to establish API policies.

As a technologist I find it is too easy to assume that the “right way” of delivering APIs is always the “right way”. First, I’ll let you in on a secret—there is no right way. But, beyond this fact, the policies and patterns you adapt as part of API operation need to be in alignment with your consumers, and can’t be too far out ahead of where they are at. Sure, you can push some API consumers to change their ways, but it will depend on the industry you operate in, and might not always be possible. Sometimes, you will need to push forward cautiously, while you build a customer base and develop an awareness of what the realities are on the ground for your consumers within each industry.

Stripe’s decision reflects what is happening between 2010 and 2015, so we shouldn’t put too much weight on this particular pattern, and more on the fact that this pattern still lives in their API after all these years. My focus in writing this story is more about the need for external evidence to inform your API policies and patterns. As I am mapping out the different patterns in use across the APIs I am profiling for [APIs.io](https://apis.io), I have shifted my view of whether the patterns I come across are positive or negative, and more focused on where and when they exist, and gathering details about the context they operate. Leaving some room that there might be other industry and enterprise influences for what the patterns exist or do not exist, and make sure I keep my API dogma and ideology in check.
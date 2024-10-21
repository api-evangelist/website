---
published: true
layout: post
title: 'How Do You Communicate an API Is Free To Use in a Machine-Readable Way?'
tags:
  - Plans
  - Sign-Up
  - Login
  - Authentication
  - Onboarding
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-immigration_dumping-ground-public-market-fish.jpg
---
I am working on how to better communicate in a machine-readable way that an API is free to use. There is a lot taken for granted at this layer when technologists are looking to automate with APIs, and I want to keep shining a light on the missing steps, but also translate human-readable steps into machine-readable ones that can actually be automated around. I profiled two APIs last week that were free to use, but one of them was open and did not require signing up with the other one requiring an active account with email before you can begin making APIs calls-—this has got me thinking more about how to express that an API is free to use.

Most people would begin with this work in an OpenAPI definition, which in my opinion does a poor job of expressing onboarding in any machine-readable way. API developers often assume that an OpenAPI possesses everything you need to onboard with an API, but it quickly becomes a “[How to Draw an Owl](https://apievangelist.com/2023/01/21/draw-an-owl-api-edition-part-one/)” situation. Using OpenAPI you can express the security definitions for an API, which will tell you how you must use API keys, OAuth, JWT, and other authentication mechanisms. It doesn’t tell you where to obtain those keys and tokens. It may have an external documentation URL which will loosely send you in the direction of where to sign-up, but doesn’t actually do it in one click. So in an OpenAPI scenario, can we just assume that the absence of a security definition means that an API is free and open to use? I don’t think so, but it seems to reflect how technologists are good at assuming things and creating “[How to Draw an Owl](https://apievangelist.com/2023/01/21/draw-an-owl-api-edition-part-one/)” situations.

After the OpenAPI, I would move towards the API plans being something that would articulate this, but sadly this aspect of API operations is just human-readable, which I can provide a reference to the plans page, but I really can’t parse the nuance of what is available via API plans, let alone differentiate between free and paid access to an API.

<script src="https://gist.github.com/kinlane/5fb138973158e4b665256deebd71e46f.js"></script> 

API plans and pricing is something I’ve worked on developing into a machine-readable artifact, which is something I will continue as part of my [API Commons](https://apicommons.org) work. I am not at all happy with the current schema, and is something I will harden as part of profiling for the APIs I am profiling for APIs.io. Here is what I have so far, which is used to describe the two tiers of access available for APIs.io.

<script src="https://gist.github.com/kinlane/106907d44671a0a8c19c21aa26b228f2.js"></script>

I will add this to the API Commons in coming weeks and begin the process of hardening the examples, but also the JSON Schema backing it. I will create versions of it for Stripe, Twilio, and other common APIs to help shape the schema on my API Commons forge. However, this still feels like it is missing more details about how to onboard. While I may link to the human and machine readable versions of the pricing page and have security definitions in my OpenAPI, I still don’t have any nuance regarding whether or not you have to sign-up in the first place and where you obtain your tokens and keys. To do this I would provide APIs.json property links to the sign-up and login for an API.

<script src="https://gist.github.com/kinlane/3551bbe1d7471073750d48310146edc8.js"></script>

Again, these are just a human-readable reference and really doesn’t tell me much in any sort of machine-readable and automatable way. I feel like we need some sort of intersection across all of these areas. I am still doing more work on ways that people are making the sign-up for APIs more machine-readable and automated, but these are usually using OpenId and other mechanisms and won’t speak to the free or paid nature of an API. Expressing that an API is free to use, including whether or not you need to sign-up for an account feels much more difficult than one would think, and is something that I feel has to be explicit.

As with all of the API Commons schema I will do a lot more work while profiling other APIs. I will slow down and think more about how I can express in human and machine-readable ways the access for an API. Plans, sign-up, and OpenAPI security definitions are like the place to begin, but the devil is always in the details. Even when API producers are sharing security definitions via OpenAPI, it assumes you the consumer will figure out the rest—-a space I am looking to fill with an APIs.json complete with authentication, sign-up, and plans properties. But these are just human-readable properties, these aren’t things that another computer can read and semantically understand what the hell is going on. And this is just one of several areas of onboarding and integrating with APIs that can’t be automated currently-—we haven’t talked about the legal and other dimensions.
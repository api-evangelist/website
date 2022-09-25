---
published: true
layout: post
title: Providing a Guest API Key
date: 2018-01-16T09:00:00.000Z
tags:
  - API Evangelist
  - Onboarding
  - Management
  - Authentication
image: >-
  https://s3.amazonaws.com/kinlane-productions/washington-metro/wmata-guest-key.png
---
<p><a href="https://developer.wmata.com/Products"><img src="https://s3.amazonaws.com/kinlane-productions/washington-metro/wmata-guest-key.png" align="right" width="45%" style="padding: 15px;" /></a></p>I'm spending time immersed in the world of transit data and APIs lately, and found a simple, yet useful approach to helping onboard developers over at the [Washington Metropolitan Area Transit Authority (WMATA) API](https://developer.wmata.com/). When you you click on [their products page](https://developer.wmata.com/Products) (not sure why they use this name), you get a guest API key which allows you try out the API, and kick the tires. Of course, you can't use the key in production applications, as it is rate limited and can change at any time, but the concept is simple, and provides an example which other API providers might want to consider.

In my days as the API Evangelist I've seen API providers do this in a variety of ways, by providing sample API URLs complete with an API key, and by embedding a key in the OpenAPI definition, so that the interactive documentation picks up the key and will allow developers to make live, interactive API calls--to name a few. No matter what your approach, providing a guest key for users to play around without signing up makes a lot of sense. Of course, you want to rotate this key regularly, or at least be monitoring it to see what IP addresses it is being called from, and maybe understand how its being used--you never know, it might reveal some interesting use cases.

Whatever your approach, get out of the way of your consumers. Don't expect that everyone is going to want to sign up for an account so that they can learn about what your API does. Not everyone is interested in handing over their email address, and other information just so they can test drive. If you have API management in place (which you should), it really doesn't take much to generate test users, applications, and keys, monitor them, and rotate them on a regular basis. I recommend using them like you would marketing tags, and strategically place them into different blog posts, documentation, widgets, and other resources--you never know what other insight you might learn about how people are putting your resources to use.

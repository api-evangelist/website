---
published: true
layout: post
title: >-
  Stack Exchange Has An API That Returns The Details For All Of Your Access
  Tokens
date: 2018-09-10T09:00:00.000Z
tags:
  - API Evangelist
  - Authentication
  - Environments
  - OAuth
image: >-
  https://s3.amazonaws.com/kinlane-productions/stack-exchange/stack-exchange-access-tokens-api.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm a big fan of helpful authentication features, where API providers make it easier to manage our increasingly hellish environment, application, token, and other management duties of the average API integrator. To help me better manage my API apps, and the OAuth tokens I have in play, I am trying to document all the sensible approaches I come across while putting different APIs to work, and scouring the API landscape for stories.

One example of this in action is out of the Stack Exchange API, [where you can find an API endpoint for accessing the details of your OAuth tokens, and invalidate, and de-authorize them](https://api.stackexchange.com/docs/read-access-tokens). A pretty useful API endpoint when you are integrating with APIs, and find yourself having to manage many tokens across many APIs, apps, and users. Helping you check in on the overall health and activity of your tokens, revoking, renewing, and making sure they work when you need them the most.

It is helpful for me to write about the helpful authentication practices I come across while using APIs. It helps me aggregate them into a nice list of features API providers should consider supporting. If I don't write about it here on the blog, then it doesn't exist in my research, and my future storytelling. My goal is to help spread the knowledge about what is working across the sector, so that more API providers will adopt along the way. You know what is better than Stack Exchange providing an API to manage your access tokens? All API providers providing you with an API to manage your access tokens!

These stories, and any other relevant links I've curated will be published to [my API authentication research](http://authentication.apievangelist.com/). Eventually I'll roll all the features I've aggregated into either a long form blog post, or white paper I'll publish and put out with the assistance of one of my partners. I'm interested in the authentication portion of this, but also I'm looking to begin defining processes for helping us better manage our API integration environments, application ids, secrets, tokens, and other goodies we depend on to secure our consumption of APIs across many different providers. It is something that will continue to expand, multiply, and grow more complex with each additional API we add to our growing list of dependencies.

---
published: true
layout: post
title: Adding Ping Events To my Webhooks And API Research
date: 2017-10-19T13:00:00.000Z
tags:
  - API Evangelist
  - Webhooks
  - Orchestration
  - Github
image: >-
  https://s3.amazonaws.com/kinlane-productions/github/github-webhook-ping-events.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/github-webhook-ping-events.png" align="right" width="40%" style="padding: 15px;" /></p>I am adding another building block to my webhooks research [out of Github](https://developer.github.com/webhooks/). As I continue this work, it is clear that Gthub will continue to play a significant role in my [webhook research](https://webhooks.apievangelist.com/) and storytelling, because they seem to be the most advanced when it comes to orchestration via API and webhooks. I'm guessing this is a by-product of continuous integration (CI) and continuous deployment (CD), which Github is at the heart of. The API platforms that have embraced automation and orchestration as part of what they do, always have the most advanced webhook implementations, and provide the best examples of webhooks in action, which we can all consider as part of our operations.

[Today's webhook building block is the ping event](https://developer.github.com/webhooks/#ping-event). "When you create a new webhook, we'll send you a simple ping event to let you know you've set up the webhook correctly. This event isn't stored so it isn't retrievable via the Events API. You can trigger a ping again by calling the ping endpoint." A pretty simple, but handy features when it comes to getting up and going with webhooks, making sure everything is working properly out of the gate--something that clearly comes from experience, and listening to the problems your consumers are encountering.

These types of subtle webhook features are exactly the types of building blocks I'm looking to aggregate as part of my research. As I do with other areas of my research, is at some point I will publish all of these into a single, (hopefully) coherent guide to webhooks. After going through the webhook implementations across the leading providers like Github, I should have a wealth of common patterns in use. Since webhooks aren't any formal standard, it is yet another aspect of doing business with APIs we have to learn from the health practices already in use across the space. It helps to emulate providers like Github, because developers are pretty familiar with how Github works, when your webhooks behave in similar ways it reduces the cognitive load API consumers face when they are getting started.

One other thing to note in this story--[my link to Github's documentation goes directly to the section on webhook ping events](https://developer.github.com/webhooks/#ping-event), because they use anchors for all titles and subtitles. This is something that makes storytelling around API operations soooooooooo much easier, and more precise. Please, please, please emulate this in your API operations. If I can directly link to something interesting within your API documentation, the chances are much greater I will tell a story, and publish a blog post about it. If I have to make a user search for whatever I'm talking about, I'm probably just gonna pass on it. One more trick for your toolbox, when it comes to getting me to tell more stories about what you are up to.

---
published: true
layout: post
title: Wildcard Webhook Events
date: 2017-08-16T12:00:00.000Z
tags:
  - API Evangelist
  - Webhooks
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-asterisk.png'
---
<p><a href="http://webhooks.apievangelist.com"><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-asterisk.png" align="right" width="30%" style="padding: 15px;" /></a></p>I have been studying the approach of a variety of webhook implementations in preparation for an API consulting project I'm working on. Even though I'm very familiar with how webhooks works, and confident in my ability to design and develop a solution, I'm ALWAYS looking to understand what leading API providers are up to, and how I can improve my knowledge and awareness.

With his round of research, Github has provided me with several webhook nuggets for my API storytelling notebook. One of their web features I though was the notion of a wildcard webhook event:

> [Wildcard Event](https://developer.github.com/webhooks/) - We also support a wildcard (*) that will match all supported events. When you add the wildcard event, we'll replace any existing events you have configured with the wildcard event and send you payloads for all supported events. You'll also automatically get any new events we might add in the future.

I have been working to identify a set of objects and associated webhook events, and the notion of a wildcard event is interesting. It seems like you could apply this globally, or to specific objects / resources, allowing you to get pushes for any events that occur. I'm not sure I'll have time to apply this feature in my current project, but it is worth adding to my webhook toolbox for future projects.

There are three other features I've extracted from Github's approach to webhooks that I've added to my API storytelling notebook, to hopefully craft into future blog posts. I'll be adding these all as potential webhook building blocks that API providers can consider. I'm hoping to find some more time and money to invest into [my webhook research](http://webhooks.apievangelist.com) this fall, and be able to publish a formal guide for the world of webhooks. I'm always surprised by the lack of formal guidance when it comes to webhooks, and is something I'd like to see change in the near future.

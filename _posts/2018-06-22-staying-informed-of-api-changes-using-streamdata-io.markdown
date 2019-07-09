---
published: true
layout: post
title: Staying Informed of API Changes Using Streamdata.io
date: 2018-06-22T09:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Event-Driven
  - Twitter
image: 'https://s3.amazonaws.com/kinlane-productions/twitter/twitter-automation.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>My friend James Higginbotham ([@launchany](https://twitter.com/launchany?lang=en)) was sharing his frustration with being able to stay in tune with changes to a variety of APIs. Like me, James works to stay in tune with a variety of signals available via platforms like Twitter, Github, and other commonly used services. These platforms don't always properly signal when things are updated, changed, or advanced, making it difficult to understand the granular changes that occur like likes, votes, edits, and other common events that occur via highly active platforms.

This challenge is why the evolution towards a more event-driven approach to operating an API platform is not just more efficient, it gives users what they need. Using event-driven architectural approaches like Webhooks, and real times streams. This is one of the reasons I'm interested in what [Streamdata.io](http://streamdata.io) does, beyond them helping support me financially, is that they allow me to focus on the event-driven shift that is occurring with many leading API providers, and needs to be brought to the attention of other platforms. Helping API providers be more efficient in what they are doing, while also meeting the needs of the most demanding customers like James and myself.

It is easy to think Streamdata.io is just about streaming real time data. This is definitely a large aspect of what the SaaS solution does, but the approach to using Server-Sent Events (SSE), with incremental updates using JSON Patch adds another useful dimension when it comes to understanding what has changed. You can proxy an existing HTTP API that returns a JSON response using Streamdata.io, and the first response will look just like any other, but every pushed response after that will be a JSON Patch of just what has changed. Doing the heavy lifting of figuring out what has changed in each API response and only sending you the difference, and allowing you to focus only on what has changed, and not having to rely on timestamps, and other signals within the JSON response to understand what the difference is from the previous API response.

Using Streamdata.io you don't have to keep polling an API asking if things have changed, you just proxy the API and you get pushed changes via an HTTP stream. You also don't have to sort through each response and try to understand what changed, you just take the JSON Patch response, and it tells you what has changed. I'm going to create a draft blueprint for James of how to do this, that he can use across a variety of APIs to establish multiple API connections using long running, server-side API streams for a variety of topics. Allowing him to monitor many different APIs, and stay in tune with what changes as efficiently as possible. Once I craft a generic blueprint, I'm going to apply to Twitter and see if I can increase the efficiency of my Twitter monitoring, by turning their REST APIs into real time feeds using [Streamdata.io](http://streamdata.io).

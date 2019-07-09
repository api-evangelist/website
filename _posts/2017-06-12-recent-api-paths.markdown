---
title: Recent API Paths
date: 2017-06-12 13:00:00 Z
tags:
- Design
- API Evangelist
image: https://s3.amazonaws.com/kinlane-productions/box/box-recent-item-object.png
---

<p><a href="https://developer.box.com/v2.0/reference#recent-item-object"><img src="https://s3.amazonaws.com/kinlane-productions/box/box-recent-item-object.png" align="right" width="40%" style="padding: 15px;" /></a></p>I was learning about [a new API path for the document platform Box, that was designed specifically for showing recently updated objects](https://developer.box.com/v2.0/reference#recent-item-object). I think that the concept of having API paths dedicated to showing recently changed elements makes sense, helping eliminate the need for API consumers to learn about which parameters are needed to achieve their immediate goals, helping expose useful aspects of the platform through API design.

As an API consumer, it can be a lot of work to get at the meaningful and relevant context of an API Platform if you do not know all the right knobs and levers to pull on. This is where API design comes in handy, helping surface the most relevant and contextual aspects of what is going on. While this may not be the approach all API providers should be taking, especially if you have a savvy API consumer audience, in times when you have a wider, more unknown audience who may be looking to just get at what is going on with their users platform integrations, this type of API design can be a good way to reduce friction.

I am writing about the concept of recent API paths, to think about how this can be added to my [API design toolbox](http://design.apievangelist.com). While not a REST, hypermedia (wait maybe) design pattern, I think that in some scenarios, having a recent API path makes a lot of sense. Some platforms are only relevant for a specific time period, and the rest of what is happening can be dealt with through search, taxonomy, and other ways of archiving. Once I write about an API design pattern I come across it kinds of activates it in my brain and makes it something I will be thinking about as I review other APIs, as well as design my own APIs, and who knows, maybe it will do the same for you!
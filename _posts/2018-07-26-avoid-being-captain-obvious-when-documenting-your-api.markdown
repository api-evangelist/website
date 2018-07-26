---
published: true
layout: post
title: Avoid Being Captain Obvious When Documenting Your API
date: 2018-07-26T09:00:00.000Z
tags:
  - API Evangelist
  - Documentation
  - Getting Started
image: 'https://s3.amazonaws.com/kinlane-productions/captain_small.jpg'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I read a lot of API documentation, and help review API portals for clients, and one of the most common rookie mistakes I see made, is people pointing out the obvious, and writing a bunch of fluffy, meaningless content that gets in the way of people actually using an API. When the obvious API industry stuff is combined with the assumed elements of what a company does, you end up with a meaningless set of obstacles that slow API integration down. Here is the most common thing I read when entering an API portal:

_"This is an API for querying data from the [Company X] platform, to get access to JSON from our system which allows you to get data from our system into yours using the web. You will need to write code to make calls to our APIs documented here on the page below. Our API uses REST to accept request and provide responses in a JSON format."_

I've read API after API that never tells you what the API does. It just assumes you know what the company does, and then goes into verbose explanations of what API, REST, JSON, and other things that should be intuitive if an API is well designed, and immediately accessible via an API. People tend to make to many assumptions about API consumers already knowing what a company does, while also assuming they known absolutely nothing about APIs, and burying actual API documentation behind a bunch of API blah blah blah, instead of just doing and being the API.

It is another side effect of developers, database, and IT folk not being very good at thinking outside of their bubble. It goes beyond techies not having social skills, and is more about them not having to think about other people at all. They just don't have the ability to put themselves in the shoes of someone landing on the home page of their developer portal, and not knowing anything about the company or the API, and asking themselves, "what does this person need?". Which I get being something developers don't think about with internal APIs, but publishing an API publicly, and not stepping back to think about what someone is going to need isn't acceptable.

Even with my experience, I still struggle to say exactly what needs to be said. There is no perfect introduction to a complex, often abstract set of APIs. However, you can invest a little more time thinking about what others will be needing, maybe run your portal by some external people for a little coherence testing. Most of all, just try to avoid being captain obvious, or captain assumption, and writing content that states the obvious while leaving out most of the critical details you take for granted. It really is the most important lessons we can take away from providing APIs, the ability for them to push us out of our boxes, from behind our firewalls, and have to engage with the real world.

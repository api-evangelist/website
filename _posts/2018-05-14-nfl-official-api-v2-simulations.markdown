---
published: true
layout: post
title: Sports Data API Simulations From SportRadar
date: 2018-05-14T12:00:00.000Z
tags:
  - API Evangelist
  - Sports
  - Virtualization
  - Sandboxes
  - Simulations
image: >-
  https://s3.amazonaws.com/kinlane-productions/sportradar/sportradar-simulations.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm a big fan of API sandboxes, labs, and other virtualization environments. [API sandboxes should be default in heavily regulated industries like banking](https://streamdata.io/blog/sandbox-default-feature-banking-apis/). I also support the virtualization of schema and data used across API operations, [like I am doing at the Department of Veterans Affairs (VA), with synthetic healthcare data](http://apievangelist.com/2018/05/01/synthetic-healthcare-records-for-your-api-using-synthea/). I'm very interested in anything that moves forward the [API virtualization](http://virtualization.apievangelist.com/) conversation, so I found [the live sporting API simulations over at SportRadar](https://developer.sportradar.com/files/indexFootball.html#nfl-official-api-v2-simulations) very interesting.

SportRadar's _"live simulations give you the opportunity to test your code against a simulation of live data before the preseason starts or any time! Our simulation system replays select completed games allowing you to view our API feeds as if they were happening live."_ Here are the details of their NFL Official API simulations that run every day:

- 11:00 am - Data is reset for the day’s simulations.
- 1:00 pm - PST week 1 games will run – Oakland at Houston, Detroit at Seattle, Miami at Pittsburgh, and New York at Green Bay
- 2:00 pm – PST week 2 games will run - Seattle at Atlanta, Houston at New England, Green Bay at Dallas, and Pittsburgh at Kansas City
- 3:00 pm – PST week 3 games will run – Green Bay at Atlanta and Pittsburgh at New England
- 4:00 pm – PST week 4 games will run – New England vs Atlanta

Providing a pretty compelling evolution in the concept API virtualization when it comes to event data, or data that will happen on a schedule. I wanted to write up this story to make sure I bookmarked this as part of my API virtualization research. If I don't write about it, it doesn't happen. As I'm working to include API sandboxes, lab environments, and other API virtualization approaches in my consulting, I'm keen to add new dimensions like API simulation, which provide great material for workshops, presentations, and talks.

I feel like ALL APIs should have some sort of sandbox to play in while developing. Not just heavily regulated industries, or those with sensitive production data and content. It can be stressful to have to develop against a live environment, and having a realistic sandbox, labs, and simulations which provide complete copies of production APIs, along with real world synthetic data can help developers be more successful in getting up and running. I'll keep profiling interesting approaches like this one out of SportRadar, and add to [my API virtualization research](http://virtualization.apievangelist.com/), helping round off my toolbox when it comes to helping API providers develop their sandbox environments.

---
published: true
layout: post
title: The Transit Feed API Is A Nice Blueprint For Your Home Grown API Project
date: 2018-01-03T13:00:00.000Z
tags:
  - API Evangelist
  - Transit
  - Portal
  - Documentation
  - Issues
image: >-
  https://s3.amazonaws.com/kinlane-productions/transit-feeds-api/transit-feeds-api-home-page.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/transit-feeds-api/transit-feeds-api-home-page.png" align="right" width="45%" style="padding:15px;" /></p>I look at a lot of APIs. When I land on the home page of an API portal, more often than not I am lost, confused, and unsure of what I need to do to get started. Us developers are very good at complexifying things, and making our APIs implementations as messy as our backends, and the API ideas in our heads. I suffer from this still, and I know what it takes to deliver a simple, useful API experience. It just takes time, resources, as well as knowledge to it properly, and simply. Oh, and caring. You have to care.

I am always on the hunt for good examples of simple API implementations that people can emulate, that aren't the API rockstars like Twilio and Stripe who have crazy amounts of resources at their disposal. One good example of a simple, useful, well presented API can be found with [the Transit Feeds API, which aggregates the feeds of many different transit providers around the world](http://transitfeeds.com/). When I land on the home page of Transit Feeds, I immediately know what is going on, and I go from home page to making my first API call in under 60 seconds--pretty impressive stuff, for a home grown API project.

While there are still some rough edges, Transit Feeds has all the hallmarks of a quality API implementation. Simple UI, with a clear message about what it does on the home, but most importantly an API that does one thing, and does it well--providing access to transit feeds. The site uses Github OAuth to allow me to instantly sign up and get my API key--which is how ALL APIs should work. You land on the portal, you immediately know what they do, and you have your keys in hand, making an API call, all without having to create yet another API developer account.

The Transit Feed API [provides an OpenAPI for their API](http://transitfeeds.com/api/transitfeeds-api.yaml), and uses it to drive [their Swagger UI API documentation](http://transitfeeds.com/api/swagger/). I wish the API documentation was embedded onto the docs page, but I'm just thankful they are using OpenAPI, and provide detailed interactive API documentations. Additionally, they have a great [updates page](http://transitfeeds.com/news), providing recent site, feed, and data updates across the project. To provide support they wisely [use Github Issues to help provide a feedback loop](https://transitfeeds.com/issues) with all their API consumers.

It isn't rocket surgery. Transit Feed makes it look easy. They provide a pretty simple blueprint that the rest of us can follow. They have all the essential building blocks, in an easy to understand, easy to get up and running format. They leverage OpenAPI and Github, which should be the default for any public API. I'd love to see some POST and PUT methods for the API, encouraging for more engagement with users, but as I said earlier, I'm pretty happy with what is there, and just hope that the project owners keep investing in the Transit Feed API. It provides a great example for me to use when working with transit data, but also gives me a home grown example of an API project that any of my readers could emulate.

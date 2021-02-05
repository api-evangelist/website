---
published: true
layout: post
title: A Blueprint For An Augmented Transit API
date: 2018-01-09T13:00:00.000Z
tags:
  - API Evangelist
  - Transit
  - Augmented
  - 511
  - 311
  - 911
  - City Government
image: >-
  https://s3.amazonaws.com/kinlane-productions/metrohero/metro-hero-dashboard.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/metrohero/metro-hero-dashboard.png" align="right" width="45%" style="padding: 15px" /></p>I'm working through research on the world of [transit APIs](http://transit.apievangelist.com) as part of my partnership with [Streamdata.io](http://apis.how/streamdata). From what I've gathered so far, the world of transit data and APIs is quite a mess, and there is a pretty significant opportunity to improve upon what already exists. In the course of my research, I stumbled across [MetroHero](https://dcmetrohero.com/), which is an application and API provider that operates on top of the [Washington Metropolitan Area Transit Authority](https://wmata.com/) data and API feeds.

I'm still working my way through their website, services, APIs, as well as talking with their team, but I'm fascinated with what they are doing, and wanted to think a little more about it before I talk with them this week. While their approach to improving upon WMATA applications is interesting, I think applying this way of thought to a government API is more interesting (surprise). [The MetroHero API is what I'd consider to be an augmented API](https://www.dcmetrohero.com/apis), operating on top of the WMATA API, and improving upon the data and services they make available about the Washington DC transit system.

The MetroHero API, taken directly from their developer portal, "are available for free. In return, we require the following":

- You must abide by WMATA's Transit Data Terms of Use; by using our APIs, you agree to these terms of service.
- Any data returned by or derived from data returned by our APIs must be freely available to all users of your application. Any paywalled application that utilizes our APIs must also provide a free tier with access to the same data returned by or derived from our APIs.
- Any data returned by or derived from data returned by our APIs must be prominently credited back to MetroHero. For example, if this data is being displayed to users on a website or in an application, MetroHero must always be visually credited wherever and whenever the data appears or is used.

The MetroHero API is not sanctioned by WMATA. The MetroHero team doesn't charge for their API, while also being very passionate about improving upon the WMATA APIs. I've been tuned into what MetroHero does since [I first wrote about WMATA's terms of service changes impacting them a while back](https://apievangelist.com/2017/11/30/licensing-over-dc-transit-data/), and I have been intrigued by an API that augments, and improve upon a government agency's API. This is a topic I've been thinking about since [my earlier frustrations with the federal government APIs I had been working on getting shutdown during the fall of 2013](http://apievangelist.com/2013/10/17/shutdown-of-government-open-data-and-apis-is-not-government-services-business-as-usual/). An experience that has pushed me to think more about ways in which we can improve upon existing government services using APIs.

I'm looking to craft a blueprint that reflects what MetroHero is already doing. Something that is forkable, and executable. I would like to see MetroHero be the default in communities. While transit is first in line, I'm envisioning a model that goes well beyond just transit, and into other 511 information like automobile traffic and incidents, then move into 311, and 911. I will be adding this blueprint to my [Adopta.Agency](http://adopta.agency/) project, and focusing it on the local level, rather than at the federal level. The sub-domain for the project will Transit.Adopta.Agency (not setup), then I'll add 511,911,311, and others later. I still have a lot of work to do on the transit portal blueprint, so first things first.

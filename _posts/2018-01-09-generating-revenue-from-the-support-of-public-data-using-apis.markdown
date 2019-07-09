---
published: true
layout: post
title: Generating Revenue From The Support Of Public Data Using APIs
date: 2018-01-09T10:00:00.000Z
tags:
  - API Evangelist
  - Public Data
  - Monetization
  - City Government
  - County Government
  - State Government
  - Federal Government
  - Public Data Monetization
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/machine-road_blue_circuit_4.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/machine-road_blue_circuit_4.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm exploring the different ways that public data access via APIs can be invested in, even with the opportunity for generating revenue, but without charging access to the data itself. I want public data to remain accessible, but in reality it costs money to provide access to public data, to refine, and evolve it. This is meant to be an exploration of how public data is invested in, not how you lock up public data, so please read everything before commenting, as every time I write about this subject, there are folks who blindly declare that ALL public data has to be free, no matter what. I agree (mostly), but there has to be commercial monetization opportunities around public data, otherwise it will never evolve, improve, be enriched, and in some cases available at all.

I am looking for opportunities for public data stewards / owners to generated much needed revenue, as well as commercial interests to come in and augment, and build upon what is already available--going beyond what cash and resource strapped data stewards / owners might be able to do on their own. Here are a couple of areas I'm documenting a little more right now.

- **Wholesale APIs** - Deploying, managing, and providing access to public data via APIs that are designed specifically for individual consumers. This could be deploying an API on AWS, Google, Azure, or other infrastructure provider, and providing private, or even I guess public access to the data. Delivering a personalized, customized, and performant public data API experience.
- **Real Time APIs** - Providing a proxied stream of data from one or many public data sources, going beyond what the data steward / owner is capable of delivering. Charging for the technology, not access to the data itself.
- **Cached** - Delivering a cached experience, so that when the primary source goes down, all API consumers are still able to get at historical, or other relevant data without interruption.
- **Transformation** - Providing access to the data but in a different format than the source can provide. This is where the line begins to get blurry because technically you would be charging for access to the data here, albeit in a different format. Maybe it could be done as a wholesale API, where you charge for the service, not the data?
- **Enriched** - Enriching public data, adding in additional data points, and other relevant data and content that makes it better. Another area things start to get blurry, because again, you are beginning to charge for access to the data. Maybe you would need to have a way to separate public, from the enrichment, I guess?

Those are just a couple of examples I'm looking thinking about. Most public data sources restrict the ability to charge for access to their data by any 3rd party--makes sense. In this particular exercise I'm looking at transit data, and how the overall data and API access experience can be improved upon. There are augmented APIs built upon public transit feeds, like we see from [MetroHero](https://dcmetrohero.com/), who is built upon [WMATA](https://wmata.com/). They clearly state that they are not sanctioned by WMATA, and could go away at any point, and make it known the data is freely available, and should remain that way downstream. I'm also looking at building upon [MTA transit feeds in NYC](http://datamine.mta.info/list-of-feeds), making the GTFS Realtime feeds available as SIRI feeds, but it is something that will cost me money, and I can't afford to just provide for access free, subsidizing other applications without some return.

I'd like to improve upon MTA transit feeds. Make them more usable, and available in a streaming format using [Streamdata.io](http://apis.how/streamdata). I can't do this in their current format. I can easily proxy their feeds, and transform into a simpler SIRI JSON feed, but then I'm expected to just make them freely available. I'm looking to see how I can do this as a wholesale API, as well as make available in a paid streaming format. I'm not charging for the data, I'm charging for the serving of it in real time? IDK. I am just exploring these thoughts right now. I get where all the concerns come into the picture around making money off public data, and limiting who gets access, however I really want public data to remain available, and improve--this is something that takes money, investment, and the ability to generate revenue.

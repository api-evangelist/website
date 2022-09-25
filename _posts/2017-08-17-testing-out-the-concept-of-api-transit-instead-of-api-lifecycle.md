---
published: true
layout: post
title: Testing Out The Concept Of API Transit Instead Of API Lifecycle
date: 2017-08-17T11:00:00.000Z
tags:
  - API Evangelist
  - Lifecycle
  - API Transit
image: >-
  https://s3.amazonaws.com/kinlane-productions/talks/november-2015/subway-map-15.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/talks/november-2015/subway-map-15.png" align="right" width="40%" style="padding: 15px;" /></p>It isn't often that I make up acronyms, terms, or phrases. [For a number of years I pushed forward the concept of API reciprocity](https://apievangelist.com/2013/02/27/merging-api-automation-and-interoperability-into-api-reciprocity/), but eventually conceded to the notion of integration platform as a service (iPaaS). Even with this failure I'm playing around with the evolution a new concept around how we map out our entire API operations, an area we commonly call the API lifecycle, but I'm exploring with calling it API transit.

When I think about the API lifecycle I am regularly reminded that it is something that is rarely a linear thing from define to deprecation, or even something that goes round and round in a circular format as the name lifecycle implies. This always brings me back to [my API subway map work](http://apievangelist.com/2014/12/01/my-turkey-holiday-project-a-subway-map-api/), with the development of [my subway map API](http://subway.map.apievangelist.com/), and [the keynote I gave on the subject at APIStrat in Austin](https://apievangelist.com/2015/11/29/the-api-lifecycle-my-talk-from-defrag-and-apistrat/). The subway map concept provides a pretty comprehensive way to map out the unlimited directions in which an API operations might take, and I'm looking to see if it can handle both the provider side needs, as well as that of the API consumer.

While I like the subway map analogy, I really like the more general concept of API transit. The concept of an APi subway map seems one dimensional, where API transit seems like it could handle multiple dimensions. I'm not sure there is a fit here, but I wanted to explore the definition of transit, as well as use the phrase in some API storytelling to test out a little bit, and see if it even is coherent. Ok, so what do my friends over at [the Oxford Dictionaries API](https://developer.oxforddictionaries.com/documentation) have to say on the subject?

etymologies:

- late Middle English (denoting passage from one place to another): from Latin transitus, from transire ‘go across’

definitions:

- the carrying of people or things from one place to another
- the conveyance of passengers on public transport.
- the action of passing through or across a place

I like the idea that API transit could be about the process of carrying people (users data) or things (anything digital) from one place to another -- with an API transmit map helping visualize this. I like that the map can be used by API providers as a guide for all the stops along the API lifecycle, but instead of being linear or circular, it can be all the above. Each API transit line could visualize an API lifecycle, and help API providers deliver consistently along each layer of API operations. The same maps, and lines can also be used to help API consumers navigate all API resources available via any API transit district.

"Denoting passage from one place to another" could be applied to training API providers about what is now called the API lifecycle, but could also be a series of journeys along pre-specified API transit lines, teaching them about concepts around API design, deployment, management, testing, and other aspects of API operations. These same lines can be used to guide each stop along the API lifecycle, helping act as an assembly line for delivering, maintaining, and even deprecating APIs. Once APIs make it to production, the same API transit map can be used to help engage with API consumers, helping move the people and their things from one place to another.

I'm not 100% sold on the concept, and it is something I'm not sure I will keep using. I do want to invest more time into my API subway map, which I'm going to rebrand as API transit map for the next wave of development. I have the API working, I just need to get the routing to work properly, so that it will lay down each of my API transit lines in a coherent way, allowing them to overlap, and work with and around each other. I have a model in my head for how I can use to help teach folks about key concepts of API operations from definition to deprecation. I also have a model for how it can guide the delivery and management of APIs, acting as a map and framework for managing API operations. I just don't have the API consumer portion of the equation. I'm guessing it will take me another couple years before this comes into focus for me, but I still enjoy working on the concept, and pushing it forward a little bit each year.

---
title: How Twitter Handles Sorting For Their API
date: 2017-05-24 15:00:00 Z
tags:
- Design
- Sorting
- Twitter
---

<p><a href="https://dev.twitter.com/ads/basics/sorting"><img src="https://s3.amazonaws.com/kinlane-productions/twitter/twitter-developer-sorting.png" align="right" width="40%" /></a></p>I was looking into some of the common approaches by API providers for sorting of data in API responses. I'm not in the business of finding the right answer, I am in the business of finding successful examples from APIs(brands) that people are familiar with--[I thought Twitter's page in their API documentation dedicated to sorting was worth noting](https://dev.twitter.com/ads/basics/sorting).

When you craft your Twitter API request you just append sort_by=[attribute name]-[asc/desc] where the attribute is a valid attribute that is returned in the JSON of your GET request. An example of this is using ?name-asc to sort by name alphabetically or ?name-desc to sort in reverse. Providing a pretty basic approach that API providers can consider when designing sort functionality in their API.

I'll be documenting all the approaches I find from known providers, developing a catalog of options for a variety of use cases. I'll also spend some time looking at how GraphQL tackles the problem, providing a much more holistic approach to managing data using APIs. When I go through my API design checklist each round, I like adding a variety of diverse tooling to it, based upon examples I find from the strongest API providers. [Healthy diversity in your API toolbox will be increasingly important](http://apievangelist.com/2017/03/10/focus-on-having-a-robust-and-diverse-api-toolbox/) to assist in tackling a variety of data, content, or algorithmic challenges.
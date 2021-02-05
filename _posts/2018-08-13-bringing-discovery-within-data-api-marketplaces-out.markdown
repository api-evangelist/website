---
published: true
layout: post
title: Bringing Discovery Within Data API Marketplaces Out Into The Open
date: 2018-08-13T09:00:00.000Z
tags:
  - API Evangelist
  - Data
  - Marketplaces
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/granaryfield_dali_three.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I spend time reviewing each wave of data API marketplaces as they emerge on the landscape every couple of years. There are a number of reasons why these data marketplaces exist, ranging from supporting government agencies, NGOs, or for commercial purposes. One of the most common elements of API-driven data marketplaces that frustrates me is when they don't do the hard work to expose the meta data around the databases, datasets, spreadsheets, and the raw data they are providing access to--making it very difficult to actually discover anything of interest.

You can see a couple examples of this with [mLab](https://docs.mlab.com/data-api/#list-databases), [World Health Organization](http://apps.who.int/gho/data/node.resources.api), [Data.World](https://apidocs.data.world/api), and others. While these platforms provide (sometimes) impressive ability to manage data stores, but they don't always do a good job exposing the meta data of their catalogs as part of the available APIs. Dynamically generating API endpoints, documentation, and other resources based upon the data that is being published to their platforms. Leaving developers to do the digging, and making the investment to understand what is available on a platform.

Some of the platforms I encounter obfuscate their data metadata on purpose, requiring developers to qualified before they get access to valuable resources. Most I think, just do not put themselves in the position of an API consumer who lands on their developer page, and doesn't know anything about an API. They understand the database, and the API, so it all makes sense to them, and they don't have any empathy for anyone else who isn't in the know. Which is a common trait of database centered people who speak in acronyms, and schema that they assume other people know, and do not spend much time thinking outside of that bubble.

I could make a career out of deploying APIs on top of other data marketplace APIs. Autogenerating a more accessible, indexable, intuitive layer on top of what they've already deployed. I regularly find a wealth of data that is accessible through an API interface, but will most likely never be found by anyone. Before most developers will ever make the investment to onboard with an API, they need to understand what valuable resources are available. I can imagine many developers stumble across these data marketplaces, spend about 15 minutes looking around, maybe sign up for a key, but then give up because of the overhead involved with actually understanding what data is actually available.

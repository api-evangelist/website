---
published: true
layout: post
title: An Opportunity Around Providing A Common OpenAPI Enum Catalog
date: 2018-02-21T12:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Documentation
image: 'https://s3.amazonaws.com/kinlane-productions/openapi/enums/bitcoin-pools.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/openapi/enums/bitcoin-pools.png" align="right" width="45%" style="padding: 15px;" /></p>I'm down in the details of the OpenAPI specification lately, working my way through hundreds of OpenAPI definitions, trying to once again make sense of the API landscape at scale. I'm working to prepare as many API path definitions as I possibly can to be runnable within one or two clicks. OpenAPI definitions, and Postman Collections are essential to making this happen, both of which require complete details on the request surface area for an API. I need to know everything about the path, as well as any headers, path, or query parameters that need to included. A significant aspect of this definition being complete includes default, and enum values being present.

If I can't quickly choose from a list of values, or run with a default value, when executing an API, the time to seeing a live response grows significantly. If I have to travel back to the HTML documentation, or worse, do some Googling before I can make an API call, I just went from seconds to potentially minutes or hours before I can see a real world API response. Additionally, if there are many potential values available for each API parameter, enums become critical building blocks to helping me understand all the dimensions of an API's surface area. Something that should have been considered as part of the API's design, but often just gets left as part of API documentation.

When playing with a Bitcoin API with the following path /blocks/{pool_name}, I need to the list of pools I can choose from. When looking to get a stock market quote from an API with the following path, /stock/{symbol}/quote, I need a list of all the ticker symbols. Having, or not having these enum values at documentation, and execute time, are essential. Many of these lists of values are so common, developers take them for granted. Assuming that API consumers just have them laying around, and really aren't worth including in documentation. You'd think we all have lists of states, countries, stock tickers, Bitcoin pools, and other data just laying around, but even as the API Evangelist, I often find myself coming up short.

All of this demonstrates a pretty significant opportunity for someone to create a Github hosted, searchable, forkable list of common OpenAPI enum lists. Providing an easy place for API providers, and API consumers to discover simple, or complex lists of values that should be present in API documentation, and included as part of all OpenAPIs. I recommend just publishing each enum JSON or YAML list as a Github Gist, and then publishing as a catalog via a simple Github Pages website. If I don't see something pop up in the next couple of months, I'll probably begin publishing something myself. However, I need another API related project like I need a hole in the head, so I'm holding off in hopes another hero or champion steps up and owns the enum portion of the growing OpenAPI conversation.

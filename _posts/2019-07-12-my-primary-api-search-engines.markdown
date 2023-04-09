---
published: true
layout: post
title: 'My Primary API Search Engines'
date: 2019-07-12T09:00:00.000Z
tags:
  - API Evangelist
  - Search
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/aws-s3-stories-crypto-machine-bletchley-copper-circuit.png
---

I am building out several prototypes for the moving parts of an API search engine I want to build, pushing my usage of APIs.json and OpenAPI, but also trying to improve how I define, store, index, and retrieve valuable data about thousands of APIs through a simple search interface. I’m breaking out the actual indexing and search into their own areas, with rating system being another separate dimension, but even before I get there I have to actually develop the primary engines for my search prototypes, feeding the indexes with fresh signals of where APIs exist across the online landscape. There isn’t an adequate search engine out there, so I’m determined to jumpstart the conversation with an API search engine of my own. Something that is different from what web search engines do, and tailored to the unique mess we’ve created within the API industry.

My index of APIs.json and OpenAPI definitions, even with a slick search interface is just a catalog, directory, or static index of a small piece of the APIs that are out there. I see a true API search engine as three parts

1. The Humans Searching for APIs - Providing humans with web application to search for new and familiar APIs.
2. The Search Engine Searching For APIs - Ensuring that the search engine is regularly searching for new APIs.
3. Other Systems Searching For APIs - Providing an API for other systems to search for new and familiar APIs.

Without the ability for the search engine to actually seek out new APIs, it isn’t a search engine in my opinion—-it is a search application. Without an API for searching for APIs, in my opinion, it isn’t an API search engine. It takes all three of these areas to make an application a true API search engine, otherwise we just have another catalog, directory, marketplace, or whatever you want to call it.

To help me put the engine into my API search engine, I’m starting with a handful of sources I’ve cultivated over the last five years studying the API industry. Providing me with some seriously rich sources of information when it comes to identifying new APIs:

- **GitHub Code Search API** - I have a vocabulary I use for uncovering artifacts that provide clues to where APIs exist. I can also expand this search to topics, repos, and other dimensions of GitHub search, but I’m going to make sure I’m exhausting and optimizing core search for all I can before I move on.  GitHub provides me with a handful of nuggets when it comes to finding APIs:
    - **Swagger** - Machine readable JSON and YAML API definitions.
    - **OpenAPI** - Machine readable JSON and YAML API definitions.
    - **Postman** - Machine readable JSON API definitions.
    - **API Blueprint** - Machine readable markdown definitions.
    - **RAML** - Machine readable YAML definitions.
    - **HAR** - Machine readable traffic snapshots.
    - **Domains** - Domains doing interesting things with APIs.
    - **People** - People doing interesting things with APIs.
- **Bing Web Search API** - I use my vocabulary to uncover domains and artifacts that provide clues to where APIs exist. Unlike GitHub, I have to pay for these API calls, so I’m being much more careful about how I spider, and coherently defining the vocabulary I use to uncover this landscape.  Bing provides me with a handful of nuggets when it comes to finding APIs:
    - **Domains** - A look into many different domains who are talking APIs in specific verticals.
    - **GitHub** - I find that Bing has some interesting indexes of GitHub — wondering how this will evolve.
- **Twitter** - I use my vocabulary to identify new domains where people are talking about APIs, and additional signs of APIs.
    - **Domains** - A look into many different domains who are talking APIs in specific verticals.
    - **People** - People doing interesting things with APIs.
- **Domain** - I have an exhaustive list of domains to spider for API artifacts, autogenerating OpenAPI index along the way.
    - **URLs** - I look for a handful of valuable URLs for use as part of my index.
        - **Twitter** - Their Twitter accounts.
        - **GitHub** - Their GitHub accounts.
        - **LinkedIn** - Their LinkedIn accounts.
        - **Feeds** - Their Atom and RSS feeds.
        - **Definitions** - Any API definitions I can find.
        - **Documentation** - Where their documentation is.
        - **Other Links** - I have a long list of other links I look for

These four areas represent the primary engines for my API search engine. I currently have these engines running on AWS, processing GitHub and Bing searches, and I’m currently refining my existing Twitter, and relevant domain harvesting engines. While Bing and GitHub are harvesting API signals, and indexing API artifacts like OpenAPI, Postman, and others, I’m going to overhaul my Twitter and domain approaches. Twitter has always been a treasure trove of API signals, but like on GitHub, it is getting harder to obtain these API signals at scale—-as their value increases, things are getting tighter with API access. Also, running a proper domain harvesting campaign across thousands of domains isn’t easy, and will require some refactoring to do at the scale I need for this type of effort.

While I have two of these up and running, indexing new APIs, I still have a significant amount of work to invest in each engine. What I have now is purely of prototype. It will take several cycles until I get each engine performing as desired, and then I’m expecting ongoing tweaks, adjustments, and refinements to be made daily, weekly, and monthly to get the results I’m looking for. There are many areas of deficiency in the API sector that bother me, but not having a simple way to search for new and existing APIs is one are I cannot tolerate any longer. I am happy that ProgrammableWeb has been around all these years, but they haven’t moved the needle in the right way. I also get why people do API marketplaces, but I’m afraid they aren’t moving the needle in a positive direction either. I’d say that APIs.Guru (https://apis.guru/openapi-directory/) is the most progressive vision when it comes to API search in the last decade--with all the innovation supposedly going on, that is just sad. I am guessing that venture capital does not always equal meaningful things we need will get built.

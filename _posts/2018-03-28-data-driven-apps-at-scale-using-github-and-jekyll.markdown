---
published: true
layout: post
title: Data Driven Apps At Scale Using Github And Jekyll
date: 2018-03-28T09:00:00.000Z
tags:
  - API Evangelist
  - Jekyll
  - Github
  - Discovery
  - Definitions
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/43_113_800_500_0_max_0_-5_-5.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I've pushed my Github driven, Jekyll fueled, application delivery process to a new levels the last couple of weeks. I've been investing more cycles into [my API Stack work](http://theapistack.com/), as I build out an [API Gallery for Streamdata.io](http://api.gallery.streamdata.io/). All of my work as the API Evangelist has long lived as independent Github repositories, with a JSON or YAML core that drives the static Jekyll UI for my websites, applications, and API developer portals. Designed to be independent, data and API driven micro-solutions to some related aspect of my API research. I'm just turning up the volume on what already exists.

I'm taking this to the next level with my approach to API discovery. API Stack used to be a single Github repository with huge number of APIs.json and OpenAPI definitions, but after hitting the ceiling with the size of the repository, I've begun to shard projects by entity, topic, and collection. So far I have [285 entities](https://github.com/api-stack-providers), with 9850 API paths, [spanning 397 topics](https://github.com/api-stack-topics). Each entity, and topic exists within its own Github repository, acting as an individual set of API definitions, including an OpenAPI, Postman Collection, and APIs.json index. Allowing me to move forward each API definition for an entity independently, and begin aggregating APIs into interesting collections by topic, industry, or other relevant area.

There is no backend database for these projects. Well, there is a central system I use to help me orchestrate things, but each project is standalone, with everything it needs stored in the Github repository. It is something that took some engineering, and time to setup and first, but now that it is setup, managing it is actually pretty easy. The approach has also allowing me to scale it without any additional performance issues. Each entity I add becomes its own repo, and unless I hit some magic number for the number of repositories I can have within an organization, I should be able to scale to several thousand repos pretty quickly. Doing the same thing for topics, and other types of collections I'm aggregating APIs into.

Each entity repository has the OpenAPI, and Postman Collection for its provider. I'm also breaking out each individual API path into it's own OpenAPI definition, and considering doing the same for Postman Collections--distilling things down to its smallest possible unit of compute. The APIs.json for each repository indexes the OpenAPI, Postman collection, as well as the other elements of API operations like documentation, blog, Twitter, and Github accounts. In the future I will be publishing other machine readable artifacts here including details on plans and pricing, terms of service, monitoring, performance, and other aspects of the ranking and profiling of the API sector that I do.

I'm getting ready to softly launch Streamdata.io's API Gallery, but my API Stack work will continue to be my workbench for this type of API discovery work. I'll keep harvesting, scraping, and profiling APIs and their operations, and as they come into focus I'll sync with Streamdata.io's API Gallery, and look at how I can help Postman with their API Network, APIs.guru with their directory, as well as other API aggregation and integration platforms like AnyAPI, APIDeck, and others. I'm just getting to the point where I feel like things are working as I want them to, and are ready for me to shift into higher gear. There are still a lot of issues with individual entities, and topics, but the process is working well--I just need to spend more time refining the API definitions themselves, and work on syncing with other efforts in the space.

Right now I'm heavily using the Github API to make all this work, but I'm probably going to switch to relying on Git for the heaviest lifting. However, as a 30 year database person, I have admit that I am rather enjoying the scope of delivering JSON and YAML driven API-driven continuous deployment and integration projects like this that have a machine readable layer, but also a UI layer for humans to put to use. It provides me a with a very API way of driving how I profile APIs, quantify what it is they do, and begin to rank and make sense of the growing API landscape. Continuing with my way of doing things out in the open, while hopefully providing more value to the API discovery conversation, in an OpenAPI and Postman Collection driven API universe.

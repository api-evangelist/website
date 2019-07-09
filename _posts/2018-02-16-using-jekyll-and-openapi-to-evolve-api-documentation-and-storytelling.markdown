---
published: true
layout: post
title: Using Jekyll And OpenAPI To Evolve My API Documentation And Storytelling
date: 2018-02-16T09:00:00.000Z
tags:
  - API Evangelist
  - Documentation
  - Jekyll
  - Communication
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/68_158_800_500_0_max_0_1_-1.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/68_158_800_500_0_max_0_1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm reworking my API Stack work as independent sets of [Jekyll collections](https://jekyllrb.com/docs/collections/). Historically I just dumped all [APIs.json](http://apisjson.org/), and OpenAPIs into the central data folder, and grouped them into folders by company name. Now I am breaking them out into tag based collections, using a similar structure. Further evolving how I document and tell stories using each API. I have been published a single OpenAPI for each platform, but now I'm publishing a separate OpenAPI for each API path--we will see where this goes, it might ultimately end up biting me in the ass. I'm doing this because I want to be able to talk about a single API path, and provide a definition that can be viewed, interpreted, and executed against, independent of the other paths--Jekyll+OpenAPI is helping me accomplish this.

With each API provider possessing its own APIs.json index, and each API path having its own OpenAPI definition, I'm able to mix up how I document and tell stories around these APIs. I can list them by API provider, or by individual API path. I can filter based upon tags, and provide execute-time links that reference each individual unit of API. I have separate JavaScript functions that can be referenced if the API path is GET, POST, or PUT. I can even inherit other relevant links like API sign up or terms of service as part of its documentation. I can reference all of this as part of larger documentation, or within blog posts, and other pages throughout the website--which will be refreshed whenever I update the OpenAPI definition.

If you aren't familiar with how Jekyll works. It is a static content solution, that allows you do develop collections. You can put CSV, JSON, or YAML into these collections (folders), and they become objects you can reference using Liquid syntax. So if I put Twitter's APIs.json, and OpenAPI into a folder within my social collection, I can reference as site.social.twitter which is the APIs.json for Twitter's entire API operations, and I can reference individual APIs as site.social.twitter.search for the individual OpenAPI defining the Twitter search API path. This decouples API documentation for me, and allows me to not just document APIs, but tell stories with  API definitions, making my API portals much more interactive, and hopefully engaging.

I just got my API stack approach refreshed using this new format. Now I just need to go through all my APIs and rebuild the underlying Github repository. I have thousands of APIs that I track on, and I'm curious how this approach holds up at scale. While [API Stack](http://theapistack.com) is a single repository, I can essentially publish any collection of APIs I desire to any of the hundreds of repositories that make up the API Evangelist network. Allowing me to seamless tell stories using the technical details of API operations, and the individual API resources they serve up. Further evolving how I tell stories around the APIs I'm tracking on. While my API documentation has always been interactive, I think this newer, more modular approach, reflects the value each unit of value an API brings to the table, rather than just looking to document all the APIs a provider possesses.

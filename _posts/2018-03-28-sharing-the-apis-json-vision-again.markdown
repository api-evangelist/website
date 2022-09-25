---
published: true
layout: post
title: Sharing The APIs.json Vision Again
date: 2018-03-28T13:00:00.000Z
tags:
  - API Evangelist
  - Discovery
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/apis-json/apis-json-home-page-2018.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I know many folks in the API sector don't know about [APIs.json](http://apisjson.org/format.html), and if they do they often think it is yet another API definition format, competing wit OpenAPI, Postman Collections, and others. So, I want to take a moment to share the vision again, and maybe convert one or two more folks to the possibilities around having a machine readable format for the entire operations. This is where APIs.json elevates the conversation, is it isn't just about defining an API, it is about defining API operations, looking to make things more discoverable, and executable by default.

[APIs.json](http://apisjson.org/format.html) is a JSON format, as the name implies, but admittedly a bad name, as I've already started created APIs.yaml editions, which defines the entire API operations, not just any single API. It starts with the basics of the API providers, with: name, description, image, tags, created, and modified. Then it has a collection for defining one or many actual APIs. Repeating the need for a name, description, image, and tags, but this time for each API--admittedly this might be redundant in many cases. Each API also has a humanURL and baseURL for each API, providing two key links that developers will need. After that, we start getting to the meat of APIs.json, with the properties collection.

The properties collection is an array of URLs and types, which can point to many different building blocks of API operations. Common elements that should be present with every API provider like:

- **Documentation** - URL to the API documentation.
- **Plans & Pricing** - Landing page for the API tiers.
- **Terms of Service** - Where do you find the legal department.
- **Sign Up** - How do you sign up for an API.

These elements are often times meant for humans, but the goal of APIs.json is to also provide machine readable URLs of common building blocks, including:

- **[OpenAPI](https://www.openapis.org/)** - Where do you find the OpenAPI definition?
- **[Postman Collection](https://www.getpostman.com/docs/v6/postman/collections/creating_collections)** - Is there a Postman Collection available?
- **[API Commons](http://apicommons.org/)** - What is the licensing for the API?

APIs.json isn't meant to compete with these existing API definition formats, it is designed to index them. It is meant to provide a complete index of the human, and machine readable components required to operate an API platform. The properties collection is meant to index all of these, but also work to move the human elements towards being more machine readable, as we've seen happen with documentation and OpenAPI, as well as what we achieved with licensing and [API Commons](http://apicommons.org/). Ultimately we'd like to see all the essential aspects of API integration become machine readable--elements like:

- **Pricing** - A machine readable breakdown of pricing, tiers, and limits.
- **Terms of Services** - Breaking down TOS so they can be interpreted by a machine.
- **Signup** - Making signup for APIs something that is automated.

Yes, this will all take a significant amount of work, just like indexing APIs, and making them more discoverable, but it has to be done. Currently, [I'm just looking to keep APIs.json, OpenAPI, and Postman Collection definitions up to date across thousands of Github repositories included in my API Stack work](http://theapistack.com/). As this work stabilizes, and continues to come into focus, I'll be pushing forward with better defining signup and pricing across API providers, and then get to work on terms of service. [We need all of these elements of API operations to become machine readable and executable as part of the discovery process](http://apievangelist.com/2018/02/28/what-we-need-to-be-machine-readable-at-api-run-time/), otherwise this shit will never scale.

That is a fresh look at the [APIs.json](http://apisjson.org/format.html) vision. There is more to it than just indexing API operations and making them more discoverable. I am also using to build different topical, and industry level collections, which you can reference as part of the APIs.json includes property. But, we'll save that for another story. In the mean time, I'm going to get back to work profiling APIs using APIsjson, and publishing them to my API Stack organization(s), and syndicating them out to other partners like APIs.io, Streamdata.io, and Postman Network. If you'd like to know more about APIs.json, feel free to reach out, and I'll make sure and work on more stories around how I am using the API discovery format.

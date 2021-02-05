---
published: true
layout: post
title: The Importance Of Tags In OpenAPI Definitions For Machine Learning APIs
date: 2018-03-12T14:00:00.000Z
tags:
  - API Evangelist
  - Machine Learning
  - Definitions
  - Discovery
image: >-
  https://s3.amazonaws.com/kinlane-productions/contrafabulists/machine+learning.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I am profiling APIs as part of my partnership with [Streamdata.io](http://streamdata.io), and my continued [API Stack](http://theapistack.com) work. As part of my work, I am creating OpenAPI, Postman Collections, and APIs.json indexes for APIs in a variety of business sectors, and as I'm finishing up the profile for [ParallelDots machine learning APIs](https://docs.paralleldots.com/), I am struck (again) by the importance of tags within OpenAPI definitions when it comes to defining what any API does, and something that will have significant effects on the growing machine learning, and artificial intelligence space.

While profiling ParallelDots, I had to generate the OpenAPI definition from the Postman Collection they provide, which was void of any tags. I went through the handful of API paths, manually adding tags for each of the machine learning resources. I'm adding tags like sentiment, emotions, semantics, taxonomy, and classification, to each path. Trying to capture what resources were available, allowing for the discovery, filtering, and execution of each individual machine learning model being exposed using a simple web API. While the summary and description explain what each API does to developers, the tags are really the precise meaning in a machine readable context.

In the fast moving, abstract realm of machine learning, and artificial intelligence it can be difficult to truly understand what each API does, or doesn't do. I struggle with it, and I'm pretty well versed in what is possible and not possible with machine learning. Precise tagging provide us with a single definition of what each machine learning API does, setting a baseline of understanding for putting ML APIs to work. Something that if I consistently apply across all of the machine learning APIs I'm profiling, I can can begin honing and dialing in my catalog of valuable API resources, and begin creating a coherent map of what is possible with machine learning APIs--helping ground us in this often hyped realm.

Once I have a map of the machine learning landscape established, I want to continue evolving my API ranking strategy to apply specifically to machine learning models being exposed via APIs. Not just understanding what they do, but also the quality of what they do. Are the machine algorithms delivering as advertised? Which APIs have a consistent track record in not just the reliability of the APIs, but also the reliability of the responses. Further bringing clarity to the fast moving, venture capital fueled, magical, mystical realm of artificial intelligence. Helping average business consumers better understand which APIs they can depend on, and which ones they might want to avoid.

I'm hoping my API Stack profiling will encourage more API providers to begin doing the heavy lifting of creating OpenAPI definitions, complete with tags themselves. We are always going to need the participation of the community to help make sure they are complete, and as meaningful as they can, but API providers will need to step up and invest in the process whenever possible. As the machine learning and artificial intelligence realms mature, we are going to need a meaningful vocabulary for describing what it is they do, and a ranking system for sorting out the good, the mediocre, and the bad. We'll need all of this to be contained within the machine readable definitions we are using for discovery, and at runtime, allowing us to automate more efficiently using machine learning APIs.

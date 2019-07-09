---
published: true
layout: post
title: Including API Dependencies Within Your API Definition
date: 2017-08-04T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Dependencies
---
[I was learning about Pivio, a discovery specification for microservices the other day, and found their focus on microservice dependency to be pretty interesting](http://apievangelist.com/2017/08/03/microservice-discovery-using-pivio/). API dependencies has been an area I have found myself increasingly thinking about, as well as tracking on in my API research. I'm pretty close to publishing a project dedicated to understanding API, and microservices dependencies, which would overlap with containers, serverless, and other aspects of the API lifecycle that are all about breaking down the monolith.

Each service definition using Pivio has a depends_on object, which allows for defining both internal and external service dependencies. Here is a snippet from a sample Pivio document to help articulate this interesting feature:

<script src="https://gist.github.com/kinlane/728a92155bc507a526182b3b767a73d1.js"></script>

This is where you can start connecting the cords between all of your services, something that is applicable to any APIs, whether you've drank the microservices kool-aid or not. I find it interesting that Pivio has internal, and external. I'd love to see an OpenAPI linked off each of the services it depends on. I also am fascinated with the first question for external, why? What a great first question for any dependency--it should also be available for internal services as well. Every API provider should be inquiring why a dependency exist whenever possible, and having it quantified in this way just opens up more chances for this question to get asked.

Seeing dependencies quantified in Pivio makes me happy. It has been something I've wanted to reflect in [APIs.json](http://apisjson.org) for some time now. Currently, I do not know of any way to quantify the relationship between APIs, and Pivio provides a glimpse at one possible way we might be able to map this world out. [I have been learning more about Cytoscape, a network data integration, analysis, and visualization framework](http://www.cytoscape.org/). Having a machine readable API dependencies definition would allow me to create a network visualization of any API or microservices discovery catalog. It wouldn't take much work at all to map out API and microservice dependencies at the internal and external levels, further helping to quantify the platforms we operate.

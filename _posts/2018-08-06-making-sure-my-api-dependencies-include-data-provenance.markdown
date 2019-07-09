---
published: true
layout: post
title: Making Sure My API Dependencies Include Data Provenance
date: 2018-08-06T13:00:00.000Z
tags:
  - API Evangelist
  - Dependencies
  - Data
  - Provenance
  - Observability
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/23_19_800_500_0_max_0_-5_-1.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>[I am publishing a new API for locations](http://locations.apievangelist.com/#Updates). I am tired of needing some of the same location based resources across projects, and not having a simple, standardized API I can depend on. So I got to work finding the most accurate and complete data set I could find of cities, regions, and countries. I settled on using the complete, and easy to use [countries-regions-cities](https://github.com/prograhammer/countries-regions-cities) project by [David Graham](https://github.com/prograhammer)--providing a straightforward SQL script I can use as the seed for my locations API database.

After crafting an API for this database using AWS API Gateway and Lambda, and working my way down [my API checklist](https://apievangelist.com/2018/07/12/my-api-lifecycle-checklist-and-scorecard/), it occurred to me that I wanted to include David Graham's work as one of the project dependencies. Giving him attribution, while honestly acknowledging my project's dependency on the data he provided. I'm working hard to include all dependencies within each of the microservices that I'm publishing, being mindful of every data, code, and human dependency that exists behind each service I deliver. Even if I don't rely on regular updates from them, I still want to acknowledge their contribution, and consider attribution as one layer of my API dependency discussion.

Having a dependency section of my API checklist has helped me evolve how I think about defining the dependencies my services have. I initially began tracking all other services that my microservices were dependent on, but then I quickly began adding details about the other software, data, and people the service depends on as well. I'm also pulling together a machine readable definition for tracking on my microservice dependencies. It will be something I include in the API discovery (APIs.json) document for each service, alongside the OpenAPI, and other specifications. Allowing me to track on the dependencies (and attribution) for all of my APIs, and API related artifacts that I am producing on a regular basis. Providing data provenance for each of my services, documenting the origins of all the data I'm using across my services, and making accessible via an API.

For me, having the data provenance behind each service provides me with a nice clean inventory of all my suppliers. Understanding the data, services, open source code, and people I depend on to deliver a service is important to helping me make sense of my operations. For the people behind the data, services, and open source code I depend on it helps provide attribution, and showcase their valuable contribution to the services I offer. For partner and 3rd party consumers of my services, being observable about the dependencies that exist behind a service they are depending on, helps them make much more educated decisions around which services they put to work, and bake into their applications and systems. In the end, everyone is better off if I invest in data provenance as part of my wider API dependency efforts.
